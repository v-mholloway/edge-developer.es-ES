---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: cfb99be772170ee458fa252133f90240d75af3db
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878053"
---
# 0.8.355: IWebView2WebView3 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface IWebView2WebView3
  : public IWebView2WebView
```

Funcionalidad adicional implementada por el objeto WebView principal.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Detener](#stop) | Detenga todas las navegaciones y las búsquedas de recursos pendientes.
[add_NewWindowRequested](#add_newwindowrequested) | Agregue un controlador de eventos para el evento NewWindowRequested.
[remove_NewWindowRequested](#remove_newwindowrequested) | Quitar un controlador de eventos agregado previamente con add_NewWindowRequested.
[add_DocumentTitleChanged](#add_documenttitlechanged) | Agregue un controlador de eventos para el evento DocumentTitleChanged.
[remove_DocumentTitleChanged](#remove_documenttitlechanged) | Quitar un controlador de eventos agregado previamente con add_DocumentTitleChanged.
[get_DocumentTitle](#get_documenttitle) | Título del documento de nivel superior actual.

Puede ejecutar QueryInterface para esta interfaz desde el objeto que implementa [IWebView2WebView](IWebView2WebView.md). Para obtener más información, consulta la interfaz de [IWebView2WebView](IWebView2WebView.md) .

## Miembros

#### Detener 

Detenga todas las navegaciones y las búsquedas de recursos pendientes.

> [HRESULT público](#stop)()

#### add_NewWindowRequested 

Agregue un controlador de eventos para el evento NewWindowRequested.

> [add_NewWindowRequested](#add_newwindowrequested)de HRESULT público ([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Se desencadena cuando el contenido de la vista en WebView solicita abrir una nueva ventana, por ejemplo, a través de window. Open. La aplicación puede pasar una vista previa de destino que se considerará la ventana abierta.

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<IWebView2NewWindowRequestedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<IWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));

                auto newAppWindow = new AppWindow(L"");
                newAppWindow->m_onWebViewFirstInitialized = [args, deferral, newAppWindow]() {
                    CHECK_FAILURE(args->put_NewWindow(newAppWindow->m_webView.get()));
                    CHECK_FAILURE(args->put_Handled(TRUE));
                    CHECK_FAILURE(deferral->Complete());
                };

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_NewWindowRequested 

Quitar un controlador de eventos agregado previamente con add_NewWindowRequested.

> [remove_NewWindowRequested](#remove_newwindowrequested)de HRESULT público (token EventRegistrationToken)

#### add_DocumentTitleChanged 

Agregue un controlador de eventos para el evento DocumentTitleChanged.

> [add_DocumentTitleChanged](#add_documenttitlechanged)de HRESULT público ([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

El evento se desencadena cuando la propiedad DocumentTitle de WebView cambia y se puede activar antes o después del evento NavigationCompleted.

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<IWebView2DocumentTitleChangedEventHandler>(
            [this](IWebView2WebView3* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### remove_DocumentTitleChanged 

Quitar un controlador de eventos agregado previamente con add_DocumentTitleChanged.

> [remove_DocumentTitleChanged](#remove_documenttitlechanged)de HRESULT público (token EventRegistrationToken)

#### get_DocumentTitle 

Título del documento de nivel superior actual.

> [get_DocumentTitleción](#get_documenttitle)HRESULT pública (título LPWStr *)

Si el documento no tiene un título explícito o no está vacío, de lo contrario, se usará un valor predeterminado que puede o no coincidir con el URI del documento.


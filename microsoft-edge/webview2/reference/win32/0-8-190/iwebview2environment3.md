---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: d16a12aae823c48b7dd4b0b5e8225cdd40c1dafc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878529"
---
# 0.8.355: IWebView2Environment3 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface IWebView2Environment3
  : public IWebView2Environment2
```

Funcionalidad adicional implementada por el objeto de entorno.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[add_NewVersionAvailable](#add_newversionavailable) | El evento NewVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.
[remove_NewVersionAvailable](#remove_newversionavailable) | Quitar un controlador de eventos agregado previamente con add_NewVersionAvailable.

Para obtener más información, consulta la interfaz de [IWebView2Environment](IWebView2Environment.md) . Puede ejecutar QueryInterface para esta interfaz desde el objeto que implementa [IWebView2Environment](IWebView2Environment.md).

## Miembros

#### add_NewVersionAvailable 

El evento NewVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.

> [add_NewVersionAvailable](#add_newversionavailable)de HRESULT público ([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) * EventHandler, EventRegistrationToken * token)

Para usar la versión más reciente del explorador, debes crear un nuevo [IWebView2Environment](IWebView2Environment.md) y [IWebView2WebView](IWebView2WebView.md). El evento solo se desencadenará para la nueva versión desde el mismo canal de borde desde el que se está ejecutando el código. Cuando no se esté ejecutando con Edge instalado, no se desencadenará ningún evento.

Dado que una carpeta de datos de usuario solo se puede usar en un proceso del explorador a la vez, si desea usar la misma carpeta datos de usuario en las vistas web con la nueva versión del explorador, debe cerrar primero los [IWebView2Environment](IWebView2Environment.md) y IWebView2WebViews que usan la versión anterior del explorador. O simplemente pide al usuario que reinicie la aplicación.

```cpp
    // After the environment is successfully created,
    // register a handler for the NewVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewVersionAvailable(
        Callback<IWebView2NewVersionAvailableEventHandler>(
            [this](IWebView2Environment* sender, IWebView2NewVersionAvailableEventArgs* args)
                -> HRESULT {
                // Get the version value from args
                wil::unique_cotaskmem_string newVersion;
                CHECK_FAILURE(args->get_NewVersion(&newVersion));
                std::wstring message = L"We detected there is a new version for the browser.";
                message += L"\n\nVersion number: ";
                message += newVersion.get();
                message += L"\n\n";
                if (m_webView)
                {
                    message += L"Do you want to restart the app? \n\n";
                    message += L"Click No if you only want to re-create the webviews. \n";
                    message += L"Click Cancel for no action. \n";
                }
                int response = MessageBox(
                    m_mainWindow, message.c_str(), L"New available version",
                    m_webView ? MB_YESNOCANCEL : MB_OK);

                if (response == IDYES)
                {
                    RestartApp();
                }
                else if (response == IDNO)
                {
                    ReinitializeWebViewWithNewBrowser();
                }
                else
                {
                    // do nothing
                }

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_NewVersionAvailable 

Quitar un controlador de eventos agregado previamente con add_NewVersionAvailable.

> [remove_NewVersionAvailable](#remove_newversionavailable)de HRESULT público (token EventRegistrationToken)


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 06cff80d1c0dd25ab0753edd521f2c04b49816c3
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878011"
---
# 0.8.355: IWebView2WebView5 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface IWebView2WebView5
  : public IWebView2WebView4
```

Funcionalidad adicional implementada por el objeto WebView principal.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged) | Notifica cuando cambia la propiedad ContainsFullScreenElement.
[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged) | Quitar un controlador de eventos agregado previamente con el método de evento add_ correspondiente.
[get_ContainsFullScreenElement](#get_containsfullscreenelement) | Indica si WebView contiene un elemento HTML de pantalla completa.
[add_WebResourceRequested](#add_webresourcerequested) | Agregue un controlador de eventos para el evento WebResourceRequested.
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.

Puede ejecutar QueryInterface para esta interfaz desde el objeto que implementa [IWebView2WebView](IWebView2WebView.md). Para obtener más información, consulta la interfaz de [IWebView2WebView](IWebView2WebView.md) .

## Miembros

#### add_ContainsFullScreenElementChanged 

Notifica cuando cambia la propiedad ContainsFullScreenElement.

> [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)de HRESULT público ([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Esto significa que un elemento HTML dentro de la vista de WebView está escribiendo Fullscreen en el tamaño de WebView o saliendo de pantalla completa. Este evento es útil cuando, por ejemplo, un elemento de vídeo solicita la pantalla completa. El agente de escucha de ContainsFullScreenElementChanged puede cambiar el tamaño de la vista en WebView en respuesta.

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<IWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](IWebView2WebView5* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
                    if (m_containsFullscreenElement)
                    {
                        EnterFullScreen();
                    }
                    else
                    {
                        ExitFullScreen();
                    }
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_ContainsFullScreenElementChanged 

Quitar un controlador de eventos agregado previamente con el método de evento add_ correspondiente.

> [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)de HRESULT público (token EventRegistrationToken)

#### get_ContainsFullScreenElement 

Indica si WebView contiene un elemento HTML de pantalla completa.

> [get_ContainsFullScreenElement](#get_containsfullscreenelement)de HRESULT público (bool * ContainsFullScreenElement)

#### add_WebResourceRequested 

Agregue un controlador de eventos para el evento WebResourceRequested.

> [add_WebResourceRequested](#add_webresourcerequested)de HRESULT público ([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Se desencadena cuando WebView realiza una solicitud HTTP a una dirección URL y un filtro de contexto de recursos coincidentes que se agregaron con AddWebResourceRequestedFilter. Debe agregar al menos un filtro para que se active el evento.

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<IWebView2WebResourceRequestedEventHandler>(
                    [this](
                        IWebView2WebView* sender,
                        IWebView2WebResourceRequestedEventArgs* args) {
                        wil::com_ptr<IWebView2WebResourceRequestedEventArgs2>
                            webResourceEventArgs2;
                        args->QueryInterface(IID_PPV_ARGS(&webResourceEventArgs2));
                        WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            webResourceEventArgs2->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<IWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### AddWebResourceRequestedFilter 

Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.

> [ADDWEBRESOURCEREQUESTEDFILTER](#addwebresourcerequestedfilter)HRESULT público (LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)

El parámetro URI puede ser una cadena comodín (' ': cero o más, '? ': exactamente uno). nullptr es equivalente a L "". Consulta WEBVIEW2_WEB_RESOURCE_CONTEXT enum para obtener una descripción de los filtros de contexto de recursos.

#### RemoveWebResourceRequestedFilter 

Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.

> [REMOVEWEBRESOURCEREQUESTEDFILTER](#removewebresourcerequestedfilter)HRESULT público (LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)

Si se agregó el mismo filtro varias veces, tendrá que quitarlo tantas veces como se agregara para que la eliminación sea efectiva. Devuelve E_INVALIDARG para un filtro que nunca se ha agregado.


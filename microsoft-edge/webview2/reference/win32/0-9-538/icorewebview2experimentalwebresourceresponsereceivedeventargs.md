---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
ms.openlocfilehash: 056667b4ee1995763fee81c8d7a9be31496f7f3e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886561"
---
# interfaz ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento WebResourceResponseReceived.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Request](#get_request) | Objeto de solicitud de recursos Web. Se omitirán todas las modificaciones realizadas a este objeto.
[get_Response](#get_response) | Objeto de respuesta de recursos Web.
[PopulateResponseContent](#populateresponsecontent) | Método Async para solicitar la secuencia de contenido de la respuesta.

Contendrá la solicitud a medida que se envió y la respuesta a medida que se recibió. Nota: para obtener la secuencia de contenido de la respuesta, primero llame a PopulateResponseContent y espere a que se complete la llamada asincrónica, de lo contrario el objeto de la secuencia de contenido devuelto será null.

## Miembros

#### get_Request 

Objeto de solicitud de recursos Web. Se omitirán todas las modificaciones realizadas a este objeto.

> [get_Request](#get_request)de HRESULT público (solicitud ICoreWebView2WebResourceRequest * *)

#### get_Response 

Objeto de respuesta de recursos Web.

> [get_Response](#get_response)de HRESULT público (respuesta de ICoreWebView2WebResourceResponse * *)

Se omitirán todas las modificaciones realizadas a este objeto.

#### PopulateResponseContent 

Método Async para solicitar la secuencia de contenido de la respuesta.

> [PopulateResponseContent](#populateresponsecontent)(controlador[ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) *) Public HRESULT

```cpp
                    args->PopulateResponseContent(
                        Callback<
                            ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler>(
                            [this, webResourceRequest, webResourceResponse](HRESULT result) {
                                std::wstring message =
                                    L"{ \"kind\": \"event\", \"name\": "
                                    L"\"WebResourceResponseReceived\", \"args\": {"
                                    L"\"request\": " +
                                    RequestToJsonString(webResourceRequest.get()) +
                                    L", "
                                    L"\"response\": " +
                                    ResponseToJsonString(webResourceResponse.get()) + L"}";

                                message +=
                                    WebViewPropertiesToJsonString(m_webviewEventSource.get());
                                message += L"}";
                                PostEventMessage(message);
                                return S_OK;
                            })
                            .Get());
```


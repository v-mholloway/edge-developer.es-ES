---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: aa5206be13790fd7a783f2afb4471de90fc8f2ae
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885721"
---
# 0.8.355: IWebView2WebResourceRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento WebResourceRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Request](#get_request) | La solicitud HTTP.
[get_Response](#get_response) | La respuesta HTTP.
[put_Response](#put_response) | Establezca la propiedad Response.
[GetDeferral](#getdeferral) | Obtén un objeto [IWebView2Deferral](IWebView2Deferral.md) y coloca el evento en un estado diferido.

## Miembros

#### get_Request 

La solicitud HTTP.

> [get_Request](#get_request)de HRESULT público (solicitud[IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) * *)

#### get_Response 

La respuesta HTTP.

> [get_Response](#get_response)de HRESULT público (respuesta de[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) * *)

#### put_Response 

Establezca la propiedad Response.

> [put_Response](#put_response)de HRESULT público (respuesta de[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) *)

#### GetDeferral 

Obtén un objeto [IWebView2Deferral](IWebView2Deferral.md) y coloca el evento en un estado diferido.

> [GETDEFERRAL](#getdeferral)HRESULT ([IWebView2Deferral](IWebView2Deferral.md) * * aplazamiento)

Puede usar el objeto [IWebView2Deferral](IWebView2Deferral.md) para completar la solicitud de red más adelante.


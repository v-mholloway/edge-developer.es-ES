---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 00aaddcc732076e4f7aa808b04132641fe7fe969
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886447"
---
# 0.9.430: ICoreWebView2WebResourceRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento WebResourceRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Request](#get_request) | La solicitud HTTP.
[get_Response](#get_response) | La respuesta HTTP.
[put_Response](#put_response) | Establezca la propiedad Response.
[GetDeferral](#getdeferral) | Obtén un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) y coloca el evento en un estado diferido.
[get_ResourceContext](#get_resourcecontext) | Los contextos de solicitud de recursos Web.

## Miembros

#### get_Request 

La solicitud HTTP.

> [get_Request](#get_request)de HRESULT público (solicitud[ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) * *)

#### get_Response 

La respuesta HTTP.

> [get_Response](#get_response)de HRESULT público (respuesta de[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) * *)

#### put_Response 

Establezca la propiedad Response.

> [put_Response](#put_response)de HRESULT público (respuesta de[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) *)

#### GetDeferral 

Obtén un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) y coloca el evento en un estado diferido.

> [GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](ICoreWebView2Deferral.md) * * aplazamiento)

Puede usar el objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) para completar la solicitud de red más adelante.

#### get_ResourceContext 

Los contextos de solicitud de recursos Web.

> [get_ResourceContext](#get_resourcecontext)de HRESULT público (CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT *)


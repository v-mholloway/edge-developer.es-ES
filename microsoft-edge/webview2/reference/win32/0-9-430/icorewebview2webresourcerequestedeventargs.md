---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 59557ca86e8b044fb937fe93b3060c0879abb6f1
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655403"
---
# interfaz ICoreWebView2WebResourceRequestedEventArgs 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

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


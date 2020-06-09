---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 85954a3f866ed9fd778af93fc27872af2d20eb2e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697948"
---
# interfaz ICoreWebView2WebResourceRequestedEventArgs 

> [!NOTE]
> Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515. Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento WebResourceRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Request](#get_request) | La solicitud HTTP.
[get_ResourceContext](#get_resourcecontext) | Los contextos de solicitud de recursos Web.
[get_Response](#get_response) | La respuesta HTTP.
[GetDeferral](#getdeferral) | Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.
[put_Response](#put_response) | Establezca la propiedad Response.

## Miembros

#### get_Request 

La solicitud HTTP.

> [get_Request](#get_request)de HRESULT público (solicitud[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) * *)

#### get_ResourceContext 

Los contextos de solicitud de recursos Web.

> [get_ResourceContext](#get_resourcecontext)de HRESULT público (COREWEBVIEW2_WEB_RESOURCE_CONTEXT *)

#### get_Response 

La respuesta HTTP.

> [get_Response](#get_response)de HRESULT público (respuesta de[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) * *)

#### GetDeferral 

Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.

> [GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) * * aplazamiento)

Puede usar el objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para completar la solicitud de red más adelante.

#### put_Response 

Establezca la propiedad Response.

> [put_Response](#put_response)de HRESULT público (respuesta de[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) *)


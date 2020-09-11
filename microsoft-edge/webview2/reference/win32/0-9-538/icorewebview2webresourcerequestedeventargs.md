---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 2e55a43282a7548acefdb0b1ed1b8cac2254ef21
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010393"
---
# 0.9.579: ICoreWebView2WebResourceRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Argumentos de evento para el evento WebResourceRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Request](#get_request) | La solicitud de recursos Web.
[get_ResourceContext](#get_resourcecontext) | El contexto de la solicitud de recursos Web.
[get_Response](#get_response) | Un marcador de posición para el objeto de respuesta de recursos Web.
[GetDeferral](#getdeferral) | Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.
[put_Response](#put_response) | Establezca la propiedad Response.

## Miembros

#### get_Request 

La solicitud de recursos Web.

> [get_Request](#get_request)de HRESULT público (solicitud[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) * *)

Es posible que en el objeto de solicitud falten algunos encabezados que la pila de red agrega más adelante.

#### get_ResourceContext 

El contexto de la solicitud de recursos Web.

> [get_ResourceContext](#get_resourcecontext)de HRESULT público (COREWEBVIEW2_WEB_RESOURCE_CONTEXT *)

#### get_Response 

Un marcador de posición para el objeto de respuesta de recursos Web.

> [get_Response](#get_response)de HRESULT público (respuesta de[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) * *)

Si se establece este objeto, la solicitud de recursos Web se completará con esta respuesta.

#### GetDeferral 

Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.

> [GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) * * aplazamiento)

Puedes usar el objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para completar la solicitud más adelante.

#### put_Response 

Establezca la propiedad Response.

> [put_Response](#put_response)de HRESULT público (respuesta de[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) *)

Se puede crear un objeto de respuesta de recursos Web vacío con CreateWebResourceResponse y, a continuación, se ha modificado para construir la respuesta.


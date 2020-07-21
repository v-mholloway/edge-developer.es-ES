---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 656510998879e77c2e7797c700dacc5966299210
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884655"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs (clase) 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

Argumentos de evento para el evento WebResourceRequested.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Solicitud](#request) | La solicitud HTTP.
[ResourceContext](#resourcecontext) | Los contextos de solicitud de recursos Web.
[Respuesta](#response) | La respuesta HTTP.
[GetDeferral](#getdeferral) | Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.

## Miembros

#### Solicitud 

La solicitud HTTP.

> [solicitud](#request) de HttpRequestMessage pública

#### ResourceContext 

Los contextos de solicitud de recursos Web.

> [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) pública [ResourceContext](#resourcecontext)

#### Respuesta 

La respuesta HTTP.

> [respuesta](#response) de HttpResponseMessage pública

#### GetDeferral 

Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.

> Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()

Puede usar el objeto CoreWebView2Deferral para completar la solicitud de red más adelante.


---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 53cc31bc714417ab902fa8fdef9fd83f80871f10
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879670"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs 

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


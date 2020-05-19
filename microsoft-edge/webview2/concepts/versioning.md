---
description: Modelos de control de versiones usados para Microsoft Edge WebView2
title: Control de versiones de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 78184d3c670aa39e0a7f4a31e1216b5bc730c16e
ms.sourcegitcommit: 5bdffe91a6594f77eeffa4e864fda90a02784771
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659674"
---
# Descripción de las versiones y WebView2 del explorador  

WebView2 depende de Microsoft Edge para funcionar.  Cada SDK de WebView2 requiere que se instale una versión mínima del explorador.  Esta versión del explorador se especifica en nuestras notas de la [versión][Webview2Releasenotes].  Es posible que vea la versión mínima reflejada en la versión del paquete de SDK.  Por ejemplo, si usa el `SDK package version 0.9.488` , debe instalar Microsoft Edge con un número de compilación de 488 o posterior.  Para obtener más información sobre las versiones más recientes del explorador, vea [canales de explorador][DeployedgeChannels].  

> [!NOTE]
> WebView2 está actualmente en versión preliminar.  Mientras que el equipo de WebView de Microsoft Edge se esfuerza por garantizar la compatibilidad con versiones anteriores de los exploradores y los SDK, no se garantiza que algunas versiones más recientes del explorador no admitan versiones anteriores de SDK.  Si hay cambios importantes entre las versiones del explorador y los SDK, el equipo de WebView de Microsoft Edge indica los cambios en las notas de la [versión][Webview2Releasenotes].  

En el futuro, el equipo de WebView de Microsoft Edge planea cambiar el modelo de distribución.  El equipo de WebView de Microsoft Edge planea quitar la dependencia directa en el explorador Microsoft Edge de WebView2.  Para obtener más información, vea [WebView2 Runtime][Webview2IndexEdgeRuntime] en la sección de [distribución][Webview2Distibution] .  

## API experimentales  

Aunque WebView2 es una versión preliminar, se espera que las API del SDK permanezcan igual en GA.  Hay [API experimentales][Webview2ReferenceWin3209488Experimental] incluidas en el SDK.  Evalúe las API experimentales y envíe sus comentarios con el [repositorio de comentarios de WebView][GithubMicrosoftedgeWebviewfeedback].  

### Guía básica  

Después de que WebView2 alcance un estado de disponibilidad general estable y publicamos el SDK de la versión 1.0.0, el equipo de WebView de Microsoft Edge planea mover todas las API experimentales a un paquete preliminar.  La versión preliminar del paquete continúa permitiendo los comentarios y la comprensión de las características más recientes, mientras que la versión estable mantiene la compatibilidad con versiones anteriores.  

<!--links -->

[Webview2Distibution]: ./distribution.md "Distribución de aplicaciones mediante WebView2 | Microsoft docs"  
[Webview2IndexEdgeRuntime]: ./distribution.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2 Runtime: distribución de aplicaciones con WebView2 | Microsoft docs"  
[Webview2ReferenceWin3209488Experimental]: ../reference/win32/0-9-488-reference-webview2.md#experimental "Experimental-referencia (WebView2) | Microsoft docs"  
[Webview2Releasenotes]: ../releasenotes.md "Notas de la versión para el SDK de WebView2 | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Información general de los canales de Microsoft Edge | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

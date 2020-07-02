---
description: Modelos de control de versiones usados para Microsoft Edge WebView2
title: Control de versiones de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 059bbeb34f372af0cef944e484599c0b50543cc9
ms.sourcegitcommit: 288bd2a1bec418a84d1f0bda013c1913886bd269
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844428"
---
# Comprender las versiones de SDK de WebView2  

WebView2 depende de Microsoft Edge para funcionar.  Cada SDK de WebView2 requiere que se instale una versión mínima del explorador.  La versión mínima se refleja en la versión del paquete del SDK.  Por ejemplo, si usa el `SDK package version 0.9.488` , debe instalar Microsoft Edge con un número de compilación de 488 o posterior.  La versión del explorador también se especifica en las [notas][Releasenotes]de la versión de WebView2.  Para obtener más información sobre las versiones más recientes del explorador, vea [canales de explorador][DeployedgeChannels].  

> [!NOTE]
> WebView2 está actualmente en versión preliminar.  Mientras el equipo de WebView se esfuerza por garantizar la compatibilidad con versiones anteriores de los exploradores y las versiones del explorador, no se garantiza porque es posible que las versiones más recientes del explorador no admitan versiones anteriores del SDK.  Si hay cambios importantes entre las versiones del explorador y los SDK, el equipo de WebView especifica los cambios en las notas de la [versión][Releasenotes].  

En el futuro, el equipo de WebView planea cambiar el modelo de distribución de las aplicaciones de WebView2.  Para obtener más información, consulte ver el [modo de distribución de perenne][DistributionEvergreenMode].  
 
## Versión y paquete preliminar  

En la versión preliminar, el paquete de versión contiene lo siguiente.  

*   [API Win32 C/C++][ReferenceWin3209538]: API en el SDK que se espera que permanezcan iguales en la GA. 

En la versión preliminar, el paquete anterior contiene los siguientes componentes:  

*   API de .NET: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]y [Core][ReferenceDotnet09538]
*   API experimentales.  Para obtener más información, vea la sección [API experimentales](#experimental-apis) .  

### API experimentales  

El equipo de WebView está probando las API que representan la futura funcionalidad denominada API experimental.  Las API experimentales se marcan como `experimental` en el SDK.  Algunas API experimentales pueden suministrarse como API totalmente estable en el paquete de versión.  Debes esperar que todas las API experimentales cambien antes de su liberación.  Evalúa las API experimentales y comparte tus comentarios con el [repositorio de comentarios de WebView][GithubMicrosoftedgeWebviewfeedback].   

> [!CAUTION]
> Evite usar las API experimentales en aplicaciones de producción.  

### Guía básica  

Después de que WebView2 alcance un estado de disponibilidad general estable, el paquete de versión contiene todas las API de Win32 C/C++ y .NET estables.  El paquete preliminar contiene las API experimentales que están sujetas a cambio en función de los comentarios del desarrollador y de la información compartida.  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Modo de distribución de hoja perenne: distribución de aplicaciones mediante WebView2 | Microsoft docs"  
[ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[Releasenotes]: ../releasenotes.md "Notas de la versión para el SDK de WebView2 | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Información general de los canales de Microsoft Edge | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

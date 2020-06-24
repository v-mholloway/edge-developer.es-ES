---
description: Modelos de control de versiones usados para Microsoft Edge WebView2
title: Control de versiones de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 3862576134d1179fb24b2ce865f705b2bf1db8a6
ms.sourcegitcommit: de171a8e7ccd9f23846f3cd06519e4a0104f1c52
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/23/2020
ms.locfileid: "10757609"
---
# Comprender las versiones de SDK de WebView2  

WebView2 depende de Microsoft Edge para funcionar. Cada SDK de WebView2 requiere que se instale una versión mínima del explorador.  La versión mínima se refleja en la versión del paquete del SDK.  Por ejemplo, si usa el `SDK package version 0.9.488` , debe instalar Microsoft Edge con un número de compilación de 488 o posterior. La versión del explorador también se especifica en las [notas][Webview2Releasenotes]de la versión de WebView2.  Para obtener más información sobre las versiones más recientes del explorador, vea [canales de explorador][DeployedgeChannels].  

> [!NOTE]
> WebView2 está actualmente en versión preliminar.  Mientras que el equipo de WebView de Microsoft Edge se esfuerza por garantizar la compatibilidad con versiones anteriores de los exploradores y los SDK, no se garantiza que algunas versiones más recientes del explorador no admitan versiones anteriores de SDK.  Si hay cambios importantes entre las versiones del explorador y los SDK, el equipo de WebView de Microsoft Edge especifica los cambios en las notas de la [versión][Webview2Releasenotes].  

En el futuro, el modelo de distribución para las aplicaciones de WebView2 cambiará. Para obtener más información, consulte [WebView2 Runtime][Webview2IndexEdgeRuntime].  
 
## Versión y paquete preliminar  

En la versión preliminar, el paquete de versión contiene lo siguiente.  

*   [API Win32 C/C++][Webview2ReferenceWin3209538]: API en el SDK que se espera que permanezcan iguales en la GA. 

En la versión preliminar, el paquete preliminar contiene lo siguiente.  

*   API de .NET: [WPF][Webview2ReferenceWpf09515], [WinForms][Webview2ReferenceWinforms09515]y [Core][Webview2ReferenceDotnet09538]
*   API experimentales.  Para obtener más información, consulta la sección [API de Experimantal](#experimental-apis) .  

### API experimentales  

El equipo de WebView está probando las API que representan la futura funcionalidad denominada API experimental.  Las API experimentales se marcan como `experimental` en el SDK.  Algunas API experimentales pueden suministrarse como API totalmente estable en el paquete de versión.  Debes esperar que todas las API experimentales cambien antes de su liberación.  Evalúa las API experimentales y comparte tus comentarios con el [repositorio de comentarios de WebView][GithubMicrosoftedgeWebviewfeedback].   

> [!CAUTION]
> Evite usar las API experimentales en aplicaciones de producción.  

### Guía básica  

Después de que WebView2 alcance un estado de disponibilidad general estable, el paquete de versión contiene todas las API de Win32 C/C++ y .NET estables.  El paquete preliminar contiene las API experimentales que están sujetas a cambio en función de los comentarios del desarrollador y de la información compartida.  

<!--links -->

[Webview2IndexEdgeRuntime]: ./distribution.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2 Runtime: distribución de aplicaciones con WebView2 | Microsoft docs"  
[Webview2ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[Webview2ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[Webview2ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[Webview2ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[Webview2Releasenotes]: ../releasenotes.md "Notas de la versión para el SDK de WebView2 | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Información general de los canales de Microsoft Edge | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

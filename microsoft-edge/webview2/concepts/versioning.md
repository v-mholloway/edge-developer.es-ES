---
description: Modelos de control de versiones usados para Microsoft Edge WebView2
title: Control de versiones de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: acf3103f39d33586ee0614aeb0f10de0ab71c89a
ms.sourcegitcommit: b3555043e9d5aefa5a9e36ba4d73934d41559f49
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894315"
---
# Comprender las versiones de SDK de WebView2  

WebView2 depende de Microsoft Edge para funcionar.  Cada SDK de WebView2 requiere que se instale una versión mínima del explorador.  La versión mínima se refleja en la versión del paquete del SDK.  Por ejemplo, si usa el `SDK package version 0.9.488` , debe instalar Microsoft Edge con un número de compilación de 488 o posterior.  La versión del explorador también se especifica en las [notas][Releasenotes]de la versión de WebView2.  Para obtener más información sobre las versiones más recientes del explorador, vea [canales de explorador][DeployedgeChannels].  

> [!NOTE]
> WebView2 está actualmente en versión preliminar.  Mientras el equipo de WebView se esfuerza por garantizar la compatibilidad con versiones anteriores de los exploradores y las versiones del explorador, no se garantiza porque es posible que las versiones más recientes del explorador no admitan las versiones anteriores del SDK.  Si hay cambios importantes entre las versiones del explorador y los SDK, especificamos los cambios en las notas de la [versión][Releasenotes].  

En el futuro, planearemos cambiar el modelo de distribución de las aplicaciones de WebView2.  Para obtener más información, consulte [modo de distribución de perenne][DistributionEvergreenMode].  
 
## Versión y paquete preliminar  

En la versión preliminar, el paquete de versión contiene lo siguiente.  

*   [API Win32 C/C++][ReferenceWin3209538]: API en el SDK que se espera que permanezcan iguales en la GA.  

En la versión preliminar, el paquete anterior contiene los siguientes componentes:  

*   API de .NET: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]y [Core][ReferenceDotnet09538]  
*   API experimentales.  Para obtener más información, vea la sección [API experimentales](#experimental-apis) .  

## API experimentales  

Estamos probando las API experimentales que pueden representar la futura funcionalidad.  Las API experimentales se marcan como `experimental` en el SDK.  Las API experimentales pueden suministrarse como API totalmente estable en el paquete de versión.  Debes esperar que todas las API experimentales cambien antes de su liberación.  Evalúa las API experimentales y comparte tus comentarios con el [repositorio de comentarios de WebView][GithubMicrosoftedgeWebviewfeedback].   

> [!CAUTION]
> Evite usar las API experimentales en aplicaciones de producción.  

## Guía básica  

Después de que WebView2 alcance un estado de disponibilidad general estable, el paquete de versión contiene todas las API de Win32 C/C++ y .NET estables.  El paquete preliminar contiene las API experimentales que están sujetas a cambio en función de los comentarios del desarrollador y de la información compartida.  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Modo de distribución de hoja perenne: distribución de aplicaciones mediante WebView2 | Microsoft docs"  
[ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[Releasenotes]: ../releasenotes.md "Notas de la versión para el SDK de WebView2 | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Información general de los canales de Microsoft Edge | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

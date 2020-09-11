---
description: Modelos de control de versiones usados para Microsoft Edge WebView2
title: Control de versiones de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 3ce1f0653a14d92571f1365cbfebc8bb2215ecbe
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010680"
---
# Comprender las versiones de SDK de WebView2  

WebView2 depende de Microsoft Edge para funcionar.  Cada SDK de WebView2 requiere que se instale una versión mínima del explorador.  La versión mínima se refleja en la versión del paquete del SDK.  Por ejemplo, si usa el `SDK package version 0.9.488` , debe instalar Microsoft Edge con un número de compilación de 488 o posterior.  La versión del explorador también se especifica en las [notas][Releasenotes]de la versión de WebView2.  Para obtener más información sobre la versión más reciente del explorador Microsoft Edge, vaya a [canales de explorador][DeployedgeChannels].  

> [!NOTE]
> WebView2 está actualmente en versión preliminar.  Mientras el equipo de WebView se esfuerza por garantizar la compatibilidad con versiones anteriores de los exploradores y las versiones del explorador, no se garantiza porque es posible que las versiones más recientes del explorador no admitan las versiones anteriores del SDK.  Si hay cambios importantes entre las versiones del explorador y los SDK, los cambios se especifican en las notas de la [versión][Releasenotes].  

En el futuro, el equipo de WebView planea cambiar el modelo de distribución de las aplicaciones de WebView2.  Para obtener más información, vaya al [modo de distribución de perenne][DistributionEvergreenMode].  

## Versión de lanzamiento y versión preliminar  

En la versión preliminar, el paquete de versión contiene lo siguiente.  

*   [API Win32 C/C++][ReferenceWin3209622]: API en el SDK que se espera que permanezcan iguales en la GA.  

En la versión preliminar, el paquete de versión preliminar contiene los siguientes componentes.  

*   API de .NET: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]y [Core][ReferenceDotnet09628]  
*   API experimentales.  Para obtener más información, vea la sección [API experimentales](#experimental-apis) .  

## API experimentales  

El equipo de WebView está probando las API experimentales que pueden representar la funcionalidad futura.  Las API experimentales se marcan como `experimental` en el SDK.  Las API experimentales pueden suministrarse como API totalmente estable en el paquete de versión.  Debes esperar que todas las API experimentales cambien antes de su liberación.  Evalúa las API experimentales y comparte tus comentarios con el [repositorio de comentarios de WebView][GithubMicrosoftedgeWebviewfeedback].  

> [!CAUTION]
> Evite usar las API experimentales en aplicaciones de producción.  

## Coincidencia de WebView2 versiones en tiempo de ejecución  

Al escribir una aplicación de WebView2 con una versión de SDK determinada, los usuarios de tu aplicación pueden ejecutarla con varias versiones compatibles del tiempo de ejecución de WebView2.  En el futuro, una versión de tiempo de ejecución de WebView2 compatible más reciente contiene todas las API no experimentales de una versión de tiempo de ejecución de WebView2 compatible anterior, además de nuevas API no experimentales.  

*   Los programadores de **Win32 C/C++** , cuando `QueryInterface` se usan para obtener una nueva interfaz, deben comprobar un valor devuelto de `E_NOINTERFACE` , lo que puede indicar que el tiempo de ejecución de WebView2 es más antiguo y no es compatible con esa interfaz en particular.  
*   Los desarrolladores de **.net y WinUI** deben comprobar una `No such interface supported` excepción al usar métodos, propiedades y eventos agregados en SDK posteriores, que pueden ocurrir cuando el tiempo de ejecución de WebView2 es más antiguo y no es compatible con esas API específicas.  

Si una API no está disponible, considera la posibilidad de deshabilitar la característica asociada, si es posible, o de informar al usuario final de que necesitan actualizar su WebView2 versión de tiempo de ejecución.  

Las API experimentales se pueden introducir, modificar y quitar de SDK a SDK.  Al intentar usar una API experimental que no está disponible en el tiempo de ejecución de WebView2, es posible que observe el mismo comportamiento descrito anteriormente.  

## Guía básica  

Después de que WebView2 alcance un estado de disponibilidad general estable, el paquete de versión contiene todas las API de Win32 C/C++ y .NET estables.  El paquete de versión preliminar contiene las API experimentales que están sujetas a cambios en función de los comentarios y de la información compartida.  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Modo de distribución de hoja perenne: distribución de aplicaciones mediante WebView2 | Microsoft docs"  
[ReferenceDotnet09628]: ../reference/dotnet/0-9-628-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[ReferenceWin3209622]: ../reference/win32/0-9-622-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[Releasenotes]: ../releasenotes.md "Notas de la versión para el SDK de WebView2 | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Información general de los canales de Microsoft Edge | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

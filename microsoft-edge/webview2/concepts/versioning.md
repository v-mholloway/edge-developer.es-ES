---
description: Modelos de control de versiones usados para Microsoft Edge WebView2
title: Control de versiones de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: a47c7295e87cf4295f8cdf898b62aa3b550aa9a5
ms.sourcegitcommit: af91bfc3e6d8afc51f0fbbc0fe392262f424225c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120343"
---
# Comprender las versiones de SDK de WebView2  

Para desarrollar una aplicación de WebView2, debes instalar el [motor de tiempo de ejecución de WebView2][MicrosoftDeveloperEdgeWebview2] o un canal de [Microsoft Edge no estable][MicrosoftedgeinsiderDownload].  La versión mínima requerida se incluye en la versión del paquete NuGet del SDK.  Por ejemplo, si usa el `SDK package version 0.9.488` , debe instalar el [motor en tiempo de ejecución de WebView2][MicrosoftDeveloperEdgeWebview2] o un canal de [Microsoft Edge no estable][MicrosoftedgeinsiderDownload] con un número de compilación de 488 o posterior.  La versión mínima requerida también se especifica en las notas de la [versión][Releasenotes]de WebView2.  Las nuevas versiones del SDK de WebView2 se distribuyen a la misma cadencia general que el explorador Microsoft Edge \ (cromo \), que es aproximadamente cada seis semanas.  

> [!IMPORTANT]
> Al desarrollar aplicaciones de WebView2 de hoja perenne, pruebe regularmente la aplicación con las versiones más recientes del tiempo de ejecución de WebView2 y de los exploradores de Microsoft Edge no estables.  Debido a que la plataforma web está evolucionando constantemente, la mejor manera de garantizar que tu aplicación funcione como se pretende.  

## Versión de lanzamiento y versión preliminar  

El paquete de NuGet de WebView2 contiene una versión y un paquete de versión preliminar.  

El paquete de versión es compatible con versiones posteriores y contiene las [API de C/C++ Win32][ReferenceWin32].  Las API de este SDK son totalmente compatibles.  

El paquete de versión preliminar es un supraconjunto del paquete de versiones con los componentes adicionales que se enumeran a continuación.  

*   API de .NET: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]y [Core][DotnetMicrosoftWebWebview2CoreNamespace]  
*   API experimentales: para obtener más información, vaya a la sección [API experimentales](#experimental-apis) .  

## API experimentales  

El equipo de WebView está probando las API experimentales que pueden estar incluidas en versiones futuras.  Las API experimentales se marcan como `experimental` en el SDK.  Las API experimentales pueden suministrarse como API totalmente estable en el paquete de versión.  Puede evaluar las API experimentales y compartir los comentarios con el [repositorio de comentarios de WebView][GithubMicrosoftedgeWebviewfeedback].  

> [!CAUTION]
> Evite usar las API experimentales en aplicaciones de producción.  

## Coincidencia de WebView2 versiones en tiempo de ejecución  

Al escribir una aplicación de WebView2 con una versión de SDK determinada, los usuarios de la aplicación pueden ejecutarla con varias versiones compatibles del motor en tiempo de ejecución de WebView2.  El equipo de WebView está trabajando en una versión de tiempo de ejecución de WebView2 compatible que contiene las API no experimentales de versiones anteriores del motor de tiempo de ejecución y nuevas API no experimentales.  

Según el SDK que use, tenga en cuenta los siguientes elementos: 

*   **C/C++ Win32**.  Cuando use `QueryInterface` para obtener una nueva interfaz, compruebe si el valor devuelto es `E_NOINTERFACE` .  Este valor puede indicar que el tiempo de ejecución de WebView2 es una versión anterior y no es compatible con esa interfaz.  
*   **.Net y WinUI**.  Comprueba una `No such interface supported` excepción al usar métodos, propiedades y eventos que se agregaron a SDK más recientes.  Esta excepción puede producirse cuando el tiempo de ejecución de WebView2 es una versión anterior y no es compatible con esas API.  

Si una API no está disponible, considere la posibilidad de quitar la característica asociada o informe a los usuarios de que necesitan actualizar su versión del tiempo de ejecución de WebView2.  

Las API experimentales se pueden introducir, modificar y quitar de SDK a SDK.  Es posible que las API experimentales no estén disponibles en la versión instalada del tiempo de ejecución de WebView2.  

## Guía básica  

El paquete de versión contiene todas las API de C/C++ de Win32, estables y estables.  En el futuro, el paquete de versión contendrá todas las API de .NET compatibles y estables cuando estén disponibles para el público.  El paquete de versión preliminar contiene las API experimentales que están sujetas a cambios en función de los comentarios y de la información compartida.  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->  

[Releasenotes]: ../releasenotes.md "Notas de la versión para el SDK de WebView2 | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Información general de los canales de Microsoft Edge | Microsoft docs"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Espacio de nombres Microsoft. Web. WebView2. Core | Microsoft docs"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Espacio de nombres Microsoft. Web. WebView2. WPF | Microsoft docs"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Espacio de nombres Microsoft. Web. WebView2. WinForms | Microsoft docs"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Referencia de C++ de WebView2 Win32 | Microsoft docs"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Microsoft Developer"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar los canales de Insider de Microsoft Edge"  

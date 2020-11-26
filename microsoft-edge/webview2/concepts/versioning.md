---
description: Modelos de control de versiones usados para Microsoft Edge WebView2
title: Control de versiones de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 54d62de00a89a3c433fd77e9ec20945adbfc19c3
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "11191613"
---
# Comprender las versiones de SDK de WebView2  

Las nuevas versiones del SDK de WebView2 se distribuyen a la misma cadencia general que el explorador Microsoft Edge \ (cromo \), que es aproximadamente cada seis semanas.  

## Versión de lanzamiento y versión preliminar  

El paquete de NuGet de WebView2 contiene una versión y un paquete de versión preliminar.  

El **paquete de versión** es compatible con versiones posteriores y contiene los siguientes componentes.  

*   [API Win32 C/C++][ReferenceWin32]
*   API de .NET:  [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]y [Core][DotnetMicrosoftWebWebview2CoreNamespace].  
    
Las API del SDK son totalmente compatibles.  

El **paquete de versión preliminar** es un supraconjunto del paquete de versiones con las [API experimentales](#experimental-apis).  

### Guía básica  

El paquete de versión contiene todas las API de Win32 C/C++ y .NET, estables y estables.  El paquete de versión preliminar contiene las API experimentales que están sujetas a cambios en función de los comentarios.  

## API experimentales  

El equipo de WebView está buscando comentarios sobre las API experimentales que pueden estar incluidas en versiones futuras.  Las API experimentales se marcan como `experimental` en el SDK.  Para ayudarle a evaluar las API experimentales y compartir sus comentarios, navegue hasta el [repositorio de comentarios de WebView][GithubMicrosoftedgeWebviewfeedback].  

> [!CAUTION]
> Las API experimentales se pueden introducir, modificar y quitar de SDK a SDK.  Evite usar las API experimentales en aplicaciones de producción.  

> [!NOTE]
> Es posible que las API experimentales no estén disponibles en la versión instalada del tiempo de ejecución de WebView2.  

## Coincidencia de WebView2 versiones en tiempo de ejecución  
Las aplicaciones de WebView2 requieren que los usuarios instalen un [motor en tiempo de ejecución de WebView2][MicrosoftDeveloperEdgeWebview2].  El tiempo de ejecución de WebView2 se actualiza automáticamente a la versión más reciente disponible.  En algunos escenarios, es posible que los usuarios deseen detener las actualizaciones automáticas del tiempo de ejecución de WebView2, lo que puede provocar problemas de compatibilidad de la aplicación.  

Si se detienen las actualizaciones en tiempo de ejecución de WebView2, asegúrate de comprender la versión mínima del [tiempo de ejecución de WebView2][MicrosoftDeveloperEdgeWebview2] requerida por tu aplicación.  Considere los dos elementos siguientes:  

1.  La versión mínima requerida del SDK, que se encuentra en las [notas][Webview2Releasenotes] de la versión de WebView2 en **versión mínima de tiempo de ejecución de WebView2**.  Por ejemplo, para el SDK de la versión [1.0.622.22][Webview2Releasenotes1062222], debe instalar el [motor en tiempo de ejecución de WebView2][MicrosoftDeveloperEdgeWebview2] o un canal de [Microsoft Edge no estable][MicrosoftedgeinsiderDownload] con un número de compilación de `86.0.616.0` o posterior.  La versión mínima requerida por el SDK solo cambia cuando se produce un cambio importante en la plataforma Web.  
1.  La versión mínima requerida del paquete NuGet necesaria para admitir las interfaces y las API que usas en tu aplicación.  Las nuevas interfaces y API se agregan periódicamente a WebView2.  Las API e interfaces empaquetadas en un SDK requieren diferentes versiones del tiempo de ejecución de WebView2, ya que las API y la interfaz se agregan al SDK en diferentes momentos.  La versión de tiempo de ejecución de WebView2 requerida coincide con el número de compilación, el tercer número, de la versión de SDK que se introdujo en la API por primera vez.  Por ejemplo, una nueva API o interfaz agregada en la versión [1.0.622.22][Webview2Releasenotes1062222] de SDK requiere la versión de tiempo de ejecución de WebView2:  `86.0.622.0`  una API o una interfaz agregada en una versión de SDK posterior requiere el tiempo de ejecución de WebView2 que tiene el mismo número de versión que el SDK.  Para ayudarte a determinar si la versión de tiempo de ejecución de WebView2 es compatible con una interfaz o una API, navega para [determinar WebView2 requisito en tiempo de ejecución](#determine-webview2-runtime-requirement).  
    
> [!IMPORTANT]
> Al desarrollar [aplicaciones de WebView2 de perennes][Webview2ConceptsDistributionEvergreenDistributionMode], prueba regularmente tu aplicación con las versiones más recientes del tiempo de ejecución de WebView2 y de los exploradores de Microsoft Edge no estables.  Debido a que la plataforma web está evolucionando constantemente, la mejor manera de garantizar que tu aplicación sea la espera.  

### Determinar requisito de tiempo de ejecución de WebView2  

Según el SDK que use, tenga en cuenta los siguientes elementos:  

*   **C/C++ Win32**.  Cuando use `QueryInterface` para obtener una nueva interfaz, compruebe un valor devuelto de `E_NOINTERFACE` .  El valor puede indicar que el tiempo de ejecución de WebView2 es una versión anterior y no es compatible con esa interfaz.  Para obtener un ejemplo de cómo funciona, vaya a la [línea 622-AppWindow. cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].  
*   **.Net y WinUI**.  Comprueba una `No such interface supported` excepción al usar métodos, propiedades y eventos que se agregaron a SDK más recientes.  La excepción puede producirse cuando el tiempo de ejecución de WebView2 es una versión anterior y no es compatible con las API.  
    
Si una API no está disponible, considera la posibilidad de quitar la característica asociada o informa a los usuarios de que se requiere una actualización para el tiempo de ejecución de WebView2.  

<!--
## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  
1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  
    -->  

<!--links -->  

[Webview2ConceptsDistributionEvergreenDistributionMode]: ./distribution.md#evergreen-distribution-mode "Modo de distribución de hoja perenne: distribución de aplicaciones con WebView2 | Microsoft docs"  
[Webview2Releasenotes]: ../releasenotes.md "Notas de la versión para el SDK de WebView2 | Microsoft docs"  
[Webview2Releasenotes1062222]: ../releasenotes.md#1062222 "1.0.622.22-notas de la versión para el SDK de WebView2 | Microsoft docs"   

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Información general de los canales de Microsoft Edge | Microsoft docs"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Espacio de nombres Microsoft. Web. WebView2. Core | Microsoft docs"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Espacio de nombres Microsoft. Web. WebView2. WPF | Microsoft docs"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Espacio de nombres Microsoft. Web. WebView2. WinForms | Microsoft docs"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Referencia de C++ de WebView2 Win32 | Microsoft docs"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Microsoft Developer"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622]: https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622 "Línea 622-AppWindow. cpp-MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar los canales de Insider de Microsoft Edge"  

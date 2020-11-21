---
description: Modelos de control de versiones usados para Microsoft Edge WebView2
title: Control de versiones de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/18/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 132ccab0f9f378eedd8c83a7404c350161556f2e
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182398"
---
# Comprender las versiones de SDK de WebView2

Las nuevas versiones del SDK de WebView2 se distribuyen a la misma cadencia general que el explorador Microsoft Edge \ (cromo \), que es aproximadamente cada seis semanas.  

## Versión de lanzamiento y versión preliminar  

El paquete de NuGet de WebView2 contiene una versión y un paquete de versión preliminar.  

El paquete de versión es compatible con versiones posteriores y contiene las [API de C/C++ Win32][ReferenceWin32].  Las API de este SDK son totalmente compatibles.  

El paquete de versión preliminar es un supraconjunto del paquete de versiones con los componentes adicionales que se enumeran a continuación.  

*   API de .NET: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]y [Core][DotnetMicrosoftWebWebview2CoreNamespace]  
*   API experimentales: para obtener más información, vaya a la sección [API experimentales](#experimental-apis) .  

### Guía básica  

El paquete de versión contiene todas las API de C/C++ de Win32, estables y estables.  En el futuro, el paquete de versión contendrá todas las API de .NET compatibles y estables cuando estén disponibles para el público.  El paquete de versión preliminar contiene las API experimentales que están sujetas a cambios en función de los comentarios. 

## API experimentales  

El equipo de WebView está buscando comentarios sobre las API experimentales que pueden estar incluidas en versiones futuras.  Las API experimentales se marcan como `experimental` en el SDK.  Puede evaluar las API experimentales y compartir los comentarios con el [repositorio de comentarios de WebView][GithubMicrosoftedgeWebviewfeedback].  

> [!CAUTION]
> Las API experimentales se pueden introducir, modificar y quitar de SDK a SDK.  Evite usar las API experimentales en aplicaciones de producción.  

> [!NOTE]
> Es posible que las API experimentales no estén disponibles en la versión instalada del tiempo de ejecución de WebView2.  

## Coincidencia de WebView2 versiones en tiempo de ejecución  
Las aplicaciones de WebView2 requieren que los usuarios instalen un [motor en tiempo de ejecución de WebView2][MicrosoftDeveloperEdgeWebview2]. El tiempo de ejecución de WebView2 se actualiza automáticamente a la última versión que está disponible. En algunos escenarios, es posible que los usuarios necesiten detener las actualizaciones automáticas del tiempo de ejecución de WebView2, lo que puede provocar problemas de compatibilidad de la aplicación.

Si se detienen las actualizaciones en tiempo de ejecución de WebView2, asegúrese de que comprende la versión mínima del [tiempo de ejecución de WebView2][MicrosoftDeveloperEdgeWebview2] que necesita la aplicación. Considere los dos elementos siguientes:  

1. La versión mínima requerida del SDK, que puede encontrarse en las [notas][Releasenotes] de la versión de WebView2 en **versión mínima de tiempo de ejecución de WebView2**. Por ejemplo, para el SDK de la versión [1.0.622.22](https://docs.microsoft.com/microsoft-edge/webview2/releasenotes#1062222), debe instalar el [motor en tiempo de ejecución de WebView2][MicrosoftDeveloperEdgeWebview2] o un canal de [Microsoft Edge no estable][MicrosoftedgeinsiderDownload] con un número de compilación de **86.0.616.0** o posterior. La versión mínima requerida por el SDK solo cambiará cuando haya un cambio importante en la plataforma Web.

2. La versión mínima requerida del paquete NuGet necesaria para admitir las interfaces y las API que se usan en la aplicación. Las nuevas interfaces y API se agregan periódicamente a WebView2. Las API e interfaces empaquetadas en un SDK requerirán diferentes versiones del tiempo de ejecución de WebView2 porque se agregaron al SDK en diferentes momentos.  La versión de tiempo de ejecución de WebView2 requerida coincide con el número de compilación, el tercer número, de la versión de SDK que se introdujo en la API por primera vez. Por ejemplo, una nueva API o interfaz agregada en SDK versión [1.0.622.22](https://docs.microsoft.com/microsoft-edge/webview2/releasenotes#1062222) necesitará la versión de tiempo de ejecución de WebView2:86,0. **622**. 0. Una API o interfaz agregada en una versión de SDK posterior requiere el tiempo de ejecución de WebView2 que tenga el mismo número de versión que el SDK. Puedes determinar si la versión de tiempo de ejecución de WebView2 admite una interfaz o una API [mediante programación](#determine-webview2-runtime-requirement).

> [!IMPORTANT]
> Al desarrollar [aplicaciones de WebView2 de hoja perenne](distribution.md#evergreen-distribution-mode), pruebe regularmente la aplicación con las versiones más recientes del tiempo de ejecución de WebView2 y de los exploradores de Microsoft Edge no estables.  Debido a que la plataforma web está evolucionando constantemente, la mejor manera de garantizar que tu aplicación funcione como se pretende.  

### Determinar requisito de tiempo de ejecución de WebView2

Según el SDK que use, tenga en cuenta los siguientes elementos: 

*   **C/C++ Win32**.  Cuando use `QueryInterface` para obtener una nueva interfaz, compruebe si el valor devuelto es `E_NOINTERFACE` .  Este valor puede indicar que el tiempo de ejecución de WebView2 es una versión anterior y no es compatible con esa interfaz. Navegue hasta el ejemplo WebView2API para obtener un [ejemplo](https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622) de cómo funciona.
*   **.Net y WinUI**.  Comprueba una `No such interface supported` excepción al usar métodos, propiedades y eventos que se agregaron a SDK más recientes.  Esta excepción puede producirse cuando el tiempo de ejecución de WebView2 es una versión anterior y no es compatible con esas API.  

Si una API no está disponible, considere la posibilidad de quitar la característica asociada o informe a los usuarios de que necesitan actualizar su versión del tiempo de ejecución de WebView2.  



 

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

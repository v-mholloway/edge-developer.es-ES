---
description: Modelos de versión usados para Microsoft Edge WebView2
title: Comprender las versiones de SDK de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, controlador de explorador, edge html
ms.openlocfilehash: 645eb4e50ba6bd74ab046b09d7071ff3c375a923
ms.sourcegitcommit: 9f5dd05432f87339f4c3d71f1f9ce1d06afcaf4b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/23/2021
ms.locfileid: "11675123"
---
# <a name="understand-webview2-sdk-versions"></a>Comprender las versiones de SDK de WebView2  

Las nuevas versiones del SDK de WebView2 se envían con la misma cadencia general que el explorador Microsoft Edge \(Chromium\), que es aproximadamente cada seis semanas.  

## <a name="release-and-prerelease-package"></a>Paquete de versión y versión preliminar  

El paquete webView2 NuGet contiene un paquete de versión y de versión previa.  

El **paquete de versión** es compatible con reenvío y contiene los siguientes componentes.  

*   [API de Win32 C/C++][ReferenceWin32]
*   API de .NET:  [WPF,][DotnetMicrosoftWebWebview2WpfNamespace] [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]y [Core][DotnetMicrosoftWebWebview2CoreNamespace].  
    
Las API del SDK son totalmente compatibles.  

El **paquete de versión preliminar** es un superconjunto del paquete de versión con API [experimentales.](#experimental-apis)  Evita usar el SDK de versión preliminar para crear aplicaciones de producción.  

### <a name="roadmap"></a>Guía básica  

El paquete de versión contiene todas las API de Win32 C/C++ y .NET estables y admitidas.  El paquete de versión preliminar contiene API experimentales que están sujetas a cambios en función de sus comentarios.  

## <a name="experimental-apis"></a>API experimentales  

El equipo de WebView está buscando comentarios sobre las API experimentales que pueden incluirse en futuras versiones.  Las API experimentales se marcan como `experimental` en el SDK.  Para ayudarle a evaluar las API experimentales y compartir sus comentarios, vaya al repositorio de comentarios [de WebView][GithubMicrosoftedgeWebviewfeedback].  

> [!CAUTION]
> Las API experimentales pueden introducirse, modificarse y quitarse del SDK al SDK.  Evita usar las API experimentales en aplicaciones de producción.  Después de la versión de una API como estable y pública, Microsoft admite la versión experimental de esa API para dos versiones en un estado en desuso. 

> [!NOTE]
> Es posible que las API experimentales no estén disponibles en la versión instalada de WebView2 Runtime.  

## <a name="matching-webview2-runtime-versions"></a>Coincidencia de versiones de WebView2 Runtime  
Las aplicaciones de WebView2 requieren que los usuarios instalen [webView2 Runtime][MicrosoftDeveloperEdgeWebview2].  WebView2 Runtime se actualiza automáticamente a la versión más reciente disponible.  En algunos escenarios, es posible que los usuarios quieran detener las actualizaciones automáticas de WebView2 Runtime, lo que puede provocar problemas de compatibilidad de aplicaciones.  

Si se detienen las actualizaciones de WebView2 Runtime, asegúrate de comprender la versión mínima de [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] que requiere la aplicación.  Tenga en cuenta los dos elementos siguientes:  

1.  La versión mínima necesaria del SDK para cargar correctamente una instancia webview2 se encuentra en las Notas de la versión de [WebView2][Webview2ReleaseNotes] en Minimum Microsoft Edge version to **load**.  La versión mínima para cargar requerida por el SDK solo cambia cuando se produce un cambio importante en la plataforma web.  Por ejemplo, para sdk versión [1.0.622.22][Webview2ReleaseNotes1062222], debe instalar [webView2 Runtime][MicrosoftDeveloperEdgeWebview2] o un canal [de Microsoft Edge][MicrosoftedgeinsiderDownload] no estable con un número de compilación o `86.0.616.0` posterior.   
1.  La versión mínima necesaria del paquete NuGet necesario para admitir las interfaces y las API [][Webview2ReleaseNotes] de la aplicación se encuentra en las Notas de la versión de WebView2 en **Compatibilidad completa**de api .  Las nuevas interfaces y API se agregan periódicamente a WebView2.  Las API e interfaces agrupadas en un SDK requieren diferentes versiones de WebView2 Runtime, ya que las API y la interfaz se agregan al SDK en momentos diferentes.  La versión necesaria de WebView2 Runtime coincide con el número de compilación, el tercer número, de la versión del SDK en la que se introdujo por primera vez la API.  Por ejemplo, una nueva API o interfaz agregada en sdk versión [1.0.622.22][Webview2ReleaseNotes1062222] requiere la versión de Tiempo de ejecución de WebView2 `86.0.622.0` o posterior.  Una API o interfaz agregada en una versión posterior del SDK requiere un Tiempo de ejecución de WebView2 que tenga el mismo número de versión que el SDK.  Para ayudarle a determinar si la versión de WebView2 Runtime admite una interfaz o API, vaya a Determinar el requisito de Tiempo de ejecución [de WebView2](#determine-webview2-runtime-requirement).  
    
> [!IMPORTANT]
> Al desarrollar aplicaciones [de Evergreen WebView2,][Webview2ConceptsDistributionEvergreenDistributionMode]prueba la aplicación con regularidad con las versiones más recientes de WebView2 Runtime y los canales de Microsoft Edge estables.  Dado que la plataforma web está en constante evolución, las pruebas periódicas son la mejor manera de garantizar que la aplicación funciona según lo previsto.  

### <a name="determine-webview2-runtime-requirement"></a>Determinar el requisito de Tiempo de ejecución de WebView2  

En función del SDK que use, tenga en cuenta los siguientes elementos:  

*   **Win32 C/C++**.  Al usar `QueryInterface` para obtener una nueva interfaz, compruebe un valor devuelto de `E_NOINTERFACE` .  El valor puede indicar que WebView2 Runtime es una versión anterior y no admite esa interfaz.  Para obtener un ejemplo de cómo funciona, vaya a [Línea 622 - AppWindow.cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].  
*   **.NET y WinUI**.  Compruebe si hay una excepción al usar métodos, propiedades y eventos que se agregaron a `No such interface supported` SDK más recientes.  La excepción puede producirse cuando WebView2 Runtime es una versión anterior y no admite las API.  
    
Si una API no está disponible, considere la posibilidad de quitar la característica asociada o informar a los usuarios de que es necesaria una actualización de WebView2 Runtime.  

<!--
## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  
1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  
    -->  

<!--links -->  

[Webview2ConceptsDistributionEvergreenDistributionMode]: ./distribution.md#evergreen-distribution-mode "Modo de distribución Evergreen: distribución de aplicaciones con WebView2 | Microsoft Docs"  
[Webview2ReleaseNotes]: ../release-notes.md "Notas de la versión de WebView2 SDK | Microsoft Docs"  
[Webview2ReleaseNotes1062222]: ../release-notes.md#1062222 "1.0.622.22: notas de la versión de WebView2 SDK | Microsoft Docs"   

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Información general sobre los canales de Microsoft Edge | Microsoft Docs"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Espacio de nombres Microsoft.Web.WebView2.Core | Microsoft Docs"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Espacio de nombres Microsoft.Web.WebView2.Wpf | Microsoft Docs"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Espacio de nombres Microsoft.Web.WebView2.WinForms | Microsoft Docs"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "WebView2 Win32 C++ Reference | Microsoft Docs"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Microsoft Developer"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622]: https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622 "Línea 622 - AppWindow.cpp - MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

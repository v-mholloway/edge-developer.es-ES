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
# <span data-ttu-id="ab38a-104">Comprender las versiones de SDK de WebView2</span><span class="sxs-lookup"><span data-stu-id="ab38a-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="ab38a-105">Las nuevas versiones del SDK de WebView2 se distribuyen a la misma cadencia general que el explorador Microsoft Edge \ (cromo \), que es aproximadamente cada seis semanas.</span><span class="sxs-lookup"><span data-stu-id="ab38a-105">New versions of the WebView2 SDK are shipped at the same general cadence as the Microsoft Edge \(Chromium\) browser, which is approximately every six weeks.</span></span>  

## <span data-ttu-id="ab38a-106">Versión de lanzamiento y versión preliminar</span><span class="sxs-lookup"><span data-stu-id="ab38a-106">Release and prerelease package</span></span>  

<span data-ttu-id="ab38a-107">El paquete de NuGet de WebView2 contiene una versión y un paquete de versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="ab38a-107">The WebView2 NuGet package contains both a release and pre-release package.</span></span>  

<span data-ttu-id="ab38a-108">El **paquete de versión** es compatible con versiones posteriores y contiene los siguientes componentes.</span><span class="sxs-lookup"><span data-stu-id="ab38a-108">The **release package** is forward compatible and contains the following components.</span></span>  

*   [<span data-ttu-id="ab38a-109">API Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="ab38a-109">Win32 C/C++ APIs</span></span>][ReferenceWin32]
*   <span data-ttu-id="ab38a-110">API de .NET:  [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]y [Core][DotnetMicrosoftWebWebview2CoreNamespace].</span><span class="sxs-lookup"><span data-stu-id="ab38a-110">.NET APIs:  [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace], and [Core][DotnetMicrosoftWebWebview2CoreNamespace].</span></span>  
    
<span data-ttu-id="ab38a-111">Las API del SDK son totalmente compatibles.</span><span class="sxs-lookup"><span data-stu-id="ab38a-111">APIs in the SDK are fully supported.</span></span>  

<span data-ttu-id="ab38a-112">El **paquete de versión preliminar** es un supraconjunto del paquete de versiones con las [API experimentales](#experimental-apis).</span><span class="sxs-lookup"><span data-stu-id="ab38a-112">The **prerelease package** is a superset of the release package with [Experimental APIs](#experimental-apis).</span></span>  

### <span data-ttu-id="ab38a-113">Guía básica</span><span class="sxs-lookup"><span data-stu-id="ab38a-113">Roadmap</span></span>  

<span data-ttu-id="ab38a-114">El paquete de versión contiene todas las API de Win32 C/C++ y .NET, estables y estables.</span><span class="sxs-lookup"><span data-stu-id="ab38a-114">The release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="ab38a-115">El paquete de versión preliminar contiene las API experimentales que están sujetas a cambios en función de los comentarios.</span><span class="sxs-lookup"><span data-stu-id="ab38a-115">The prerelease package contains experimental APIs that are subject to change based on your feedback.</span></span>  

## <span data-ttu-id="ab38a-116">API experimentales</span><span class="sxs-lookup"><span data-stu-id="ab38a-116">Experimental APIs</span></span>  

<span data-ttu-id="ab38a-117">El equipo de WebView está buscando comentarios sobre las API experimentales que pueden estar incluidas en versiones futuras.</span><span class="sxs-lookup"><span data-stu-id="ab38a-117">The WebView team is seeking feedback on experimental APIs that may be included in future releases.</span></span>  <span data-ttu-id="ab38a-118">Las API experimentales se marcan como `experimental` en el SDK.</span><span class="sxs-lookup"><span data-stu-id="ab38a-118">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="ab38a-119">Para ayudarle a evaluar las API experimentales y compartir sus comentarios, navegue hasta el [repositorio de comentarios de WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="ab38a-119">To help you evaluate the Experimental APIs and share your feedback, navigate to the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="ab38a-120">Las API experimentales se pueden introducir, modificar y quitar de SDK a SDK.</span><span class="sxs-lookup"><span data-stu-id="ab38a-120">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="ab38a-121">Evite usar las API experimentales en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ab38a-121">Avoid using the experimental APIs in production apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="ab38a-122">Es posible que las API experimentales no estén disponibles en la versión instalada del tiempo de ejecución de WebView2.</span><span class="sxs-lookup"><span data-stu-id="ab38a-122">Experimental APIs may not be available in your installed version of the WebView2 Runtime.</span></span>  

## <span data-ttu-id="ab38a-123">Coincidencia de WebView2 versiones en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="ab38a-123">Matching WebView2 Runtime versions</span></span>  
<span data-ttu-id="ab38a-124">Las aplicaciones de WebView2 requieren que los usuarios instalen un [motor en tiempo de ejecución de WebView2][MicrosoftDeveloperEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="ab38a-124">WebView2 apps require users to install a [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2].</span></span>  <span data-ttu-id="ab38a-125">El tiempo de ejecución de WebView2 se actualiza automáticamente a la versión más reciente disponible.</span><span class="sxs-lookup"><span data-stu-id="ab38a-125">The WebView2 Runtime automatically updates to the latest version available.</span></span>  <span data-ttu-id="ab38a-126">En algunos escenarios, es posible que los usuarios deseen detener las actualizaciones automáticas del tiempo de ejecución de WebView2, lo que puede provocar problemas de compatibilidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab38a-126">In some scenarios, users may want to stop automatic WebView2 Runtime updates, which may cause app compatibility issues.</span></span>  

<span data-ttu-id="ab38a-127">Si se detienen las actualizaciones en tiempo de ejecución de WebView2, asegúrate de comprender la versión mínima del [tiempo de ejecución de WebView2][MicrosoftDeveloperEdgeWebview2] requerida por tu aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab38a-127">If WebView2 Runtime updates are stopped, ensure you understand the minimum version of the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] required by your app.</span></span>  <span data-ttu-id="ab38a-128">Considere los dos elementos siguientes:</span><span class="sxs-lookup"><span data-stu-id="ab38a-128">Consider the following two items:</span></span>  

1.  <span data-ttu-id="ab38a-129">La versión mínima requerida del SDK, que se encuentra en las [notas][Webview2Releasenotes] de la versión de WebView2 en **versión mínima de tiempo de ejecución de WebView2**.</span><span class="sxs-lookup"><span data-stu-id="ab38a-129">The minimum required version of the SDK, in found in the WebView2 [Release Notes][Webview2Releasenotes] under **minimum WebView2 Runtime version**.</span></span>  <span data-ttu-id="ab38a-130">Por ejemplo, para el SDK de la versión [1.0.622.22][Webview2Releasenotes1062222], debe instalar el [motor en tiempo de ejecución de WebView2][MicrosoftDeveloperEdgeWebview2] o un canal de [Microsoft Edge no estable][MicrosoftedgeinsiderDownload] con un número de compilación de `86.0.616.0` o posterior.</span><span class="sxs-lookup"><span data-stu-id="ab38a-130">For example, for SDK version [1.0.622.22][Webview2Releasenotes1062222], you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload] with a build number of `86.0.616.0` or later.</span></span>  <span data-ttu-id="ab38a-131">La versión mínima requerida por el SDK solo cambia cuando se produce un cambio importante en la plataforma Web.</span><span class="sxs-lookup"><span data-stu-id="ab38a-131">The minimum version required by the SDK only changes when a breaking change occurs in the web platform.</span></span>  
1.  <span data-ttu-id="ab38a-132">La versión mínima requerida del paquete NuGet necesaria para admitir las interfaces y las API que usas en tu aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab38a-132">The minimum required version of the NuGet package required to support the interfaces and APIs that you use in your app.</span></span>  <span data-ttu-id="ab38a-133">Las nuevas interfaces y API se agregan periódicamente a WebView2.</span><span class="sxs-lookup"><span data-stu-id="ab38a-133">New interfaces and APIs are added periodically to WebView2.</span></span>  <span data-ttu-id="ab38a-134">Las API e interfaces empaquetadas en un SDK requieren diferentes versiones del tiempo de ejecución de WebView2, ya que las API y la interfaz se agregan al SDK en diferentes momentos.</span><span class="sxs-lookup"><span data-stu-id="ab38a-134">APIs and interfaces bundled in an SDK require different versions of the WebView2 Runtime, because APIs and interface are added to the SDK at different times.</span></span>  <span data-ttu-id="ab38a-135">La versión de tiempo de ejecución de WebView2 requerida coincide con el número de compilación, el tercer número, de la versión de SDK que se introdujo en la API por primera vez.</span><span class="sxs-lookup"><span data-stu-id="ab38a-135">The required WebView2 Runtime version matches the build number, the third number, of the SDK version the API was first introduced in.</span></span>  <span data-ttu-id="ab38a-136">Por ejemplo, una nueva API o interfaz agregada en la versión [1.0.622.22][Webview2Releasenotes1062222] de SDK requiere la versión de tiempo de ejecución de WebView2:  `86.0.622.0`  una API o una interfaz agregada en una versión de SDK posterior requiere el tiempo de ejecución de WebView2 que tiene el mismo número de versión que el SDK.</span><span class="sxs-lookup"><span data-stu-id="ab38a-136">For example, a new API or interface added in SDK version [1.0.622.22][Webview2Releasenotes1062222] requires the WebView2 Runtime version:  `86.0.622.0`  An API or interface added in a later SDK release requires the WebView2 Runtime that has the same version number as the SDK.</span></span>  <span data-ttu-id="ab38a-137">Para ayudarte a determinar si la versión de tiempo de ejecución de WebView2 es compatible con una interfaz o una API, navega para [determinar WebView2 requisito en tiempo de ejecución](#determine-webview2-runtime-requirement).</span><span class="sxs-lookup"><span data-stu-id="ab38a-137">To help you determine if the WebView2 Runtime version supports an interface or API, navigate to [Determine WebView2 Runtime requirement](#determine-webview2-runtime-requirement).</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="ab38a-138">Al desarrollar [aplicaciones de WebView2 de perennes][Webview2ConceptsDistributionEvergreenDistributionMode], prueba regularmente tu aplicación con las versiones más recientes del tiempo de ejecución de WebView2 y de los exploradores de Microsoft Edge no estables.</span><span class="sxs-lookup"><span data-stu-id="ab38a-138">When developing [Evergreen WebView2 apps][Webview2ConceptsDistributionEvergreenDistributionMode], regularly test your app against the latest versions of the WebView2 Runtime and non-stable Microsoft Edge browsers.</span></span>  <span data-ttu-id="ab38a-139">Debido a que la plataforma web está evolucionando constantemente, la mejor manera de garantizar que tu aplicación sea la espera.</span><span class="sxs-lookup"><span data-stu-id="ab38a-139">Because the web platform is constantly evolving, regular testing is the best way to ensure your app performs as intended.</span></span>  

### <span data-ttu-id="ab38a-140">Determinar requisito de tiempo de ejecución de WebView2</span><span class="sxs-lookup"><span data-stu-id="ab38a-140">Determine WebView2 Runtime requirement</span></span>  

<span data-ttu-id="ab38a-141">Según el SDK que use, tenga en cuenta los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="ab38a-141">Depending on which SDK you use, consider the following items:</span></span>  

*   <span data-ttu-id="ab38a-142">**C/C++ Win32**.</span><span class="sxs-lookup"><span data-stu-id="ab38a-142">**Win32 C/C++**.</span></span>  <span data-ttu-id="ab38a-143">Cuando use `QueryInterface` para obtener una nueva interfaz, compruebe un valor devuelto de `E_NOINTERFACE` .</span><span class="sxs-lookup"><span data-stu-id="ab38a-143">When using `QueryInterface` to obtain a new interface, verify a return value of `E_NOINTERFACE`.</span></span>  <span data-ttu-id="ab38a-144">El valor puede indicar que el tiempo de ejecución de WebView2 es una versión anterior y no es compatible con esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="ab38a-144">The value may indicate that the WebView2 Runtime is a previous version, and doesn't support that interface.</span></span>  <span data-ttu-id="ab38a-145">Para obtener un ejemplo de cómo funciona, vaya a la [línea 622-AppWindow. cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].</span><span class="sxs-lookup"><span data-stu-id="ab38a-145">For an example of how it works, navigate to [Line 622 - AppWindow.cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].</span></span>  
*   <span data-ttu-id="ab38a-146">**.Net y WinUI**.</span><span class="sxs-lookup"><span data-stu-id="ab38a-146">**.NET and WinUI**.</span></span>  <span data-ttu-id="ab38a-147">Comprueba una `No such interface supported` excepción al usar métodos, propiedades y eventos que se agregaron a SDK más recientes.</span><span class="sxs-lookup"><span data-stu-id="ab38a-147">Check for a `No such interface supported` exception when using methods, properties, and events that were added to more recent SDKs.</span></span>  <span data-ttu-id="ab38a-148">La excepción puede producirse cuando el tiempo de ejecución de WebView2 es una versión anterior y no es compatible con las API.</span><span class="sxs-lookup"><span data-stu-id="ab38a-148">The exception may occur when the WebView2 Runtime is a previous version, and does not support the APIs.</span></span>  
    
<span data-ttu-id="ab38a-149">Si una API no está disponible, considera la posibilidad de quitar la característica asociada o informa a los usuarios de que se requiere una actualización para el tiempo de ejecución de WebView2.</span><span class="sxs-lookup"><span data-stu-id="ab38a-149">If an API is unavailable, consider removing the associated feature, or inform your users that an update to the WebView2 Runtime is required.</span></span>  

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

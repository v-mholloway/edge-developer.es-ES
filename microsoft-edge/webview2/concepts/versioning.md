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
# <span data-ttu-id="d0cbc-104">Comprender las versiones de SDK de WebView2</span><span class="sxs-lookup"><span data-stu-id="d0cbc-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="d0cbc-105">Para desarrollar una aplicación de WebView2, debes instalar el [motor de tiempo de ejecución de WebView2][MicrosoftDeveloperEdgeWebview2] o un canal de [Microsoft Edge no estable][MicrosoftedgeinsiderDownload].</span><span class="sxs-lookup"><span data-stu-id="d0cbc-105">To develop a WebView2 application, you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload].</span></span>  <span data-ttu-id="d0cbc-106">La versión mínima requerida se incluye en la versión del paquete NuGet del SDK.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-106">The minimum version that's required is included in the NuGet package version of the SDK.</span></span>  <span data-ttu-id="d0cbc-107">Por ejemplo, si usa el `SDK package version 0.9.488` , debe instalar el [motor en tiempo de ejecución de WebView2][MicrosoftDeveloperEdgeWebview2] o un canal de [Microsoft Edge no estable][MicrosoftedgeinsiderDownload] con un número de compilación de 488 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-107">For example, if you use the `SDK package version 0.9.488`, then you must install either the [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] or a [non-stable Microsoft Edge channel][MicrosoftedgeinsiderDownload] with a build number of 488 or later.</span></span>  <span data-ttu-id="d0cbc-108">La versión mínima requerida también se especifica en las notas de la [versión][Releasenotes]de WebView2.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-108">The minimum version required is also specified in the WebView2 [Release Notes][Releasenotes].</span></span>  <span data-ttu-id="d0cbc-109">Las nuevas versiones del SDK de WebView2 se distribuyen a la misma cadencia general que el explorador Microsoft Edge \ (cromo \), que es aproximadamente cada seis semanas.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-109">New versions of the WebView2 SDK are shipped at the same general cadence as the Microsoft Edge \(Chromium\) browser, which is approximately every six weeks.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="d0cbc-110">Al desarrollar aplicaciones de WebView2 de hoja perenne, pruebe regularmente la aplicación con las versiones más recientes del tiempo de ejecución de WebView2 y de los exploradores de Microsoft Edge no estables.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-110">When developing Evergreen WebView2 applications, regularly test your application against the latest versions of the WebView2 Runtime and non-stable Microsoft Edge browsers.</span></span>  <span data-ttu-id="d0cbc-111">Debido a que la plataforma web está evolucionando constantemente, la mejor manera de garantizar que tu aplicación funcione como se pretende.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-111">Because the web platform is constantly evolving, regular testing is the best way to ensure your application performs as intended.</span></span>  

## <span data-ttu-id="d0cbc-112">Versión de lanzamiento y versión preliminar</span><span class="sxs-lookup"><span data-stu-id="d0cbc-112">Release and prerelease package</span></span>  

<span data-ttu-id="d0cbc-113">El paquete de NuGet de WebView2 contiene una versión y un paquete de versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-113">The WebView2 NuGet package contains both a release and pre-release package.</span></span>  

<span data-ttu-id="d0cbc-114">El paquete de versión es compatible con versiones posteriores y contiene las [API de C/C++ Win32][ReferenceWin32].</span><span class="sxs-lookup"><span data-stu-id="d0cbc-114">The release package is forward compatible and contains the [Win32 C/C++ APIs][ReferenceWin32].</span></span>  <span data-ttu-id="d0cbc-115">Las API de este SDK son totalmente compatibles.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-115">APIs in this SDK are fully supported.</span></span>  

<span data-ttu-id="d0cbc-116">El paquete de versión preliminar es un supraconjunto del paquete de versiones con los componentes adicionales que se enumeran a continuación.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-116">The prerelease package is a superset of the release package with the additional components listed below.</span></span>  

*   <span data-ttu-id="d0cbc-117">API de .NET: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]y [Core][DotnetMicrosoftWebWebview2CoreNamespace]</span><span class="sxs-lookup"><span data-stu-id="d0cbc-117">.NET APIs: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace], and [Core][DotnetMicrosoftWebWebview2CoreNamespace]</span></span>  
*   <span data-ttu-id="d0cbc-118">API experimentales: para obtener más información, vaya a la sección [API experimentales](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="d0cbc-118">Experimental APIs:  For more information, navigate to the [Experimental APIs](#experimental-apis) section.</span></span>  

## <span data-ttu-id="d0cbc-119">API experimentales</span><span class="sxs-lookup"><span data-stu-id="d0cbc-119">Experimental APIs</span></span>  

<span data-ttu-id="d0cbc-120">El equipo de WebView está probando las API experimentales que pueden estar incluidas en versiones futuras.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-120">The WebView team is testing experimental APIs that may be included in future releases.</span></span>  <span data-ttu-id="d0cbc-121">Las API experimentales se marcan como `experimental` en el SDK.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-121">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="d0cbc-122">Las API experimentales pueden suministrarse como API totalmente estable en el paquete de versión.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-122">Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="d0cbc-123">Puede evaluar las API experimentales y compartir los comentarios con el [repositorio de comentarios de WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="d0cbc-123">You can evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="d0cbc-124">Evite usar las API experimentales en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-124">Avoid using the experimental APIs in production apps.</span></span>  

## <span data-ttu-id="d0cbc-125">Coincidencia de WebView2 versiones en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="d0cbc-125">Matching WebView2 Runtime versions</span></span>  

<span data-ttu-id="d0cbc-126">Al escribir una aplicación de WebView2 con una versión de SDK determinada, los usuarios de la aplicación pueden ejecutarla con varias versiones compatibles del motor en tiempo de ejecución de WebView2.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-126">When writing a WebView2 app using a particular SDK version, users of your app may run it with several compatible versions of the WebView2 Runtime.</span></span>  <span data-ttu-id="d0cbc-127">El equipo de WebView está trabajando en una versión de tiempo de ejecución de WebView2 compatible que contiene las API no experimentales de versiones anteriores del motor de tiempo de ejecución y nuevas API no experimentales.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-127">The WebView team is working on a compatible WebView2 Runtime version that contains non-experimental APIs from previous versions of the Runtime and new non-experimental APIs.</span></span>  

<span data-ttu-id="d0cbc-128">Según el SDK que use, tenga en cuenta los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="d0cbc-128">Depending on which SDK you use, consider the following items:</span></span> 

*   <span data-ttu-id="d0cbc-129">**C/C++ Win32**.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-129">**Win32 C/C++**.</span></span>  <span data-ttu-id="d0cbc-130">Cuando use `QueryInterface` para obtener una nueva interfaz, compruebe si el valor devuelto es `E_NOINTERFACE` .</span><span class="sxs-lookup"><span data-stu-id="d0cbc-130">When using `QueryInterface` to obtain a new interface, check for a return value of `E_NOINTERFACE`.</span></span>  <span data-ttu-id="d0cbc-131">Este valor puede indicar que el tiempo de ejecución de WebView2 es una versión anterior y no es compatible con esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-131">This value may indicate that the WebView2 Runtime is a previous version, and doesn't support that interface.</span></span>  
*   <span data-ttu-id="d0cbc-132">**.Net y WinUI**.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-132">**.NET and WinUI**.</span></span>  <span data-ttu-id="d0cbc-133">Comprueba una `No such interface supported` excepción al usar métodos, propiedades y eventos que se agregaron a SDK más recientes.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-133">Check for a `No such interface supported` exception when using methods, properties, and events that were added to more recent SDKs.</span></span>  <span data-ttu-id="d0cbc-134">Esta excepción puede producirse cuando el tiempo de ejecución de WebView2 es una versión anterior y no es compatible con esas API.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-134">This exception may occur when the WebView2 Runtime is a previous version, and doesn't support those APIs.</span></span>  

<span data-ttu-id="d0cbc-135">Si una API no está disponible, considere la posibilidad de quitar la característica asociada o informe a los usuarios de que necesitan actualizar su versión del tiempo de ejecución de WebView2.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-135">If an API is unavailable, consider removing the associated feature, or inform your users that they need to update their version of the WebView2 Runtime.</span></span>  

<span data-ttu-id="d0cbc-136">Las API experimentales se pueden introducir, modificar y quitar de SDK a SDK.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-136">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="d0cbc-137">Es posible que las API experimentales no estén disponibles en la versión instalada del tiempo de ejecución de WebView2.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-137">Experimental APIs may not be available in your installed version of the WebView2 Runtime.</span></span>  

## <span data-ttu-id="d0cbc-138">Guía básica</span><span class="sxs-lookup"><span data-stu-id="d0cbc-138">Roadmap</span></span>  

<span data-ttu-id="d0cbc-139">El paquete de versión contiene todas las API de C/C++ de Win32, estables y estables.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-139">The release package contains all of the stable, supported Win32 C/C++ APIs.</span></span>  <span data-ttu-id="d0cbc-140">En el futuro, el paquete de versión contendrá todas las API de .NET compatibles y estables cuando estén disponibles para el público.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-140">In the future, the release package will contain all stable, supported .NET APIs when they are made generally available.</span></span>  <span data-ttu-id="d0cbc-141">El paquete de versión preliminar contiene las API experimentales que están sujetas a cambios en función de los comentarios y de la información compartida.</span><span class="sxs-lookup"><span data-stu-id="d0cbc-141">The prerelease package contains experimental APIs that are subject to change based upon your feedback and shared insights.</span></span>  

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

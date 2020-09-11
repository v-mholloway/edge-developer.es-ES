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
# <span data-ttu-id="6fe81-104">Comprender las versiones de SDK de WebView2</span><span class="sxs-lookup"><span data-stu-id="6fe81-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="6fe81-105">WebView2 depende de Microsoft Edge para funcionar.</span><span class="sxs-lookup"><span data-stu-id="6fe81-105">WebView2 depends on Microsoft Edge to function.</span></span>  <span data-ttu-id="6fe81-106">Cada SDK de WebView2 requiere que se instale una versión mínima del explorador.</span><span class="sxs-lookup"><span data-stu-id="6fe81-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="6fe81-107">La versión mínima se refleja en la versión del paquete del SDK.</span><span class="sxs-lookup"><span data-stu-id="6fe81-107">The minimum version is reflected in the package version of the SDK.</span></span>  <span data-ttu-id="6fe81-108">Por ejemplo, si usa el `SDK package version 0.9.488` , debe instalar Microsoft Edge con un número de compilación de 488 o posterior.</span><span class="sxs-lookup"><span data-stu-id="6fe81-108">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span>  <span data-ttu-id="6fe81-109">La versión del explorador también se especifica en las [notas][Releasenotes]de la versión de WebView2.</span><span class="sxs-lookup"><span data-stu-id="6fe81-109">The browser version is also specified in the WebView2 [Release Notes][Releasenotes].</span></span>  <span data-ttu-id="6fe81-110">Para obtener más información sobre la versión más reciente del explorador Microsoft Edge, vaya a [canales de explorador][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="6fe81-110">For more information about the latest release of the Microsoft Edge browser, navigate to [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="6fe81-111">WebView2 está actualmente en versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="6fe81-111">WebView2 is currently in preview.</span></span>  <span data-ttu-id="6fe81-112">Mientras el equipo de WebView se esfuerza por garantizar la compatibilidad con versiones anteriores de los exploradores y las versiones del explorador, no se garantiza porque es posible que las versiones más recientes del explorador no admitan las versiones anteriores del SDK.</span><span class="sxs-lookup"><span data-stu-id="6fe81-112">While the WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed because newer versions of the browser may not support previous SDK versions.</span></span>  <span data-ttu-id="6fe81-113">Si hay cambios importantes entre las versiones del explorador y los SDK, los cambios se especifican en las notas de la [versión][Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="6fe81-113">If there are breaking changes between browser versions and SDKs, the changes are specified in the [Release Notes][Releasenotes].</span></span>  

<span data-ttu-id="6fe81-114">En el futuro, el equipo de WebView planea cambiar el modelo de distribución de las aplicaciones de WebView2.</span><span class="sxs-lookup"><span data-stu-id="6fe81-114">In the future, the WebView team plans to change the distribution model for WebView2 apps.</span></span>  <span data-ttu-id="6fe81-115">Para obtener más información, vaya al [modo de distribución de perenne][DistributionEvergreenMode].</span><span class="sxs-lookup"><span data-stu-id="6fe81-115">For more information, navigate to [Evergreen distribution mode][DistributionEvergreenMode].</span></span>  

## <span data-ttu-id="6fe81-116">Versión de lanzamiento y versión preliminar</span><span class="sxs-lookup"><span data-stu-id="6fe81-116">Release and prerelease package</span></span>  

<span data-ttu-id="6fe81-117">En la versión preliminar, el paquete de versión contiene lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="6fe81-117">In preview, the release package contains the following.</span></span>  

*   <span data-ttu-id="6fe81-118">[API Win32 C/C++][ReferenceWin3209622]: API en el SDK que se espera que permanezcan iguales en la GA.</span><span class="sxs-lookup"><span data-stu-id="6fe81-118">[Win32 C/C++ APIs][ReferenceWin3209622]: APIs in the SDK that are expected to remain the same at GA.</span></span>  

<span data-ttu-id="6fe81-119">En la versión preliminar, el paquete de versión preliminar contiene los siguientes componentes.</span><span class="sxs-lookup"><span data-stu-id="6fe81-119">In preview, the prerelease package contains the following components.</span></span>  

*   <span data-ttu-id="6fe81-120">API de .NET: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]y [Core][ReferenceDotnet09628]</span><span class="sxs-lookup"><span data-stu-id="6fe81-120">.NET APIs: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515], and [Core][ReferenceDotnet09628]</span></span>  
*   <span data-ttu-id="6fe81-121">API experimentales.</span><span class="sxs-lookup"><span data-stu-id="6fe81-121">Experimental APIs.</span></span>  <span data-ttu-id="6fe81-122">Para obtener más información, vea la sección [API experimentales](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="6fe81-122">For more information, see the [Experimental APIs](#experimental-apis) section.</span></span>  

## <span data-ttu-id="6fe81-123">API experimentales</span><span class="sxs-lookup"><span data-stu-id="6fe81-123">Experimental APIs</span></span>  

<span data-ttu-id="6fe81-124">El equipo de WebView está probando las API experimentales que pueden representar la funcionalidad futura.</span><span class="sxs-lookup"><span data-stu-id="6fe81-124">The WebView team is testing experimental APIs that may represent future functionality.</span></span>  <span data-ttu-id="6fe81-125">Las API experimentales se marcan como `experimental` en el SDK.</span><span class="sxs-lookup"><span data-stu-id="6fe81-125">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="6fe81-126">Las API experimentales pueden suministrarse como API totalmente estable en el paquete de versión.</span><span class="sxs-lookup"><span data-stu-id="6fe81-126">Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="6fe81-127">Debes esperar que todas las API experimentales cambien antes de su liberación.</span><span class="sxs-lookup"><span data-stu-id="6fe81-127">You should expect all experimental APIs to change before release.</span></span>  <span data-ttu-id="6fe81-128">Evalúa las API experimentales y comparte tus comentarios con el [repositorio de comentarios de WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="6fe81-128">Please evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

> [!CAUTION]
> <span data-ttu-id="6fe81-129">Evite usar las API experimentales en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6fe81-129">Avoid using the experimental APIs in production apps.</span></span>  

## <span data-ttu-id="6fe81-130">Coincidencia de WebView2 versiones en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="6fe81-130">Matching WebView2 Runtime versions</span></span>  

<span data-ttu-id="6fe81-131">Al escribir una aplicación de WebView2 con una versión de SDK determinada, los usuarios de tu aplicación pueden ejecutarla con varias versiones compatibles del tiempo de ejecución de WebView2.</span><span class="sxs-lookup"><span data-stu-id="6fe81-131">When writing a WebView2 app using a particular SDK version, the users fo you app may run your it with various compatible versions of the WebView2 Runtime.</span></span>  <span data-ttu-id="6fe81-132">En el futuro, una versión de tiempo de ejecución de WebView2 compatible más reciente contiene todas las API no experimentales de una versión de tiempo de ejecución de WebView2 compatible anterior, además de nuevas API no experimentales.</span><span class="sxs-lookup"><span data-stu-id="6fe81-132">In the future, a newer compatible WebView2 Runtime version contains all the non-experimental APIs from an older compatible WebView2 Runtime version plus additional new non-experimental APIs.</span></span>  

*   <span data-ttu-id="6fe81-133">Los programadores de **Win32 C/C++** , cuando `QueryInterface` se usan para obtener una nueva interfaz, deben comprobar un valor devuelto de `E_NOINTERFACE` , lo que puede indicar que el tiempo de ejecución de WebView2 es más antiguo y no es compatible con esa interfaz en particular.</span><span class="sxs-lookup"><span data-stu-id="6fe81-133">**Win32 C/C++** developers, when using `QueryInterface` to obtain a new interface, should check for a return value of `E_NOINTERFACE`, which may indicate that the WebView2 Runtime is older and does not support that particular interface.</span></span>  
*   <span data-ttu-id="6fe81-134">Los desarrolladores de **.net y WinUI** deben comprobar una `No such interface supported` excepción al usar métodos, propiedades y eventos agregados en SDK posteriores, que pueden ocurrir cuando el tiempo de ejecución de WebView2 es más antiguo y no es compatible con esas API específicas.</span><span class="sxs-lookup"><span data-stu-id="6fe81-134">**.NET and WinUI** developers should check for a `No such interface supported` exception when using methods, properties, and events added in later SDKs which may occur when the WebView2 Runtime is older and does not support those particular APIs.</span></span>  

<span data-ttu-id="6fe81-135">Si una API no está disponible, considera la posibilidad de deshabilitar la característica asociada, si es posible, o de informar al usuario final de que necesitan actualizar su WebView2 versión de tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="6fe81-135">If an API is unavailable, consider disabling the associated feature, if possible, or otherwise informing the end user they need to update their WebView2 Runtime version.</span></span>  

<span data-ttu-id="6fe81-136">Las API experimentales se pueden introducir, modificar y quitar de SDK a SDK.</span><span class="sxs-lookup"><span data-stu-id="6fe81-136">Experimental APIs may be introduced, modified, and removed from SDK to SDK.</span></span>  <span data-ttu-id="6fe81-137">Al intentar usar una API experimental que no está disponible en el tiempo de ejecución de WebView2, es posible que observe el mismo comportamiento descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6fe81-137">When attempting to use an experimental API that is not available in the WebView2 Runtime you may observe the same previously described behavior.</span></span>  

## <span data-ttu-id="6fe81-138">Guía básica</span><span class="sxs-lookup"><span data-stu-id="6fe81-138">Roadmap</span></span>  

<span data-ttu-id="6fe81-139">Después de que WebView2 alcance un estado de disponibilidad general estable, el paquete de versión contiene todas las API de Win32 C/C++ y .NET estables.</span><span class="sxs-lookup"><span data-stu-id="6fe81-139">After WebView2 reaches a stable general available state, the release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="6fe81-140">El paquete de versión preliminar contiene las API experimentales que están sujetas a cambios en función de los comentarios y de la información compartida.</span><span class="sxs-lookup"><span data-stu-id="6fe81-140">The prerelease package contains experimental APIs that are subject to change based upon your feedback and shared insights.</span></span>  

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

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
# <span data-ttu-id="16d87-104">Comprender las versiones de SDK de WebView2</span><span class="sxs-lookup"><span data-stu-id="16d87-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="16d87-105">WebView2 depende de Microsoft Edge para funcionar.</span><span class="sxs-lookup"><span data-stu-id="16d87-105">WebView2 depends on Microsoft Edge to function.</span></span> <span data-ttu-id="16d87-106">Cada SDK de WebView2 requiere que se instale una versión mínima del explorador.</span><span class="sxs-lookup"><span data-stu-id="16d87-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="16d87-107">La versión mínima se refleja en la versión del paquete del SDK.</span><span class="sxs-lookup"><span data-stu-id="16d87-107">The minimum version is reflected in the package version of the SDK.</span></span>  <span data-ttu-id="16d87-108">Por ejemplo, si usa el `SDK package version 0.9.488` , debe instalar Microsoft Edge con un número de compilación de 488 o posterior.</span><span class="sxs-lookup"><span data-stu-id="16d87-108">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span> <span data-ttu-id="16d87-109">La versión del explorador también se especifica en las [notas][Webview2Releasenotes]de la versión de WebView2.</span><span class="sxs-lookup"><span data-stu-id="16d87-109">The browser version is also specified in the WebView2 [Release Notes][Webview2Releasenotes].</span></span>  <span data-ttu-id="16d87-110">Para obtener más información sobre las versiones más recientes del explorador, vea [canales de explorador][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="16d87-110">For more information on the latest releases of the browser, see [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="16d87-111">WebView2 está actualmente en versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="16d87-111">WebView2 is currently in preview.</span></span>  <span data-ttu-id="16d87-112">Mientras que el equipo de WebView de Microsoft Edge se esfuerza por garantizar la compatibilidad con versiones anteriores de los exploradores y los SDK, no se garantiza que algunas versiones más recientes del explorador no admitan versiones anteriores de SDK.</span><span class="sxs-lookup"><span data-stu-id="16d87-112">While, the Microsoft Edge WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed as some newer versions of the browser may not support older SDK versions.</span></span>  <span data-ttu-id="16d87-113">Si hay cambios importantes entre las versiones del explorador y los SDK, el equipo de WebView de Microsoft Edge especifica los cambios en las notas de la [versión][Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="16d87-113">If there are breaking changes between browser versions and SDKs, the Microsoft Edge WebView team specifies the changes in the [release notes][Webview2Releasenotes].</span></span>  

<span data-ttu-id="16d87-114">En el futuro, el modelo de distribución para las aplicaciones de WebView2 cambiará.</span><span class="sxs-lookup"><span data-stu-id="16d87-114">In the future, the distribution model for WebView2 applications will change.</span></span> <span data-ttu-id="16d87-115">Para obtener más información, consulte [WebView2 Runtime][Webview2IndexEdgeRuntime].</span><span class="sxs-lookup"><span data-stu-id="16d87-115">For more information, see [WebView2 Runtime][Webview2IndexEdgeRuntime].</span></span>  
 
## <span data-ttu-id="16d87-116">Versión y paquete preliminar</span><span class="sxs-lookup"><span data-stu-id="16d87-116">Release and pre-release package</span></span>  

<span data-ttu-id="16d87-117">En la versión preliminar, el paquete de versión contiene lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="16d87-117">In preview, the release package contains the following.</span></span>  

*   <span data-ttu-id="16d87-118">[API Win32 C/C++][Webview2ReferenceWin3209538]: API en el SDK que se espera que permanezcan iguales en la GA.</span><span class="sxs-lookup"><span data-stu-id="16d87-118">[Win32 C/C++ APIs][Webview2ReferenceWin3209538]: APIs in the SDK that are expected to remain the same at GA.</span></span> 

<span data-ttu-id="16d87-119">En la versión preliminar, el paquete preliminar contiene lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="16d87-119">In preview, the pre-release package contains the following.</span></span>  

*   <span data-ttu-id="16d87-120">API de .NET: [WPF][Webview2ReferenceWpf09515], [WinForms][Webview2ReferenceWinforms09515]y [Core][Webview2ReferenceDotnet09538]</span><span class="sxs-lookup"><span data-stu-id="16d87-120">.NET APIs: [WPF][Webview2ReferenceWpf09515], [WinForms][Webview2ReferenceWinforms09515], and [Core][Webview2ReferenceDotnet09538]</span></span>
*   <span data-ttu-id="16d87-121">API experimentales.</span><span class="sxs-lookup"><span data-stu-id="16d87-121">Experimental APIs.</span></span>  <span data-ttu-id="16d87-122">Para obtener más información, consulta la sección [API de Experimantal](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="16d87-122">For more information, see the [Experimantal APIs](#experimental-apis) section.</span></span>  

### <span data-ttu-id="16d87-123">API experimentales</span><span class="sxs-lookup"><span data-stu-id="16d87-123">Experimental APIs</span></span>  

<span data-ttu-id="16d87-124">El equipo de WebView está probando las API que representan la futura funcionalidad denominada API experimental.</span><span class="sxs-lookup"><span data-stu-id="16d87-124">The WebView Team is testing APIs that represent future functionality named Experimental APIs.</span></span>  <span data-ttu-id="16d87-125">Las API experimentales se marcan como `experimental` en el SDK.</span><span class="sxs-lookup"><span data-stu-id="16d87-125">The Experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="16d87-126">Algunas API experimentales pueden suministrarse como API totalmente estable en el paquete de versión.</span><span class="sxs-lookup"><span data-stu-id="16d87-126">Some Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="16d87-127">Debes esperar que todas las API experimentales cambien antes de su liberación.</span><span class="sxs-lookup"><span data-stu-id="16d87-127">You should expect all experimental APIs to change before release.</span></span>  <span data-ttu-id="16d87-128">Evalúa las API experimentales y comparte tus comentarios con el [repositorio de comentarios de WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="16d87-128">Please evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>   

> [!CAUTION]
> <span data-ttu-id="16d87-129">Evite usar las API experimentales en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="16d87-129">Avoid using the experimental APIs in production applications.</span></span>  

### <span data-ttu-id="16d87-130">Guía básica</span><span class="sxs-lookup"><span data-stu-id="16d87-130">Roadmap</span></span>  

<span data-ttu-id="16d87-131">Después de que WebView2 alcance un estado de disponibilidad general estable, el paquete de versión contiene todas las API de Win32 C/C++ y .NET estables.</span><span class="sxs-lookup"><span data-stu-id="16d87-131">After WebView2 reaches a stable general available state, the release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="16d87-132">El paquete preliminar contiene las API experimentales que están sujetas a cambio en función de los comentarios del desarrollador y de la información compartida.</span><span class="sxs-lookup"><span data-stu-id="16d87-132">The pre-release package contains experimental APIs that are subject to change based upon developer feedback and shared insights.</span></span>  

<!--links -->

[Webview2IndexEdgeRuntime]: ./distribution.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2 Runtime: distribución de aplicaciones con WebView2 | Microsoft docs"  
[Webview2ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[Webview2ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[Webview2ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[Webview2ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[Webview2Releasenotes]: ../releasenotes.md "Notas de la versión para el SDK de WebView2 | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Información general de los canales de Microsoft Edge | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

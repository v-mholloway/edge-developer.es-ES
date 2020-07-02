---
description: Modelos de control de versiones usados para Microsoft Edge WebView2
title: Control de versiones de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 059bbeb34f372af0cef944e484599c0b50543cc9
ms.sourcegitcommit: 288bd2a1bec418a84d1f0bda013c1913886bd269
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844428"
---
# <span data-ttu-id="6ed47-104">Comprender las versiones de SDK de WebView2</span><span class="sxs-lookup"><span data-stu-id="6ed47-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="6ed47-105">WebView2 depende de Microsoft Edge para funcionar.</span><span class="sxs-lookup"><span data-stu-id="6ed47-105">WebView2 depends on Microsoft Edge to function.</span></span>  <span data-ttu-id="6ed47-106">Cada SDK de WebView2 requiere que se instale una versión mínima del explorador.</span><span class="sxs-lookup"><span data-stu-id="6ed47-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="6ed47-107">La versión mínima se refleja en la versión del paquete del SDK.</span><span class="sxs-lookup"><span data-stu-id="6ed47-107">The minimum version is reflected in the package version of the SDK.</span></span>  <span data-ttu-id="6ed47-108">Por ejemplo, si usa el `SDK package version 0.9.488` , debe instalar Microsoft Edge con un número de compilación de 488 o posterior.</span><span class="sxs-lookup"><span data-stu-id="6ed47-108">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span>  <span data-ttu-id="6ed47-109">La versión del explorador también se especifica en las [notas][Releasenotes]de la versión de WebView2.</span><span class="sxs-lookup"><span data-stu-id="6ed47-109">The browser version is also specified in the WebView2 [Release Notes][Releasenotes].</span></span>  <span data-ttu-id="6ed47-110">Para obtener más información sobre las versiones más recientes del explorador, vea [canales de explorador][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="6ed47-110">For more information on the latest releases of the browser, see [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="6ed47-111">WebView2 está actualmente en versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="6ed47-111">WebView2 is currently in preview.</span></span>  <span data-ttu-id="6ed47-112">Mientras el equipo de WebView se esfuerza por garantizar la compatibilidad con versiones anteriores de los exploradores y las versiones del explorador, no se garantiza porque es posible que las versiones más recientes del explorador no admitan versiones anteriores del SDK.</span><span class="sxs-lookup"><span data-stu-id="6ed47-112">While the WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed since newer versions of the browser may not support older SDK versions.</span></span>  <span data-ttu-id="6ed47-113">Si hay cambios importantes entre las versiones del explorador y los SDK, el equipo de WebView especifica los cambios en las notas de la [versión][Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="6ed47-113">If there are breaking changes between browser versions and SDKs, the WebView team specifies the changes in the [release notes][Releasenotes].</span></span>  

<span data-ttu-id="6ed47-114">En el futuro, el equipo de WebView planea cambiar el modelo de distribución de las aplicaciones de WebView2.</span><span class="sxs-lookup"><span data-stu-id="6ed47-114">In the future, the  WebView team plans to change the distribution model for WebView2 applications.</span></span>  <span data-ttu-id="6ed47-115">Para obtener más información, consulte ver el [modo de distribución de perenne][DistributionEvergreenMode].</span><span class="sxs-lookup"><span data-stu-id="6ed47-115">For more information, see see [Evergreen distribution mode][DistributionEvergreenMode].</span></span>  
 
## <span data-ttu-id="6ed47-116">Versión y paquete preliminar</span><span class="sxs-lookup"><span data-stu-id="6ed47-116">Release and pre-release package</span></span>  

<span data-ttu-id="6ed47-117">En la versión preliminar, el paquete de versión contiene lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="6ed47-117">In preview, the release package contains the following.</span></span>  

*   <span data-ttu-id="6ed47-118">[API Win32 C/C++][ReferenceWin3209538]: API en el SDK que se espera que permanezcan iguales en la GA.</span><span class="sxs-lookup"><span data-stu-id="6ed47-118">[Win32 C/C++ APIs][ReferenceWin3209538]: APIs in the SDK that are expected to remain the same at GA.</span></span> 

<span data-ttu-id="6ed47-119">En la versión preliminar, el paquete anterior contiene los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="6ed47-119">In preview, the pre-release package contains the following components.</span></span>  

*   <span data-ttu-id="6ed47-120">API de .NET: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]y [Core][ReferenceDotnet09538]</span><span class="sxs-lookup"><span data-stu-id="6ed47-120">.NET APIs: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515], and [Core][ReferenceDotnet09538]</span></span>
*   <span data-ttu-id="6ed47-121">API experimentales.</span><span class="sxs-lookup"><span data-stu-id="6ed47-121">Experimental APIs.</span></span>  <span data-ttu-id="6ed47-122">Para obtener más información, vea la sección [API experimentales](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="6ed47-122">For more information, see the [Experimental APIs](#experimental-apis) section.</span></span>  

### <span data-ttu-id="6ed47-123">API experimentales</span><span class="sxs-lookup"><span data-stu-id="6ed47-123">Experimental APIs</span></span>  

<span data-ttu-id="6ed47-124">El equipo de WebView está probando las API que representan la futura funcionalidad denominada API experimental.</span><span class="sxs-lookup"><span data-stu-id="6ed47-124">The WebView Team is testing APIs that represent future functionality named Experimental APIs.</span></span>  <span data-ttu-id="6ed47-125">Las API experimentales se marcan como `experimental` en el SDK.</span><span class="sxs-lookup"><span data-stu-id="6ed47-125">The Experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="6ed47-126">Algunas API experimentales pueden suministrarse como API totalmente estable en el paquete de versión.</span><span class="sxs-lookup"><span data-stu-id="6ed47-126">Some Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="6ed47-127">Debes esperar que todas las API experimentales cambien antes de su liberación.</span><span class="sxs-lookup"><span data-stu-id="6ed47-127">You should expect all experimental APIs to change before release.</span></span>  <span data-ttu-id="6ed47-128">Evalúa las API experimentales y comparte tus comentarios con el [repositorio de comentarios de WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="6ed47-128">Please evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>   

> [!CAUTION]
> <span data-ttu-id="6ed47-129">Evite usar las API experimentales en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6ed47-129">Avoid using the experimental APIs in production applications.</span></span>  

### <span data-ttu-id="6ed47-130">Guía básica</span><span class="sxs-lookup"><span data-stu-id="6ed47-130">Roadmap</span></span>  

<span data-ttu-id="6ed47-131">Después de que WebView2 alcance un estado de disponibilidad general estable, el paquete de versión contiene todas las API de Win32 C/C++ y .NET estables.</span><span class="sxs-lookup"><span data-stu-id="6ed47-131">After WebView2 reaches a stable general available state, the release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="6ed47-132">El paquete preliminar contiene las API experimentales que están sujetas a cambio en función de los comentarios del desarrollador y de la información compartida.</span><span class="sxs-lookup"><span data-stu-id="6ed47-132">The pre-release package contains experimental APIs that are subject to change based upon developer feedback and shared insights.</span></span>  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Modo de distribución de hoja perenne: distribución de aplicaciones mediante WebView2 | Microsoft docs"  
[ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[Releasenotes]: ../releasenotes.md "Notas de la versión para el SDK de WebView2 | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Información general de los canales de Microsoft Edge | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

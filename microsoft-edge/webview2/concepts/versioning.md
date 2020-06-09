---
description: Modelos de control de versiones usados para Microsoft Edge WebView2
title: Control de versiones de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: cc924a146057a3c8c578ccea187e1dd63dedcbe6
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697220"
---
# <span data-ttu-id="74d60-104">Descripción de las versiones y WebView2 del explorador</span><span class="sxs-lookup"><span data-stu-id="74d60-104">Understanding browser versions and WebView2</span></span>  

<span data-ttu-id="74d60-105">WebView2 depende de Microsoft Edge para funcionar.</span><span class="sxs-lookup"><span data-stu-id="74d60-105">WebView2 depends on Microsoft Edge to function.</span></span>  <span data-ttu-id="74d60-106">Cada SDK de WebView2 requiere que se instale una versión mínima del explorador.</span><span class="sxs-lookup"><span data-stu-id="74d60-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="74d60-107">Esta versión del explorador se especifica en nuestras notas de la [versión][Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="74d60-107">This browser version is specified in our [Release Notes][Webview2Releasenotes].</span></span>  <span data-ttu-id="74d60-108">Es posible que vea la versión mínima reflejada en la versión del paquete de SDK.</span><span class="sxs-lookup"><span data-stu-id="74d60-108">You may see the minimum version reflected in the package version of the SDK.</span></span>  <span data-ttu-id="74d60-109">Por ejemplo, si usa el `SDK package version 0.9.488` , debe instalar Microsoft Edge con un número de compilación de 488 o posterior.</span><span class="sxs-lookup"><span data-stu-id="74d60-109">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span>  <span data-ttu-id="74d60-110">Para obtener más información sobre las versiones más recientes del explorador, vea [canales de explorador][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="74d60-110">For more information on the latest releases of the browser, see [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="74d60-111">WebView2 está actualmente en versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="74d60-111">WebView2 is currently in Preview.</span></span>  <span data-ttu-id="74d60-112">Mientras que el equipo de WebView de Microsoft Edge se esfuerza por garantizar la compatibilidad con versiones anteriores de los exploradores y los SDK, no se garantiza que algunas versiones más recientes del explorador no admitan versiones anteriores de SDK.</span><span class="sxs-lookup"><span data-stu-id="74d60-112">While, the Microsoft Edge WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed as some newer versions of the browser may not support older SDK versions.</span></span>  <span data-ttu-id="74d60-113">Si hay cambios importantes entre las versiones del explorador y los SDK, el equipo de WebView de Microsoft Edge indica los cambios en las notas de la [versión][Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="74d60-113">If there are breaking changes between browser versions and SDKs, the Microsoft Edge WebView team indicates the changes in the [release notes][Webview2Releasenotes].</span></span>  

<span data-ttu-id="74d60-114">En el futuro, el equipo de WebView de Microsoft Edge planea cambiar el modelo de distribución.</span><span class="sxs-lookup"><span data-stu-id="74d60-114">In the future, the Microsoft Edge WebView team plans to change the distribution model.</span></span>  <span data-ttu-id="74d60-115">El equipo de WebView de Microsoft Edge planea quitar la dependencia directa en el explorador Microsoft Edge de WebView2.</span><span class="sxs-lookup"><span data-stu-id="74d60-115">The Microsoft Edge WebView team plans to remove the direct dependency on the Microsoft Edge browser from WebView2.</span></span>  <span data-ttu-id="74d60-116">Para obtener más información, vea [WebView2 Runtime][Webview2IndexEdgeRuntime] en la sección de [distribución][Webview2Distibution] .</span><span class="sxs-lookup"><span data-stu-id="74d60-116">To learn more, see [WebView2 Runtime][Webview2IndexEdgeRuntime] in the [Distribution][Webview2Distibution] section.</span></span>  

## <span data-ttu-id="74d60-117">API experimentales</span><span class="sxs-lookup"><span data-stu-id="74d60-117">Experimental APIs</span></span>  

<span data-ttu-id="74d60-118">Aunque WebView2 es una versión preliminar, se espera que las API del SDK permanezcan igual en GA.</span><span class="sxs-lookup"><span data-stu-id="74d60-118">While WebView2 is a preview, the APIs in the SDK are expected to remain the same at GA.</span></span>  <span data-ttu-id="74d60-119">Hay [API experimentales][Webview2ReferenceWin3209538Experimental] incluidas en el SDK.</span><span class="sxs-lookup"><span data-stu-id="74d60-119">There are [experimental APIs][Webview2ReferenceWin3209538Experimental] included in the SDK.</span></span>  <span data-ttu-id="74d60-120">Evalúe las API experimentales y envíe sus comentarios con el [repositorio de comentarios de WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="74d60-120">Please evaluate the experimental APIs and send your feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

### <span data-ttu-id="74d60-121">Guía básica</span><span class="sxs-lookup"><span data-stu-id="74d60-121">Roadmap</span></span>  

<span data-ttu-id="74d60-122">Después de que WebView2 alcance un estado de disponibilidad general estable y publicamos el SDK de la versión 1.0.0, el equipo de WebView de Microsoft Edge planea mover todas las API experimentales a un paquete preliminar.</span><span class="sxs-lookup"><span data-stu-id="74d60-122">After WebView2 reaches a stable general available state and we release the 1.0.0 SDK, the Microsoft Edge WebView team plans to move all experimental APIs to a pre-release package.</span></span>  <span data-ttu-id="74d60-123">La versión preliminar del paquete continúa permitiendo los comentarios y la comprensión de las características más recientes, mientras que la versión estable mantiene la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="74d60-123">The pre-release package continues to allow for feedback and insight into the latest features, while the stable release version maintains backward compatibility.</span></span>  

<!--links -->

[Webview2Distibution]: ./distribution.md "Distribución de aplicaciones mediante WebView2 | Microsoft docs"  
[Webview2IndexEdgeRuntime]: ./distribution.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2 Runtime: distribución de aplicaciones con WebView2 | Microsoft docs"  
[Webview2ReferenceWin3209538Experimental]: ../reference/win32/0-9-538-reference-webview2.md#experimental "Experimental-referencia (WebView2) | Microsoft docs"  
[Webview2Releasenotes]: ../releasenotes.md "Notas de la versión para el SDK de WebView2 | Microsoft docs"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Información general de los canales de Microsoft Edge | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

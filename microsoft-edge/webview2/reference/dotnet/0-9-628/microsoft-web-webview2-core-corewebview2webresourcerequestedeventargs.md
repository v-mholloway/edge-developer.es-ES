---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 501483894a2abca58c5a1856ab587b93be904c8b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012626"
---
# <span data-ttu-id="aa7ad-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="aa7ad-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

<span data-ttu-id="aa7ad-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="aa7ad-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="aa7ad-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="aa7ad-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="aa7ad-107">Argumentos de evento para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="aa7ad-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="aa7ad-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="aa7ad-108">Summary</span></span>

 <span data-ttu-id="aa7ad-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="aa7ad-109">Members</span></span>                        | <span data-ttu-id="aa7ad-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="aa7ad-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aa7ad-111">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aa7ad-111">Request</span></span>](#request) | <span data-ttu-id="aa7ad-112">La solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="aa7ad-112">The Web resource request.</span></span>
[<span data-ttu-id="aa7ad-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="aa7ad-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="aa7ad-114">El contexto de la solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="aa7ad-114">The web resource request context.</span></span>
[<span data-ttu-id="aa7ad-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa7ad-115">Response</span></span>](#response) | <span data-ttu-id="aa7ad-116">Un marcador de posición para el objeto de respuesta de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="aa7ad-116">A placeholder for the web resource response object.</span></span>
[<span data-ttu-id="aa7ad-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="aa7ad-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="aa7ad-118">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="aa7ad-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="aa7ad-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="aa7ad-119">Members</span></span>

#### <span data-ttu-id="aa7ad-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aa7ad-120">Request</span></span> 

<span data-ttu-id="aa7ad-121">La solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="aa7ad-121">The Web resource request.</span></span>

> <span data-ttu-id="aa7ad-122">[solicitud](#request) de [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md) pública</span><span class="sxs-lookup"><span data-stu-id="aa7ad-122">public [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md) [Request](#request)</span></span>

<span data-ttu-id="aa7ad-123">Es posible que en el objeto de solicitud falten algunos encabezados que la pila de red agrega más adelante.</span><span class="sxs-lookup"><span data-stu-id="aa7ad-123">The request object may be missing some headers that are added by network stack later on.</span></span>

#### <span data-ttu-id="aa7ad-124">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="aa7ad-124">ResourceContext</span></span> 

<span data-ttu-id="aa7ad-125">El contexto de la solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="aa7ad-125">The web resource request context.</span></span>

> <span data-ttu-id="aa7ad-126">[CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) pública [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="aa7ad-126">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="aa7ad-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa7ad-127">Response</span></span> 

<span data-ttu-id="aa7ad-128">Un marcador de posición para el objeto de respuesta de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="aa7ad-128">A placeholder for the web resource response object.</span></span>

> <span data-ttu-id="aa7ad-129">[respuesta](#response) de [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) pública</span><span class="sxs-lookup"><span data-stu-id="aa7ad-129">public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [Response](#response)</span></span>

<span data-ttu-id="aa7ad-130">Si se establece este objeto, la solicitud de recursos Web se completará con esta respuesta.</span><span class="sxs-lookup"><span data-stu-id="aa7ad-130">If this object is set, the web resource request will be completed with this response.</span></span> <span data-ttu-id="aa7ad-131">Se puede crear un objeto de respuesta de recursos Web vacío con CreateWebResourceResponse y, a continuación, se ha modificado para construir la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aa7ad-131">An empty Web resource response object can be created with CreateWebResourceResponse and then modified to construct the response.</span></span>

#### <span data-ttu-id="aa7ad-132">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="aa7ad-132">GetDeferral</span></span> 

<span data-ttu-id="aa7ad-133">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="aa7ad-133">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="aa7ad-134">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="aa7ad-134">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="aa7ad-135">Puedes usar el objeto CoreWebView2Deferral para completar la solicitud más adelante.</span><span class="sxs-lookup"><span data-stu-id="aa7ad-135">You can use the CoreWebView2Deferral object to complete the request at a later time.</span></span>


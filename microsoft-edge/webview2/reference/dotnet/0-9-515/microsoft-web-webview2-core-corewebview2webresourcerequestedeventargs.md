---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 9210a4b70d0e2edf30cbaad906f57b360688dfe8
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655157"
---
# <span data-ttu-id="9100d-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9100d-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

<span data-ttu-id="9100d-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="9100d-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="9100d-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="9100d-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="9100d-107">Argumentos de evento para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9100d-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="9100d-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="9100d-108">Summary</span></span>

 <span data-ttu-id="9100d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9100d-109">Members</span></span>                        | <span data-ttu-id="9100d-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9100d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9100d-111">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9100d-111">Request</span></span>](#request) | <span data-ttu-id="9100d-112">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="9100d-112">The HTTP request.</span></span>
[<span data-ttu-id="9100d-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="9100d-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="9100d-114">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="9100d-114">The web resource request contexts.</span></span>
[<span data-ttu-id="9100d-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9100d-115">Response</span></span>](#response) | <span data-ttu-id="9100d-116">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="9100d-116">The HTTP response.</span></span>
[<span data-ttu-id="9100d-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="9100d-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="9100d-118">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="9100d-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="9100d-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="9100d-119">Members</span></span>

#### <span data-ttu-id="9100d-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9100d-120">Request</span></span> 

<span data-ttu-id="9100d-121">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="9100d-121">The HTTP request.</span></span>

> <span data-ttu-id="9100d-122">[solicitud](#request) de HttpRequestMessage pública</span><span class="sxs-lookup"><span data-stu-id="9100d-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="9100d-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="9100d-123">ResourceContext</span></span> 

<span data-ttu-id="9100d-124">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="9100d-124">The web resource request contexts.</span></span>

> <span data-ttu-id="9100d-125">[CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) pública [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="9100d-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="9100d-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9100d-126">Response</span></span> 

<span data-ttu-id="9100d-127">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="9100d-127">The HTTP response.</span></span>

> <span data-ttu-id="9100d-128">[respuesta](#response) de HttpResponseMessage pública</span><span class="sxs-lookup"><span data-stu-id="9100d-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="9100d-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="9100d-129">GetDeferral</span></span> 

<span data-ttu-id="9100d-130">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="9100d-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="9100d-131">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="9100d-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="9100d-132">Puede usar el objeto CoreWebView2Deferral para completar la solicitud de red más adelante.</span><span class="sxs-lookup"><span data-stu-id="9100d-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>


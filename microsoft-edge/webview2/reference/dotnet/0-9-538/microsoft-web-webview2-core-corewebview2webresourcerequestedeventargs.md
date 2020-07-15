---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 53cc31bc714417ab902fa8fdef9fd83f80871f10
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879670"
---
# <span data-ttu-id="48fa1-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="48fa1-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

<span data-ttu-id="48fa1-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="48fa1-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="48fa1-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="48fa1-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="48fa1-107">Argumentos de evento para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="48fa1-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="48fa1-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="48fa1-108">Summary</span></span>

 <span data-ttu-id="48fa1-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="48fa1-109">Members</span></span>                        | <span data-ttu-id="48fa1-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="48fa1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="48fa1-111">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48fa1-111">Request</span></span>](#request) | <span data-ttu-id="48fa1-112">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="48fa1-112">The HTTP request.</span></span>
[<span data-ttu-id="48fa1-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="48fa1-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="48fa1-114">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="48fa1-114">The web resource request contexts.</span></span>
[<span data-ttu-id="48fa1-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48fa1-115">Response</span></span>](#response) | <span data-ttu-id="48fa1-116">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="48fa1-116">The HTTP response.</span></span>
[<span data-ttu-id="48fa1-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="48fa1-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="48fa1-118">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="48fa1-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="48fa1-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="48fa1-119">Members</span></span>

#### <span data-ttu-id="48fa1-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48fa1-120">Request</span></span> 

<span data-ttu-id="48fa1-121">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="48fa1-121">The HTTP request.</span></span>

> <span data-ttu-id="48fa1-122">[solicitud](#request) de HttpRequestMessage pública</span><span class="sxs-lookup"><span data-stu-id="48fa1-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="48fa1-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="48fa1-123">ResourceContext</span></span> 

<span data-ttu-id="48fa1-124">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="48fa1-124">The web resource request contexts.</span></span>

> <span data-ttu-id="48fa1-125">[CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) pública [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="48fa1-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="48fa1-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48fa1-126">Response</span></span> 

<span data-ttu-id="48fa1-127">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="48fa1-127">The HTTP response.</span></span>

> <span data-ttu-id="48fa1-128">[respuesta](#response) de HttpResponseMessage pública</span><span class="sxs-lookup"><span data-stu-id="48fa1-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="48fa1-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="48fa1-129">GetDeferral</span></span> 

<span data-ttu-id="48fa1-130">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="48fa1-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="48fa1-131">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="48fa1-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="48fa1-132">Puede usar el objeto CoreWebView2Deferral para completar la solicitud de red más adelante.</span><span class="sxs-lookup"><span data-stu-id="48fa1-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>


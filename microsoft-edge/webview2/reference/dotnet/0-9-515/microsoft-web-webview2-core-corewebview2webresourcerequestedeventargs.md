---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 656510998879e77c2e7797c700dacc5966299210
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884655"
---
# <span data-ttu-id="d1ea0-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs (clase)</span><span class="sxs-lookup"><span data-stu-id="d1ea0-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="d1ea0-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="d1ea0-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="d1ea0-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="d1ea0-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="d1ea0-107">Argumentos de evento para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d1ea0-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="d1ea0-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="d1ea0-108">Summary</span></span>

 <span data-ttu-id="d1ea0-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1ea0-109">Members</span></span>                        | <span data-ttu-id="d1ea0-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="d1ea0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d1ea0-111">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d1ea0-111">Request</span></span>](#request) | <span data-ttu-id="d1ea0-112">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="d1ea0-112">The HTTP request.</span></span>
[<span data-ttu-id="d1ea0-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="d1ea0-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="d1ea0-114">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="d1ea0-114">The web resource request contexts.</span></span>
[<span data-ttu-id="d1ea0-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d1ea0-115">Response</span></span>](#response) | <span data-ttu-id="d1ea0-116">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="d1ea0-116">The HTTP response.</span></span>
[<span data-ttu-id="d1ea0-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d1ea0-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="d1ea0-118">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="d1ea0-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="d1ea0-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1ea0-119">Members</span></span>

#### <span data-ttu-id="d1ea0-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d1ea0-120">Request</span></span> 

<span data-ttu-id="d1ea0-121">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="d1ea0-121">The HTTP request.</span></span>

> <span data-ttu-id="d1ea0-122">[solicitud](#request) de HttpRequestMessage pública</span><span class="sxs-lookup"><span data-stu-id="d1ea0-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="d1ea0-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="d1ea0-123">ResourceContext</span></span> 

<span data-ttu-id="d1ea0-124">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="d1ea0-124">The web resource request contexts.</span></span>

> <span data-ttu-id="d1ea0-125">[CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) pública [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="d1ea0-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="d1ea0-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d1ea0-126">Response</span></span> 

<span data-ttu-id="d1ea0-127">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="d1ea0-127">The HTTP response.</span></span>

> <span data-ttu-id="d1ea0-128">[respuesta](#response) de HttpResponseMessage pública</span><span class="sxs-lookup"><span data-stu-id="d1ea0-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="d1ea0-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d1ea0-129">GetDeferral</span></span> 

<span data-ttu-id="d1ea0-130">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="d1ea0-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="d1ea0-131">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="d1ea0-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="d1ea0-132">Puede usar el objeto CoreWebView2Deferral para completar la solicitud de red más adelante.</span><span class="sxs-lookup"><span data-stu-id="d1ea0-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>


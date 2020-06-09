---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 3d85b1116a3f75058bda59f1c374700555b42a5e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699442"
---
# <span data-ttu-id="2ce8b-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2ce8b-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

<span data-ttu-id="2ce8b-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="2ce8b-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="2ce8b-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="2ce8b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="2ce8b-107">Argumentos de evento para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2ce8b-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="2ce8b-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="2ce8b-108">Summary</span></span>

 <span data-ttu-id="2ce8b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2ce8b-109">Members</span></span>                        | <span data-ttu-id="2ce8b-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2ce8b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2ce8b-111">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2ce8b-111">Request</span></span>](#request) | <span data-ttu-id="2ce8b-112">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="2ce8b-112">The HTTP request.</span></span>
[<span data-ttu-id="2ce8b-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="2ce8b-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="2ce8b-114">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="2ce8b-114">The web resource request contexts.</span></span>
[<span data-ttu-id="2ce8b-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ce8b-115">Response</span></span>](#response) | <span data-ttu-id="2ce8b-116">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="2ce8b-116">The HTTP response.</span></span>
[<span data-ttu-id="2ce8b-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2ce8b-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="2ce8b-118">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="2ce8b-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="2ce8b-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="2ce8b-119">Members</span></span>

#### <span data-ttu-id="2ce8b-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2ce8b-120">Request</span></span> 

<span data-ttu-id="2ce8b-121">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="2ce8b-121">The HTTP request.</span></span>

> <span data-ttu-id="2ce8b-122">[solicitud](#request) de HttpRequestMessage pública</span><span class="sxs-lookup"><span data-stu-id="2ce8b-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="2ce8b-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="2ce8b-123">ResourceContext</span></span> 

<span data-ttu-id="2ce8b-124">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="2ce8b-124">The web resource request contexts.</span></span>

> <span data-ttu-id="2ce8b-125">[CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) pública [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="2ce8b-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="2ce8b-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ce8b-126">Response</span></span> 

<span data-ttu-id="2ce8b-127">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="2ce8b-127">The HTTP response.</span></span>

> <span data-ttu-id="2ce8b-128">[respuesta](#response) de HttpResponseMessage pública</span><span class="sxs-lookup"><span data-stu-id="2ce8b-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="2ce8b-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2ce8b-129">GetDeferral</span></span> 

<span data-ttu-id="2ce8b-130">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="2ce8b-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="2ce8b-131">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="2ce8b-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="2ce8b-132">Puede usar el objeto CoreWebView2Deferral para completar la solicitud de red más adelante.</span><span class="sxs-lookup"><span data-stu-id="2ce8b-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 2f9fb899746922206ff3f6cbfd129d69389fd60e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879313"
---
# <span data-ttu-id="f9ba3-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs (clase)</span><span class="sxs-lookup"><span data-stu-id="f9ba3-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="f9ba3-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="f9ba3-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="f9ba3-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="f9ba3-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="f9ba3-107">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f9ba3-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f9ba3-108">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="f9ba3-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f9ba3-109">Argumentos de evento para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="f9ba3-109">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="f9ba3-110">Resumen</span><span class="sxs-lookup"><span data-stu-id="f9ba3-110">Summary</span></span>

 <span data-ttu-id="f9ba3-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f9ba3-111">Members</span></span>                        | <span data-ttu-id="f9ba3-112">Descripciones</span><span class="sxs-lookup"><span data-stu-id="f9ba3-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f9ba3-113">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f9ba3-113">Request</span></span>](#request) | <span data-ttu-id="f9ba3-114">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="f9ba3-114">The HTTP request.</span></span>
[<span data-ttu-id="f9ba3-115">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="f9ba3-115">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="f9ba3-116">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="f9ba3-116">The web resource request contexts.</span></span>
[<span data-ttu-id="f9ba3-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9ba3-117">Response</span></span>](#response) | <span data-ttu-id="f9ba3-118">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f9ba3-118">The HTTP response.</span></span>
[<span data-ttu-id="f9ba3-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f9ba3-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="f9ba3-120">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="f9ba3-120">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="f9ba3-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="f9ba3-121">Members</span></span>

#### <span data-ttu-id="f9ba3-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f9ba3-122">Request</span></span> 

<span data-ttu-id="f9ba3-123">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="f9ba3-123">The HTTP request.</span></span>

> <span data-ttu-id="f9ba3-124">[solicitud](#request) de HttpRequestMessage pública</span><span class="sxs-lookup"><span data-stu-id="f9ba3-124">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="f9ba3-125">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="f9ba3-125">ResourceContext</span></span> 

<span data-ttu-id="f9ba3-126">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="f9ba3-126">The web resource request contexts.</span></span>

> <span data-ttu-id="f9ba3-127">[CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) pública [ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="f9ba3-127">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="f9ba3-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9ba3-128">Response</span></span> 

<span data-ttu-id="f9ba3-129">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f9ba3-129">The HTTP response.</span></span>

> <span data-ttu-id="f9ba3-130">[respuesta](#response) de HttpResponseMessage pública</span><span class="sxs-lookup"><span data-stu-id="f9ba3-130">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="f9ba3-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f9ba3-131">GetDeferral</span></span> 

<span data-ttu-id="f9ba3-132">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="f9ba3-132">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="f9ba3-133">Public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="f9ba3-133">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="f9ba3-134">Puede usar el objeto CoreWebView2Deferral para completar la solicitud de red más adelante.</span><span class="sxs-lookup"><span data-stu-id="f9ba3-134">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>


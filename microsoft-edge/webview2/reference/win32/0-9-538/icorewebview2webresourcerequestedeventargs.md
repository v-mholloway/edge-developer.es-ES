---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 3613ed9b2ef562e8760de1a88322ef028ddf4ca9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879222"
---
# <span data-ttu-id="7f721-104">interfaz ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7f721-104">interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="7f721-105">Argumentos de evento para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="7f721-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="7f721-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="7f721-106">Summary</span></span>

 <span data-ttu-id="7f721-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7f721-107">Members</span></span>                        | <span data-ttu-id="7f721-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7f721-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7f721-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="7f721-109">get_Request</span></span>](#get_request) | <span data-ttu-id="7f721-110">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="7f721-110">The HTTP request.</span></span>
[<span data-ttu-id="7f721-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="7f721-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="7f721-112">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="7f721-112">The web resource request contexts.</span></span>
[<span data-ttu-id="7f721-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="7f721-113">get_Response</span></span>](#get_response) | <span data-ttu-id="7f721-114">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="7f721-114">The HTTP response.</span></span>
[<span data-ttu-id="7f721-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="7f721-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="7f721-116">Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="7f721-116">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="7f721-117">put_Response</span><span class="sxs-lookup"><span data-stu-id="7f721-117">put_Response</span></span>](#put_response) | <span data-ttu-id="7f721-118">Establezca la propiedad Response.</span><span class="sxs-lookup"><span data-stu-id="7f721-118">Set the Response property.</span></span>

## <span data-ttu-id="7f721-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="7f721-119">Members</span></span>

#### <span data-ttu-id="7f721-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="7f721-120">get_Request</span></span> 

<span data-ttu-id="7f721-121">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="7f721-121">The HTTP request.</span></span>

> <span data-ttu-id="7f721-122">[get_Request](#get_request)de HRESULT público (solicitud[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="7f721-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="7f721-123">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="7f721-123">get_ResourceContext</span></span> 

<span data-ttu-id="7f721-124">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="7f721-124">The web resource request contexts.</span></span>

> <span data-ttu-id="7f721-125">[get_ResourceContext](#get_resourcecontext)de HRESULT público (COREWEBVIEW2_WEB_RESOURCE_CONTEXT \*)</span><span class="sxs-lookup"><span data-stu-id="7f721-125">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="7f721-126">get_Response</span><span class="sxs-lookup"><span data-stu-id="7f721-126">get_Response</span></span> 

<span data-ttu-id="7f721-127">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="7f721-127">The HTTP response.</span></span>

> <span data-ttu-id="7f721-128">[get_Response](#get_response)de HRESULT público (respuesta de[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="7f721-128">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

#### <span data-ttu-id="7f721-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="7f721-129">GetDeferral</span></span> 

<span data-ttu-id="7f721-130">Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="7f721-130">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="7f721-131">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="7f721-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="7f721-132">Puede usar el objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para completar la solicitud de red más adelante.</span><span class="sxs-lookup"><span data-stu-id="7f721-132">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="7f721-133">put_Response</span><span class="sxs-lookup"><span data-stu-id="7f721-133">put_Response</span></span> 

<span data-ttu-id="7f721-134">Establezca la propiedad Response.</span><span class="sxs-lookup"><span data-stu-id="7f721-134">Set the Response property.</span></span>

> <span data-ttu-id="7f721-135">[put_Response](#put_response)de HRESULT público (respuesta de[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="7f721-135">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>


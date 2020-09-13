---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 14b88f83e9635c94e205df05f6764e059f0def78
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012611"
---
# <span data-ttu-id="34177-104">interfaz ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="34177-104">interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="34177-105">Argumentos de evento para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="34177-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="34177-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="34177-106">Summary</span></span>

 <span data-ttu-id="34177-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="34177-107">Members</span></span>                        | <span data-ttu-id="34177-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="34177-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="34177-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="34177-109">get_Request</span></span>](#get_request) | <span data-ttu-id="34177-110">La solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="34177-110">The Web resource request.</span></span>
[<span data-ttu-id="34177-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="34177-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="34177-112">El contexto de la solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="34177-112">The web resource request context.</span></span>
[<span data-ttu-id="34177-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="34177-113">get_Response</span></span>](#get_response) | <span data-ttu-id="34177-114">Un marcador de posición para el objeto de respuesta de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="34177-114">A placeholder for the web resource response object.</span></span>
[<span data-ttu-id="34177-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="34177-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="34177-116">Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="34177-116">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="34177-117">put_Response</span><span class="sxs-lookup"><span data-stu-id="34177-117">put_Response</span></span>](#put_response) | <span data-ttu-id="34177-118">Establezca la propiedad Response.</span><span class="sxs-lookup"><span data-stu-id="34177-118">Set the Response property.</span></span>

## <span data-ttu-id="34177-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="34177-119">Members</span></span>

#### <span data-ttu-id="34177-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="34177-120">get_Request</span></span> 

<span data-ttu-id="34177-121">La solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="34177-121">The Web resource request.</span></span>

> <span data-ttu-id="34177-122">[get_Request](#get_request)de HRESULT público (solicitud[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="34177-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

<span data-ttu-id="34177-123">Es posible que en el objeto de solicitud falten algunos encabezados que la pila de red agrega más adelante.</span><span class="sxs-lookup"><span data-stu-id="34177-123">The request object may be missing some headers that are added by network stack later on.</span></span>

#### <span data-ttu-id="34177-124">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="34177-124">get_ResourceContext</span></span> 

<span data-ttu-id="34177-125">El contexto de la solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="34177-125">The web resource request context.</span></span>

> <span data-ttu-id="34177-126">[get_ResourceContext](#get_resourcecontext)de HRESULT público (COREWEBVIEW2_WEB_RESOURCE_CONTEXT \*)</span><span class="sxs-lookup"><span data-stu-id="34177-126">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="34177-127">get_Response</span><span class="sxs-lookup"><span data-stu-id="34177-127">get_Response</span></span> 

<span data-ttu-id="34177-128">Un marcador de posición para el objeto de respuesta de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="34177-128">A placeholder for the web resource response object.</span></span>

> <span data-ttu-id="34177-129">[get_Response](#get_response)de HRESULT público (respuesta de[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="34177-129">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

<span data-ttu-id="34177-130">Si se establece este objeto, la solicitud de recursos Web se completará con esta respuesta.</span><span class="sxs-lookup"><span data-stu-id="34177-130">If this object is set, the web resource request will be completed with this response.</span></span>

#### <span data-ttu-id="34177-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="34177-131">GetDeferral</span></span> 

<span data-ttu-id="34177-132">Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="34177-132">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="34177-133">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="34177-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="34177-134">Puedes usar el objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para completar la solicitud más adelante.</span><span class="sxs-lookup"><span data-stu-id="34177-134">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the request at a later time.</span></span>

#### <span data-ttu-id="34177-135">put_Response</span><span class="sxs-lookup"><span data-stu-id="34177-135">put_Response</span></span> 

<span data-ttu-id="34177-136">Establezca la propiedad Response.</span><span class="sxs-lookup"><span data-stu-id="34177-136">Set the Response property.</span></span>

> <span data-ttu-id="34177-137">[put_Response](#put_response)de HRESULT público (respuesta de[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="34177-137">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>

<span data-ttu-id="34177-138">Se puede crear un objeto de respuesta de recursos Web vacío con CreateWebResourceResponse y, a continuación, se ha modificado para construir la respuesta.</span><span class="sxs-lookup"><span data-stu-id="34177-138">An empty Web resource response object can be created with CreateWebResourceResponse and then modified to construct the response.</span></span>

---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 00aaddcc732076e4f7aa808b04132641fe7fe969
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886447"
---
# <span data-ttu-id="947f8-104">0.9.430: ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="947f8-104">0.9.430 - interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="947f8-105">Argumentos de evento para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="947f8-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="947f8-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="947f8-106">Summary</span></span>

 <span data-ttu-id="947f8-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="947f8-107">Members</span></span>                        | <span data-ttu-id="947f8-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="947f8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="947f8-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="947f8-109">get_Request</span></span>](#get_request) | <span data-ttu-id="947f8-110">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="947f8-110">The HTTP request.</span></span>
[<span data-ttu-id="947f8-111">get_Response</span><span class="sxs-lookup"><span data-stu-id="947f8-111">get_Response</span></span>](#get_response) | <span data-ttu-id="947f8-112">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="947f8-112">The HTTP response.</span></span>
[<span data-ttu-id="947f8-113">put_Response</span><span class="sxs-lookup"><span data-stu-id="947f8-113">put_Response</span></span>](#put_response) | <span data-ttu-id="947f8-114">Establezca la propiedad Response.</span><span class="sxs-lookup"><span data-stu-id="947f8-114">Set the Response property.</span></span>
[<span data-ttu-id="947f8-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="947f8-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="947f8-116">Obtén un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="947f8-116">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="947f8-117">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="947f8-117">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="947f8-118">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="947f8-118">The web resource request contexts.</span></span>

## <span data-ttu-id="947f8-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="947f8-119">Members</span></span>

#### <span data-ttu-id="947f8-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="947f8-120">get_Request</span></span> 

<span data-ttu-id="947f8-121">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="947f8-121">The HTTP request.</span></span>

> <span data-ttu-id="947f8-122">[get_Request](#get_request)de HRESULT público (solicitud[ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="947f8-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="947f8-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="947f8-123">get_Response</span></span> 

<span data-ttu-id="947f8-124">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="947f8-124">The HTTP response.</span></span>

> <span data-ttu-id="947f8-125">[get_Response](#get_response)de HRESULT público (respuesta de[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="947f8-125">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="947f8-126">put_Response</span><span class="sxs-lookup"><span data-stu-id="947f8-126">put_Response</span></span> 

<span data-ttu-id="947f8-127">Establezca la propiedad Response.</span><span class="sxs-lookup"><span data-stu-id="947f8-127">Set the Response property.</span></span>

> <span data-ttu-id="947f8-128">[put_Response](#put_response)de HRESULT público (respuesta de[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="947f8-128">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="947f8-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="947f8-129">GetDeferral</span></span> 

<span data-ttu-id="947f8-130">Obtén un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="947f8-130">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="947f8-131">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="947f8-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="947f8-132">Puede usar el objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) para completar la solicitud de red más adelante.</span><span class="sxs-lookup"><span data-stu-id="947f8-132">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="947f8-133">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="947f8-133">get_ResourceContext</span></span> 

<span data-ttu-id="947f8-134">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="947f8-134">The web resource request contexts.</span></span>

> <span data-ttu-id="947f8-135">[get_ResourceContext](#get_resourcecontext)de HRESULT público (CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \*)</span><span class="sxs-lookup"><span data-stu-id="947f8-135">public HRESULT [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>


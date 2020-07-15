---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 70a7d997dfd89b6d9bb8eb8af9a87ff0a130b69f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880307"
---
# <span data-ttu-id="8e23b-104">0.9.515: ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8e23b-104">0.9.515 - interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="8e23b-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="8e23b-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="8e23b-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="8e23b-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="8e23b-107">Argumentos de evento para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="8e23b-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="8e23b-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="8e23b-108">Summary</span></span>

 <span data-ttu-id="8e23b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8e23b-109">Members</span></span>                        | <span data-ttu-id="8e23b-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="8e23b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8e23b-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="8e23b-111">get_Request</span></span>](#get_request) | <span data-ttu-id="8e23b-112">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="8e23b-112">The HTTP request.</span></span>
[<span data-ttu-id="8e23b-113">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="8e23b-113">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="8e23b-114">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="8e23b-114">The web resource request contexts.</span></span>
[<span data-ttu-id="8e23b-115">get_Response</span><span class="sxs-lookup"><span data-stu-id="8e23b-115">get_Response</span></span>](#get_response) | <span data-ttu-id="8e23b-116">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="8e23b-116">The HTTP response.</span></span>
[<span data-ttu-id="8e23b-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="8e23b-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="8e23b-118">Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="8e23b-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="8e23b-119">put_Response</span><span class="sxs-lookup"><span data-stu-id="8e23b-119">put_Response</span></span>](#put_response) | <span data-ttu-id="8e23b-120">Establezca la propiedad Response.</span><span class="sxs-lookup"><span data-stu-id="8e23b-120">Set the Response property.</span></span>

## <span data-ttu-id="8e23b-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="8e23b-121">Members</span></span>

#### <span data-ttu-id="8e23b-122">get_Request</span><span class="sxs-lookup"><span data-stu-id="8e23b-122">get_Request</span></span> 

<span data-ttu-id="8e23b-123">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="8e23b-123">The HTTP request.</span></span>

> <span data-ttu-id="8e23b-124">[get_Request](#get_request)de HRESULT público (solicitud[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="8e23b-124">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="8e23b-125">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="8e23b-125">get_ResourceContext</span></span> 

<span data-ttu-id="8e23b-126">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="8e23b-126">The web resource request contexts.</span></span>

> <span data-ttu-id="8e23b-127">[get_ResourceContext](#get_resourcecontext)de HRESULT público (COREWEBVIEW2_WEB_RESOURCE_CONTEXT \*)</span><span class="sxs-lookup"><span data-stu-id="8e23b-127">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="8e23b-128">get_Response</span><span class="sxs-lookup"><span data-stu-id="8e23b-128">get_Response</span></span> 

<span data-ttu-id="8e23b-129">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="8e23b-129">The HTTP response.</span></span>

> <span data-ttu-id="8e23b-130">[get_Response](#get_response)de HRESULT público (respuesta de[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="8e23b-130">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

#### <span data-ttu-id="8e23b-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="8e23b-131">GetDeferral</span></span> 

<span data-ttu-id="8e23b-132">Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="8e23b-132">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="8e23b-133">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="8e23b-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="8e23b-134">Puede usar el objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para completar la solicitud de red más adelante.</span><span class="sxs-lookup"><span data-stu-id="8e23b-134">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="8e23b-135">put_Response</span><span class="sxs-lookup"><span data-stu-id="8e23b-135">put_Response</span></span> 

<span data-ttu-id="8e23b-136">Establezca la propiedad Response.</span><span class="sxs-lookup"><span data-stu-id="8e23b-136">Set the Response property.</span></span>

> <span data-ttu-id="8e23b-137">[put_Response](#put_response)de HRESULT público (respuesta de[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="8e23b-137">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 59557ca86e8b044fb937fe93b3060c0879abb6f1
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655403"
---
# <span data-ttu-id="d073d-104">interfaz ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d073d-104">interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="d073d-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="d073d-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="d073d-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="d073d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="d073d-107">Argumentos de evento para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d073d-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="d073d-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="d073d-108">Summary</span></span>

 <span data-ttu-id="d073d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="d073d-109">Members</span></span>                        | <span data-ttu-id="d073d-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="d073d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d073d-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="d073d-111">get_Request</span></span>](#get_request) | <span data-ttu-id="d073d-112">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="d073d-112">The HTTP request.</span></span>
[<span data-ttu-id="d073d-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="d073d-113">get_Response</span></span>](#get_response) | <span data-ttu-id="d073d-114">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="d073d-114">The HTTP response.</span></span>
[<span data-ttu-id="d073d-115">put_Response</span><span class="sxs-lookup"><span data-stu-id="d073d-115">put_Response</span></span>](#put_response) | <span data-ttu-id="d073d-116">Establezca la propiedad Response.</span><span class="sxs-lookup"><span data-stu-id="d073d-116">Set the Response property.</span></span>
[<span data-ttu-id="d073d-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d073d-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="d073d-118">Obtén un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="d073d-118">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="d073d-119">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="d073d-119">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="d073d-120">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="d073d-120">The web resource request contexts.</span></span>

## <span data-ttu-id="d073d-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="d073d-121">Members</span></span>

#### <span data-ttu-id="d073d-122">get_Request</span><span class="sxs-lookup"><span data-stu-id="d073d-122">get_Request</span></span> 

<span data-ttu-id="d073d-123">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="d073d-123">The HTTP request.</span></span>

> <span data-ttu-id="d073d-124">[get_Request](#get_request)de HRESULT público (solicitud[ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="d073d-124">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="d073d-125">get_Response</span><span class="sxs-lookup"><span data-stu-id="d073d-125">get_Response</span></span> 

<span data-ttu-id="d073d-126">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="d073d-126">The HTTP response.</span></span>

> <span data-ttu-id="d073d-127">[get_Response](#get_response)de HRESULT público (respuesta de[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="d073d-127">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="d073d-128">put_Response</span><span class="sxs-lookup"><span data-stu-id="d073d-128">put_Response</span></span> 

<span data-ttu-id="d073d-129">Establezca la propiedad Response.</span><span class="sxs-lookup"><span data-stu-id="d073d-129">Set the Response property.</span></span>

> <span data-ttu-id="d073d-130">[put_Response](#put_response)de HRESULT público (respuesta de[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="d073d-130">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="d073d-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d073d-131">GetDeferral</span></span> 

<span data-ttu-id="d073d-132">Obtén un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="d073d-132">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="d073d-133">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="d073d-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="d073d-134">Puede usar el objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) para completar la solicitud de red más adelante.</span><span class="sxs-lookup"><span data-stu-id="d073d-134">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="d073d-135">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="d073d-135">get_ResourceContext</span></span> 

<span data-ttu-id="d073d-136">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="d073d-136">The web resource request contexts.</span></span>

> <span data-ttu-id="d073d-137">[get_ResourceContext](#get_resourcecontext)de HRESULT público (CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \*)</span><span class="sxs-lookup"><span data-stu-id="d073d-137">public HRESULT [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 899a6f50db1d77f3f24524c5ccec139dcbdbcaf9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655139"
---
# <span data-ttu-id="0209d-104">interfaz IWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="0209d-104">interface IWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="0209d-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="0209d-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="0209d-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="0209d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="0209d-107">Argumentos de evento para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="0209d-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="0209d-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="0209d-108">Summary</span></span>

 <span data-ttu-id="0209d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0209d-109">Members</span></span>                        | <span data-ttu-id="0209d-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="0209d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0209d-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="0209d-111">get_Request</span></span>](#get_request) | <span data-ttu-id="0209d-112">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="0209d-112">The HTTP request.</span></span>
[<span data-ttu-id="0209d-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="0209d-113">get_Response</span></span>](#get_response) | <span data-ttu-id="0209d-114">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="0209d-114">The HTTP response.</span></span>
[<span data-ttu-id="0209d-115">put_Response</span><span class="sxs-lookup"><span data-stu-id="0209d-115">put_Response</span></span>](#put_response) | <span data-ttu-id="0209d-116">Establezca la propiedad Response.</span><span class="sxs-lookup"><span data-stu-id="0209d-116">Set the Response property.</span></span>
[<span data-ttu-id="0209d-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="0209d-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="0209d-118">Obtén un objeto [IWebView2Deferral](IWebView2Deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="0209d-118">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

## <span data-ttu-id="0209d-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="0209d-119">Members</span></span>

#### <span data-ttu-id="0209d-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="0209d-120">get_Request</span></span> 

<span data-ttu-id="0209d-121">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="0209d-121">The HTTP request.</span></span>

> <span data-ttu-id="0209d-122">[get_Request](#get_request)de HRESULT público (solicitud[IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="0209d-122">public HRESULT [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="0209d-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="0209d-123">get_Response</span></span> 

<span data-ttu-id="0209d-124">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="0209d-124">The HTTP response.</span></span>

> <span data-ttu-id="0209d-125">[get_Response](#get_response)de HRESULT público (respuesta de[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="0209d-125">public HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="0209d-126">put_Response</span><span class="sxs-lookup"><span data-stu-id="0209d-126">put_Response</span></span> 

<span data-ttu-id="0209d-127">Establezca la propiedad Response.</span><span class="sxs-lookup"><span data-stu-id="0209d-127">Set the Response property.</span></span>

> <span data-ttu-id="0209d-128">[put_Response](#put_response)de HRESULT público (respuesta de[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="0209d-128">public HRESULT [put_Response](#put_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="0209d-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="0209d-129">GetDeferral</span></span> 

<span data-ttu-id="0209d-130">Obtén un objeto [IWebView2Deferral](IWebView2Deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="0209d-130">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="0209d-131">[GETDEFERRAL](#getdeferral)HRESULT ([IWebView2Deferral](IWebView2Deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="0209d-131">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="0209d-132">Puede usar el objeto [IWebView2Deferral](IWebView2Deferral.md) para completar la solicitud de red más adelante.</span><span class="sxs-lookup"><span data-stu-id="0209d-132">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the network request at a later time.</span></span>


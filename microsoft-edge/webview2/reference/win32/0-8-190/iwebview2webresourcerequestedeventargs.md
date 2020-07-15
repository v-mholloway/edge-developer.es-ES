---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 40474d6b1169467022e5bb47e82eba3883edc2aa
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878102"
---
# <span data-ttu-id="466a3-104">0.8.355: IWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="466a3-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="466a3-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="466a3-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="466a3-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="466a3-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="466a3-107">Argumentos de evento para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="466a3-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="466a3-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="466a3-108">Summary</span></span>

 <span data-ttu-id="466a3-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="466a3-109">Members</span></span>                        | <span data-ttu-id="466a3-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="466a3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="466a3-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="466a3-111">get_Request</span></span>](#get_request) | <span data-ttu-id="466a3-112">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="466a3-112">The HTTP request.</span></span>
[<span data-ttu-id="466a3-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="466a3-113">get_Response</span></span>](#get_response) | <span data-ttu-id="466a3-114">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="466a3-114">The HTTP response.</span></span>
[<span data-ttu-id="466a3-115">put_Response</span><span class="sxs-lookup"><span data-stu-id="466a3-115">put_Response</span></span>](#put_response) | <span data-ttu-id="466a3-116">Establezca la propiedad Response.</span><span class="sxs-lookup"><span data-stu-id="466a3-116">Set the Response property.</span></span>
[<span data-ttu-id="466a3-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="466a3-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="466a3-118">Obtén un objeto [IWebView2Deferral](IWebView2Deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="466a3-118">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

## <span data-ttu-id="466a3-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="466a3-119">Members</span></span>

#### <span data-ttu-id="466a3-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="466a3-120">get_Request</span></span> 

<span data-ttu-id="466a3-121">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="466a3-121">The HTTP request.</span></span>

> <span data-ttu-id="466a3-122">[get_Request](#get_request)de HRESULT público (solicitud[IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="466a3-122">public HRESULT [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="466a3-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="466a3-123">get_Response</span></span> 

<span data-ttu-id="466a3-124">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="466a3-124">The HTTP response.</span></span>

> <span data-ttu-id="466a3-125">[get_Response](#get_response)de HRESULT público (respuesta de[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="466a3-125">public HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="466a3-126">put_Response</span><span class="sxs-lookup"><span data-stu-id="466a3-126">put_Response</span></span> 

<span data-ttu-id="466a3-127">Establezca la propiedad Response.</span><span class="sxs-lookup"><span data-stu-id="466a3-127">Set the Response property.</span></span>

> <span data-ttu-id="466a3-128">[put_Response](#put_response)de HRESULT público (respuesta de[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="466a3-128">public HRESULT [put_Response](#put_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="466a3-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="466a3-129">GetDeferral</span></span> 

<span data-ttu-id="466a3-130">Obtén un objeto [IWebView2Deferral](IWebView2Deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="466a3-130">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="466a3-131">[GETDEFERRAL](#getdeferral)HRESULT ([IWebView2Deferral](IWebView2Deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="466a3-131">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="466a3-132">Puede usar el objeto [IWebView2Deferral](IWebView2Deferral.md) para completar la solicitud de red más adelante.</span><span class="sxs-lookup"><span data-stu-id="466a3-132">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the network request at a later time.</span></span>


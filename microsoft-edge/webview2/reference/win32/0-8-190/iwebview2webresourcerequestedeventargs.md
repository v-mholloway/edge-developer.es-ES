---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: aa5206be13790fd7a783f2afb4471de90fc8f2ae
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885721"
---
# <span data-ttu-id="3fe20-104">0.8.355: IWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="3fe20-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="3fe20-105">Argumentos de evento para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="3fe20-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="3fe20-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="3fe20-106">Summary</span></span>

 <span data-ttu-id="3fe20-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="3fe20-107">Members</span></span>                        | <span data-ttu-id="3fe20-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="3fe20-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3fe20-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="3fe20-109">get_Request</span></span>](#get_request) | <span data-ttu-id="3fe20-110">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="3fe20-110">The HTTP request.</span></span>
[<span data-ttu-id="3fe20-111">get_Response</span><span class="sxs-lookup"><span data-stu-id="3fe20-111">get_Response</span></span>](#get_response) | <span data-ttu-id="3fe20-112">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="3fe20-112">The HTTP response.</span></span>
[<span data-ttu-id="3fe20-113">put_Response</span><span class="sxs-lookup"><span data-stu-id="3fe20-113">put_Response</span></span>](#put_response) | <span data-ttu-id="3fe20-114">Establezca la propiedad Response.</span><span class="sxs-lookup"><span data-stu-id="3fe20-114">Set the Response property.</span></span>
[<span data-ttu-id="3fe20-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="3fe20-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="3fe20-116">Obtén un objeto [IWebView2Deferral](IWebView2Deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="3fe20-116">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

## <span data-ttu-id="3fe20-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="3fe20-117">Members</span></span>

#### <span data-ttu-id="3fe20-118">get_Request</span><span class="sxs-lookup"><span data-stu-id="3fe20-118">get_Request</span></span> 

<span data-ttu-id="3fe20-119">La solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="3fe20-119">The HTTP request.</span></span>

> <span data-ttu-id="3fe20-120">[get_Request](#get_request)de HRESULT público (solicitud[IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="3fe20-120">public HRESULT [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="3fe20-121">get_Response</span><span class="sxs-lookup"><span data-stu-id="3fe20-121">get_Response</span></span> 

<span data-ttu-id="3fe20-122">La respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="3fe20-122">The HTTP response.</span></span>

> <span data-ttu-id="3fe20-123">[get_Response](#get_response)de HRESULT público (respuesta de[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="3fe20-123">public HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="3fe20-124">put_Response</span><span class="sxs-lookup"><span data-stu-id="3fe20-124">put_Response</span></span> 

<span data-ttu-id="3fe20-125">Establezca la propiedad Response.</span><span class="sxs-lookup"><span data-stu-id="3fe20-125">Set the Response property.</span></span>

> <span data-ttu-id="3fe20-126">[put_Response](#put_response)de HRESULT público (respuesta de[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="3fe20-126">public HRESULT [put_Response](#put_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="3fe20-127">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="3fe20-127">GetDeferral</span></span> 

<span data-ttu-id="3fe20-128">Obtén un objeto [IWebView2Deferral](IWebView2Deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="3fe20-128">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="3fe20-129">[GETDEFERRAL](#getdeferral)HRESULT ([IWebView2Deferral](IWebView2Deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="3fe20-129">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="3fe20-130">Puede usar el objeto [IWebView2Deferral](IWebView2Deferral.md) para completar la solicitud de red más adelante.</span><span class="sxs-lookup"><span data-stu-id="3fe20-130">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the network request at a later time.</span></span>


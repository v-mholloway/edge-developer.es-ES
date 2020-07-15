---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 44f7477eaa81198ef64d332faa0c3a22225d5ea4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880974"
---
# <span data-ttu-id="4f578-104">0.9.430: ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="4f578-104">0.9.430 - interface ICoreWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="4f578-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="4f578-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="4f578-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="4f578-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="4f578-107">Encabezados de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="4f578-107">HTTP response headers.</span></span>

## <span data-ttu-id="4f578-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="4f578-108">Summary</span></span>

 <span data-ttu-id="4f578-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="4f578-109">Members</span></span>                        | <span data-ttu-id="4f578-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="4f578-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4f578-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="4f578-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="4f578-112">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="4f578-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="4f578-113">Contains</span><span class="sxs-lookup"><span data-stu-id="4f578-113">Contains</span></span>](#contains) | <span data-ttu-id="4f578-114">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="4f578-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="4f578-115">GetHeader</span><span class="sxs-lookup"><span data-stu-id="4f578-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="4f578-116">Obtiene el primer valor de encabezado de la colección que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="4f578-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="4f578-117">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="4f578-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="4f578-118">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="4f578-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="4f578-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="4f578-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="4f578-120">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="4f578-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="4f578-121">Se usa para construir un WebResourceResponse para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="4f578-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="4f578-122">Miembros</span><span class="sxs-lookup"><span data-stu-id="4f578-122">Members</span></span>

#### <span data-ttu-id="4f578-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="4f578-123">AppendHeader</span></span> 

<span data-ttu-id="4f578-124">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="4f578-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="4f578-125">[APPENDHEADER](#appendheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="4f578-125">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="4f578-126">Contains</span><span class="sxs-lookup"><span data-stu-id="4f578-126">Contains</span></span> 

<span data-ttu-id="4f578-127">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="4f578-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="4f578-128">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="4f578-128">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="4f578-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="4f578-129">GetHeader</span></span> 

<span data-ttu-id="4f578-130">Obtiene el primer valor de encabezado de la colección que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="4f578-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="4f578-131">HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="4f578-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="4f578-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="4f578-132">GetHeaders</span></span> 

<span data-ttu-id="4f578-133">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="4f578-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="4f578-134">[GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* iterator)</span><span class="sxs-lookup"><span data-stu-id="4f578-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="4f578-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="4f578-135">GetIterator</span></span> 

<span data-ttu-id="4f578-136">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="4f578-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="4f578-137">[GETITERATOR](#getiterator)HRESULT ([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="4f578-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


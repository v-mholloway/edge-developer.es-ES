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
ms.openlocfilehash: b23b724977b9d164c48dc99d0da2e64d61539549
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655429"
---
# <span data-ttu-id="e85c0-104">interfaz ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="e85c0-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="e85c0-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="e85c0-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="e85c0-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="e85c0-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="e85c0-107">Encabezados de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="e85c0-107">HTTP response headers.</span></span>

## <span data-ttu-id="e85c0-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="e85c0-108">Summary</span></span>

 <span data-ttu-id="e85c0-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="e85c0-109">Members</span></span>                        | <span data-ttu-id="e85c0-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e85c0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e85c0-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="e85c0-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="e85c0-112">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="e85c0-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="e85c0-113">Contains</span><span class="sxs-lookup"><span data-stu-id="e85c0-113">Contains</span></span>](#contains) | <span data-ttu-id="e85c0-114">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="e85c0-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="e85c0-115">GetHeader</span><span class="sxs-lookup"><span data-stu-id="e85c0-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="e85c0-116">Obtiene el primer valor de encabezado de la colección que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="e85c0-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="e85c0-117">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="e85c0-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="e85c0-118">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="e85c0-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="e85c0-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="e85c0-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="e85c0-120">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="e85c0-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="e85c0-121">Se usa para construir un WebResourceResponse para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="e85c0-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="e85c0-122">Miembros</span><span class="sxs-lookup"><span data-stu-id="e85c0-122">Members</span></span>

#### <span data-ttu-id="e85c0-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="e85c0-123">AppendHeader</span></span> 

<span data-ttu-id="e85c0-124">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="e85c0-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="e85c0-125">[APPENDHEADER](#appendheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="e85c0-125">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="e85c0-126">Contains</span><span class="sxs-lookup"><span data-stu-id="e85c0-126">Contains</span></span> 

<span data-ttu-id="e85c0-127">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="e85c0-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="e85c0-128">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="e85c0-128">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="e85c0-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="e85c0-129">GetHeader</span></span> 

<span data-ttu-id="e85c0-130">Obtiene el primer valor de encabezado de la colección que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="e85c0-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="e85c0-131">HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="e85c0-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="e85c0-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="e85c0-132">GetHeaders</span></span> 

<span data-ttu-id="e85c0-133">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="e85c0-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="e85c0-134">[GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* iterator)</span><span class="sxs-lookup"><span data-stu-id="e85c0-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="e85c0-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="e85c0-135">GetIterator</span></span> 

<span data-ttu-id="e85c0-136">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="e85c0-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="e85c0-137">[GETITERATOR](#getiterator)HRESULT ([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="e85c0-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


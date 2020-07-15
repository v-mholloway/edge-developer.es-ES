---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2HttpResponseHeaders
ms.openlocfilehash: 359e79b2ecfd92ee0b7dc608a5ae5748ff6f20ce
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878746"
---
# <span data-ttu-id="943f3-104">interfaz ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="943f3-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="943f3-105">Encabezados de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="943f3-105">HTTP response headers.</span></span>

## <span data-ttu-id="943f3-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="943f3-106">Summary</span></span>

 <span data-ttu-id="943f3-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="943f3-107">Members</span></span>                        | <span data-ttu-id="943f3-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="943f3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="943f3-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="943f3-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="943f3-110">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="943f3-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="943f3-111">Contains</span><span class="sxs-lookup"><span data-stu-id="943f3-111">Contains</span></span>](#contains) | <span data-ttu-id="943f3-112">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="943f3-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="943f3-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="943f3-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="943f3-114">Obtiene el primer valor de encabezado de la colección que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="943f3-114">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="943f3-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="943f3-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="943f3-116">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="943f3-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="943f3-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="943f3-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="943f3-118">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="943f3-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="943f3-119">Se usa para construir un WebResourceResponse para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="943f3-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="943f3-120">Miembros</span><span class="sxs-lookup"><span data-stu-id="943f3-120">Members</span></span>

#### <span data-ttu-id="943f3-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="943f3-121">AppendHeader</span></span> 

<span data-ttu-id="943f3-122">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="943f3-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="943f3-123">[APPENDHEADER](#appendheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="943f3-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name, LPCWSTR value)</span></span>

#### <span data-ttu-id="943f3-124">Contains</span><span class="sxs-lookup"><span data-stu-id="943f3-124">Contains</span></span> 

<span data-ttu-id="943f3-125">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="943f3-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="943f3-126">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="943f3-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="943f3-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="943f3-127">GetHeader</span></span> 

<span data-ttu-id="943f3-128">Obtiene el primer valor de encabezado de la colección que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="943f3-128">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="943f3-129">HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="943f3-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="943f3-130">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="943f3-130">GetHeaders</span></span> 

<span data-ttu-id="943f3-131">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="943f3-131">Gets the header values matching the name.</span></span>

> <span data-ttu-id="943f3-132">[GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterator)</span><span class="sxs-lookup"><span data-stu-id="943f3-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="943f3-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="943f3-133">GetIterator</span></span> 

<span data-ttu-id="943f3-134">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="943f3-134">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="943f3-135">[GETITERATOR](#getiterator)HRESULT ([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="943f3-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>


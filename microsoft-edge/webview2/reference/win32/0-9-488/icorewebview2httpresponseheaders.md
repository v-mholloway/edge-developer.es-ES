---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 63044cae80aebfb1e759070ec797673b0c9378d2
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697255"
---
# <span data-ttu-id="51b74-104">interfaz ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="51b74-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="51b74-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="51b74-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="51b74-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="51b74-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="51b74-107">Encabezados de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="51b74-107">HTTP response headers.</span></span>

## <span data-ttu-id="51b74-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="51b74-108">Summary</span></span>

 <span data-ttu-id="51b74-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="51b74-109">Members</span></span>                        | <span data-ttu-id="51b74-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="51b74-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="51b74-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="51b74-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="51b74-112">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="51b74-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="51b74-113">Contains</span><span class="sxs-lookup"><span data-stu-id="51b74-113">Contains</span></span>](#contains) | <span data-ttu-id="51b74-114">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="51b74-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="51b74-115">GetHeader</span><span class="sxs-lookup"><span data-stu-id="51b74-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="51b74-116">Obtiene el primer valor de encabezado de la colección que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="51b74-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="51b74-117">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="51b74-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="51b74-118">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="51b74-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="51b74-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="51b74-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="51b74-120">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="51b74-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="51b74-121">Se usa para construir un WebResourceResponse para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="51b74-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="51b74-122">Miembros</span><span class="sxs-lookup"><span data-stu-id="51b74-122">Members</span></span>

#### <span data-ttu-id="51b74-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="51b74-123">AppendHeader</span></span> 

<span data-ttu-id="51b74-124">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="51b74-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="51b74-125">[APPENDHEADER](#appendheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="51b74-125">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name, LPCWSTR value)</span></span>

#### <span data-ttu-id="51b74-126">Contains</span><span class="sxs-lookup"><span data-stu-id="51b74-126">Contains</span></span> 

<span data-ttu-id="51b74-127">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="51b74-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="51b74-128">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="51b74-128">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="51b74-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="51b74-129">GetHeader</span></span> 

<span data-ttu-id="51b74-130">Obtiene el primer valor de encabezado de la colección que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="51b74-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="51b74-131">HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="51b74-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="51b74-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="51b74-132">GetHeaders</span></span> 

<span data-ttu-id="51b74-133">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="51b74-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="51b74-134">[GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterator)</span><span class="sxs-lookup"><span data-stu-id="51b74-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="51b74-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="51b74-135">GetIterator</span></span> 

<span data-ttu-id="51b74-136">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="51b74-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="51b74-137">[GETITERATOR](#getiterator)HRESULT ([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="51b74-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>


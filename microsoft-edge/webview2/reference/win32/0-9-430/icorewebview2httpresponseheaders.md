---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 321d18a726ac19db92018cb27d31867029991cf0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886223"
---
# <span data-ttu-id="8c7c6-104">0.9.430: ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="8c7c6-104">0.9.430 - interface ICoreWebView2HttpResponseHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="8c7c6-105">Encabezados de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="8c7c6-105">HTTP response headers.</span></span>

## <span data-ttu-id="8c7c6-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="8c7c6-106">Summary</span></span>

 <span data-ttu-id="8c7c6-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8c7c6-107">Members</span></span>                        | <span data-ttu-id="8c7c6-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="8c7c6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8c7c6-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="8c7c6-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="8c7c6-110">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="8c7c6-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="8c7c6-111">Contains</span><span class="sxs-lookup"><span data-stu-id="8c7c6-111">Contains</span></span>](#contains) | <span data-ttu-id="8c7c6-112">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="8c7c6-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="8c7c6-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="8c7c6-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="8c7c6-114">Obtiene el primer valor de encabezado de la colección que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="8c7c6-114">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="8c7c6-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="8c7c6-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="8c7c6-116">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="8c7c6-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="8c7c6-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="8c7c6-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="8c7c6-118">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="8c7c6-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="8c7c6-119">Se usa para construir un WebResourceResponse para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="8c7c6-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="8c7c6-120">Miembros</span><span class="sxs-lookup"><span data-stu-id="8c7c6-120">Members</span></span>

#### <span data-ttu-id="8c7c6-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="8c7c6-121">AppendHeader</span></span> 

<span data-ttu-id="8c7c6-122">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="8c7c6-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="8c7c6-123">[APPENDHEADER](#appendheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="8c7c6-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="8c7c6-124">Contains</span><span class="sxs-lookup"><span data-stu-id="8c7c6-124">Contains</span></span> 

<span data-ttu-id="8c7c6-125">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="8c7c6-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="8c7c6-126">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="8c7c6-126">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="8c7c6-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="8c7c6-127">GetHeader</span></span> 

<span data-ttu-id="8c7c6-128">Obtiene el primer valor de encabezado de la colección que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="8c7c6-128">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="8c7c6-129">HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="8c7c6-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="8c7c6-130">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="8c7c6-130">GetHeaders</span></span> 

<span data-ttu-id="8c7c6-131">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="8c7c6-131">Gets the header values matching the name.</span></span>

> <span data-ttu-id="8c7c6-132">[GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* iterator)</span><span class="sxs-lookup"><span data-stu-id="8c7c6-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="8c7c6-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="8c7c6-133">GetIterator</span></span> 

<span data-ttu-id="8c7c6-134">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="8c7c6-134">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="8c7c6-135">[GETITERATOR](#getiterator)HRESULT ([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="8c7c6-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


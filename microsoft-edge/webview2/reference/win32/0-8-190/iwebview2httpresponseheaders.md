---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 077c85b2458c2cf843c4d2f0548d17ec01ba4751
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885964"
---
# <span data-ttu-id="03765-104">0.8.355: IWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="03765-104">0.8.355 - interface IWebView2HttpResponseHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="03765-105">Encabezados de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="03765-105">HTTP response headers.</span></span>

## <span data-ttu-id="03765-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="03765-106">Summary</span></span>

 <span data-ttu-id="03765-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="03765-107">Members</span></span>                        | <span data-ttu-id="03765-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="03765-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="03765-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="03765-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="03765-110">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="03765-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="03765-111">Contains</span><span class="sxs-lookup"><span data-stu-id="03765-111">Contains</span></span>](#contains) | <span data-ttu-id="03765-112">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="03765-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="03765-113">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="03765-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="03765-114">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="03765-114">Gets the header values matching the name.</span></span>
[<span data-ttu-id="03765-115">GetIterator</span><span class="sxs-lookup"><span data-stu-id="03765-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="03765-116">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="03765-116">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="03765-117">Se usa para construir un WebResourceResponse para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="03765-117">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="03765-118">Miembros</span><span class="sxs-lookup"><span data-stu-id="03765-118">Members</span></span>

#### <span data-ttu-id="03765-119">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="03765-119">AppendHeader</span></span> 

<span data-ttu-id="03765-120">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="03765-120">Appends header line with name and value.</span></span>

> <span data-ttu-id="03765-121">[APPENDHEADER](#appendheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="03765-121">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="03765-122">Contains</span><span class="sxs-lookup"><span data-stu-id="03765-122">Contains</span></span> 

<span data-ttu-id="03765-123">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="03765-123">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="03765-124">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="03765-124">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="03765-125">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="03765-125">GetHeaders</span></span> 

<span data-ttu-id="03765-126">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="03765-126">Gets the header values matching the name.</span></span>

> <span data-ttu-id="03765-127">[GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* iterator)</span><span class="sxs-lookup"><span data-stu-id="03765-127">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="03765-128">GetIterator</span><span class="sxs-lookup"><span data-stu-id="03765-128">GetIterator</span></span> 

<span data-ttu-id="03765-129">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="03765-129">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="03765-130">[GETITERATOR](#getiterator)HRESULT ([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="03765-130">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


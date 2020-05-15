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
ms.openlocfilehash: 0f3564fa96bc1c13527cbf3b26ce92114d44eae4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655276"
---
# <span data-ttu-id="1ff27-104">interfaz IWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="1ff27-104">interface IWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="1ff27-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="1ff27-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="1ff27-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="1ff27-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="1ff27-107">Encabezados de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="1ff27-107">HTTP response headers.</span></span>

## <span data-ttu-id="1ff27-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="1ff27-108">Summary</span></span>

 <span data-ttu-id="1ff27-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1ff27-109">Members</span></span>                        | <span data-ttu-id="1ff27-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="1ff27-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1ff27-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="1ff27-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="1ff27-112">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="1ff27-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="1ff27-113">Contains</span><span class="sxs-lookup"><span data-stu-id="1ff27-113">Contains</span></span>](#contains) | <span data-ttu-id="1ff27-114">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="1ff27-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="1ff27-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="1ff27-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="1ff27-116">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="1ff27-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="1ff27-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="1ff27-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="1ff27-118">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="1ff27-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="1ff27-119">Se usa para construir un WebResourceResponse para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="1ff27-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="1ff27-120">Miembros</span><span class="sxs-lookup"><span data-stu-id="1ff27-120">Members</span></span>

#### <span data-ttu-id="1ff27-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="1ff27-121">AppendHeader</span></span> 

<span data-ttu-id="1ff27-122">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="1ff27-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="1ff27-123">[APPENDHEADER](#appendheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="1ff27-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="1ff27-124">Contains</span><span class="sxs-lookup"><span data-stu-id="1ff27-124">Contains</span></span> 

<span data-ttu-id="1ff27-125">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="1ff27-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="1ff27-126">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="1ff27-126">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="1ff27-127">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="1ff27-127">GetHeaders</span></span> 

<span data-ttu-id="1ff27-128">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="1ff27-128">Gets the header values matching the name.</span></span>

> <span data-ttu-id="1ff27-129">[GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* iterator)</span><span class="sxs-lookup"><span data-stu-id="1ff27-129">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="1ff27-130">GetIterator</span><span class="sxs-lookup"><span data-stu-id="1ff27-130">GetIterator</span></span> 

<span data-ttu-id="1ff27-131">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="1ff27-131">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="1ff27-132">[GETITERATOR](#getiterator)HRESULT ([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="1ff27-132">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 48a04ea60dff4cf9b6b52377927ee9085fb8bea2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878438"
---
# <span data-ttu-id="35f93-104">0.8.355: IWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="35f93-104">0.8.355 - interface IWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="35f93-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="35f93-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="35f93-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="35f93-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="35f93-107">Encabezados de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="35f93-107">HTTP response headers.</span></span>

## <span data-ttu-id="35f93-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="35f93-108">Summary</span></span>

 <span data-ttu-id="35f93-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="35f93-109">Members</span></span>                        | <span data-ttu-id="35f93-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="35f93-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="35f93-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="35f93-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="35f93-112">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="35f93-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="35f93-113">Contains</span><span class="sxs-lookup"><span data-stu-id="35f93-113">Contains</span></span>](#contains) | <span data-ttu-id="35f93-114">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="35f93-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="35f93-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="35f93-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="35f93-116">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="35f93-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="35f93-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="35f93-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="35f93-118">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="35f93-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="35f93-119">Se usa para construir un WebResourceResponse para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="35f93-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="35f93-120">Miembros</span><span class="sxs-lookup"><span data-stu-id="35f93-120">Members</span></span>

#### <span data-ttu-id="35f93-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="35f93-121">AppendHeader</span></span> 

<span data-ttu-id="35f93-122">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="35f93-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="35f93-123">[APPENDHEADER](#appendheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="35f93-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="35f93-124">Contains</span><span class="sxs-lookup"><span data-stu-id="35f93-124">Contains</span></span> 

<span data-ttu-id="35f93-125">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="35f93-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="35f93-126">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="35f93-126">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="35f93-127">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="35f93-127">GetHeaders</span></span> 

<span data-ttu-id="35f93-128">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="35f93-128">Gets the header values matching the name.</span></span>

> <span data-ttu-id="35f93-129">[GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* iterator)</span><span class="sxs-lookup"><span data-stu-id="35f93-129">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="35f93-130">GetIterator</span><span class="sxs-lookup"><span data-stu-id="35f93-130">GetIterator</span></span> 

<span data-ttu-id="35f93-131">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="35f93-131">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="35f93-132">[GETITERATOR](#getiterator)HRESULT ([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="35f93-132">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


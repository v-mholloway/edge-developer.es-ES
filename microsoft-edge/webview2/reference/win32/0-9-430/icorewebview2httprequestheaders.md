---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: a67c5c267178ea873cd12d8a22dea7409b260d52
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881000"
---
# <span data-ttu-id="a6535-104">0.9.430: ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="a6535-104">0.9.430 - interface ICoreWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="a6535-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="a6535-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="a6535-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="a6535-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="a6535-107">Encabezados de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="a6535-107">HTTP request headers.</span></span>

## <span data-ttu-id="a6535-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="a6535-108">Summary</span></span>

 <span data-ttu-id="a6535-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a6535-109">Members</span></span>                        | <span data-ttu-id="a6535-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a6535-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a6535-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="a6535-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="a6535-112">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="a6535-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="a6535-113">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="a6535-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="a6535-114">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="a6535-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="a6535-115">Contains</span><span class="sxs-lookup"><span data-stu-id="a6535-115">Contains</span></span>](#contains) | <span data-ttu-id="a6535-116">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="a6535-116">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="a6535-117">SetHeader</span><span class="sxs-lookup"><span data-stu-id="a6535-117">SetHeader</span></span>](#setheader) | <span data-ttu-id="a6535-118">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="a6535-118">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="a6535-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="a6535-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="a6535-120">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="a6535-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="a6535-121">GetIterator</span><span class="sxs-lookup"><span data-stu-id="a6535-121">GetIterator</span></span>](#getiterator) | <span data-ttu-id="a6535-122">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="a6535-122">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="a6535-123">Se usa para inspeccionar la solicitud HTTP en el evento WebResourceRequested y el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="a6535-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="a6535-124">Ten en cuenta que puedes modificar los encabezados de la solicitud HTTP desde un evento de WebResourceRequested, pero no desde un evento de NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="a6535-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="a6535-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="a6535-125">Members</span></span>

#### <span data-ttu-id="a6535-126">GetHeader</span><span class="sxs-lookup"><span data-stu-id="a6535-126">GetHeader</span></span> 

<span data-ttu-id="a6535-127">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="a6535-127">Gets the header value matching the name.</span></span>

> <span data-ttu-id="a6535-128">HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="a6535-128">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="a6535-129">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="a6535-129">GetHeaders</span></span> 

<span data-ttu-id="a6535-130">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="a6535-130">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="a6535-131">[GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* iterator)</span><span class="sxs-lookup"><span data-stu-id="a6535-131">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="a6535-132">Contains</span><span class="sxs-lookup"><span data-stu-id="a6535-132">Contains</span></span> 

<span data-ttu-id="a6535-133">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="a6535-133">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="a6535-134">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="a6535-134">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="a6535-135">SetHeader</span><span class="sxs-lookup"><span data-stu-id="a6535-135">SetHeader</span></span> 

<span data-ttu-id="a6535-136">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="a6535-136">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="a6535-137">[SETHEADER](#setheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="a6535-137">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="a6535-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="a6535-138">RemoveHeader</span></span> 

<span data-ttu-id="a6535-139">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="a6535-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="a6535-140">[REMOVEHEADER](#removeheader)HRESULT público (LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="a6535-140">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="a6535-141">GetIterator</span><span class="sxs-lookup"><span data-stu-id="a6535-141">GetIterator</span></span> 

<span data-ttu-id="a6535-142">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="a6535-142">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="a6535-143">[GETITERATOR](#getiterator)HRESULT ([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="a6535-143">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


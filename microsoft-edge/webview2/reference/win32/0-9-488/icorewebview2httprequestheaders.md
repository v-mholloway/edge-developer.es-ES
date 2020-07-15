---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 2587a3e07869076be659e29d484a647b74c2bd7f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880552"
---
# <span data-ttu-id="0e90f-104">0.9.515: ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="0e90f-104">0.9.515 - interface ICoreWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="0e90f-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="0e90f-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="0e90f-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="0e90f-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="0e90f-107">Encabezados de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="0e90f-107">HTTP request headers.</span></span>

## <span data-ttu-id="0e90f-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="0e90f-108">Summary</span></span>

 <span data-ttu-id="0e90f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0e90f-109">Members</span></span>                        | <span data-ttu-id="0e90f-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="0e90f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0e90f-111">Contains</span><span class="sxs-lookup"><span data-stu-id="0e90f-111">Contains</span></span>](#contains) | <span data-ttu-id="0e90f-112">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="0e90f-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="0e90f-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="0e90f-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="0e90f-114">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="0e90f-114">Gets the header value matching the name.</span></span>
[<span data-ttu-id="0e90f-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="0e90f-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="0e90f-116">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="0e90f-116">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="0e90f-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="0e90f-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="0e90f-118">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="0e90f-118">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="0e90f-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="0e90f-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="0e90f-120">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="0e90f-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="0e90f-121">SetHeader</span><span class="sxs-lookup"><span data-stu-id="0e90f-121">SetHeader</span></span>](#setheader) | <span data-ttu-id="0e90f-122">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="0e90f-122">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="0e90f-123">Se usa para inspeccionar la solicitud HTTP en el evento WebResourceRequested y el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="0e90f-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="0e90f-124">Ten en cuenta que puedes modificar los encabezados de la solicitud HTTP desde un evento de WebResourceRequested, pero no desde un evento de NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="0e90f-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="0e90f-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="0e90f-125">Members</span></span>

#### <span data-ttu-id="0e90f-126">Contains</span><span class="sxs-lookup"><span data-stu-id="0e90f-126">Contains</span></span> 

<span data-ttu-id="0e90f-127">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="0e90f-127">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="0e90f-128">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="0e90f-128">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="0e90f-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="0e90f-129">GetHeader</span></span> 

<span data-ttu-id="0e90f-130">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="0e90f-130">Gets the header value matching the name.</span></span>

> <span data-ttu-id="0e90f-131">HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="0e90f-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="0e90f-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="0e90f-132">GetHeaders</span></span> 

<span data-ttu-id="0e90f-133">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="0e90f-133">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="0e90f-134">[GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterator)</span><span class="sxs-lookup"><span data-stu-id="0e90f-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="0e90f-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="0e90f-135">GetIterator</span></span> 

<span data-ttu-id="0e90f-136">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="0e90f-136">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="0e90f-137">[GETITERATOR](#getiterator)HRESULT ([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="0e90f-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="0e90f-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="0e90f-138">RemoveHeader</span></span> 

<span data-ttu-id="0e90f-139">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="0e90f-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="0e90f-140">[REMOVEHEADER](#removeheader)HRESULT público (LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="0e90f-140">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="0e90f-141">SetHeader</span><span class="sxs-lookup"><span data-stu-id="0e90f-141">SetHeader</span></span> 

<span data-ttu-id="0e90f-142">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="0e90f-142">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="0e90f-143">[SETHEADER](#setheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="0e90f-143">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>


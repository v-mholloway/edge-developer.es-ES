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
ms.openlocfilehash: e12809d1db7e8c7764ad75e9a10f44ac3f445fa4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655227"
---
# <span data-ttu-id="7ff16-104">interfaz ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="7ff16-104">interface ICoreWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="7ff16-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="7ff16-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="7ff16-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="7ff16-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="7ff16-107">Encabezados de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="7ff16-107">HTTP request headers.</span></span>

## <span data-ttu-id="7ff16-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="7ff16-108">Summary</span></span>

 <span data-ttu-id="7ff16-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7ff16-109">Members</span></span>                        | <span data-ttu-id="7ff16-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7ff16-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7ff16-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="7ff16-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="7ff16-112">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="7ff16-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="7ff16-113">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="7ff16-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="7ff16-114">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="7ff16-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="7ff16-115">Contains</span><span class="sxs-lookup"><span data-stu-id="7ff16-115">Contains</span></span>](#contains) | <span data-ttu-id="7ff16-116">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="7ff16-116">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="7ff16-117">SetHeader</span><span class="sxs-lookup"><span data-stu-id="7ff16-117">SetHeader</span></span>](#setheader) | <span data-ttu-id="7ff16-118">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="7ff16-118">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="7ff16-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="7ff16-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="7ff16-120">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="7ff16-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="7ff16-121">GetIterator</span><span class="sxs-lookup"><span data-stu-id="7ff16-121">GetIterator</span></span>](#getiterator) | <span data-ttu-id="7ff16-122">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="7ff16-122">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="7ff16-123">Se usa para inspeccionar la solicitud HTTP en el evento WebResourceRequested y el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="7ff16-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="7ff16-124">Ten en cuenta que puedes modificar los encabezados de la solicitud HTTP desde un evento de WebResourceRequested, pero no desde un evento de NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="7ff16-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="7ff16-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="7ff16-125">Members</span></span>

#### <span data-ttu-id="7ff16-126">GetHeader</span><span class="sxs-lookup"><span data-stu-id="7ff16-126">GetHeader</span></span> 

<span data-ttu-id="7ff16-127">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="7ff16-127">Gets the header value matching the name.</span></span>

> <span data-ttu-id="7ff16-128">HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="7ff16-128">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="7ff16-129">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="7ff16-129">GetHeaders</span></span> 

<span data-ttu-id="7ff16-130">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="7ff16-130">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="7ff16-131">[GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* iterator)</span><span class="sxs-lookup"><span data-stu-id="7ff16-131">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="7ff16-132">Contains</span><span class="sxs-lookup"><span data-stu-id="7ff16-132">Contains</span></span> 

<span data-ttu-id="7ff16-133">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="7ff16-133">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="7ff16-134">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="7ff16-134">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="7ff16-135">SetHeader</span><span class="sxs-lookup"><span data-stu-id="7ff16-135">SetHeader</span></span> 

<span data-ttu-id="7ff16-136">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="7ff16-136">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="7ff16-137">[SETHEADER](#setheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="7ff16-137">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="7ff16-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="7ff16-138">RemoveHeader</span></span> 

<span data-ttu-id="7ff16-139">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="7ff16-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="7ff16-140">[REMOVEHEADER](#removeheader)HRESULT público (LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="7ff16-140">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="7ff16-141">GetIterator</span><span class="sxs-lookup"><span data-stu-id="7ff16-141">GetIterator</span></span> 

<span data-ttu-id="7ff16-142">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="7ff16-142">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="7ff16-143">[GETITERATOR](#getiterator)HRESULT ([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="7ff16-143">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


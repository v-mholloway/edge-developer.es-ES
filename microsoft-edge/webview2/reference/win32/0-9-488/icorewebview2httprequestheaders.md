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
ms.openlocfilehash: effceb6fafb062b1747f39876b8d2a5e02721aa8
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697276"
---
# <span data-ttu-id="081d2-104">interfaz ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="081d2-104">interface ICoreWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="081d2-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="081d2-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="081d2-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="081d2-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="081d2-107">Encabezados de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="081d2-107">HTTP request headers.</span></span>

## <span data-ttu-id="081d2-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="081d2-108">Summary</span></span>

 <span data-ttu-id="081d2-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="081d2-109">Members</span></span>                        | <span data-ttu-id="081d2-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="081d2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="081d2-111">Contains</span><span class="sxs-lookup"><span data-stu-id="081d2-111">Contains</span></span>](#contains) | <span data-ttu-id="081d2-112">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="081d2-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="081d2-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="081d2-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="081d2-114">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="081d2-114">Gets the header value matching the name.</span></span>
[<span data-ttu-id="081d2-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="081d2-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="081d2-116">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="081d2-116">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="081d2-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="081d2-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="081d2-118">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="081d2-118">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="081d2-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="081d2-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="081d2-120">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="081d2-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="081d2-121">SetHeader</span><span class="sxs-lookup"><span data-stu-id="081d2-121">SetHeader</span></span>](#setheader) | <span data-ttu-id="081d2-122">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="081d2-122">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="081d2-123">Se usa para inspeccionar la solicitud HTTP en el evento WebResourceRequested y el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="081d2-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="081d2-124">Ten en cuenta que puedes modificar los encabezados de la solicitud HTTP desde un evento de WebResourceRequested, pero no desde un evento de NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="081d2-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="081d2-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="081d2-125">Members</span></span>

#### <span data-ttu-id="081d2-126">Contains</span><span class="sxs-lookup"><span data-stu-id="081d2-126">Contains</span></span> 

<span data-ttu-id="081d2-127">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="081d2-127">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="081d2-128">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="081d2-128">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="081d2-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="081d2-129">GetHeader</span></span> 

<span data-ttu-id="081d2-130">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="081d2-130">Gets the header value matching the name.</span></span>

> <span data-ttu-id="081d2-131">HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="081d2-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="081d2-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="081d2-132">GetHeaders</span></span> 

<span data-ttu-id="081d2-133">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="081d2-133">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="081d2-134">[GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterator)</span><span class="sxs-lookup"><span data-stu-id="081d2-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="081d2-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="081d2-135">GetIterator</span></span> 

<span data-ttu-id="081d2-136">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="081d2-136">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="081d2-137">[GETITERATOR](#getiterator)HRESULT ([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="081d2-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="081d2-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="081d2-138">RemoveHeader</span></span> 

<span data-ttu-id="081d2-139">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="081d2-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="081d2-140">[REMOVEHEADER](#removeheader)HRESULT público (LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="081d2-140">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="081d2-141">SetHeader</span><span class="sxs-lookup"><span data-stu-id="081d2-141">SetHeader</span></span> 

<span data-ttu-id="081d2-142">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="081d2-142">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="081d2-143">[SETHEADER](#setheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="081d2-143">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>


---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2HttpRequestHeaders
ms.openlocfilehash: 7a59511e9d899fe4a66f2671f67f7c7cd7f101df
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011325"
---
# <span data-ttu-id="eaee6-104">0.9.579: ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="eaee6-104">0.9.579 - interface ICoreWebView2HttpRequestHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="eaee6-105">Encabezados de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="eaee6-105">HTTP request headers.</span></span>

## <span data-ttu-id="eaee6-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="eaee6-106">Summary</span></span>

 <span data-ttu-id="eaee6-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="eaee6-107">Members</span></span>                        | <span data-ttu-id="eaee6-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="eaee6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eaee6-109">Contains</span><span class="sxs-lookup"><span data-stu-id="eaee6-109">Contains</span></span>](#contains) | <span data-ttu-id="eaee6-110">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="eaee6-110">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="eaee6-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="eaee6-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="eaee6-112">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="eaee6-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="eaee6-113">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="eaee6-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="eaee6-114">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="eaee6-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="eaee6-115">GetIterator</span><span class="sxs-lookup"><span data-stu-id="eaee6-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="eaee6-116">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="eaee6-116">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="eaee6-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="eaee6-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="eaee6-118">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="eaee6-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="eaee6-119">SetHeader</span><span class="sxs-lookup"><span data-stu-id="eaee6-119">SetHeader</span></span>](#setheader) | <span data-ttu-id="eaee6-120">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="eaee6-120">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="eaee6-121">Se usa para inspeccionar la solicitud HTTP en el evento WebResourceRequested y el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="eaee6-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="eaee6-122">Ten en cuenta que puedes modificar los encabezados de la solicitud HTTP desde un evento de WebResourceRequested, pero no desde un evento de NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="eaee6-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="eaee6-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="eaee6-123">Members</span></span>

#### <span data-ttu-id="eaee6-124">Contains</span><span class="sxs-lookup"><span data-stu-id="eaee6-124">Contains</span></span> 

<span data-ttu-id="eaee6-125">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="eaee6-125">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="eaee6-126">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="eaee6-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="eaee6-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="eaee6-127">GetHeader</span></span> 

<span data-ttu-id="eaee6-128">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="eaee6-128">Gets the header value matching the name.</span></span>

> <span data-ttu-id="eaee6-129">HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="eaee6-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="eaee6-130">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="eaee6-130">GetHeaders</span></span> 

<span data-ttu-id="eaee6-131">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="eaee6-131">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="eaee6-132">[GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterator)</span><span class="sxs-lookup"><span data-stu-id="eaee6-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="eaee6-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="eaee6-133">GetIterator</span></span> 

<span data-ttu-id="eaee6-134">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="eaee6-134">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="eaee6-135">[GETITERATOR](#getiterator)HRESULT ([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="eaee6-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="eaee6-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="eaee6-136">RemoveHeader</span></span> 

<span data-ttu-id="eaee6-137">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="eaee6-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="eaee6-138">[REMOVEHEADER](#removeheader)HRESULT público (LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="eaee6-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="eaee6-139">SetHeader</span><span class="sxs-lookup"><span data-stu-id="eaee6-139">SetHeader</span></span> 

<span data-ttu-id="eaee6-140">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="eaee6-140">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="eaee6-141">[SETHEADER](#setheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="eaee6-141">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>


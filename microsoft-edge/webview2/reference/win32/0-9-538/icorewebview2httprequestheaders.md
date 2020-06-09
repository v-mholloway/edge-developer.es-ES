---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 19018ff63b62b0d76bed6dcce9cf1dbce2a37b11
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699350"
---
# <span data-ttu-id="6b813-104">interfaz ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="6b813-104">interface ICoreWebView2HttpRequestHeaders</span></span> 

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="6b813-105">Encabezados de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="6b813-105">HTTP request headers.</span></span>

## <span data-ttu-id="6b813-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="6b813-106">Summary</span></span>

 <span data-ttu-id="6b813-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6b813-107">Members</span></span>                        | <span data-ttu-id="6b813-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6b813-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6b813-109">Contains</span><span class="sxs-lookup"><span data-stu-id="6b813-109">Contains</span></span>](#contains) | <span data-ttu-id="6b813-110">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="6b813-110">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="6b813-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="6b813-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="6b813-112">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="6b813-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="6b813-113">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="6b813-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="6b813-114">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="6b813-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="6b813-115">GetIterator</span><span class="sxs-lookup"><span data-stu-id="6b813-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="6b813-116">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="6b813-116">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="6b813-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="6b813-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="6b813-118">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="6b813-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="6b813-119">SetHeader</span><span class="sxs-lookup"><span data-stu-id="6b813-119">SetHeader</span></span>](#setheader) | <span data-ttu-id="6b813-120">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="6b813-120">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="6b813-121">Se usa para inspeccionar la solicitud HTTP en el evento WebResourceRequested y el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="6b813-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="6b813-122">Ten en cuenta que puedes modificar los encabezados de la solicitud HTTP desde un evento de WebResourceRequested, pero no desde un evento de NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="6b813-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="6b813-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="6b813-123">Members</span></span>

#### <span data-ttu-id="6b813-124">Contains</span><span class="sxs-lookup"><span data-stu-id="6b813-124">Contains</span></span> 

<span data-ttu-id="6b813-125">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="6b813-125">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="6b813-126">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="6b813-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="6b813-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="6b813-127">GetHeader</span></span> 

<span data-ttu-id="6b813-128">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="6b813-128">Gets the header value matching the name.</span></span>

> <span data-ttu-id="6b813-129">HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="6b813-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="6b813-130">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="6b813-130">GetHeaders</span></span> 

<span data-ttu-id="6b813-131">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="6b813-131">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="6b813-132">[GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterator)</span><span class="sxs-lookup"><span data-stu-id="6b813-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="6b813-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="6b813-133">GetIterator</span></span> 

<span data-ttu-id="6b813-134">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="6b813-134">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="6b813-135">[GETITERATOR](#getiterator)HRESULT ([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="6b813-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="6b813-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="6b813-136">RemoveHeader</span></span> 

<span data-ttu-id="6b813-137">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="6b813-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="6b813-138">[REMOVEHEADER](#removeheader)HRESULT público (LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="6b813-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="6b813-139">SetHeader</span><span class="sxs-lookup"><span data-stu-id="6b813-139">SetHeader</span></span> 

<span data-ttu-id="6b813-140">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="6b813-140">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="6b813-141">[SETHEADER](#setheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="6b813-141">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>


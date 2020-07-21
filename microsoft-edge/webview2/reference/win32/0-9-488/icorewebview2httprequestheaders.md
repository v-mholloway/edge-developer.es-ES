---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 3197368c7ce202fae3223d517d060a23a6b21ef8
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885497"
---
# <span data-ttu-id="88eb4-104">0.9.515: ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="88eb4-104">0.9.515 - interface ICoreWebView2HttpRequestHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="88eb4-105">Encabezados de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="88eb4-105">HTTP request headers.</span></span>

## <span data-ttu-id="88eb4-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="88eb4-106">Summary</span></span>

 <span data-ttu-id="88eb4-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="88eb4-107">Members</span></span>                        | <span data-ttu-id="88eb4-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="88eb4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="88eb4-109">Contains</span><span class="sxs-lookup"><span data-stu-id="88eb4-109">Contains</span></span>](#contains) | <span data-ttu-id="88eb4-110">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="88eb4-110">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="88eb4-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="88eb4-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="88eb4-112">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="88eb4-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="88eb4-113">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="88eb4-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="88eb4-114">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="88eb4-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="88eb4-115">GetIterator</span><span class="sxs-lookup"><span data-stu-id="88eb4-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="88eb4-116">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="88eb4-116">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="88eb4-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="88eb4-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="88eb4-118">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="88eb4-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="88eb4-119">SetHeader</span><span class="sxs-lookup"><span data-stu-id="88eb4-119">SetHeader</span></span>](#setheader) | <span data-ttu-id="88eb4-120">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="88eb4-120">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="88eb4-121">Se usa para inspeccionar la solicitud HTTP en el evento WebResourceRequested y el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="88eb4-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="88eb4-122">Ten en cuenta que puedes modificar los encabezados de la solicitud HTTP desde un evento de WebResourceRequested, pero no desde un evento de NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="88eb4-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="88eb4-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="88eb4-123">Members</span></span>

#### <span data-ttu-id="88eb4-124">Contains</span><span class="sxs-lookup"><span data-stu-id="88eb4-124">Contains</span></span> 

<span data-ttu-id="88eb4-125">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="88eb4-125">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="88eb4-126">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="88eb4-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="88eb4-127">GetHeader</span><span class="sxs-lookup"><span data-stu-id="88eb4-127">GetHeader</span></span> 

<span data-ttu-id="88eb4-128">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="88eb4-128">Gets the header value matching the name.</span></span>

> <span data-ttu-id="88eb4-129">HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="88eb4-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="88eb4-130">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="88eb4-130">GetHeaders</span></span> 

<span data-ttu-id="88eb4-131">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="88eb4-131">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="88eb4-132">[GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterator)</span><span class="sxs-lookup"><span data-stu-id="88eb4-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="88eb4-133">GetIterator</span><span class="sxs-lookup"><span data-stu-id="88eb4-133">GetIterator</span></span> 

<span data-ttu-id="88eb4-134">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="88eb4-134">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="88eb4-135">[GETITERATOR](#getiterator)HRESULT ([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="88eb4-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="88eb4-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="88eb4-136">RemoveHeader</span></span> 

<span data-ttu-id="88eb4-137">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="88eb4-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="88eb4-138">[REMOVEHEADER](#removeheader)HRESULT público (LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="88eb4-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="88eb4-139">SetHeader</span><span class="sxs-lookup"><span data-stu-id="88eb4-139">SetHeader</span></span> 

<span data-ttu-id="88eb4-140">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="88eb4-140">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="88eb4-141">[SETHEADER](#setheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="88eb4-141">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>


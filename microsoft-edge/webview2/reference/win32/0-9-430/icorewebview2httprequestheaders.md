---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 04a8bf376ad7649021c4ab1555c3090cce5b52fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885614"
---
# <span data-ttu-id="3a97c-104">0.9.430: ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="3a97c-104">0.9.430 - interface ICoreWebView2HttpRequestHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="3a97c-105">Encabezados de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="3a97c-105">HTTP request headers.</span></span>

## <span data-ttu-id="3a97c-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="3a97c-106">Summary</span></span>

 <span data-ttu-id="3a97c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="3a97c-107">Members</span></span>                        | <span data-ttu-id="3a97c-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="3a97c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3a97c-109">GetHeader</span><span class="sxs-lookup"><span data-stu-id="3a97c-109">GetHeader</span></span>](#getheader) | <span data-ttu-id="3a97c-110">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="3a97c-110">Gets the header value matching the name.</span></span>
[<span data-ttu-id="3a97c-111">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="3a97c-111">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="3a97c-112">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="3a97c-112">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="3a97c-113">Contains</span><span class="sxs-lookup"><span data-stu-id="3a97c-113">Contains</span></span>](#contains) | <span data-ttu-id="3a97c-114">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="3a97c-114">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="3a97c-115">SetHeader</span><span class="sxs-lookup"><span data-stu-id="3a97c-115">SetHeader</span></span>](#setheader) | <span data-ttu-id="3a97c-116">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="3a97c-116">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="3a97c-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="3a97c-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="3a97c-118">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="3a97c-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="3a97c-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="3a97c-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="3a97c-120">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="3a97c-120">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="3a97c-121">Se usa para inspeccionar la solicitud HTTP en el evento WebResourceRequested y el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="3a97c-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="3a97c-122">Ten en cuenta que puedes modificar los encabezados de la solicitud HTTP desde un evento de WebResourceRequested, pero no desde un evento de NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="3a97c-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="3a97c-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="3a97c-123">Members</span></span>

#### <span data-ttu-id="3a97c-124">GetHeader</span><span class="sxs-lookup"><span data-stu-id="3a97c-124">GetHeader</span></span> 

<span data-ttu-id="3a97c-125">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="3a97c-125">Gets the header value matching the name.</span></span>

> <span data-ttu-id="3a97c-126">HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="3a97c-126">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="3a97c-127">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="3a97c-127">GetHeaders</span></span> 

<span data-ttu-id="3a97c-128">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="3a97c-128">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="3a97c-129">[GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* iterator)</span><span class="sxs-lookup"><span data-stu-id="3a97c-129">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="3a97c-130">Contains</span><span class="sxs-lookup"><span data-stu-id="3a97c-130">Contains</span></span> 

<span data-ttu-id="3a97c-131">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="3a97c-131">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="3a97c-132">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="3a97c-132">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="3a97c-133">SetHeader</span><span class="sxs-lookup"><span data-stu-id="3a97c-133">SetHeader</span></span> 

<span data-ttu-id="3a97c-134">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="3a97c-134">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="3a97c-135">[SETHEADER](#setheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="3a97c-135">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="3a97c-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="3a97c-136">RemoveHeader</span></span> 

<span data-ttu-id="3a97c-137">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="3a97c-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="3a97c-138">[REMOVEHEADER](#removeheader)HRESULT público (LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="3a97c-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="3a97c-139">GetIterator</span><span class="sxs-lookup"><span data-stu-id="3a97c-139">GetIterator</span></span> 

<span data-ttu-id="3a97c-140">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="3a97c-140">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="3a97c-141">[GETITERATOR](#getiterator)HRESULT ([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="3a97c-141">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


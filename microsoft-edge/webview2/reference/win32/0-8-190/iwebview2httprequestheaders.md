---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 1e0148c0d1e27cb4f1c52fb6ad55cc2e7613a94b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885971"
---
# <span data-ttu-id="2a69f-104">0.8.355: IWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="2a69f-104">0.8.355 - interface IWebView2HttpRequestHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="2a69f-105">Encabezados de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="2a69f-105">HTTP request headers.</span></span>

## <span data-ttu-id="2a69f-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="2a69f-106">Summary</span></span>

 <span data-ttu-id="2a69f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2a69f-107">Members</span></span>                        | <span data-ttu-id="2a69f-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2a69f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2a69f-109">GetHeader</span><span class="sxs-lookup"><span data-stu-id="2a69f-109">GetHeader</span></span>](#getheader) | <span data-ttu-id="2a69f-110">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="2a69f-110">Gets the header value matching the name.</span></span>
[<span data-ttu-id="2a69f-111">Contains</span><span class="sxs-lookup"><span data-stu-id="2a69f-111">Contains</span></span>](#contains) | <span data-ttu-id="2a69f-112">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="2a69f-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="2a69f-113">SetHeader</span><span class="sxs-lookup"><span data-stu-id="2a69f-113">SetHeader</span></span>](#setheader) | <span data-ttu-id="2a69f-114">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="2a69f-114">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="2a69f-115">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="2a69f-115">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="2a69f-116">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="2a69f-116">Removes header that matches the name.</span></span>
[<span data-ttu-id="2a69f-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="2a69f-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="2a69f-118">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="2a69f-118">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="2a69f-119">Se usa para inspeccionar la solicitud HTTP en el evento WebResourceRequested y el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2a69f-119">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="2a69f-120">Ten en cuenta que puedes modificar los encabezados de la solicitud HTTP desde un evento de WebResourceRequested, pero no desde un evento de NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2a69f-120">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="2a69f-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="2a69f-121">Members</span></span>

#### <span data-ttu-id="2a69f-122">GetHeader</span><span class="sxs-lookup"><span data-stu-id="2a69f-122">GetHeader</span></span> 

<span data-ttu-id="2a69f-123">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="2a69f-123">Gets the header value matching the name.</span></span>

> <span data-ttu-id="2a69f-124">HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="2a69f-124">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="2a69f-125">Contains</span><span class="sxs-lookup"><span data-stu-id="2a69f-125">Contains</span></span> 

<span data-ttu-id="2a69f-126">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="2a69f-126">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="2a69f-127">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="2a69f-127">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="2a69f-128">SetHeader</span><span class="sxs-lookup"><span data-stu-id="2a69f-128">SetHeader</span></span> 

<span data-ttu-id="2a69f-129">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="2a69f-129">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="2a69f-130">[SETHEADER](#setheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="2a69f-130">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="2a69f-131">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="2a69f-131">RemoveHeader</span></span> 

<span data-ttu-id="2a69f-132">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="2a69f-132">Removes header that matches the name.</span></span>

> <span data-ttu-id="2a69f-133">[REMOVEHEADER](#removeheader)HRESULT público (LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="2a69f-133">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="2a69f-134">GetIterator</span><span class="sxs-lookup"><span data-stu-id="2a69f-134">GetIterator</span></span> 

<span data-ttu-id="2a69f-135">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="2a69f-135">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="2a69f-136">[GETITERATOR](#getiterator)HRESULT ([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="2a69f-136">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


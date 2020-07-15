---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 162d6dde904868ad6a4864b81c0ca76d50638c06
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878459"
---
# <span data-ttu-id="c4fdc-104">0.8.355: IWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="c4fdc-104">0.8.355 - interface IWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="c4fdc-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="c4fdc-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="c4fdc-107">Encabezados de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-107">HTTP request headers.</span></span>

## <span data-ttu-id="c4fdc-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="c4fdc-108">Summary</span></span>

 <span data-ttu-id="c4fdc-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c4fdc-109">Members</span></span>                        | <span data-ttu-id="c4fdc-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="c4fdc-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c4fdc-111">GetHeader</span><span class="sxs-lookup"><span data-stu-id="c4fdc-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="c4fdc-112">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="c4fdc-113">Contains</span><span class="sxs-lookup"><span data-stu-id="c4fdc-113">Contains</span></span>](#contains) | <span data-ttu-id="c4fdc-114">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-114">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="c4fdc-115">SetHeader</span><span class="sxs-lookup"><span data-stu-id="c4fdc-115">SetHeader</span></span>](#setheader) | <span data-ttu-id="c4fdc-116">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-116">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="c4fdc-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="c4fdc-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="c4fdc-118">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="c4fdc-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="c4fdc-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="c4fdc-120">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-120">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="c4fdc-121">Se usa para inspeccionar la solicitud HTTP en el evento WebResourceRequested y el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="c4fdc-122">Ten en cuenta que puedes modificar los encabezados de la solicitud HTTP desde un evento de WebResourceRequested, pero no desde un evento de NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="c4fdc-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="c4fdc-123">Members</span></span>

#### <span data-ttu-id="c4fdc-124">GetHeader</span><span class="sxs-lookup"><span data-stu-id="c4fdc-124">GetHeader</span></span> 

<span data-ttu-id="c4fdc-125">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-125">Gets the header value matching the name.</span></span>

> <span data-ttu-id="c4fdc-126">HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr \* Value)</span><span class="sxs-lookup"><span data-stu-id="c4fdc-126">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="c4fdc-127">Contains</span><span class="sxs-lookup"><span data-stu-id="c4fdc-127">Contains</span></span> 

<span data-ttu-id="c4fdc-128">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-128">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="c4fdc-129">el valor HRESULT público [contiene](#contains)(LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="c4fdc-129">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="c4fdc-130">SetHeader</span><span class="sxs-lookup"><span data-stu-id="c4fdc-130">SetHeader</span></span> 

<span data-ttu-id="c4fdc-131">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-131">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="c4fdc-132">[SETHEADER](#setheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)</span><span class="sxs-lookup"><span data-stu-id="c4fdc-132">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="c4fdc-133">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="c4fdc-133">RemoveHeader</span></span> 

<span data-ttu-id="c4fdc-134">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-134">Removes header that matches the name.</span></span>

> <span data-ttu-id="c4fdc-135">[REMOVEHEADER](#removeheader)HRESULT público (LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="c4fdc-135">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="c4fdc-136">GetIterator</span><span class="sxs-lookup"><span data-stu-id="c4fdc-136">GetIterator</span></span> 

<span data-ttu-id="c4fdc-137">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="c4fdc-137">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="c4fdc-138">[GETITERATOR](#getiterator)HRESULT ([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* iterador)</span><span class="sxs-lookup"><span data-stu-id="c4fdc-138">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>


---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
ms.openlocfilehash: 1441d5a45caf4e8f561de2487438b66e067760f6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012606"
---
# <span data-ttu-id="26243-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="26243-104">Microsoft.Web.WebView2.Core.CoreWebView2HttpRequestHeaders class</span></span> 

<span data-ttu-id="26243-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="26243-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="26243-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="26243-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="26243-107">Encabezados de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="26243-107">HTTP request headers.</span></span>

## <span data-ttu-id="26243-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="26243-108">Summary</span></span>

 <span data-ttu-id="26243-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="26243-109">Members</span></span>                        | <span data-ttu-id="26243-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="26243-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="26243-111">Contains</span><span class="sxs-lookup"><span data-stu-id="26243-111">Contains</span></span>](#contains) | <span data-ttu-id="26243-112">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="26243-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="26243-113">GetHeader</span><span class="sxs-lookup"><span data-stu-id="26243-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="26243-114">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="26243-114">Gets the header value matching the name.</span></span>
[<span data-ttu-id="26243-115">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="26243-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="26243-116">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="26243-116">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="26243-117">GetIterator</span><span class="sxs-lookup"><span data-stu-id="26243-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="26243-118">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="26243-118">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="26243-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="26243-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="26243-120">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="26243-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="26243-121">SetHeader</span><span class="sxs-lookup"><span data-stu-id="26243-121">SetHeader</span></span>](#setheader) | <span data-ttu-id="26243-122">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="26243-122">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="26243-123">Se usa para inspeccionar la solicitud HTTP en el evento WebResourceRequested y el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="26243-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="26243-124">Ten en cuenta que puedes modificar los encabezados de la solicitud HTTP desde un evento de WebResourceRequested, pero no desde un evento de NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="26243-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="26243-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="26243-125">Members</span></span>

#### <span data-ttu-id="26243-126">Contains</span><span class="sxs-lookup"><span data-stu-id="26243-126">Contains</span></span> 

<span data-ttu-id="26243-127">Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="26243-127">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="26243-128">Public bool [contiene](#contains)(cadena nombre)</span><span class="sxs-lookup"><span data-stu-id="26243-128">public bool [Contains](#contains)(string name)</span></span>

#### <span data-ttu-id="26243-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="26243-129">GetHeader</span></span> 

<span data-ttu-id="26243-130">Obtiene el valor de encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="26243-130">Gets the header value matching the name.</span></span>

> <span data-ttu-id="26243-131">cadena pública [GetHeader](#getheader)(cadena nombre)</span><span class="sxs-lookup"><span data-stu-id="26243-131">public string [GetHeader](#getheader)(string name)</span></span>

#### <span data-ttu-id="26243-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="26243-132">GetHeaders</span></span> 

<span data-ttu-id="26243-133">Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.</span><span class="sxs-lookup"><span data-stu-id="26243-133">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="26243-134">Public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(cadena nombre)</span><span class="sxs-lookup"><span data-stu-id="26243-134">public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(string name)</span></span>

#### <span data-ttu-id="26243-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="26243-135">GetIterator</span></span> 

<span data-ttu-id="26243-136">Obtiene un iterador en la colección de encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="26243-136">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="26243-137">Public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()</span><span class="sxs-lookup"><span data-stu-id="26243-137">public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()</span></span>

#### <span data-ttu-id="26243-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="26243-138">RemoveHeader</span></span> 

<span data-ttu-id="26243-139">Quita el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="26243-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="26243-140">public void [RemoveHeader](#removeheader)(string name)</span><span class="sxs-lookup"><span data-stu-id="26243-140">public void [RemoveHeader](#removeheader)(string name)</span></span>

#### <span data-ttu-id="26243-141">SetHeader</span><span class="sxs-lookup"><span data-stu-id="26243-141">SetHeader</span></span> 

<span data-ttu-id="26243-142">Agrega o actualiza el encabezado que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="26243-142">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="26243-143">public void [SetHeader](#setheader)(string name, valor de cadena)</span><span class="sxs-lookup"><span data-stu-id="26243-143">public void [SetHeader](#setheader)(string name, string value)</span></span>


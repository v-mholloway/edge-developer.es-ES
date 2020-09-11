---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders
ms.openlocfilehash: 51218283460975421859c65da8a43553767ad216
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012670"
---
# <span data-ttu-id="15989-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="15989-104">Microsoft.Web.WebView2.Core.CoreWebView2HttpResponseHeaders class</span></span> 

<span data-ttu-id="15989-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="15989-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="15989-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="15989-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="15989-107">Encabezados de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="15989-107">HTTP response headers.</span></span>

## <span data-ttu-id="15989-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="15989-108">Summary</span></span>

 <span data-ttu-id="15989-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="15989-109">Members</span></span>                        | <span data-ttu-id="15989-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="15989-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="15989-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="15989-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="15989-112">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="15989-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="15989-113">Contains</span><span class="sxs-lookup"><span data-stu-id="15989-113">Contains</span></span>](#contains) | <span data-ttu-id="15989-114">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="15989-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="15989-115">GetHeader</span><span class="sxs-lookup"><span data-stu-id="15989-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="15989-116">Obtiene el primer valor de encabezado de la colección que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="15989-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="15989-117">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="15989-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="15989-118">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="15989-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="15989-119">GetIterator</span><span class="sxs-lookup"><span data-stu-id="15989-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="15989-120">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="15989-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="15989-121">Se usa para construir un WebResourceResponse para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="15989-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="15989-122">Miembros</span><span class="sxs-lookup"><span data-stu-id="15989-122">Members</span></span>

#### <span data-ttu-id="15989-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="15989-123">AppendHeader</span></span> 

<span data-ttu-id="15989-124">Anexa la línea de encabezado con el nombre y el valor.</span><span class="sxs-lookup"><span data-stu-id="15989-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="15989-125">public void [AppendHeader](#appendheader)(string name, valor de cadena)</span><span class="sxs-lookup"><span data-stu-id="15989-125">public void [AppendHeader](#appendheader)(string name, string value)</span></span>

#### <span data-ttu-id="15989-126">Contains</span><span class="sxs-lookup"><span data-stu-id="15989-126">Contains</span></span> 

<span data-ttu-id="15989-127">Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="15989-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="15989-128">Public bool [contiene](#contains)(cadena nombre)</span><span class="sxs-lookup"><span data-stu-id="15989-128">public bool [Contains](#contains)(string name)</span></span>

#### <span data-ttu-id="15989-129">GetHeader</span><span class="sxs-lookup"><span data-stu-id="15989-129">GetHeader</span></span> 

<span data-ttu-id="15989-130">Obtiene el primer valor de encabezado de la colección que coincide con el nombre.</span><span class="sxs-lookup"><span data-stu-id="15989-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="15989-131">cadena pública [GetHeader](#getheader)(cadena nombre)</span><span class="sxs-lookup"><span data-stu-id="15989-131">public string [GetHeader](#getheader)(string name)</span></span>

#### <span data-ttu-id="15989-132">GetHeaders</span><span class="sxs-lookup"><span data-stu-id="15989-132">GetHeaders</span></span> 

<span data-ttu-id="15989-133">Obtiene los valores de encabezado que coinciden con el nombre.</span><span class="sxs-lookup"><span data-stu-id="15989-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="15989-134">Public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(cadena nombre)</span><span class="sxs-lookup"><span data-stu-id="15989-134">public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(string name)</span></span>

#### <span data-ttu-id="15989-135">GetIterator</span><span class="sxs-lookup"><span data-stu-id="15989-135">GetIterator</span></span> 

<span data-ttu-id="15989-136">Obtiene un iterador sobre la colección de encabezados de respuesta completos.</span><span class="sxs-lookup"><span data-stu-id="15989-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="15989-137">Public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()</span><span class="sxs-lookup"><span data-stu-id="15989-137">public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()</span></span>


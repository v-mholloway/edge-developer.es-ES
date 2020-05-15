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
ms.openlocfilehash: d6b51600479f47eebb09d5cff8fb096455fb1766
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655120"
---
# <span data-ttu-id="dc71a-104">interfaz ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="dc71a-104">interface ICoreWebView2WebResourceResponse</span></span> 

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="dc71a-105">Una respuesta HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="dc71a-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="dc71a-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="dc71a-106">Summary</span></span>

 <span data-ttu-id="dc71a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="dc71a-107">Members</span></span>                        | <span data-ttu-id="dc71a-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="dc71a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dc71a-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="dc71a-109">get_Content</span></span>](#get_content) | <span data-ttu-id="dc71a-110">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="dc71a-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="dc71a-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="dc71a-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="dc71a-112">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="dc71a-112">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="dc71a-113">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="dc71a-113">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="dc71a-114">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="dc71a-114">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="dc71a-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="dc71a-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="dc71a-116">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="dc71a-116">The HTTP response status code.</span></span>
[<span data-ttu-id="dc71a-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="dc71a-117">put_Content</span></span>](#put_content) | <span data-ttu-id="dc71a-118">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="dc71a-118">Set the Content property.</span></span>
[<span data-ttu-id="dc71a-119">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="dc71a-119">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="dc71a-120">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="dc71a-120">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="dc71a-121">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="dc71a-121">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="dc71a-122">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="dc71a-122">Set the StatusCode property.</span></span>

## <span data-ttu-id="dc71a-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="dc71a-123">Members</span></span>

#### <span data-ttu-id="dc71a-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="dc71a-124">get_Content</span></span> 

<span data-ttu-id="dc71a-125">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="dc71a-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="dc71a-126">[get_Content](#get_content)(HRESULT) público (contenido de IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="dc71a-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="dc71a-127">La secuencia debe tener todos los datos de contenido disponibles por el momento en que se completa este aplazamiento de eventos de WebResourceRequested de respuesta.</span><span class="sxs-lookup"><span data-stu-id="dc71a-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="dc71a-128">La secuencia debe ser ágil o crearse a partir de un subproceso en segundo plano para evitar el impacto en el rendimiento del subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="dc71a-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="dc71a-129">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="dc71a-129">Null means no content data.</span></span> <span data-ttu-id="dc71a-130">Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)</span><span class="sxs-lookup"><span data-stu-id="dc71a-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="dc71a-131">get_Headers</span><span class="sxs-lookup"><span data-stu-id="dc71a-131">get_Headers</span></span> 

<span data-ttu-id="dc71a-132">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="dc71a-132">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="dc71a-133">[get_Headers](#get_headers)de HRESULT público (encabezados[ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="dc71a-133">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="dc71a-134">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="dc71a-134">get_ReasonPhrase</span></span> 

<span data-ttu-id="dc71a-135">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="dc71a-135">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="dc71a-136">[get_ReasonPhrase](#get_reasonphrase)de HRESULT público (LPWStr \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="dc71a-136">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="dc71a-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="dc71a-137">get_StatusCode</span></span> 

<span data-ttu-id="dc71a-138">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="dc71a-138">The HTTP response status code.</span></span>

> <span data-ttu-id="dc71a-139">[get_StatusCode](#get_statuscode)de HRESULT público (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="dc71a-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="dc71a-140">put_Content</span><span class="sxs-lookup"><span data-stu-id="dc71a-140">put_Content</span></span> 

<span data-ttu-id="dc71a-141">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="dc71a-141">Set the Content property.</span></span>

> <span data-ttu-id="dc71a-142">[put_Content](#put_content)(HRESULT) público (contenido de IStream \*)</span><span class="sxs-lookup"><span data-stu-id="dc71a-142">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="dc71a-143">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="dc71a-143">put_ReasonPhrase</span></span> 

<span data-ttu-id="dc71a-144">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="dc71a-144">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="dc71a-145">[put_ReasonPhrase](#put_reasonphrase)pública HRESULT (LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="dc71a-145">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="dc71a-146">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="dc71a-146">put_StatusCode</span></span> 

<span data-ttu-id="dc71a-147">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="dc71a-147">Set the StatusCode property.</span></span>

> <span data-ttu-id="dc71a-148">[put_StatusCode](#put_statuscode)de HRESULT público (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="dc71a-148">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>


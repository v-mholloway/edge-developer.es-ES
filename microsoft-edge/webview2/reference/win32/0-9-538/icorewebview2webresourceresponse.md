---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2WebResourceResponse
ms.openlocfilehash: 551486afae47dc5dcedf4e2119d5f8fed5066c2e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879537"
---
# <span data-ttu-id="f97c4-104">interfaz ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="f97c4-104">interface ICoreWebView2WebResourceResponse</span></span> 

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="f97c4-105">Una respuesta HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="f97c4-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="f97c4-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="f97c4-106">Summary</span></span>

 <span data-ttu-id="f97c4-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f97c4-107">Members</span></span>                        | <span data-ttu-id="f97c4-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="f97c4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f97c4-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="f97c4-109">get_Content</span></span>](#get_content) | <span data-ttu-id="f97c4-110">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="f97c4-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="f97c4-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="f97c4-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="f97c4-112">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="f97c4-112">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="f97c4-113">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="f97c4-113">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="f97c4-114">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f97c4-114">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="f97c4-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="f97c4-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="f97c4-116">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f97c4-116">The HTTP response status code.</span></span>
[<span data-ttu-id="f97c4-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="f97c4-117">put_Content</span></span>](#put_content) | <span data-ttu-id="f97c4-118">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="f97c4-118">Set the Content property.</span></span>
[<span data-ttu-id="f97c4-119">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="f97c4-119">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="f97c4-120">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="f97c4-120">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="f97c4-121">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="f97c4-121">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="f97c4-122">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="f97c4-122">Set the StatusCode property.</span></span>

## <span data-ttu-id="f97c4-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="f97c4-123">Members</span></span>

#### <span data-ttu-id="f97c4-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="f97c4-124">get_Content</span></span> 

<span data-ttu-id="f97c4-125">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="f97c4-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="f97c4-126">[get_Content](#get_content)(HRESULT) público (contenido de IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="f97c4-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="f97c4-127">La secuencia debe tener todos los datos de contenido disponibles por el momento en que se completa este aplazamiento de eventos de WebResourceRequested de respuesta.</span><span class="sxs-lookup"><span data-stu-id="f97c4-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="f97c4-128">La secuencia debe ser ágil o crearse a partir de un subproceso en segundo plano para evitar el impacto en el rendimiento del subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="f97c4-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="f97c4-129">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="f97c4-129">Null means no content data.</span></span> <span data-ttu-id="f97c4-130">Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)</span><span class="sxs-lookup"><span data-stu-id="f97c4-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="f97c4-131">get_Headers</span><span class="sxs-lookup"><span data-stu-id="f97c4-131">get_Headers</span></span> 

<span data-ttu-id="f97c4-132">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="f97c4-132">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="f97c4-133">[get_Headers](#get_headers)de HRESULT público (encabezados[ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="f97c4-133">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="f97c4-134">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="f97c4-134">get_ReasonPhrase</span></span> 

<span data-ttu-id="f97c4-135">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f97c4-135">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="f97c4-136">[get_ReasonPhrase](#get_reasonphrase)de HRESULT público (LPWStr \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="f97c4-136">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="f97c4-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="f97c4-137">get_StatusCode</span></span> 

<span data-ttu-id="f97c4-138">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f97c4-138">The HTTP response status code.</span></span>

> <span data-ttu-id="f97c4-139">[get_StatusCode](#get_statuscode)de HRESULT público (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="f97c4-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="f97c4-140">put_Content</span><span class="sxs-lookup"><span data-stu-id="f97c4-140">put_Content</span></span> 

<span data-ttu-id="f97c4-141">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="f97c4-141">Set the Content property.</span></span>

> <span data-ttu-id="f97c4-142">[put_Content](#put_content)(HRESULT) público (contenido de IStream \*)</span><span class="sxs-lookup"><span data-stu-id="f97c4-142">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="f97c4-143">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="f97c4-143">put_ReasonPhrase</span></span> 

<span data-ttu-id="f97c4-144">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="f97c4-144">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="f97c4-145">[put_ReasonPhrase](#put_reasonphrase)pública HRESULT (LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="f97c4-145">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="f97c4-146">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="f97c4-146">put_StatusCode</span></span> 

<span data-ttu-id="f97c4-147">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="f97c4-147">Set the StatusCode property.</span></span>

> <span data-ttu-id="f97c4-148">[put_StatusCode](#put_statuscode)de HRESULT público (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="f97c4-148">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>


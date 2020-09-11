---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2WebResourceResponse
ms.openlocfilehash: f259a9e6630470ed0557c4ab9593fdb1b8bbced2
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012615"
---
# <span data-ttu-id="7fa70-104">interfaz ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="7fa70-104">interface ICoreWebView2WebResourceResponse</span></span> 

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="7fa70-105">Una respuesta HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="7fa70-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="7fa70-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="7fa70-106">Summary</span></span>

 <span data-ttu-id="7fa70-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7fa70-107">Members</span></span>                        | <span data-ttu-id="7fa70-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7fa70-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7fa70-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="7fa70-109">get_Content</span></span>](#get_content) | <span data-ttu-id="7fa70-110">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="7fa70-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="7fa70-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="7fa70-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="7fa70-112">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="7fa70-112">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="7fa70-113">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="7fa70-113">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="7fa70-114">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="7fa70-114">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="7fa70-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="7fa70-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="7fa70-116">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="7fa70-116">The HTTP response status code.</span></span>
[<span data-ttu-id="7fa70-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="7fa70-117">put_Content</span></span>](#put_content) | <span data-ttu-id="7fa70-118">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="7fa70-118">Set the Content property.</span></span>
[<span data-ttu-id="7fa70-119">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="7fa70-119">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="7fa70-120">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="7fa70-120">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="7fa70-121">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="7fa70-121">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="7fa70-122">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="7fa70-122">Set the StatusCode property.</span></span>

## <span data-ttu-id="7fa70-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="7fa70-123">Members</span></span>

#### <span data-ttu-id="7fa70-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="7fa70-124">get_Content</span></span> 

<span data-ttu-id="7fa70-125">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="7fa70-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="7fa70-126">[get_Content](#get_content)(HRESULT) público (contenido de IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="7fa70-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="7fa70-127">La secuencia debe tener todos los datos de contenido disponibles por el momento en que se completa este aplazamiento de eventos de WebResourceRequested de respuesta.</span><span class="sxs-lookup"><span data-stu-id="7fa70-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="7fa70-128">La secuencia debe ser ágil o crearse a partir de un subproceso en segundo plano para evitar el impacto en el rendimiento del subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="7fa70-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="7fa70-129">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="7fa70-129">Null means no content data.</span></span> <span data-ttu-id="7fa70-130">Se aplican las semánticas de IStream (devuelva S_OK para leer las llamadas hasta que se agoten todos los datos).</span><span class="sxs-lookup"><span data-stu-id="7fa70-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted).</span></span>

#### <span data-ttu-id="7fa70-131">get_Headers</span><span class="sxs-lookup"><span data-stu-id="7fa70-131">get_Headers</span></span> 

<span data-ttu-id="7fa70-132">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="7fa70-132">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="7fa70-133">[get_Headers](#get_headers)de HRESULT público (encabezados[ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="7fa70-133">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="7fa70-134">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="7fa70-134">get_ReasonPhrase</span></span> 

<span data-ttu-id="7fa70-135">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="7fa70-135">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="7fa70-136">[get_ReasonPhrase](#get_reasonphrase)de HRESULT público (LPWStr \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="7fa70-136">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="7fa70-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="7fa70-137">get_StatusCode</span></span> 

<span data-ttu-id="7fa70-138">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="7fa70-138">The HTTP response status code.</span></span>

> <span data-ttu-id="7fa70-139">[get_StatusCode](#get_statuscode)de HRESULT público (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="7fa70-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="7fa70-140">put_Content</span><span class="sxs-lookup"><span data-stu-id="7fa70-140">put_Content</span></span> 

<span data-ttu-id="7fa70-141">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="7fa70-141">Set the Content property.</span></span>

> <span data-ttu-id="7fa70-142">[put_Content](#put_content)(HRESULT) público (contenido de IStream \*)</span><span class="sxs-lookup"><span data-stu-id="7fa70-142">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="7fa70-143">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="7fa70-143">put_ReasonPhrase</span></span> 

<span data-ttu-id="7fa70-144">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="7fa70-144">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="7fa70-145">[put_ReasonPhrase](#put_reasonphrase)pública HRESULT (LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="7fa70-145">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="7fa70-146">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="7fa70-146">put_StatusCode</span></span> 

<span data-ttu-id="7fa70-147">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="7fa70-147">Set the StatusCode property.</span></span>

> <span data-ttu-id="7fa70-148">[put_StatusCode](#put_statuscode)de HRESULT público (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="7fa70-148">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 6d28a5e0b08406cdf83b7e0a60428463e9647d45
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655267"
---
# <span data-ttu-id="4d564-104">interfaz ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="4d564-104">interface ICoreWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="4d564-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="4d564-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="4d564-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="4d564-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="4d564-107">Una respuesta HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="4d564-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="4d564-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="4d564-108">Summary</span></span>

 <span data-ttu-id="4d564-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="4d564-109">Members</span></span>                        | <span data-ttu-id="4d564-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="4d564-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4d564-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="4d564-111">get_Content</span></span>](#get_content) | <span data-ttu-id="4d564-112">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="4d564-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="4d564-113">put_Content</span><span class="sxs-lookup"><span data-stu-id="4d564-113">put_Content</span></span>](#put_content) | <span data-ttu-id="4d564-114">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="4d564-114">Set the Content property.</span></span>
[<span data-ttu-id="4d564-115">get_Headers</span><span class="sxs-lookup"><span data-stu-id="4d564-115">get_Headers</span></span>](#get_headers) | <span data-ttu-id="4d564-116">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="4d564-116">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="4d564-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="4d564-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="4d564-118">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="4d564-118">The HTTP response status code.</span></span>
[<span data-ttu-id="4d564-119">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="4d564-119">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="4d564-120">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="4d564-120">Set the StatusCode property.</span></span>
[<span data-ttu-id="4d564-121">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="4d564-121">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="4d564-122">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="4d564-122">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="4d564-123">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="4d564-123">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="4d564-124">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="4d564-124">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="4d564-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="4d564-125">Members</span></span>

#### <span data-ttu-id="4d564-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="4d564-126">get_Content</span></span> 

<span data-ttu-id="4d564-127">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="4d564-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="4d564-128">[get_Content](#get_content)(HRESULT) público (contenido de IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="4d564-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="4d564-129">La secuencia debe tener todos los datos de contenido disponibles por el momento en que se completa este aplazamiento de eventos de WebResourceRequested de respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d564-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="4d564-130">La secuencia debe ser ágil o crearse a partir de un subproceso en segundo plano para evitar el impacto en el rendimiento del subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4d564-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="4d564-131">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="4d564-131">Null means no content data.</span></span> <span data-ttu-id="4d564-132">Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)</span><span class="sxs-lookup"><span data-stu-id="4d564-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="4d564-133">put_Content</span><span class="sxs-lookup"><span data-stu-id="4d564-133">put_Content</span></span> 

<span data-ttu-id="4d564-134">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="4d564-134">Set the Content property.</span></span>

> <span data-ttu-id="4d564-135">[put_Content](#put_content)(HRESULT) público (contenido de IStream \*)</span><span class="sxs-lookup"><span data-stu-id="4d564-135">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="4d564-136">get_Headers</span><span class="sxs-lookup"><span data-stu-id="4d564-136">get_Headers</span></span> 

<span data-ttu-id="4d564-137">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="4d564-137">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="4d564-138">[get_Headers](#get_headers)de HRESULT público (encabezados[ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="4d564-138">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="4d564-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="4d564-139">get_StatusCode</span></span> 

<span data-ttu-id="4d564-140">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="4d564-140">The HTTP response status code.</span></span>

> <span data-ttu-id="4d564-141">[get_StatusCode](#get_statuscode)de HRESULT público (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="4d564-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="4d564-142">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="4d564-142">put_StatusCode</span></span> 

<span data-ttu-id="4d564-143">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="4d564-143">Set the StatusCode property.</span></span>

> <span data-ttu-id="4d564-144">[put_StatusCode](#put_statuscode)de HRESULT público (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="4d564-144">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="4d564-145">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="4d564-145">get_ReasonPhrase</span></span> 

<span data-ttu-id="4d564-146">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="4d564-146">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="4d564-147">[get_ReasonPhrase](#get_reasonphrase)de HRESULT público (LPWStr \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="4d564-147">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="4d564-148">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="4d564-148">put_ReasonPhrase</span></span> 

<span data-ttu-id="4d564-149">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="4d564-149">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="4d564-150">[put_ReasonPhrase](#put_reasonphrase)pública HRESULT (LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="4d564-150">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 7a649944686df4d425141d5d22c03c5874572d1a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877346"
---
# <span data-ttu-id="3c268-104">0.9.515: ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="3c268-104">0.9.515 - interface ICoreWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="3c268-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="3c268-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="3c268-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="3c268-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="3c268-107">Una respuesta HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="3c268-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="3c268-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="3c268-108">Summary</span></span>

 <span data-ttu-id="3c268-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="3c268-109">Members</span></span>                        | <span data-ttu-id="3c268-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="3c268-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3c268-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="3c268-111">get_Content</span></span>](#get_content) | <span data-ttu-id="3c268-112">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="3c268-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="3c268-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="3c268-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="3c268-114">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="3c268-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="3c268-115">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="3c268-115">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="3c268-116">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="3c268-116">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="3c268-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="3c268-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="3c268-118">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="3c268-118">The HTTP response status code.</span></span>
[<span data-ttu-id="3c268-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="3c268-119">put_Content</span></span>](#put_content) | <span data-ttu-id="3c268-120">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="3c268-120">Set the Content property.</span></span>
[<span data-ttu-id="3c268-121">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="3c268-121">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="3c268-122">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="3c268-122">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="3c268-123">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="3c268-123">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="3c268-124">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="3c268-124">Set the StatusCode property.</span></span>

## <span data-ttu-id="3c268-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="3c268-125">Members</span></span>

#### <span data-ttu-id="3c268-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="3c268-126">get_Content</span></span> 

<span data-ttu-id="3c268-127">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="3c268-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="3c268-128">[get_Content](#get_content)(HRESULT) público (contenido de IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="3c268-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="3c268-129">La secuencia debe tener todos los datos de contenido disponibles por el momento en que se completa este aplazamiento de eventos de WebResourceRequested de respuesta.</span><span class="sxs-lookup"><span data-stu-id="3c268-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="3c268-130">La secuencia debe ser ágil o crearse a partir de un subproceso en segundo plano para evitar el impacto en el rendimiento del subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="3c268-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="3c268-131">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="3c268-131">Null means no content data.</span></span> <span data-ttu-id="3c268-132">Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)</span><span class="sxs-lookup"><span data-stu-id="3c268-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="3c268-133">get_Headers</span><span class="sxs-lookup"><span data-stu-id="3c268-133">get_Headers</span></span> 

<span data-ttu-id="3c268-134">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="3c268-134">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="3c268-135">[get_Headers](#get_headers)de HRESULT público (encabezados[ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="3c268-135">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="3c268-136">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="3c268-136">get_ReasonPhrase</span></span> 

<span data-ttu-id="3c268-137">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="3c268-137">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="3c268-138">[get_ReasonPhrase](#get_reasonphrase)de HRESULT público (LPWStr \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="3c268-138">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="3c268-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="3c268-139">get_StatusCode</span></span> 

<span data-ttu-id="3c268-140">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="3c268-140">The HTTP response status code.</span></span>

> <span data-ttu-id="3c268-141">[get_StatusCode](#get_statuscode)de HRESULT público (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="3c268-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="3c268-142">put_Content</span><span class="sxs-lookup"><span data-stu-id="3c268-142">put_Content</span></span> 

<span data-ttu-id="3c268-143">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="3c268-143">Set the Content property.</span></span>

> <span data-ttu-id="3c268-144">[put_Content](#put_content)(HRESULT) público (contenido de IStream \*)</span><span class="sxs-lookup"><span data-stu-id="3c268-144">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="3c268-145">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="3c268-145">put_ReasonPhrase</span></span> 

<span data-ttu-id="3c268-146">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="3c268-146">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="3c268-147">[put_ReasonPhrase](#put_reasonphrase)pública HRESULT (LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="3c268-147">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="3c268-148">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="3c268-148">put_StatusCode</span></span> 

<span data-ttu-id="3c268-149">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="3c268-149">Set the StatusCode property.</span></span>

> <span data-ttu-id="3c268-150">[put_StatusCode](#put_statuscode)de HRESULT público (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="3c268-150">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>


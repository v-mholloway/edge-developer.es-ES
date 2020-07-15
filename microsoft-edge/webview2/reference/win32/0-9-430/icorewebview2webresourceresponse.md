---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: c0c33bab95f8d2c7908864b1869bc9a186216ef9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877549"
---
# <span data-ttu-id="97088-104">0.9.430: ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="97088-104">0.9.430 - interface ICoreWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="97088-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="97088-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="97088-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="97088-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="97088-107">Una respuesta HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="97088-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="97088-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="97088-108">Summary</span></span>

 <span data-ttu-id="97088-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="97088-109">Members</span></span>                        | <span data-ttu-id="97088-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="97088-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="97088-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="97088-111">get_Content</span></span>](#get_content) | <span data-ttu-id="97088-112">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="97088-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="97088-113">put_Content</span><span class="sxs-lookup"><span data-stu-id="97088-113">put_Content</span></span>](#put_content) | <span data-ttu-id="97088-114">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="97088-114">Set the Content property.</span></span>
[<span data-ttu-id="97088-115">get_Headers</span><span class="sxs-lookup"><span data-stu-id="97088-115">get_Headers</span></span>](#get_headers) | <span data-ttu-id="97088-116">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="97088-116">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="97088-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="97088-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="97088-118">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="97088-118">The HTTP response status code.</span></span>
[<span data-ttu-id="97088-119">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="97088-119">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="97088-120">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="97088-120">Set the StatusCode property.</span></span>
[<span data-ttu-id="97088-121">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="97088-121">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="97088-122">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="97088-122">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="97088-123">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="97088-123">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="97088-124">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="97088-124">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="97088-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="97088-125">Members</span></span>

#### <span data-ttu-id="97088-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="97088-126">get_Content</span></span> 

<span data-ttu-id="97088-127">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="97088-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="97088-128">[get_Content](#get_content)(HRESULT) público (contenido de IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="97088-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="97088-129">La secuencia debe tener todos los datos de contenido disponibles por el momento en que se completa este aplazamiento de eventos de WebResourceRequested de respuesta.</span><span class="sxs-lookup"><span data-stu-id="97088-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="97088-130">La secuencia debe ser ágil o crearse a partir de un subproceso en segundo plano para evitar el impacto en el rendimiento del subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="97088-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="97088-131">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="97088-131">Null means no content data.</span></span> <span data-ttu-id="97088-132">Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)</span><span class="sxs-lookup"><span data-stu-id="97088-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="97088-133">put_Content</span><span class="sxs-lookup"><span data-stu-id="97088-133">put_Content</span></span> 

<span data-ttu-id="97088-134">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="97088-134">Set the Content property.</span></span>

> <span data-ttu-id="97088-135">[put_Content](#put_content)(HRESULT) público (contenido de IStream \*)</span><span class="sxs-lookup"><span data-stu-id="97088-135">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="97088-136">get_Headers</span><span class="sxs-lookup"><span data-stu-id="97088-136">get_Headers</span></span> 

<span data-ttu-id="97088-137">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="97088-137">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="97088-138">[get_Headers](#get_headers)de HRESULT público (encabezados[ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="97088-138">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="97088-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="97088-139">get_StatusCode</span></span> 

<span data-ttu-id="97088-140">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="97088-140">The HTTP response status code.</span></span>

> <span data-ttu-id="97088-141">[get_StatusCode](#get_statuscode)de HRESULT público (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="97088-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="97088-142">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="97088-142">put_StatusCode</span></span> 

<span data-ttu-id="97088-143">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="97088-143">Set the StatusCode property.</span></span>

> <span data-ttu-id="97088-144">[put_StatusCode](#put_statuscode)de HRESULT público (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="97088-144">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="97088-145">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="97088-145">get_ReasonPhrase</span></span> 

<span data-ttu-id="97088-146">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="97088-146">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="97088-147">[get_ReasonPhrase](#get_reasonphrase)de HRESULT público (LPWStr \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="97088-147">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="97088-148">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="97088-148">put_ReasonPhrase</span></span> 

<span data-ttu-id="97088-149">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="97088-149">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="97088-150">[put_ReasonPhrase](#put_reasonphrase)pública HRESULT (LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="97088-150">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>


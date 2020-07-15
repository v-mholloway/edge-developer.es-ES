---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 95c0a881a8a201d21ca9cb2662c282b36efa2ed3
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878109"
---
# <span data-ttu-id="98318-104">0.8.355: IWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="98318-104">0.8.355 - interface IWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="98318-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="98318-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="98318-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="98318-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="98318-107">Una respuesta HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="98318-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="98318-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="98318-108">Summary</span></span>

 <span data-ttu-id="98318-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="98318-109">Members</span></span>                        | <span data-ttu-id="98318-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="98318-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="98318-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="98318-111">get_Content</span></span>](#get_content) | <span data-ttu-id="98318-112">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="98318-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="98318-113">put_Content</span><span class="sxs-lookup"><span data-stu-id="98318-113">put_Content</span></span>](#put_content) | <span data-ttu-id="98318-114">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="98318-114">Set the Content property.</span></span>
[<span data-ttu-id="98318-115">get_Headers</span><span class="sxs-lookup"><span data-stu-id="98318-115">get_Headers</span></span>](#get_headers) | <span data-ttu-id="98318-116">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="98318-116">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="98318-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="98318-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="98318-118">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="98318-118">The HTTP response status code.</span></span>
[<span data-ttu-id="98318-119">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="98318-119">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="98318-120">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="98318-120">Set the StatusCode property.</span></span>
[<span data-ttu-id="98318-121">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="98318-121">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="98318-122">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="98318-122">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="98318-123">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="98318-123">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="98318-124">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="98318-124">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="98318-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="98318-125">Members</span></span>

#### <span data-ttu-id="98318-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="98318-126">get_Content</span></span> 

<span data-ttu-id="98318-127">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="98318-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="98318-128">[get_Content](#get_content)(HRESULT) público (contenido de IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="98318-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="98318-129">La secuencia debe tener todos los datos de contenido disponibles por el momento en que se completa este aplazamiento de eventos de WebResourceRequested de respuesta.</span><span class="sxs-lookup"><span data-stu-id="98318-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="98318-130">La secuencia debe ser ágil o crearse a partir de un subproceso en segundo plano para evitar el impacto en el rendimiento del subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="98318-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="98318-131">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="98318-131">Null means no content data.</span></span> <span data-ttu-id="98318-132">Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)</span><span class="sxs-lookup"><span data-stu-id="98318-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="98318-133">put_Content</span><span class="sxs-lookup"><span data-stu-id="98318-133">put_Content</span></span> 

<span data-ttu-id="98318-134">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="98318-134">Set the Content property.</span></span>

> <span data-ttu-id="98318-135">[put_Content](#put_content)(HRESULT) público (contenido de IStream \*)</span><span class="sxs-lookup"><span data-stu-id="98318-135">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="98318-136">get_Headers</span><span class="sxs-lookup"><span data-stu-id="98318-136">get_Headers</span></span> 

<span data-ttu-id="98318-137">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="98318-137">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="98318-138">[get_Headers](#get_headers)de HRESULT público (encabezados[IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="98318-138">public HRESULT [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="98318-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="98318-139">get_StatusCode</span></span> 

<span data-ttu-id="98318-140">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="98318-140">The HTTP response status code.</span></span>

> <span data-ttu-id="98318-141">[get_StatusCode](#get_statuscode)de HRESULT público (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="98318-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="98318-142">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="98318-142">put_StatusCode</span></span> 

<span data-ttu-id="98318-143">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="98318-143">Set the StatusCode property.</span></span>

> <span data-ttu-id="98318-144">[put_StatusCode](#put_statuscode)de HRESULT público (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="98318-144">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="98318-145">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="98318-145">get_ReasonPhrase</span></span> 

<span data-ttu-id="98318-146">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="98318-146">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="98318-147">[get_ReasonPhrase](#get_reasonphrase)de HRESULT público (LPWStr \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="98318-147">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="98318-148">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="98318-148">put_ReasonPhrase</span></span> 

<span data-ttu-id="98318-149">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="98318-149">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="98318-150">[put_ReasonPhrase](#put_reasonphrase)pública HRESULT (LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="98318-150">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>


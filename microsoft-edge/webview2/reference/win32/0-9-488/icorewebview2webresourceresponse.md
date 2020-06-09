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
ms.openlocfilehash: 5b80691f0e42be4cdea7c99b165bfe9cebf632dd
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697934"
---
# <span data-ttu-id="a563e-104">interfaz ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="a563e-104">interface ICoreWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="a563e-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="a563e-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="a563e-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="a563e-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="a563e-107">Una respuesta HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="a563e-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="a563e-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="a563e-108">Summary</span></span>

 <span data-ttu-id="a563e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a563e-109">Members</span></span>                        | <span data-ttu-id="a563e-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a563e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a563e-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="a563e-111">get_Content</span></span>](#get_content) | <span data-ttu-id="a563e-112">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="a563e-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="a563e-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="a563e-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="a563e-114">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="a563e-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="a563e-115">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="a563e-115">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="a563e-116">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="a563e-116">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="a563e-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="a563e-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="a563e-118">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="a563e-118">The HTTP response status code.</span></span>
[<span data-ttu-id="a563e-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="a563e-119">put_Content</span></span>](#put_content) | <span data-ttu-id="a563e-120">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="a563e-120">Set the Content property.</span></span>
[<span data-ttu-id="a563e-121">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="a563e-121">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="a563e-122">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="a563e-122">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="a563e-123">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="a563e-123">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="a563e-124">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="a563e-124">Set the StatusCode property.</span></span>

## <span data-ttu-id="a563e-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="a563e-125">Members</span></span>

#### <span data-ttu-id="a563e-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="a563e-126">get_Content</span></span> 

<span data-ttu-id="a563e-127">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="a563e-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="a563e-128">[get_Content](#get_content)(HRESULT) público (contenido de IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="a563e-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="a563e-129">La secuencia debe tener todos los datos de contenido disponibles por el momento en que se completa este aplazamiento de eventos de WebResourceRequested de respuesta.</span><span class="sxs-lookup"><span data-stu-id="a563e-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="a563e-130">La secuencia debe ser ágil o crearse a partir de un subproceso en segundo plano para evitar el impacto en el rendimiento del subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a563e-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="a563e-131">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="a563e-131">Null means no content data.</span></span> <span data-ttu-id="a563e-132">Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)</span><span class="sxs-lookup"><span data-stu-id="a563e-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="a563e-133">get_Headers</span><span class="sxs-lookup"><span data-stu-id="a563e-133">get_Headers</span></span> 

<span data-ttu-id="a563e-134">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="a563e-134">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="a563e-135">[get_Headers](#get_headers)de HRESULT público (encabezados[ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="a563e-135">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="a563e-136">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="a563e-136">get_ReasonPhrase</span></span> 

<span data-ttu-id="a563e-137">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="a563e-137">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="a563e-138">[get_ReasonPhrase](#get_reasonphrase)de HRESULT público (LPWStr \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="a563e-138">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="a563e-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="a563e-139">get_StatusCode</span></span> 

<span data-ttu-id="a563e-140">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="a563e-140">The HTTP response status code.</span></span>

> <span data-ttu-id="a563e-141">[get_StatusCode](#get_statuscode)de HRESULT público (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="a563e-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="a563e-142">put_Content</span><span class="sxs-lookup"><span data-stu-id="a563e-142">put_Content</span></span> 

<span data-ttu-id="a563e-143">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="a563e-143">Set the Content property.</span></span>

> <span data-ttu-id="a563e-144">[put_Content](#put_content)(HRESULT) público (contenido de IStream \*)</span><span class="sxs-lookup"><span data-stu-id="a563e-144">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="a563e-145">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="a563e-145">put_ReasonPhrase</span></span> 

<span data-ttu-id="a563e-146">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="a563e-146">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="a563e-147">[put_ReasonPhrase](#put_reasonphrase)pública HRESULT (LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="a563e-147">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="a563e-148">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="a563e-148">put_StatusCode</span></span> 

<span data-ttu-id="a563e-149">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="a563e-149">Set the StatusCode property.</span></span>

> <span data-ttu-id="a563e-150">[put_StatusCode](#put_statuscode)de HRESULT público (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="a563e-150">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>


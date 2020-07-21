---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 82c94869a84165de4c3b8d09937d6ea5d1f79256
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885691"
---
# <span data-ttu-id="b0273-104">0.8.355: IWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="b0273-104">0.8.355 - interface IWebView2WebResourceResponse</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="b0273-105">Una respuesta HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="b0273-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="b0273-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="b0273-106">Summary</span></span>

 <span data-ttu-id="b0273-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b0273-107">Members</span></span>                        | <span data-ttu-id="b0273-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b0273-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b0273-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="b0273-109">get_Content</span></span>](#get_content) | <span data-ttu-id="b0273-110">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="b0273-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="b0273-111">put_Content</span><span class="sxs-lookup"><span data-stu-id="b0273-111">put_Content</span></span>](#put_content) | <span data-ttu-id="b0273-112">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="b0273-112">Set the Content property.</span></span>
[<span data-ttu-id="b0273-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="b0273-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="b0273-114">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="b0273-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="b0273-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="b0273-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="b0273-116">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="b0273-116">The HTTP response status code.</span></span>
[<span data-ttu-id="b0273-117">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="b0273-117">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="b0273-118">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="b0273-118">Set the StatusCode property.</span></span>
[<span data-ttu-id="b0273-119">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="b0273-119">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="b0273-120">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="b0273-120">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="b0273-121">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="b0273-121">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="b0273-122">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="b0273-122">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="b0273-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="b0273-123">Members</span></span>

#### <span data-ttu-id="b0273-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="b0273-124">get_Content</span></span> 

<span data-ttu-id="b0273-125">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="b0273-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="b0273-126">[get_Content](#get_content)(HRESULT) público (contenido de IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="b0273-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="b0273-127">La secuencia debe tener todos los datos de contenido disponibles por el momento en que se completa este aplazamiento de eventos de WebResourceRequested de respuesta.</span><span class="sxs-lookup"><span data-stu-id="b0273-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="b0273-128">La secuencia debe ser ágil o crearse a partir de un subproceso en segundo plano para evitar el impacto en el rendimiento del subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="b0273-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="b0273-129">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="b0273-129">Null means no content data.</span></span> <span data-ttu-id="b0273-130">Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)</span><span class="sxs-lookup"><span data-stu-id="b0273-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="b0273-131">put_Content</span><span class="sxs-lookup"><span data-stu-id="b0273-131">put_Content</span></span> 

<span data-ttu-id="b0273-132">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="b0273-132">Set the Content property.</span></span>

> <span data-ttu-id="b0273-133">[put_Content](#put_content)(HRESULT) público (contenido de IStream \*)</span><span class="sxs-lookup"><span data-stu-id="b0273-133">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="b0273-134">get_Headers</span><span class="sxs-lookup"><span data-stu-id="b0273-134">get_Headers</span></span> 

<span data-ttu-id="b0273-135">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="b0273-135">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="b0273-136">[get_Headers](#get_headers)de HRESULT público (encabezados[IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="b0273-136">public HRESULT [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="b0273-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="b0273-137">get_StatusCode</span></span> 

<span data-ttu-id="b0273-138">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="b0273-138">The HTTP response status code.</span></span>

> <span data-ttu-id="b0273-139">[get_StatusCode](#get_statuscode)de HRESULT público (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="b0273-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="b0273-140">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="b0273-140">put_StatusCode</span></span> 

<span data-ttu-id="b0273-141">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="b0273-141">Set the StatusCode property.</span></span>

> <span data-ttu-id="b0273-142">[put_StatusCode](#put_statuscode)de HRESULT público (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="b0273-142">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="b0273-143">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="b0273-143">get_ReasonPhrase</span></span> 

<span data-ttu-id="b0273-144">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="b0273-144">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="b0273-145">[get_ReasonPhrase](#get_reasonphrase)de HRESULT público (LPWStr \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="b0273-145">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="b0273-146">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="b0273-146">put_ReasonPhrase</span></span> 

<span data-ttu-id="b0273-147">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="b0273-147">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="b0273-148">[put_ReasonPhrase](#put_reasonphrase)pública HRESULT (LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="b0273-148">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>


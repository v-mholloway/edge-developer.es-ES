---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 61f731a948dee970731ba3dbe83426cbb40eb831
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884004"
---
# <span data-ttu-id="67d67-104">0.9.430: ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="67d67-104">0.9.430 - interface ICoreWebView2WebResourceResponse</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="67d67-105">Una respuesta HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="67d67-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="67d67-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="67d67-106">Summary</span></span>

 <span data-ttu-id="67d67-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="67d67-107">Members</span></span>                        | <span data-ttu-id="67d67-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="67d67-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="67d67-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="67d67-109">get_Content</span></span>](#get_content) | <span data-ttu-id="67d67-110">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="67d67-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="67d67-111">put_Content</span><span class="sxs-lookup"><span data-stu-id="67d67-111">put_Content</span></span>](#put_content) | <span data-ttu-id="67d67-112">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="67d67-112">Set the Content property.</span></span>
[<span data-ttu-id="67d67-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="67d67-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="67d67-114">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="67d67-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="67d67-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="67d67-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="67d67-116">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="67d67-116">The HTTP response status code.</span></span>
[<span data-ttu-id="67d67-117">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="67d67-117">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="67d67-118">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="67d67-118">Set the StatusCode property.</span></span>
[<span data-ttu-id="67d67-119">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="67d67-119">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="67d67-120">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="67d67-120">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="67d67-121">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="67d67-121">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="67d67-122">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="67d67-122">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="67d67-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="67d67-123">Members</span></span>

#### <span data-ttu-id="67d67-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="67d67-124">get_Content</span></span> 

<span data-ttu-id="67d67-125">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="67d67-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="67d67-126">[get_Content](#get_content)(HRESULT) público (contenido de IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="67d67-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="67d67-127">La secuencia debe tener todos los datos de contenido disponibles por el momento en que se completa este aplazamiento de eventos de WebResourceRequested de respuesta.</span><span class="sxs-lookup"><span data-stu-id="67d67-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="67d67-128">La secuencia debe ser ágil o crearse a partir de un subproceso en segundo plano para evitar el impacto en el rendimiento del subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="67d67-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="67d67-129">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="67d67-129">Null means no content data.</span></span> <span data-ttu-id="67d67-130">Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)</span><span class="sxs-lookup"><span data-stu-id="67d67-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="67d67-131">put_Content</span><span class="sxs-lookup"><span data-stu-id="67d67-131">put_Content</span></span> 

<span data-ttu-id="67d67-132">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="67d67-132">Set the Content property.</span></span>

> <span data-ttu-id="67d67-133">[put_Content](#put_content)(HRESULT) público (contenido de IStream \*)</span><span class="sxs-lookup"><span data-stu-id="67d67-133">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="67d67-134">get_Headers</span><span class="sxs-lookup"><span data-stu-id="67d67-134">get_Headers</span></span> 

<span data-ttu-id="67d67-135">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="67d67-135">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="67d67-136">[get_Headers](#get_headers)de HRESULT público (encabezados[ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="67d67-136">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="67d67-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="67d67-137">get_StatusCode</span></span> 

<span data-ttu-id="67d67-138">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="67d67-138">The HTTP response status code.</span></span>

> <span data-ttu-id="67d67-139">[get_StatusCode](#get_statuscode)de HRESULT público (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="67d67-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="67d67-140">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="67d67-140">put_StatusCode</span></span> 

<span data-ttu-id="67d67-141">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="67d67-141">Set the StatusCode property.</span></span>

> <span data-ttu-id="67d67-142">[put_StatusCode](#put_statuscode)de HRESULT público (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="67d67-142">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="67d67-143">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="67d67-143">get_ReasonPhrase</span></span> 

<span data-ttu-id="67d67-144">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="67d67-144">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="67d67-145">[get_ReasonPhrase](#get_reasonphrase)de HRESULT público (LPWStr \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="67d67-145">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="67d67-146">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="67d67-146">put_ReasonPhrase</span></span> 

<span data-ttu-id="67d67-147">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="67d67-147">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="67d67-148">[put_ReasonPhrase](#put_reasonphrase)pública HRESULT (LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="67d67-148">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>


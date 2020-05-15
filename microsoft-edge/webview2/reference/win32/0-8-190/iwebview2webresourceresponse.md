---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: ad3f4e5e95b0309628644f17e5d647ab6d4af658
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655128"
---
# <span data-ttu-id="f1433-104">interfaz IWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="f1433-104">interface IWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="f1433-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="f1433-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="f1433-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="f1433-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="f1433-107">Una respuesta HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="f1433-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="f1433-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="f1433-108">Summary</span></span>

 <span data-ttu-id="f1433-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="f1433-109">Members</span></span>                        | <span data-ttu-id="f1433-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="f1433-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f1433-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="f1433-111">get_Content</span></span>](#get_content) | <span data-ttu-id="f1433-112">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="f1433-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="f1433-113">put_Content</span><span class="sxs-lookup"><span data-stu-id="f1433-113">put_Content</span></span>](#put_content) | <span data-ttu-id="f1433-114">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="f1433-114">Set the Content property.</span></span>
[<span data-ttu-id="f1433-115">get_Headers</span><span class="sxs-lookup"><span data-stu-id="f1433-115">get_Headers</span></span>](#get_headers) | <span data-ttu-id="f1433-116">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="f1433-116">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="f1433-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="f1433-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="f1433-118">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f1433-118">The HTTP response status code.</span></span>
[<span data-ttu-id="f1433-119">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="f1433-119">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="f1433-120">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="f1433-120">Set the StatusCode property.</span></span>
[<span data-ttu-id="f1433-121">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="f1433-121">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="f1433-122">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f1433-122">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="f1433-123">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="f1433-123">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="f1433-124">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="f1433-124">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="f1433-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="f1433-125">Members</span></span>

#### <span data-ttu-id="f1433-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="f1433-126">get_Content</span></span> 

<span data-ttu-id="f1433-127">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="f1433-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="f1433-128">[get_Content](#get_content)(HRESULT) público (contenido de IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="f1433-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="f1433-129">La secuencia debe tener todos los datos de contenido disponibles por el momento en que se completa este aplazamiento de eventos de WebResourceRequested de respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1433-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="f1433-130">La secuencia debe ser ágil o crearse a partir de un subproceso en segundo plano para evitar el impacto en el rendimiento del subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="f1433-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="f1433-131">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="f1433-131">Null means no content data.</span></span> <span data-ttu-id="f1433-132">Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)</span><span class="sxs-lookup"><span data-stu-id="f1433-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="f1433-133">put_Content</span><span class="sxs-lookup"><span data-stu-id="f1433-133">put_Content</span></span> 

<span data-ttu-id="f1433-134">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="f1433-134">Set the Content property.</span></span>

> <span data-ttu-id="f1433-135">[put_Content](#put_content)(HRESULT) público (contenido de IStream \*)</span><span class="sxs-lookup"><span data-stu-id="f1433-135">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="f1433-136">get_Headers</span><span class="sxs-lookup"><span data-stu-id="f1433-136">get_Headers</span></span> 

<span data-ttu-id="f1433-137">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="f1433-137">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="f1433-138">[get_Headers](#get_headers)de HRESULT público (encabezados[IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="f1433-138">public HRESULT [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="f1433-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="f1433-139">get_StatusCode</span></span> 

<span data-ttu-id="f1433-140">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f1433-140">The HTTP response status code.</span></span>

> <span data-ttu-id="f1433-141">[get_StatusCode](#get_statuscode)de HRESULT público (int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="f1433-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="f1433-142">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="f1433-142">put_StatusCode</span></span> 

<span data-ttu-id="f1433-143">Establezca la propiedad StatusCode.</span><span class="sxs-lookup"><span data-stu-id="f1433-143">Set the StatusCode property.</span></span>

> <span data-ttu-id="f1433-144">[put_StatusCode](#put_statuscode)de HRESULT público (int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="f1433-144">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="f1433-145">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="f1433-145">get_ReasonPhrase</span></span> 

<span data-ttu-id="f1433-146">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="f1433-146">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="f1433-147">[get_ReasonPhrase](#get_reasonphrase)de HRESULT público (LPWStr \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="f1433-147">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="f1433-148">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="f1433-148">put_ReasonPhrase</span></span> 

<span data-ttu-id="f1433-149">Establezca la propiedad ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="f1433-149">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="f1433-150">[put_ReasonPhrase](#put_reasonphrase)pública HRESULT (LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="f1433-150">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>


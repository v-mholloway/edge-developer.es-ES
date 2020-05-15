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
ms.openlocfilehash: 4b76cf998f8e2fd8982f7e51f1d9167e3862ec02
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655125"
---
# <span data-ttu-id="e943a-104">interfaz ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="e943a-104">interface ICoreWebView2WebResourceRequest</span></span> 

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="e943a-105">Una solicitud HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="e943a-105">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="e943a-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e943a-106">Summary</span></span>

 <span data-ttu-id="e943a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e943a-107">Members</span></span>                        | <span data-ttu-id="e943a-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e943a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e943a-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="e943a-109">get_Content</span></span>](#get_content) | <span data-ttu-id="e943a-110">El cuerpo del mensaje de la solicitud HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="e943a-110">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="e943a-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="e943a-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="e943a-112">Los encabezados de solicitud HTTP mutable.</span><span class="sxs-lookup"><span data-stu-id="e943a-112">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="e943a-113">get_Method</span><span class="sxs-lookup"><span data-stu-id="e943a-113">get_Method</span></span>](#get_method) | <span data-ttu-id="e943a-114">El método de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="e943a-114">The HTTP request method.</span></span>
[<span data-ttu-id="e943a-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="e943a-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="e943a-116">Identificador URI de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e943a-116">The request URI.</span></span>
[<span data-ttu-id="e943a-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="e943a-117">put_Content</span></span>](#put_content) | <span data-ttu-id="e943a-118">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="e943a-118">Set the Content property.</span></span>
[<span data-ttu-id="e943a-119">put_Method</span><span class="sxs-lookup"><span data-stu-id="e943a-119">put_Method</span></span>](#put_method) | <span data-ttu-id="e943a-120">Establezca la propiedad Method.</span><span class="sxs-lookup"><span data-stu-id="e943a-120">Set the Method property.</span></span>
[<span data-ttu-id="e943a-121">put_Uri</span><span class="sxs-lookup"><span data-stu-id="e943a-121">put_Uri</span></span>](#put_uri) | <span data-ttu-id="e943a-122">Establezca la propiedad URI.</span><span class="sxs-lookup"><span data-stu-id="e943a-122">Set the Uri property.</span></span>

## <span data-ttu-id="e943a-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="e943a-123">Members</span></span>

#### <span data-ttu-id="e943a-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="e943a-124">get_Content</span></span> 

<span data-ttu-id="e943a-125">El cuerpo del mensaje de la solicitud HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="e943a-125">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="e943a-126">[get_Content](#get_content)(HRESULT) público (contenido de IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="e943a-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="e943a-127">Los datos de publicación estarán aquí.</span><span class="sxs-lookup"><span data-stu-id="e943a-127">POST data would be here.</span></span> <span data-ttu-id="e943a-128">Si se establece una secuencia, lo que invalidará el cuerpo del mensaje, la secuencia debe tener todos los datos de contenido disponibles en el momento en que se complete el aplazamiento de eventos de WebResourceRequested de esta respuesta.</span><span class="sxs-lookup"><span data-stu-id="e943a-128">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="e943a-129">La secuencia debe ser ágil o crearse a partir de un STA de fondo para evitar el impacto en el rendimiento en el subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e943a-129">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="e943a-130">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="e943a-130">Null means no content data.</span></span> <span data-ttu-id="e943a-131">Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)</span><span class="sxs-lookup"><span data-stu-id="e943a-131">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="e943a-132">get_Headers</span><span class="sxs-lookup"><span data-stu-id="e943a-132">get_Headers</span></span> 

<span data-ttu-id="e943a-133">Los encabezados de solicitud HTTP mutable.</span><span class="sxs-lookup"><span data-stu-id="e943a-133">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="e943a-134">[get_Headers](#get_headers)de HRESULT público (encabezados[ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="e943a-134">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="e943a-135">get_Method</span><span class="sxs-lookup"><span data-stu-id="e943a-135">get_Method</span></span> 

<span data-ttu-id="e943a-136">El método de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="e943a-136">The HTTP request method.</span></span>

> <span data-ttu-id="e943a-137">[get_Method](#get_method)de HRESULT público (método LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="e943a-137">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="e943a-138">get_Uri</span><span class="sxs-lookup"><span data-stu-id="e943a-138">get_Uri</span></span> 

<span data-ttu-id="e943a-139">Identificador URI de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e943a-139">The request URI.</span></span>

> <span data-ttu-id="e943a-140">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="e943a-140">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="e943a-141">put_Content</span><span class="sxs-lookup"><span data-stu-id="e943a-141">put_Content</span></span> 

<span data-ttu-id="e943a-142">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="e943a-142">Set the Content property.</span></span>

> <span data-ttu-id="e943a-143">[put_Content](#put_content)(HRESULT) público (contenido de IStream \*)</span><span class="sxs-lookup"><span data-stu-id="e943a-143">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="e943a-144">put_Method</span><span class="sxs-lookup"><span data-stu-id="e943a-144">put_Method</span></span> 

<span data-ttu-id="e943a-145">Establezca la propiedad Method.</span><span class="sxs-lookup"><span data-stu-id="e943a-145">Set the Method property.</span></span>

> <span data-ttu-id="e943a-146">[put_Method](#put_method)de HRESULT público (método LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="e943a-146">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="e943a-147">put_Uri</span><span class="sxs-lookup"><span data-stu-id="e943a-147">put_Uri</span></span> 

<span data-ttu-id="e943a-148">Establezca la propiedad URI.</span><span class="sxs-lookup"><span data-stu-id="e943a-148">Set the Uri property.</span></span>

> <span data-ttu-id="e943a-149">[put_Uri](#put_uri)de HRESULT público (URI de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="e943a-149">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>


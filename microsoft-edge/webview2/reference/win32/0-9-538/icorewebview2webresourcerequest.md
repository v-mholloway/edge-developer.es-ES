---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: c715a195a52d95e91095e006c71e50de46dc05e4
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699397"
---
# <span data-ttu-id="8af02-104">interfaz ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="8af02-104">interface ICoreWebView2WebResourceRequest</span></span> 

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="8af02-105">Una solicitud HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="8af02-105">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="8af02-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="8af02-106">Summary</span></span>

 <span data-ttu-id="8af02-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8af02-107">Members</span></span>                        | <span data-ttu-id="8af02-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="8af02-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8af02-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="8af02-109">get_Content</span></span>](#get_content) | <span data-ttu-id="8af02-110">El cuerpo del mensaje de la solicitud HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="8af02-110">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="8af02-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="8af02-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="8af02-112">Los encabezados de solicitud HTTP mutable.</span><span class="sxs-lookup"><span data-stu-id="8af02-112">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="8af02-113">get_Method</span><span class="sxs-lookup"><span data-stu-id="8af02-113">get_Method</span></span>](#get_method) | <span data-ttu-id="8af02-114">El método de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="8af02-114">The HTTP request method.</span></span>
[<span data-ttu-id="8af02-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="8af02-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="8af02-116">Identificador URI de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8af02-116">The request URI.</span></span>
[<span data-ttu-id="8af02-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="8af02-117">put_Content</span></span>](#put_content) | <span data-ttu-id="8af02-118">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="8af02-118">Set the Content property.</span></span>
[<span data-ttu-id="8af02-119">put_Method</span><span class="sxs-lookup"><span data-stu-id="8af02-119">put_Method</span></span>](#put_method) | <span data-ttu-id="8af02-120">Establezca la propiedad Method.</span><span class="sxs-lookup"><span data-stu-id="8af02-120">Set the Method property.</span></span>
[<span data-ttu-id="8af02-121">put_Uri</span><span class="sxs-lookup"><span data-stu-id="8af02-121">put_Uri</span></span>](#put_uri) | <span data-ttu-id="8af02-122">Establezca la propiedad URI.</span><span class="sxs-lookup"><span data-stu-id="8af02-122">Set the Uri property.</span></span>

## <span data-ttu-id="8af02-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="8af02-123">Members</span></span>

#### <span data-ttu-id="8af02-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="8af02-124">get_Content</span></span> 

<span data-ttu-id="8af02-125">El cuerpo del mensaje de la solicitud HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="8af02-125">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="8af02-126">[get_Content](#get_content)(HRESULT) público (contenido de IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="8af02-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="8af02-127">Los datos de publicación estarán aquí.</span><span class="sxs-lookup"><span data-stu-id="8af02-127">POST data would be here.</span></span> <span data-ttu-id="8af02-128">Si se establece una secuencia, lo que invalidará el cuerpo del mensaje, la secuencia debe tener todos los datos de contenido disponibles en el momento en que se complete el aplazamiento de eventos de WebResourceRequested de esta respuesta.</span><span class="sxs-lookup"><span data-stu-id="8af02-128">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="8af02-129">La secuencia debe ser ágil o crearse a partir de un STA de fondo para evitar el impacto en el rendimiento en el subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="8af02-129">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="8af02-130">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="8af02-130">Null means no content data.</span></span> <span data-ttu-id="8af02-131">Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)</span><span class="sxs-lookup"><span data-stu-id="8af02-131">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="8af02-132">get_Headers</span><span class="sxs-lookup"><span data-stu-id="8af02-132">get_Headers</span></span> 

<span data-ttu-id="8af02-133">Los encabezados de solicitud HTTP mutable.</span><span class="sxs-lookup"><span data-stu-id="8af02-133">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="8af02-134">[get_Headers](#get_headers)de HRESULT público (encabezados[ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="8af02-134">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="8af02-135">get_Method</span><span class="sxs-lookup"><span data-stu-id="8af02-135">get_Method</span></span> 

<span data-ttu-id="8af02-136">El método de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="8af02-136">The HTTP request method.</span></span>

> <span data-ttu-id="8af02-137">[get_Method](#get_method)de HRESULT público (método LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="8af02-137">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="8af02-138">get_Uri</span><span class="sxs-lookup"><span data-stu-id="8af02-138">get_Uri</span></span> 

<span data-ttu-id="8af02-139">Identificador URI de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8af02-139">The request URI.</span></span>

> <span data-ttu-id="8af02-140">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="8af02-140">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="8af02-141">put_Content</span><span class="sxs-lookup"><span data-stu-id="8af02-141">put_Content</span></span> 

<span data-ttu-id="8af02-142">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="8af02-142">Set the Content property.</span></span>

> <span data-ttu-id="8af02-143">[put_Content](#put_content)(HRESULT) público (contenido de IStream \*)</span><span class="sxs-lookup"><span data-stu-id="8af02-143">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="8af02-144">put_Method</span><span class="sxs-lookup"><span data-stu-id="8af02-144">put_Method</span></span> 

<span data-ttu-id="8af02-145">Establezca la propiedad Method.</span><span class="sxs-lookup"><span data-stu-id="8af02-145">Set the Method property.</span></span>

> <span data-ttu-id="8af02-146">[put_Method](#put_method)de HRESULT público (método LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="8af02-146">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="8af02-147">put_Uri</span><span class="sxs-lookup"><span data-stu-id="8af02-147">put_Uri</span></span> 

<span data-ttu-id="8af02-148">Establezca la propiedad URI.</span><span class="sxs-lookup"><span data-stu-id="8af02-148">Set the Uri property.</span></span>

> <span data-ttu-id="8af02-149">[put_Uri](#put_uri)de HRESULT público (URI de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="8af02-149">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>


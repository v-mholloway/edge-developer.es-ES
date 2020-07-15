---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: a2ac747a9981b3d44e8dbddd390bbb9b72690105
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880139"
---
# <span data-ttu-id="cc0c0-104">0.9.430: ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="cc0c0-104">0.9.430 - interface ICoreWebView2WebResourceRequest</span></span> 

> [!NOTE]
> <span data-ttu-id="cc0c0-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="cc0c0-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="cc0c0-107">Una solicitud HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="cc0c0-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="cc0c0-108">Summary</span></span>

 <span data-ttu-id="cc0c0-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="cc0c0-109">Members</span></span>                        | <span data-ttu-id="cc0c0-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="cc0c0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cc0c0-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="cc0c0-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="cc0c0-112">Identificador URI de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-112">The request URI.</span></span>
[<span data-ttu-id="cc0c0-113">put_Uri</span><span class="sxs-lookup"><span data-stu-id="cc0c0-113">put_Uri</span></span>](#put_uri) | <span data-ttu-id="cc0c0-114">Establezca la propiedad URI.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-114">Set the Uri property.</span></span>
[<span data-ttu-id="cc0c0-115">get_Method</span><span class="sxs-lookup"><span data-stu-id="cc0c0-115">get_Method</span></span>](#get_method) | <span data-ttu-id="cc0c0-116">El método de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-116">The HTTP request method.</span></span>
[<span data-ttu-id="cc0c0-117">put_Method</span><span class="sxs-lookup"><span data-stu-id="cc0c0-117">put_Method</span></span>](#put_method) | <span data-ttu-id="cc0c0-118">Establezca la propiedad Method.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-118">Set the Method property.</span></span>
[<span data-ttu-id="cc0c0-119">get_Content</span><span class="sxs-lookup"><span data-stu-id="cc0c0-119">get_Content</span></span>](#get_content) | <span data-ttu-id="cc0c0-120">El cuerpo del mensaje de la solicitud HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-120">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="cc0c0-121">put_Content</span><span class="sxs-lookup"><span data-stu-id="cc0c0-121">put_Content</span></span>](#put_content) | <span data-ttu-id="cc0c0-122">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-122">Set the Content property.</span></span>
[<span data-ttu-id="cc0c0-123">get_Headers</span><span class="sxs-lookup"><span data-stu-id="cc0c0-123">get_Headers</span></span>](#get_headers) | <span data-ttu-id="cc0c0-124">Los encabezados de solicitud HTTP mutable.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-124">The mutable HTTP request headers.</span></span>

## <span data-ttu-id="cc0c0-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="cc0c0-125">Members</span></span>

#### <span data-ttu-id="cc0c0-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="cc0c0-126">get_Uri</span></span> 

<span data-ttu-id="cc0c0-127">Identificador URI de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-127">The request URI.</span></span>

> <span data-ttu-id="cc0c0-128">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="cc0c0-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="cc0c0-129">put_Uri</span><span class="sxs-lookup"><span data-stu-id="cc0c0-129">put_Uri</span></span> 

<span data-ttu-id="cc0c0-130">Establezca la propiedad URI.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-130">Set the Uri property.</span></span>

> <span data-ttu-id="cc0c0-131">[put_Uri](#put_uri)de HRESULT público (URI de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="cc0c0-131">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

#### <span data-ttu-id="cc0c0-132">get_Method</span><span class="sxs-lookup"><span data-stu-id="cc0c0-132">get_Method</span></span> 

<span data-ttu-id="cc0c0-133">El método de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-133">The HTTP request method.</span></span>

> <span data-ttu-id="cc0c0-134">[get_Method](#get_method)de HRESULT público (método LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="cc0c0-134">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="cc0c0-135">put_Method</span><span class="sxs-lookup"><span data-stu-id="cc0c0-135">put_Method</span></span> 

<span data-ttu-id="cc0c0-136">Establezca la propiedad Method.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-136">Set the Method property.</span></span>

> <span data-ttu-id="cc0c0-137">[put_Method](#put_method)de HRESULT público (método LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="cc0c0-137">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="cc0c0-138">get_Content</span><span class="sxs-lookup"><span data-stu-id="cc0c0-138">get_Content</span></span> 

<span data-ttu-id="cc0c0-139">El cuerpo del mensaje de la solicitud HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-139">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="cc0c0-140">[get_Content](#get_content)(HRESULT) público (contenido de IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="cc0c0-140">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="cc0c0-141">Los datos de publicación estarán aquí.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-141">POST data would be here.</span></span> <span data-ttu-id="cc0c0-142">Si se establece una secuencia, lo que invalidará el cuerpo del mensaje, la secuencia debe tener todos los datos de contenido disponibles en el momento en que se complete el aplazamiento de eventos de WebResourceRequested de esta respuesta.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-142">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="cc0c0-143">La secuencia debe ser ágil o crearse a partir de un STA de fondo para evitar el impacto en el rendimiento en el subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-143">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="cc0c0-144">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-144">Null means no content data.</span></span> <span data-ttu-id="cc0c0-145">Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)</span><span class="sxs-lookup"><span data-stu-id="cc0c0-145">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="cc0c0-146">put_Content</span><span class="sxs-lookup"><span data-stu-id="cc0c0-146">put_Content</span></span> 

<span data-ttu-id="cc0c0-147">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-147">Set the Content property.</span></span>

> <span data-ttu-id="cc0c0-148">[put_Content](#put_content)(HRESULT) público (contenido de IStream \*)</span><span class="sxs-lookup"><span data-stu-id="cc0c0-148">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="cc0c0-149">get_Headers</span><span class="sxs-lookup"><span data-stu-id="cc0c0-149">get_Headers</span></span> 

<span data-ttu-id="cc0c0-150">Los encabezados de solicitud HTTP mutable.</span><span class="sxs-lookup"><span data-stu-id="cc0c0-150">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="cc0c0-151">[get_Headers](#get_headers)de HRESULT público (encabezados[ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="cc0c0-151">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* headers)</span></span>


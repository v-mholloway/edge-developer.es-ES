---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 3c9736c8b5a3cfb0de994285f3a1f90d62666fd0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878151"
---
# <span data-ttu-id="33a25-104">0.8.355: IWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="33a25-104">0.8.355 - interface IWebView2WebResourceRequest</span></span> 

> [!NOTE]
> <span data-ttu-id="33a25-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="33a25-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="33a25-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="33a25-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="33a25-107">Una solicitud HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="33a25-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="33a25-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="33a25-108">Summary</span></span>

 <span data-ttu-id="33a25-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="33a25-109">Members</span></span>                        | <span data-ttu-id="33a25-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="33a25-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="33a25-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="33a25-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="33a25-112">Identificador URI de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="33a25-112">The request URI.</span></span>
[<span data-ttu-id="33a25-113">put_Uri</span><span class="sxs-lookup"><span data-stu-id="33a25-113">put_Uri</span></span>](#put_uri) | <span data-ttu-id="33a25-114">Establezca la propiedad URI.</span><span class="sxs-lookup"><span data-stu-id="33a25-114">Set the Uri property.</span></span>
[<span data-ttu-id="33a25-115">get_Method</span><span class="sxs-lookup"><span data-stu-id="33a25-115">get_Method</span></span>](#get_method) | <span data-ttu-id="33a25-116">El método de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="33a25-116">The HTTP request method.</span></span>
[<span data-ttu-id="33a25-117">put_Method</span><span class="sxs-lookup"><span data-stu-id="33a25-117">put_Method</span></span>](#put_method) | <span data-ttu-id="33a25-118">Establezca la propiedad Method.</span><span class="sxs-lookup"><span data-stu-id="33a25-118">Set the Method property.</span></span>
[<span data-ttu-id="33a25-119">get_Content</span><span class="sxs-lookup"><span data-stu-id="33a25-119">get_Content</span></span>](#get_content) | <span data-ttu-id="33a25-120">El cuerpo del mensaje de la solicitud HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="33a25-120">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="33a25-121">put_Content</span><span class="sxs-lookup"><span data-stu-id="33a25-121">put_Content</span></span>](#put_content) | <span data-ttu-id="33a25-122">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="33a25-122">Set the Content property.</span></span>
[<span data-ttu-id="33a25-123">get_Headers</span><span class="sxs-lookup"><span data-stu-id="33a25-123">get_Headers</span></span>](#get_headers) | <span data-ttu-id="33a25-124">Los encabezados de solicitud HTTP mutable.</span><span class="sxs-lookup"><span data-stu-id="33a25-124">The mutable HTTP request headers.</span></span>

## <span data-ttu-id="33a25-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="33a25-125">Members</span></span>

#### <span data-ttu-id="33a25-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="33a25-126">get_Uri</span></span> 

<span data-ttu-id="33a25-127">Identificador URI de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="33a25-127">The request URI.</span></span>

> <span data-ttu-id="33a25-128">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="33a25-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="33a25-129">put_Uri</span><span class="sxs-lookup"><span data-stu-id="33a25-129">put_Uri</span></span> 

<span data-ttu-id="33a25-130">Establezca la propiedad URI.</span><span class="sxs-lookup"><span data-stu-id="33a25-130">Set the Uri property.</span></span>

> <span data-ttu-id="33a25-131">[put_Uri](#put_uri)de HRESULT público (URI de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="33a25-131">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

#### <span data-ttu-id="33a25-132">get_Method</span><span class="sxs-lookup"><span data-stu-id="33a25-132">get_Method</span></span> 

<span data-ttu-id="33a25-133">El método de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="33a25-133">The HTTP request method.</span></span>

> <span data-ttu-id="33a25-134">[get_Method](#get_method)de HRESULT público (método LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="33a25-134">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="33a25-135">put_Method</span><span class="sxs-lookup"><span data-stu-id="33a25-135">put_Method</span></span> 

<span data-ttu-id="33a25-136">Establezca la propiedad Method.</span><span class="sxs-lookup"><span data-stu-id="33a25-136">Set the Method property.</span></span>

> <span data-ttu-id="33a25-137">[put_Method](#put_method)de HRESULT público (método LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="33a25-137">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="33a25-138">get_Content</span><span class="sxs-lookup"><span data-stu-id="33a25-138">get_Content</span></span> 

<span data-ttu-id="33a25-139">El cuerpo del mensaje de la solicitud HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="33a25-139">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="33a25-140">[get_Content](#get_content)(HRESULT) público (contenido de IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="33a25-140">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="33a25-141">Los datos de publicación estarán aquí.</span><span class="sxs-lookup"><span data-stu-id="33a25-141">POST data would be here.</span></span> <span data-ttu-id="33a25-142">Si se establece una secuencia, lo que invalidará el cuerpo del mensaje, la secuencia debe tener todos los datos de contenido disponibles en el momento en que se complete el aplazamiento de eventos de WebResourceRequested de esta respuesta.</span><span class="sxs-lookup"><span data-stu-id="33a25-142">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="33a25-143">La secuencia debe ser ágil o crearse a partir de un STA de fondo para evitar el impacto en el rendimiento en el subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="33a25-143">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="33a25-144">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="33a25-144">Null means no content data.</span></span> <span data-ttu-id="33a25-145">Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)</span><span class="sxs-lookup"><span data-stu-id="33a25-145">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="33a25-146">put_Content</span><span class="sxs-lookup"><span data-stu-id="33a25-146">put_Content</span></span> 

<span data-ttu-id="33a25-147">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="33a25-147">Set the Content property.</span></span>

> <span data-ttu-id="33a25-148">[put_Content](#put_content)(HRESULT) público (contenido de IStream \*)</span><span class="sxs-lookup"><span data-stu-id="33a25-148">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="33a25-149">get_Headers</span><span class="sxs-lookup"><span data-stu-id="33a25-149">get_Headers</span></span> 

<span data-ttu-id="33a25-150">Los encabezados de solicitud HTTP mutable.</span><span class="sxs-lookup"><span data-stu-id="33a25-150">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="33a25-151">[get_Headers](#get_headers)de HRESULT público (encabezados[IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="33a25-151">public HRESULT [get_Headers](#get_headers)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* headers)</span></span>


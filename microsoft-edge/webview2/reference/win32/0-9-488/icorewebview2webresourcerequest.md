---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: cdea3b4d4643e6f14e546eb9edd27bf1534beadd
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877353"
---
# <span data-ttu-id="30aef-104">0.9.515: ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="30aef-104">0.9.515 - interface ICoreWebView2WebResourceRequest</span></span> 

> [!NOTE]
> <span data-ttu-id="30aef-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="30aef-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="30aef-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="30aef-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="30aef-107">Una solicitud HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="30aef-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="30aef-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="30aef-108">Summary</span></span>

 <span data-ttu-id="30aef-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="30aef-109">Members</span></span>                        | <span data-ttu-id="30aef-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="30aef-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="30aef-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="30aef-111">get_Content</span></span>](#get_content) | <span data-ttu-id="30aef-112">El cuerpo del mensaje de la solicitud HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="30aef-112">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="30aef-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="30aef-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="30aef-114">Los encabezados de solicitud HTTP mutable.</span><span class="sxs-lookup"><span data-stu-id="30aef-114">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="30aef-115">get_Method</span><span class="sxs-lookup"><span data-stu-id="30aef-115">get_Method</span></span>](#get_method) | <span data-ttu-id="30aef-116">El método de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="30aef-116">The HTTP request method.</span></span>
[<span data-ttu-id="30aef-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="30aef-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="30aef-118">Identificador URI de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="30aef-118">The request URI.</span></span>
[<span data-ttu-id="30aef-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="30aef-119">put_Content</span></span>](#put_content) | <span data-ttu-id="30aef-120">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="30aef-120">Set the Content property.</span></span>
[<span data-ttu-id="30aef-121">put_Method</span><span class="sxs-lookup"><span data-stu-id="30aef-121">put_Method</span></span>](#put_method) | <span data-ttu-id="30aef-122">Establezca la propiedad Method.</span><span class="sxs-lookup"><span data-stu-id="30aef-122">Set the Method property.</span></span>
[<span data-ttu-id="30aef-123">put_Uri</span><span class="sxs-lookup"><span data-stu-id="30aef-123">put_Uri</span></span>](#put_uri) | <span data-ttu-id="30aef-124">Establezca la propiedad URI.</span><span class="sxs-lookup"><span data-stu-id="30aef-124">Set the Uri property.</span></span>

## <span data-ttu-id="30aef-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="30aef-125">Members</span></span>

#### <span data-ttu-id="30aef-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="30aef-126">get_Content</span></span> 

<span data-ttu-id="30aef-127">El cuerpo del mensaje de la solicitud HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="30aef-127">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="30aef-128">[get_Content](#get_content)(HRESULT) público (contenido de IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="30aef-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="30aef-129">Los datos de publicación estarán aquí.</span><span class="sxs-lookup"><span data-stu-id="30aef-129">POST data would be here.</span></span> <span data-ttu-id="30aef-130">Si se establece una secuencia, lo que invalidará el cuerpo del mensaje, la secuencia debe tener todos los datos de contenido disponibles en el momento en que se complete el aplazamiento de eventos de WebResourceRequested de esta respuesta.</span><span class="sxs-lookup"><span data-stu-id="30aef-130">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="30aef-131">La secuencia debe ser ágil o crearse a partir de un STA de fondo para evitar el impacto en el rendimiento en el subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="30aef-131">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="30aef-132">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="30aef-132">Null means no content data.</span></span> <span data-ttu-id="30aef-133">Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)</span><span class="sxs-lookup"><span data-stu-id="30aef-133">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="30aef-134">get_Headers</span><span class="sxs-lookup"><span data-stu-id="30aef-134">get_Headers</span></span> 

<span data-ttu-id="30aef-135">Los encabezados de solicitud HTTP mutable.</span><span class="sxs-lookup"><span data-stu-id="30aef-135">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="30aef-136">[get_Headers](#get_headers)de HRESULT público (encabezados[ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="30aef-136">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="30aef-137">get_Method</span><span class="sxs-lookup"><span data-stu-id="30aef-137">get_Method</span></span> 

<span data-ttu-id="30aef-138">El método de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="30aef-138">The HTTP request method.</span></span>

> <span data-ttu-id="30aef-139">[get_Method](#get_method)de HRESULT público (método LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="30aef-139">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="30aef-140">get_Uri</span><span class="sxs-lookup"><span data-stu-id="30aef-140">get_Uri</span></span> 

<span data-ttu-id="30aef-141">Identificador URI de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="30aef-141">The request URI.</span></span>

> <span data-ttu-id="30aef-142">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="30aef-142">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="30aef-143">put_Content</span><span class="sxs-lookup"><span data-stu-id="30aef-143">put_Content</span></span> 

<span data-ttu-id="30aef-144">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="30aef-144">Set the Content property.</span></span>

> <span data-ttu-id="30aef-145">[put_Content](#put_content)(HRESULT) público (contenido de IStream \*)</span><span class="sxs-lookup"><span data-stu-id="30aef-145">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="30aef-146">put_Method</span><span class="sxs-lookup"><span data-stu-id="30aef-146">put_Method</span></span> 

<span data-ttu-id="30aef-147">Establezca la propiedad Method.</span><span class="sxs-lookup"><span data-stu-id="30aef-147">Set the Method property.</span></span>

> <span data-ttu-id="30aef-148">[put_Method](#put_method)de HRESULT público (método LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="30aef-148">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="30aef-149">put_Uri</span><span class="sxs-lookup"><span data-stu-id="30aef-149">put_Uri</span></span> 

<span data-ttu-id="30aef-150">Establezca la propiedad URI.</span><span class="sxs-lookup"><span data-stu-id="30aef-150">Set the Uri property.</span></span>

> <span data-ttu-id="30aef-151">[put_Uri](#put_uri)de HRESULT público (URI de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="30aef-151">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>


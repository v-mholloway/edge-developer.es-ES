---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: e9d84fbd459d56b82ab4b7d253526e517960c1db
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885726"
---
# <span data-ttu-id="1c120-104">0.8.355: IWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="1c120-104">0.8.355 - interface IWebView2WebResourceRequest</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="1c120-105">Una solicitud HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="1c120-105">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="1c120-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="1c120-106">Summary</span></span>

 <span data-ttu-id="1c120-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1c120-107">Members</span></span>                        | <span data-ttu-id="1c120-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="1c120-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1c120-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="1c120-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="1c120-110">Identificador URI de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1c120-110">The request URI.</span></span>
[<span data-ttu-id="1c120-111">put_Uri</span><span class="sxs-lookup"><span data-stu-id="1c120-111">put_Uri</span></span>](#put_uri) | <span data-ttu-id="1c120-112">Establezca la propiedad URI.</span><span class="sxs-lookup"><span data-stu-id="1c120-112">Set the Uri property.</span></span>
[<span data-ttu-id="1c120-113">get_Method</span><span class="sxs-lookup"><span data-stu-id="1c120-113">get_Method</span></span>](#get_method) | <span data-ttu-id="1c120-114">El método de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="1c120-114">The HTTP request method.</span></span>
[<span data-ttu-id="1c120-115">put_Method</span><span class="sxs-lookup"><span data-stu-id="1c120-115">put_Method</span></span>](#put_method) | <span data-ttu-id="1c120-116">Establezca la propiedad Method.</span><span class="sxs-lookup"><span data-stu-id="1c120-116">Set the Method property.</span></span>
[<span data-ttu-id="1c120-117">get_Content</span><span class="sxs-lookup"><span data-stu-id="1c120-117">get_Content</span></span>](#get_content) | <span data-ttu-id="1c120-118">El cuerpo del mensaje de la solicitud HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="1c120-118">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="1c120-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="1c120-119">put_Content</span></span>](#put_content) | <span data-ttu-id="1c120-120">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="1c120-120">Set the Content property.</span></span>
[<span data-ttu-id="1c120-121">get_Headers</span><span class="sxs-lookup"><span data-stu-id="1c120-121">get_Headers</span></span>](#get_headers) | <span data-ttu-id="1c120-122">Los encabezados de solicitud HTTP mutable.</span><span class="sxs-lookup"><span data-stu-id="1c120-122">The mutable HTTP request headers.</span></span>

## <span data-ttu-id="1c120-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="1c120-123">Members</span></span>

#### <span data-ttu-id="1c120-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="1c120-124">get_Uri</span></span> 

<span data-ttu-id="1c120-125">Identificador URI de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1c120-125">The request URI.</span></span>

> <span data-ttu-id="1c120-126">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="1c120-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="1c120-127">put_Uri</span><span class="sxs-lookup"><span data-stu-id="1c120-127">put_Uri</span></span> 

<span data-ttu-id="1c120-128">Establezca la propiedad URI.</span><span class="sxs-lookup"><span data-stu-id="1c120-128">Set the Uri property.</span></span>

> <span data-ttu-id="1c120-129">[put_Uri](#put_uri)de HRESULT público (URI de LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="1c120-129">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

#### <span data-ttu-id="1c120-130">get_Method</span><span class="sxs-lookup"><span data-stu-id="1c120-130">get_Method</span></span> 

<span data-ttu-id="1c120-131">El método de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="1c120-131">The HTTP request method.</span></span>

> <span data-ttu-id="1c120-132">[get_Method](#get_method)de HRESULT público (método LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="1c120-132">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="1c120-133">put_Method</span><span class="sxs-lookup"><span data-stu-id="1c120-133">put_Method</span></span> 

<span data-ttu-id="1c120-134">Establezca la propiedad Method.</span><span class="sxs-lookup"><span data-stu-id="1c120-134">Set the Method property.</span></span>

> <span data-ttu-id="1c120-135">[put_Method](#put_method)de HRESULT público (método LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="1c120-135">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="1c120-136">get_Content</span><span class="sxs-lookup"><span data-stu-id="1c120-136">get_Content</span></span> 

<span data-ttu-id="1c120-137">El cuerpo del mensaje de la solicitud HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="1c120-137">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="1c120-138">[get_Content](#get_content)(HRESULT) público (contenido de IStream \* \*)</span><span class="sxs-lookup"><span data-stu-id="1c120-138">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="1c120-139">Los datos de publicación estarán aquí.</span><span class="sxs-lookup"><span data-stu-id="1c120-139">POST data would be here.</span></span> <span data-ttu-id="1c120-140">Si se establece una secuencia, lo que invalidará el cuerpo del mensaje, la secuencia debe tener todos los datos de contenido disponibles en el momento en que se complete el aplazamiento de eventos de WebResourceRequested de esta respuesta.</span><span class="sxs-lookup"><span data-stu-id="1c120-140">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="1c120-141">La secuencia debe ser ágil o crearse a partir de un STA de fondo para evitar el impacto en el rendimiento en el subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1c120-141">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="1c120-142">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="1c120-142">Null means no content data.</span></span> <span data-ttu-id="1c120-143">Se aplican las semánticas de IStream (Return S_OK para leer las llamadas hasta que se agoten todos los datos)</span><span class="sxs-lookup"><span data-stu-id="1c120-143">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="1c120-144">put_Content</span><span class="sxs-lookup"><span data-stu-id="1c120-144">put_Content</span></span> 

<span data-ttu-id="1c120-145">Establezca la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="1c120-145">Set the Content property.</span></span>

> <span data-ttu-id="1c120-146">[put_Content](#put_content)(HRESULT) público (contenido de IStream \*)</span><span class="sxs-lookup"><span data-stu-id="1c120-146">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="1c120-147">get_Headers</span><span class="sxs-lookup"><span data-stu-id="1c120-147">get_Headers</span></span> 

<span data-ttu-id="1c120-148">Los encabezados de solicitud HTTP mutable.</span><span class="sxs-lookup"><span data-stu-id="1c120-148">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="1c120-149">[get_Headers](#get_headers)de HRESULT público (encabezados[IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="1c120-149">public HRESULT [get_Headers](#get_headers)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* headers)</span></span>


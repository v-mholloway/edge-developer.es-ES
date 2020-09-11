---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest
ms.openlocfilehash: 5c8d164b24995cc31070232dd9b1a2d88fc16cec
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012627"
---
# <span data-ttu-id="e8a19-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="e8a19-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequest class</span></span> 

<span data-ttu-id="e8a19-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="e8a19-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="e8a19-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="e8a19-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="e8a19-107">Una solicitud HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="e8a19-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="e8a19-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="e8a19-108">Summary</span></span>

 <span data-ttu-id="e8a19-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="e8a19-109">Members</span></span>                        | <span data-ttu-id="e8a19-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e8a19-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e8a19-111">Contenido</span><span class="sxs-lookup"><span data-stu-id="e8a19-111">Content</span></span>](#content) | <span data-ttu-id="e8a19-112">El cuerpo del mensaje de la solicitud HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="e8a19-112">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="e8a19-113">Encabezados</span><span class="sxs-lookup"><span data-stu-id="e8a19-113">Headers</span></span>](#headers) | <span data-ttu-id="e8a19-114">Los encabezados de solicitud HTTP mutable.</span><span class="sxs-lookup"><span data-stu-id="e8a19-114">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="e8a19-115">Método</span><span class="sxs-lookup"><span data-stu-id="e8a19-115">Method</span></span>](#method) | <span data-ttu-id="e8a19-116">El método de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="e8a19-116">The HTTP request method.</span></span>
[<span data-ttu-id="e8a19-117">URI</span><span class="sxs-lookup"><span data-stu-id="e8a19-117">Uri</span></span>](#uri) | <span data-ttu-id="e8a19-118">Identificador URI de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e8a19-118">The request URI.</span></span>

## <span data-ttu-id="e8a19-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="e8a19-119">Members</span></span>

#### <span data-ttu-id="e8a19-120">Contenido</span><span class="sxs-lookup"><span data-stu-id="e8a19-120">Content</span></span> 

<span data-ttu-id="e8a19-121">El cuerpo del mensaje de la solicitud HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="e8a19-121">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="e8a19-122">[contenido](#content) de secuencia pública</span><span class="sxs-lookup"><span data-stu-id="e8a19-122">public Stream [Content](#content)</span></span>

<span data-ttu-id="e8a19-123">Los datos de publicación estarán aquí.</span><span class="sxs-lookup"><span data-stu-id="e8a19-123">POST data would be here.</span></span> <span data-ttu-id="e8a19-124">Si se establece una secuencia, lo que invalidará el cuerpo del mensaje, la secuencia debe tener todos los datos de contenido disponibles en el momento en que se complete el aplazamiento de eventos de WebResourceRequested de esta respuesta.</span><span class="sxs-lookup"><span data-stu-id="e8a19-124">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="e8a19-125">La secuencia debe ser ágil o crearse a partir de un STA de fondo para evitar el impacto en el rendimiento en el subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e8a19-125">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="e8a19-126">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="e8a19-126">Null means no content data.</span></span> <span data-ttu-id="e8a19-127">Se aplican las semánticas de IStream (devuelva S_OK para leer las llamadas hasta que se agoten todos los datos).</span><span class="sxs-lookup"><span data-stu-id="e8a19-127">IStream semantics apply (return S_OK to Read calls until all data is exhausted).</span></span>

#### <span data-ttu-id="e8a19-128">Encabezados</span><span class="sxs-lookup"><span data-stu-id="e8a19-128">Headers</span></span> 

<span data-ttu-id="e8a19-129">Los encabezados de solicitud HTTP mutable.</span><span class="sxs-lookup"><span data-stu-id="e8a19-129">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="e8a19-130">[encabezados](#headers) de [CoreWebView2HttpRequestHeaders](microsoft-web-webview2-core-corewebview2httprequestheaders.md) pública</span><span class="sxs-lookup"><span data-stu-id="e8a19-130">public [CoreWebView2HttpRequestHeaders](microsoft-web-webview2-core-corewebview2httprequestheaders.md) [Headers](#headers)</span></span>

#### <span data-ttu-id="e8a19-131">Método</span><span class="sxs-lookup"><span data-stu-id="e8a19-131">Method</span></span> 

<span data-ttu-id="e8a19-132">El método de solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="e8a19-132">The HTTP request method.</span></span>

> <span data-ttu-id="e8a19-133">[método](#method) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="e8a19-133">public string [Method](#method)</span></span>

#### <span data-ttu-id="e8a19-134">URI</span><span class="sxs-lookup"><span data-stu-id="e8a19-134">Uri</span></span> 

<span data-ttu-id="e8a19-135">Identificador URI de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e8a19-135">The request URI.</span></span>

> <span data-ttu-id="e8a19-136">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="e8a19-136">public string [Uri](#uri)</span></span>


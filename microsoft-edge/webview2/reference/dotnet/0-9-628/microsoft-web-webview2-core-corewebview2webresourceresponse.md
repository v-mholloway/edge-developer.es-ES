---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
ms.openlocfilehash: 5359634d83717ce844d2c1604a2645ceffc477cc
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012623"
---
# <span data-ttu-id="d0b8e-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="d0b8e-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponse class</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="d0b8e-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="d0b8e-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="d0b8e-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="d0b8e-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="d0b8e-107">Una respuesta HTTP usada con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="d0b8e-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="d0b8e-108">Summary</span></span>

 <span data-ttu-id="d0b8e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="d0b8e-109">Members</span></span>                        | <span data-ttu-id="d0b8e-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="d0b8e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d0b8e-111">Contenido</span><span class="sxs-lookup"><span data-stu-id="d0b8e-111">Content</span></span>](#content) | <span data-ttu-id="d0b8e-112">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="d0b8e-113">Encabezados</span><span class="sxs-lookup"><span data-stu-id="d0b8e-113">Headers</span></span>](#headers) | <span data-ttu-id="d0b8e-114">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="d0b8e-115">ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="d0b8e-115">ReasonPhrase</span></span>](#reasonphrase) | <span data-ttu-id="d0b8e-116">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-116">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="d0b8e-117">StatusCode</span><span class="sxs-lookup"><span data-stu-id="d0b8e-117">StatusCode</span></span>](#statuscode) | <span data-ttu-id="d0b8e-118">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-118">The HTTP response status code.</span></span>

## <span data-ttu-id="d0b8e-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="d0b8e-119">Members</span></span>

#### <span data-ttu-id="d0b8e-120">Contenido</span><span class="sxs-lookup"><span data-stu-id="d0b8e-120">Content</span></span> 

<span data-ttu-id="d0b8e-121">Contenido de la respuesta HTTP como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-121">HTTP response content as stream.</span></span>

> <span data-ttu-id="d0b8e-122">[contenido](#content) de secuencia pública</span><span class="sxs-lookup"><span data-stu-id="d0b8e-122">public Stream [Content](#content)</span></span>

<span data-ttu-id="d0b8e-123">La secuencia debe tener todos los datos de contenido disponibles por el momento en que se completa este aplazamiento de eventos de WebResourceRequested de respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-123">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="d0b8e-124">La secuencia debe ser ágil o crearse a partir de un subproceso en segundo plano para evitar el impacto en el rendimiento del subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-124">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="d0b8e-125">Null significa que no hay datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-125">Null means no content data.</span></span> <span data-ttu-id="d0b8e-126">Se aplican las semánticas de IStream (devuelva S_OK para leer las llamadas hasta que se agoten todos los datos).</span><span class="sxs-lookup"><span data-stu-id="d0b8e-126">IStream semantics apply (return S_OK to Read calls until all data is exhausted).</span></span>

#### <span data-ttu-id="d0b8e-127">Encabezados</span><span class="sxs-lookup"><span data-stu-id="d0b8e-127">Headers</span></span> 

<span data-ttu-id="d0b8e-128">Encabezados de respuesta HTTP invalidados.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-128">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="d0b8e-129">[encabezados](#headers) de [CoreWebView2HttpResponseHeaders](microsoft-web-webview2-core-corewebview2httpresponseheaders.md) pública</span><span class="sxs-lookup"><span data-stu-id="d0b8e-129">public [CoreWebView2HttpResponseHeaders](microsoft-web-webview2-core-corewebview2httpresponseheaders.md) [Headers](#headers)</span></span>

#### <span data-ttu-id="d0b8e-130">ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="d0b8e-130">ReasonPhrase</span></span> 

<span data-ttu-id="d0b8e-131">La frase de razón de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-131">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="d0b8e-132">cadena pública [ReasonPhrase](#reasonphrase)</span><span class="sxs-lookup"><span data-stu-id="d0b8e-132">public string [ReasonPhrase](#reasonphrase)</span></span>

#### <span data-ttu-id="d0b8e-133">StatusCode</span><span class="sxs-lookup"><span data-stu-id="d0b8e-133">StatusCode</span></span> 

<span data-ttu-id="d0b8e-134">El código de estado de respuesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="d0b8e-134">The HTTP response status code.</span></span>

> <span data-ttu-id="d0b8e-135">public int [StatusCode](#statuscode)</span><span class="sxs-lookup"><span data-stu-id="d0b8e-135">public int [StatusCode](#statuscode)</span></span>


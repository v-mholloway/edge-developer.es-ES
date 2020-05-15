---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 8b7ac3ab27cf5a2d9e80a77eabc488599820a02f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655500"
---
# <span data-ttu-id="f4956-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="f4956-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

<span data-ttu-id="f4956-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f4956-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f4956-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="f4956-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f4956-107">Argumentos de evento para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="f4956-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="f4956-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="f4956-108">Summary</span></span>

 <span data-ttu-id="f4956-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="f4956-109">Members</span></span>                        | <span data-ttu-id="f4956-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="f4956-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f4956-111">Cancelar</span><span class="sxs-lookup"><span data-stu-id="f4956-111">Cancel</span></span>](#cancel) | <span data-ttu-id="f4956-112">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="f4956-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="f4956-113">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="f4956-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="f4956-114">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="f4956-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="f4956-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="f4956-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="f4956-116">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="f4956-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="f4956-117">NavigationId</span><span class="sxs-lookup"><span data-stu-id="f4956-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="f4956-118">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="f4956-118">The ID of the navigation.</span></span>
[<span data-ttu-id="f4956-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="f4956-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="f4956-120">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="f4956-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="f4956-121">URI</span><span class="sxs-lookup"><span data-stu-id="f4956-121">Uri</span></span>](#uri) | <span data-ttu-id="f4956-122">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="f4956-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="f4956-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="f4956-123">Members</span></span>

#### <span data-ttu-id="f4956-124">Cancelar</span><span class="sxs-lookup"><span data-stu-id="f4956-124">Cancel</span></span> 

<span data-ttu-id="f4956-125">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="f4956-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="f4956-126">[cancelación](#cancel) pública de bool</span><span class="sxs-lookup"><span data-stu-id="f4956-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="f4956-127">Si se establece, será como si la navegación nunca ocurriera y el contenido de la página actual permanecerá intacto.</span><span class="sxs-lookup"><span data-stu-id="f4956-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="f4956-128">Por razones de rendimiento, pueden producirse solicitudes HTTP mientras el host responde.</span><span class="sxs-lookup"><span data-stu-id="f4956-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="f4956-129">Esto significa que las cookies se pueden establecer y usar parte de una solicitud de navegación.</span><span class="sxs-lookup"><span data-stu-id="f4956-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="f4956-130">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="f4956-130">IsRedirected</span></span> 

<span data-ttu-id="f4956-131">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="f4956-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="f4956-132">Public bool [IsRedirected](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="f4956-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="f4956-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="f4956-133">IsUserInitiated</span></span> 

<span data-ttu-id="f4956-134">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="f4956-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="f4956-135">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="f4956-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="f4956-136">NavigationId</span><span class="sxs-lookup"><span data-stu-id="f4956-136">NavigationId</span></span> 

<span data-ttu-id="f4956-137">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="f4956-137">The ID of the navigation.</span></span>

> <span data-ttu-id="f4956-138">ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="f4956-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="f4956-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="f4956-139">RequestHeaders</span></span> 

<span data-ttu-id="f4956-140">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="f4956-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="f4956-141">HttpRequestHeaders pública [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="f4956-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="f4956-142">Tenga en cuenta que no puede modificar los encabezados de la solicitud HTTP en un evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="f4956-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="f4956-143">URI</span><span class="sxs-lookup"><span data-stu-id="f4956-143">Uri</span></span> 

<span data-ttu-id="f4956-144">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="f4956-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="f4956-145">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="f4956-145">public string [Uri](#uri)</span></span>


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
ms.openlocfilehash: 58ca180e73c3e4644e466e13c4059f32102f1896
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699315"
---
# <span data-ttu-id="a1246-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="a1246-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

<span data-ttu-id="a1246-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="a1246-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="a1246-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="a1246-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="a1246-107">Argumentos de evento para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="a1246-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="a1246-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="a1246-108">Summary</span></span>

 <span data-ttu-id="a1246-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a1246-109">Members</span></span>                        | <span data-ttu-id="a1246-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a1246-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a1246-111">Cancelar</span><span class="sxs-lookup"><span data-stu-id="a1246-111">Cancel</span></span>](#cancel) | <span data-ttu-id="a1246-112">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="a1246-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="a1246-113">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="a1246-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="a1246-114">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="a1246-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="a1246-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a1246-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="a1246-116">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="a1246-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="a1246-117">NavigationId</span><span class="sxs-lookup"><span data-stu-id="a1246-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="a1246-118">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="a1246-118">The ID of the navigation.</span></span>
[<span data-ttu-id="a1246-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="a1246-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="a1246-120">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="a1246-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="a1246-121">URI</span><span class="sxs-lookup"><span data-stu-id="a1246-121">Uri</span></span>](#uri) | <span data-ttu-id="a1246-122">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="a1246-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="a1246-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="a1246-123">Members</span></span>

#### <span data-ttu-id="a1246-124">Cancelar</span><span class="sxs-lookup"><span data-stu-id="a1246-124">Cancel</span></span> 

<span data-ttu-id="a1246-125">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="a1246-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="a1246-126">[cancelación](#cancel) pública de bool</span><span class="sxs-lookup"><span data-stu-id="a1246-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="a1246-127">Si se establece, será como si la navegación nunca ocurriera y el contenido de la página actual permanecerá intacto.</span><span class="sxs-lookup"><span data-stu-id="a1246-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="a1246-128">Por razones de rendimiento, pueden producirse solicitudes HTTP mientras el host responde.</span><span class="sxs-lookup"><span data-stu-id="a1246-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="a1246-129">Esto significa que las cookies se pueden establecer y usar parte de una solicitud de navegación.</span><span class="sxs-lookup"><span data-stu-id="a1246-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="a1246-130">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="a1246-130">IsRedirected</span></span> 

<span data-ttu-id="a1246-131">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="a1246-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="a1246-132">Public bool [IsRedirected](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="a1246-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="a1246-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a1246-133">IsUserInitiated</span></span> 

<span data-ttu-id="a1246-134">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="a1246-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="a1246-135">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="a1246-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="a1246-136">NavigationId</span><span class="sxs-lookup"><span data-stu-id="a1246-136">NavigationId</span></span> 

<span data-ttu-id="a1246-137">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="a1246-137">The ID of the navigation.</span></span>

> <span data-ttu-id="a1246-138">ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="a1246-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="a1246-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="a1246-139">RequestHeaders</span></span> 

<span data-ttu-id="a1246-140">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="a1246-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="a1246-141">HttpRequestHeaders pública [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="a1246-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="a1246-142">Tenga en cuenta que no puede modificar los encabezados de la solicitud HTTP en un evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="a1246-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="a1246-143">URI</span><span class="sxs-lookup"><span data-stu-id="a1246-143">Uri</span></span> 

<span data-ttu-id="a1246-144">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="a1246-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="a1246-145">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="a1246-145">public string [Uri](#uri)</span></span>


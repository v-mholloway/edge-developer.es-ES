---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: 1b80b42bc26316d1fcc8ac74656f24cb0db75bae
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012644"
---
# <span data-ttu-id="963f1-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="963f1-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

<span data-ttu-id="963f1-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="963f1-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="963f1-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="963f1-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="963f1-107">Argumentos de evento para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="963f1-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="963f1-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="963f1-108">Summary</span></span>

 <span data-ttu-id="963f1-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="963f1-109">Members</span></span>                        | <span data-ttu-id="963f1-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="963f1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="963f1-111">Cancelar</span><span class="sxs-lookup"><span data-stu-id="963f1-111">Cancel</span></span>](#cancel) | <span data-ttu-id="963f1-112">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="963f1-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="963f1-113">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="963f1-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="963f1-114">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="963f1-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="963f1-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="963f1-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="963f1-116">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="963f1-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="963f1-117">NavigationId</span><span class="sxs-lookup"><span data-stu-id="963f1-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="963f1-118">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="963f1-118">The ID of the navigation.</span></span>
[<span data-ttu-id="963f1-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="963f1-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="963f1-120">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="963f1-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="963f1-121">URI</span><span class="sxs-lookup"><span data-stu-id="963f1-121">Uri</span></span>](#uri) | <span data-ttu-id="963f1-122">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="963f1-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="963f1-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="963f1-123">Members</span></span>

#### <span data-ttu-id="963f1-124">Cancelar</span><span class="sxs-lookup"><span data-stu-id="963f1-124">Cancel</span></span> 

<span data-ttu-id="963f1-125">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="963f1-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="963f1-126">[cancelación](#cancel) pública de bool</span><span class="sxs-lookup"><span data-stu-id="963f1-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="963f1-127">Si se establece, será como si la navegación nunca ocurriera y el contenido de la página actual permanecerá intacto.</span><span class="sxs-lookup"><span data-stu-id="963f1-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="963f1-128">Por razones de rendimiento, pueden producirse solicitudes HTTP mientras el host responde.</span><span class="sxs-lookup"><span data-stu-id="963f1-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="963f1-129">Esto significa que las cookies se pueden establecer y usar parte de una solicitud de navegación.</span><span class="sxs-lookup"><span data-stu-id="963f1-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="963f1-130">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="963f1-130">IsRedirected</span></span> 

<span data-ttu-id="963f1-131">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="963f1-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="963f1-132">Public bool [IsRedirected](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="963f1-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="963f1-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="963f1-133">IsUserInitiated</span></span> 

<span data-ttu-id="963f1-134">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="963f1-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="963f1-135">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="963f1-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="963f1-136">NavigationId</span><span class="sxs-lookup"><span data-stu-id="963f1-136">NavigationId</span></span> 

<span data-ttu-id="963f1-137">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="963f1-137">The ID of the navigation.</span></span>

> <span data-ttu-id="963f1-138">ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="963f1-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="963f1-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="963f1-139">RequestHeaders</span></span> 

<span data-ttu-id="963f1-140">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="963f1-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="963f1-141">CoreWebView2HttpRequestHeaders pública [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="963f1-141">public CoreWebView2HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="963f1-142">Tenga en cuenta que no puede modificar los encabezados de la solicitud HTTP en un evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="963f1-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="963f1-143">URI</span><span class="sxs-lookup"><span data-stu-id="963f1-143">Uri</span></span> 

<span data-ttu-id="963f1-144">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="963f1-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="963f1-145">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="963f1-145">public string [Uri](#uri)</span></span>


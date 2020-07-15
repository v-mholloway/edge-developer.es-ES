---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: ea3936ac1267fa085f62db843f5cac3fad2635b5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879789"
---
# <span data-ttu-id="bbbdf-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs (clase)</span><span class="sxs-lookup"><span data-stu-id="bbbdf-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="bbbdf-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="bbbdf-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="bbbdf-107">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="bbbdf-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="bbbdf-108">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="bbbdf-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="bbbdf-109">Argumentos de evento para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-109">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="bbbdf-110">Resumen</span><span class="sxs-lookup"><span data-stu-id="bbbdf-110">Summary</span></span>

 <span data-ttu-id="bbbdf-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="bbbdf-111">Members</span></span>                        | <span data-ttu-id="bbbdf-112">Descripciones</span><span class="sxs-lookup"><span data-stu-id="bbbdf-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bbbdf-113">Cancelar</span><span class="sxs-lookup"><span data-stu-id="bbbdf-113">Cancel</span></span>](#cancel) | <span data-ttu-id="bbbdf-114">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-114">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="bbbdf-115">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="bbbdf-115">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="bbbdf-116">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="bbbdf-117">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="bbbdf-117">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="bbbdf-118">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-118">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="bbbdf-119">NavigationId</span><span class="sxs-lookup"><span data-stu-id="bbbdf-119">NavigationId</span></span>](#navigationid) | <span data-ttu-id="bbbdf-120">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-120">The ID of the navigation.</span></span>
[<span data-ttu-id="bbbdf-121">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="bbbdf-121">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="bbbdf-122">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-122">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="bbbdf-123">URI</span><span class="sxs-lookup"><span data-stu-id="bbbdf-123">Uri</span></span>](#uri) | <span data-ttu-id="bbbdf-124">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-124">The uri of the requested navigation.</span></span>

## <span data-ttu-id="bbbdf-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="bbbdf-125">Members</span></span>

#### <span data-ttu-id="bbbdf-126">Cancelar</span><span class="sxs-lookup"><span data-stu-id="bbbdf-126">Cancel</span></span> 

<span data-ttu-id="bbbdf-127">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-127">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="bbbdf-128">[cancelación](#cancel) pública de bool</span><span class="sxs-lookup"><span data-stu-id="bbbdf-128">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="bbbdf-129">Si se establece, será como si la navegación nunca ocurriera y el contenido de la página actual permanecerá intacto.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-129">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="bbbdf-130">Por razones de rendimiento, pueden producirse solicitudes HTTP mientras el host responde.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-130">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="bbbdf-131">Esto significa que las cookies se pueden establecer y usar parte de una solicitud de navegación.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-131">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="bbbdf-132">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="bbbdf-132">IsRedirected</span></span> 

<span data-ttu-id="bbbdf-133">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="bbbdf-134">Public bool [IsRedirected](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="bbbdf-134">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="bbbdf-135">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="bbbdf-135">IsUserInitiated</span></span> 

<span data-ttu-id="bbbdf-136">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="bbbdf-137">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="bbbdf-137">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="bbbdf-138">NavigationId</span><span class="sxs-lookup"><span data-stu-id="bbbdf-138">NavigationId</span></span> 

<span data-ttu-id="bbbdf-139">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-139">The ID of the navigation.</span></span>

> <span data-ttu-id="bbbdf-140">ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="bbbdf-140">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="bbbdf-141">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="bbbdf-141">RequestHeaders</span></span> 

<span data-ttu-id="bbbdf-142">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="bbbdf-143">HttpRequestHeaders pública [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="bbbdf-143">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="bbbdf-144">Tenga en cuenta que no puede modificar los encabezados de la solicitud HTTP en un evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="bbbdf-145">URI</span><span class="sxs-lookup"><span data-stu-id="bbbdf-145">Uri</span></span> 

<span data-ttu-id="bbbdf-146">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="bbbdf-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="bbbdf-147">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="bbbdf-147">public string [Uri](#uri)</span></span>


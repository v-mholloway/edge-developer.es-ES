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
ms.openlocfilehash: 98e242ace5eb0ae5958ddb1eb6cd380d194294be
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697633"
---
# <span data-ttu-id="fee28-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="fee28-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="fee28-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="fee28-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="fee28-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="fee28-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="fee28-107">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="fee28-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="fee28-108">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="fee28-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="fee28-109">Argumentos de evento para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="fee28-109">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="fee28-110">Resumen</span><span class="sxs-lookup"><span data-stu-id="fee28-110">Summary</span></span>

 <span data-ttu-id="fee28-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="fee28-111">Members</span></span>                        | <span data-ttu-id="fee28-112">Descripciones</span><span class="sxs-lookup"><span data-stu-id="fee28-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fee28-113">Cancelar</span><span class="sxs-lookup"><span data-stu-id="fee28-113">Cancel</span></span>](#cancel) | <span data-ttu-id="fee28-114">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="fee28-114">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="fee28-115">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="fee28-115">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="fee28-116">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="fee28-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="fee28-117">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="fee28-117">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="fee28-118">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="fee28-118">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="fee28-119">NavigationId</span><span class="sxs-lookup"><span data-stu-id="fee28-119">NavigationId</span></span>](#navigationid) | <span data-ttu-id="fee28-120">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="fee28-120">The ID of the navigation.</span></span>
[<span data-ttu-id="fee28-121">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="fee28-121">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="fee28-122">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="fee28-122">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="fee28-123">URI</span><span class="sxs-lookup"><span data-stu-id="fee28-123">Uri</span></span>](#uri) | <span data-ttu-id="fee28-124">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="fee28-124">The uri of the requested navigation.</span></span>

## <span data-ttu-id="fee28-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="fee28-125">Members</span></span>

#### <span data-ttu-id="fee28-126">Cancelar</span><span class="sxs-lookup"><span data-stu-id="fee28-126">Cancel</span></span> 

<span data-ttu-id="fee28-127">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="fee28-127">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="fee28-128">[cancelación](#cancel) pública de bool</span><span class="sxs-lookup"><span data-stu-id="fee28-128">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="fee28-129">Si se establece, será como si la navegación nunca ocurriera y el contenido de la página actual permanecerá intacto.</span><span class="sxs-lookup"><span data-stu-id="fee28-129">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="fee28-130">Por razones de rendimiento, pueden producirse solicitudes HTTP mientras el host responde.</span><span class="sxs-lookup"><span data-stu-id="fee28-130">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="fee28-131">Esto significa que las cookies se pueden establecer y usar parte de una solicitud de navegación.</span><span class="sxs-lookup"><span data-stu-id="fee28-131">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="fee28-132">IsRedirected</span><span class="sxs-lookup"><span data-stu-id="fee28-132">IsRedirected</span></span> 

<span data-ttu-id="fee28-133">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="fee28-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="fee28-134">Public bool [IsRedirected](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="fee28-134">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="fee28-135">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="fee28-135">IsUserInitiated</span></span> 

<span data-ttu-id="fee28-136">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="fee28-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="fee28-137">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="fee28-137">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="fee28-138">NavigationId</span><span class="sxs-lookup"><span data-stu-id="fee28-138">NavigationId</span></span> 

<span data-ttu-id="fee28-139">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="fee28-139">The ID of the navigation.</span></span>

> <span data-ttu-id="fee28-140">ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="fee28-140">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="fee28-141">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="fee28-141">RequestHeaders</span></span> 

<span data-ttu-id="fee28-142">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="fee28-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="fee28-143">HttpRequestHeaders pública [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="fee28-143">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="fee28-144">Tenga en cuenta que no puede modificar los encabezados de la solicitud HTTP en un evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="fee28-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="fee28-145">URI</span><span class="sxs-lookup"><span data-stu-id="fee28-145">Uri</span></span> 

<span data-ttu-id="fee28-146">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="fee28-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="fee28-147">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="fee28-147">public string [Uri](#uri)</span></span>


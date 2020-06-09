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
ms.openlocfilehash: 705289c386a174bf6ac3929fabf9ede92e0987ae
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699304"
---
# <span data-ttu-id="b6bee-104">interfaz ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="b6bee-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="b6bee-105">Argumentos de evento para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="b6bee-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="b6bee-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="b6bee-106">Summary</span></span>

 <span data-ttu-id="b6bee-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b6bee-107">Members</span></span>                        | <span data-ttu-id="b6bee-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b6bee-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b6bee-109">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="b6bee-109">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="b6bee-110">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="b6bee-110">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="b6bee-111">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="b6bee-111">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="b6bee-112">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="b6bee-112">True when the navigation is redirected.</span></span>
[<span data-ttu-id="b6bee-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="b6bee-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="b6bee-114">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="b6bee-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="b6bee-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="b6bee-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="b6bee-116">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="b6bee-116">The ID of the navigation.</span></span>
[<span data-ttu-id="b6bee-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="b6bee-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="b6bee-118">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="b6bee-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="b6bee-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b6bee-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="b6bee-120">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="b6bee-120">The uri of the requested navigation.</span></span>
[<span data-ttu-id="b6bee-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="b6bee-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="b6bee-122">Establezca la propiedad cancelar.</span><span class="sxs-lookup"><span data-stu-id="b6bee-122">Set the Cancel property.</span></span>

## <span data-ttu-id="b6bee-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="b6bee-123">Members</span></span>

#### <span data-ttu-id="b6bee-124">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="b6bee-124">get_Cancel</span></span> 

<span data-ttu-id="b6bee-125">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="b6bee-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="b6bee-126">[get_Cancel](#get_cancel)de HRESULT público (bool \* CANCEL)</span><span class="sxs-lookup"><span data-stu-id="b6bee-126">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="b6bee-127">Si se establece, será como si la navegación nunca ocurriera y el contenido de la página actual permanecerá intacto.</span><span class="sxs-lookup"><span data-stu-id="b6bee-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="b6bee-128">Por razones de rendimiento, pueden producirse solicitudes HTTP mientras el host responde.</span><span class="sxs-lookup"><span data-stu-id="b6bee-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="b6bee-129">Esto significa que las cookies se pueden establecer y usar parte de una solicitud de navegación.</span><span class="sxs-lookup"><span data-stu-id="b6bee-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="b6bee-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="b6bee-130">get_IsRedirected</span></span> 

<span data-ttu-id="b6bee-131">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="b6bee-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="b6bee-132">[get_IsRedirected](#get_isredirected)de HRESULT público (bool \* IsRedirected)</span><span class="sxs-lookup"><span data-stu-id="b6bee-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="b6bee-133">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="b6bee-133">get_IsUserInitiated</span></span> 

<span data-ttu-id="b6bee-134">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="b6bee-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="b6bee-135">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="b6bee-135">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="b6bee-136">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="b6bee-136">get_NavigationId</span></span> 

<span data-ttu-id="b6bee-137">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="b6bee-137">The ID of the navigation.</span></span>

> <span data-ttu-id="b6bee-138">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="b6bee-138">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="b6bee-139">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="b6bee-139">get_RequestHeaders</span></span> 

<span data-ttu-id="b6bee-140">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="b6bee-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="b6bee-141">[get_RequestHeaders](#get_requestheaders)(HRESULT) público ([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="b6bee-141">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="b6bee-142">Tenga en cuenta que no puede modificar los encabezados de la solicitud HTTP en un evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="b6bee-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="b6bee-143">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b6bee-143">get_Uri</span></span> 

<span data-ttu-id="b6bee-144">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="b6bee-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="b6bee-145">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="b6bee-145">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="b6bee-146">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="b6bee-146">put_Cancel</span></span> 

<span data-ttu-id="b6bee-147">Establezca la propiedad cancelar.</span><span class="sxs-lookup"><span data-stu-id="b6bee-147">Set the Cancel property.</span></span>

> <span data-ttu-id="b6bee-148">[put_Cancel](#put_cancel)de HRESULT público (bool CANCEL)</span><span class="sxs-lookup"><span data-stu-id="b6bee-148">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 3b348d64bb09fcdc693ffbdfa5481fe6d7520cae
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655143"
---
# <span data-ttu-id="88230-104">interfaz ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="88230-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="88230-105">Argumentos de evento para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="88230-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="88230-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="88230-106">Summary</span></span>

 <span data-ttu-id="88230-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="88230-107">Members</span></span>                        | <span data-ttu-id="88230-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="88230-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="88230-109">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="88230-109">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="88230-110">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="88230-110">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="88230-111">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="88230-111">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="88230-112">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="88230-112">True when the navigation is redirected.</span></span>
[<span data-ttu-id="88230-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="88230-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="88230-114">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="88230-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="88230-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="88230-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="88230-116">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="88230-116">The ID of the navigation.</span></span>
[<span data-ttu-id="88230-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="88230-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="88230-118">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="88230-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="88230-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="88230-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="88230-120">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="88230-120">The uri of the requested navigation.</span></span>
[<span data-ttu-id="88230-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="88230-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="88230-122">Establezca la propiedad cancelar.</span><span class="sxs-lookup"><span data-stu-id="88230-122">Set the Cancel property.</span></span>

## <span data-ttu-id="88230-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="88230-123">Members</span></span>

#### <span data-ttu-id="88230-124">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="88230-124">get_Cancel</span></span> 

<span data-ttu-id="88230-125">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="88230-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="88230-126">[get_Cancel](#get_cancel)de HRESULT público (bool \* CANCEL)</span><span class="sxs-lookup"><span data-stu-id="88230-126">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="88230-127">Si se establece, será como si la navegación nunca ocurriera y el contenido de la página actual permanecerá intacto.</span><span class="sxs-lookup"><span data-stu-id="88230-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="88230-128">Por razones de rendimiento, pueden producirse solicitudes HTTP mientras el host responde.</span><span class="sxs-lookup"><span data-stu-id="88230-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="88230-129">Esto significa que las cookies se pueden establecer y usar parte de una solicitud de navegación.</span><span class="sxs-lookup"><span data-stu-id="88230-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="88230-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="88230-130">get_IsRedirected</span></span> 

<span data-ttu-id="88230-131">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="88230-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="88230-132">[get_IsRedirected](#get_isredirected)de HRESULT público (bool \* IsRedirected)</span><span class="sxs-lookup"><span data-stu-id="88230-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="88230-133">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="88230-133">get_IsUserInitiated</span></span> 

<span data-ttu-id="88230-134">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="88230-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="88230-135">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="88230-135">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="88230-136">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="88230-136">get_NavigationId</span></span> 

<span data-ttu-id="88230-137">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="88230-137">The ID of the navigation.</span></span>

> <span data-ttu-id="88230-138">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="88230-138">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="88230-139">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="88230-139">get_RequestHeaders</span></span> 

<span data-ttu-id="88230-140">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="88230-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="88230-141">[get_RequestHeaders](#get_requestheaders)(HRESULT) público ([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="88230-141">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="88230-142">Tenga en cuenta que no puede modificar los encabezados de la solicitud HTTP en un evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="88230-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="88230-143">get_Uri</span><span class="sxs-lookup"><span data-stu-id="88230-143">get_Uri</span></span> 

<span data-ttu-id="88230-144">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="88230-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="88230-145">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="88230-145">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="88230-146">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="88230-146">put_Cancel</span></span> 

<span data-ttu-id="88230-147">Establezca la propiedad cancelar.</span><span class="sxs-lookup"><span data-stu-id="88230-147">Set the Cancel property.</span></span>

> <span data-ttu-id="88230-148">[put_Cancel](#put_cancel)de HRESULT público (bool CANCEL)</span><span class="sxs-lookup"><span data-stu-id="88230-148">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>


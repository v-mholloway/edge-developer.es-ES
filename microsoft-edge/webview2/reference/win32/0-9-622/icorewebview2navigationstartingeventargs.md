---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: ebfb4aaf3f0c2b5531aaab3783572cf550bebf83
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012731"
---
# <span data-ttu-id="35eff-104">interfaz ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="35eff-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="35eff-105">Argumentos de evento para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="35eff-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="35eff-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="35eff-106">Summary</span></span>

 <span data-ttu-id="35eff-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="35eff-107">Members</span></span>                        | <span data-ttu-id="35eff-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="35eff-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="35eff-109">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="35eff-109">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="35eff-110">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="35eff-110">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="35eff-111">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="35eff-111">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="35eff-112">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="35eff-112">True when the navigation is redirected.</span></span>
[<span data-ttu-id="35eff-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="35eff-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="35eff-114">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="35eff-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="35eff-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="35eff-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="35eff-116">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="35eff-116">The ID of the navigation.</span></span>
[<span data-ttu-id="35eff-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="35eff-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="35eff-118">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="35eff-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="35eff-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="35eff-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="35eff-120">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="35eff-120">The uri of the requested navigation.</span></span>
[<span data-ttu-id="35eff-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="35eff-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="35eff-122">Establezca la propiedad cancelar.</span><span class="sxs-lookup"><span data-stu-id="35eff-122">Set the Cancel property.</span></span>

## <span data-ttu-id="35eff-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="35eff-123">Members</span></span>

#### <span data-ttu-id="35eff-124">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="35eff-124">get_Cancel</span></span> 

<span data-ttu-id="35eff-125">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="35eff-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="35eff-126">[get_Cancel](#get_cancel)de HRESULT público (bool \* CANCEL)</span><span class="sxs-lookup"><span data-stu-id="35eff-126">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="35eff-127">Si se establece, será como si la navegación nunca ocurriera y el contenido de la página actual permanecerá intacto.</span><span class="sxs-lookup"><span data-stu-id="35eff-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="35eff-128">Por razones de rendimiento, pueden producirse solicitudes HTTP mientras el host responde.</span><span class="sxs-lookup"><span data-stu-id="35eff-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="35eff-129">Esto significa que las cookies se pueden establecer y usar parte de una solicitud de navegación.</span><span class="sxs-lookup"><span data-stu-id="35eff-129">This means cookies can be set and used part of a request for the navigation.</span></span> <span data-ttu-id="35eff-130">Cancelación de la navegación a: no se admite la navegación en blanco o en el marco a srcdoc.</span><span class="sxs-lookup"><span data-stu-id="35eff-130">Cancellation for navigation to about:blank or frame navigation to srcdoc is not supported.</span></span> <span data-ttu-id="35eff-131">Dichos intentos serán ignorados.</span><span class="sxs-lookup"><span data-stu-id="35eff-131">Such attempts will be ignored.</span></span>

#### <span data-ttu-id="35eff-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="35eff-132">get_IsRedirected</span></span> 

<span data-ttu-id="35eff-133">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="35eff-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="35eff-134">[get_IsRedirected](#get_isredirected)de HRESULT público (bool \* IsRedirected)</span><span class="sxs-lookup"><span data-stu-id="35eff-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="35eff-135">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="35eff-135">get_IsUserInitiated</span></span> 

<span data-ttu-id="35eff-136">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="35eff-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="35eff-137">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="35eff-137">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="35eff-138">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="35eff-138">get_NavigationId</span></span> 

<span data-ttu-id="35eff-139">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="35eff-139">The ID of the navigation.</span></span>

> <span data-ttu-id="35eff-140">[get_NavigationId](#get_navigationid)(HRESULT) público (UINT64 \* NavigationId)</span><span class="sxs-lookup"><span data-stu-id="35eff-140">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigationId)</span></span>

#### <span data-ttu-id="35eff-141">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="35eff-141">get_RequestHeaders</span></span> 

<span data-ttu-id="35eff-142">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="35eff-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="35eff-143">[get_RequestHeaders](#get_requestheaders)(HRESULT) público ([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="35eff-143">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="35eff-144">Tenga en cuenta que no puede modificar los encabezados de la solicitud HTTP en un evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="35eff-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="35eff-145">get_Uri</span><span class="sxs-lookup"><span data-stu-id="35eff-145">get_Uri</span></span> 

<span data-ttu-id="35eff-146">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="35eff-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="35eff-147">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="35eff-147">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="35eff-148">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="35eff-148">put_Cancel</span></span> 

<span data-ttu-id="35eff-149">Establezca la propiedad cancelar.</span><span class="sxs-lookup"><span data-stu-id="35eff-149">Set the Cancel property.</span></span>

> <span data-ttu-id="35eff-150">[put_Cancel](#put_cancel)de HRESULT público (bool CANCEL)</span><span class="sxs-lookup"><span data-stu-id="35eff-150">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>


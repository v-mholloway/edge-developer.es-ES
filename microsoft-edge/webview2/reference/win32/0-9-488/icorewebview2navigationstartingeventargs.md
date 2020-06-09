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
ms.openlocfilehash: d56f40a9780313c79f421559eaf54750828542a5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697192"
---
# <span data-ttu-id="6487b-104">interfaz ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="6487b-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="6487b-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="6487b-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="6487b-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="6487b-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="6487b-107">Argumentos de evento para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="6487b-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="6487b-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="6487b-108">Summary</span></span>

 <span data-ttu-id="6487b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6487b-109">Members</span></span>                        | <span data-ttu-id="6487b-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6487b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6487b-111">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="6487b-111">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="6487b-112">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="6487b-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="6487b-113">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="6487b-113">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="6487b-114">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="6487b-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="6487b-115">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6487b-115">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="6487b-116">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="6487b-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="6487b-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="6487b-117">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="6487b-118">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="6487b-118">The ID of the navigation.</span></span>
[<span data-ttu-id="6487b-119">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="6487b-119">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="6487b-120">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="6487b-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="6487b-121">get_Uri</span><span class="sxs-lookup"><span data-stu-id="6487b-121">get_Uri</span></span>](#get_uri) | <span data-ttu-id="6487b-122">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="6487b-122">The uri of the requested navigation.</span></span>
[<span data-ttu-id="6487b-123">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="6487b-123">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="6487b-124">Establezca la propiedad cancelar.</span><span class="sxs-lookup"><span data-stu-id="6487b-124">Set the Cancel property.</span></span>

## <span data-ttu-id="6487b-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="6487b-125">Members</span></span>

#### <span data-ttu-id="6487b-126">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="6487b-126">get_Cancel</span></span> 

<span data-ttu-id="6487b-127">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="6487b-127">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="6487b-128">[get_Cancel](#get_cancel)de HRESULT público (bool \* CANCEL)</span><span class="sxs-lookup"><span data-stu-id="6487b-128">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="6487b-129">Si se establece, será como si la navegación nunca ocurriera y el contenido de la página actual permanecerá intacto.</span><span class="sxs-lookup"><span data-stu-id="6487b-129">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="6487b-130">Por razones de rendimiento, pueden producirse solicitudes HTTP mientras el host responde.</span><span class="sxs-lookup"><span data-stu-id="6487b-130">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="6487b-131">Esto significa que las cookies se pueden establecer y usar parte de una solicitud de navegación.</span><span class="sxs-lookup"><span data-stu-id="6487b-131">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="6487b-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="6487b-132">get_IsRedirected</span></span> 

<span data-ttu-id="6487b-133">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="6487b-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="6487b-134">[get_IsRedirected](#get_isredirected)de HRESULT público (bool \* IsRedirected)</span><span class="sxs-lookup"><span data-stu-id="6487b-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="6487b-135">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6487b-135">get_IsUserInitiated</span></span> 

<span data-ttu-id="6487b-136">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="6487b-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="6487b-137">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="6487b-137">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="6487b-138">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="6487b-138">get_NavigationId</span></span> 

<span data-ttu-id="6487b-139">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="6487b-139">The ID of the navigation.</span></span>

> <span data-ttu-id="6487b-140">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="6487b-140">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="6487b-141">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="6487b-141">get_RequestHeaders</span></span> 

<span data-ttu-id="6487b-142">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="6487b-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="6487b-143">[get_RequestHeaders](#get_requestheaders)(HRESULT) público ([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="6487b-143">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="6487b-144">Tenga en cuenta que no puede modificar los encabezados de la solicitud HTTP en un evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="6487b-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="6487b-145">get_Uri</span><span class="sxs-lookup"><span data-stu-id="6487b-145">get_Uri</span></span> 

<span data-ttu-id="6487b-146">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="6487b-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="6487b-147">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="6487b-147">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="6487b-148">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="6487b-148">put_Cancel</span></span> 

<span data-ttu-id="6487b-149">Establezca la propiedad cancelar.</span><span class="sxs-lookup"><span data-stu-id="6487b-149">Set the Cancel property.</span></span>

> <span data-ttu-id="6487b-150">[put_Cancel](#put_cancel)de HRESULT público (bool CANCEL)</span><span class="sxs-lookup"><span data-stu-id="6487b-150">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>


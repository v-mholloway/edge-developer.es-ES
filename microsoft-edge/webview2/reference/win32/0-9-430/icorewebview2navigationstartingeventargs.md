---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: b0b868b99d3f77679b3684a20e7744d7a22fd715
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655262"
---
# <span data-ttu-id="2825a-104">interfaz ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="2825a-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="2825a-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="2825a-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="2825a-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="2825a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="2825a-107">Argumentos de evento para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2825a-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="2825a-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="2825a-108">Summary</span></span>

 <span data-ttu-id="2825a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2825a-109">Members</span></span>                        | <span data-ttu-id="2825a-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2825a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2825a-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2825a-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="2825a-112">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="2825a-112">The uri of the requested navigation.</span></span>
[<span data-ttu-id="2825a-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="2825a-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="2825a-114">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="2825a-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="2825a-115">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="2825a-115">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="2825a-116">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="2825a-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="2825a-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="2825a-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="2825a-118">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="2825a-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="2825a-119">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="2825a-119">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="2825a-120">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="2825a-120">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="2825a-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="2825a-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="2825a-122">Establezca la propiedad cancelar.</span><span class="sxs-lookup"><span data-stu-id="2825a-122">Set the Cancel property.</span></span>
[<span data-ttu-id="2825a-123">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="2825a-123">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="2825a-124">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="2825a-124">The ID of the navigation.</span></span>

## <span data-ttu-id="2825a-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="2825a-125">Members</span></span>

#### <span data-ttu-id="2825a-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2825a-126">get_Uri</span></span> 

<span data-ttu-id="2825a-127">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="2825a-127">The uri of the requested navigation.</span></span>

> <span data-ttu-id="2825a-128">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="2825a-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="2825a-129">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="2825a-129">get_IsUserInitiated</span></span> 

<span data-ttu-id="2825a-130">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="2825a-130">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="2825a-131">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="2825a-131">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="2825a-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="2825a-132">get_IsRedirected</span></span> 

<span data-ttu-id="2825a-133">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="2825a-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="2825a-134">[get_IsRedirected](#get_isredirected)de HRESULT público (bool \* IsRedirected)</span><span class="sxs-lookup"><span data-stu-id="2825a-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="2825a-135">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="2825a-135">get_RequestHeaders</span></span> 

<span data-ttu-id="2825a-136">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="2825a-136">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="2825a-137">[get_RequestHeaders](#get_requestheaders)(HRESULT) público ([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="2825a-137">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="2825a-138">Tenga en cuenta que no puede modificar los encabezados de la solicitud HTTP en un evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="2825a-138">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="2825a-139">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="2825a-139">get_Cancel</span></span> 

<span data-ttu-id="2825a-140">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="2825a-140">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="2825a-141">[get_Cancel](#get_cancel)de HRESULT público (bool \* CANCEL)</span><span class="sxs-lookup"><span data-stu-id="2825a-141">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="2825a-142">Si se establece, será como si la navegación nunca ocurriera y el contenido de la página actual permanecerá intacto.</span><span class="sxs-lookup"><span data-stu-id="2825a-142">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="2825a-143">Por razones de rendimiento, pueden producirse solicitudes HTTP mientras el host responde.</span><span class="sxs-lookup"><span data-stu-id="2825a-143">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="2825a-144">Esto significa que las cookies se pueden establecer y usar parte de una solicitud de navegación.</span><span class="sxs-lookup"><span data-stu-id="2825a-144">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="2825a-145">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="2825a-145">put_Cancel</span></span> 

<span data-ttu-id="2825a-146">Establezca la propiedad cancelar.</span><span class="sxs-lookup"><span data-stu-id="2825a-146">Set the Cancel property.</span></span>

> <span data-ttu-id="2825a-147">[put_Cancel](#put_cancel)de HRESULT público (bool CANCEL)</span><span class="sxs-lookup"><span data-stu-id="2825a-147">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

#### <span data-ttu-id="2825a-148">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="2825a-148">get_NavigationId</span></span> 

<span data-ttu-id="2825a-149">IDENTIFICADOR de la navegación.</span><span class="sxs-lookup"><span data-stu-id="2825a-149">The ID of the navigation.</span></span>

> <span data-ttu-id="2825a-150">[get_NavigationId](#get_navigationid)de HRESULT público (UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="2825a-150">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>


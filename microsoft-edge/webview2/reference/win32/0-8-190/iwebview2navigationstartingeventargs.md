---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: ee6886e32b32f4da4bbdc04fe6e866210a76488b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655512"
---
# <span data-ttu-id="abc4e-104">interfaz IWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="abc4e-104">interface IWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="abc4e-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="abc4e-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="abc4e-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="abc4e-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="abc4e-107">Argumentos de evento para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="abc4e-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="abc4e-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="abc4e-108">Summary</span></span>

 <span data-ttu-id="abc4e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="abc4e-109">Members</span></span>                        | <span data-ttu-id="abc4e-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="abc4e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="abc4e-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="abc4e-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="abc4e-112">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="abc4e-112">The uri of the requested navigation.</span></span>
[<span data-ttu-id="abc4e-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="abc4e-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="abc4e-114">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="abc4e-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="abc4e-115">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="abc4e-115">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="abc4e-116">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="abc4e-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="abc4e-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="abc4e-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="abc4e-118">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="abc4e-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="abc4e-119">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="abc4e-119">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="abc4e-120">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="abc4e-120">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="abc4e-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="abc4e-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="abc4e-122">Establezca la propiedad cancelar.</span><span class="sxs-lookup"><span data-stu-id="abc4e-122">Set the Cancel property.</span></span>

## <span data-ttu-id="abc4e-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="abc4e-123">Members</span></span>

#### <span data-ttu-id="abc4e-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="abc4e-124">get_Uri</span></span> 

<span data-ttu-id="abc4e-125">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="abc4e-125">The uri of the requested navigation.</span></span>

> <span data-ttu-id="abc4e-126">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="abc4e-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="abc4e-127">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="abc4e-127">get_IsUserInitiated</span></span> 

<span data-ttu-id="abc4e-128">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="abc4e-128">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="abc4e-129">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="abc4e-129">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="abc4e-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="abc4e-130">get_IsRedirected</span></span> 

<span data-ttu-id="abc4e-131">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="abc4e-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="abc4e-132">[get_IsRedirected](#get_isredirected)de HRESULT público (bool \* IsRedirected)</span><span class="sxs-lookup"><span data-stu-id="abc4e-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="abc4e-133">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="abc4e-133">get_RequestHeaders</span></span> 

<span data-ttu-id="abc4e-134">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="abc4e-134">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="abc4e-135">[get_RequestHeaders](#get_requestheaders)(HRESULT) público ([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="abc4e-135">public HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="abc4e-136">Tenga en cuenta que no puede modificar los encabezados de la solicitud HTTP en un evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="abc4e-136">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="abc4e-137">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="abc4e-137">get_Cancel</span></span> 

<span data-ttu-id="abc4e-138">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="abc4e-138">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="abc4e-139">[get_Cancel](#get_cancel)de HRESULT público (bool \* CANCEL)</span><span class="sxs-lookup"><span data-stu-id="abc4e-139">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="abc4e-140">Si se establece, será como si la navegación nunca ocurriera y el contenido de la página actual permanecerá intacto.</span><span class="sxs-lookup"><span data-stu-id="abc4e-140">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="abc4e-141">Por razones de rendimiento, pueden producirse solicitudes HTTP mientras el host responde.</span><span class="sxs-lookup"><span data-stu-id="abc4e-141">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="abc4e-142">Esto significa que las cookies se pueden establecer y usar parte de una solicitud de navegación.</span><span class="sxs-lookup"><span data-stu-id="abc4e-142">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="abc4e-143">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="abc4e-143">put_Cancel</span></span> 

<span data-ttu-id="abc4e-144">Establezca la propiedad cancelar.</span><span class="sxs-lookup"><span data-stu-id="abc4e-144">Set the Cancel property.</span></span>

> <span data-ttu-id="abc4e-145">[put_Cancel](#put_cancel)de HRESULT público (bool CANCEL)</span><span class="sxs-lookup"><span data-stu-id="abc4e-145">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>


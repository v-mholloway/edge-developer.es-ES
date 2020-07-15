---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 8bc625d12cc3b3ebe06970fd282dd8f60bcabd22
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878403"
---
# <span data-ttu-id="44283-104">0.8.355: IWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="44283-104">0.8.355 - interface IWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="44283-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="44283-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="44283-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="44283-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="44283-107">Argumentos de evento para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="44283-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="44283-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="44283-108">Summary</span></span>

 <span data-ttu-id="44283-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="44283-109">Members</span></span>                        | <span data-ttu-id="44283-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="44283-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="44283-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="44283-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="44283-112">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="44283-112">The uri of the requested navigation.</span></span>
[<span data-ttu-id="44283-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="44283-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="44283-114">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="44283-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="44283-115">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="44283-115">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="44283-116">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="44283-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="44283-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="44283-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="44283-118">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="44283-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="44283-119">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="44283-119">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="44283-120">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="44283-120">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="44283-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="44283-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="44283-122">Establezca la propiedad cancelar.</span><span class="sxs-lookup"><span data-stu-id="44283-122">Set the Cancel property.</span></span>

## <span data-ttu-id="44283-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="44283-123">Members</span></span>

#### <span data-ttu-id="44283-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="44283-124">get_Uri</span></span> 

<span data-ttu-id="44283-125">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="44283-125">The uri of the requested navigation.</span></span>

> <span data-ttu-id="44283-126">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="44283-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="44283-127">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="44283-127">get_IsUserInitiated</span></span> 

<span data-ttu-id="44283-128">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="44283-128">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="44283-129">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="44283-129">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="44283-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="44283-130">get_IsRedirected</span></span> 

<span data-ttu-id="44283-131">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="44283-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="44283-132">[get_IsRedirected](#get_isredirected)de HRESULT público (bool \* IsRedirected)</span><span class="sxs-lookup"><span data-stu-id="44283-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="44283-133">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="44283-133">get_RequestHeaders</span></span> 

<span data-ttu-id="44283-134">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="44283-134">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="44283-135">[get_RequestHeaders](#get_requestheaders)(HRESULT) público ([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="44283-135">public HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="44283-136">Tenga en cuenta que no puede modificar los encabezados de la solicitud HTTP en un evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="44283-136">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="44283-137">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="44283-137">get_Cancel</span></span> 

<span data-ttu-id="44283-138">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="44283-138">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="44283-139">[get_Cancel](#get_cancel)de HRESULT público (bool \* CANCEL)</span><span class="sxs-lookup"><span data-stu-id="44283-139">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="44283-140">Si se establece, será como si la navegación nunca ocurriera y el contenido de la página actual permanecerá intacto.</span><span class="sxs-lookup"><span data-stu-id="44283-140">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="44283-141">Por razones de rendimiento, pueden producirse solicitudes HTTP mientras el host responde.</span><span class="sxs-lookup"><span data-stu-id="44283-141">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="44283-142">Esto significa que las cookies se pueden establecer y usar parte de una solicitud de navegación.</span><span class="sxs-lookup"><span data-stu-id="44283-142">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="44283-143">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="44283-143">put_Cancel</span></span> 

<span data-ttu-id="44283-144">Establezca la propiedad cancelar.</span><span class="sxs-lookup"><span data-stu-id="44283-144">Set the Cancel property.</span></span>

> <span data-ttu-id="44283-145">[put_Cancel](#put_cancel)de HRESULT público (bool CANCEL)</span><span class="sxs-lookup"><span data-stu-id="44283-145">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>


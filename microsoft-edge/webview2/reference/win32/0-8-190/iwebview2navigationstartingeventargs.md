---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 5996f0eff4db17530750eb39c7693ea0f8496a4d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885901"
---
# <span data-ttu-id="3c85c-104">0.8.355: IWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="3c85c-104">0.8.355 - interface IWebView2NavigationStartingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="3c85c-105">Argumentos de evento para el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="3c85c-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="3c85c-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="3c85c-106">Summary</span></span>

 <span data-ttu-id="3c85c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="3c85c-107">Members</span></span>                        | <span data-ttu-id="3c85c-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="3c85c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3c85c-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="3c85c-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="3c85c-110">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="3c85c-110">The uri of the requested navigation.</span></span>
[<span data-ttu-id="3c85c-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="3c85c-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="3c85c-112">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="3c85c-112">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="3c85c-113">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="3c85c-113">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="3c85c-114">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="3c85c-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="3c85c-115">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="3c85c-115">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="3c85c-116">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="3c85c-116">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="3c85c-117">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="3c85c-117">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="3c85c-118">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="3c85c-118">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="3c85c-119">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="3c85c-119">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="3c85c-120">Establezca la propiedad cancelar.</span><span class="sxs-lookup"><span data-stu-id="3c85c-120">Set the Cancel property.</span></span>

## <span data-ttu-id="3c85c-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="3c85c-121">Members</span></span>

#### <span data-ttu-id="3c85c-122">get_Uri</span><span class="sxs-lookup"><span data-stu-id="3c85c-122">get_Uri</span></span> 

<span data-ttu-id="3c85c-123">Identificador URI de la navegación solicitada.</span><span class="sxs-lookup"><span data-stu-id="3c85c-123">The uri of the requested navigation.</span></span>

> <span data-ttu-id="3c85c-124">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="3c85c-124">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="3c85c-125">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="3c85c-125">get_IsUserInitiated</span></span> 

<span data-ttu-id="3c85c-126">True cuando se inició la navegación mediante un gesto de usuario, en lugar de navegar mediante programación.</span><span class="sxs-lookup"><span data-stu-id="3c85c-126">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="3c85c-127">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="3c85c-127">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="3c85c-128">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="3c85c-128">get_IsRedirected</span></span> 

<span data-ttu-id="3c85c-129">True cuando se redirige la navegación.</span><span class="sxs-lookup"><span data-stu-id="3c85c-129">True when the navigation is redirected.</span></span>

> <span data-ttu-id="3c85c-130">[get_IsRedirected](#get_isredirected)de HRESULT público (bool \* IsRedirected)</span><span class="sxs-lookup"><span data-stu-id="3c85c-130">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="3c85c-131">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="3c85c-131">get_RequestHeaders</span></span> 

<span data-ttu-id="3c85c-132">Los encabezados de la solicitud HTTP para la navegación.</span><span class="sxs-lookup"><span data-stu-id="3c85c-132">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="3c85c-133">[get_RequestHeaders](#get_requestheaders)(HRESULT) público ([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="3c85c-133">public HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="3c85c-134">Tenga en cuenta que no puede modificar los encabezados de la solicitud HTTP en un evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="3c85c-134">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="3c85c-135">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="3c85c-135">get_Cancel</span></span> 

<span data-ttu-id="3c85c-136">El anfitrión puede establecer esta marca para cancelar la navegación.</span><span class="sxs-lookup"><span data-stu-id="3c85c-136">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="3c85c-137">[get_Cancel](#get_cancel)de HRESULT público (bool \* CANCEL)</span><span class="sxs-lookup"><span data-stu-id="3c85c-137">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="3c85c-138">Si se establece, será como si la navegación nunca ocurriera y el contenido de la página actual permanecerá intacto.</span><span class="sxs-lookup"><span data-stu-id="3c85c-138">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="3c85c-139">Por razones de rendimiento, pueden producirse solicitudes HTTP mientras el host responde.</span><span class="sxs-lookup"><span data-stu-id="3c85c-139">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="3c85c-140">Esto significa que las cookies se pueden establecer y usar parte de una solicitud de navegación.</span><span class="sxs-lookup"><span data-stu-id="3c85c-140">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="3c85c-141">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="3c85c-141">put_Cancel</span></span> 

<span data-ttu-id="3c85c-142">Establezca la propiedad cancelar.</span><span class="sxs-lookup"><span data-stu-id="3c85c-142">Set the Cancel property.</span></span>

> <span data-ttu-id="3c85c-143">[put_Cancel](#put_cancel)de HRESULT público (bool CANCEL)</span><span class="sxs-lookup"><span data-stu-id="3c85c-143">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>


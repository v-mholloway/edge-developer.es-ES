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
ms.openlocfilehash: 743cd0fc6a1a9b21605dfa427273a7a457f806d7
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697612"
---
# <span data-ttu-id="e0a48-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e0a48-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="e0a48-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="e0a48-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="e0a48-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="e0a48-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="e0a48-107">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="e0a48-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="e0a48-108">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="e0a48-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="e0a48-109">Argumentos de evento para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="e0a48-109">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="e0a48-110">Resumen</span><span class="sxs-lookup"><span data-stu-id="e0a48-110">Summary</span></span>

 <span data-ttu-id="e0a48-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e0a48-111">Members</span></span>                        | <span data-ttu-id="e0a48-112">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e0a48-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e0a48-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="e0a48-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="e0a48-114">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="e0a48-114">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="e0a48-115">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="e0a48-115">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="e0a48-116">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="e0a48-116">The type of the permission that is requested.</span></span>
[<span data-ttu-id="e0a48-117">Estado</span><span class="sxs-lookup"><span data-stu-id="e0a48-117">State</span></span>](#state) | <span data-ttu-id="e0a48-118">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="e0a48-118">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="e0a48-119">URI</span><span class="sxs-lookup"><span data-stu-id="e0a48-119">Uri</span></span>](#uri) | <span data-ttu-id="e0a48-120">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="e0a48-120">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="e0a48-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e0a48-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="e0a48-122">Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="e0a48-122">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="e0a48-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="e0a48-123">Members</span></span>

#### <span data-ttu-id="e0a48-124">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="e0a48-124">IsUserInitiated</span></span> 

<span data-ttu-id="e0a48-125">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="e0a48-125">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="e0a48-126">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="e0a48-126">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="e0a48-127">Tenga en cuenta que el que se inicia mediante un movimiento de usuario no significa que el usuario vaya a tener acceso al recurso asociado.</span><span class="sxs-lookup"><span data-stu-id="e0a48-127">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="e0a48-128">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="e0a48-128">PermissionKind</span></span> 

<span data-ttu-id="e0a48-129">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="e0a48-129">The type of the permission that is requested.</span></span>

> <span data-ttu-id="e0a48-130">CoreWebView2PermissionKind pública [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="e0a48-130">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="e0a48-131">Estado</span><span class="sxs-lookup"><span data-stu-id="e0a48-131">State</span></span> 

<span data-ttu-id="e0a48-132">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="e0a48-132">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="e0a48-133">[Estado](#state) de CoreWebView2PermissionState público</span><span class="sxs-lookup"><span data-stu-id="e0a48-133">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="e0a48-134">Si se concede la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0a48-134">whether the request is granted.</span></span>

<span data-ttu-id="e0a48-135">El valor predeterminado es CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="e0a48-135">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="e0a48-136">URI</span><span class="sxs-lookup"><span data-stu-id="e0a48-136">Uri</span></span> 

<span data-ttu-id="e0a48-137">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="e0a48-137">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="e0a48-138">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="e0a48-138">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="e0a48-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e0a48-139">GetDeferral</span></span> 

<span data-ttu-id="e0a48-140">Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="e0a48-140">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="e0a48-141">Public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="e0a48-141">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="e0a48-142">El desarrollador puede usar el objeto de aplazamiento para tomar la decisión de permiso más adelante.</span><span class="sxs-lookup"><span data-stu-id="e0a48-142">Developer can use the deferral object to make the permission decision at a later time.</span></span>


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
ms.openlocfilehash: 58d87d1815b81969c4424eacfcec26ffe425192e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699313"
---
# <span data-ttu-id="c2de6-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c2de6-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

<span data-ttu-id="c2de6-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="c2de6-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="c2de6-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="c2de6-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="c2de6-107">Argumentos de evento para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="c2de6-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="c2de6-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="c2de6-108">Summary</span></span>

 <span data-ttu-id="c2de6-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2de6-109">Members</span></span>                        | <span data-ttu-id="c2de6-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="c2de6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c2de6-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c2de6-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="c2de6-112">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="c2de6-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="c2de6-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="c2de6-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="c2de6-114">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="c2de6-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="c2de6-115">Estado</span><span class="sxs-lookup"><span data-stu-id="c2de6-115">State</span></span>](#state) | <span data-ttu-id="c2de6-116">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="c2de6-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="c2de6-117">URI</span><span class="sxs-lookup"><span data-stu-id="c2de6-117">Uri</span></span>](#uri) | <span data-ttu-id="c2de6-118">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="c2de6-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="c2de6-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c2de6-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="c2de6-120">Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="c2de6-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="c2de6-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2de6-121">Members</span></span>

#### <span data-ttu-id="c2de6-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c2de6-122">IsUserInitiated</span></span> 

<span data-ttu-id="c2de6-123">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="c2de6-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="c2de6-124">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="c2de6-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="c2de6-125">Tenga en cuenta que el que se inicia mediante un movimiento de usuario no significa que el usuario vaya a tener acceso al recurso asociado.</span><span class="sxs-lookup"><span data-stu-id="c2de6-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="c2de6-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="c2de6-126">PermissionKind</span></span> 

<span data-ttu-id="c2de6-127">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="c2de6-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="c2de6-128">CoreWebView2PermissionKind pública [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="c2de6-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="c2de6-129">Estado</span><span class="sxs-lookup"><span data-stu-id="c2de6-129">State</span></span> 

<span data-ttu-id="c2de6-130">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="c2de6-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="c2de6-131">[Estado](#state) de CoreWebView2PermissionState público</span><span class="sxs-lookup"><span data-stu-id="c2de6-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="c2de6-132">Si se concede la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c2de6-132">whether the request is granted.</span></span>

<span data-ttu-id="c2de6-133">El valor predeterminado es CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="c2de6-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="c2de6-134">URI</span><span class="sxs-lookup"><span data-stu-id="c2de6-134">Uri</span></span> 

<span data-ttu-id="c2de6-135">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="c2de6-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="c2de6-136">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="c2de6-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="c2de6-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c2de6-137">GetDeferral</span></span> 

<span data-ttu-id="c2de6-138">Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="c2de6-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="c2de6-139">Public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="c2de6-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="c2de6-140">El desarrollador puede usar el objeto de aplazamiento para tomar la decisión de permiso más adelante.</span><span class="sxs-lookup"><span data-stu-id="c2de6-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>


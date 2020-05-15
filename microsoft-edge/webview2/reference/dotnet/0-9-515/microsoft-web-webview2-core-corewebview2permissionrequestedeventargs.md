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
ms.openlocfilehash: 5aeeebfc3d8434c096e6946e5161437809f207d3
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655095"
---
# <span data-ttu-id="6a168-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6a168-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

<span data-ttu-id="6a168-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="6a168-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="6a168-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="6a168-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="6a168-107">Argumentos de evento para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="6a168-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="6a168-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="6a168-108">Summary</span></span>

 <span data-ttu-id="6a168-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6a168-109">Members</span></span>                        | <span data-ttu-id="6a168-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6a168-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6a168-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6a168-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="6a168-112">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="6a168-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="6a168-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="6a168-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="6a168-114">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="6a168-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="6a168-115">Estado</span><span class="sxs-lookup"><span data-stu-id="6a168-115">State</span></span>](#state) | <span data-ttu-id="6a168-116">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="6a168-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="6a168-117">URI</span><span class="sxs-lookup"><span data-stu-id="6a168-117">Uri</span></span>](#uri) | <span data-ttu-id="6a168-118">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="6a168-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="6a168-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="6a168-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="6a168-120">Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="6a168-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="6a168-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="6a168-121">Members</span></span>

#### <span data-ttu-id="6a168-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6a168-122">IsUserInitiated</span></span> 

<span data-ttu-id="6a168-123">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="6a168-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="6a168-124">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="6a168-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="6a168-125">Tenga en cuenta que el que se inicia mediante un movimiento de usuario no significa que el usuario vaya a tener acceso al recurso asociado.</span><span class="sxs-lookup"><span data-stu-id="6a168-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="6a168-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="6a168-126">PermissionKind</span></span> 

<span data-ttu-id="6a168-127">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="6a168-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="6a168-128">CoreWebView2PermissionKind pública [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="6a168-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="6a168-129">Estado</span><span class="sxs-lookup"><span data-stu-id="6a168-129">State</span></span> 

<span data-ttu-id="6a168-130">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="6a168-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="6a168-131">[Estado](#state) de CoreWebView2PermissionState público</span><span class="sxs-lookup"><span data-stu-id="6a168-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="6a168-132">Si se concede la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6a168-132">whether the request is granted.</span></span>

<span data-ttu-id="6a168-133">El valor predeterminado es CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="6a168-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="6a168-134">URI</span><span class="sxs-lookup"><span data-stu-id="6a168-134">Uri</span></span> 

<span data-ttu-id="6a168-135">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="6a168-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="6a168-136">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="6a168-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="6a168-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="6a168-137">GetDeferral</span></span> 

<span data-ttu-id="6a168-138">Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="6a168-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="6a168-139">Public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="6a168-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="6a168-140">El desarrollador puede usar el objeto de aplazamiento para tomar la decisión de permiso más adelante.</span><span class="sxs-lookup"><span data-stu-id="6a168-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>


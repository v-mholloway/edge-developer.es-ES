---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: 2ad85879ccf69ccecef355ea07d311cc5a23de11
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010944"
---
# <span data-ttu-id="2e68e-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs (clase)</span><span class="sxs-lookup"><span data-stu-id="2e68e-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="2e68e-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="2e68e-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="2e68e-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="2e68e-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="2e68e-107">Argumentos de evento para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="2e68e-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="2e68e-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="2e68e-108">Summary</span></span>

 <span data-ttu-id="2e68e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2e68e-109">Members</span></span>                        | <span data-ttu-id="2e68e-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2e68e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2e68e-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="2e68e-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="2e68e-112">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="2e68e-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="2e68e-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="2e68e-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="2e68e-114">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="2e68e-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="2e68e-115">Estado</span><span class="sxs-lookup"><span data-stu-id="2e68e-115">State</span></span>](#state) | <span data-ttu-id="2e68e-116">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="2e68e-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="2e68e-117">URI</span><span class="sxs-lookup"><span data-stu-id="2e68e-117">Uri</span></span>](#uri) | <span data-ttu-id="2e68e-118">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="2e68e-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="2e68e-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2e68e-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="2e68e-120">Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="2e68e-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="2e68e-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="2e68e-121">Members</span></span>

#### <span data-ttu-id="2e68e-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="2e68e-122">IsUserInitiated</span></span> 

<span data-ttu-id="2e68e-123">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="2e68e-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="2e68e-124">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="2e68e-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="2e68e-125">Tenga en cuenta que el que se inicia mediante un movimiento de usuario no significa que el usuario vaya a tener acceso al recurso asociado.</span><span class="sxs-lookup"><span data-stu-id="2e68e-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="2e68e-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="2e68e-126">PermissionKind</span></span> 

<span data-ttu-id="2e68e-127">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="2e68e-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="2e68e-128">CoreWebView2PermissionKind pública [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="2e68e-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="2e68e-129">Estado</span><span class="sxs-lookup"><span data-stu-id="2e68e-129">State</span></span> 

<span data-ttu-id="2e68e-130">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="2e68e-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="2e68e-131">[Estado](#state) de CoreWebView2PermissionState público</span><span class="sxs-lookup"><span data-stu-id="2e68e-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="2e68e-132">Si se concede la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2e68e-132">whether the request is granted.</span></span>

<span data-ttu-id="2e68e-133">El valor predeterminado es CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="2e68e-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="2e68e-134">URI</span><span class="sxs-lookup"><span data-stu-id="2e68e-134">Uri</span></span> 

<span data-ttu-id="2e68e-135">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="2e68e-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="2e68e-136">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="2e68e-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="2e68e-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2e68e-137">GetDeferral</span></span> 

<span data-ttu-id="2e68e-138">Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="2e68e-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="2e68e-139">Public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="2e68e-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="2e68e-140">El desarrollador puede usar el objeto de aplazamiento para tomar la decisión de permiso más adelante.</span><span class="sxs-lookup"><span data-stu-id="2e68e-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>


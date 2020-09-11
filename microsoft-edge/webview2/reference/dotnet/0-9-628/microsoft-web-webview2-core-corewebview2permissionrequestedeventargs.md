---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: 87993559d4d70daef84cbd86a2305f09cc017aa9
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012641"
---
# <span data-ttu-id="cac1b-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="cac1b-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

<span data-ttu-id="cac1b-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="cac1b-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="cac1b-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="cac1b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="cac1b-107">Argumentos de evento para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="cac1b-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="cac1b-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="cac1b-108">Summary</span></span>

 <span data-ttu-id="cac1b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="cac1b-109">Members</span></span>                        | <span data-ttu-id="cac1b-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="cac1b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cac1b-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="cac1b-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="cac1b-112">True cuando se inició la solicitud de nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con target.</span><span class="sxs-lookup"><span data-stu-id="cac1b-112">True when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="cac1b-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="cac1b-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="cac1b-114">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="cac1b-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="cac1b-115">Estado</span><span class="sxs-lookup"><span data-stu-id="cac1b-115">State</span></span>](#state) | <span data-ttu-id="cac1b-116">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="cac1b-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="cac1b-117">URI</span><span class="sxs-lookup"><span data-stu-id="cac1b-117">Uri</span></span>](#uri) | <span data-ttu-id="cac1b-118">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="cac1b-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="cac1b-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="cac1b-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="cac1b-120">Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="cac1b-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="cac1b-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="cac1b-121">Members</span></span>

#### <span data-ttu-id="cac1b-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="cac1b-122">IsUserInitiated</span></span> 

<span data-ttu-id="cac1b-123">True cuando se inició la solicitud de nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con target.</span><span class="sxs-lookup"><span data-stu-id="cac1b-123">True when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="cac1b-124">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="cac1b-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="cac1b-125">El bloqueador de ventanas emergentes de Edge está deshabilitado para WebView, por lo que la aplicación puede usar esta marca para bloquear los mensajes emergentes no iniciados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="cac1b-125">The Edge popup blocker is disabled for WebView so the app can use this flag to block non-user initiated popups.</span></span>

#### <span data-ttu-id="cac1b-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="cac1b-126">PermissionKind</span></span> 

<span data-ttu-id="cac1b-127">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="cac1b-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="cac1b-128">CoreWebView2PermissionKind pública [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="cac1b-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="cac1b-129">Estado</span><span class="sxs-lookup"><span data-stu-id="cac1b-129">State</span></span> 

<span data-ttu-id="cac1b-130">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="cac1b-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="cac1b-131">[Estado](#state) de CoreWebView2PermissionState público</span><span class="sxs-lookup"><span data-stu-id="cac1b-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="cac1b-132">Si se concede la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cac1b-132">whether the request is granted.</span></span>

<span data-ttu-id="cac1b-133">El valor predeterminado es CoreWebView2PermissionState. default.</span><span class="sxs-lookup"><span data-stu-id="cac1b-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="cac1b-134">URI</span><span class="sxs-lookup"><span data-stu-id="cac1b-134">Uri</span></span> 

<span data-ttu-id="cac1b-135">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="cac1b-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="cac1b-136">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="cac1b-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="cac1b-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="cac1b-137">GetDeferral</span></span> 

<span data-ttu-id="cac1b-138">Se puede llamar a GetDeferral para que devuelva un objeto CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="cac1b-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="cac1b-139">Public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="cac1b-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="cac1b-140">El desarrollador puede usar el objeto de aplazamiento para tomar la decisión de permiso más adelante.</span><span class="sxs-lookup"><span data-stu-id="cac1b-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>


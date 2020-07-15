---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 88f5008dbc9a4ebfccfe96299899a2474ecc6d95
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880412"
---
# <span data-ttu-id="b3fdc-104">0.9.515: ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b3fdc-104">0.9.515 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="b3fdc-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="b3fdc-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="b3fdc-107">Argumentos de evento para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="b3fdc-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="b3fdc-108">Summary</span></span>

 <span data-ttu-id="b3fdc-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b3fdc-109">Members</span></span>                        | <span data-ttu-id="b3fdc-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b3fdc-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b3fdc-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="b3fdc-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="b3fdc-112">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="b3fdc-113">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="b3fdc-113">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="b3fdc-114">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="b3fdc-115">get_State</span><span class="sxs-lookup"><span data-stu-id="b3fdc-115">get_State</span></span>](#get_state) | <span data-ttu-id="b3fdc-116">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="b3fdc-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="b3fdc-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b3fdc-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="b3fdc-118">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="b3fdc-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b3fdc-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="b3fdc-120">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="b3fdc-120">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="b3fdc-121">put_State</span><span class="sxs-lookup"><span data-stu-id="b3fdc-121">put_State</span></span>](#put_state) | <span data-ttu-id="b3fdc-122">Establezca la propiedad State.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-122">Set the State property.</span></span>

## <span data-ttu-id="b3fdc-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="b3fdc-123">Members</span></span>

#### <span data-ttu-id="b3fdc-124">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="b3fdc-124">get_IsUserInitiated</span></span> 

<span data-ttu-id="b3fdc-125">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-125">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="b3fdc-126">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="b3fdc-126">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="b3fdc-127">Tenga en cuenta que el que se inicia mediante un movimiento de usuario no significa que el usuario vaya a tener acceso al recurso asociado.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-127">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="b3fdc-128">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="b3fdc-128">get_PermissionKind</span></span> 

<span data-ttu-id="b3fdc-129">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-129">The type of the permission that is requested.</span></span>

> <span data-ttu-id="b3fdc-130">[get_PermissionKind](#get_permissionkind)de HRESULT público (valor COREWEBVIEW2_PERMISSION_KIND \*)</span><span class="sxs-lookup"><span data-stu-id="b3fdc-130">public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="b3fdc-131">get_State</span><span class="sxs-lookup"><span data-stu-id="b3fdc-131">get_State</span></span> 

<span data-ttu-id="b3fdc-132">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="b3fdc-132">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="b3fdc-133">[get_State](#get_state)de HRESULT público (valor COREWEBVIEW2_PERMISSION_STATE \*)</span><span class="sxs-lookup"><span data-stu-id="b3fdc-133">public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="b3fdc-134">Si se concede la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-134">whether the request is granted.</span></span> <span data-ttu-id="b3fdc-135">El valor predeterminado es COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-135">Default value is COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="b3fdc-136">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b3fdc-136">get_Uri</span></span> 

<span data-ttu-id="b3fdc-137">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-137">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="b3fdc-138">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="b3fdc-138">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="b3fdc-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b3fdc-139">GetDeferral</span></span> 

<span data-ttu-id="b3fdc-140">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="b3fdc-140">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="b3fdc-141">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="b3fdc-141">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="b3fdc-142">El desarrollador puede usar el objeto de aplazamiento para tomar la decisión de permiso más adelante.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-142">Developer can use the deferral object to make the permission decision at a later time.</span></span>

#### <span data-ttu-id="b3fdc-143">put_State</span><span class="sxs-lookup"><span data-stu-id="b3fdc-143">put_State</span></span> 

<span data-ttu-id="b3fdc-144">Establezca la propiedad State.</span><span class="sxs-lookup"><span data-stu-id="b3fdc-144">Set the State property.</span></span>

> <span data-ttu-id="b3fdc-145">[put_State](#put_state)de HRESULT público (valor de COREWEBVIEW2_PERMISSION_STATE)</span><span class="sxs-lookup"><span data-stu-id="b3fdc-145">public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE value)</span></span>


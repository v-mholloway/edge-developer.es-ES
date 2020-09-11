---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: 4abb6fb058765a05ebb32fe97474348c4aebde12
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010036"
---
# <span data-ttu-id="6aec7-104">0.9.579: ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6aec7-104">0.9.579 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="6aec7-105">Argumentos de evento para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="6aec7-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="6aec7-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="6aec7-106">Summary</span></span>

 <span data-ttu-id="6aec7-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6aec7-107">Members</span></span>                        | <span data-ttu-id="6aec7-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6aec7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6aec7-109">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6aec7-109">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="6aec7-110">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="6aec7-110">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="6aec7-111">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="6aec7-111">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="6aec7-112">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="6aec7-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="6aec7-113">get_State</span><span class="sxs-lookup"><span data-stu-id="6aec7-113">get_State</span></span>](#get_state) | <span data-ttu-id="6aec7-114">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="6aec7-114">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="6aec7-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="6aec7-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="6aec7-116">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="6aec7-116">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="6aec7-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="6aec7-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="6aec7-118">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="6aec7-118">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="6aec7-119">put_State</span><span class="sxs-lookup"><span data-stu-id="6aec7-119">put_State</span></span>](#put_state) | <span data-ttu-id="6aec7-120">Establezca la propiedad State.</span><span class="sxs-lookup"><span data-stu-id="6aec7-120">Set the State property.</span></span>

## <span data-ttu-id="6aec7-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="6aec7-121">Members</span></span>

#### <span data-ttu-id="6aec7-122">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6aec7-122">get_IsUserInitiated</span></span> 

<span data-ttu-id="6aec7-123">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="6aec7-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="6aec7-124">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="6aec7-124">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="6aec7-125">Tenga en cuenta que el que se inicia mediante un movimiento de usuario no significa que el usuario vaya a tener acceso al recurso asociado.</span><span class="sxs-lookup"><span data-stu-id="6aec7-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="6aec7-126">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="6aec7-126">get_PermissionKind</span></span> 

<span data-ttu-id="6aec7-127">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="6aec7-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="6aec7-128">[get_PermissionKind](#get_permissionkind)de HRESULT público (valor COREWEBVIEW2_PERMISSION_KIND \*)</span><span class="sxs-lookup"><span data-stu-id="6aec7-128">public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="6aec7-129">get_State</span><span class="sxs-lookup"><span data-stu-id="6aec7-129">get_State</span></span> 

<span data-ttu-id="6aec7-130">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="6aec7-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="6aec7-131">[get_State](#get_state)de HRESULT público (valor COREWEBVIEW2_PERMISSION_STATE \*)</span><span class="sxs-lookup"><span data-stu-id="6aec7-131">public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="6aec7-132">Si se concede la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6aec7-132">whether the request is granted.</span></span> <span data-ttu-id="6aec7-133">El valor predeterminado es COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="6aec7-133">Default value is COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="6aec7-134">get_Uri</span><span class="sxs-lookup"><span data-stu-id="6aec7-134">get_Uri</span></span> 

<span data-ttu-id="6aec7-135">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="6aec7-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="6aec7-136">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="6aec7-136">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="6aec7-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="6aec7-137">GetDeferral</span></span> 

<span data-ttu-id="6aec7-138">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="6aec7-138">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="6aec7-139">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="6aec7-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="6aec7-140">El desarrollador puede usar el objeto de aplazamiento para tomar la decisión de permiso más adelante.</span><span class="sxs-lookup"><span data-stu-id="6aec7-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

#### <span data-ttu-id="6aec7-141">put_State</span><span class="sxs-lookup"><span data-stu-id="6aec7-141">put_State</span></span> 

<span data-ttu-id="6aec7-142">Establezca la propiedad State.</span><span class="sxs-lookup"><span data-stu-id="6aec7-142">Set the State property.</span></span>

> <span data-ttu-id="6aec7-143">[put_State](#put_state)de HRESULT público (valor de COREWEBVIEW2_PERMISSION_STATE)</span><span class="sxs-lookup"><span data-stu-id="6aec7-143">public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE value)</span></span>


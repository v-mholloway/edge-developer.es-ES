---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 75f88a08f5a94df85a471658704fcd77a5926417
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877794"
---
# <span data-ttu-id="41a11-104">0.9.430: ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="41a11-104">0.9.430 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="41a11-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="41a11-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="41a11-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="41a11-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="41a11-107">Argumentos de evento para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="41a11-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="41a11-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="41a11-108">Summary</span></span>

 <span data-ttu-id="41a11-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="41a11-109">Members</span></span>                        | <span data-ttu-id="41a11-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="41a11-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="41a11-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="41a11-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="41a11-112">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="41a11-112">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="41a11-113">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="41a11-113">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="41a11-114">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="41a11-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="41a11-115">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="41a11-115">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="41a11-116">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="41a11-116">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="41a11-117">get_State</span><span class="sxs-lookup"><span data-stu-id="41a11-117">get_State</span></span>](#get_state) | <span data-ttu-id="41a11-118">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="41a11-118">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="41a11-119">put_State</span><span class="sxs-lookup"><span data-stu-id="41a11-119">put_State</span></span>](#put_state) | <span data-ttu-id="41a11-120">Establezca la propiedad State.</span><span class="sxs-lookup"><span data-stu-id="41a11-120">Set the State property.</span></span>
[<span data-ttu-id="41a11-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="41a11-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="41a11-122">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="41a11-122">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="41a11-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="41a11-123">Members</span></span>

#### <span data-ttu-id="41a11-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="41a11-124">get_Uri</span></span> 

<span data-ttu-id="41a11-125">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="41a11-125">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="41a11-126">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="41a11-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="41a11-127">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="41a11-127">get_PermissionKind</span></span> 

<span data-ttu-id="41a11-128">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="41a11-128">The type of the permission that is requested.</span></span>

> <span data-ttu-id="41a11-129">[get_PermissionKind](#get_permissionkind)de HRESULT público (valor CORE_WEBVIEW2_PERMISSION_KIND \*)</span><span class="sxs-lookup"><span data-stu-id="41a11-129">public HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="41a11-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="41a11-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="41a11-131">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="41a11-131">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="41a11-132">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="41a11-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="41a11-133">Tenga en cuenta que el que se inicia mediante un movimiento de usuario no significa que el usuario vaya a tener acceso al recurso asociado.</span><span class="sxs-lookup"><span data-stu-id="41a11-133">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="41a11-134">get_State</span><span class="sxs-lookup"><span data-stu-id="41a11-134">get_State</span></span> 

<span data-ttu-id="41a11-135">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="41a11-135">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="41a11-136">[get_State](#get_state)de HRESULT público (valor CORE_WEBVIEW2_PERMISSION_STATE \*)</span><span class="sxs-lookup"><span data-stu-id="41a11-136">public HRESULT [get_State](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="41a11-137">Si se concede la solicitud.</span><span class="sxs-lookup"><span data-stu-id="41a11-137">whether the request is granted.</span></span> <span data-ttu-id="41a11-138">El valor predeterminado es CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="41a11-138">Default value is CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="41a11-139">put_State</span><span class="sxs-lookup"><span data-stu-id="41a11-139">put_State</span></span> 

<span data-ttu-id="41a11-140">Establezca la propiedad State.</span><span class="sxs-lookup"><span data-stu-id="41a11-140">Set the State property.</span></span>

> <span data-ttu-id="41a11-141">[put_State](#put_state)de HRESULT público (valor de CORE_WEBVIEW2_PERMISSION_STATE)</span><span class="sxs-lookup"><span data-stu-id="41a11-141">public HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="41a11-142">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="41a11-142">GetDeferral</span></span> 

<span data-ttu-id="41a11-143">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="41a11-143">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="41a11-144">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="41a11-144">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="41a11-145">El desarrollador puede usar el objeto de aplazamiento para tomar la decisión de permiso más adelante.</span><span class="sxs-lookup"><span data-stu-id="41a11-145">Developer can use the deferral object to make the permission decision at a later time.</span></span>


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: e29765a4b8a3e620b8c627c7b05b9f0b4ff63f95
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886419"
---
# <span data-ttu-id="99248-104">0.9.430: ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="99248-104">0.9.430 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="99248-105">Argumentos de evento para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="99248-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="99248-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="99248-106">Summary</span></span>

 <span data-ttu-id="99248-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="99248-107">Members</span></span>                        | <span data-ttu-id="99248-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="99248-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="99248-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="99248-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="99248-110">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="99248-110">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="99248-111">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="99248-111">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="99248-112">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="99248-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="99248-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="99248-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="99248-114">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="99248-114">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="99248-115">get_State</span><span class="sxs-lookup"><span data-stu-id="99248-115">get_State</span></span>](#get_state) | <span data-ttu-id="99248-116">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="99248-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="99248-117">put_State</span><span class="sxs-lookup"><span data-stu-id="99248-117">put_State</span></span>](#put_state) | <span data-ttu-id="99248-118">Establezca la propiedad State.</span><span class="sxs-lookup"><span data-stu-id="99248-118">Set the State property.</span></span>
[<span data-ttu-id="99248-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="99248-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="99248-120">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="99248-120">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="99248-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="99248-121">Members</span></span>

#### <span data-ttu-id="99248-122">get_Uri</span><span class="sxs-lookup"><span data-stu-id="99248-122">get_Uri</span></span> 

<span data-ttu-id="99248-123">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="99248-123">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="99248-124">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="99248-124">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="99248-125">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="99248-125">get_PermissionKind</span></span> 

<span data-ttu-id="99248-126">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="99248-126">The type of the permission that is requested.</span></span>

> <span data-ttu-id="99248-127">[get_PermissionKind](#get_permissionkind)de HRESULT público (valor CORE_WEBVIEW2_PERMISSION_KIND \*)</span><span class="sxs-lookup"><span data-stu-id="99248-127">public HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="99248-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="99248-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="99248-129">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="99248-129">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="99248-130">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="99248-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="99248-131">Tenga en cuenta que el que se inicia mediante un movimiento de usuario no significa que el usuario vaya a tener acceso al recurso asociado.</span><span class="sxs-lookup"><span data-stu-id="99248-131">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="99248-132">get_State</span><span class="sxs-lookup"><span data-stu-id="99248-132">get_State</span></span> 

<span data-ttu-id="99248-133">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="99248-133">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="99248-134">[get_State](#get_state)de HRESULT público (valor CORE_WEBVIEW2_PERMISSION_STATE \*)</span><span class="sxs-lookup"><span data-stu-id="99248-134">public HRESULT [get_State](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="99248-135">Si se concede la solicitud.</span><span class="sxs-lookup"><span data-stu-id="99248-135">whether the request is granted.</span></span> <span data-ttu-id="99248-136">El valor predeterminado es CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="99248-136">Default value is CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="99248-137">put_State</span><span class="sxs-lookup"><span data-stu-id="99248-137">put_State</span></span> 

<span data-ttu-id="99248-138">Establezca la propiedad State.</span><span class="sxs-lookup"><span data-stu-id="99248-138">Set the State property.</span></span>

> <span data-ttu-id="99248-139">[put_State](#put_state)de HRESULT público (valor de CORE_WEBVIEW2_PERMISSION_STATE)</span><span class="sxs-lookup"><span data-stu-id="99248-139">public HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="99248-140">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="99248-140">GetDeferral</span></span> 

<span data-ttu-id="99248-141">Se puede llamar a GetDeferral para que devuelva un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="99248-141">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="99248-142">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="99248-142">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="99248-143">El desarrollador puede usar el objeto de aplazamiento para tomar la decisión de permiso más adelante.</span><span class="sxs-lookup"><span data-stu-id="99248-143">Developer can use the deferral object to make the permission decision at a later time.</span></span>


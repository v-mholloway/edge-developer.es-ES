---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: e2a9486011d5ef3ef480271ed32a7c8b586cf9bd
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885831"
---
# <span data-ttu-id="97ee9-104">0.8.355: IWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="97ee9-104">0.8.355 - interface IWebView2PermissionRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="97ee9-105">Argumentos de evento para el evento PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="97ee9-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="97ee9-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="97ee9-106">Summary</span></span>

 <span data-ttu-id="97ee9-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="97ee9-107">Members</span></span>                        | <span data-ttu-id="97ee9-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="97ee9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="97ee9-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="97ee9-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="97ee9-110">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="97ee9-110">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="97ee9-111">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="97ee9-111">get_PermissionType</span></span>](#get_permissiontype) | <span data-ttu-id="97ee9-112">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="97ee9-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="97ee9-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="97ee9-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="97ee9-114">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="97ee9-114">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="97ee9-115">get_State</span><span class="sxs-lookup"><span data-stu-id="97ee9-115">get_State</span></span>](#get_state) | <span data-ttu-id="97ee9-116">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="97ee9-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="97ee9-117">put_State</span><span class="sxs-lookup"><span data-stu-id="97ee9-117">put_State</span></span>](#put_state) | <span data-ttu-id="97ee9-118">Establezca la propiedad State.</span><span class="sxs-lookup"><span data-stu-id="97ee9-118">Set the State property.</span></span>
[<span data-ttu-id="97ee9-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="97ee9-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="97ee9-120">Se puede llamar a GetDeferral para que devuelva un objeto [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="97ee9-120">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="97ee9-121">Miembros</span><span class="sxs-lookup"><span data-stu-id="97ee9-121">Members</span></span>

#### <span data-ttu-id="97ee9-122">get_Uri</span><span class="sxs-lookup"><span data-stu-id="97ee9-122">get_Uri</span></span> 

<span data-ttu-id="97ee9-123">El origen del contenido web que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="97ee9-123">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="97ee9-124">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="97ee9-124">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="97ee9-125">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="97ee9-125">get_PermissionType</span></span> 

<span data-ttu-id="97ee9-126">Tipo del permiso solicitado.</span><span class="sxs-lookup"><span data-stu-id="97ee9-126">The type of the permission that is requested.</span></span>

> <span data-ttu-id="97ee9-127">[get_PermissionType](#get_permissiontype)de HRESULT público (valor WEBVIEW2_PERMISSION_TYPE \*)</span><span class="sxs-lookup"><span data-stu-id="97ee9-127">public HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE \* value)</span></span>

#### <span data-ttu-id="97ee9-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="97ee9-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="97ee9-129">True cuando la solicitud de permiso se ha iniciado mediante un gesto de usuario.</span><span class="sxs-lookup"><span data-stu-id="97ee9-129">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="97ee9-130">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="97ee9-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="97ee9-131">Tenga en cuenta que el que se inicia mediante un movimiento de usuario no significa que el usuario vaya a tener acceso al recurso asociado.</span><span class="sxs-lookup"><span data-stu-id="97ee9-131">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="97ee9-132">get_State</span><span class="sxs-lookup"><span data-stu-id="97ee9-132">get_State</span></span> 

<span data-ttu-id="97ee9-133">El estado de una solicitud de permiso, es decir,</span><span class="sxs-lookup"><span data-stu-id="97ee9-133">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="97ee9-134">[get_State](#get_state)de HRESULT público (valor WEBVIEW2_PERMISSION_STATE \*)</span><span class="sxs-lookup"><span data-stu-id="97ee9-134">public HRESULT [get_State](#get_state)(WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="97ee9-135">Si se concede la solicitud.</span><span class="sxs-lookup"><span data-stu-id="97ee9-135">whether the request is granted.</span></span> <span data-ttu-id="97ee9-136">El valor predeterminado es WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="97ee9-136">Default value is WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="97ee9-137">put_State</span><span class="sxs-lookup"><span data-stu-id="97ee9-137">put_State</span></span> 

<span data-ttu-id="97ee9-138">Establezca la propiedad State.</span><span class="sxs-lookup"><span data-stu-id="97ee9-138">Set the State property.</span></span>

> <span data-ttu-id="97ee9-139">[put_State](#put_state)de HRESULT público (valor de WEBVIEW2_PERMISSION_STATE)</span><span class="sxs-lookup"><span data-stu-id="97ee9-139">public HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="97ee9-140">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="97ee9-140">GetDeferral</span></span> 

<span data-ttu-id="97ee9-141">Se puede llamar a GetDeferral para que devuelva un objeto [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="97ee9-141">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="97ee9-142">[GETDEFERRAL](#getdeferral)HRESULT ([IWebView2Deferral](IWebView2Deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="97ee9-142">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="97ee9-143">El desarrollador puede usar el objeto de aplazamiento para tomar la decisión de permiso más adelante.</span><span class="sxs-lookup"><span data-stu-id="97ee9-143">Developer can use the deferral object to make the permission decision at a later time.</span></span>


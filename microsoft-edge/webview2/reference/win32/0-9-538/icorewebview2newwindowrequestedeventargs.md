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
ms.openlocfilehash: af8df8ff67a0fbe7fd4ec9308b1562b9ef987933
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699466"
---
# <span data-ttu-id="6b2ff-104">interfaz ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6b2ff-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="6b2ff-105">Argumentos de evento para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="6b2ff-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="6b2ff-106">Summary</span></span>

 <span data-ttu-id="6b2ff-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6b2ff-107">Members</span></span>                        | <span data-ttu-id="6b2ff-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6b2ff-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6b2ff-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="6b2ff-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="6b2ff-110">Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="6b2ff-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6b2ff-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="6b2ff-112">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="6b2ff-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="6b2ff-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="6b2ff-114">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-114">Gets the new window.</span></span>
[<span data-ttu-id="6b2ff-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="6b2ff-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="6b2ff-116">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="6b2ff-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="6b2ff-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="6b2ff-118">Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="6b2ff-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="6b2ff-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="6b2ff-120">Establece si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-120">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="6b2ff-121">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="6b2ff-121">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="6b2ff-122">Establece una vista previa como resultado de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-122">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="6b2ff-123">El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="6b2ff-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="6b2ff-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="6b2ff-124">Members</span></span>

#### <span data-ttu-id="6b2ff-125">get_Handled</span><span class="sxs-lookup"><span data-stu-id="6b2ff-125">get_Handled</span></span> 

<span data-ttu-id="6b2ff-126">Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-126">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="6b2ff-127">[get_Handled](#get_handled)de HRESULT público (bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="6b2ff-127">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="6b2ff-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6b2ff-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="6b2ff-129">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-129">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="6b2ff-130">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="6b2ff-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="6b2ff-131">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="6b2ff-131">get_NewWindow</span></span> 

<span data-ttu-id="6b2ff-132">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-132">Gets the new window.</span></span>

> <span data-ttu-id="6b2ff-133">[get_NewWindow](#get_newwindow)de HRESULT público ([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="6b2ff-133">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="6b2ff-134">get_Uri</span><span class="sxs-lookup"><span data-stu-id="6b2ff-134">get_Uri</span></span> 

<span data-ttu-id="6b2ff-135">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-135">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="6b2ff-136">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="6b2ff-136">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="6b2ff-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="6b2ff-137">GetDeferral</span></span> 

<span data-ttu-id="6b2ff-138">Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-138">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="6b2ff-139">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="6b2ff-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="6b2ff-140">Puedes usar el objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para completar la solicitud de apertura de ventana más adelante.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-140">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="6b2ff-141">Mientras se difiere este evento, se devolverá la ventana de apertura de WindowProxy a una ventana no navegada, que se desplazará cuando se complete el aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-141">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="6b2ff-142">put_Handled</span><span class="sxs-lookup"><span data-stu-id="6b2ff-142">put_Handled</span></span> 

<span data-ttu-id="6b2ff-143">Establece si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-143">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="6b2ff-144">[put_Handled](#put_handled)de HRESULT público (bool controlado)</span><span class="sxs-lookup"><span data-stu-id="6b2ff-144">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="6b2ff-145">Si es falso y no se establece NewWindow, WebView abrirá una ventana emergente y se devolverá como WindowProxy abierto.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-145">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="6b2ff-146">Si se establece en true y no se establece NewWindow para una Window. Open Call, el WindowProxy abierto será para un objeto de ventana ficticio y no se cargará ninguna ventana.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-146">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="6b2ff-147">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-147">Default is false.</span></span>

#### <span data-ttu-id="6b2ff-148">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="6b2ff-148">put_NewWindow</span></span> 

<span data-ttu-id="6b2ff-149">Establece una vista previa como resultado de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-149">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="6b2ff-150">[put_NewWindow](#put_newwindow)(HRESULT) público ([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="6b2ff-150">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="6b2ff-151">No se debe navegar por la WebView de destino.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-151">The target webview should not be navigated.</span></span> <span data-ttu-id="6b2ff-152">Si se establece NewWindow, la ventana de nivel superior volverá como la WindowProxy abierta.</span><span class="sxs-lookup"><span data-stu-id="6b2ff-152">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>


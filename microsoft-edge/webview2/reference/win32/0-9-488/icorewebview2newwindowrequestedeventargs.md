---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: cc64e805b0d929d71340d5a012e7848860c35f5c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655327"
---
# <span data-ttu-id="f35e0-104">interfaz ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f35e0-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="f35e0-105">Argumentos de evento para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="f35e0-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="f35e0-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="f35e0-106">Summary</span></span>

 <span data-ttu-id="f35e0-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f35e0-107">Members</span></span>                        | <span data-ttu-id="f35e0-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="f35e0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f35e0-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="f35e0-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="f35e0-110">Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="f35e0-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="f35e0-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="f35e0-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="f35e0-112">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="f35e0-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="f35e0-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="f35e0-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="f35e0-114">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="f35e0-114">Gets the new window.</span></span>
[<span data-ttu-id="f35e0-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="f35e0-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="f35e0-116">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="f35e0-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="f35e0-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f35e0-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="f35e0-118">Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="f35e0-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="f35e0-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="f35e0-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="f35e0-120">Establece si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="f35e0-120">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="f35e0-121">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="f35e0-121">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="f35e0-122">Establece una vista previa como resultado de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="f35e0-122">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="f35e0-123">El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="f35e0-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="f35e0-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="f35e0-124">Members</span></span>

#### <span data-ttu-id="f35e0-125">get_Handled</span><span class="sxs-lookup"><span data-stu-id="f35e0-125">get_Handled</span></span> 

<span data-ttu-id="f35e0-126">Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="f35e0-126">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="f35e0-127">[get_Handled](#get_handled)de HRESULT público (bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="f35e0-127">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="f35e0-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="f35e0-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="f35e0-129">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="f35e0-129">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="f35e0-130">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="f35e0-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="f35e0-131">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="f35e0-131">get_NewWindow</span></span> 

<span data-ttu-id="f35e0-132">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="f35e0-132">Gets the new window.</span></span>

> <span data-ttu-id="f35e0-133">[get_NewWindow](#get_newwindow)de HRESULT público ([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="f35e0-133">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="f35e0-134">get_Uri</span><span class="sxs-lookup"><span data-stu-id="f35e0-134">get_Uri</span></span> 

<span data-ttu-id="f35e0-135">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="f35e0-135">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="f35e0-136">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="f35e0-136">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="f35e0-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f35e0-137">GetDeferral</span></span> 

<span data-ttu-id="f35e0-138">Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="f35e0-138">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="f35e0-139">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="f35e0-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="f35e0-140">Puedes usar el objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para completar la solicitud de apertura de ventana más adelante.</span><span class="sxs-lookup"><span data-stu-id="f35e0-140">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="f35e0-141">Mientras se difiere este evento, se devolverá la ventana de apertura de WindowProxy a una ventana no navegada, que se desplazará cuando se complete el aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="f35e0-141">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="f35e0-142">put_Handled</span><span class="sxs-lookup"><span data-stu-id="f35e0-142">put_Handled</span></span> 

<span data-ttu-id="f35e0-143">Establece si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="f35e0-143">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="f35e0-144">[put_Handled](#put_handled)de HRESULT público (bool controlado)</span><span class="sxs-lookup"><span data-stu-id="f35e0-144">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="f35e0-145">Si es falso y no se establece NewWindow, WebView abrirá una ventana emergente y se devolverá como WindowProxy abierto.</span><span class="sxs-lookup"><span data-stu-id="f35e0-145">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="f35e0-146">Si se establece en true y no se establece NewWindow para una Window. Open Call, el WindowProxy abierto será para un objeto de ventana ficticio y no se cargará ninguna ventana.</span><span class="sxs-lookup"><span data-stu-id="f35e0-146">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="f35e0-147">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="f35e0-147">Default is false.</span></span>

#### <span data-ttu-id="f35e0-148">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="f35e0-148">put_NewWindow</span></span> 

<span data-ttu-id="f35e0-149">Establece una vista previa como resultado de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="f35e0-149">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="f35e0-150">[put_NewWindow](#put_newwindow)(HRESULT) público ([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="f35e0-150">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="f35e0-151">No se debe navegar por la WebView de destino.</span><span class="sxs-lookup"><span data-stu-id="f35e0-151">The target webview should not be navigated.</span></span> <span data-ttu-id="f35e0-152">Si se establece NewWindow, la ventana de nivel superior volverá como la WindowProxy abierta.</span><span class="sxs-lookup"><span data-stu-id="f35e0-152">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>


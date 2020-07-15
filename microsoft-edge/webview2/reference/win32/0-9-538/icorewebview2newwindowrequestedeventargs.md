---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2NewWindowRequestedEventArgs
ms.openlocfilehash: bb18b6662fd5921406e19b3c333c97f8a1cd0dbc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879439"
---
# <span data-ttu-id="e57f1-104">interfaz ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e57f1-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="e57f1-105">Argumentos de evento para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="e57f1-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="e57f1-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e57f1-106">Summary</span></span>

 <span data-ttu-id="e57f1-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e57f1-107">Members</span></span>                        | <span data-ttu-id="e57f1-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e57f1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e57f1-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="e57f1-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="e57f1-110">Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="e57f1-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="e57f1-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="e57f1-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="e57f1-112">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="e57f1-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="e57f1-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="e57f1-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="e57f1-114">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="e57f1-114">Gets the new window.</span></span>
[<span data-ttu-id="e57f1-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="e57f1-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="e57f1-116">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="e57f1-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="e57f1-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e57f1-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="e57f1-118">Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="e57f1-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="e57f1-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="e57f1-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="e57f1-120">Establece si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="e57f1-120">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="e57f1-121">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="e57f1-121">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="e57f1-122">Establece una vista previa como resultado de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="e57f1-122">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="e57f1-123">El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="e57f1-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="e57f1-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="e57f1-124">Members</span></span>

#### <span data-ttu-id="e57f1-125">get_Handled</span><span class="sxs-lookup"><span data-stu-id="e57f1-125">get_Handled</span></span> 

<span data-ttu-id="e57f1-126">Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="e57f1-126">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="e57f1-127">[get_Handled](#get_handled)de HRESULT público (bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="e57f1-127">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="e57f1-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="e57f1-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="e57f1-129">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="e57f1-129">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="e57f1-130">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="e57f1-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="e57f1-131">El bloqueador de ventanas emergentes de Edge está deshabilitado para WebView, por lo que la aplicación puede usar esta marca para bloquear los mensajes emergentes no iniciados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="e57f1-131">The Edge popup blocker is disabled for WebView so the app can use this flag to block non-user initiated popups.</span></span>

#### <span data-ttu-id="e57f1-132">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="e57f1-132">get_NewWindow</span></span> 

<span data-ttu-id="e57f1-133">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="e57f1-133">Gets the new window.</span></span>

> <span data-ttu-id="e57f1-134">[get_NewWindow](#get_newwindow)de HRESULT público ([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="e57f1-134">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="e57f1-135">get_Uri</span><span class="sxs-lookup"><span data-stu-id="e57f1-135">get_Uri</span></span> 

<span data-ttu-id="e57f1-136">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="e57f1-136">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="e57f1-137">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="e57f1-137">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="e57f1-138">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e57f1-138">GetDeferral</span></span> 

<span data-ttu-id="e57f1-139">Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="e57f1-139">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="e57f1-140">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="e57f1-140">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="e57f1-141">Puedes usar el objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para completar la solicitud de apertura de ventana más adelante.</span><span class="sxs-lookup"><span data-stu-id="e57f1-141">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="e57f1-142">Mientras se difiere este evento, se devolverá la ventana de apertura de WindowProxy a una ventana no navegada, que se desplazará cuando se complete el aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="e57f1-142">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="e57f1-143">put_Handled</span><span class="sxs-lookup"><span data-stu-id="e57f1-143">put_Handled</span></span> 

<span data-ttu-id="e57f1-144">Establece si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="e57f1-144">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="e57f1-145">[put_Handled](#put_handled)de HRESULT público (bool controlado)</span><span class="sxs-lookup"><span data-stu-id="e57f1-145">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="e57f1-146">Si es falso y no se establece NewWindow, WebView abrirá una ventana emergente y se devolverá como WindowProxy abierto.</span><span class="sxs-lookup"><span data-stu-id="e57f1-146">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="e57f1-147">Si se establece en true y no se establece NewWindow para una Window. Open Call, el WindowProxy abierto será para un objeto de ventana ficticio y no se cargará ninguna ventana.</span><span class="sxs-lookup"><span data-stu-id="e57f1-147">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="e57f1-148">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="e57f1-148">Default is false.</span></span>

#### <span data-ttu-id="e57f1-149">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="e57f1-149">put_NewWindow</span></span> 

<span data-ttu-id="e57f1-150">Establece una vista previa como resultado de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="e57f1-150">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="e57f1-151">[put_NewWindow](#put_newwindow)(HRESULT) público ([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="e57f1-151">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="e57f1-152">No se debe navegar por la WebView de destino.</span><span class="sxs-lookup"><span data-stu-id="e57f1-152">The target webview should not be navigated.</span></span> <span data-ttu-id="e57f1-153">Si se establece NewWindow, la ventana de nivel superior volverá como la WindowProxy abierta.</span><span class="sxs-lookup"><span data-stu-id="e57f1-153">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>


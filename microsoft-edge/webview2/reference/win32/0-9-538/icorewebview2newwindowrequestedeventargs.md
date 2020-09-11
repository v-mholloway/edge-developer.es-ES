---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2NewWindowRequestedEventArgs
ms.openlocfilehash: 5486aa66e39e220e819bb00211a79bd449a25bfe
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010064"
---
# <span data-ttu-id="3b595-104">0.9.579: ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="3b595-104">0.9.579 - interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="3b595-105">Argumentos de evento para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="3b595-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="3b595-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="3b595-106">Summary</span></span>

 <span data-ttu-id="3b595-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="3b595-107">Members</span></span>                        | <span data-ttu-id="3b595-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="3b595-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3b595-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="3b595-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="3b595-110">Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="3b595-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="3b595-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="3b595-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="3b595-112">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="3b595-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="3b595-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="3b595-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="3b595-114">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="3b595-114">Gets the new window.</span></span>
[<span data-ttu-id="3b595-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="3b595-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="3b595-116">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="3b595-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="3b595-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="3b595-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="3b595-118">Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="3b595-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="3b595-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="3b595-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="3b595-120">Establece si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="3b595-120">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="3b595-121">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="3b595-121">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="3b595-122">Establece una vista previa como resultado de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="3b595-122">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="3b595-123">El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="3b595-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="3b595-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="3b595-124">Members</span></span>

#### <span data-ttu-id="3b595-125">get_Handled</span><span class="sxs-lookup"><span data-stu-id="3b595-125">get_Handled</span></span> 

<span data-ttu-id="3b595-126">Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="3b595-126">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="3b595-127">[get_Handled](#get_handled)de HRESULT público (bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="3b595-127">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="3b595-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="3b595-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="3b595-129">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="3b595-129">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="3b595-130">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="3b595-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="3b595-131">El bloqueador de ventanas emergentes de Edge está deshabilitado para WebView, por lo que la aplicación puede usar esta marca para bloquear los mensajes emergentes no iniciados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="3b595-131">The Edge popup blocker is disabled for WebView so the app can use this flag to block non-user initiated popups.</span></span>

#### <span data-ttu-id="3b595-132">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="3b595-132">get_NewWindow</span></span> 

<span data-ttu-id="3b595-133">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="3b595-133">Gets the new window.</span></span>

> <span data-ttu-id="3b595-134">[get_NewWindow](#get_newwindow)de HRESULT público ([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="3b595-134">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="3b595-135">get_Uri</span><span class="sxs-lookup"><span data-stu-id="3b595-135">get_Uri</span></span> 

<span data-ttu-id="3b595-136">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="3b595-136">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="3b595-137">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="3b595-137">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="3b595-138">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="3b595-138">GetDeferral</span></span> 

<span data-ttu-id="3b595-139">Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="3b595-139">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="3b595-140">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="3b595-140">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="3b595-141">Puedes usar el objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para completar la solicitud de apertura de ventana más adelante.</span><span class="sxs-lookup"><span data-stu-id="3b595-141">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="3b595-142">Mientras se difiere este evento, se devolverá la ventana de apertura de WindowProxy a una ventana no navegada, que se desplazará cuando se complete el aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="3b595-142">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="3b595-143">put_Handled</span><span class="sxs-lookup"><span data-stu-id="3b595-143">put_Handled</span></span> 

<span data-ttu-id="3b595-144">Establece si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="3b595-144">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="3b595-145">[put_Handled](#put_handled)de HRESULT público (bool controlado)</span><span class="sxs-lookup"><span data-stu-id="3b595-145">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="3b595-146">Si es falso y no se establece NewWindow, WebView abrirá una ventana emergente y se devolverá como WindowProxy abierto.</span><span class="sxs-lookup"><span data-stu-id="3b595-146">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="3b595-147">Si se establece en true y no se establece NewWindow para una Window. Open Call, el WindowProxy abierto será para un objeto de ventana ficticio y no se cargará ninguna ventana.</span><span class="sxs-lookup"><span data-stu-id="3b595-147">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="3b595-148">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="3b595-148">Default is false.</span></span>

#### <span data-ttu-id="3b595-149">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="3b595-149">put_NewWindow</span></span> 

<span data-ttu-id="3b595-150">Establece una vista previa como resultado de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="3b595-150">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="3b595-151">[put_NewWindow](#put_newwindow)(HRESULT) público ([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="3b595-151">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="3b595-152">No se debe navegar por la WebView de destino.</span><span class="sxs-lookup"><span data-stu-id="3b595-152">The target webview should not be navigated.</span></span> <span data-ttu-id="3b595-153">Si se establece NewWindow, la ventana de nivel superior volverá como la WindowProxy abierta.</span><span class="sxs-lookup"><span data-stu-id="3b595-153">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>


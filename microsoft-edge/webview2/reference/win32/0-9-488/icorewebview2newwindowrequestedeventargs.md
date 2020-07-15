---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: aeefa0257a273f0eecd99d3f666adc03be709d9a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880496"
---
# <span data-ttu-id="2e5e8-104">0.9.515: ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2e5e8-104">0.9.515 - interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="2e5e8-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="2e5e8-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="2e5e8-107">Argumentos de evento para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="2e5e8-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="2e5e8-108">Summary</span></span>

 <span data-ttu-id="2e5e8-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2e5e8-109">Members</span></span>                        | <span data-ttu-id="2e5e8-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2e5e8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2e5e8-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="2e5e8-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="2e5e8-112">Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-112">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="2e5e8-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="2e5e8-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="2e5e8-114">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="2e5e8-115">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="2e5e8-115">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="2e5e8-116">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-116">Gets the new window.</span></span>
[<span data-ttu-id="2e5e8-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2e5e8-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="2e5e8-118">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="2e5e8-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2e5e8-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="2e5e8-120">Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-120">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="2e5e8-121">put_Handled</span><span class="sxs-lookup"><span data-stu-id="2e5e8-121">put_Handled</span></span>](#put_handled) | <span data-ttu-id="2e5e8-122">Establece si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-122">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="2e5e8-123">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="2e5e8-123">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="2e5e8-124">Establece una vista previa como resultado de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-124">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="2e5e8-125">El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="2e5e8-125">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="2e5e8-126">Miembros</span><span class="sxs-lookup"><span data-stu-id="2e5e8-126">Members</span></span>

#### <span data-ttu-id="2e5e8-127">get_Handled</span><span class="sxs-lookup"><span data-stu-id="2e5e8-127">get_Handled</span></span> 

<span data-ttu-id="2e5e8-128">Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-128">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="2e5e8-129">[get_Handled](#get_handled)de HRESULT público (bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="2e5e8-129">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="2e5e8-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="2e5e8-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="2e5e8-131">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-131">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="2e5e8-132">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="2e5e8-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="2e5e8-133">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="2e5e8-133">get_NewWindow</span></span> 

<span data-ttu-id="2e5e8-134">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-134">Gets the new window.</span></span>

> <span data-ttu-id="2e5e8-135">[get_NewWindow](#get_newwindow)de HRESULT público ([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="2e5e8-135">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="2e5e8-136">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2e5e8-136">get_Uri</span></span> 

<span data-ttu-id="2e5e8-137">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-137">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="2e5e8-138">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="2e5e8-138">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="2e5e8-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2e5e8-139">GetDeferral</span></span> 

<span data-ttu-id="2e5e8-140">Obtén un objeto [ICoreWebView2Deferral](icorewebview2deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-140">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="2e5e8-141">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="2e5e8-141">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="2e5e8-142">Puedes usar el objeto [ICoreWebView2Deferral](icorewebview2deferral.md) para completar la solicitud de apertura de ventana más adelante.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-142">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="2e5e8-143">Mientras se difiere este evento, se devolverá la ventana de apertura de WindowProxy a una ventana no navegada, que se desplazará cuando se complete el aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-143">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="2e5e8-144">put_Handled</span><span class="sxs-lookup"><span data-stu-id="2e5e8-144">put_Handled</span></span> 

<span data-ttu-id="2e5e8-145">Establece si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-145">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="2e5e8-146">[put_Handled](#put_handled)de HRESULT público (bool controlado)</span><span class="sxs-lookup"><span data-stu-id="2e5e8-146">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="2e5e8-147">Si es falso y no se establece NewWindow, WebView abrirá una ventana emergente y se devolverá como WindowProxy abierto.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-147">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="2e5e8-148">Si se establece en true y no se establece NewWindow para una Window. Open Call, el WindowProxy abierto será para un objeto de ventana ficticio y no se cargará ninguna ventana.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-148">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="2e5e8-149">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-149">Default is false.</span></span>

#### <span data-ttu-id="2e5e8-150">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="2e5e8-150">put_NewWindow</span></span> 

<span data-ttu-id="2e5e8-151">Establece una vista previa como resultado de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-151">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="2e5e8-152">[put_NewWindow](#put_newwindow)(HRESULT) público ([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="2e5e8-152">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="2e5e8-153">No se debe navegar por la WebView de destino.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-153">The target webview should not be navigated.</span></span> <span data-ttu-id="2e5e8-154">Si se establece NewWindow, la ventana de nivel superior volverá como la WindowProxy abierta.</span><span class="sxs-lookup"><span data-stu-id="2e5e8-154">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>


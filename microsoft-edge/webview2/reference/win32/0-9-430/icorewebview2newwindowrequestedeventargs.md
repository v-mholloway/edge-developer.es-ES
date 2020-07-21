---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 73f62e7130d50028b527353c6ba1a238f694dcda
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885684"
---
# <span data-ttu-id="0f971-104">0.9.430: ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="0f971-104">0.9.430 - interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="0f971-105">Argumentos de evento para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="0f971-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="0f971-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="0f971-106">Summary</span></span>

 <span data-ttu-id="0f971-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0f971-107">Members</span></span>                        | <span data-ttu-id="0f971-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="0f971-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0f971-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="0f971-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="0f971-110">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="0f971-110">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="0f971-111">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="0f971-111">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="0f971-112">Establece una vista previa como resultado de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="0f971-112">Sets a WebView as a result of the NewWindowRequest.</span></span>
[<span data-ttu-id="0f971-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="0f971-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="0f971-114">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="0f971-114">Gets the new window.</span></span>
[<span data-ttu-id="0f971-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="0f971-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="0f971-116">Establece si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="0f971-116">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="0f971-117">get_Handled</span><span class="sxs-lookup"><span data-stu-id="0f971-117">get_Handled</span></span>](#get_handled) | <span data-ttu-id="0f971-118">Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="0f971-118">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="0f971-119">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="0f971-119">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="0f971-120">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="0f971-120">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="0f971-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="0f971-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="0f971-122">Obtén un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="0f971-122">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

<span data-ttu-id="0f971-123">El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () etc.).</span><span class="sxs-lookup"><span data-stu-id="0f971-123">The event is fired when content inside webview requested to a open a new window (through window.open() etc.)</span></span>

## <span data-ttu-id="0f971-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="0f971-124">Members</span></span>

#### <span data-ttu-id="0f971-125">get_Uri</span><span class="sxs-lookup"><span data-stu-id="0f971-125">get_Uri</span></span> 

<span data-ttu-id="0f971-126">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="0f971-126">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="0f971-127">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="0f971-127">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="0f971-128">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="0f971-128">put_NewWindow</span></span> 

<span data-ttu-id="0f971-129">Establece una vista previa como resultado de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="0f971-129">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="0f971-130">[put_NewWindow](#put_newwindow)(HRESULT) público ([ICoreWebView2](ICoreWebView2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="0f971-130">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](ICoreWebView2.md) \* newWindow)</span></span>

<span data-ttu-id="0f971-131">No se debe navegar por la WebView de destino.</span><span class="sxs-lookup"><span data-stu-id="0f971-131">The target webview should not be navigated.</span></span> <span data-ttu-id="0f971-132">Si se establece NewWindow, la ventana de nivel superior volverá como la WindowProxy abierta.</span><span class="sxs-lookup"><span data-stu-id="0f971-132">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="0f971-133">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="0f971-133">get_NewWindow</span></span> 

<span data-ttu-id="0f971-134">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="0f971-134">Gets the new window.</span></span>

> <span data-ttu-id="0f971-135">[get_NewWindow](#get_newwindow)de HRESULT público ([ICoreWebView2](ICoreWebView2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="0f971-135">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](ICoreWebView2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="0f971-136">put_Handled</span><span class="sxs-lookup"><span data-stu-id="0f971-136">put_Handled</span></span> 

<span data-ttu-id="0f971-137">Establece si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="0f971-137">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="0f971-138">[put_Handled](#put_handled)de HRESULT público (bool controlado)</span><span class="sxs-lookup"><span data-stu-id="0f971-138">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="0f971-139">Si es falso y no se establece NewWindow, WebView abrirá una ventana emergente y se devolverá como WindowProxy abierto.</span><span class="sxs-lookup"><span data-stu-id="0f971-139">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="0f971-140">Si se establece en true y no se establece NewWindow para una Window. Open Call, el WindowProxy abierto será para un objeto de ventana ficticio y no se cargará ninguna ventana.</span><span class="sxs-lookup"><span data-stu-id="0f971-140">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="0f971-141">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="0f971-141">Default is false.</span></span>

#### <span data-ttu-id="0f971-142">get_Handled</span><span class="sxs-lookup"><span data-stu-id="0f971-142">get_Handled</span></span> 

<span data-ttu-id="0f971-143">Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="0f971-143">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="0f971-144">[get_Handled](#get_handled)de HRESULT público (bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="0f971-144">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="0f971-145">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="0f971-145">get_IsUserInitiated</span></span> 

<span data-ttu-id="0f971-146">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="0f971-146">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="0f971-147">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="0f971-147">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="0f971-148">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="0f971-148">GetDeferral</span></span> 

<span data-ttu-id="0f971-149">Obtén un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="0f971-149">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="0f971-150">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="0f971-150">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="0f971-151">Puedes usar el objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) para completar la solicitud de apertura de ventana más adelante.</span><span class="sxs-lookup"><span data-stu-id="0f971-151">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="0f971-152">Mientras se difiere este evento, se devolverá la ventana de apertura de WindowProxy a una ventana no navegada, que se desplazará cuando se complete el aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="0f971-152">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>


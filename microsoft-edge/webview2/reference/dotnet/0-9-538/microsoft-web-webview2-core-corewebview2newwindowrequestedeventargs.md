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
ms.openlocfilehash: 54e2c06ef65f64560fbd5687148eace253352203
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699314"
---
# <span data-ttu-id="ec9b3-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ec9b3-104">Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

<span data-ttu-id="ec9b3-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="ec9b3-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="ec9b3-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="ec9b3-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="ec9b3-107">Argumentos de evento para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="ec9b3-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="ec9b3-108">Summary</span></span>

 <span data-ttu-id="ec9b3-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="ec9b3-109">Members</span></span>                        | <span data-ttu-id="ec9b3-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ec9b3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ec9b3-111">Handled</span><span class="sxs-lookup"><span data-stu-id="ec9b3-111">Handled</span></span>](#handled) | <span data-ttu-id="ec9b3-112">Si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-112">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="ec9b3-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ec9b3-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="ec9b3-114">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="ec9b3-115">NewWindow</span><span class="sxs-lookup"><span data-stu-id="ec9b3-115">NewWindow</span></span>](#newwindow) | <span data-ttu-id="ec9b3-116">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-116">Gets the new window.</span></span>
[<span data-ttu-id="ec9b3-117">URI</span><span class="sxs-lookup"><span data-stu-id="ec9b3-117">Uri</span></span>](#uri) | <span data-ttu-id="ec9b3-118">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="ec9b3-119">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="ec9b3-119">WindowFeatures</span></span>](#windowfeatures) | <span data-ttu-id="ec9b3-120">Características de la ventana especificadas por la llamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-120">Window features specified by the window.open call.</span></span>
[<span data-ttu-id="ec9b3-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ec9b3-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="ec9b3-122">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-122">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="ec9b3-123">El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="ec9b3-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="ec9b3-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="ec9b3-124">Members</span></span>

#### <span data-ttu-id="ec9b3-125">Handled</span><span class="sxs-lookup"><span data-stu-id="ec9b3-125">Handled</span></span> 

<span data-ttu-id="ec9b3-126">Si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-126">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="ec9b3-127">bool público [Handled](#handled)</span><span class="sxs-lookup"><span data-stu-id="ec9b3-127">public bool [Handled](#handled)</span></span>

<span data-ttu-id="ec9b3-128">Si es falso y no se establece NewWindow, WebView abrirá una ventana emergente y se devolverá como WindowProxy abierto.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-128">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="ec9b3-129">Si se establece en true y no se establece NewWindow para una Window. Open Call, el WindowProxy abierto será para un objeto de ventana ficticio y no se cargará ninguna ventana.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-129">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="ec9b3-130">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-130">Default is false.</span></span>

#### <span data-ttu-id="ec9b3-131">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="ec9b3-131">IsUserInitiated</span></span> 

<span data-ttu-id="ec9b3-132">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-132">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="ec9b3-133">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="ec9b3-133">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="ec9b3-134">NewWindow</span><span class="sxs-lookup"><span data-stu-id="ec9b3-134">NewWindow</span></span> 

<span data-ttu-id="ec9b3-135">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-135">Gets the new window.</span></span>

> <span data-ttu-id="ec9b3-136">CoreWebView2 pública [NewWindow](#newwindow)</span><span class="sxs-lookup"><span data-stu-id="ec9b3-136">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="ec9b3-137">URI</span><span class="sxs-lookup"><span data-stu-id="ec9b3-137">Uri</span></span> 

<span data-ttu-id="ec9b3-138">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-138">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="ec9b3-139">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="ec9b3-139">public string [Uri](#uri)</span></span>

<span data-ttu-id="ec9b3-140">No se debe navegar por la WebView de destino.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-140">The target webview should not be navigated.</span></span> <span data-ttu-id="ec9b3-141">Si se establece NewWindow, la ventana de nivel superior volverá como la WindowProxy abierta.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-141">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="ec9b3-142">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="ec9b3-142">WindowFeatures</span></span> 

> [!NOTE]
> <span data-ttu-id="ec9b3-143">Esta es una [API experimental](../../../concepts/versioning.md#experimental-apis) que se incluía con nuestra versión [de SDK 0.9.538-prerelease](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="ec9b3-143">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="ec9b3-144">Características de la ventana especificadas por la llamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-144">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="ec9b3-145">CoreWebView2WindowFeatures pública [WindowFeatures](#windowfeatures)</span><span class="sxs-lookup"><span data-stu-id="ec9b3-145">public CoreWebView2WindowFeatures [WindowFeatures](#windowfeatures)</span></span>

<span data-ttu-id="ec9b3-146">Estas características se pueden considerar para posicionar y cambiar el tamaño de nuevas ventanas de WebView.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-146">These features can be considered for positioning and sizing of new webview windows.</span></span>

#### <span data-ttu-id="ec9b3-147">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ec9b3-147">GetDeferral</span></span> 

<span data-ttu-id="ec9b3-148">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-148">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="ec9b3-149">Public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="ec9b3-149">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="ec9b3-150">Puedes usar el objeto CoreWebView2Deferral para completar la solicitud de apertura de ventana más adelante.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-150">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="ec9b3-151">Mientras se difiere este evento, se devolverá la ventana de apertura de WindowProxy a una ventana no navegada, que se desplazará cuando se complete el aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="ec9b3-151">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>


---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs
ms.openlocfilehash: 5e5d16c025dccf788b355280eaa3ac3e910f240d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012642"
---
# <span data-ttu-id="559a1-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="559a1-104">Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

<span data-ttu-id="559a1-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="559a1-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="559a1-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="559a1-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="559a1-107">Argumentos de evento para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="559a1-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="559a1-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="559a1-108">Summary</span></span>

 <span data-ttu-id="559a1-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="559a1-109">Members</span></span>                        | <span data-ttu-id="559a1-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="559a1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="559a1-111">Handled</span><span class="sxs-lookup"><span data-stu-id="559a1-111">Handled</span></span>](#handled) | <span data-ttu-id="559a1-112">Si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="559a1-112">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="559a1-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="559a1-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="559a1-114">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="559a1-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="559a1-115">NewWindow</span><span class="sxs-lookup"><span data-stu-id="559a1-115">NewWindow</span></span>](#newwindow) | <span data-ttu-id="559a1-116">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="559a1-116">Gets the new window.</span></span>
[<span data-ttu-id="559a1-117">URI</span><span class="sxs-lookup"><span data-stu-id="559a1-117">Uri</span></span>](#uri) | <span data-ttu-id="559a1-118">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="559a1-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="559a1-119">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="559a1-119">WindowFeatures</span></span>](#windowfeatures) | <span data-ttu-id="559a1-120">Características de la ventana especificadas por la llamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="559a1-120">Window features specified by the window.open call.</span></span>
[<span data-ttu-id="559a1-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="559a1-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="559a1-122">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="559a1-122">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="559a1-123">El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="559a1-123">The event is fired when content inside WebView requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="559a1-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="559a1-124">Members</span></span>

#### <span data-ttu-id="559a1-125">Handled</span><span class="sxs-lookup"><span data-stu-id="559a1-125">Handled</span></span> 

<span data-ttu-id="559a1-126">Si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="559a1-126">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="559a1-127">bool público [Handled](#handled)</span><span class="sxs-lookup"><span data-stu-id="559a1-127">public bool [Handled](#handled)</span></span>

<span data-ttu-id="559a1-128">Si es falso y no se establece NewWindow, WebView abrirá una ventana emergente y se devolverá como WindowProxy abierto.</span><span class="sxs-lookup"><span data-stu-id="559a1-128">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="559a1-129">Si se establece en true y no se establece NewWindow para una Window. Open Call, el WindowProxy abierto será para un objeto de ventana ficticio y no se cargará ninguna ventana.</span><span class="sxs-lookup"><span data-stu-id="559a1-129">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="559a1-130">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="559a1-130">Default is false.</span></span>

#### <span data-ttu-id="559a1-131">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="559a1-131">IsUserInitiated</span></span> 

<span data-ttu-id="559a1-132">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="559a1-132">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="559a1-133">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="559a1-133">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="559a1-134">NewWindow</span><span class="sxs-lookup"><span data-stu-id="559a1-134">NewWindow</span></span> 

<span data-ttu-id="559a1-135">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="559a1-135">Gets the new window.</span></span>

> <span data-ttu-id="559a1-136">CoreWebView2 pública [NewWindow](#newwindow)</span><span class="sxs-lookup"><span data-stu-id="559a1-136">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="559a1-137">URI</span><span class="sxs-lookup"><span data-stu-id="559a1-137">Uri</span></span> 

<span data-ttu-id="559a1-138">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="559a1-138">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="559a1-139">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="559a1-139">public string [Uri](#uri)</span></span>

<span data-ttu-id="559a1-140">No se debe navegar por la WebView de destino.</span><span class="sxs-lookup"><span data-stu-id="559a1-140">The target WebView should not be navigated.</span></span> <span data-ttu-id="559a1-141">Si se establece NewWindow, la ventana de nivel superior volverá como la WindowProxy abierta.</span><span class="sxs-lookup"><span data-stu-id="559a1-141">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="559a1-142">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="559a1-142">WindowFeatures</span></span> 

<span data-ttu-id="559a1-143">Características de la ventana especificadas por la llamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="559a1-143">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="559a1-144">CoreWebView2WindowFeatures pública [WindowFeatures](#windowfeatures)</span><span class="sxs-lookup"><span data-stu-id="559a1-144">public CoreWebView2WindowFeatures [WindowFeatures](#windowfeatures)</span></span>

<span data-ttu-id="559a1-145">Estas características se pueden considerar para posicionar y cambiar el tamaño de nuevas ventanas de WebView.</span><span class="sxs-lookup"><span data-stu-id="559a1-145">These features can be considered for positioning and sizing of new WebView windows.</span></span>

#### <span data-ttu-id="559a1-146">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="559a1-146">GetDeferral</span></span> 

<span data-ttu-id="559a1-147">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="559a1-147">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="559a1-148">Public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="559a1-148">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="559a1-149">Puedes usar el objeto CoreWebView2Deferral para completar la solicitud de apertura de ventana más adelante.</span><span class="sxs-lookup"><span data-stu-id="559a1-149">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="559a1-150">Mientras se difiere este evento, se devolverá la ventana de apertura de WindowProxy a una ventana no navegada, que se desplazará cuando se complete el aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="559a1-150">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>


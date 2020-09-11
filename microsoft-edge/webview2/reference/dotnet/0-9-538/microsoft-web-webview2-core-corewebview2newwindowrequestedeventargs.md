---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs
ms.openlocfilehash: adeb4c0f223e8b38e3cefb93ae189a351d9828a5
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010911"
---
# <span data-ttu-id="a44e4-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs (clase)</span><span class="sxs-lookup"><span data-stu-id="a44e4-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="a44e4-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="a44e4-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="a44e4-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="a44e4-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="a44e4-107">Argumentos de evento para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="a44e4-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="a44e4-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="a44e4-108">Summary</span></span>

 <span data-ttu-id="a44e4-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a44e4-109">Members</span></span>                        | <span data-ttu-id="a44e4-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a44e4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a44e4-111">Handled</span><span class="sxs-lookup"><span data-stu-id="a44e4-111">Handled</span></span>](#handled) | <span data-ttu-id="a44e4-112">Si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="a44e4-112">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="a44e4-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a44e4-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="a44e4-114">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="a44e4-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="a44e4-115">NewWindow</span><span class="sxs-lookup"><span data-stu-id="a44e4-115">NewWindow</span></span>](#newwindow) | <span data-ttu-id="a44e4-116">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="a44e4-116">Gets the new window.</span></span>
[<span data-ttu-id="a44e4-117">URI</span><span class="sxs-lookup"><span data-stu-id="a44e4-117">Uri</span></span>](#uri) | <span data-ttu-id="a44e4-118">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="a44e4-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="a44e4-119">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="a44e4-119">WindowFeatures</span></span>](#windowfeatures) | <span data-ttu-id="a44e4-120">Características de la ventana especificadas por la llamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="a44e4-120">Window features specified by the window.open call.</span></span>
[<span data-ttu-id="a44e4-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="a44e4-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="a44e4-122">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="a44e4-122">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="a44e4-123">El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="a44e4-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="a44e4-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="a44e4-124">Members</span></span>

#### <span data-ttu-id="a44e4-125">Handled</span><span class="sxs-lookup"><span data-stu-id="a44e4-125">Handled</span></span> 

<span data-ttu-id="a44e4-126">Si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="a44e4-126">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="a44e4-127">bool público [Handled](#handled)</span><span class="sxs-lookup"><span data-stu-id="a44e4-127">public bool [Handled](#handled)</span></span>

<span data-ttu-id="a44e4-128">Si es falso y no se establece NewWindow, WebView abrirá una ventana emergente y se devolverá como WindowProxy abierto.</span><span class="sxs-lookup"><span data-stu-id="a44e4-128">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="a44e4-129">Si se establece en true y no se establece NewWindow para una Window. Open Call, el WindowProxy abierto será para un objeto de ventana ficticio y no se cargará ninguna ventana.</span><span class="sxs-lookup"><span data-stu-id="a44e4-129">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="a44e4-130">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="a44e4-130">Default is false.</span></span>

#### <span data-ttu-id="a44e4-131">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a44e4-131">IsUserInitiated</span></span> 

<span data-ttu-id="a44e4-132">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="a44e4-132">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="a44e4-133">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="a44e4-133">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="a44e4-134">NewWindow</span><span class="sxs-lookup"><span data-stu-id="a44e4-134">NewWindow</span></span> 

<span data-ttu-id="a44e4-135">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="a44e4-135">Gets the new window.</span></span>

> <span data-ttu-id="a44e4-136">CoreWebView2 pública [NewWindow](#newwindow)</span><span class="sxs-lookup"><span data-stu-id="a44e4-136">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="a44e4-137">URI</span><span class="sxs-lookup"><span data-stu-id="a44e4-137">Uri</span></span> 

<span data-ttu-id="a44e4-138">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="a44e4-138">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="a44e4-139">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="a44e4-139">public string [Uri](#uri)</span></span>

<span data-ttu-id="a44e4-140">No se debe navegar por la WebView de destino.</span><span class="sxs-lookup"><span data-stu-id="a44e4-140">The target webview should not be navigated.</span></span> <span data-ttu-id="a44e4-141">Si se establece NewWindow, la ventana de nivel superior volverá como la WindowProxy abierta.</span><span class="sxs-lookup"><span data-stu-id="a44e4-141">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="a44e4-142">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="a44e4-142">WindowFeatures</span></span> 

<span data-ttu-id="a44e4-143">Características de la ventana especificadas por la llamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="a44e4-143">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="a44e4-144">CoreWebView2WindowFeatures pública [WindowFeatures](#windowfeatures)</span><span class="sxs-lookup"><span data-stu-id="a44e4-144">public CoreWebView2WindowFeatures [WindowFeatures](#windowfeatures)</span></span>

<span data-ttu-id="a44e4-145">Estas características se pueden considerar para posicionar y cambiar el tamaño de nuevas ventanas de WebView.</span><span class="sxs-lookup"><span data-stu-id="a44e4-145">These features can be considered for positioning and sizing of new webview windows.</span></span>

#### <span data-ttu-id="a44e4-146">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="a44e4-146">GetDeferral</span></span> 

<span data-ttu-id="a44e4-147">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="a44e4-147">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="a44e4-148">Public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="a44e4-148">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="a44e4-149">Puedes usar el objeto CoreWebView2Deferral para completar la solicitud de apertura de ventana más adelante.</span><span class="sxs-lookup"><span data-stu-id="a44e4-149">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="a44e4-150">Mientras se difiere este evento, se devolverá la ventana de apertura de WindowProxy a una ventana no navegada, que se desplazará cuando se complete el aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="a44e4-150">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>


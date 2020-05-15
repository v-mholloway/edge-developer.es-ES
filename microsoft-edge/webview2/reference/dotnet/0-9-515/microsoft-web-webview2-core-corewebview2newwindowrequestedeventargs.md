---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: cca15ccc5292f5eaf6f317ffb657f46fcd84b4a9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655446"
---
# <span data-ttu-id="7799f-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7799f-104">Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

<span data-ttu-id="7799f-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="7799f-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="7799f-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="7799f-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="7799f-107">Argumentos de evento para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="7799f-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="7799f-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="7799f-108">Summary</span></span>

 <span data-ttu-id="7799f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7799f-109">Members</span></span>                        | <span data-ttu-id="7799f-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7799f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7799f-111">Handled</span><span class="sxs-lookup"><span data-stu-id="7799f-111">Handled</span></span>](#handled) | <span data-ttu-id="7799f-112">Si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="7799f-112">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="7799f-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="7799f-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="7799f-114">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="7799f-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="7799f-115">NewWindow</span><span class="sxs-lookup"><span data-stu-id="7799f-115">NewWindow</span></span>](#newwindow) | <span data-ttu-id="7799f-116">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="7799f-116">Gets the new window.</span></span>
[<span data-ttu-id="7799f-117">URI</span><span class="sxs-lookup"><span data-stu-id="7799f-117">Uri</span></span>](#uri) | <span data-ttu-id="7799f-118">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="7799f-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="7799f-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="7799f-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="7799f-120">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="7799f-120">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="7799f-121">El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="7799f-121">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="7799f-122">Miembros</span><span class="sxs-lookup"><span data-stu-id="7799f-122">Members</span></span>

#### <span data-ttu-id="7799f-123">Handled</span><span class="sxs-lookup"><span data-stu-id="7799f-123">Handled</span></span> 

<span data-ttu-id="7799f-124">Si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="7799f-124">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="7799f-125">bool público [Handled](#handled)</span><span class="sxs-lookup"><span data-stu-id="7799f-125">public bool [Handled](#handled)</span></span>

<span data-ttu-id="7799f-126">Si es falso y no se establece NewWindow, WebView abrirá una ventana emergente y se devolverá como WindowProxy abierto.</span><span class="sxs-lookup"><span data-stu-id="7799f-126">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="7799f-127">Si se establece en true y no se establece NewWindow para una Window. Open Call, el WindowProxy abierto será para un objeto de ventana ficticio y no se cargará ninguna ventana.</span><span class="sxs-lookup"><span data-stu-id="7799f-127">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="7799f-128">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="7799f-128">Default is false.</span></span>

#### <span data-ttu-id="7799f-129">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="7799f-129">IsUserInitiated</span></span> 

<span data-ttu-id="7799f-130">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="7799f-130">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="7799f-131">Public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="7799f-131">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="7799f-132">NewWindow</span><span class="sxs-lookup"><span data-stu-id="7799f-132">NewWindow</span></span> 

<span data-ttu-id="7799f-133">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="7799f-133">Gets the new window.</span></span>

> <span data-ttu-id="7799f-134">CoreWebView2 pública [NewWindow](#newwindow)</span><span class="sxs-lookup"><span data-stu-id="7799f-134">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="7799f-135">URI</span><span class="sxs-lookup"><span data-stu-id="7799f-135">Uri</span></span> 

<span data-ttu-id="7799f-136">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="7799f-136">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="7799f-137">[URI](#uri) de cadena pública</span><span class="sxs-lookup"><span data-stu-id="7799f-137">public string [Uri](#uri)</span></span>

<span data-ttu-id="7799f-138">No se debe navegar por la WebView de destino.</span><span class="sxs-lookup"><span data-stu-id="7799f-138">The target webview should not be navigated.</span></span> <span data-ttu-id="7799f-139">Si se establece NewWindow, la ventana de nivel superior volverá como la WindowProxy abierta.</span><span class="sxs-lookup"><span data-stu-id="7799f-139">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="7799f-140">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="7799f-140">GetDeferral</span></span> 

<span data-ttu-id="7799f-141">Obtén un objeto CoreWebView2Deferral y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="7799f-141">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="7799f-142">Public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="7799f-142">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="7799f-143">Puedes usar el objeto CoreWebView2Deferral para completar la solicitud de apertura de ventana más adelante.</span><span class="sxs-lookup"><span data-stu-id="7799f-143">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="7799f-144">Mientras se difiere este evento, se devolverá la ventana de apertura de WindowProxy a una ventana no navegada, que se desplazará cuando se complete el aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="7799f-144">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>


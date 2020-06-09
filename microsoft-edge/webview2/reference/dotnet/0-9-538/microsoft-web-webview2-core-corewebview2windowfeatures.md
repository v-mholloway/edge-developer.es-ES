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
ms.openlocfilehash: 9ee85620ece653a2312076f7b6f4fe9f6ca3da92
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699452"
---
# <span data-ttu-id="12318-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="12318-104">Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

> [!NOTE]
> <span data-ttu-id="12318-105">Esta es una [API experimental](../../../concepts/versioning.md#experimental-apis) que se incluía con nuestra versión [de SDK 0.9.538-prerelease](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="12318-105">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="12318-106">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="12318-106">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="12318-107">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="12318-107">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="12318-108">Características de la ventana de una ventana emergente de vista previa.</span><span class="sxs-lookup"><span data-stu-id="12318-108">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="12318-109">Resumen</span><span class="sxs-lookup"><span data-stu-id="12318-109">Summary</span></span>

 <span data-ttu-id="12318-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="12318-110">Members</span></span>                        | <span data-ttu-id="12318-111">Descripciones</span><span class="sxs-lookup"><span data-stu-id="12318-111">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="12318-112">Altura</span><span class="sxs-lookup"><span data-stu-id="12318-112">Height</span></span>](#height) | <span data-ttu-id="12318-113">El alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="12318-113">The height of the window.</span></span>
[<span data-ttu-id="12318-114">Izquierda</span><span class="sxs-lookup"><span data-stu-id="12318-114">Left</span></span>](#left) | <span data-ttu-id="12318-115">La posición izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="12318-115">The left position of the window.</span></span>
[<span data-ttu-id="12318-116">Barra</span><span class="sxs-lookup"><span data-stu-id="12318-116">MenuBar</span></span>](#menubar) | <span data-ttu-id="12318-117">Si se muestra o no la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="12318-117">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="12318-118">Barras</span><span class="sxs-lookup"><span data-stu-id="12318-118">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="12318-119">Si se muestran o no las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="12318-119">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="12318-120">Estado</span><span class="sxs-lookup"><span data-stu-id="12318-120">Status</span></span>](#status) | <span data-ttu-id="12318-121">Si desea o no agregar una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="12318-121">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="12318-122">Barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="12318-122">Toolbar</span></span>](#toolbar) | <span data-ttu-id="12318-123">Si desea que se muestre o no la barra de herramientas del explorador.</span><span class="sxs-lookup"><span data-stu-id="12318-123">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="12318-124">Top</span><span class="sxs-lookup"><span data-stu-id="12318-124">Top</span></span>](#top) | <span data-ttu-id="12318-125">La posición superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="12318-125">The top position of the window.</span></span>
[<span data-ttu-id="12318-126">Ancho</span><span class="sxs-lookup"><span data-stu-id="12318-126">Width</span></span>](#width) | <span data-ttu-id="12318-127">Ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="12318-127">The width of the window.</span></span>
[<span data-ttu-id="12318-128">HasPosition</span><span class="sxs-lookup"><span data-stu-id="12318-128">HasPosition</span></span>](#hasposition) | <span data-ttu-id="12318-129">Ha especificado valores de la izquierda y de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="12318-129">Has specified left and top values.</span></span>
[<span data-ttu-id="12318-130">HasSize</span><span class="sxs-lookup"><span data-stu-id="12318-130">HasSize</span></span>](#hassize) | <span data-ttu-id="12318-131">Ha especificado valores de alto y ancho.</span><span class="sxs-lookup"><span data-stu-id="12318-131">Has specified height and width values.</span></span>

## <span data-ttu-id="12318-132">Miembros</span><span class="sxs-lookup"><span data-stu-id="12318-132">Members</span></span>

#### <span data-ttu-id="12318-133">Altura</span><span class="sxs-lookup"><span data-stu-id="12318-133">Height</span></span> 

<span data-ttu-id="12318-134">El alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="12318-134">The height of the window.</span></span>

> <span data-ttu-id="12318-135">[alto](#height) de uint público</span><span class="sxs-lookup"><span data-stu-id="12318-135">public uint [Height](#height)</span></span>

#### <span data-ttu-id="12318-136">Izquierda</span><span class="sxs-lookup"><span data-stu-id="12318-136">Left</span></span> 

<span data-ttu-id="12318-137">La posición izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="12318-137">The left position of the window.</span></span>

> <span data-ttu-id="12318-138">uint público [restante](#left)</span><span class="sxs-lookup"><span data-stu-id="12318-138">public uint [Left](#left)</span></span>

<span data-ttu-id="12318-139">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="12318-139">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="12318-140">Barra</span><span class="sxs-lookup"><span data-stu-id="12318-140">MenuBar</span></span> 

<span data-ttu-id="12318-141">Si se muestra o no la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="12318-141">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="12318-142">[MenuBar](#menubar) de public int</span><span class="sxs-lookup"><span data-stu-id="12318-142">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="12318-143">Barras</span><span class="sxs-lookup"><span data-stu-id="12318-143">ScrollBars</span></span> 

<span data-ttu-id="12318-144">Si se muestran o no las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="12318-144">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="12318-145">Barras de [desplazamiento](#scrollbars) public int</span><span class="sxs-lookup"><span data-stu-id="12318-145">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="12318-146">Estado</span><span class="sxs-lookup"><span data-stu-id="12318-146">Status</span></span> 

<span data-ttu-id="12318-147">Si desea o no agregar una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="12318-147">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="12318-148">[Estado](#status) de public int</span><span class="sxs-lookup"><span data-stu-id="12318-148">public int [Status](#status)</span></span>

#### <span data-ttu-id="12318-149">Barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="12318-149">Toolbar</span></span> 

<span data-ttu-id="12318-150">Si desea que se muestre o no la barra de herramientas del explorador.</span><span class="sxs-lookup"><span data-stu-id="12318-150">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="12318-151">Barra de [herramientas](#toolbar) int pública</span><span class="sxs-lookup"><span data-stu-id="12318-151">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="12318-152">Top</span><span class="sxs-lookup"><span data-stu-id="12318-152">Top</span></span> 

<span data-ttu-id="12318-153">La posición superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="12318-153">The top position of the window.</span></span>

> <span data-ttu-id="12318-154">uint público [superior](#top)</span><span class="sxs-lookup"><span data-stu-id="12318-154">public uint [Top](#top)</span></span>

<span data-ttu-id="12318-155">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="12318-155">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="12318-156">Ancho</span><span class="sxs-lookup"><span data-stu-id="12318-156">Width</span></span> 

<span data-ttu-id="12318-157">Ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="12318-157">The width of the window.</span></span>

> <span data-ttu-id="12318-158">[ancho](#width) de uint público</span><span class="sxs-lookup"><span data-stu-id="12318-158">public uint [Width](#width)</span></span>

#### <span data-ttu-id="12318-159">HasPosition</span><span class="sxs-lookup"><span data-stu-id="12318-159">HasPosition</span></span> 

<span data-ttu-id="12318-160">Ha especificado valores de la izquierda y de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="12318-160">Has specified left and top values.</span></span>

> <span data-ttu-id="12318-161">public int [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="12318-161">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="12318-162">HasSize</span><span class="sxs-lookup"><span data-stu-id="12318-162">HasSize</span></span> 

<span data-ttu-id="12318-163">Ha especificado valores de alto y ancho.</span><span class="sxs-lookup"><span data-stu-id="12318-163">Has specified height and width values.</span></span>

> <span data-ttu-id="12318-164">public int [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="12318-164">public int [HasSize](#hassize)()</span></span>


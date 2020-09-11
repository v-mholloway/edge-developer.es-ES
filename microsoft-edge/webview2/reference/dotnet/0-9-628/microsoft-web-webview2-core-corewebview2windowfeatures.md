---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
ms.openlocfilehash: 41ae506965067b478c3cb588eed0c8029704c4a3
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012619"
---
# <span data-ttu-id="fba7c-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="fba7c-104">Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

<span data-ttu-id="fba7c-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="fba7c-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="fba7c-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="fba7c-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="fba7c-107">Características de la ventana de una ventana emergente de vista previa.</span><span class="sxs-lookup"><span data-stu-id="fba7c-107">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="fba7c-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="fba7c-108">Summary</span></span>

 <span data-ttu-id="fba7c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="fba7c-109">Members</span></span>                        | <span data-ttu-id="fba7c-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="fba7c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fba7c-111">Altura</span><span class="sxs-lookup"><span data-stu-id="fba7c-111">Height</span></span>](#height) | <span data-ttu-id="fba7c-112">El alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fba7c-112">The height of the window.</span></span>
[<span data-ttu-id="fba7c-113">Izquierda</span><span class="sxs-lookup"><span data-stu-id="fba7c-113">Left</span></span>](#left) | <span data-ttu-id="fba7c-114">La posición izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fba7c-114">The left position of the window.</span></span>
[<span data-ttu-id="fba7c-115">Barra</span><span class="sxs-lookup"><span data-stu-id="fba7c-115">MenuBar</span></span>](#menubar) | <span data-ttu-id="fba7c-116">Si se muestra o no la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="fba7c-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="fba7c-117">Barras</span><span class="sxs-lookup"><span data-stu-id="fba7c-117">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="fba7c-118">Si se muestran o no las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="fba7c-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="fba7c-119">Estado</span><span class="sxs-lookup"><span data-stu-id="fba7c-119">Status</span></span>](#status) | <span data-ttu-id="fba7c-120">Si desea o no agregar una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="fba7c-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="fba7c-121">Barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="fba7c-121">Toolbar</span></span>](#toolbar) | <span data-ttu-id="fba7c-122">Si desea que se muestre o no la barra de herramientas del explorador.</span><span class="sxs-lookup"><span data-stu-id="fba7c-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="fba7c-123">Top</span><span class="sxs-lookup"><span data-stu-id="fba7c-123">Top</span></span>](#top) | <span data-ttu-id="fba7c-124">La posición superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fba7c-124">The top position of the window.</span></span>
[<span data-ttu-id="fba7c-125">Ancho</span><span class="sxs-lookup"><span data-stu-id="fba7c-125">Width</span></span>](#width) | <span data-ttu-id="fba7c-126">Ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fba7c-126">The width of the window.</span></span>
[<span data-ttu-id="fba7c-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="fba7c-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="fba7c-128">Ha especificado valores de la izquierda y de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="fba7c-128">Has specified left and top values.</span></span>
[<span data-ttu-id="fba7c-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="fba7c-129">HasSize</span></span>](#hassize) | <span data-ttu-id="fba7c-130">Ha especificado valores de alto y ancho.</span><span class="sxs-lookup"><span data-stu-id="fba7c-130">Has specified height and width values.</span></span>

## <span data-ttu-id="fba7c-131">Miembros</span><span class="sxs-lookup"><span data-stu-id="fba7c-131">Members</span></span>

#### <span data-ttu-id="fba7c-132">Altura</span><span class="sxs-lookup"><span data-stu-id="fba7c-132">Height</span></span> 

<span data-ttu-id="fba7c-133">El alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fba7c-133">The height of the window.</span></span>

> <span data-ttu-id="fba7c-134">[alto](#height) de uint público</span><span class="sxs-lookup"><span data-stu-id="fba7c-134">public uint [Height](#height)</span></span>

#### <span data-ttu-id="fba7c-135">Izquierda</span><span class="sxs-lookup"><span data-stu-id="fba7c-135">Left</span></span> 

<span data-ttu-id="fba7c-136">La posición izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fba7c-136">The left position of the window.</span></span>

> <span data-ttu-id="fba7c-137">uint público [restante](#left)</span><span class="sxs-lookup"><span data-stu-id="fba7c-137">public uint [Left](#left)</span></span>

<span data-ttu-id="fba7c-138">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="fba7c-138">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="fba7c-139">Barra</span><span class="sxs-lookup"><span data-stu-id="fba7c-139">MenuBar</span></span> 

<span data-ttu-id="fba7c-140">Si se muestra o no la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="fba7c-140">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="fba7c-141">[MenuBar](#menubar) de public int</span><span class="sxs-lookup"><span data-stu-id="fba7c-141">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="fba7c-142">Barras</span><span class="sxs-lookup"><span data-stu-id="fba7c-142">ScrollBars</span></span> 

<span data-ttu-id="fba7c-143">Si se muestran o no las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="fba7c-143">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="fba7c-144">Barras de [desplazamiento](#scrollbars) public int</span><span class="sxs-lookup"><span data-stu-id="fba7c-144">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="fba7c-145">Estado</span><span class="sxs-lookup"><span data-stu-id="fba7c-145">Status</span></span> 

<span data-ttu-id="fba7c-146">Si desea o no agregar una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="fba7c-146">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="fba7c-147">[Estado](#status) de public int</span><span class="sxs-lookup"><span data-stu-id="fba7c-147">public int [Status](#status)</span></span>

#### <span data-ttu-id="fba7c-148">Barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="fba7c-148">Toolbar</span></span> 

<span data-ttu-id="fba7c-149">Si desea que se muestre o no la barra de herramientas del explorador.</span><span class="sxs-lookup"><span data-stu-id="fba7c-149">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="fba7c-150">Barra de [herramientas](#toolbar) int pública</span><span class="sxs-lookup"><span data-stu-id="fba7c-150">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="fba7c-151">Top</span><span class="sxs-lookup"><span data-stu-id="fba7c-151">Top</span></span> 

<span data-ttu-id="fba7c-152">La posición superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fba7c-152">The top position of the window.</span></span>

> <span data-ttu-id="fba7c-153">uint público [superior](#top)</span><span class="sxs-lookup"><span data-stu-id="fba7c-153">public uint [Top](#top)</span></span>

<span data-ttu-id="fba7c-154">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="fba7c-154">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="fba7c-155">Ancho</span><span class="sxs-lookup"><span data-stu-id="fba7c-155">Width</span></span> 

<span data-ttu-id="fba7c-156">Ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fba7c-156">The width of the window.</span></span>

> <span data-ttu-id="fba7c-157">[ancho](#width) de uint público</span><span class="sxs-lookup"><span data-stu-id="fba7c-157">public uint [Width](#width)</span></span>

#### <span data-ttu-id="fba7c-158">HasPosition</span><span class="sxs-lookup"><span data-stu-id="fba7c-158">HasPosition</span></span> 

<span data-ttu-id="fba7c-159">Ha especificado valores de la izquierda y de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="fba7c-159">Has specified left and top values.</span></span>

> <span data-ttu-id="fba7c-160">public int [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="fba7c-160">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="fba7c-161">HasSize</span><span class="sxs-lookup"><span data-stu-id="fba7c-161">HasSize</span></span> 

<span data-ttu-id="fba7c-162">Ha especificado valores de alto y ancho.</span><span class="sxs-lookup"><span data-stu-id="fba7c-162">Has specified height and width values.</span></span>

> <span data-ttu-id="fba7c-163">public int [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="fba7c-163">public int [HasSize](#hassize)()</span></span>


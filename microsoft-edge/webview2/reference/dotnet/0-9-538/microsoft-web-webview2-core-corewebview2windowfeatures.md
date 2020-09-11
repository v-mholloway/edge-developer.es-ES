---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
ms.openlocfilehash: 59e051c0537357fed89d6300db69ea479b656c7e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010519"
---
# <span data-ttu-id="6c8de-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures (clase)</span><span class="sxs-lookup"><span data-stu-id="6c8de-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="6c8de-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="6c8de-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="6c8de-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="6c8de-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="6c8de-107">Características de la ventana de una ventana emergente de vista previa.</span><span class="sxs-lookup"><span data-stu-id="6c8de-107">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="6c8de-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="6c8de-108">Summary</span></span>

 <span data-ttu-id="6c8de-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c8de-109">Members</span></span>                        | <span data-ttu-id="6c8de-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6c8de-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6c8de-111">Altura</span><span class="sxs-lookup"><span data-stu-id="6c8de-111">Height</span></span>](#height) | <span data-ttu-id="6c8de-112">El alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6c8de-112">The height of the window.</span></span>
[<span data-ttu-id="6c8de-113">Izquierda</span><span class="sxs-lookup"><span data-stu-id="6c8de-113">Left</span></span>](#left) | <span data-ttu-id="6c8de-114">La posición izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6c8de-114">The left position of the window.</span></span>
[<span data-ttu-id="6c8de-115">Barra</span><span class="sxs-lookup"><span data-stu-id="6c8de-115">MenuBar</span></span>](#menubar) | <span data-ttu-id="6c8de-116">Si se muestra o no la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="6c8de-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="6c8de-117">Barras</span><span class="sxs-lookup"><span data-stu-id="6c8de-117">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="6c8de-118">Si se muestran o no las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="6c8de-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="6c8de-119">Estado</span><span class="sxs-lookup"><span data-stu-id="6c8de-119">Status</span></span>](#status) | <span data-ttu-id="6c8de-120">Si desea o no agregar una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="6c8de-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="6c8de-121">Barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="6c8de-121">Toolbar</span></span>](#toolbar) | <span data-ttu-id="6c8de-122">Si desea que se muestre o no la barra de herramientas del explorador.</span><span class="sxs-lookup"><span data-stu-id="6c8de-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="6c8de-123">Top</span><span class="sxs-lookup"><span data-stu-id="6c8de-123">Top</span></span>](#top) | <span data-ttu-id="6c8de-124">La posición superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6c8de-124">The top position of the window.</span></span>
[<span data-ttu-id="6c8de-125">Ancho</span><span class="sxs-lookup"><span data-stu-id="6c8de-125">Width</span></span>](#width) | <span data-ttu-id="6c8de-126">Ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6c8de-126">The width of the window.</span></span>
[<span data-ttu-id="6c8de-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="6c8de-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="6c8de-128">Ha especificado valores de la izquierda y de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="6c8de-128">Has specified left and top values.</span></span>
[<span data-ttu-id="6c8de-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="6c8de-129">HasSize</span></span>](#hassize) | <span data-ttu-id="6c8de-130">Ha especificado valores de alto y ancho.</span><span class="sxs-lookup"><span data-stu-id="6c8de-130">Has specified height and width values.</span></span>

## <span data-ttu-id="6c8de-131">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c8de-131">Members</span></span>

#### <span data-ttu-id="6c8de-132">Altura</span><span class="sxs-lookup"><span data-stu-id="6c8de-132">Height</span></span> 

<span data-ttu-id="6c8de-133">El alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6c8de-133">The height of the window.</span></span>

> <span data-ttu-id="6c8de-134">[alto](#height) de uint público</span><span class="sxs-lookup"><span data-stu-id="6c8de-134">public uint [Height](#height)</span></span>

#### <span data-ttu-id="6c8de-135">Izquierda</span><span class="sxs-lookup"><span data-stu-id="6c8de-135">Left</span></span> 

<span data-ttu-id="6c8de-136">La posición izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6c8de-136">The left position of the window.</span></span>

> <span data-ttu-id="6c8de-137">uint público [restante](#left)</span><span class="sxs-lookup"><span data-stu-id="6c8de-137">public uint [Left](#left)</span></span>

<span data-ttu-id="6c8de-138">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="6c8de-138">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="6c8de-139">Barra</span><span class="sxs-lookup"><span data-stu-id="6c8de-139">MenuBar</span></span> 

<span data-ttu-id="6c8de-140">Si se muestra o no la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="6c8de-140">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="6c8de-141">[MenuBar](#menubar) de public int</span><span class="sxs-lookup"><span data-stu-id="6c8de-141">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="6c8de-142">Barras</span><span class="sxs-lookup"><span data-stu-id="6c8de-142">ScrollBars</span></span> 

<span data-ttu-id="6c8de-143">Si se muestran o no las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="6c8de-143">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="6c8de-144">Barras de [desplazamiento](#scrollbars) public int</span><span class="sxs-lookup"><span data-stu-id="6c8de-144">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="6c8de-145">Estado</span><span class="sxs-lookup"><span data-stu-id="6c8de-145">Status</span></span> 

<span data-ttu-id="6c8de-146">Si desea o no agregar una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="6c8de-146">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="6c8de-147">[Estado](#status) de public int</span><span class="sxs-lookup"><span data-stu-id="6c8de-147">public int [Status](#status)</span></span>

#### <span data-ttu-id="6c8de-148">Barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="6c8de-148">Toolbar</span></span> 

<span data-ttu-id="6c8de-149">Si desea que se muestre o no la barra de herramientas del explorador.</span><span class="sxs-lookup"><span data-stu-id="6c8de-149">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="6c8de-150">Barra de [herramientas](#toolbar) int pública</span><span class="sxs-lookup"><span data-stu-id="6c8de-150">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="6c8de-151">Top</span><span class="sxs-lookup"><span data-stu-id="6c8de-151">Top</span></span> 

<span data-ttu-id="6c8de-152">La posición superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6c8de-152">The top position of the window.</span></span>

> <span data-ttu-id="6c8de-153">uint público [superior](#top)</span><span class="sxs-lookup"><span data-stu-id="6c8de-153">public uint [Top](#top)</span></span>

<span data-ttu-id="6c8de-154">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="6c8de-154">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="6c8de-155">Ancho</span><span class="sxs-lookup"><span data-stu-id="6c8de-155">Width</span></span> 

<span data-ttu-id="6c8de-156">Ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6c8de-156">The width of the window.</span></span>

> <span data-ttu-id="6c8de-157">[ancho](#width) de uint público</span><span class="sxs-lookup"><span data-stu-id="6c8de-157">public uint [Width](#width)</span></span>

#### <span data-ttu-id="6c8de-158">HasPosition</span><span class="sxs-lookup"><span data-stu-id="6c8de-158">HasPosition</span></span> 

<span data-ttu-id="6c8de-159">Ha especificado valores de la izquierda y de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="6c8de-159">Has specified left and top values.</span></span>

> <span data-ttu-id="6c8de-160">public int [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="6c8de-160">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="6c8de-161">HasSize</span><span class="sxs-lookup"><span data-stu-id="6c8de-161">HasSize</span></span> 

<span data-ttu-id="6c8de-162">Ha especificado valores de alto y ancho.</span><span class="sxs-lookup"><span data-stu-id="6c8de-162">Has specified height and width values.</span></span>

> <span data-ttu-id="6c8de-163">public int [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="6c8de-163">public int [HasSize](#hassize)()</span></span>


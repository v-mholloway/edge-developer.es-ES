---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
ms.openlocfilehash: d6d6f52456823488c07288c8ed07b9655a29883a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884440"
---
# <span data-ttu-id="f125e-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="f125e-104">Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="f125e-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f125e-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f125e-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="f125e-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f125e-107">Características de la ventana de una ventana emergente de vista previa.</span><span class="sxs-lookup"><span data-stu-id="f125e-107">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="f125e-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="f125e-108">Summary</span></span>

 <span data-ttu-id="f125e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="f125e-109">Members</span></span>                        | <span data-ttu-id="f125e-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="f125e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f125e-111">Altura</span><span class="sxs-lookup"><span data-stu-id="f125e-111">Height</span></span>](#height) | <span data-ttu-id="f125e-112">El alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="f125e-112">The height of the window.</span></span>
[<span data-ttu-id="f125e-113">Izquierda</span><span class="sxs-lookup"><span data-stu-id="f125e-113">Left</span></span>](#left) | <span data-ttu-id="f125e-114">La posición izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="f125e-114">The left position of the window.</span></span>
[<span data-ttu-id="f125e-115">Barra</span><span class="sxs-lookup"><span data-stu-id="f125e-115">MenuBar</span></span>](#menubar) | <span data-ttu-id="f125e-116">Si se muestra o no la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="f125e-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="f125e-117">Barras</span><span class="sxs-lookup"><span data-stu-id="f125e-117">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="f125e-118">Si se muestran o no las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="f125e-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="f125e-119">Estado</span><span class="sxs-lookup"><span data-stu-id="f125e-119">Status</span></span>](#status) | <span data-ttu-id="f125e-120">Si desea o no agregar una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="f125e-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="f125e-121">Barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="f125e-121">Toolbar</span></span>](#toolbar) | <span data-ttu-id="f125e-122">Si desea que se muestre o no la barra de herramientas del explorador.</span><span class="sxs-lookup"><span data-stu-id="f125e-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="f125e-123">Top</span><span class="sxs-lookup"><span data-stu-id="f125e-123">Top</span></span>](#top) | <span data-ttu-id="f125e-124">La posición superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="f125e-124">The top position of the window.</span></span>
[<span data-ttu-id="f125e-125">Ancho</span><span class="sxs-lookup"><span data-stu-id="f125e-125">Width</span></span>](#width) | <span data-ttu-id="f125e-126">Ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="f125e-126">The width of the window.</span></span>
[<span data-ttu-id="f125e-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="f125e-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="f125e-128">Ha especificado valores de la izquierda y de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="f125e-128">Has specified left and top values.</span></span>
[<span data-ttu-id="f125e-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="f125e-129">HasSize</span></span>](#hassize) | <span data-ttu-id="f125e-130">Ha especificado valores de alto y ancho.</span><span class="sxs-lookup"><span data-stu-id="f125e-130">Has specified height and width values.</span></span>

## <span data-ttu-id="f125e-131">Miembros</span><span class="sxs-lookup"><span data-stu-id="f125e-131">Members</span></span>

#### <span data-ttu-id="f125e-132">Altura</span><span class="sxs-lookup"><span data-stu-id="f125e-132">Height</span></span> 

<span data-ttu-id="f125e-133">El alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="f125e-133">The height of the window.</span></span>

> <span data-ttu-id="f125e-134">[alto](#height) de uint público</span><span class="sxs-lookup"><span data-stu-id="f125e-134">public uint [Height](#height)</span></span>

#### <span data-ttu-id="f125e-135">Izquierda</span><span class="sxs-lookup"><span data-stu-id="f125e-135">Left</span></span> 

<span data-ttu-id="f125e-136">La posición izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="f125e-136">The left position of the window.</span></span>

> <span data-ttu-id="f125e-137">uint público [restante](#left)</span><span class="sxs-lookup"><span data-stu-id="f125e-137">public uint [Left](#left)</span></span>

<span data-ttu-id="f125e-138">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="f125e-138">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="f125e-139">Barra</span><span class="sxs-lookup"><span data-stu-id="f125e-139">MenuBar</span></span> 

<span data-ttu-id="f125e-140">Si se muestra o no la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="f125e-140">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="f125e-141">[MenuBar](#menubar) de public int</span><span class="sxs-lookup"><span data-stu-id="f125e-141">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="f125e-142">Barras</span><span class="sxs-lookup"><span data-stu-id="f125e-142">ScrollBars</span></span> 

<span data-ttu-id="f125e-143">Si se muestran o no las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="f125e-143">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="f125e-144">Barras de [desplazamiento](#scrollbars) public int</span><span class="sxs-lookup"><span data-stu-id="f125e-144">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="f125e-145">Estado</span><span class="sxs-lookup"><span data-stu-id="f125e-145">Status</span></span> 

<span data-ttu-id="f125e-146">Si desea o no agregar una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="f125e-146">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="f125e-147">[Estado](#status) de public int</span><span class="sxs-lookup"><span data-stu-id="f125e-147">public int [Status](#status)</span></span>

#### <span data-ttu-id="f125e-148">Barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="f125e-148">Toolbar</span></span> 

<span data-ttu-id="f125e-149">Si desea que se muestre o no la barra de herramientas del explorador.</span><span class="sxs-lookup"><span data-stu-id="f125e-149">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="f125e-150">Barra de [herramientas](#toolbar) int pública</span><span class="sxs-lookup"><span data-stu-id="f125e-150">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="f125e-151">Top</span><span class="sxs-lookup"><span data-stu-id="f125e-151">Top</span></span> 

<span data-ttu-id="f125e-152">La posición superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="f125e-152">The top position of the window.</span></span>

> <span data-ttu-id="f125e-153">uint público [superior](#top)</span><span class="sxs-lookup"><span data-stu-id="f125e-153">public uint [Top](#top)</span></span>

<span data-ttu-id="f125e-154">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="f125e-154">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="f125e-155">Ancho</span><span class="sxs-lookup"><span data-stu-id="f125e-155">Width</span></span> 

<span data-ttu-id="f125e-156">Ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="f125e-156">The width of the window.</span></span>

> <span data-ttu-id="f125e-157">[ancho](#width) de uint público</span><span class="sxs-lookup"><span data-stu-id="f125e-157">public uint [Width](#width)</span></span>

#### <span data-ttu-id="f125e-158">HasPosition</span><span class="sxs-lookup"><span data-stu-id="f125e-158">HasPosition</span></span> 

<span data-ttu-id="f125e-159">Ha especificado valores de la izquierda y de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="f125e-159">Has specified left and top values.</span></span>

> <span data-ttu-id="f125e-160">public int [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="f125e-160">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="f125e-161">HasSize</span><span class="sxs-lookup"><span data-stu-id="f125e-161">HasSize</span></span> 

<span data-ttu-id="f125e-162">Ha especificado valores de alto y ancho.</span><span class="sxs-lookup"><span data-stu-id="f125e-162">Has specified height and width values.</span></span>

> <span data-ttu-id="f125e-163">public int [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="f125e-163">public int [HasSize](#hassize)()</span></span>


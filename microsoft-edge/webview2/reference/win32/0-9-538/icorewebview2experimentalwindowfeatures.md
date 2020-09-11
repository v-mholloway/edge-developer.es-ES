---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalWindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalWindowFeatures
ms.openlocfilehash: ee740f7d227ae98d451ba1c5e8f1017fe92514a8
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011373"
---
# <span data-ttu-id="71069-104">0.9.579: ICoreWebView2ExperimentalWindowFeatures</span><span class="sxs-lookup"><span data-stu-id="71069-104">0.9.579 - interface ICoreWebView2ExperimentalWindowFeatures</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

<span data-ttu-id="71069-105">Características de la ventana de una ventana emergente de vista previa.</span><span class="sxs-lookup"><span data-stu-id="71069-105">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="71069-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="71069-106">Summary</span></span>

 <span data-ttu-id="71069-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="71069-107">Members</span></span>                        | <span data-ttu-id="71069-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="71069-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="71069-109">get_Height</span><span class="sxs-lookup"><span data-stu-id="71069-109">get_Height</span></span>](#get_height) | <span data-ttu-id="71069-110">El alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="71069-110">The height of the window.</span></span>
[<span data-ttu-id="71069-111">get_Left</span><span class="sxs-lookup"><span data-stu-id="71069-111">get_Left</span></span>](#get_left) | <span data-ttu-id="71069-112">La posición izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="71069-112">The left position of the window.</span></span> <span data-ttu-id="71069-113">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="71069-113">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="71069-114">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="71069-114">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="71069-115">Si se muestra o no la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="71069-115">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="71069-116">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="71069-116">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="71069-117">Si se muestran o no las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="71069-117">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="71069-118">get_Status</span><span class="sxs-lookup"><span data-stu-id="71069-118">get_Status</span></span>](#get_status) | <span data-ttu-id="71069-119">Si desea o no agregar una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="71069-119">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="71069-120">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="71069-120">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="71069-121">Si desea que se muestre o no la barra de herramientas del explorador.</span><span class="sxs-lookup"><span data-stu-id="71069-121">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="71069-122">get_Top</span><span class="sxs-lookup"><span data-stu-id="71069-122">get_Top</span></span>](#get_top) | <span data-ttu-id="71069-123">La posición superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="71069-123">The top position of the window.</span></span> <span data-ttu-id="71069-124">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="71069-124">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="71069-125">get_Width</span><span class="sxs-lookup"><span data-stu-id="71069-125">get_Width</span></span>](#get_width) | <span data-ttu-id="71069-126">Ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="71069-126">The width of the window.</span></span>
[<span data-ttu-id="71069-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="71069-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="71069-128">Ha especificado valores de la izquierda y de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="71069-128">Has specified left and top values.</span></span>
[<span data-ttu-id="71069-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="71069-129">HasSize</span></span>](#hassize) | <span data-ttu-id="71069-130">Ha especificado valores de alto y ancho.</span><span class="sxs-lookup"><span data-stu-id="71069-130">Has specified height and width values.</span></span>

<span data-ttu-id="71069-131">Estos campos coinciden con el ' windowFeatures ' pasado a Window. Open según lo especificado en [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="71069-131">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="71069-132">Miembros</span><span class="sxs-lookup"><span data-stu-id="71069-132">Members</span></span>

#### <span data-ttu-id="71069-133">get_Height</span><span class="sxs-lookup"><span data-stu-id="71069-133">get_Height</span></span> 

<span data-ttu-id="71069-134">El alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="71069-134">The height of the window.</span></span>

> <span data-ttu-id="71069-135">[get_Height](#get_height)de HRESULT público (UINT32 \* height)</span><span class="sxs-lookup"><span data-stu-id="71069-135">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="71069-136">El valor mínimo es 100.</span><span class="sxs-lookup"><span data-stu-id="71069-136">Minimum value is 100.</span></span> <span data-ttu-id="71069-137">Dará un error si HasSize es falso.</span><span class="sxs-lookup"><span data-stu-id="71069-137">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="71069-138">get_Left</span><span class="sxs-lookup"><span data-stu-id="71069-138">get_Left</span></span> 

<span data-ttu-id="71069-139">La posición izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="71069-139">The left position of the window.</span></span> <span data-ttu-id="71069-140">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="71069-140">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="71069-141">[get_Left](#get_left)de HRESULT público (UINT32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="71069-141">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="71069-142">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="71069-142">get_MenuBar</span></span> 

<span data-ttu-id="71069-143">Si se muestra o no la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="71069-143">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="71069-144">[get_MenuBar](#get_menubar)de HRESULT público (bool \* MenuBar)</span><span class="sxs-lookup"><span data-stu-id="71069-144">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="71069-145">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="71069-145">get_ScrollBars</span></span> 

<span data-ttu-id="71069-146">Si se muestran o no las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="71069-146">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="71069-147">[get_ScrollBars](#get_scrollbars)de HRESULT público (bool \* ScrollBars)</span><span class="sxs-lookup"><span data-stu-id="71069-147">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="71069-148">get_Status</span><span class="sxs-lookup"><span data-stu-id="71069-148">get_Status</span></span> 

<span data-ttu-id="71069-149">Si desea o no agregar una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="71069-149">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="71069-150">[get_Status](#get_status)de HRESULT público (bool \* status)</span><span class="sxs-lookup"><span data-stu-id="71069-150">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="71069-151">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="71069-151">get_Toolbar</span></span> 

<span data-ttu-id="71069-152">Si desea que se muestre o no la barra de herramientas del explorador.</span><span class="sxs-lookup"><span data-stu-id="71069-152">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="71069-153">[get_Toolbar](#get_toolbar)de HRESULT público (una barra de herramientas de bool \*)</span><span class="sxs-lookup"><span data-stu-id="71069-153">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="71069-154">get_Top</span><span class="sxs-lookup"><span data-stu-id="71069-154">get_Top</span></span> 

<span data-ttu-id="71069-155">La posición superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="71069-155">The top position of the window.</span></span> <span data-ttu-id="71069-156">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="71069-156">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="71069-157">[get_Top](#get_top)de HRESULT público (UINT32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="71069-157">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="71069-158">get_Width</span><span class="sxs-lookup"><span data-stu-id="71069-158">get_Width</span></span> 

<span data-ttu-id="71069-159">Ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="71069-159">The width of the window.</span></span>

> <span data-ttu-id="71069-160">[get_Width](#get_width)de HRESULT público (UINT32 \* width)</span><span class="sxs-lookup"><span data-stu-id="71069-160">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="71069-161">El valor mínimo es 100.</span><span class="sxs-lookup"><span data-stu-id="71069-161">Minimum value is 100.</span></span> <span data-ttu-id="71069-162">Dará un error si HasSize es falso.</span><span class="sxs-lookup"><span data-stu-id="71069-162">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="71069-163">HasPosition</span><span class="sxs-lookup"><span data-stu-id="71069-163">HasPosition</span></span> 

<span data-ttu-id="71069-164">Ha especificado valores de la izquierda y de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="71069-164">Has specified left and top values.</span></span>

> <span data-ttu-id="71069-165">[HASPOSITION](#hasposition)HRESULT público (bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="71069-165">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="71069-166">HasSize</span><span class="sxs-lookup"><span data-stu-id="71069-166">HasSize</span></span> 

<span data-ttu-id="71069-167">Ha especificado valores de alto y ancho.</span><span class="sxs-lookup"><span data-stu-id="71069-167">Has specified height and width values.</span></span>

> <span data-ttu-id="71069-168">[HASSIZE](#hassize)HRESULT público (bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="71069-168">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>


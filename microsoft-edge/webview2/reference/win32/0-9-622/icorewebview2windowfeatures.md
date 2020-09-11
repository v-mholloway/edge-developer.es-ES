---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2WindowFeatures
ms.openlocfilehash: 90b5a09a752250dc342e7eefad031c9b5b83d345
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012701"
---
# <span data-ttu-id="80586-104">interfaz ICoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="80586-104">interface ICoreWebView2WindowFeatures</span></span> 

```
interface ICoreWebView2WindowFeatures
  : public IUnknown
```

<span data-ttu-id="80586-105">Características de la ventana de una ventana emergente de vista previa.</span><span class="sxs-lookup"><span data-stu-id="80586-105">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="80586-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="80586-106">Summary</span></span>

 <span data-ttu-id="80586-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="80586-107">Members</span></span>                        | <span data-ttu-id="80586-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="80586-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="80586-109">get_Height</span><span class="sxs-lookup"><span data-stu-id="80586-109">get_Height</span></span>](#get_height) | <span data-ttu-id="80586-110">El alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="80586-110">The height of the window.</span></span>
[<span data-ttu-id="80586-111">get_Left</span><span class="sxs-lookup"><span data-stu-id="80586-111">get_Left</span></span>](#get_left) | <span data-ttu-id="80586-112">La posición izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="80586-112">The left position of the window.</span></span> <span data-ttu-id="80586-113">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="80586-113">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="80586-114">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="80586-114">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="80586-115">Si se muestra o no la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="80586-115">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="80586-116">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="80586-116">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="80586-117">Si se muestran o no las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="80586-117">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="80586-118">get_Status</span><span class="sxs-lookup"><span data-stu-id="80586-118">get_Status</span></span>](#get_status) | <span data-ttu-id="80586-119">Si desea o no agregar una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="80586-119">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="80586-120">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="80586-120">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="80586-121">Si desea que se muestre o no la barra de herramientas del explorador.</span><span class="sxs-lookup"><span data-stu-id="80586-121">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="80586-122">get_Top</span><span class="sxs-lookup"><span data-stu-id="80586-122">get_Top</span></span>](#get_top) | <span data-ttu-id="80586-123">La posición superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="80586-123">The top position of the window.</span></span> <span data-ttu-id="80586-124">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="80586-124">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="80586-125">get_Width</span><span class="sxs-lookup"><span data-stu-id="80586-125">get_Width</span></span>](#get_width) | <span data-ttu-id="80586-126">Ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="80586-126">The width of the window.</span></span>
[<span data-ttu-id="80586-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="80586-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="80586-128">Ha especificado valores de la izquierda y de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="80586-128">Has specified left and top values.</span></span>
[<span data-ttu-id="80586-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="80586-129">HasSize</span></span>](#hassize) | <span data-ttu-id="80586-130">Ha especificado valores de alto y ancho.</span><span class="sxs-lookup"><span data-stu-id="80586-130">Has specified height and width values.</span></span>

<span data-ttu-id="80586-131">Estos campos coinciden con el ' windowFeatures ' pasado a Window. Open según lo especificado en [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="80586-131">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="80586-132">Miembros</span><span class="sxs-lookup"><span data-stu-id="80586-132">Members</span></span>

#### <span data-ttu-id="80586-133">get_Height</span><span class="sxs-lookup"><span data-stu-id="80586-133">get_Height</span></span> 

<span data-ttu-id="80586-134">El alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="80586-134">The height of the window.</span></span>

> <span data-ttu-id="80586-135">[get_Height](#get_height)de HRESULT público (UINT32 \* height)</span><span class="sxs-lookup"><span data-stu-id="80586-135">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="80586-136">El valor mínimo es 100.</span><span class="sxs-lookup"><span data-stu-id="80586-136">Minimum value is 100.</span></span> <span data-ttu-id="80586-137">Dará un error si HasSize es falso.</span><span class="sxs-lookup"><span data-stu-id="80586-137">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="80586-138">get_Left</span><span class="sxs-lookup"><span data-stu-id="80586-138">get_Left</span></span> 

<span data-ttu-id="80586-139">La posición izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="80586-139">The left position of the window.</span></span> <span data-ttu-id="80586-140">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="80586-140">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="80586-141">[get_Left](#get_left)de HRESULT público (UINT32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="80586-141">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="80586-142">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="80586-142">get_MenuBar</span></span> 

<span data-ttu-id="80586-143">Si se muestra o no la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="80586-143">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="80586-144">[get_MenuBar](#get_menubar)de HRESULT público (bool \* MenuBar)</span><span class="sxs-lookup"><span data-stu-id="80586-144">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="80586-145">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="80586-145">get_ScrollBars</span></span> 

<span data-ttu-id="80586-146">Si se muestran o no las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="80586-146">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="80586-147">[get_ScrollBars](#get_scrollbars)de HRESULT público (bool \* ScrollBars)</span><span class="sxs-lookup"><span data-stu-id="80586-147">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="80586-148">get_Status</span><span class="sxs-lookup"><span data-stu-id="80586-148">get_Status</span></span> 

<span data-ttu-id="80586-149">Si desea o no agregar una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="80586-149">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="80586-150">[get_Status](#get_status)de HRESULT público (bool \* status)</span><span class="sxs-lookup"><span data-stu-id="80586-150">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="80586-151">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="80586-151">get_Toolbar</span></span> 

<span data-ttu-id="80586-152">Si desea que se muestre o no la barra de herramientas del explorador.</span><span class="sxs-lookup"><span data-stu-id="80586-152">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="80586-153">[get_Toolbar](#get_toolbar)de HRESULT público (una barra de herramientas de bool \*)</span><span class="sxs-lookup"><span data-stu-id="80586-153">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="80586-154">get_Top</span><span class="sxs-lookup"><span data-stu-id="80586-154">get_Top</span></span> 

<span data-ttu-id="80586-155">La posición superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="80586-155">The top position of the window.</span></span> <span data-ttu-id="80586-156">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="80586-156">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="80586-157">[get_Top](#get_top)de HRESULT público (UINT32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="80586-157">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="80586-158">get_Width</span><span class="sxs-lookup"><span data-stu-id="80586-158">get_Width</span></span> 

<span data-ttu-id="80586-159">Ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="80586-159">The width of the window.</span></span>

> <span data-ttu-id="80586-160">[get_Width](#get_width)de HRESULT público (UINT32 \* width)</span><span class="sxs-lookup"><span data-stu-id="80586-160">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="80586-161">El valor mínimo es 100.</span><span class="sxs-lookup"><span data-stu-id="80586-161">Minimum value is 100.</span></span> <span data-ttu-id="80586-162">Dará un error si HasSize es falso.</span><span class="sxs-lookup"><span data-stu-id="80586-162">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="80586-163">HasPosition</span><span class="sxs-lookup"><span data-stu-id="80586-163">HasPosition</span></span> 

<span data-ttu-id="80586-164">Ha especificado valores de la izquierda y de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="80586-164">Has specified left and top values.</span></span>

> <span data-ttu-id="80586-165">[HASPOSITION](#hasposition)HRESULT público (bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="80586-165">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="80586-166">HasSize</span><span class="sxs-lookup"><span data-stu-id="80586-166">HasSize</span></span> 

<span data-ttu-id="80586-167">Ha especificado valores de alto y ancho.</span><span class="sxs-lookup"><span data-stu-id="80586-167">Has specified height and width values.</span></span>

> <span data-ttu-id="80586-168">[HASSIZE](#hassize)HRESULT público (bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="80586-168">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>


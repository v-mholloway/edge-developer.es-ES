---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalWindowFeatures
ms.openlocfilehash: 8b56d16e9c78738e9aa61e8c4c5b841b7fe4932f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879908"
---
# <span data-ttu-id="7f533-104">interfaz ICoreWebView2ExperimentalWindowFeatures</span><span class="sxs-lookup"><span data-stu-id="7f533-104">interface ICoreWebView2ExperimentalWindowFeatures</span></span> 

> [!NOTE]
> <span data-ttu-id="7f533-105">Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="7f533-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

<span data-ttu-id="7f533-106">Características de la ventana de una ventana emergente de vista previa.</span><span class="sxs-lookup"><span data-stu-id="7f533-106">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="7f533-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="7f533-107">Summary</span></span>

 <span data-ttu-id="7f533-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7f533-108">Members</span></span>                        | <span data-ttu-id="7f533-109">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7f533-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7f533-110">get_Height</span><span class="sxs-lookup"><span data-stu-id="7f533-110">get_Height</span></span>](#get_height) | <span data-ttu-id="7f533-111">El alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="7f533-111">The height of the window.</span></span>
[<span data-ttu-id="7f533-112">get_Left</span><span class="sxs-lookup"><span data-stu-id="7f533-112">get_Left</span></span>](#get_left) | <span data-ttu-id="7f533-113">La posición izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="7f533-113">The left position of the window.</span></span> <span data-ttu-id="7f533-114">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="7f533-114">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="7f533-115">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="7f533-115">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="7f533-116">Si se muestra o no la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="7f533-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="7f533-117">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="7f533-117">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="7f533-118">Si se muestran o no las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="7f533-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="7f533-119">get_Status</span><span class="sxs-lookup"><span data-stu-id="7f533-119">get_Status</span></span>](#get_status) | <span data-ttu-id="7f533-120">Si desea o no agregar una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="7f533-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="7f533-121">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="7f533-121">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="7f533-122">Si desea que se muestre o no la barra de herramientas del explorador.</span><span class="sxs-lookup"><span data-stu-id="7f533-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="7f533-123">get_Top</span><span class="sxs-lookup"><span data-stu-id="7f533-123">get_Top</span></span>](#get_top) | <span data-ttu-id="7f533-124">La posición superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="7f533-124">The top position of the window.</span></span> <span data-ttu-id="7f533-125">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="7f533-125">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="7f533-126">get_Width</span><span class="sxs-lookup"><span data-stu-id="7f533-126">get_Width</span></span>](#get_width) | <span data-ttu-id="7f533-127">Ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="7f533-127">The width of the window.</span></span>
[<span data-ttu-id="7f533-128">HasPosition</span><span class="sxs-lookup"><span data-stu-id="7f533-128">HasPosition</span></span>](#hasposition) | <span data-ttu-id="7f533-129">Ha especificado valores de la izquierda y de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="7f533-129">Has specified left and top values.</span></span>
[<span data-ttu-id="7f533-130">HasSize</span><span class="sxs-lookup"><span data-stu-id="7f533-130">HasSize</span></span>](#hassize) | <span data-ttu-id="7f533-131">Ha especificado valores de alto y ancho.</span><span class="sxs-lookup"><span data-stu-id="7f533-131">Has specified height and width values.</span></span>

<span data-ttu-id="7f533-132">Estos campos coinciden con el ' windowFeatures ' pasado a Window. Open según lo especificado en[https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="7f533-132">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="7f533-133">Miembros</span><span class="sxs-lookup"><span data-stu-id="7f533-133">Members</span></span>

#### <span data-ttu-id="7f533-134">get_Height</span><span class="sxs-lookup"><span data-stu-id="7f533-134">get_Height</span></span> 

<span data-ttu-id="7f533-135">El alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="7f533-135">The height of the window.</span></span>

> <span data-ttu-id="7f533-136">[get_Height](#get_height)de HRESULT público (UINT32 \* height)</span><span class="sxs-lookup"><span data-stu-id="7f533-136">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="7f533-137">El valor mínimo es 100.</span><span class="sxs-lookup"><span data-stu-id="7f533-137">Minimum value is 100.</span></span> <span data-ttu-id="7f533-138">Dará un error si HasSize es falso.</span><span class="sxs-lookup"><span data-stu-id="7f533-138">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="7f533-139">get_Left</span><span class="sxs-lookup"><span data-stu-id="7f533-139">get_Left</span></span> 

<span data-ttu-id="7f533-140">La posición izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="7f533-140">The left position of the window.</span></span> <span data-ttu-id="7f533-141">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="7f533-141">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="7f533-142">[get_Left](#get_left)de HRESULT público (UINT32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="7f533-142">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="7f533-143">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="7f533-143">get_MenuBar</span></span> 

<span data-ttu-id="7f533-144">Si se muestra o no la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="7f533-144">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="7f533-145">[get_MenuBar](#get_menubar)de HRESULT público (bool \* MenuBar)</span><span class="sxs-lookup"><span data-stu-id="7f533-145">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="7f533-146">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="7f533-146">get_ScrollBars</span></span> 

<span data-ttu-id="7f533-147">Si se muestran o no las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="7f533-147">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="7f533-148">[get_ScrollBars](#get_scrollbars)de HRESULT público (bool \* ScrollBars)</span><span class="sxs-lookup"><span data-stu-id="7f533-148">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="7f533-149">get_Status</span><span class="sxs-lookup"><span data-stu-id="7f533-149">get_Status</span></span> 

<span data-ttu-id="7f533-150">Si desea o no agregar una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="7f533-150">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="7f533-151">[get_Status](#get_status)de HRESULT público (bool \* status)</span><span class="sxs-lookup"><span data-stu-id="7f533-151">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="7f533-152">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="7f533-152">get_Toolbar</span></span> 

<span data-ttu-id="7f533-153">Si desea que se muestre o no la barra de herramientas del explorador.</span><span class="sxs-lookup"><span data-stu-id="7f533-153">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="7f533-154">[get_Toolbar](#get_toolbar)de HRESULT público (una barra de herramientas de bool \*)</span><span class="sxs-lookup"><span data-stu-id="7f533-154">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="7f533-155">get_Top</span><span class="sxs-lookup"><span data-stu-id="7f533-155">get_Top</span></span> 

<span data-ttu-id="7f533-156">La posición superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="7f533-156">The top position of the window.</span></span> <span data-ttu-id="7f533-157">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="7f533-157">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="7f533-158">[get_Top](#get_top)de HRESULT público (UINT32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="7f533-158">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="7f533-159">get_Width</span><span class="sxs-lookup"><span data-stu-id="7f533-159">get_Width</span></span> 

<span data-ttu-id="7f533-160">Ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="7f533-160">The width of the window.</span></span>

> <span data-ttu-id="7f533-161">[get_Width](#get_width)de HRESULT público (UINT32 \* width)</span><span class="sxs-lookup"><span data-stu-id="7f533-161">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="7f533-162">El valor mínimo es 100.</span><span class="sxs-lookup"><span data-stu-id="7f533-162">Minimum value is 100.</span></span> <span data-ttu-id="7f533-163">Dará un error si HasSize es falso.</span><span class="sxs-lookup"><span data-stu-id="7f533-163">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="7f533-164">HasPosition</span><span class="sxs-lookup"><span data-stu-id="7f533-164">HasPosition</span></span> 

<span data-ttu-id="7f533-165">Ha especificado valores de la izquierda y de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="7f533-165">Has specified left and top values.</span></span>

> <span data-ttu-id="7f533-166">[HASPOSITION](#hasposition)HRESULT público (bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="7f533-166">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="7f533-167">HasSize</span><span class="sxs-lookup"><span data-stu-id="7f533-167">HasSize</span></span> 

<span data-ttu-id="7f533-168">Ha especificado valores de alto y ancho.</span><span class="sxs-lookup"><span data-stu-id="7f533-168">Has specified height and width values.</span></span>

> <span data-ttu-id="7f533-169">[HASSIZE](#hassize)HRESULT público (bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="7f533-169">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>


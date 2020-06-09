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
ms.openlocfilehash: 576f54f2a7ecc2e1e99758719e80cc589c5bc791
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699472"
---
# <span data-ttu-id="fe12c-104">interfaz ICoreWebView2ExperimentalWindowFeatures</span><span class="sxs-lookup"><span data-stu-id="fe12c-104">interface ICoreWebView2ExperimentalWindowFeatures</span></span> 

> [!NOTE]
> <span data-ttu-id="fe12c-105">Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="fe12c-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

<span data-ttu-id="fe12c-106">Características de la ventana de una ventana emergente de vista previa.</span><span class="sxs-lookup"><span data-stu-id="fe12c-106">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="fe12c-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="fe12c-107">Summary</span></span>

 <span data-ttu-id="fe12c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="fe12c-108">Members</span></span>                        | <span data-ttu-id="fe12c-109">Descripciones</span><span class="sxs-lookup"><span data-stu-id="fe12c-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fe12c-110">get_Height</span><span class="sxs-lookup"><span data-stu-id="fe12c-110">get_Height</span></span>](#get_height) | <span data-ttu-id="fe12c-111">El alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fe12c-111">The height of the window.</span></span>
[<span data-ttu-id="fe12c-112">get_Left</span><span class="sxs-lookup"><span data-stu-id="fe12c-112">get_Left</span></span>](#get_left) | <span data-ttu-id="fe12c-113">La posición izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fe12c-113">The left position of the window.</span></span> <span data-ttu-id="fe12c-114">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="fe12c-114">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="fe12c-115">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="fe12c-115">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="fe12c-116">Si se muestra o no la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="fe12c-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="fe12c-117">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="fe12c-117">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="fe12c-118">Si se muestran o no las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="fe12c-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="fe12c-119">get_Status</span><span class="sxs-lookup"><span data-stu-id="fe12c-119">get_Status</span></span>](#get_status) | <span data-ttu-id="fe12c-120">Si desea o no agregar una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="fe12c-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="fe12c-121">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="fe12c-121">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="fe12c-122">Si desea que se muestre o no la barra de herramientas del explorador.</span><span class="sxs-lookup"><span data-stu-id="fe12c-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="fe12c-123">get_Top</span><span class="sxs-lookup"><span data-stu-id="fe12c-123">get_Top</span></span>](#get_top) | <span data-ttu-id="fe12c-124">La posición superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fe12c-124">The top position of the window.</span></span> <span data-ttu-id="fe12c-125">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="fe12c-125">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="fe12c-126">get_Width</span><span class="sxs-lookup"><span data-stu-id="fe12c-126">get_Width</span></span>](#get_width) | <span data-ttu-id="fe12c-127">Ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fe12c-127">The width of the window.</span></span>
[<span data-ttu-id="fe12c-128">HasPosition</span><span class="sxs-lookup"><span data-stu-id="fe12c-128">HasPosition</span></span>](#hasposition) | <span data-ttu-id="fe12c-129">Ha especificado valores de la izquierda y de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="fe12c-129">Has specified left and top values.</span></span>
[<span data-ttu-id="fe12c-130">HasSize</span><span class="sxs-lookup"><span data-stu-id="fe12c-130">HasSize</span></span>](#hassize) | <span data-ttu-id="fe12c-131">Ha especificado valores de alto y ancho.</span><span class="sxs-lookup"><span data-stu-id="fe12c-131">Has specified height and width values.</span></span>

<span data-ttu-id="fe12c-132">Estos campos coinciden con el ' windowFeatures ' pasado a Window. Open según lo especificado en[https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="fe12c-132">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="fe12c-133">Miembros</span><span class="sxs-lookup"><span data-stu-id="fe12c-133">Members</span></span>

#### <span data-ttu-id="fe12c-134">get_Height</span><span class="sxs-lookup"><span data-stu-id="fe12c-134">get_Height</span></span> 

<span data-ttu-id="fe12c-135">El alto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fe12c-135">The height of the window.</span></span>

> <span data-ttu-id="fe12c-136">[get_Height](#get_height)de HRESULT público (UINT32 \* height)</span><span class="sxs-lookup"><span data-stu-id="fe12c-136">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="fe12c-137">El valor mínimo es 100.</span><span class="sxs-lookup"><span data-stu-id="fe12c-137">Minimum value is 100.</span></span> <span data-ttu-id="fe12c-138">Dará un error si HasSize es falso.</span><span class="sxs-lookup"><span data-stu-id="fe12c-138">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="fe12c-139">get_Left</span><span class="sxs-lookup"><span data-stu-id="fe12c-139">get_Left</span></span> 

<span data-ttu-id="fe12c-140">La posición izquierda de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fe12c-140">The left position of the window.</span></span> <span data-ttu-id="fe12c-141">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="fe12c-141">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="fe12c-142">[get_Left](#get_left)de HRESULT público (UINT32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="fe12c-142">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="fe12c-143">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="fe12c-143">get_MenuBar</span></span> 

<span data-ttu-id="fe12c-144">Si se muestra o no la barra de menús.</span><span class="sxs-lookup"><span data-stu-id="fe12c-144">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="fe12c-145">[get_MenuBar](#get_menubar)de HRESULT público (bool \* MenuBar)</span><span class="sxs-lookup"><span data-stu-id="fe12c-145">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="fe12c-146">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="fe12c-146">get_ScrollBars</span></span> 

<span data-ttu-id="fe12c-147">Si se muestran o no las barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="fe12c-147">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="fe12c-148">[get_ScrollBars](#get_scrollbars)de HRESULT público (bool \* ScrollBars)</span><span class="sxs-lookup"><span data-stu-id="fe12c-148">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="fe12c-149">get_Status</span><span class="sxs-lookup"><span data-stu-id="fe12c-149">get_Status</span></span> 

<span data-ttu-id="fe12c-150">Si desea o no agregar una barra de estado.</span><span class="sxs-lookup"><span data-stu-id="fe12c-150">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="fe12c-151">[get_Status](#get_status)de HRESULT público (bool \* status)</span><span class="sxs-lookup"><span data-stu-id="fe12c-151">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="fe12c-152">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="fe12c-152">get_Toolbar</span></span> 

<span data-ttu-id="fe12c-153">Si desea que se muestre o no la barra de herramientas del explorador.</span><span class="sxs-lookup"><span data-stu-id="fe12c-153">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="fe12c-154">[get_Toolbar](#get_toolbar)de HRESULT público (una barra de herramientas de bool \*)</span><span class="sxs-lookup"><span data-stu-id="fe12c-154">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="fe12c-155">get_Top</span><span class="sxs-lookup"><span data-stu-id="fe12c-155">get_Top</span></span> 

<span data-ttu-id="fe12c-156">La posición superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fe12c-156">The top position of the window.</span></span> <span data-ttu-id="fe12c-157">Dará un error si HasPosition es falso.</span><span class="sxs-lookup"><span data-stu-id="fe12c-157">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="fe12c-158">[get_Top](#get_top)de HRESULT público (UINT32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="fe12c-158">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="fe12c-159">get_Width</span><span class="sxs-lookup"><span data-stu-id="fe12c-159">get_Width</span></span> 

<span data-ttu-id="fe12c-160">Ancho de la ventana.</span><span class="sxs-lookup"><span data-stu-id="fe12c-160">The width of the window.</span></span>

> <span data-ttu-id="fe12c-161">[get_Width](#get_width)de HRESULT público (UINT32 \* width)</span><span class="sxs-lookup"><span data-stu-id="fe12c-161">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="fe12c-162">El valor mínimo es 100.</span><span class="sxs-lookup"><span data-stu-id="fe12c-162">Minimum value is 100.</span></span> <span data-ttu-id="fe12c-163">Dará un error si HasSize es falso.</span><span class="sxs-lookup"><span data-stu-id="fe12c-163">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="fe12c-164">HasPosition</span><span class="sxs-lookup"><span data-stu-id="fe12c-164">HasPosition</span></span> 

<span data-ttu-id="fe12c-165">Ha especificado valores de la izquierda y de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="fe12c-165">Has specified left and top values.</span></span>

> <span data-ttu-id="fe12c-166">[HASPOSITION](#hasposition)HRESULT público (bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="fe12c-166">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="fe12c-167">HasSize</span><span class="sxs-lookup"><span data-stu-id="fe12c-167">HasSize</span></span> 

<span data-ttu-id="fe12c-168">Ha especificado valores de alto y ancho.</span><span class="sxs-lookup"><span data-stu-id="fe12c-168">Has specified height and width values.</span></span>

> <span data-ttu-id="fe12c-169">[HASSIZE](#hassize)HRESULT público (bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="fe12c-169">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>


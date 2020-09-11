---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
ms.openlocfilehash: 34ffa5fe0eabfe8e822db2792d2b25ab5106442a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012639"
---
# <span data-ttu-id="e3795-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="e3795-104">Microsoft.Web.WebView2.Core.CoreWebView2PointerInfo class</span></span> 

<span data-ttu-id="e3795-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="e3795-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="e3795-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="e3795-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="e3795-107">Esto representa principalmente un objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="e3795-107">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="e3795-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="e3795-108">Summary</span></span>

 <span data-ttu-id="e3795-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="e3795-109">Members</span></span>                        | <span data-ttu-id="e3795-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e3795-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e3795-111">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="e3795-111">ButtonChangeKind</span></span>](#buttonchangekind) | <span data-ttu-id="e3795-112">El ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-112">The ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="e3795-113">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="e3795-113">DisplayRect</span></span>](#displayrect) | <span data-ttu-id="e3795-114">El DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-114">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="e3795-115">FrameId</span><span class="sxs-lookup"><span data-stu-id="e3795-115">FrameId</span></span>](#frameid) | <span data-ttu-id="e3795-116">El FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-116">The FrameID of the pointer event.</span></span>
[<span data-ttu-id="e3795-117">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="e3795-117">HimetricLocation</span></span>](#himetriclocation) | <span data-ttu-id="e3795-118">El HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-118">The HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="e3795-119">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="e3795-119">HimetricLocationRaw</span></span>](#himetriclocationraw) | <span data-ttu-id="e3795-120">El HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-120">The HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="e3795-121">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="e3795-121">HistoryCount</span></span>](#historycount) | <span data-ttu-id="e3795-122">El HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-122">The HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="e3795-123">InputData</span><span class="sxs-lookup"><span data-stu-id="e3795-123">InputData</span></span>](#inputdata) | <span data-ttu-id="e3795-124">El InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-124">The InputData of the pointer event.</span></span>
[<span data-ttu-id="e3795-125">KeyStates</span><span class="sxs-lookup"><span data-stu-id="e3795-125">KeyStates</span></span>](#keystates) | <span data-ttu-id="e3795-126">El KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-126">The KeyStates of the pointer event.</span></span>
[<span data-ttu-id="e3795-127">PenFlags</span><span class="sxs-lookup"><span data-stu-id="e3795-127">PenFlags</span></span>](#penflags) | <span data-ttu-id="e3795-128">El PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-128">The PenFlags of the pointer event.</span></span>
[<span data-ttu-id="e3795-129">PenMask</span><span class="sxs-lookup"><span data-stu-id="e3795-129">PenMask</span></span>](#penmask) | <span data-ttu-id="e3795-130">El PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-130">The PenMask of the pointer event.</span></span>
[<span data-ttu-id="e3795-131">PenPressure</span><span class="sxs-lookup"><span data-stu-id="e3795-131">PenPressure</span></span>](#penpressure) | <span data-ttu-id="e3795-132">El PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-132">The PenPressure of the pointer event.</span></span>
[<span data-ttu-id="e3795-133">PenRotation</span><span class="sxs-lookup"><span data-stu-id="e3795-133">PenRotation</span></span>](#penrotation) | <span data-ttu-id="e3795-134">El PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-134">The PenRotation of the pointer event.</span></span>
[<span data-ttu-id="e3795-135">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="e3795-135">PenTiltX</span></span>](#pentiltx) | <span data-ttu-id="e3795-136">El PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-136">The PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="e3795-137">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="e3795-137">PenTiltY</span></span>](#pentilty) | <span data-ttu-id="e3795-138">El PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-138">The PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="e3795-139">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="e3795-139">PerformanceCount</span></span>](#performancecount) | <span data-ttu-id="e3795-140">El PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-140">The PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="e3795-141">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="e3795-141">PixelLocation</span></span>](#pixellocation) | <span data-ttu-id="e3795-142">El PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-142">The PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="e3795-143">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="e3795-143">PixelLocationRaw</span></span>](#pixellocationraw) | <span data-ttu-id="e3795-144">El PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-144">The PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="e3795-145">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="e3795-145">PointerDeviceRect</span></span>](#pointerdevicerect) | <span data-ttu-id="e3795-146">El PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-146">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="e3795-147">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="e3795-147">PointerFlags</span></span>](#pointerflags) | <span data-ttu-id="e3795-148">El PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-148">The PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="e3795-149">PointerId</span><span class="sxs-lookup"><span data-stu-id="e3795-149">PointerId</span></span>](#pointerid) | <span data-ttu-id="e3795-150">El PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-150">The PointerId of the pointer event.</span></span>
[<span data-ttu-id="e3795-151">PointerKind</span><span class="sxs-lookup"><span data-stu-id="e3795-151">PointerKind</span></span>](#pointerkind) | <span data-ttu-id="e3795-152">El PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-152">The PointerKind of the pointer event.</span></span>
[<span data-ttu-id="e3795-153">Tiempo</span><span class="sxs-lookup"><span data-stu-id="e3795-153">Time</span></span>](#time) | <span data-ttu-id="e3795-154">Hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-154">The Time of the pointer event.</span></span>
[<span data-ttu-id="e3795-155">TouchContact</span><span class="sxs-lookup"><span data-stu-id="e3795-155">TouchContact</span></span>](#touchcontact) | <span data-ttu-id="e3795-156">El TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-156">The TouchContact of the pointer event.</span></span>
[<span data-ttu-id="e3795-157">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="e3795-157">TouchContactRaw</span></span>](#touchcontactraw) | <span data-ttu-id="e3795-158">El TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-158">The TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="e3795-159">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="e3795-159">TouchFlags</span></span>](#touchflags) | <span data-ttu-id="e3795-160">El TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-160">The TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="e3795-161">TouchMask</span><span class="sxs-lookup"><span data-stu-id="e3795-161">TouchMask</span></span>](#touchmask) | <span data-ttu-id="e3795-162">El TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-162">The TouchMask of the pointer event.</span></span>
[<span data-ttu-id="e3795-163">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="e3795-163">TouchOrientation</span></span>](#touchorientation) | <span data-ttu-id="e3795-164">El TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-164">The TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="e3795-165">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="e3795-165">TouchPressure</span></span>](#touchpressure) | <span data-ttu-id="e3795-166">El TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-166">The TouchPressure of the pointer event.</span></span>

## <span data-ttu-id="e3795-167">Miembros</span><span class="sxs-lookup"><span data-stu-id="e3795-167">Members</span></span>

#### <span data-ttu-id="e3795-168">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="e3795-168">ButtonChangeKind</span></span> 

<span data-ttu-id="e3795-169">El ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-169">The ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="e3795-170">public int [ButtonChangeKind](#buttonchangekind)</span><span class="sxs-lookup"><span data-stu-id="e3795-170">public int [ButtonChangeKind](#buttonchangekind)</span></span>

<span data-ttu-id="e3795-171">Esto corresponde a la propiedad ButtonChangeKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="e3795-171">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="e3795-172">Los valores están definidos por la enumeración POINTER_BUTTON_CHANGE_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-172">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-173">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="e3795-173">DisplayRect</span></span> 

<span data-ttu-id="e3795-174">El DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-174">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="e3795-175">[DisplayRect](#displayrect) de rectángulo público</span><span class="sxs-lookup"><span data-stu-id="e3795-175">public Rectangle [DisplayRect](#displayrect)</span></span>

#### <span data-ttu-id="e3795-176">FrameId</span><span class="sxs-lookup"><span data-stu-id="e3795-176">FrameId</span></span> 

<span data-ttu-id="e3795-177">El FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-177">The FrameID of the pointer event.</span></span>

> <span data-ttu-id="e3795-178">uint pública [FrameId](#frameid)</span><span class="sxs-lookup"><span data-stu-id="e3795-178">public uint [FrameId](#frameid)</span></span>

<span data-ttu-id="e3795-179">Esto corresponde a la propiedad frameId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-179">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-180">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="e3795-180">HimetricLocation</span></span> 

<span data-ttu-id="e3795-181">El HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-181">The HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="e3795-182">Punto público [HimetricLocation](#himetriclocation)</span><span class="sxs-lookup"><span data-stu-id="e3795-182">public Point [HimetricLocation](#himetriclocation)</span></span>

<span data-ttu-id="e3795-183">Esto corresponde a la propiedad ptHimetricLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-183">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-184">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="e3795-184">HimetricLocationRaw</span></span> 

<span data-ttu-id="e3795-185">El HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-185">The HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="e3795-186">Punto público [HimetricLocationRaw](#himetriclocationraw)</span><span class="sxs-lookup"><span data-stu-id="e3795-186">public Point [HimetricLocationRaw](#himetriclocationraw)</span></span>

<span data-ttu-id="e3795-187">Esto corresponde a la propiedad ptHimetricLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-187">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-188">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="e3795-188">HistoryCount</span></span> 

<span data-ttu-id="e3795-189">El HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-189">The HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="e3795-190">uint pública [HistoryCount](#historycount)</span><span class="sxs-lookup"><span data-stu-id="e3795-190">public uint [HistoryCount](#historycount)</span></span>

<span data-ttu-id="e3795-191">Esto corresponde a la propiedad historyCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-191">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-192">InputData</span><span class="sxs-lookup"><span data-stu-id="e3795-192">InputData</span></span> 

<span data-ttu-id="e3795-193">El InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-193">The InputData of the pointer event.</span></span>

> <span data-ttu-id="e3795-194">public int [InputData](#inputdata)</span><span class="sxs-lookup"><span data-stu-id="e3795-194">public int [InputData](#inputdata)</span></span>

<span data-ttu-id="e3795-195">Esto corresponde a la propiedad InputData de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-195">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-196">KeyStates</span><span class="sxs-lookup"><span data-stu-id="e3795-196">KeyStates</span></span> 

<span data-ttu-id="e3795-197">El KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-197">The KeyStates of the pointer event.</span></span>

> <span data-ttu-id="e3795-198">uint pública [KeyStates](#keystates)</span><span class="sxs-lookup"><span data-stu-id="e3795-198">public uint [KeyStates](#keystates)</span></span>

<span data-ttu-id="e3795-199">Esto corresponde a la propiedad dwKeyStates de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-199">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-200">PenFlags</span><span class="sxs-lookup"><span data-stu-id="e3795-200">PenFlags</span></span> 

<span data-ttu-id="e3795-201">El PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-201">The PenFlags of the pointer event.</span></span>

> <span data-ttu-id="e3795-202">uint pública [PenFlags](#penflags)</span><span class="sxs-lookup"><span data-stu-id="e3795-202">public uint [PenFlags](#penflags)</span></span>

<span data-ttu-id="e3795-203">Esto corresponde a la propiedad penFlags de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="e3795-203">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="e3795-204">Los valores están definidos por las constantes de PEN_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-204">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-205">PenMask</span><span class="sxs-lookup"><span data-stu-id="e3795-205">PenMask</span></span> 

<span data-ttu-id="e3795-206">El PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-206">The PenMask of the pointer event.</span></span>

> <span data-ttu-id="e3795-207">uint pública [PenMask](#penmask)</span><span class="sxs-lookup"><span data-stu-id="e3795-207">public uint [PenMask](#penmask)</span></span>

<span data-ttu-id="e3795-208">Esto corresponde a la propiedad penMask de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="e3795-208">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="e3795-209">Los valores están definidos por las constantes de PEN_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-209">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-210">PenPressure</span><span class="sxs-lookup"><span data-stu-id="e3795-210">PenPressure</span></span> 

<span data-ttu-id="e3795-211">El PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-211">The PenPressure of the pointer event.</span></span>

> <span data-ttu-id="e3795-212">uint pública [PenPressure](#penpressure)</span><span class="sxs-lookup"><span data-stu-id="e3795-212">public uint [PenPressure](#penpressure)</span></span>

<span data-ttu-id="e3795-213">Esto corresponde a la propiedad de presión de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-213">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-214">PenRotation</span><span class="sxs-lookup"><span data-stu-id="e3795-214">PenRotation</span></span> 

<span data-ttu-id="e3795-215">El PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-215">The PenRotation of the pointer event.</span></span>

> <span data-ttu-id="e3795-216">uint pública [PenRotation](#penrotation)</span><span class="sxs-lookup"><span data-stu-id="e3795-216">public uint [PenRotation](#penrotation)</span></span>

<span data-ttu-id="e3795-217">Esto corresponde a la propiedad Rotation de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-217">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-218">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="e3795-218">PenTiltX</span></span> 

<span data-ttu-id="e3795-219">El PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-219">The PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="e3795-220">public int [PenTiltX](#pentiltx)</span><span class="sxs-lookup"><span data-stu-id="e3795-220">public int [PenTiltX](#pentiltx)</span></span>

<span data-ttu-id="e3795-221">Esto corresponde a la propiedad tiltX de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-221">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-222">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="e3795-222">PenTiltY</span></span> 

<span data-ttu-id="e3795-223">El PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-223">The PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="e3795-224">public int [PenTiltY](#pentilty)</span><span class="sxs-lookup"><span data-stu-id="e3795-224">public int [PenTiltY](#pentilty)</span></span>

<span data-ttu-id="e3795-225">Esto corresponde a la propiedad Tilt de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-225">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-226">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="e3795-226">PerformanceCount</span></span> 

<span data-ttu-id="e3795-227">El PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-227">The PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="e3795-228">ulong [PerformanceCount](#performancecount)</span><span class="sxs-lookup"><span data-stu-id="e3795-228">public ulong [PerformanceCount](#performancecount)</span></span>

<span data-ttu-id="e3795-229">Esto corresponde a la propiedad PerformanceCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-229">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-230">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="e3795-230">PixelLocation</span></span> 

<span data-ttu-id="e3795-231">El PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-231">The PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="e3795-232">Punto público [PixelLocation](#pixellocation)</span><span class="sxs-lookup"><span data-stu-id="e3795-232">public Point [PixelLocation](#pixellocation)</span></span>

<span data-ttu-id="e3795-233">Esto corresponde a la propiedad ptPixelLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-233">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-234">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="e3795-234">PixelLocationRaw</span></span> 

<span data-ttu-id="e3795-235">El PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-235">The PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="e3795-236">Punto público [PixelLocationRaw](#pixellocationraw)</span><span class="sxs-lookup"><span data-stu-id="e3795-236">public Point [PixelLocationRaw](#pixellocationraw)</span></span>

<span data-ttu-id="e3795-237">Esto corresponde a la propiedad ptPixelLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-237">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-238">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="e3795-238">PointerDeviceRect</span></span> 

<span data-ttu-id="e3795-239">El PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-239">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="e3795-240">[PointerDeviceRect](#pointerdevicerect) de rectángulo público</span><span class="sxs-lookup"><span data-stu-id="e3795-240">public Rectangle [PointerDeviceRect](#pointerdevicerect)</span></span>

#### <span data-ttu-id="e3795-241">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="e3795-241">PointerFlags</span></span> 

<span data-ttu-id="e3795-242">El PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-242">The PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="e3795-243">uint pública [PointerFlags](#pointerflags)</span><span class="sxs-lookup"><span data-stu-id="e3795-243">public uint [PointerFlags](#pointerflags)</span></span>

<span data-ttu-id="e3795-244">Esto corresponde a la propiedad pointerFlags de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="e3795-244">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="e3795-245">Los valores están definidos por las constantes de POINTER_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-245">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-246">PointerId</span><span class="sxs-lookup"><span data-stu-id="e3795-246">PointerId</span></span> 

<span data-ttu-id="e3795-247">El PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-247">The PointerId of the pointer event.</span></span>

> <span data-ttu-id="e3795-248">uint pública [PointerId](#pointerid)</span><span class="sxs-lookup"><span data-stu-id="e3795-248">public uint [PointerId](#pointerid)</span></span>

<span data-ttu-id="e3795-249">Esto corresponde a la propiedad pointerId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-249">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-250">PointerKind</span><span class="sxs-lookup"><span data-stu-id="e3795-250">PointerKind</span></span> 

<span data-ttu-id="e3795-251">El PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-251">The PointerKind of the pointer event.</span></span>

> <span data-ttu-id="e3795-252">uint pública [PointerKind](#pointerkind)</span><span class="sxs-lookup"><span data-stu-id="e3795-252">public uint [PointerKind](#pointerkind)</span></span>

<span data-ttu-id="e3795-253">Esto corresponde a la propiedad pointerKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="e3795-253">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="e3795-254">Los valores están definidos por la enumeración POINTER_INPUT_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-254">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="e3795-255">Es compatible con PT_PEN y PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="e3795-255">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="e3795-256">Tiempo</span><span class="sxs-lookup"><span data-stu-id="e3795-256">Time</span></span> 

<span data-ttu-id="e3795-257">Hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-257">The Time of the pointer event.</span></span>

> <span data-ttu-id="e3795-258">[hora](#time) uint pública</span><span class="sxs-lookup"><span data-stu-id="e3795-258">public uint [Time](#time)</span></span>

<span data-ttu-id="e3795-259">Esto corresponde a la propiedad dwTime de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-259">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-260">TouchContact</span><span class="sxs-lookup"><span data-stu-id="e3795-260">TouchContact</span></span> 

<span data-ttu-id="e3795-261">El TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-261">The TouchContact of the pointer event.</span></span>

> <span data-ttu-id="e3795-262">[TouchContact](#touchcontact) de rectángulo público</span><span class="sxs-lookup"><span data-stu-id="e3795-262">public Rectangle [TouchContact](#touchcontact)</span></span>

<span data-ttu-id="e3795-263">Esto corresponde a la propiedad rcContact de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-263">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-264">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="e3795-264">TouchContactRaw</span></span> 

<span data-ttu-id="e3795-265">El TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-265">The TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="e3795-266">[TouchContactRaw](#touchcontactraw) de rectángulo público</span><span class="sxs-lookup"><span data-stu-id="e3795-266">public Rectangle [TouchContactRaw](#touchcontactraw)</span></span>

<span data-ttu-id="e3795-267">Esto corresponde a la propiedad rcContactRaw de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-267">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-268">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="e3795-268">TouchFlags</span></span> 

<span data-ttu-id="e3795-269">El TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-269">The TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="e3795-270">uint pública [TouchFlags](#touchflags)</span><span class="sxs-lookup"><span data-stu-id="e3795-270">public uint [TouchFlags](#touchflags)</span></span>

<span data-ttu-id="e3795-271">Esto corresponde a la propiedad touchFlags de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="e3795-271">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="e3795-272">Los valores están definidos por las constantes de TOUCH_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-272">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-273">TouchMask</span><span class="sxs-lookup"><span data-stu-id="e3795-273">TouchMask</span></span> 

<span data-ttu-id="e3795-274">El TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-274">The TouchMask of the pointer event.</span></span>

> <span data-ttu-id="e3795-275">uint pública [TouchMask](#touchmask)</span><span class="sxs-lookup"><span data-stu-id="e3795-275">public uint [TouchMask](#touchmask)</span></span>

<span data-ttu-id="e3795-276">Esto corresponde a la propiedad touchMask de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="e3795-276">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="e3795-277">Los valores están definidos por las constantes de TOUCH_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-277">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-278">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="e3795-278">TouchOrientation</span></span> 

<span data-ttu-id="e3795-279">El TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-279">The TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="e3795-280">uint pública [TouchOrientation](#touchorientation)</span><span class="sxs-lookup"><span data-stu-id="e3795-280">public uint [TouchOrientation](#touchorientation)</span></span>

<span data-ttu-id="e3795-281">Esto corresponde a la propiedad Orientation de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-281">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="e3795-282">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="e3795-282">TouchPressure</span></span> 

<span data-ttu-id="e3795-283">El TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="e3795-283">The TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="e3795-284">uint pública [TouchPressure](#touchpressure)</span><span class="sxs-lookup"><span data-stu-id="e3795-284">public uint [TouchPressure](#touchpressure)</span></span>

<span data-ttu-id="e3795-285">Esto corresponde a la propiedad de presión de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="e3795-285">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>


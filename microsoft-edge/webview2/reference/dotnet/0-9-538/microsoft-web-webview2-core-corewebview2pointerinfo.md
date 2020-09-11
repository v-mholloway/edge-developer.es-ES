---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
ms.openlocfilehash: 9ce4c9c3f076d54f03295ffda84c5fb0f03b4166
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010905"
---
# <span data-ttu-id="c1992-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo (clase)</span><span class="sxs-lookup"><span data-stu-id="c1992-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2PointerInfo class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="c1992-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="c1992-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="c1992-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="c1992-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="c1992-107">Esto representa principalmente un objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="c1992-107">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="c1992-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="c1992-108">Summary</span></span>

 <span data-ttu-id="c1992-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c1992-109">Members</span></span>                        | <span data-ttu-id="c1992-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="c1992-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c1992-111">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="c1992-111">ButtonChangeKind</span></span>](#buttonchangekind) | <span data-ttu-id="c1992-112">El ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-112">The ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="c1992-113">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="c1992-113">DisplayRect</span></span>](#displayrect) | <span data-ttu-id="c1992-114">El DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-114">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="c1992-115">FrameId</span><span class="sxs-lookup"><span data-stu-id="c1992-115">FrameId</span></span>](#frameid) | <span data-ttu-id="c1992-116">El FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-116">The FrameID of the pointer event.</span></span>
[<span data-ttu-id="c1992-117">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="c1992-117">HimetricLocation</span></span>](#himetriclocation) | <span data-ttu-id="c1992-118">El HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-118">The HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="c1992-119">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="c1992-119">HimetricLocationRaw</span></span>](#himetriclocationraw) | <span data-ttu-id="c1992-120">El HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-120">The HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="c1992-121">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="c1992-121">HistoryCount</span></span>](#historycount) | <span data-ttu-id="c1992-122">El HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-122">The HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="c1992-123">InputData</span><span class="sxs-lookup"><span data-stu-id="c1992-123">InputData</span></span>](#inputdata) | <span data-ttu-id="c1992-124">El InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-124">The InputData of the pointer event.</span></span>
[<span data-ttu-id="c1992-125">KeyStates</span><span class="sxs-lookup"><span data-stu-id="c1992-125">KeyStates</span></span>](#keystates) | <span data-ttu-id="c1992-126">El KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-126">The KeyStates of the pointer event.</span></span>
[<span data-ttu-id="c1992-127">PenFlags</span><span class="sxs-lookup"><span data-stu-id="c1992-127">PenFlags</span></span>](#penflags) | <span data-ttu-id="c1992-128">El PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-128">The PenFlags of the pointer event.</span></span>
[<span data-ttu-id="c1992-129">PenMask</span><span class="sxs-lookup"><span data-stu-id="c1992-129">PenMask</span></span>](#penmask) | <span data-ttu-id="c1992-130">El PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-130">The PenMask of the pointer event.</span></span>
[<span data-ttu-id="c1992-131">PenPressure</span><span class="sxs-lookup"><span data-stu-id="c1992-131">PenPressure</span></span>](#penpressure) | <span data-ttu-id="c1992-132">El PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-132">The PenPressure of the pointer event.</span></span>
[<span data-ttu-id="c1992-133">PenRotation</span><span class="sxs-lookup"><span data-stu-id="c1992-133">PenRotation</span></span>](#penrotation) | <span data-ttu-id="c1992-134">El PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-134">The PenRotation of the pointer event.</span></span>
[<span data-ttu-id="c1992-135">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="c1992-135">PenTiltX</span></span>](#pentiltx) | <span data-ttu-id="c1992-136">El PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-136">The PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="c1992-137">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="c1992-137">PenTiltY</span></span>](#pentilty) | <span data-ttu-id="c1992-138">El PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-138">The PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="c1992-139">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="c1992-139">PerformanceCount</span></span>](#performancecount) | <span data-ttu-id="c1992-140">El PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-140">The PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="c1992-141">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="c1992-141">PixelLocation</span></span>](#pixellocation) | <span data-ttu-id="c1992-142">El PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-142">The PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="c1992-143">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="c1992-143">PixelLocationRaw</span></span>](#pixellocationraw) | <span data-ttu-id="c1992-144">El PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-144">The PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="c1992-145">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="c1992-145">PointerDeviceRect</span></span>](#pointerdevicerect) | <span data-ttu-id="c1992-146">El PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-146">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="c1992-147">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="c1992-147">PointerFlags</span></span>](#pointerflags) | <span data-ttu-id="c1992-148">El PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-148">The PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="c1992-149">PointerId</span><span class="sxs-lookup"><span data-stu-id="c1992-149">PointerId</span></span>](#pointerid) | <span data-ttu-id="c1992-150">El PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-150">The PointerId of the pointer event.</span></span>
[<span data-ttu-id="c1992-151">PointerKind</span><span class="sxs-lookup"><span data-stu-id="c1992-151">PointerKind</span></span>](#pointerkind) | <span data-ttu-id="c1992-152">El PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-152">The PointerKind of the pointer event.</span></span>
[<span data-ttu-id="c1992-153">Tiempo</span><span class="sxs-lookup"><span data-stu-id="c1992-153">Time</span></span>](#time) | <span data-ttu-id="c1992-154">Hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-154">The Time of the pointer event.</span></span>
[<span data-ttu-id="c1992-155">TouchContact</span><span class="sxs-lookup"><span data-stu-id="c1992-155">TouchContact</span></span>](#touchcontact) | <span data-ttu-id="c1992-156">El TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-156">The TouchContact of the pointer event.</span></span>
[<span data-ttu-id="c1992-157">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="c1992-157">TouchContactRaw</span></span>](#touchcontactraw) | <span data-ttu-id="c1992-158">El TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-158">The TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="c1992-159">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="c1992-159">TouchFlags</span></span>](#touchflags) | <span data-ttu-id="c1992-160">El TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-160">The TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="c1992-161">TouchMask</span><span class="sxs-lookup"><span data-stu-id="c1992-161">TouchMask</span></span>](#touchmask) | <span data-ttu-id="c1992-162">El TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-162">The TouchMask of the pointer event.</span></span>
[<span data-ttu-id="c1992-163">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="c1992-163">TouchOrientation</span></span>](#touchorientation) | <span data-ttu-id="c1992-164">El TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-164">The TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="c1992-165">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="c1992-165">TouchPressure</span></span>](#touchpressure) | <span data-ttu-id="c1992-166">El TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-166">The TouchPressure of the pointer event.</span></span>

## <span data-ttu-id="c1992-167">Miembros</span><span class="sxs-lookup"><span data-stu-id="c1992-167">Members</span></span>

#### <span data-ttu-id="c1992-168">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="c1992-168">ButtonChangeKind</span></span> 

<span data-ttu-id="c1992-169">El ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-169">The ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="c1992-170">public int [ButtonChangeKind](#buttonchangekind)</span><span class="sxs-lookup"><span data-stu-id="c1992-170">public int [ButtonChangeKind](#buttonchangekind)</span></span>

<span data-ttu-id="c1992-171">Esto corresponde a la propiedad ButtonChangeKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="c1992-171">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="c1992-172">Los valores están definidos por la enumeración POINTER_BUTTON_CHANGE_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-172">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-173">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="c1992-173">DisplayRect</span></span> 

<span data-ttu-id="c1992-174">El DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-174">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="c1992-175">Public Rect [DisplayRect](#displayrect)</span><span class="sxs-lookup"><span data-stu-id="c1992-175">public Rect [DisplayRect](#displayrect)</span></span>

#### <span data-ttu-id="c1992-176">FrameId</span><span class="sxs-lookup"><span data-stu-id="c1992-176">FrameId</span></span> 

<span data-ttu-id="c1992-177">El FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-177">The FrameID of the pointer event.</span></span>

> <span data-ttu-id="c1992-178">uint pública [FrameId](#frameid)</span><span class="sxs-lookup"><span data-stu-id="c1992-178">public uint [FrameId](#frameid)</span></span>

<span data-ttu-id="c1992-179">Esto corresponde a la propiedad frameId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-179">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-180">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="c1992-180">HimetricLocation</span></span> 

<span data-ttu-id="c1992-181">El HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-181">The HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="c1992-182">Punto público [HimetricLocation](#himetriclocation)</span><span class="sxs-lookup"><span data-stu-id="c1992-182">public Point [HimetricLocation](#himetriclocation)</span></span>

<span data-ttu-id="c1992-183">Esto corresponde a la propiedad ptHimetricLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-183">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-184">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="c1992-184">HimetricLocationRaw</span></span> 

<span data-ttu-id="c1992-185">El HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-185">The HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="c1992-186">Punto público [HimetricLocationRaw](#himetriclocationraw)</span><span class="sxs-lookup"><span data-stu-id="c1992-186">public Point [HimetricLocationRaw](#himetriclocationraw)</span></span>

<span data-ttu-id="c1992-187">Esto corresponde a la propiedad ptHimetricLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-187">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-188">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="c1992-188">HistoryCount</span></span> 

<span data-ttu-id="c1992-189">El HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-189">The HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="c1992-190">uint pública [HistoryCount](#historycount)</span><span class="sxs-lookup"><span data-stu-id="c1992-190">public uint [HistoryCount](#historycount)</span></span>

<span data-ttu-id="c1992-191">Esto corresponde a la propiedad historyCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-191">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-192">InputData</span><span class="sxs-lookup"><span data-stu-id="c1992-192">InputData</span></span> 

<span data-ttu-id="c1992-193">El InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-193">The InputData of the pointer event.</span></span>

> <span data-ttu-id="c1992-194">public int [InputData](#inputdata)</span><span class="sxs-lookup"><span data-stu-id="c1992-194">public int [InputData](#inputdata)</span></span>

<span data-ttu-id="c1992-195">Esto corresponde a la propiedad InputData de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-195">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-196">KeyStates</span><span class="sxs-lookup"><span data-stu-id="c1992-196">KeyStates</span></span> 

<span data-ttu-id="c1992-197">El KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-197">The KeyStates of the pointer event.</span></span>

> <span data-ttu-id="c1992-198">uint pública [KeyStates](#keystates)</span><span class="sxs-lookup"><span data-stu-id="c1992-198">public uint [KeyStates](#keystates)</span></span>

<span data-ttu-id="c1992-199">Esto corresponde a la propiedad dwKeyStates de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-199">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-200">PenFlags</span><span class="sxs-lookup"><span data-stu-id="c1992-200">PenFlags</span></span> 

<span data-ttu-id="c1992-201">El PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-201">The PenFlags of the pointer event.</span></span>

> <span data-ttu-id="c1992-202">uint pública [PenFlags](#penflags)</span><span class="sxs-lookup"><span data-stu-id="c1992-202">public uint [PenFlags](#penflags)</span></span>

<span data-ttu-id="c1992-203">Esto corresponde a la propiedad penFlags de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="c1992-203">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="c1992-204">Los valores están definidos por las constantes de PEN_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-204">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-205">PenMask</span><span class="sxs-lookup"><span data-stu-id="c1992-205">PenMask</span></span> 

<span data-ttu-id="c1992-206">El PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-206">The PenMask of the pointer event.</span></span>

> <span data-ttu-id="c1992-207">uint pública [PenMask](#penmask)</span><span class="sxs-lookup"><span data-stu-id="c1992-207">public uint [PenMask](#penmask)</span></span>

<span data-ttu-id="c1992-208">Esto corresponde a la propiedad penMask de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="c1992-208">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="c1992-209">Los valores están definidos por las constantes de PEN_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-209">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-210">PenPressure</span><span class="sxs-lookup"><span data-stu-id="c1992-210">PenPressure</span></span> 

<span data-ttu-id="c1992-211">El PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-211">The PenPressure of the pointer event.</span></span>

> <span data-ttu-id="c1992-212">uint pública [PenPressure](#penpressure)</span><span class="sxs-lookup"><span data-stu-id="c1992-212">public uint [PenPressure](#penpressure)</span></span>

<span data-ttu-id="c1992-213">Esto corresponde a la propiedad de presión de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-213">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-214">PenRotation</span><span class="sxs-lookup"><span data-stu-id="c1992-214">PenRotation</span></span> 

<span data-ttu-id="c1992-215">El PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-215">The PenRotation of the pointer event.</span></span>

> <span data-ttu-id="c1992-216">uint pública [PenRotation](#penrotation)</span><span class="sxs-lookup"><span data-stu-id="c1992-216">public uint [PenRotation](#penrotation)</span></span>

<span data-ttu-id="c1992-217">Esto corresponde a la propiedad Rotation de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-217">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-218">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="c1992-218">PenTiltX</span></span> 

<span data-ttu-id="c1992-219">El PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-219">The PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="c1992-220">public int [PenTiltX](#pentiltx)</span><span class="sxs-lookup"><span data-stu-id="c1992-220">public int [PenTiltX](#pentiltx)</span></span>

<span data-ttu-id="c1992-221">Esto corresponde a la propiedad tiltX de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-221">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-222">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="c1992-222">PenTiltY</span></span> 

<span data-ttu-id="c1992-223">El PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-223">The PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="c1992-224">public int [PenTiltY](#pentilty)</span><span class="sxs-lookup"><span data-stu-id="c1992-224">public int [PenTiltY](#pentilty)</span></span>

<span data-ttu-id="c1992-225">Esto corresponde a la propiedad Tilt de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-225">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-226">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="c1992-226">PerformanceCount</span></span> 

<span data-ttu-id="c1992-227">El PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-227">The PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="c1992-228">ulong [PerformanceCount](#performancecount)</span><span class="sxs-lookup"><span data-stu-id="c1992-228">public ulong [PerformanceCount](#performancecount)</span></span>

<span data-ttu-id="c1992-229">Esto corresponde a la propiedad PerformanceCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-229">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-230">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="c1992-230">PixelLocation</span></span> 

<span data-ttu-id="c1992-231">El PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-231">The PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="c1992-232">Punto público [PixelLocation](#pixellocation)</span><span class="sxs-lookup"><span data-stu-id="c1992-232">public Point [PixelLocation](#pixellocation)</span></span>

<span data-ttu-id="c1992-233">Esto corresponde a la propiedad ptPixelLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-233">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-234">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="c1992-234">PixelLocationRaw</span></span> 

<span data-ttu-id="c1992-235">El PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-235">The PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="c1992-236">Punto público [PixelLocationRaw](#pixellocationraw)</span><span class="sxs-lookup"><span data-stu-id="c1992-236">public Point [PixelLocationRaw](#pixellocationraw)</span></span>

<span data-ttu-id="c1992-237">Esto corresponde a la propiedad ptPixelLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-237">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-238">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="c1992-238">PointerDeviceRect</span></span> 

<span data-ttu-id="c1992-239">El PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-239">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="c1992-240">Public Rect [PointerDeviceRect](#pointerdevicerect)</span><span class="sxs-lookup"><span data-stu-id="c1992-240">public Rect [PointerDeviceRect](#pointerdevicerect)</span></span>

#### <span data-ttu-id="c1992-241">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="c1992-241">PointerFlags</span></span> 

<span data-ttu-id="c1992-242">El PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-242">The PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="c1992-243">uint pública [PointerFlags](#pointerflags)</span><span class="sxs-lookup"><span data-stu-id="c1992-243">public uint [PointerFlags](#pointerflags)</span></span>

<span data-ttu-id="c1992-244">Esto corresponde a la propiedad pointerFlags de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="c1992-244">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="c1992-245">Los valores están definidos por las constantes de POINTER_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-245">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-246">PointerId</span><span class="sxs-lookup"><span data-stu-id="c1992-246">PointerId</span></span> 

<span data-ttu-id="c1992-247">El PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-247">The PointerId of the pointer event.</span></span>

> <span data-ttu-id="c1992-248">uint pública [PointerId](#pointerid)</span><span class="sxs-lookup"><span data-stu-id="c1992-248">public uint [PointerId](#pointerid)</span></span>

<span data-ttu-id="c1992-249">Esto corresponde a la propiedad pointerId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-249">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-250">PointerKind</span><span class="sxs-lookup"><span data-stu-id="c1992-250">PointerKind</span></span> 

<span data-ttu-id="c1992-251">El PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-251">The PointerKind of the pointer event.</span></span>

> <span data-ttu-id="c1992-252">uint pública [PointerKind](#pointerkind)</span><span class="sxs-lookup"><span data-stu-id="c1992-252">public uint [PointerKind](#pointerkind)</span></span>

<span data-ttu-id="c1992-253">Esto corresponde a la propiedad pointerKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="c1992-253">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="c1992-254">Los valores están definidos por la enumeración POINTER_INPUT_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-254">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="c1992-255">Es compatible con PT_PEN y PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="c1992-255">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="c1992-256">Tiempo</span><span class="sxs-lookup"><span data-stu-id="c1992-256">Time</span></span> 

<span data-ttu-id="c1992-257">Hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-257">The Time of the pointer event.</span></span>

> <span data-ttu-id="c1992-258">[hora](#time) uint pública</span><span class="sxs-lookup"><span data-stu-id="c1992-258">public uint [Time](#time)</span></span>

<span data-ttu-id="c1992-259">Esto corresponde a la propiedad dwTime de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-259">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-260">TouchContact</span><span class="sxs-lookup"><span data-stu-id="c1992-260">TouchContact</span></span> 

<span data-ttu-id="c1992-261">El TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-261">The TouchContact of the pointer event.</span></span>

> <span data-ttu-id="c1992-262">Public Rect [TouchContact](#touchcontact)</span><span class="sxs-lookup"><span data-stu-id="c1992-262">public Rect [TouchContact](#touchcontact)</span></span>

<span data-ttu-id="c1992-263">Esto corresponde a la propiedad rcContact de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-263">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-264">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="c1992-264">TouchContactRaw</span></span> 

<span data-ttu-id="c1992-265">El TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-265">The TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="c1992-266">Public Rect [TouchContactRaw](#touchcontactraw)</span><span class="sxs-lookup"><span data-stu-id="c1992-266">public Rect [TouchContactRaw](#touchcontactraw)</span></span>

<span data-ttu-id="c1992-267">Esto corresponde a la propiedad rcContactRaw de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-267">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-268">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="c1992-268">TouchFlags</span></span> 

<span data-ttu-id="c1992-269">El TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-269">The TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="c1992-270">uint pública [TouchFlags](#touchflags)</span><span class="sxs-lookup"><span data-stu-id="c1992-270">public uint [TouchFlags](#touchflags)</span></span>

<span data-ttu-id="c1992-271">Esto corresponde a la propiedad touchFlags de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="c1992-271">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="c1992-272">Los valores están definidos por las constantes de TOUCH_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-272">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-273">TouchMask</span><span class="sxs-lookup"><span data-stu-id="c1992-273">TouchMask</span></span> 

<span data-ttu-id="c1992-274">El TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-274">The TouchMask of the pointer event.</span></span>

> <span data-ttu-id="c1992-275">uint pública [TouchMask](#touchmask)</span><span class="sxs-lookup"><span data-stu-id="c1992-275">public uint [TouchMask](#touchmask)</span></span>

<span data-ttu-id="c1992-276">Esto corresponde a la propiedad touchMask de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="c1992-276">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="c1992-277">Los valores están definidos por las constantes de TOUCH_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-277">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-278">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="c1992-278">TouchOrientation</span></span> 

<span data-ttu-id="c1992-279">El TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-279">The TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="c1992-280">uint pública [TouchOrientation](#touchorientation)</span><span class="sxs-lookup"><span data-stu-id="c1992-280">public uint [TouchOrientation](#touchorientation)</span></span>

<span data-ttu-id="c1992-281">Esto corresponde a la propiedad Orientation de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-281">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c1992-282">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="c1992-282">TouchPressure</span></span> 

<span data-ttu-id="c1992-283">El TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="c1992-283">The TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="c1992-284">uint pública [TouchPressure](#touchpressure)</span><span class="sxs-lookup"><span data-stu-id="c1992-284">public uint [TouchPressure](#touchpressure)</span></span>

<span data-ttu-id="c1992-285">Esto corresponde a la propiedad de presión de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c1992-285">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>


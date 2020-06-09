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
ms.openlocfilehash: ef0546c03e2d2ccc87677125772b1663f2ec6362
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699416"
---
# <span data-ttu-id="ba093-104">interfaz ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="ba093-104">interface ICoreWebView2ExperimentalPointerInfo</span></span> 

> [!NOTE]
> <span data-ttu-id="ba093-105">Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="ba093-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="ba093-106">Esto representa principalmente un objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ba093-106">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="ba093-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="ba093-107">Summary</span></span>

 <span data-ttu-id="ba093-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ba093-108">Members</span></span>                        | <span data-ttu-id="ba093-109">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ba093-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ba093-110">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="ba093-110">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="ba093-111">Obtén la ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-111">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="ba093-112">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="ba093-112">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="ba093-113">Obtén la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-113">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="ba093-114">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="ba093-114">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="ba093-115">Obtén la FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-115">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="ba093-116">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="ba093-116">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="ba093-117">Obtén la HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-117">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="ba093-118">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ba093-118">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="ba093-119">Obtén la HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-119">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="ba093-120">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="ba093-120">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="ba093-121">Obtén la HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-121">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="ba093-122">get_InputData</span><span class="sxs-lookup"><span data-stu-id="ba093-122">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="ba093-123">Obtén la InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-123">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="ba093-124">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="ba093-124">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="ba093-125">Obtén la KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-125">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="ba093-126">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="ba093-126">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="ba093-127">Obtén la PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-127">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="ba093-128">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="ba093-128">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="ba093-129">Obtén la PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-129">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="ba093-130">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="ba093-130">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="ba093-131">Obtén la PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-131">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="ba093-132">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="ba093-132">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="ba093-133">Obtén la PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-133">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="ba093-134">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="ba093-134">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="ba093-135">Obtén la PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-135">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="ba093-136">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="ba093-136">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="ba093-137">Obtén la PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-137">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="ba093-138">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="ba093-138">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="ba093-139">Obtén la PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-139">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="ba093-140">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="ba093-140">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="ba093-141">Obtén la PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-141">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="ba093-142">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ba093-142">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="ba093-143">Obtén la PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-143">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="ba093-144">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="ba093-144">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="ba093-145">Obtén la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-145">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="ba093-146">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="ba093-146">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="ba093-147">Obtén la PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-147">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="ba093-148">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="ba093-148">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="ba093-149">Obtén la PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-149">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="ba093-150">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="ba093-150">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="ba093-151">Obtén la PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-151">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="ba093-152">get_Time</span><span class="sxs-lookup"><span data-stu-id="ba093-152">get_Time</span></span>](#get_time) | <span data-ttu-id="ba093-153">Obtener la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-153">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="ba093-154">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="ba093-154">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="ba093-155">Obtén la TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-155">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="ba093-156">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="ba093-156">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="ba093-157">Obtén la TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-157">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="ba093-158">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="ba093-158">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="ba093-159">Obtén la TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-159">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="ba093-160">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="ba093-160">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="ba093-161">Obtén la TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-161">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="ba093-162">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="ba093-162">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="ba093-163">Obtén la TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-163">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="ba093-164">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="ba093-164">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="ba093-165">Obtén la TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-165">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="ba093-166">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="ba093-166">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="ba093-167">Establezca el ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-167">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="ba093-168">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="ba093-168">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="ba093-169">Establezca la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-169">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="ba093-170">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="ba093-170">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="ba093-171">Establezca el FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-171">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="ba093-172">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="ba093-172">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="ba093-173">Establezca el HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-173">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="ba093-174">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ba093-174">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="ba093-175">Establezca el HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-175">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="ba093-176">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="ba093-176">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="ba093-177">Establezca el HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-177">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="ba093-178">put_InputData</span><span class="sxs-lookup"><span data-stu-id="ba093-178">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="ba093-179">Establezca el InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-179">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="ba093-180">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="ba093-180">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="ba093-181">Establezca el KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-181">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="ba093-182">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="ba093-182">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="ba093-183">Establezca el PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-183">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="ba093-184">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="ba093-184">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="ba093-185">Establezca el PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-185">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="ba093-186">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="ba093-186">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="ba093-187">Establezca el PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-187">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="ba093-188">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="ba093-188">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="ba093-189">Establezca el PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-189">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="ba093-190">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="ba093-190">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="ba093-191">Establezca el PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-191">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="ba093-192">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="ba093-192">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="ba093-193">Establezca el PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-193">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="ba093-194">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="ba093-194">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="ba093-195">Establezca el PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-195">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="ba093-196">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="ba093-196">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="ba093-197">Establezca el PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-197">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="ba093-198">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ba093-198">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="ba093-199">Establezca el PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-199">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="ba093-200">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="ba093-200">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="ba093-201">Establezca la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-201">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="ba093-202">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="ba093-202">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="ba093-203">Establezca el PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-203">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="ba093-204">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="ba093-204">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="ba093-205">Establezca el PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-205">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="ba093-206">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="ba093-206">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="ba093-207">Establezca el PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-207">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="ba093-208">put_Time</span><span class="sxs-lookup"><span data-stu-id="ba093-208">put_Time</span></span>](#put_time) | <span data-ttu-id="ba093-209">Establezca la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-209">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="ba093-210">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="ba093-210">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="ba093-211">Establezca el TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-211">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="ba093-212">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="ba093-212">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="ba093-213">Establezca el TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-213">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="ba093-214">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="ba093-214">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="ba093-215">Establezca el TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-215">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="ba093-216">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="ba093-216">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="ba093-217">Establezca el TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-217">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="ba093-218">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="ba093-218">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="ba093-219">Establezca el TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-219">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="ba093-220">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="ba093-220">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="ba093-221">Establezca el TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-221">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="ba093-222">Toma campos de los tres y excluye algunos tipos de datos específicos de Win32, como HWND y HANDLE.</span><span class="sxs-lookup"><span data-stu-id="ba093-222">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="ba093-223">Ten en cuenta que sourceDevice se extrae, pero esperamos que PointerDeviceRect y DisplayRect cubran los casos de uso existentes de sourceDevice.</span><span class="sxs-lookup"><span data-stu-id="ba093-223">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="ba093-224">Otra diferencia importante es que se espera que cualquiera de las ubicaciones de Point o Rect estén en coordenadas físicas de WebView.</span><span class="sxs-lookup"><span data-stu-id="ba093-224">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="ba093-225">Es decir, se aplican a las coordenadas relativas a la vista de WebView y sin ajuste de PPP.</span><span class="sxs-lookup"><span data-stu-id="ba093-225">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="ba093-226">Miembros</span><span class="sxs-lookup"><span data-stu-id="ba093-226">Members</span></span>

#### <span data-ttu-id="ba093-227">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="ba093-227">get_ButtonChangeKind</span></span> 

<span data-ttu-id="ba093-228">Obtén la ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-228">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="ba093-229">[get_ButtonChangeKind](#get_buttonchangekind)de HRESULT público (INT32 \* ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="ba093-229">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="ba093-230">Esto corresponde a la propiedad ButtonChangeKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ba093-230">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ba093-231">Los valores están definidos por la enumeración POINTER_BUTTON_CHANGE_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-231">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-232">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="ba093-232">get_DisplayRect</span></span> 

<span data-ttu-id="ba093-233">Obtén la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-233">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="ba093-234">[get_DisplayRect](#get_displayrect)de HRESULT público (Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="ba093-234">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="ba093-235">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="ba093-235">get_FrameId</span></span> 

<span data-ttu-id="ba093-236">Obtén la FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-236">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="ba093-237">[get_FrameId](#get_frameid)de HRESULT público (UINT32 \* FrameId)</span><span class="sxs-lookup"><span data-stu-id="ba093-237">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="ba093-238">Esto corresponde a la propiedad frameId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-238">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-239">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="ba093-239">get_HimetricLocation</span></span> 

<span data-ttu-id="ba093-240">Obtén la HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-240">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="ba093-241">[get_HimetricLocation](#get_himetriclocation)de HRESULT público (Point \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="ba093-241">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="ba093-242">Esto corresponde a la propiedad ptHimetricLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-242">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-243">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ba093-243">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="ba093-244">Obtén la HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-244">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="ba093-245">[get_HimetricLocationRaw](#get_himetriclocationraw)de HRESULT público (Point \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="ba093-245">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="ba093-246">Esto corresponde a la propiedad ptHimetricLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-246">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-247">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="ba093-247">get_HistoryCount</span></span> 

<span data-ttu-id="ba093-248">Obtén la HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-248">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="ba093-249">[get_HistoryCount](#get_historycount)de HRESULT público (UINT32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="ba093-249">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="ba093-250">Esto corresponde a la propiedad historyCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-250">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-251">get_InputData</span><span class="sxs-lookup"><span data-stu-id="ba093-251">get_InputData</span></span> 

<span data-ttu-id="ba093-252">Obtén la InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-252">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="ba093-253">[get_InputData](#get_inputdata)de HRESULT público (INT32 \* InputData)</span><span class="sxs-lookup"><span data-stu-id="ba093-253">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="ba093-254">Esto corresponde a la propiedad InputData de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-254">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-255">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="ba093-255">get_KeyStates</span></span> 

<span data-ttu-id="ba093-256">Obtén la KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-256">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="ba093-257">[get_KeyStates](#get_keystates)de HRESULT público (DWORD \* KeyStates)</span><span class="sxs-lookup"><span data-stu-id="ba093-257">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="ba093-258">Esto corresponde a la propiedad dwKeyStates de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-258">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-259">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="ba093-259">get_PenFlags</span></span> 

<span data-ttu-id="ba093-260">Obtén la PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-260">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="ba093-261">[get_PenFlags](#get_penflags)de HRESULT público (UINT32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="ba093-261">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="ba093-262">Esto corresponde a la propiedad penFlags de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ba093-262">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="ba093-263">Los valores están definidos por las constantes de PEN_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-263">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-264">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="ba093-264">get_PenMask</span></span> 

<span data-ttu-id="ba093-265">Obtén la PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-265">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="ba093-266">[get_PenMask](#get_penmask)de HRESULT público (UINT32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="ba093-266">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="ba093-267">Esto corresponde a la propiedad penMask de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ba093-267">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="ba093-268">Los valores están definidos por las constantes de PEN_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-268">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-269">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="ba093-269">get_PenPressure</span></span> 

<span data-ttu-id="ba093-270">Obtén la PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-270">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="ba093-271">[get_PenPressure](#get_penpressure)de HRESULT público (UINT32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="ba093-271">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="ba093-272">Esto corresponde a la propiedad de presión de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-272">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-273">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="ba093-273">get_PenRotation</span></span> 

<span data-ttu-id="ba093-274">Obtén la PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-274">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="ba093-275">[get_PenRotation](#get_penrotation)de HRESULT público (UINT32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="ba093-275">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="ba093-276">Esto corresponde a la propiedad Rotation de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-276">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-277">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="ba093-277">get_PenTiltX</span></span> 

<span data-ttu-id="ba093-278">Obtén la PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-278">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="ba093-279">[get_PenTiltX](#get_pentiltx)de HRESULT público (INT32 \* PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="ba093-279">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="ba093-280">Esto corresponde a la propiedad tiltX de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-280">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-281">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="ba093-281">get_PenTiltY</span></span> 

<span data-ttu-id="ba093-282">Obtén la PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-282">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="ba093-283">[get_PenTiltY](#get_pentilty)de HRESULT público (INT32 \* PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="ba093-283">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="ba093-284">Esto corresponde a la propiedad Tilt de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-284">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-285">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="ba093-285">get_PerformanceCount</span></span> 

<span data-ttu-id="ba093-286">Obtén la PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-286">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="ba093-287">[get_PerformanceCount](#get_performancecount)(HRESULT) público (UINT64 \* PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="ba093-287">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="ba093-288">Esto corresponde a la propiedad PerformanceCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-288">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-289">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="ba093-289">get_PixelLocation</span></span> 

<span data-ttu-id="ba093-290">Obtén la PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-290">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="ba093-291">[get_PixelLocation](#get_pixellocation)de HRESULT público (Point \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="ba093-291">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="ba093-292">Esto corresponde a la propiedad ptPixelLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-292">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-293">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ba093-293">get_PixelLocationRaw</span></span> 

<span data-ttu-id="ba093-294">Obtén la PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-294">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="ba093-295">[get_PixelLocationRaw](#get_pixellocationraw)de HRESULT público (Point \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="ba093-295">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="ba093-296">Esto corresponde a la propiedad ptPixelLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-296">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-297">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="ba093-297">get_PointerDeviceRect</span></span> 

<span data-ttu-id="ba093-298">Obtén la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-298">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="ba093-299">[get_PointerDeviceRect](#get_pointerdevicerect)de HRESULT público (Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="ba093-299">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="ba093-300">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="ba093-300">get_PointerFlags</span></span> 

<span data-ttu-id="ba093-301">Obtén la PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-301">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="ba093-302">[get_PointerFlags](#get_pointerflags)de HRESULT público (UINT32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="ba093-302">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="ba093-303">Esto corresponde a la propiedad pointerFlags de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ba093-303">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ba093-304">Los valores están definidos por las constantes de POINTER_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-304">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-305">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="ba093-305">get_PointerId</span></span> 

<span data-ttu-id="ba093-306">Obtén la PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-306">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="ba093-307">[get_PointerId](#get_pointerid)de HRESULT público (UINT32 \* PointerId)</span><span class="sxs-lookup"><span data-stu-id="ba093-307">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="ba093-308">Esto corresponde a la propiedad pointerId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-308">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-309">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="ba093-309">get_PointerKind</span></span> 

<span data-ttu-id="ba093-310">Obtén la PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-310">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="ba093-311">[get_PointerKind](#get_pointerkind)de HRESULT público (DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="ba093-311">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="ba093-312">Esto corresponde a la propiedad pointerKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ba093-312">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ba093-313">Los valores están definidos por la enumeración POINTER_INPUT_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-313">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="ba093-314">Es compatible con PT_PEN y PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="ba093-314">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="ba093-315">get_Time</span><span class="sxs-lookup"><span data-stu-id="ba093-315">get_Time</span></span> 

<span data-ttu-id="ba093-316">Obtener la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-316">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="ba093-317">[get_Time](#get_time)de HRESULT público (DWORD \* hora)</span><span class="sxs-lookup"><span data-stu-id="ba093-317">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="ba093-318">Esto corresponde a la propiedad dwTime de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-318">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-319">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="ba093-319">get_TouchContact</span></span> 

<span data-ttu-id="ba093-320">Obtén la TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-320">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="ba093-321">[get_TouchContact](#get_touchcontact)de HRESULT público (Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="ba093-321">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="ba093-322">Esto corresponde a la propiedad rcContact de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-322">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-323">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="ba093-323">get_TouchContactRaw</span></span> 

<span data-ttu-id="ba093-324">Obtén la TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-324">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="ba093-325">[get_TouchContactRaw](#get_touchcontactraw)de HRESULT público (Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="ba093-325">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="ba093-326">Esto corresponde a la propiedad rcContactRaw de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-326">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-327">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="ba093-327">get_TouchFlags</span></span> 

<span data-ttu-id="ba093-328">Obtén la TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-328">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="ba093-329">[get_TouchFlags](#get_touchflags)de HRESULT público (UINT32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="ba093-329">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="ba093-330">Esto corresponde a la propiedad touchFlags de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="ba093-330">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="ba093-331">Los valores están definidos por las constantes de TOUCH_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-331">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-332">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="ba093-332">get_TouchMask</span></span> 

<span data-ttu-id="ba093-333">Obtén la TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-333">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="ba093-334">[get_TouchMask](#get_touchmask)de HRESULT público (UINT32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="ba093-334">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="ba093-335">Esto corresponde a la propiedad touchMask de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="ba093-335">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="ba093-336">Los valores están definidos por las constantes de TOUCH_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-336">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-337">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="ba093-337">get_TouchOrientation</span></span> 

<span data-ttu-id="ba093-338">Obtén la TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-338">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="ba093-339">[get_TouchOrientation](#get_touchorientation)de HRESULT público (UINT32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="ba093-339">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="ba093-340">Esto corresponde a la propiedad Orientation de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-340">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-341">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="ba093-341">get_TouchPressure</span></span> 

<span data-ttu-id="ba093-342">Obtén la TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-342">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="ba093-343">[get_TouchPressure](#get_touchpressure)de HRESULT público (UINT32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="ba093-343">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="ba093-344">Esto corresponde a la propiedad de presión de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-344">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-345">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="ba093-345">put_ButtonChangeKind</span></span> 

<span data-ttu-id="ba093-346">Establezca el ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-346">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="ba093-347">[put_ButtonChangeKind](#put_buttonchangekind)de HRESULT público (INT32 ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="ba093-347">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="ba093-348">Esto corresponde a la propiedad ButtonChangeKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ba093-348">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ba093-349">Los valores están definidos por la enumeración POINTER_BUTTON_CHANGE_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-349">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-350">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="ba093-350">put_DisplayRect</span></span> 

<span data-ttu-id="ba093-351">Establezca la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-351">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="ba093-352">[put_DisplayRect](#put_displayrect)de HRESULT público (Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="ba093-352">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="ba093-353">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="ba093-353">put_FrameId</span></span> 

<span data-ttu-id="ba093-354">Establezca el FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-354">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="ba093-355">[put_FrameId](#put_frameid)de HRESULT público (UINT32 FrameId)</span><span class="sxs-lookup"><span data-stu-id="ba093-355">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="ba093-356">Esto corresponde a la propiedad frameId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-356">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-357">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="ba093-357">put_HimetricLocation</span></span> 

<span data-ttu-id="ba093-358">Establezca el HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-358">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="ba093-359">[put_HimetricLocation](#put_himetriclocation)de HRESULT público (Point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="ba093-359">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="ba093-360">Esto corresponde a la propiedad ptHimetricLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-360">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-361">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ba093-361">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="ba093-362">Establezca el HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-362">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="ba093-363">[put_HimetricLocationRaw](#put_himetriclocationraw)de HRESULT público (Point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="ba093-363">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="ba093-364">Esto corresponde a la propiedad ptHimetricLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-364">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-365">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="ba093-365">put_HistoryCount</span></span> 

<span data-ttu-id="ba093-366">Establezca el HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-366">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="ba093-367">[put_HistoryCount](#put_historycount)de HRESULT público (UINT32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="ba093-367">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="ba093-368">Esto corresponde a la propiedad historyCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-368">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-369">put_InputData</span><span class="sxs-lookup"><span data-stu-id="ba093-369">put_InputData</span></span> 

<span data-ttu-id="ba093-370">Establezca el InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-370">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="ba093-371">[put_InputData](#put_inputdata)de HRESULT público (INT32 InputData)</span><span class="sxs-lookup"><span data-stu-id="ba093-371">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="ba093-372">Esto corresponde a la propiedad InputData de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-372">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-373">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="ba093-373">put_KeyStates</span></span> 

<span data-ttu-id="ba093-374">Establezca el KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-374">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="ba093-375">[put_KeyStates](#put_keystates)de HRESULT público (DWORD KeyStates)</span><span class="sxs-lookup"><span data-stu-id="ba093-375">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="ba093-376">Esto corresponde a la propiedad dwKeyStates de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-376">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-377">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="ba093-377">put_PenFlags</span></span> 

<span data-ttu-id="ba093-378">Establezca el PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-378">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="ba093-379">[put_PenFlags](#put_penflags)de HRESULT público (UINT32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="ba093-379">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="ba093-380">Esto corresponde a la propiedad penFlags de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ba093-380">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="ba093-381">Los valores están definidos por las constantes de PEN_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-381">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-382">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="ba093-382">put_PenMask</span></span> 

<span data-ttu-id="ba093-383">Establezca el PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-383">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="ba093-384">[put_PenMask](#put_penmask)de HRESULT público (UINT32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="ba093-384">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="ba093-385">Esto corresponde a la propiedad penMask de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ba093-385">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="ba093-386">Los valores están definidos por las constantes de PEN_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-386">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-387">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="ba093-387">put_PenPressure</span></span> 

<span data-ttu-id="ba093-388">Establezca el PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-388">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="ba093-389">[put_PenPressure](#put_penpressure)de HRESULT público (UINT32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="ba093-389">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="ba093-390">Esto corresponde a la propiedad de presión de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-390">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-391">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="ba093-391">put_PenRotation</span></span> 

<span data-ttu-id="ba093-392">Establezca el PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-392">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="ba093-393">[put_PenRotation](#put_penrotation)de HRESULT público (UINT32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="ba093-393">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="ba093-394">Esto corresponde a la propiedad Rotation de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-394">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-395">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="ba093-395">put_PenTiltX</span></span> 

<span data-ttu-id="ba093-396">Establezca el PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-396">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="ba093-397">[put_PenTiltX](#put_pentiltx)de HRESULT público (INT32 PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="ba093-397">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="ba093-398">Esto corresponde a la propiedad tiltX de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-398">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-399">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="ba093-399">put_PenTiltY</span></span> 

<span data-ttu-id="ba093-400">Establezca el PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-400">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="ba093-401">[put_PenTiltY](#put_pentilty)de HRESULT público (INT32 PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="ba093-401">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="ba093-402">Esto corresponde a la propiedad Tilt de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-402">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-403">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="ba093-403">put_PerformanceCount</span></span> 

<span data-ttu-id="ba093-404">Establezca el PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-404">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="ba093-405">[put_PerformanceCount](#put_performancecount)(HRESULT) público (UINT64 PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="ba093-405">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="ba093-406">Esto corresponde a la propiedad PerformanceCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-406">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-407">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="ba093-407">put_PixelLocation</span></span> 

<span data-ttu-id="ba093-408">Establezca el PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-408">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="ba093-409">[put_PixelLocation](#put_pixellocation)de HRESULT público (Point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="ba093-409">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="ba093-410">Esto corresponde a la propiedad ptPixelLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-410">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-411">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ba093-411">put_PixelLocationRaw</span></span> 

<span data-ttu-id="ba093-412">Establezca el PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-412">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="ba093-413">[put_PixelLocationRaw](#put_pixellocationraw)de HRESULT público (Point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="ba093-413">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="ba093-414">Esto corresponde a la propiedad ptPixelLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-414">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-415">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="ba093-415">put_PointerDeviceRect</span></span> 

<span data-ttu-id="ba093-416">Establezca la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-416">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="ba093-417">[put_PointerDeviceRect](#put_pointerdevicerect)de HRESULT público (Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="ba093-417">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="ba093-418">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="ba093-418">put_PointerFlags</span></span> 

<span data-ttu-id="ba093-419">Establezca el PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-419">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="ba093-420">[put_PointerFlags](#put_pointerflags)de HRESULT público (UINT32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="ba093-420">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="ba093-421">Esto corresponde a la propiedad pointerFlags de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ba093-421">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ba093-422">Los valores están definidos por las constantes de POINTER_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-422">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-423">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="ba093-423">put_PointerId</span></span> 

<span data-ttu-id="ba093-424">Establezca el PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-424">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="ba093-425">[put_PointerId](#put_pointerid)de HRESULT público (UINT32 PointerId)</span><span class="sxs-lookup"><span data-stu-id="ba093-425">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="ba093-426">Esto corresponde a la propiedad pointerId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-426">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-427">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="ba093-427">put_PointerKind</span></span> 

<span data-ttu-id="ba093-428">Establezca el PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-428">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="ba093-429">[put_PointerKind](#put_pointerkind)de HRESULT público (DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="ba093-429">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="ba093-430">Esto corresponde a la propiedad pointerKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ba093-430">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ba093-431">Los valores están definidos por la enumeración POINTER_INPUT_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-431">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="ba093-432">Es compatible con PT_PEN y PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="ba093-432">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="ba093-433">put_Time</span><span class="sxs-lookup"><span data-stu-id="ba093-433">put_Time</span></span> 

<span data-ttu-id="ba093-434">Establezca la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-434">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="ba093-435">[put_Time](#put_time)de HRESULT público (hora de DWORD)</span><span class="sxs-lookup"><span data-stu-id="ba093-435">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="ba093-436">Esto corresponde a la propiedad dwTime de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-436">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-437">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="ba093-437">put_TouchContact</span></span> 

<span data-ttu-id="ba093-438">Establezca el TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-438">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="ba093-439">[put_TouchContact](#put_touchcontact)de HRESULT público (Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="ba093-439">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="ba093-440">Esto corresponde a la propiedad rcContact de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-440">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-441">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="ba093-441">put_TouchContactRaw</span></span> 

<span data-ttu-id="ba093-442">Establezca el TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-442">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="ba093-443">[put_TouchContactRaw](#put_touchcontactraw)de HRESULT público (Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="ba093-443">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="ba093-444">Esto corresponde a la propiedad rcContactRaw de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-444">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-445">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="ba093-445">put_TouchFlags</span></span> 

<span data-ttu-id="ba093-446">Establezca el TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-446">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="ba093-447">[put_TouchFlags](#put_touchflags)de HRESULT público (UINT32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="ba093-447">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="ba093-448">Esto corresponde a la propiedad touchFlags de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="ba093-448">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="ba093-449">Los valores están definidos por las constantes de TOUCH_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-449">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-450">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="ba093-450">put_TouchMask</span></span> 

<span data-ttu-id="ba093-451">Establezca el TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-451">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="ba093-452">[put_TouchMask](#put_touchmask)de HRESULT público (UINT32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="ba093-452">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="ba093-453">Esto corresponde a la propiedad touchMask de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="ba093-453">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="ba093-454">Los valores están definidos por las constantes de TOUCH_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-454">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-455">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="ba093-455">put_TouchOrientation</span></span> 

<span data-ttu-id="ba093-456">Establezca el TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-456">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="ba093-457">[put_TouchOrientation](#put_touchorientation)de HRESULT público (UINT32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="ba093-457">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="ba093-458">Esto corresponde a la propiedad Orientation de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-458">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ba093-459">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="ba093-459">put_TouchPressure</span></span> 

<span data-ttu-id="ba093-460">Establezca el TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ba093-460">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="ba093-461">[put_TouchPressure](#put_touchpressure)de HRESULT público (UINT32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="ba093-461">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="ba093-462">Esto corresponde a la propiedad de presión de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ba093-462">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>


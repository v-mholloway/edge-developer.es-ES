---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalPointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalPointerInfo
ms.openlocfilehash: bc35ebaf3f1b5acf12a1d379336cd006f962390e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012736"
---
# <span data-ttu-id="462fd-104">interfaz ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="462fd-104">interface ICoreWebView2ExperimentalPointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="462fd-105">Esto representa principalmente un objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="462fd-105">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="462fd-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="462fd-106">Summary</span></span>

 <span data-ttu-id="462fd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="462fd-107">Members</span></span>                        | <span data-ttu-id="462fd-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="462fd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="462fd-109">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="462fd-109">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="462fd-110">Obtén la ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-110">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="462fd-111">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="462fd-111">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="462fd-112">Obtén la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-112">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="462fd-113">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="462fd-113">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="462fd-114">Obtén la FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-114">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="462fd-115">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="462fd-115">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="462fd-116">Obtén la HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-116">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="462fd-117">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="462fd-117">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="462fd-118">Obtén la HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-118">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="462fd-119">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="462fd-119">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="462fd-120">Obtén la HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-120">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="462fd-121">get_InputData</span><span class="sxs-lookup"><span data-stu-id="462fd-121">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="462fd-122">Obtén la InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-122">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="462fd-123">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="462fd-123">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="462fd-124">Obtén la KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-124">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="462fd-125">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="462fd-125">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="462fd-126">Obtén la PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-126">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="462fd-127">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="462fd-127">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="462fd-128">Obtén la PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-128">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="462fd-129">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="462fd-129">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="462fd-130">Obtén la PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-130">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="462fd-131">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="462fd-131">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="462fd-132">Obtén la PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-132">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="462fd-133">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="462fd-133">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="462fd-134">Obtén la PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-134">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="462fd-135">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="462fd-135">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="462fd-136">Obtén la PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-136">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="462fd-137">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="462fd-137">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="462fd-138">Obtén la PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-138">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="462fd-139">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="462fd-139">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="462fd-140">Obtén la PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-140">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="462fd-141">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="462fd-141">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="462fd-142">Obtén la PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-142">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="462fd-143">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="462fd-143">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="462fd-144">Obtén la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-144">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="462fd-145">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="462fd-145">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="462fd-146">Obtén la PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-146">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="462fd-147">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="462fd-147">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="462fd-148">Obtén la PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-148">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="462fd-149">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="462fd-149">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="462fd-150">Obtén la PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-150">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="462fd-151">get_Time</span><span class="sxs-lookup"><span data-stu-id="462fd-151">get_Time</span></span>](#get_time) | <span data-ttu-id="462fd-152">Obtener la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-152">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="462fd-153">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="462fd-153">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="462fd-154">Obtén la TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-154">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="462fd-155">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="462fd-155">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="462fd-156">Obtén la TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-156">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="462fd-157">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="462fd-157">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="462fd-158">Obtén la TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-158">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="462fd-159">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="462fd-159">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="462fd-160">Obtén la TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-160">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="462fd-161">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="462fd-161">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="462fd-162">Obtén la TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-162">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="462fd-163">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="462fd-163">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="462fd-164">Obtén la TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-164">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="462fd-165">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="462fd-165">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="462fd-166">Establezca el ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-166">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="462fd-167">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="462fd-167">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="462fd-168">Establezca la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-168">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="462fd-169">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="462fd-169">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="462fd-170">Establezca el FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-170">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="462fd-171">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="462fd-171">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="462fd-172">Establezca el HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-172">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="462fd-173">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="462fd-173">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="462fd-174">Establezca el HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-174">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="462fd-175">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="462fd-175">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="462fd-176">Establezca el HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-176">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="462fd-177">put_InputData</span><span class="sxs-lookup"><span data-stu-id="462fd-177">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="462fd-178">Establezca el InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-178">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="462fd-179">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="462fd-179">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="462fd-180">Establezca el KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-180">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="462fd-181">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="462fd-181">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="462fd-182">Establezca el PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-182">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="462fd-183">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="462fd-183">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="462fd-184">Establezca el PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-184">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="462fd-185">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="462fd-185">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="462fd-186">Establezca el PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-186">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="462fd-187">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="462fd-187">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="462fd-188">Establezca el PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-188">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="462fd-189">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="462fd-189">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="462fd-190">Establezca el PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-190">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="462fd-191">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="462fd-191">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="462fd-192">Establezca el PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-192">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="462fd-193">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="462fd-193">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="462fd-194">Establezca el PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-194">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="462fd-195">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="462fd-195">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="462fd-196">Establezca el PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-196">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="462fd-197">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="462fd-197">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="462fd-198">Establezca el PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-198">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="462fd-199">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="462fd-199">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="462fd-200">Establezca la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-200">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="462fd-201">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="462fd-201">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="462fd-202">Establezca el PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-202">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="462fd-203">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="462fd-203">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="462fd-204">Establezca el PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-204">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="462fd-205">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="462fd-205">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="462fd-206">Establezca el PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-206">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="462fd-207">put_Time</span><span class="sxs-lookup"><span data-stu-id="462fd-207">put_Time</span></span>](#put_time) | <span data-ttu-id="462fd-208">Establezca la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-208">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="462fd-209">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="462fd-209">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="462fd-210">Establezca el TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-210">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="462fd-211">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="462fd-211">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="462fd-212">Establezca el TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-212">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="462fd-213">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="462fd-213">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="462fd-214">Establezca el TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-214">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="462fd-215">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="462fd-215">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="462fd-216">Establezca el TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-216">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="462fd-217">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="462fd-217">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="462fd-218">Establezca el TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-218">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="462fd-219">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="462fd-219">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="462fd-220">Establezca el TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-220">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="462fd-221">Toma campos de los tres y excluye algunos tipos de datos específicos de Win32, como HWND y HANDLE.</span><span class="sxs-lookup"><span data-stu-id="462fd-221">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="462fd-222">Ten en cuenta que sourceDevice se extrae, pero esperamos que PointerDeviceRect y DisplayRect cubran los casos de uso existentes de sourceDevice.</span><span class="sxs-lookup"><span data-stu-id="462fd-222">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="462fd-223">Otra diferencia importante es que se espera que cualquiera de las ubicaciones de Point o Rect estén en coordenadas físicas de WebView.</span><span class="sxs-lookup"><span data-stu-id="462fd-223">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="462fd-224">Es decir, se aplican a las coordenadas relativas a la vista de WebView y sin ajuste de PPP.</span><span class="sxs-lookup"><span data-stu-id="462fd-224">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="462fd-225">Miembros</span><span class="sxs-lookup"><span data-stu-id="462fd-225">Members</span></span>

#### <span data-ttu-id="462fd-226">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="462fd-226">get_ButtonChangeKind</span></span> 

<span data-ttu-id="462fd-227">Obtén la ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-227">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="462fd-228">[get_ButtonChangeKind](#get_buttonchangekind)de HRESULT público (INT32 \* ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="462fd-228">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="462fd-229">Esto corresponde a la propiedad ButtonChangeKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="462fd-229">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="462fd-230">Los valores están definidos por la enumeración POINTER_BUTTON_CHANGE_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-230">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-231">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="462fd-231">get_DisplayRect</span></span> 

<span data-ttu-id="462fd-232">Obtén la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-232">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="462fd-233">[get_DisplayRect](#get_displayrect)de HRESULT público (Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="462fd-233">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="462fd-234">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="462fd-234">get_FrameId</span></span> 

<span data-ttu-id="462fd-235">Obtén la FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-235">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="462fd-236">[get_FrameId](#get_frameid)de HRESULT público (UINT32 \* FrameId)</span><span class="sxs-lookup"><span data-stu-id="462fd-236">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="462fd-237">Esto corresponde a la propiedad frameId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-237">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-238">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="462fd-238">get_HimetricLocation</span></span> 

<span data-ttu-id="462fd-239">Obtén la HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-239">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="462fd-240">[get_HimetricLocation](#get_himetriclocation)de HRESULT público (Point \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="462fd-240">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="462fd-241">Esto corresponde a la propiedad ptHimetricLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-241">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-242">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="462fd-242">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="462fd-243">Obtén la HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-243">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="462fd-244">[get_HimetricLocationRaw](#get_himetriclocationraw)de HRESULT público (Point \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="462fd-244">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="462fd-245">Esto corresponde a la propiedad ptHimetricLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-245">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-246">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="462fd-246">get_HistoryCount</span></span> 

<span data-ttu-id="462fd-247">Obtén la HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-247">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="462fd-248">[get_HistoryCount](#get_historycount)de HRESULT público (UINT32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="462fd-248">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="462fd-249">Esto corresponde a la propiedad historyCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-249">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-250">get_InputData</span><span class="sxs-lookup"><span data-stu-id="462fd-250">get_InputData</span></span> 

<span data-ttu-id="462fd-251">Obtén la InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-251">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="462fd-252">[get_InputData](#get_inputdata)de HRESULT público (INT32 \* InputData)</span><span class="sxs-lookup"><span data-stu-id="462fd-252">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="462fd-253">Esto corresponde a la propiedad InputData de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-253">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-254">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="462fd-254">get_KeyStates</span></span> 

<span data-ttu-id="462fd-255">Obtén la KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-255">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="462fd-256">[get_KeyStates](#get_keystates)de HRESULT público (DWORD \* KeyStates)</span><span class="sxs-lookup"><span data-stu-id="462fd-256">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="462fd-257">Esto corresponde a la propiedad dwKeyStates de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-257">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-258">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="462fd-258">get_PenFlags</span></span> 

<span data-ttu-id="462fd-259">Obtén la PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-259">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="462fd-260">[get_PenFlags](#get_penflags)de HRESULT público (UINT32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="462fd-260">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="462fd-261">Esto corresponde a la propiedad penFlags de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="462fd-261">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="462fd-262">Los valores están definidos por las constantes de PEN_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-262">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-263">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="462fd-263">get_PenMask</span></span> 

<span data-ttu-id="462fd-264">Obtén la PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-264">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="462fd-265">[get_PenMask](#get_penmask)de HRESULT público (UINT32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="462fd-265">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="462fd-266">Esto corresponde a la propiedad penMask de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="462fd-266">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="462fd-267">Los valores están definidos por las constantes de PEN_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-267">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-268">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="462fd-268">get_PenPressure</span></span> 

<span data-ttu-id="462fd-269">Obtén la PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-269">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="462fd-270">[get_PenPressure](#get_penpressure)de HRESULT público (UINT32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="462fd-270">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="462fd-271">Esto corresponde a la propiedad de presión de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-271">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-272">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="462fd-272">get_PenRotation</span></span> 

<span data-ttu-id="462fd-273">Obtén la PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-273">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="462fd-274">[get_PenRotation](#get_penrotation)de HRESULT público (UINT32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="462fd-274">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="462fd-275">Esto corresponde a la propiedad Rotation de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-275">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-276">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="462fd-276">get_PenTiltX</span></span> 

<span data-ttu-id="462fd-277">Obtén la PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-277">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="462fd-278">[get_PenTiltX](#get_pentiltx)de HRESULT público (INT32 \* PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="462fd-278">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="462fd-279">Esto corresponde a la propiedad tiltX de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-279">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-280">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="462fd-280">get_PenTiltY</span></span> 

<span data-ttu-id="462fd-281">Obtén la PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-281">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="462fd-282">[get_PenTiltY](#get_pentilty)de HRESULT público (INT32 \* PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="462fd-282">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="462fd-283">Esto corresponde a la propiedad Tilt de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-283">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-284">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="462fd-284">get_PerformanceCount</span></span> 

<span data-ttu-id="462fd-285">Obtén la PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-285">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="462fd-286">[get_PerformanceCount](#get_performancecount)(HRESULT) público (UINT64 \* PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="462fd-286">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="462fd-287">Esto corresponde a la propiedad PerformanceCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-287">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-288">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="462fd-288">get_PixelLocation</span></span> 

<span data-ttu-id="462fd-289">Obtén la PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-289">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="462fd-290">[get_PixelLocation](#get_pixellocation)de HRESULT público (Point \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="462fd-290">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="462fd-291">Esto corresponde a la propiedad ptPixelLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-291">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-292">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="462fd-292">get_PixelLocationRaw</span></span> 

<span data-ttu-id="462fd-293">Obtén la PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-293">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="462fd-294">[get_PixelLocationRaw](#get_pixellocationraw)de HRESULT público (Point \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="462fd-294">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="462fd-295">Esto corresponde a la propiedad ptPixelLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-295">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-296">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="462fd-296">get_PointerDeviceRect</span></span> 

<span data-ttu-id="462fd-297">Obtén la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-297">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="462fd-298">[get_PointerDeviceRect](#get_pointerdevicerect)de HRESULT público (Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="462fd-298">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="462fd-299">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="462fd-299">get_PointerFlags</span></span> 

<span data-ttu-id="462fd-300">Obtén la PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-300">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="462fd-301">[get_PointerFlags](#get_pointerflags)de HRESULT público (UINT32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="462fd-301">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="462fd-302">Esto corresponde a la propiedad pointerFlags de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="462fd-302">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="462fd-303">Los valores están definidos por las constantes de POINTER_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-303">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-304">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="462fd-304">get_PointerId</span></span> 

<span data-ttu-id="462fd-305">Obtén la PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-305">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="462fd-306">[get_PointerId](#get_pointerid)de HRESULT público (UINT32 \* PointerId)</span><span class="sxs-lookup"><span data-stu-id="462fd-306">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="462fd-307">Esto corresponde a la propiedad pointerId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-307">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-308">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="462fd-308">get_PointerKind</span></span> 

<span data-ttu-id="462fd-309">Obtén la PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-309">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="462fd-310">[get_PointerKind](#get_pointerkind)de HRESULT público (DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="462fd-310">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="462fd-311">Esto corresponde a la propiedad pointerKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="462fd-311">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="462fd-312">Los valores están definidos por la enumeración POINTER_INPUT_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-312">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="462fd-313">Es compatible con PT_PEN y PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="462fd-313">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="462fd-314">get_Time</span><span class="sxs-lookup"><span data-stu-id="462fd-314">get_Time</span></span> 

<span data-ttu-id="462fd-315">Obtener la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-315">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="462fd-316">[get_Time](#get_time)de HRESULT público (DWORD \* hora)</span><span class="sxs-lookup"><span data-stu-id="462fd-316">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="462fd-317">Esto corresponde a la propiedad dwTime de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-317">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-318">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="462fd-318">get_TouchContact</span></span> 

<span data-ttu-id="462fd-319">Obtén la TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-319">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="462fd-320">[get_TouchContact](#get_touchcontact)de HRESULT público (Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="462fd-320">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="462fd-321">Esto corresponde a la propiedad rcContact de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-321">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-322">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="462fd-322">get_TouchContactRaw</span></span> 

<span data-ttu-id="462fd-323">Obtén la TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-323">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="462fd-324">[get_TouchContactRaw](#get_touchcontactraw)de HRESULT público (Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="462fd-324">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="462fd-325">Esto corresponde a la propiedad rcContactRaw de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-325">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-326">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="462fd-326">get_TouchFlags</span></span> 

<span data-ttu-id="462fd-327">Obtén la TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-327">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="462fd-328">[get_TouchFlags](#get_touchflags)de HRESULT público (UINT32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="462fd-328">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="462fd-329">Esto corresponde a la propiedad touchFlags de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="462fd-329">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="462fd-330">Los valores están definidos por las constantes de TOUCH_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-330">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-331">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="462fd-331">get_TouchMask</span></span> 

<span data-ttu-id="462fd-332">Obtén la TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-332">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="462fd-333">[get_TouchMask](#get_touchmask)de HRESULT público (UINT32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="462fd-333">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="462fd-334">Esto corresponde a la propiedad touchMask de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="462fd-334">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="462fd-335">Los valores están definidos por las constantes de TOUCH_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-335">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-336">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="462fd-336">get_TouchOrientation</span></span> 

<span data-ttu-id="462fd-337">Obtén la TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-337">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="462fd-338">[get_TouchOrientation](#get_touchorientation)de HRESULT público (UINT32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="462fd-338">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="462fd-339">Esto corresponde a la propiedad Orientation de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-339">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-340">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="462fd-340">get_TouchPressure</span></span> 

<span data-ttu-id="462fd-341">Obtén la TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-341">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="462fd-342">[get_TouchPressure](#get_touchpressure)de HRESULT público (UINT32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="462fd-342">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="462fd-343">Esto corresponde a la propiedad de presión de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-343">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-344">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="462fd-344">put_ButtonChangeKind</span></span> 

<span data-ttu-id="462fd-345">Establezca el ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-345">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="462fd-346">[put_ButtonChangeKind](#put_buttonchangekind)de HRESULT público (INT32 ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="462fd-346">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="462fd-347">Esto corresponde a la propiedad ButtonChangeKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="462fd-347">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="462fd-348">Los valores están definidos por la enumeración POINTER_BUTTON_CHANGE_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-348">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-349">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="462fd-349">put_DisplayRect</span></span> 

<span data-ttu-id="462fd-350">Establezca la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-350">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="462fd-351">[put_DisplayRect](#put_displayrect)de HRESULT público (Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="462fd-351">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="462fd-352">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="462fd-352">put_FrameId</span></span> 

<span data-ttu-id="462fd-353">Establezca el FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-353">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="462fd-354">[put_FrameId](#put_frameid)de HRESULT público (UINT32 FrameId)</span><span class="sxs-lookup"><span data-stu-id="462fd-354">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="462fd-355">Esto corresponde a la propiedad frameId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-355">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-356">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="462fd-356">put_HimetricLocation</span></span> 

<span data-ttu-id="462fd-357">Establezca el HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-357">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="462fd-358">[put_HimetricLocation](#put_himetriclocation)de HRESULT público (Point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="462fd-358">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="462fd-359">Esto corresponde a la propiedad ptHimetricLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-359">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-360">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="462fd-360">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="462fd-361">Establezca el HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-361">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="462fd-362">[put_HimetricLocationRaw](#put_himetriclocationraw)de HRESULT público (Point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="462fd-362">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="462fd-363">Esto corresponde a la propiedad ptHimetricLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-363">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-364">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="462fd-364">put_HistoryCount</span></span> 

<span data-ttu-id="462fd-365">Establezca el HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-365">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="462fd-366">[put_HistoryCount](#put_historycount)de HRESULT público (UINT32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="462fd-366">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="462fd-367">Esto corresponde a la propiedad historyCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-367">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-368">put_InputData</span><span class="sxs-lookup"><span data-stu-id="462fd-368">put_InputData</span></span> 

<span data-ttu-id="462fd-369">Establezca el InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-369">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="462fd-370">[put_InputData](#put_inputdata)de HRESULT público (INT32 InputData)</span><span class="sxs-lookup"><span data-stu-id="462fd-370">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="462fd-371">Esto corresponde a la propiedad InputData de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-371">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-372">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="462fd-372">put_KeyStates</span></span> 

<span data-ttu-id="462fd-373">Establezca el KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-373">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="462fd-374">[put_KeyStates](#put_keystates)de HRESULT público (DWORD KeyStates)</span><span class="sxs-lookup"><span data-stu-id="462fd-374">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="462fd-375">Esto corresponde a la propiedad dwKeyStates de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-375">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-376">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="462fd-376">put_PenFlags</span></span> 

<span data-ttu-id="462fd-377">Establezca el PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-377">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="462fd-378">[put_PenFlags](#put_penflags)de HRESULT público (UINT32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="462fd-378">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="462fd-379">Esto corresponde a la propiedad penFlags de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="462fd-379">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="462fd-380">Los valores están definidos por las constantes de PEN_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-380">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-381">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="462fd-381">put_PenMask</span></span> 

<span data-ttu-id="462fd-382">Establezca el PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-382">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="462fd-383">[put_PenMask](#put_penmask)de HRESULT público (UINT32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="462fd-383">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="462fd-384">Esto corresponde a la propiedad penMask de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="462fd-384">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="462fd-385">Los valores están definidos por las constantes de PEN_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-385">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-386">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="462fd-386">put_PenPressure</span></span> 

<span data-ttu-id="462fd-387">Establezca el PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-387">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="462fd-388">[put_PenPressure](#put_penpressure)de HRESULT público (UINT32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="462fd-388">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="462fd-389">Esto corresponde a la propiedad de presión de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-389">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-390">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="462fd-390">put_PenRotation</span></span> 

<span data-ttu-id="462fd-391">Establezca el PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-391">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="462fd-392">[put_PenRotation](#put_penrotation)de HRESULT público (UINT32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="462fd-392">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="462fd-393">Esto corresponde a la propiedad Rotation de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-393">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-394">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="462fd-394">put_PenTiltX</span></span> 

<span data-ttu-id="462fd-395">Establezca el PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-395">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="462fd-396">[put_PenTiltX](#put_pentiltx)de HRESULT público (INT32 PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="462fd-396">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="462fd-397">Esto corresponde a la propiedad tiltX de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-397">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-398">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="462fd-398">put_PenTiltY</span></span> 

<span data-ttu-id="462fd-399">Establezca el PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-399">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="462fd-400">[put_PenTiltY](#put_pentilty)de HRESULT público (INT32 PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="462fd-400">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="462fd-401">Esto corresponde a la propiedad Tilt de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-401">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-402">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="462fd-402">put_PerformanceCount</span></span> 

<span data-ttu-id="462fd-403">Establezca el PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-403">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="462fd-404">[put_PerformanceCount](#put_performancecount)(HRESULT) público (UINT64 PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="462fd-404">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="462fd-405">Esto corresponde a la propiedad PerformanceCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-405">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-406">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="462fd-406">put_PixelLocation</span></span> 

<span data-ttu-id="462fd-407">Establezca el PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-407">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="462fd-408">[put_PixelLocation](#put_pixellocation)de HRESULT público (Point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="462fd-408">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="462fd-409">Esto corresponde a la propiedad ptPixelLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-409">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-410">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="462fd-410">put_PixelLocationRaw</span></span> 

<span data-ttu-id="462fd-411">Establezca el PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-411">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="462fd-412">[put_PixelLocationRaw](#put_pixellocationraw)de HRESULT público (Point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="462fd-412">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="462fd-413">Esto corresponde a la propiedad ptPixelLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-413">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-414">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="462fd-414">put_PointerDeviceRect</span></span> 

<span data-ttu-id="462fd-415">Establezca la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-415">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="462fd-416">[put_PointerDeviceRect](#put_pointerdevicerect)de HRESULT público (Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="462fd-416">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="462fd-417">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="462fd-417">put_PointerFlags</span></span> 

<span data-ttu-id="462fd-418">Establezca el PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-418">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="462fd-419">[put_PointerFlags](#put_pointerflags)de HRESULT público (UINT32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="462fd-419">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="462fd-420">Esto corresponde a la propiedad pointerFlags de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="462fd-420">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="462fd-421">Los valores están definidos por las constantes de POINTER_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-421">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-422">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="462fd-422">put_PointerId</span></span> 

<span data-ttu-id="462fd-423">Establezca el PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-423">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="462fd-424">[put_PointerId](#put_pointerid)de HRESULT público (UINT32 PointerId)</span><span class="sxs-lookup"><span data-stu-id="462fd-424">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="462fd-425">Esto corresponde a la propiedad pointerId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-425">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-426">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="462fd-426">put_PointerKind</span></span> 

<span data-ttu-id="462fd-427">Establezca el PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-427">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="462fd-428">[put_PointerKind](#put_pointerkind)de HRESULT público (DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="462fd-428">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="462fd-429">Esto corresponde a la propiedad pointerKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="462fd-429">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="462fd-430">Los valores están definidos por la enumeración POINTER_INPUT_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-430">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="462fd-431">Es compatible con PT_PEN y PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="462fd-431">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="462fd-432">put_Time</span><span class="sxs-lookup"><span data-stu-id="462fd-432">put_Time</span></span> 

<span data-ttu-id="462fd-433">Establezca la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-433">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="462fd-434">[put_Time](#put_time)de HRESULT público (hora de DWORD)</span><span class="sxs-lookup"><span data-stu-id="462fd-434">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="462fd-435">Esto corresponde a la propiedad dwTime de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-435">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-436">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="462fd-436">put_TouchContact</span></span> 

<span data-ttu-id="462fd-437">Establezca el TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-437">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="462fd-438">[put_TouchContact](#put_touchcontact)de HRESULT público (Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="462fd-438">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="462fd-439">Esto corresponde a la propiedad rcContact de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-439">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-440">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="462fd-440">put_TouchContactRaw</span></span> 

<span data-ttu-id="462fd-441">Establezca el TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-441">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="462fd-442">[put_TouchContactRaw](#put_touchcontactraw)de HRESULT público (Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="462fd-442">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="462fd-443">Esto corresponde a la propiedad rcContactRaw de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-443">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-444">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="462fd-444">put_TouchFlags</span></span> 

<span data-ttu-id="462fd-445">Establezca el TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-445">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="462fd-446">[put_TouchFlags](#put_touchflags)de HRESULT público (UINT32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="462fd-446">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="462fd-447">Esto corresponde a la propiedad touchFlags de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="462fd-447">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="462fd-448">Los valores están definidos por las constantes de TOUCH_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-448">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-449">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="462fd-449">put_TouchMask</span></span> 

<span data-ttu-id="462fd-450">Establezca el TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-450">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="462fd-451">[put_TouchMask](#put_touchmask)de HRESULT público (UINT32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="462fd-451">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="462fd-452">Esto corresponde a la propiedad touchMask de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="462fd-452">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="462fd-453">Los valores están definidos por las constantes de TOUCH_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-453">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-454">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="462fd-454">put_TouchOrientation</span></span> 

<span data-ttu-id="462fd-455">Establezca el TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-455">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="462fd-456">[put_TouchOrientation](#put_touchorientation)de HRESULT público (UINT32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="462fd-456">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="462fd-457">Esto corresponde a la propiedad Orientation de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-457">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="462fd-458">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="462fd-458">put_TouchPressure</span></span> 

<span data-ttu-id="462fd-459">Establezca el TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="462fd-459">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="462fd-460">[put_TouchPressure](#put_touchpressure)de HRESULT público (UINT32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="462fd-460">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="462fd-461">Esto corresponde a la propiedad de presión de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="462fd-461">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>


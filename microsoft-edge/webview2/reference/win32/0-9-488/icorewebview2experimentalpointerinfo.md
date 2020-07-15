---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalPointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 887dcd438a89dcff4da239872df4bdb51e90f1f0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880615"
---
# <span data-ttu-id="ee92b-104">0.9.515: ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="ee92b-104">0.9.515 - interface ICoreWebView2ExperimentalPointerInfo</span></span> 

> [!NOTE]
> <span data-ttu-id="ee92b-105">Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.488.</span><span class="sxs-lookup"><span data-stu-id="ee92b-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="ee92b-106">Esto representa principalmente un objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ee92b-106">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="ee92b-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="ee92b-107">Summary</span></span>

 <span data-ttu-id="ee92b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ee92b-108">Members</span></span>                        | <span data-ttu-id="ee92b-109">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ee92b-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ee92b-110">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="ee92b-110">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="ee92b-111">Obtén la ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-111">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="ee92b-112">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="ee92b-112">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="ee92b-113">Obtén la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-113">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="ee92b-114">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="ee92b-114">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="ee92b-115">Obtén la FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-115">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="ee92b-116">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="ee92b-116">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="ee92b-117">Obtén la HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-117">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="ee92b-118">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ee92b-118">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="ee92b-119">Obtén la HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-119">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="ee92b-120">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="ee92b-120">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="ee92b-121">Obtén la HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-121">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="ee92b-122">get_InputData</span><span class="sxs-lookup"><span data-stu-id="ee92b-122">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="ee92b-123">Obtén la InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-123">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="ee92b-124">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="ee92b-124">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="ee92b-125">Obtén la KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-125">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="ee92b-126">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="ee92b-126">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="ee92b-127">Obtén la PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-127">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="ee92b-128">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="ee92b-128">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="ee92b-129">Obtén la PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-129">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="ee92b-130">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="ee92b-130">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="ee92b-131">Obtén la PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-131">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="ee92b-132">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="ee92b-132">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="ee92b-133">Obtén la PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-133">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="ee92b-134">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="ee92b-134">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="ee92b-135">Obtén la PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-135">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="ee92b-136">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="ee92b-136">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="ee92b-137">Obtén la PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-137">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="ee92b-138">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="ee92b-138">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="ee92b-139">Obtén la PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-139">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="ee92b-140">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="ee92b-140">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="ee92b-141">Obtén la PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-141">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="ee92b-142">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ee92b-142">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="ee92b-143">Obtén la PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-143">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="ee92b-144">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="ee92b-144">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="ee92b-145">Obtén la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-145">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="ee92b-146">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="ee92b-146">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="ee92b-147">Obtén la PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-147">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="ee92b-148">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="ee92b-148">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="ee92b-149">Obtén la PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-149">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="ee92b-150">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="ee92b-150">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="ee92b-151">Obtén la PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-151">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="ee92b-152">get_Time</span><span class="sxs-lookup"><span data-stu-id="ee92b-152">get_Time</span></span>](#get_time) | <span data-ttu-id="ee92b-153">Obtener la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-153">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="ee92b-154">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="ee92b-154">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="ee92b-155">Obtén la TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-155">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="ee92b-156">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="ee92b-156">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="ee92b-157">Obtén la TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-157">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="ee92b-158">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="ee92b-158">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="ee92b-159">Obtén la TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-159">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="ee92b-160">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="ee92b-160">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="ee92b-161">Obtén la TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-161">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="ee92b-162">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="ee92b-162">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="ee92b-163">Obtén la TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-163">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="ee92b-164">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="ee92b-164">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="ee92b-165">Obtén la TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-165">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="ee92b-166">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="ee92b-166">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="ee92b-167">Establezca el ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-167">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="ee92b-168">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="ee92b-168">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="ee92b-169">Establezca la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-169">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="ee92b-170">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="ee92b-170">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="ee92b-171">Establezca el FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-171">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="ee92b-172">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="ee92b-172">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="ee92b-173">Establezca el HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-173">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="ee92b-174">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ee92b-174">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="ee92b-175">Establezca el HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-175">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="ee92b-176">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="ee92b-176">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="ee92b-177">Establezca el HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-177">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="ee92b-178">put_InputData</span><span class="sxs-lookup"><span data-stu-id="ee92b-178">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="ee92b-179">Establezca el InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-179">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="ee92b-180">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="ee92b-180">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="ee92b-181">Establezca el KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-181">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="ee92b-182">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="ee92b-182">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="ee92b-183">Establezca el PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-183">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="ee92b-184">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="ee92b-184">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="ee92b-185">Establezca el PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-185">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="ee92b-186">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="ee92b-186">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="ee92b-187">Establezca el PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-187">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="ee92b-188">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="ee92b-188">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="ee92b-189">Establezca el PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-189">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="ee92b-190">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="ee92b-190">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="ee92b-191">Establezca el PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-191">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="ee92b-192">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="ee92b-192">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="ee92b-193">Establezca el PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-193">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="ee92b-194">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="ee92b-194">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="ee92b-195">Establezca el PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-195">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="ee92b-196">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="ee92b-196">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="ee92b-197">Establezca el PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-197">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="ee92b-198">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ee92b-198">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="ee92b-199">Establezca el PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-199">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="ee92b-200">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="ee92b-200">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="ee92b-201">Establezca la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-201">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="ee92b-202">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="ee92b-202">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="ee92b-203">Establezca el PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-203">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="ee92b-204">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="ee92b-204">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="ee92b-205">Establezca el PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-205">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="ee92b-206">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="ee92b-206">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="ee92b-207">Establezca el PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-207">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="ee92b-208">put_Time</span><span class="sxs-lookup"><span data-stu-id="ee92b-208">put_Time</span></span>](#put_time) | <span data-ttu-id="ee92b-209">Establezca la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-209">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="ee92b-210">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="ee92b-210">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="ee92b-211">Establezca el TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-211">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="ee92b-212">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="ee92b-212">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="ee92b-213">Establezca el TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-213">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="ee92b-214">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="ee92b-214">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="ee92b-215">Establezca el TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-215">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="ee92b-216">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="ee92b-216">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="ee92b-217">Establezca el TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-217">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="ee92b-218">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="ee92b-218">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="ee92b-219">Establezca el TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-219">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="ee92b-220">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="ee92b-220">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="ee92b-221">Establezca el TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-221">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="ee92b-222">Toma campos de los tres y excluye algunos tipos de datos específicos de Win32, como HWND y HANDLE.</span><span class="sxs-lookup"><span data-stu-id="ee92b-222">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="ee92b-223">Ten en cuenta que sourceDevice se extrae, pero esperamos que PointerDeviceRect y DisplayRect cubran los casos de uso existentes de sourceDevice.</span><span class="sxs-lookup"><span data-stu-id="ee92b-223">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="ee92b-224">Otra diferencia importante es que se espera que cualquiera de las ubicaciones de Point o Rect estén en coordenadas físicas de WebView.</span><span class="sxs-lookup"><span data-stu-id="ee92b-224">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="ee92b-225">Es decir, se aplican a las coordenadas relativas a la vista de WebView y sin ajuste de PPP.</span><span class="sxs-lookup"><span data-stu-id="ee92b-225">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="ee92b-226">Miembros</span><span class="sxs-lookup"><span data-stu-id="ee92b-226">Members</span></span>

#### <span data-ttu-id="ee92b-227">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="ee92b-227">get_ButtonChangeKind</span></span> 

<span data-ttu-id="ee92b-228">Obtén la ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-228">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="ee92b-229">[get_ButtonChangeKind](#get_buttonchangekind)de HRESULT público (INT32 \* ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="ee92b-229">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="ee92b-230">Esto corresponde a la propiedad ButtonChangeKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ee92b-230">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ee92b-231">Los valores están definidos por la enumeración POINTER_BUTTON_CHANGE_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-231">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-232">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="ee92b-232">get_DisplayRect</span></span> 

<span data-ttu-id="ee92b-233">Obtén la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-233">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="ee92b-234">[get_DisplayRect](#get_displayrect)de HRESULT público (Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="ee92b-234">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="ee92b-235">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="ee92b-235">get_FrameId</span></span> 

<span data-ttu-id="ee92b-236">Obtén la FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-236">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="ee92b-237">[get_FrameId](#get_frameid)de HRESULT público (UINT32 \* FrameId)</span><span class="sxs-lookup"><span data-stu-id="ee92b-237">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="ee92b-238">Esto corresponde a la propiedad frameId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-238">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-239">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="ee92b-239">get_HimetricLocation</span></span> 

<span data-ttu-id="ee92b-240">Obtén la HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-240">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="ee92b-241">[get_HimetricLocation](#get_himetriclocation)de HRESULT público (Point \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="ee92b-241">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="ee92b-242">Esto corresponde a la propiedad ptHimetricLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-242">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-243">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ee92b-243">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="ee92b-244">Obtén la HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-244">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="ee92b-245">[get_HimetricLocationRaw](#get_himetriclocationraw)de HRESULT público (Point \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="ee92b-245">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="ee92b-246">Esto corresponde a la propiedad ptHimetricLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-246">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-247">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="ee92b-247">get_HistoryCount</span></span> 

<span data-ttu-id="ee92b-248">Obtén la HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-248">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="ee92b-249">[get_HistoryCount](#get_historycount)de HRESULT público (UINT32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="ee92b-249">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="ee92b-250">Esto corresponde a la propiedad historyCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-250">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-251">get_InputData</span><span class="sxs-lookup"><span data-stu-id="ee92b-251">get_InputData</span></span> 

<span data-ttu-id="ee92b-252">Obtén la InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-252">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="ee92b-253">[get_InputData](#get_inputdata)de HRESULT público (INT32 \* InputData)</span><span class="sxs-lookup"><span data-stu-id="ee92b-253">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="ee92b-254">Esto corresponde a la propiedad InputData de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-254">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-255">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="ee92b-255">get_KeyStates</span></span> 

<span data-ttu-id="ee92b-256">Obtén la KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-256">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="ee92b-257">[get_KeyStates](#get_keystates)de HRESULT público (DWORD \* KeyStates)</span><span class="sxs-lookup"><span data-stu-id="ee92b-257">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="ee92b-258">Esto corresponde a la propiedad dwKeyStates de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-258">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-259">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="ee92b-259">get_PenFlags</span></span> 

<span data-ttu-id="ee92b-260">Obtén la PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-260">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="ee92b-261">[get_PenFlags](#get_penflags)de HRESULT público (UINT32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="ee92b-261">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="ee92b-262">Esto corresponde a la propiedad penFlags de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ee92b-262">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="ee92b-263">Los valores están definidos por las constantes de PEN_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-263">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-264">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="ee92b-264">get_PenMask</span></span> 

<span data-ttu-id="ee92b-265">Obtén la PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-265">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="ee92b-266">[get_PenMask](#get_penmask)de HRESULT público (UINT32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="ee92b-266">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="ee92b-267">Esto corresponde a la propiedad penMask de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ee92b-267">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="ee92b-268">Los valores están definidos por las constantes de PEN_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-268">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-269">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="ee92b-269">get_PenPressure</span></span> 

<span data-ttu-id="ee92b-270">Obtén la PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-270">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="ee92b-271">[get_PenPressure](#get_penpressure)de HRESULT público (UINT32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="ee92b-271">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="ee92b-272">Esto corresponde a la propiedad de presión de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-272">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-273">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="ee92b-273">get_PenRotation</span></span> 

<span data-ttu-id="ee92b-274">Obtén la PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-274">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="ee92b-275">[get_PenRotation](#get_penrotation)de HRESULT público (UINT32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="ee92b-275">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="ee92b-276">Esto corresponde a la propiedad Rotation de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-276">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-277">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="ee92b-277">get_PenTiltX</span></span> 

<span data-ttu-id="ee92b-278">Obtén la PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-278">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="ee92b-279">[get_PenTiltX](#get_pentiltx)de HRESULT público (INT32 \* PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="ee92b-279">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="ee92b-280">Esto corresponde a la propiedad tiltX de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-280">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-281">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="ee92b-281">get_PenTiltY</span></span> 

<span data-ttu-id="ee92b-282">Obtén la PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-282">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="ee92b-283">[get_PenTiltY](#get_pentilty)de HRESULT público (INT32 \* PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="ee92b-283">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="ee92b-284">Esto corresponde a la propiedad Tilt de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-284">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-285">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="ee92b-285">get_PerformanceCount</span></span> 

<span data-ttu-id="ee92b-286">Obtén la PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-286">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="ee92b-287">[get_PerformanceCount](#get_performancecount)(HRESULT) público (UINT64 \* PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="ee92b-287">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="ee92b-288">Esto corresponde a la propiedad PerformanceCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-288">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-289">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="ee92b-289">get_PixelLocation</span></span> 

<span data-ttu-id="ee92b-290">Obtén la PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-290">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="ee92b-291">[get_PixelLocation](#get_pixellocation)de HRESULT público (Point \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="ee92b-291">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="ee92b-292">Esto corresponde a la propiedad ptPixelLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-292">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-293">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ee92b-293">get_PixelLocationRaw</span></span> 

<span data-ttu-id="ee92b-294">Obtén la PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-294">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="ee92b-295">[get_PixelLocationRaw](#get_pixellocationraw)de HRESULT público (Point \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="ee92b-295">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="ee92b-296">Esto corresponde a la propiedad ptPixelLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-296">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-297">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="ee92b-297">get_PointerDeviceRect</span></span> 

<span data-ttu-id="ee92b-298">Obtén la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-298">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="ee92b-299">[get_PointerDeviceRect](#get_pointerdevicerect)de HRESULT público (Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="ee92b-299">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="ee92b-300">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="ee92b-300">get_PointerFlags</span></span> 

<span data-ttu-id="ee92b-301">Obtén la PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-301">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="ee92b-302">[get_PointerFlags](#get_pointerflags)de HRESULT público (UINT32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="ee92b-302">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="ee92b-303">Esto corresponde a la propiedad pointerFlags de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ee92b-303">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ee92b-304">Los valores están definidos por las constantes de POINTER_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-304">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-305">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="ee92b-305">get_PointerId</span></span> 

<span data-ttu-id="ee92b-306">Obtén la PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-306">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="ee92b-307">[get_PointerId](#get_pointerid)de HRESULT público (UINT32 \* PointerId)</span><span class="sxs-lookup"><span data-stu-id="ee92b-307">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="ee92b-308">Esto corresponde a la propiedad pointerId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-308">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-309">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="ee92b-309">get_PointerKind</span></span> 

<span data-ttu-id="ee92b-310">Obtén la PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-310">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="ee92b-311">[get_PointerKind](#get_pointerkind)de HRESULT público (DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="ee92b-311">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="ee92b-312">Esto corresponde a la propiedad pointerKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ee92b-312">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ee92b-313">Los valores están definidos por la enumeración POINTER_INPUT_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-313">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="ee92b-314">Es compatible con PT_PEN y PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="ee92b-314">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="ee92b-315">get_Time</span><span class="sxs-lookup"><span data-stu-id="ee92b-315">get_Time</span></span> 

<span data-ttu-id="ee92b-316">Obtener la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-316">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="ee92b-317">[get_Time](#get_time)de HRESULT público (DWORD \* hora)</span><span class="sxs-lookup"><span data-stu-id="ee92b-317">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="ee92b-318">Esto corresponde a la propiedad dwTime de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-318">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-319">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="ee92b-319">get_TouchContact</span></span> 

<span data-ttu-id="ee92b-320">Obtén la TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-320">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="ee92b-321">[get_TouchContact](#get_touchcontact)de HRESULT público (Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="ee92b-321">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="ee92b-322">Esto corresponde a la propiedad rcContact de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-322">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-323">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="ee92b-323">get_TouchContactRaw</span></span> 

<span data-ttu-id="ee92b-324">Obtén la TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-324">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="ee92b-325">[get_TouchContactRaw](#get_touchcontactraw)de HRESULT público (Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="ee92b-325">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="ee92b-326">Esto corresponde a la propiedad rcContactRaw de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-326">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-327">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="ee92b-327">get_TouchFlags</span></span> 

<span data-ttu-id="ee92b-328">Obtén la TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-328">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="ee92b-329">[get_TouchFlags](#get_touchflags)de HRESULT público (UINT32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="ee92b-329">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="ee92b-330">Esto corresponde a la propiedad touchFlags de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="ee92b-330">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="ee92b-331">Los valores están definidos por las constantes de TOUCH_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-331">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-332">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="ee92b-332">get_TouchMask</span></span> 

<span data-ttu-id="ee92b-333">Obtén la TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-333">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="ee92b-334">[get_TouchMask](#get_touchmask)de HRESULT público (UINT32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="ee92b-334">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="ee92b-335">Esto corresponde a la propiedad touchMask de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="ee92b-335">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="ee92b-336">Los valores están definidos por las constantes de TOUCH_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-336">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-337">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="ee92b-337">get_TouchOrientation</span></span> 

<span data-ttu-id="ee92b-338">Obtén la TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-338">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="ee92b-339">[get_TouchOrientation](#get_touchorientation)de HRESULT público (UINT32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="ee92b-339">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="ee92b-340">Esto corresponde a la propiedad Orientation de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-340">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-341">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="ee92b-341">get_TouchPressure</span></span> 

<span data-ttu-id="ee92b-342">Obtén la TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-342">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="ee92b-343">[get_TouchPressure](#get_touchpressure)de HRESULT público (UINT32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="ee92b-343">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="ee92b-344">Esto corresponde a la propiedad de presión de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-344">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-345">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="ee92b-345">put_ButtonChangeKind</span></span> 

<span data-ttu-id="ee92b-346">Establezca el ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-346">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="ee92b-347">[put_ButtonChangeKind](#put_buttonchangekind)de HRESULT público (INT32 ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="ee92b-347">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="ee92b-348">Esto corresponde a la propiedad ButtonChangeKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ee92b-348">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ee92b-349">Los valores están definidos por la enumeración POINTER_BUTTON_CHANGE_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-349">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-350">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="ee92b-350">put_DisplayRect</span></span> 

<span data-ttu-id="ee92b-351">Establezca la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-351">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="ee92b-352">[put_DisplayRect](#put_displayrect)de HRESULT público (Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="ee92b-352">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="ee92b-353">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="ee92b-353">put_FrameId</span></span> 

<span data-ttu-id="ee92b-354">Establezca el FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-354">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="ee92b-355">[put_FrameId](#put_frameid)de HRESULT público (UINT32 FrameId)</span><span class="sxs-lookup"><span data-stu-id="ee92b-355">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="ee92b-356">Esto corresponde a la propiedad frameId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-356">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-357">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="ee92b-357">put_HimetricLocation</span></span> 

<span data-ttu-id="ee92b-358">Establezca el HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-358">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="ee92b-359">[put_HimetricLocation](#put_himetriclocation)de HRESULT público (Point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="ee92b-359">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="ee92b-360">Esto corresponde a la propiedad ptHimetricLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-360">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-361">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ee92b-361">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="ee92b-362">Establezca el HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-362">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="ee92b-363">[put_HimetricLocationRaw](#put_himetriclocationraw)de HRESULT público (Point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="ee92b-363">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="ee92b-364">Esto corresponde a la propiedad ptHimetricLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-364">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-365">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="ee92b-365">put_HistoryCount</span></span> 

<span data-ttu-id="ee92b-366">Establezca el HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-366">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="ee92b-367">[put_HistoryCount](#put_historycount)de HRESULT público (UINT32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="ee92b-367">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="ee92b-368">Esto corresponde a la propiedad historyCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-368">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-369">put_InputData</span><span class="sxs-lookup"><span data-stu-id="ee92b-369">put_InputData</span></span> 

<span data-ttu-id="ee92b-370">Establezca el InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-370">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="ee92b-371">[put_InputData](#put_inputdata)de HRESULT público (INT32 InputData)</span><span class="sxs-lookup"><span data-stu-id="ee92b-371">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="ee92b-372">Esto corresponde a la propiedad InputData de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-372">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-373">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="ee92b-373">put_KeyStates</span></span> 

<span data-ttu-id="ee92b-374">Establezca el KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-374">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="ee92b-375">[put_KeyStates](#put_keystates)de HRESULT público (DWORD KeyStates)</span><span class="sxs-lookup"><span data-stu-id="ee92b-375">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="ee92b-376">Esto corresponde a la propiedad dwKeyStates de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-376">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-377">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="ee92b-377">put_PenFlags</span></span> 

<span data-ttu-id="ee92b-378">Establezca el PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-378">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="ee92b-379">[put_PenFlags](#put_penflags)de HRESULT público (UINT32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="ee92b-379">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="ee92b-380">Esto corresponde a la propiedad penFlags de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ee92b-380">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="ee92b-381">Los valores están definidos por las constantes de PEN_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-381">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-382">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="ee92b-382">put_PenMask</span></span> 

<span data-ttu-id="ee92b-383">Establezca el PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-383">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="ee92b-384">[put_PenMask](#put_penmask)de HRESULT público (UINT32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="ee92b-384">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="ee92b-385">Esto corresponde a la propiedad penMask de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ee92b-385">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="ee92b-386">Los valores están definidos por las constantes de PEN_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-386">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-387">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="ee92b-387">put_PenPressure</span></span> 

<span data-ttu-id="ee92b-388">Establezca el PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-388">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="ee92b-389">[put_PenPressure](#put_penpressure)de HRESULT público (UINT32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="ee92b-389">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="ee92b-390">Esto corresponde a la propiedad de presión de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-390">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-391">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="ee92b-391">put_PenRotation</span></span> 

<span data-ttu-id="ee92b-392">Establezca el PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-392">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="ee92b-393">[put_PenRotation](#put_penrotation)de HRESULT público (UINT32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="ee92b-393">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="ee92b-394">Esto corresponde a la propiedad Rotation de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-394">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-395">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="ee92b-395">put_PenTiltX</span></span> 

<span data-ttu-id="ee92b-396">Establezca el PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-396">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="ee92b-397">[put_PenTiltX](#put_pentiltx)de HRESULT público (INT32 PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="ee92b-397">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="ee92b-398">Esto corresponde a la propiedad tiltX de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-398">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-399">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="ee92b-399">put_PenTiltY</span></span> 

<span data-ttu-id="ee92b-400">Establezca el PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-400">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="ee92b-401">[put_PenTiltY](#put_pentilty)de HRESULT público (INT32 PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="ee92b-401">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="ee92b-402">Esto corresponde a la propiedad Tilt de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-402">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-403">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="ee92b-403">put_PerformanceCount</span></span> 

<span data-ttu-id="ee92b-404">Establezca el PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-404">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="ee92b-405">[put_PerformanceCount](#put_performancecount)(HRESULT) público (UINT64 PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="ee92b-405">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="ee92b-406">Esto corresponde a la propiedad PerformanceCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-406">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-407">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="ee92b-407">put_PixelLocation</span></span> 

<span data-ttu-id="ee92b-408">Establezca el PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-408">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="ee92b-409">[put_PixelLocation](#put_pixellocation)de HRESULT público (Point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="ee92b-409">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="ee92b-410">Esto corresponde a la propiedad ptPixelLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-410">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-411">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ee92b-411">put_PixelLocationRaw</span></span> 

<span data-ttu-id="ee92b-412">Establezca el PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-412">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="ee92b-413">[put_PixelLocationRaw](#put_pixellocationraw)de HRESULT público (Point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="ee92b-413">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="ee92b-414">Esto corresponde a la propiedad ptPixelLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-414">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-415">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="ee92b-415">put_PointerDeviceRect</span></span> 

<span data-ttu-id="ee92b-416">Establezca la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-416">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="ee92b-417">[put_PointerDeviceRect](#put_pointerdevicerect)de HRESULT público (Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="ee92b-417">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="ee92b-418">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="ee92b-418">put_PointerFlags</span></span> 

<span data-ttu-id="ee92b-419">Establezca el PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-419">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="ee92b-420">[put_PointerFlags](#put_pointerflags)de HRESULT público (UINT32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="ee92b-420">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="ee92b-421">Esto corresponde a la propiedad pointerFlags de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ee92b-421">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ee92b-422">Los valores están definidos por las constantes de POINTER_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-422">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-423">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="ee92b-423">put_PointerId</span></span> 

<span data-ttu-id="ee92b-424">Establezca el PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-424">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="ee92b-425">[put_PointerId](#put_pointerid)de HRESULT público (UINT32 PointerId)</span><span class="sxs-lookup"><span data-stu-id="ee92b-425">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="ee92b-426">Esto corresponde a la propiedad pointerId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-426">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-427">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="ee92b-427">put_PointerKind</span></span> 

<span data-ttu-id="ee92b-428">Establezca el PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-428">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="ee92b-429">[put_PointerKind](#put_pointerkind)de HRESULT público (DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="ee92b-429">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="ee92b-430">Esto corresponde a la propiedad pointerKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ee92b-430">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ee92b-431">Los valores están definidos por la enumeración POINTER_INPUT_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-431">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="ee92b-432">Es compatible con PT_PEN y PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="ee92b-432">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="ee92b-433">put_Time</span><span class="sxs-lookup"><span data-stu-id="ee92b-433">put_Time</span></span> 

<span data-ttu-id="ee92b-434">Establezca la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-434">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="ee92b-435">[put_Time](#put_time)de HRESULT público (hora de DWORD)</span><span class="sxs-lookup"><span data-stu-id="ee92b-435">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="ee92b-436">Esto corresponde a la propiedad dwTime de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-436">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-437">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="ee92b-437">put_TouchContact</span></span> 

<span data-ttu-id="ee92b-438">Establezca el TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-438">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="ee92b-439">[put_TouchContact](#put_touchcontact)de HRESULT público (Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="ee92b-439">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="ee92b-440">Esto corresponde a la propiedad rcContact de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-440">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-441">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="ee92b-441">put_TouchContactRaw</span></span> 

<span data-ttu-id="ee92b-442">Establezca el TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-442">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="ee92b-443">[put_TouchContactRaw](#put_touchcontactraw)de HRESULT público (Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="ee92b-443">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="ee92b-444">Esto corresponde a la propiedad rcContactRaw de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-444">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-445">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="ee92b-445">put_TouchFlags</span></span> 

<span data-ttu-id="ee92b-446">Establezca el TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-446">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="ee92b-447">[put_TouchFlags](#put_touchflags)de HRESULT público (UINT32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="ee92b-447">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="ee92b-448">Esto corresponde a la propiedad touchFlags de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="ee92b-448">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="ee92b-449">Los valores están definidos por las constantes de TOUCH_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-449">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-450">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="ee92b-450">put_TouchMask</span></span> 

<span data-ttu-id="ee92b-451">Establezca el TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-451">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="ee92b-452">[put_TouchMask](#put_touchmask)de HRESULT público (UINT32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="ee92b-452">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="ee92b-453">Esto corresponde a la propiedad touchMask de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="ee92b-453">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="ee92b-454">Los valores están definidos por las constantes de TOUCH_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-454">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-455">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="ee92b-455">put_TouchOrientation</span></span> 

<span data-ttu-id="ee92b-456">Establezca el TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-456">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="ee92b-457">[put_TouchOrientation](#put_touchorientation)de HRESULT público (UINT32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="ee92b-457">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="ee92b-458">Esto corresponde a la propiedad Orientation de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-458">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ee92b-459">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="ee92b-459">put_TouchPressure</span></span> 

<span data-ttu-id="ee92b-460">Establezca el TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="ee92b-460">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="ee92b-461">[put_TouchPressure](#put_touchpressure)de HRESULT público (UINT32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="ee92b-461">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="ee92b-462">Esto corresponde a la propiedad de presión de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ee92b-462">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>


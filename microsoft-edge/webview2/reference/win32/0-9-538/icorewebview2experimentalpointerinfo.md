---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalPointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalPointerInfo
ms.openlocfilehash: b84c822e8b9e01d3b5a0e59baaeed5fc587d9a15
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879950"
---
# <span data-ttu-id="b83f2-104">interfaz ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="b83f2-104">interface ICoreWebView2ExperimentalPointerInfo</span></span> 

> [!NOTE]
> <span data-ttu-id="b83f2-105">Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="b83f2-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="b83f2-106">Esto representa principalmente un objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="b83f2-106">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="b83f2-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="b83f2-107">Summary</span></span>

 <span data-ttu-id="b83f2-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b83f2-108">Members</span></span>                        | <span data-ttu-id="b83f2-109">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b83f2-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b83f2-110">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="b83f2-110">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="b83f2-111">Obtén la ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-111">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="b83f2-112">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="b83f2-112">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="b83f2-113">Obtén la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-113">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="b83f2-114">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="b83f2-114">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="b83f2-115">Obtén la FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-115">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="b83f2-116">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="b83f2-116">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="b83f2-117">Obtén la HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-117">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="b83f2-118">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="b83f2-118">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="b83f2-119">Obtén la HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-119">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="b83f2-120">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="b83f2-120">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="b83f2-121">Obtén la HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-121">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="b83f2-122">get_InputData</span><span class="sxs-lookup"><span data-stu-id="b83f2-122">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="b83f2-123">Obtén la InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-123">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="b83f2-124">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="b83f2-124">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="b83f2-125">Obtén la KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-125">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="b83f2-126">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="b83f2-126">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="b83f2-127">Obtén la PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-127">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="b83f2-128">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="b83f2-128">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="b83f2-129">Obtén la PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-129">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="b83f2-130">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="b83f2-130">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="b83f2-131">Obtén la PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-131">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="b83f2-132">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="b83f2-132">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="b83f2-133">Obtén la PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-133">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="b83f2-134">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="b83f2-134">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="b83f2-135">Obtén la PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-135">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="b83f2-136">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="b83f2-136">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="b83f2-137">Obtén la PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-137">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="b83f2-138">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="b83f2-138">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="b83f2-139">Obtén la PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-139">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="b83f2-140">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="b83f2-140">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="b83f2-141">Obtén la PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-141">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="b83f2-142">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="b83f2-142">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="b83f2-143">Obtén la PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-143">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="b83f2-144">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="b83f2-144">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="b83f2-145">Obtén la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-145">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="b83f2-146">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="b83f2-146">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="b83f2-147">Obtén la PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-147">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="b83f2-148">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="b83f2-148">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="b83f2-149">Obtén la PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-149">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="b83f2-150">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="b83f2-150">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="b83f2-151">Obtén la PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-151">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="b83f2-152">get_Time</span><span class="sxs-lookup"><span data-stu-id="b83f2-152">get_Time</span></span>](#get_time) | <span data-ttu-id="b83f2-153">Obtener la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-153">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="b83f2-154">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="b83f2-154">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="b83f2-155">Obtén la TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-155">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="b83f2-156">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="b83f2-156">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="b83f2-157">Obtén la TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-157">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="b83f2-158">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="b83f2-158">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="b83f2-159">Obtén la TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-159">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="b83f2-160">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="b83f2-160">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="b83f2-161">Obtén la TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-161">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="b83f2-162">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="b83f2-162">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="b83f2-163">Obtén la TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-163">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="b83f2-164">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="b83f2-164">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="b83f2-165">Obtén la TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-165">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="b83f2-166">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="b83f2-166">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="b83f2-167">Establezca el ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-167">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="b83f2-168">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="b83f2-168">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="b83f2-169">Establezca la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-169">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="b83f2-170">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="b83f2-170">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="b83f2-171">Establezca el FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-171">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="b83f2-172">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="b83f2-172">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="b83f2-173">Establezca el HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-173">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="b83f2-174">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="b83f2-174">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="b83f2-175">Establezca el HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-175">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="b83f2-176">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="b83f2-176">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="b83f2-177">Establezca el HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-177">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="b83f2-178">put_InputData</span><span class="sxs-lookup"><span data-stu-id="b83f2-178">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="b83f2-179">Establezca el InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-179">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="b83f2-180">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="b83f2-180">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="b83f2-181">Establezca el KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-181">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="b83f2-182">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="b83f2-182">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="b83f2-183">Establezca el PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-183">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="b83f2-184">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="b83f2-184">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="b83f2-185">Establezca el PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-185">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="b83f2-186">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="b83f2-186">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="b83f2-187">Establezca el PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-187">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="b83f2-188">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="b83f2-188">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="b83f2-189">Establezca el PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-189">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="b83f2-190">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="b83f2-190">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="b83f2-191">Establezca el PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-191">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="b83f2-192">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="b83f2-192">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="b83f2-193">Establezca el PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-193">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="b83f2-194">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="b83f2-194">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="b83f2-195">Establezca el PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-195">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="b83f2-196">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="b83f2-196">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="b83f2-197">Establezca el PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-197">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="b83f2-198">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="b83f2-198">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="b83f2-199">Establezca el PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-199">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="b83f2-200">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="b83f2-200">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="b83f2-201">Establezca la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-201">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="b83f2-202">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="b83f2-202">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="b83f2-203">Establezca el PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-203">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="b83f2-204">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="b83f2-204">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="b83f2-205">Establezca el PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-205">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="b83f2-206">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="b83f2-206">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="b83f2-207">Establezca el PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-207">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="b83f2-208">put_Time</span><span class="sxs-lookup"><span data-stu-id="b83f2-208">put_Time</span></span>](#put_time) | <span data-ttu-id="b83f2-209">Establezca la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-209">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="b83f2-210">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="b83f2-210">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="b83f2-211">Establezca el TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-211">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="b83f2-212">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="b83f2-212">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="b83f2-213">Establezca el TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-213">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="b83f2-214">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="b83f2-214">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="b83f2-215">Establezca el TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-215">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="b83f2-216">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="b83f2-216">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="b83f2-217">Establezca el TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-217">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="b83f2-218">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="b83f2-218">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="b83f2-219">Establezca el TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-219">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="b83f2-220">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="b83f2-220">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="b83f2-221">Establezca el TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-221">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="b83f2-222">Toma campos de los tres y excluye algunos tipos de datos específicos de Win32, como HWND y HANDLE.</span><span class="sxs-lookup"><span data-stu-id="b83f2-222">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="b83f2-223">Ten en cuenta que sourceDevice se extrae, pero esperamos que PointerDeviceRect y DisplayRect cubran los casos de uso existentes de sourceDevice.</span><span class="sxs-lookup"><span data-stu-id="b83f2-223">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="b83f2-224">Otra diferencia importante es que se espera que cualquiera de las ubicaciones de Point o Rect estén en coordenadas físicas de WebView.</span><span class="sxs-lookup"><span data-stu-id="b83f2-224">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="b83f2-225">Es decir, se aplican a las coordenadas relativas a la vista de WebView y sin ajuste de PPP.</span><span class="sxs-lookup"><span data-stu-id="b83f2-225">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="b83f2-226">Miembros</span><span class="sxs-lookup"><span data-stu-id="b83f2-226">Members</span></span>

#### <span data-ttu-id="b83f2-227">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="b83f2-227">get_ButtonChangeKind</span></span> 

<span data-ttu-id="b83f2-228">Obtén la ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-228">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="b83f2-229">[get_ButtonChangeKind](#get_buttonchangekind)de HRESULT público (INT32 \* ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="b83f2-229">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="b83f2-230">Esto corresponde a la propiedad ButtonChangeKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="b83f2-230">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="b83f2-231">Los valores están definidos por la enumeración POINTER_BUTTON_CHANGE_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-231">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-232">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="b83f2-232">get_DisplayRect</span></span> 

<span data-ttu-id="b83f2-233">Obtén la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-233">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="b83f2-234">[get_DisplayRect](#get_displayrect)de HRESULT público (Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="b83f2-234">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="b83f2-235">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="b83f2-235">get_FrameId</span></span> 

<span data-ttu-id="b83f2-236">Obtén la FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-236">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="b83f2-237">[get_FrameId](#get_frameid)de HRESULT público (UINT32 \* FrameId)</span><span class="sxs-lookup"><span data-stu-id="b83f2-237">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="b83f2-238">Esto corresponde a la propiedad frameId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-238">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-239">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="b83f2-239">get_HimetricLocation</span></span> 

<span data-ttu-id="b83f2-240">Obtén la HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-240">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="b83f2-241">[get_HimetricLocation](#get_himetriclocation)de HRESULT público (Point \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="b83f2-241">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="b83f2-242">Esto corresponde a la propiedad ptHimetricLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-242">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-243">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="b83f2-243">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="b83f2-244">Obtén la HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-244">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="b83f2-245">[get_HimetricLocationRaw](#get_himetriclocationraw)de HRESULT público (Point \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="b83f2-245">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="b83f2-246">Esto corresponde a la propiedad ptHimetricLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-246">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-247">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="b83f2-247">get_HistoryCount</span></span> 

<span data-ttu-id="b83f2-248">Obtén la HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-248">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="b83f2-249">[get_HistoryCount](#get_historycount)de HRESULT público (UINT32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="b83f2-249">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="b83f2-250">Esto corresponde a la propiedad historyCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-250">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-251">get_InputData</span><span class="sxs-lookup"><span data-stu-id="b83f2-251">get_InputData</span></span> 

<span data-ttu-id="b83f2-252">Obtén la InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-252">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="b83f2-253">[get_InputData](#get_inputdata)de HRESULT público (INT32 \* InputData)</span><span class="sxs-lookup"><span data-stu-id="b83f2-253">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="b83f2-254">Esto corresponde a la propiedad InputData de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-254">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-255">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="b83f2-255">get_KeyStates</span></span> 

<span data-ttu-id="b83f2-256">Obtén la KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-256">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="b83f2-257">[get_KeyStates](#get_keystates)de HRESULT público (DWORD \* KeyStates)</span><span class="sxs-lookup"><span data-stu-id="b83f2-257">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="b83f2-258">Esto corresponde a la propiedad dwKeyStates de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-258">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-259">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="b83f2-259">get_PenFlags</span></span> 

<span data-ttu-id="b83f2-260">Obtén la PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-260">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="b83f2-261">[get_PenFlags](#get_penflags)de HRESULT público (UINT32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="b83f2-261">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="b83f2-262">Esto corresponde a la propiedad penFlags de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="b83f2-262">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="b83f2-263">Los valores están definidos por las constantes de PEN_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-263">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-264">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="b83f2-264">get_PenMask</span></span> 

<span data-ttu-id="b83f2-265">Obtén la PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-265">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="b83f2-266">[get_PenMask](#get_penmask)de HRESULT público (UINT32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="b83f2-266">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="b83f2-267">Esto corresponde a la propiedad penMask de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="b83f2-267">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="b83f2-268">Los valores están definidos por las constantes de PEN_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-268">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-269">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="b83f2-269">get_PenPressure</span></span> 

<span data-ttu-id="b83f2-270">Obtén la PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-270">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="b83f2-271">[get_PenPressure](#get_penpressure)de HRESULT público (UINT32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="b83f2-271">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="b83f2-272">Esto corresponde a la propiedad de presión de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-272">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-273">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="b83f2-273">get_PenRotation</span></span> 

<span data-ttu-id="b83f2-274">Obtén la PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-274">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="b83f2-275">[get_PenRotation](#get_penrotation)de HRESULT público (UINT32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="b83f2-275">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="b83f2-276">Esto corresponde a la propiedad Rotation de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-276">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-277">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="b83f2-277">get_PenTiltX</span></span> 

<span data-ttu-id="b83f2-278">Obtén la PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-278">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="b83f2-279">[get_PenTiltX](#get_pentiltx)de HRESULT público (INT32 \* PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="b83f2-279">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="b83f2-280">Esto corresponde a la propiedad tiltX de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-280">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-281">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="b83f2-281">get_PenTiltY</span></span> 

<span data-ttu-id="b83f2-282">Obtén la PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-282">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="b83f2-283">[get_PenTiltY](#get_pentilty)de HRESULT público (INT32 \* PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="b83f2-283">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="b83f2-284">Esto corresponde a la propiedad Tilt de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-284">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-285">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="b83f2-285">get_PerformanceCount</span></span> 

<span data-ttu-id="b83f2-286">Obtén la PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-286">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="b83f2-287">[get_PerformanceCount](#get_performancecount)(HRESULT) público (UINT64 \* PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="b83f2-287">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="b83f2-288">Esto corresponde a la propiedad PerformanceCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-288">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-289">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="b83f2-289">get_PixelLocation</span></span> 

<span data-ttu-id="b83f2-290">Obtén la PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-290">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="b83f2-291">[get_PixelLocation](#get_pixellocation)de HRESULT público (Point \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="b83f2-291">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="b83f2-292">Esto corresponde a la propiedad ptPixelLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-292">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-293">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="b83f2-293">get_PixelLocationRaw</span></span> 

<span data-ttu-id="b83f2-294">Obtén la PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-294">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="b83f2-295">[get_PixelLocationRaw](#get_pixellocationraw)de HRESULT público (Point \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="b83f2-295">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="b83f2-296">Esto corresponde a la propiedad ptPixelLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-296">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-297">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="b83f2-297">get_PointerDeviceRect</span></span> 

<span data-ttu-id="b83f2-298">Obtén la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-298">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="b83f2-299">[get_PointerDeviceRect](#get_pointerdevicerect)de HRESULT público (Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="b83f2-299">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="b83f2-300">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="b83f2-300">get_PointerFlags</span></span> 

<span data-ttu-id="b83f2-301">Obtén la PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-301">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="b83f2-302">[get_PointerFlags](#get_pointerflags)de HRESULT público (UINT32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="b83f2-302">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="b83f2-303">Esto corresponde a la propiedad pointerFlags de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="b83f2-303">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="b83f2-304">Los valores están definidos por las constantes de POINTER_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-304">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-305">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="b83f2-305">get_PointerId</span></span> 

<span data-ttu-id="b83f2-306">Obtén la PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-306">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="b83f2-307">[get_PointerId](#get_pointerid)de HRESULT público (UINT32 \* PointerId)</span><span class="sxs-lookup"><span data-stu-id="b83f2-307">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="b83f2-308">Esto corresponde a la propiedad pointerId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-308">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-309">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="b83f2-309">get_PointerKind</span></span> 

<span data-ttu-id="b83f2-310">Obtén la PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-310">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="b83f2-311">[get_PointerKind](#get_pointerkind)de HRESULT público (DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="b83f2-311">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="b83f2-312">Esto corresponde a la propiedad pointerKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="b83f2-312">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="b83f2-313">Los valores están definidos por la enumeración POINTER_INPUT_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-313">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="b83f2-314">Es compatible con PT_PEN y PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="b83f2-314">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="b83f2-315">get_Time</span><span class="sxs-lookup"><span data-stu-id="b83f2-315">get_Time</span></span> 

<span data-ttu-id="b83f2-316">Obtener la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-316">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="b83f2-317">[get_Time](#get_time)de HRESULT público (DWORD \* hora)</span><span class="sxs-lookup"><span data-stu-id="b83f2-317">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="b83f2-318">Esto corresponde a la propiedad dwTime de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-318">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-319">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="b83f2-319">get_TouchContact</span></span> 

<span data-ttu-id="b83f2-320">Obtén la TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-320">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="b83f2-321">[get_TouchContact](#get_touchcontact)de HRESULT público (Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="b83f2-321">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="b83f2-322">Esto corresponde a la propiedad rcContact de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-322">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-323">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="b83f2-323">get_TouchContactRaw</span></span> 

<span data-ttu-id="b83f2-324">Obtén la TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-324">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="b83f2-325">[get_TouchContactRaw](#get_touchcontactraw)de HRESULT público (Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="b83f2-325">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="b83f2-326">Esto corresponde a la propiedad rcContactRaw de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-326">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-327">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="b83f2-327">get_TouchFlags</span></span> 

<span data-ttu-id="b83f2-328">Obtén la TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-328">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="b83f2-329">[get_TouchFlags](#get_touchflags)de HRESULT público (UINT32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="b83f2-329">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="b83f2-330">Esto corresponde a la propiedad touchFlags de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="b83f2-330">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="b83f2-331">Los valores están definidos por las constantes de TOUCH_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-331">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-332">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="b83f2-332">get_TouchMask</span></span> 

<span data-ttu-id="b83f2-333">Obtén la TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-333">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="b83f2-334">[get_TouchMask](#get_touchmask)de HRESULT público (UINT32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="b83f2-334">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="b83f2-335">Esto corresponde a la propiedad touchMask de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="b83f2-335">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="b83f2-336">Los valores están definidos por las constantes de TOUCH_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-336">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-337">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="b83f2-337">get_TouchOrientation</span></span> 

<span data-ttu-id="b83f2-338">Obtén la TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-338">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="b83f2-339">[get_TouchOrientation](#get_touchorientation)de HRESULT público (UINT32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="b83f2-339">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="b83f2-340">Esto corresponde a la propiedad Orientation de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-340">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-341">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="b83f2-341">get_TouchPressure</span></span> 

<span data-ttu-id="b83f2-342">Obtén la TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-342">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="b83f2-343">[get_TouchPressure](#get_touchpressure)de HRESULT público (UINT32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="b83f2-343">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="b83f2-344">Esto corresponde a la propiedad de presión de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-344">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-345">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="b83f2-345">put_ButtonChangeKind</span></span> 

<span data-ttu-id="b83f2-346">Establezca el ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-346">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="b83f2-347">[put_ButtonChangeKind](#put_buttonchangekind)de HRESULT público (INT32 ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="b83f2-347">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="b83f2-348">Esto corresponde a la propiedad ButtonChangeKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="b83f2-348">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="b83f2-349">Los valores están definidos por la enumeración POINTER_BUTTON_CHANGE_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-349">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-350">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="b83f2-350">put_DisplayRect</span></span> 

<span data-ttu-id="b83f2-351">Establezca la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-351">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="b83f2-352">[put_DisplayRect](#put_displayrect)de HRESULT público (Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="b83f2-352">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="b83f2-353">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="b83f2-353">put_FrameId</span></span> 

<span data-ttu-id="b83f2-354">Establezca el FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-354">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="b83f2-355">[put_FrameId](#put_frameid)de HRESULT público (UINT32 FrameId)</span><span class="sxs-lookup"><span data-stu-id="b83f2-355">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="b83f2-356">Esto corresponde a la propiedad frameId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-356">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-357">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="b83f2-357">put_HimetricLocation</span></span> 

<span data-ttu-id="b83f2-358">Establezca el HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-358">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="b83f2-359">[put_HimetricLocation](#put_himetriclocation)de HRESULT público (Point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="b83f2-359">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="b83f2-360">Esto corresponde a la propiedad ptHimetricLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-360">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-361">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="b83f2-361">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="b83f2-362">Establezca el HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-362">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="b83f2-363">[put_HimetricLocationRaw](#put_himetriclocationraw)de HRESULT público (Point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="b83f2-363">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="b83f2-364">Esto corresponde a la propiedad ptHimetricLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-364">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-365">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="b83f2-365">put_HistoryCount</span></span> 

<span data-ttu-id="b83f2-366">Establezca el HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-366">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="b83f2-367">[put_HistoryCount](#put_historycount)de HRESULT público (UINT32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="b83f2-367">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="b83f2-368">Esto corresponde a la propiedad historyCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-368">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-369">put_InputData</span><span class="sxs-lookup"><span data-stu-id="b83f2-369">put_InputData</span></span> 

<span data-ttu-id="b83f2-370">Establezca el InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-370">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="b83f2-371">[put_InputData](#put_inputdata)de HRESULT público (INT32 InputData)</span><span class="sxs-lookup"><span data-stu-id="b83f2-371">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="b83f2-372">Esto corresponde a la propiedad InputData de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-372">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-373">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="b83f2-373">put_KeyStates</span></span> 

<span data-ttu-id="b83f2-374">Establezca el KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-374">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="b83f2-375">[put_KeyStates](#put_keystates)de HRESULT público (DWORD KeyStates)</span><span class="sxs-lookup"><span data-stu-id="b83f2-375">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="b83f2-376">Esto corresponde a la propiedad dwKeyStates de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-376">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-377">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="b83f2-377">put_PenFlags</span></span> 

<span data-ttu-id="b83f2-378">Establezca el PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-378">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="b83f2-379">[put_PenFlags](#put_penflags)de HRESULT público (UINT32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="b83f2-379">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="b83f2-380">Esto corresponde a la propiedad penFlags de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="b83f2-380">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="b83f2-381">Los valores están definidos por las constantes de PEN_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-381">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-382">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="b83f2-382">put_PenMask</span></span> 

<span data-ttu-id="b83f2-383">Establezca el PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-383">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="b83f2-384">[put_PenMask](#put_penmask)de HRESULT público (UINT32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="b83f2-384">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="b83f2-385">Esto corresponde a la propiedad penMask de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="b83f2-385">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="b83f2-386">Los valores están definidos por las constantes de PEN_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-386">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-387">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="b83f2-387">put_PenPressure</span></span> 

<span data-ttu-id="b83f2-388">Establezca el PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-388">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="b83f2-389">[put_PenPressure](#put_penpressure)de HRESULT público (UINT32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="b83f2-389">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="b83f2-390">Esto corresponde a la propiedad de presión de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-390">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-391">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="b83f2-391">put_PenRotation</span></span> 

<span data-ttu-id="b83f2-392">Establezca el PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-392">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="b83f2-393">[put_PenRotation](#put_penrotation)de HRESULT público (UINT32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="b83f2-393">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="b83f2-394">Esto corresponde a la propiedad Rotation de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-394">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-395">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="b83f2-395">put_PenTiltX</span></span> 

<span data-ttu-id="b83f2-396">Establezca el PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-396">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="b83f2-397">[put_PenTiltX](#put_pentiltx)de HRESULT público (INT32 PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="b83f2-397">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="b83f2-398">Esto corresponde a la propiedad tiltX de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-398">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-399">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="b83f2-399">put_PenTiltY</span></span> 

<span data-ttu-id="b83f2-400">Establezca el PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-400">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="b83f2-401">[put_PenTiltY](#put_pentilty)de HRESULT público (INT32 PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="b83f2-401">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="b83f2-402">Esto corresponde a la propiedad Tilt de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-402">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-403">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="b83f2-403">put_PerformanceCount</span></span> 

<span data-ttu-id="b83f2-404">Establezca el PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-404">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="b83f2-405">[put_PerformanceCount](#put_performancecount)(HRESULT) público (UINT64 PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="b83f2-405">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="b83f2-406">Esto corresponde a la propiedad PerformanceCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-406">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-407">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="b83f2-407">put_PixelLocation</span></span> 

<span data-ttu-id="b83f2-408">Establezca el PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-408">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="b83f2-409">[put_PixelLocation](#put_pixellocation)de HRESULT público (Point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="b83f2-409">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="b83f2-410">Esto corresponde a la propiedad ptPixelLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-410">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-411">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="b83f2-411">put_PixelLocationRaw</span></span> 

<span data-ttu-id="b83f2-412">Establezca el PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-412">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="b83f2-413">[put_PixelLocationRaw](#put_pixellocationraw)de HRESULT público (Point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="b83f2-413">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="b83f2-414">Esto corresponde a la propiedad ptPixelLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-414">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-415">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="b83f2-415">put_PointerDeviceRect</span></span> 

<span data-ttu-id="b83f2-416">Establezca la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-416">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="b83f2-417">[put_PointerDeviceRect](#put_pointerdevicerect)de HRESULT público (Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="b83f2-417">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="b83f2-418">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="b83f2-418">put_PointerFlags</span></span> 

<span data-ttu-id="b83f2-419">Establezca el PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-419">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="b83f2-420">[put_PointerFlags](#put_pointerflags)de HRESULT público (UINT32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="b83f2-420">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="b83f2-421">Esto corresponde a la propiedad pointerFlags de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="b83f2-421">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="b83f2-422">Los valores están definidos por las constantes de POINTER_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-422">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-423">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="b83f2-423">put_PointerId</span></span> 

<span data-ttu-id="b83f2-424">Establezca el PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-424">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="b83f2-425">[put_PointerId](#put_pointerid)de HRESULT público (UINT32 PointerId)</span><span class="sxs-lookup"><span data-stu-id="b83f2-425">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="b83f2-426">Esto corresponde a la propiedad pointerId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-426">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-427">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="b83f2-427">put_PointerKind</span></span> 

<span data-ttu-id="b83f2-428">Establezca el PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-428">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="b83f2-429">[put_PointerKind](#put_pointerkind)de HRESULT público (DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="b83f2-429">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="b83f2-430">Esto corresponde a la propiedad pointerKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="b83f2-430">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="b83f2-431">Los valores están definidos por la enumeración POINTER_INPUT_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-431">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="b83f2-432">Es compatible con PT_PEN y PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="b83f2-432">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="b83f2-433">put_Time</span><span class="sxs-lookup"><span data-stu-id="b83f2-433">put_Time</span></span> 

<span data-ttu-id="b83f2-434">Establezca la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-434">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="b83f2-435">[put_Time](#put_time)de HRESULT público (hora de DWORD)</span><span class="sxs-lookup"><span data-stu-id="b83f2-435">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="b83f2-436">Esto corresponde a la propiedad dwTime de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-436">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-437">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="b83f2-437">put_TouchContact</span></span> 

<span data-ttu-id="b83f2-438">Establezca el TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-438">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="b83f2-439">[put_TouchContact](#put_touchcontact)de HRESULT público (Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="b83f2-439">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="b83f2-440">Esto corresponde a la propiedad rcContact de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-440">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-441">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="b83f2-441">put_TouchContactRaw</span></span> 

<span data-ttu-id="b83f2-442">Establezca el TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-442">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="b83f2-443">[put_TouchContactRaw](#put_touchcontactraw)de HRESULT público (Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="b83f2-443">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="b83f2-444">Esto corresponde a la propiedad rcContactRaw de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-444">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-445">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="b83f2-445">put_TouchFlags</span></span> 

<span data-ttu-id="b83f2-446">Establezca el TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-446">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="b83f2-447">[put_TouchFlags](#put_touchflags)de HRESULT público (UINT32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="b83f2-447">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="b83f2-448">Esto corresponde a la propiedad touchFlags de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="b83f2-448">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="b83f2-449">Los valores están definidos por las constantes de TOUCH_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-449">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-450">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="b83f2-450">put_TouchMask</span></span> 

<span data-ttu-id="b83f2-451">Establezca el TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-451">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="b83f2-452">[put_TouchMask](#put_touchmask)de HRESULT público (UINT32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="b83f2-452">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="b83f2-453">Esto corresponde a la propiedad touchMask de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="b83f2-453">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="b83f2-454">Los valores están definidos por las constantes de TOUCH_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-454">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-455">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="b83f2-455">put_TouchOrientation</span></span> 

<span data-ttu-id="b83f2-456">Establezca el TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-456">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="b83f2-457">[put_TouchOrientation](#put_touchorientation)de HRESULT público (UINT32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="b83f2-457">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="b83f2-458">Esto corresponde a la propiedad Orientation de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-458">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="b83f2-459">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="b83f2-459">put_TouchPressure</span></span> 

<span data-ttu-id="b83f2-460">Establezca el TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="b83f2-460">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="b83f2-461">[put_TouchPressure](#put_touchpressure)de HRESULT público (UINT32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="b83f2-461">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="b83f2-462">Esto corresponde a la propiedad de presión de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="b83f2-462">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>


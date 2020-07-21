---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalPointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 8c0ed40c61344fe0a3177fd36d5629953f8801d7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885488"
---
# <span data-ttu-id="2d5db-104">0.9.515: ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="2d5db-104">0.9.515 - interface ICoreWebView2ExperimentalPointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="2d5db-105">Esto representa principalmente un objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="2d5db-105">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="2d5db-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="2d5db-106">Summary</span></span>

 <span data-ttu-id="2d5db-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2d5db-107">Members</span></span>                        | <span data-ttu-id="2d5db-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2d5db-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2d5db-109">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="2d5db-109">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="2d5db-110">Obtén la ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-110">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="2d5db-111">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="2d5db-111">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="2d5db-112">Obtén la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-112">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="2d5db-113">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="2d5db-113">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="2d5db-114">Obtén la FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-114">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="2d5db-115">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="2d5db-115">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="2d5db-116">Obtén la HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-116">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="2d5db-117">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="2d5db-117">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="2d5db-118">Obtén la HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-118">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="2d5db-119">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="2d5db-119">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="2d5db-120">Obtén la HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-120">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="2d5db-121">get_InputData</span><span class="sxs-lookup"><span data-stu-id="2d5db-121">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="2d5db-122">Obtén la InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-122">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="2d5db-123">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="2d5db-123">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="2d5db-124">Obtén la KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-124">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="2d5db-125">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="2d5db-125">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="2d5db-126">Obtén la PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-126">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="2d5db-127">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="2d5db-127">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="2d5db-128">Obtén la PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-128">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="2d5db-129">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="2d5db-129">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="2d5db-130">Obtén la PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-130">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="2d5db-131">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="2d5db-131">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="2d5db-132">Obtén la PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-132">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="2d5db-133">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="2d5db-133">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="2d5db-134">Obtén la PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-134">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="2d5db-135">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="2d5db-135">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="2d5db-136">Obtén la PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-136">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="2d5db-137">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="2d5db-137">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="2d5db-138">Obtén la PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-138">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="2d5db-139">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="2d5db-139">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="2d5db-140">Obtén la PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-140">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="2d5db-141">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="2d5db-141">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="2d5db-142">Obtén la PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-142">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="2d5db-143">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="2d5db-143">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="2d5db-144">Obtén la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-144">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="2d5db-145">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="2d5db-145">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="2d5db-146">Obtén la PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-146">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="2d5db-147">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="2d5db-147">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="2d5db-148">Obtén la PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-148">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="2d5db-149">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="2d5db-149">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="2d5db-150">Obtén la PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-150">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="2d5db-151">get_Time</span><span class="sxs-lookup"><span data-stu-id="2d5db-151">get_Time</span></span>](#get_time) | <span data-ttu-id="2d5db-152">Obtener la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-152">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="2d5db-153">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="2d5db-153">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="2d5db-154">Obtén la TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-154">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="2d5db-155">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="2d5db-155">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="2d5db-156">Obtén la TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-156">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="2d5db-157">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="2d5db-157">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="2d5db-158">Obtén la TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-158">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="2d5db-159">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="2d5db-159">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="2d5db-160">Obtén la TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-160">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="2d5db-161">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="2d5db-161">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="2d5db-162">Obtén la TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-162">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="2d5db-163">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="2d5db-163">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="2d5db-164">Obtén la TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-164">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="2d5db-165">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="2d5db-165">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="2d5db-166">Establezca el ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-166">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="2d5db-167">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="2d5db-167">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="2d5db-168">Establezca la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-168">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="2d5db-169">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="2d5db-169">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="2d5db-170">Establezca el FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-170">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="2d5db-171">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="2d5db-171">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="2d5db-172">Establezca el HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-172">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="2d5db-173">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="2d5db-173">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="2d5db-174">Establezca el HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-174">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="2d5db-175">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="2d5db-175">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="2d5db-176">Establezca el HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-176">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="2d5db-177">put_InputData</span><span class="sxs-lookup"><span data-stu-id="2d5db-177">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="2d5db-178">Establezca el InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-178">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="2d5db-179">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="2d5db-179">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="2d5db-180">Establezca el KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-180">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="2d5db-181">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="2d5db-181">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="2d5db-182">Establezca el PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-182">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="2d5db-183">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="2d5db-183">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="2d5db-184">Establezca el PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-184">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="2d5db-185">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="2d5db-185">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="2d5db-186">Establezca el PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-186">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="2d5db-187">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="2d5db-187">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="2d5db-188">Establezca el PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-188">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="2d5db-189">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="2d5db-189">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="2d5db-190">Establezca el PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-190">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="2d5db-191">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="2d5db-191">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="2d5db-192">Establezca el PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-192">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="2d5db-193">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="2d5db-193">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="2d5db-194">Establezca el PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-194">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="2d5db-195">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="2d5db-195">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="2d5db-196">Establezca el PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-196">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="2d5db-197">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="2d5db-197">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="2d5db-198">Establezca el PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-198">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="2d5db-199">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="2d5db-199">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="2d5db-200">Establezca la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-200">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="2d5db-201">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="2d5db-201">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="2d5db-202">Establezca el PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-202">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="2d5db-203">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="2d5db-203">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="2d5db-204">Establezca el PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-204">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="2d5db-205">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="2d5db-205">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="2d5db-206">Establezca el PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-206">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="2d5db-207">put_Time</span><span class="sxs-lookup"><span data-stu-id="2d5db-207">put_Time</span></span>](#put_time) | <span data-ttu-id="2d5db-208">Establezca la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-208">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="2d5db-209">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="2d5db-209">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="2d5db-210">Establezca el TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-210">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="2d5db-211">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="2d5db-211">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="2d5db-212">Establezca el TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-212">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="2d5db-213">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="2d5db-213">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="2d5db-214">Establezca el TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-214">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="2d5db-215">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="2d5db-215">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="2d5db-216">Establezca el TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-216">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="2d5db-217">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="2d5db-217">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="2d5db-218">Establezca el TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-218">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="2d5db-219">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="2d5db-219">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="2d5db-220">Establezca el TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-220">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="2d5db-221">Toma campos de los tres y excluye algunos tipos de datos específicos de Win32, como HWND y HANDLE.</span><span class="sxs-lookup"><span data-stu-id="2d5db-221">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="2d5db-222">Ten en cuenta que sourceDevice se extrae, pero esperamos que PointerDeviceRect y DisplayRect cubran los casos de uso existentes de sourceDevice.</span><span class="sxs-lookup"><span data-stu-id="2d5db-222">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="2d5db-223">Otra diferencia importante es que se espera que cualquiera de las ubicaciones de Point o Rect estén en coordenadas físicas de WebView.</span><span class="sxs-lookup"><span data-stu-id="2d5db-223">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="2d5db-224">Es decir, se aplican a las coordenadas relativas a la vista de WebView y sin ajuste de PPP.</span><span class="sxs-lookup"><span data-stu-id="2d5db-224">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="2d5db-225">Miembros</span><span class="sxs-lookup"><span data-stu-id="2d5db-225">Members</span></span>

#### <span data-ttu-id="2d5db-226">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="2d5db-226">get_ButtonChangeKind</span></span> 

<span data-ttu-id="2d5db-227">Obtén la ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-227">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="2d5db-228">[get_ButtonChangeKind](#get_buttonchangekind)de HRESULT público (INT32 \* ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="2d5db-228">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="2d5db-229">Esto corresponde a la propiedad ButtonChangeKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="2d5db-229">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="2d5db-230">Los valores están definidos por la enumeración POINTER_BUTTON_CHANGE_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-230">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-231">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="2d5db-231">get_DisplayRect</span></span> 

<span data-ttu-id="2d5db-232">Obtén la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-232">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="2d5db-233">[get_DisplayRect](#get_displayrect)de HRESULT público (Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="2d5db-233">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="2d5db-234">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="2d5db-234">get_FrameId</span></span> 

<span data-ttu-id="2d5db-235">Obtén la FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-235">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="2d5db-236">[get_FrameId](#get_frameid)de HRESULT público (UINT32 \* FrameId)</span><span class="sxs-lookup"><span data-stu-id="2d5db-236">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="2d5db-237">Esto corresponde a la propiedad frameId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-237">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-238">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="2d5db-238">get_HimetricLocation</span></span> 

<span data-ttu-id="2d5db-239">Obtén la HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-239">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="2d5db-240">[get_HimetricLocation](#get_himetriclocation)de HRESULT público (Point \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="2d5db-240">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="2d5db-241">Esto corresponde a la propiedad ptHimetricLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-241">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-242">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="2d5db-242">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="2d5db-243">Obtén la HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-243">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="2d5db-244">[get_HimetricLocationRaw](#get_himetriclocationraw)de HRESULT público (Point \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="2d5db-244">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="2d5db-245">Esto corresponde a la propiedad ptHimetricLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-245">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-246">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="2d5db-246">get_HistoryCount</span></span> 

<span data-ttu-id="2d5db-247">Obtén la HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-247">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="2d5db-248">[get_HistoryCount](#get_historycount)de HRESULT público (UINT32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="2d5db-248">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="2d5db-249">Esto corresponde a la propiedad historyCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-249">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-250">get_InputData</span><span class="sxs-lookup"><span data-stu-id="2d5db-250">get_InputData</span></span> 

<span data-ttu-id="2d5db-251">Obtén la InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-251">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="2d5db-252">[get_InputData](#get_inputdata)de HRESULT público (INT32 \* InputData)</span><span class="sxs-lookup"><span data-stu-id="2d5db-252">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="2d5db-253">Esto corresponde a la propiedad InputData de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-253">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-254">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="2d5db-254">get_KeyStates</span></span> 

<span data-ttu-id="2d5db-255">Obtén la KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-255">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="2d5db-256">[get_KeyStates](#get_keystates)de HRESULT público (DWORD \* KeyStates)</span><span class="sxs-lookup"><span data-stu-id="2d5db-256">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="2d5db-257">Esto corresponde a la propiedad dwKeyStates de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-257">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-258">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="2d5db-258">get_PenFlags</span></span> 

<span data-ttu-id="2d5db-259">Obtén la PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-259">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="2d5db-260">[get_PenFlags](#get_penflags)de HRESULT público (UINT32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="2d5db-260">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="2d5db-261">Esto corresponde a la propiedad penFlags de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="2d5db-261">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="2d5db-262">Los valores están definidos por las constantes de PEN_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-262">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-263">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="2d5db-263">get_PenMask</span></span> 

<span data-ttu-id="2d5db-264">Obtén la PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-264">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="2d5db-265">[get_PenMask](#get_penmask)de HRESULT público (UINT32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="2d5db-265">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="2d5db-266">Esto corresponde a la propiedad penMask de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="2d5db-266">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="2d5db-267">Los valores están definidos por las constantes de PEN_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-267">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-268">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="2d5db-268">get_PenPressure</span></span> 

<span data-ttu-id="2d5db-269">Obtén la PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-269">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="2d5db-270">[get_PenPressure](#get_penpressure)de HRESULT público (UINT32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="2d5db-270">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="2d5db-271">Esto corresponde a la propiedad de presión de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-271">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-272">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="2d5db-272">get_PenRotation</span></span> 

<span data-ttu-id="2d5db-273">Obtén la PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-273">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="2d5db-274">[get_PenRotation](#get_penrotation)de HRESULT público (UINT32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="2d5db-274">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="2d5db-275">Esto corresponde a la propiedad Rotation de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-275">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-276">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="2d5db-276">get_PenTiltX</span></span> 

<span data-ttu-id="2d5db-277">Obtén la PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-277">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="2d5db-278">[get_PenTiltX](#get_pentiltx)de HRESULT público (INT32 \* PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="2d5db-278">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="2d5db-279">Esto corresponde a la propiedad tiltX de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-279">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-280">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="2d5db-280">get_PenTiltY</span></span> 

<span data-ttu-id="2d5db-281">Obtén la PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-281">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="2d5db-282">[get_PenTiltY](#get_pentilty)de HRESULT público (INT32 \* PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="2d5db-282">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="2d5db-283">Esto corresponde a la propiedad Tilt de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-283">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-284">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="2d5db-284">get_PerformanceCount</span></span> 

<span data-ttu-id="2d5db-285">Obtén la PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-285">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="2d5db-286">[get_PerformanceCount](#get_performancecount)(HRESULT) público (UINT64 \* PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="2d5db-286">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="2d5db-287">Esto corresponde a la propiedad PerformanceCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-287">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-288">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="2d5db-288">get_PixelLocation</span></span> 

<span data-ttu-id="2d5db-289">Obtén la PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-289">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="2d5db-290">[get_PixelLocation](#get_pixellocation)de HRESULT público (Point \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="2d5db-290">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="2d5db-291">Esto corresponde a la propiedad ptPixelLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-291">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-292">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="2d5db-292">get_PixelLocationRaw</span></span> 

<span data-ttu-id="2d5db-293">Obtén la PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-293">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="2d5db-294">[get_PixelLocationRaw](#get_pixellocationraw)de HRESULT público (Point \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="2d5db-294">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="2d5db-295">Esto corresponde a la propiedad ptPixelLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-295">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-296">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="2d5db-296">get_PointerDeviceRect</span></span> 

<span data-ttu-id="2d5db-297">Obtén la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-297">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="2d5db-298">[get_PointerDeviceRect](#get_pointerdevicerect)de HRESULT público (Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="2d5db-298">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="2d5db-299">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="2d5db-299">get_PointerFlags</span></span> 

<span data-ttu-id="2d5db-300">Obtén la PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-300">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="2d5db-301">[get_PointerFlags](#get_pointerflags)de HRESULT público (UINT32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="2d5db-301">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="2d5db-302">Esto corresponde a la propiedad pointerFlags de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="2d5db-302">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="2d5db-303">Los valores están definidos por las constantes de POINTER_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-303">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-304">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="2d5db-304">get_PointerId</span></span> 

<span data-ttu-id="2d5db-305">Obtén la PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-305">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="2d5db-306">[get_PointerId](#get_pointerid)de HRESULT público (UINT32 \* PointerId)</span><span class="sxs-lookup"><span data-stu-id="2d5db-306">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="2d5db-307">Esto corresponde a la propiedad pointerId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-307">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-308">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="2d5db-308">get_PointerKind</span></span> 

<span data-ttu-id="2d5db-309">Obtén la PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-309">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="2d5db-310">[get_PointerKind](#get_pointerkind)de HRESULT público (DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="2d5db-310">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="2d5db-311">Esto corresponde a la propiedad pointerKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="2d5db-311">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="2d5db-312">Los valores están definidos por la enumeración POINTER_INPUT_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-312">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="2d5db-313">Es compatible con PT_PEN y PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="2d5db-313">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="2d5db-314">get_Time</span><span class="sxs-lookup"><span data-stu-id="2d5db-314">get_Time</span></span> 

<span data-ttu-id="2d5db-315">Obtener la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-315">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="2d5db-316">[get_Time](#get_time)de HRESULT público (DWORD \* hora)</span><span class="sxs-lookup"><span data-stu-id="2d5db-316">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="2d5db-317">Esto corresponde a la propiedad dwTime de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-317">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-318">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="2d5db-318">get_TouchContact</span></span> 

<span data-ttu-id="2d5db-319">Obtén la TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-319">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="2d5db-320">[get_TouchContact](#get_touchcontact)de HRESULT público (Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="2d5db-320">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="2d5db-321">Esto corresponde a la propiedad rcContact de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-321">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-322">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="2d5db-322">get_TouchContactRaw</span></span> 

<span data-ttu-id="2d5db-323">Obtén la TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-323">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="2d5db-324">[get_TouchContactRaw](#get_touchcontactraw)de HRESULT público (Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="2d5db-324">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="2d5db-325">Esto corresponde a la propiedad rcContactRaw de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-325">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-326">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="2d5db-326">get_TouchFlags</span></span> 

<span data-ttu-id="2d5db-327">Obtén la TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-327">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="2d5db-328">[get_TouchFlags](#get_touchflags)de HRESULT público (UINT32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="2d5db-328">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="2d5db-329">Esto corresponde a la propiedad touchFlags de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="2d5db-329">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="2d5db-330">Los valores están definidos por las constantes de TOUCH_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-330">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-331">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="2d5db-331">get_TouchMask</span></span> 

<span data-ttu-id="2d5db-332">Obtén la TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-332">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="2d5db-333">[get_TouchMask](#get_touchmask)de HRESULT público (UINT32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="2d5db-333">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="2d5db-334">Esto corresponde a la propiedad touchMask de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="2d5db-334">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="2d5db-335">Los valores están definidos por las constantes de TOUCH_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-335">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-336">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="2d5db-336">get_TouchOrientation</span></span> 

<span data-ttu-id="2d5db-337">Obtén la TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-337">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="2d5db-338">[get_TouchOrientation](#get_touchorientation)de HRESULT público (UINT32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="2d5db-338">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="2d5db-339">Esto corresponde a la propiedad Orientation de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-339">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-340">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="2d5db-340">get_TouchPressure</span></span> 

<span data-ttu-id="2d5db-341">Obtén la TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-341">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="2d5db-342">[get_TouchPressure](#get_touchpressure)de HRESULT público (UINT32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="2d5db-342">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="2d5db-343">Esto corresponde a la propiedad de presión de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-343">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-344">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="2d5db-344">put_ButtonChangeKind</span></span> 

<span data-ttu-id="2d5db-345">Establezca el ButtonChangeKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-345">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="2d5db-346">[put_ButtonChangeKind](#put_buttonchangekind)de HRESULT público (INT32 ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="2d5db-346">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="2d5db-347">Esto corresponde a la propiedad ButtonChangeKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="2d5db-347">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="2d5db-348">Los valores están definidos por la enumeración POINTER_BUTTON_CHANGE_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-348">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-349">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="2d5db-349">put_DisplayRect</span></span> 

<span data-ttu-id="2d5db-350">Establezca la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-350">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="2d5db-351">[put_DisplayRect](#put_displayrect)de HRESULT público (Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="2d5db-351">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="2d5db-352">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="2d5db-352">put_FrameId</span></span> 

<span data-ttu-id="2d5db-353">Establezca el FrameID del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-353">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="2d5db-354">[put_FrameId](#put_frameid)de HRESULT público (UINT32 FrameId)</span><span class="sxs-lookup"><span data-stu-id="2d5db-354">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="2d5db-355">Esto corresponde a la propiedad frameId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-355">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-356">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="2d5db-356">put_HimetricLocation</span></span> 

<span data-ttu-id="2d5db-357">Establezca el HimetricLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-357">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="2d5db-358">[put_HimetricLocation](#put_himetriclocation)de HRESULT público (Point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="2d5db-358">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="2d5db-359">Esto corresponde a la propiedad ptHimetricLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-359">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-360">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="2d5db-360">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="2d5db-361">Establezca el HimetricLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-361">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="2d5db-362">[put_HimetricLocationRaw](#put_himetriclocationraw)de HRESULT público (Point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="2d5db-362">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="2d5db-363">Esto corresponde a la propiedad ptHimetricLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-363">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-364">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="2d5db-364">put_HistoryCount</span></span> 

<span data-ttu-id="2d5db-365">Establezca el HistoryCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-365">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="2d5db-366">[put_HistoryCount](#put_historycount)de HRESULT público (UINT32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="2d5db-366">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="2d5db-367">Esto corresponde a la propiedad historyCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-367">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-368">put_InputData</span><span class="sxs-lookup"><span data-stu-id="2d5db-368">put_InputData</span></span> 

<span data-ttu-id="2d5db-369">Establezca el InputData del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-369">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="2d5db-370">[put_InputData](#put_inputdata)de HRESULT público (INT32 InputData)</span><span class="sxs-lookup"><span data-stu-id="2d5db-370">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="2d5db-371">Esto corresponde a la propiedad InputData de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-371">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-372">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="2d5db-372">put_KeyStates</span></span> 

<span data-ttu-id="2d5db-373">Establezca el KeyStates del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-373">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="2d5db-374">[put_KeyStates](#put_keystates)de HRESULT público (DWORD KeyStates)</span><span class="sxs-lookup"><span data-stu-id="2d5db-374">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="2d5db-375">Esto corresponde a la propiedad dwKeyStates de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-375">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-376">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="2d5db-376">put_PenFlags</span></span> 

<span data-ttu-id="2d5db-377">Establezca el PenFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-377">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="2d5db-378">[put_PenFlags](#put_penflags)de HRESULT público (UINT32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="2d5db-378">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="2d5db-379">Esto corresponde a la propiedad penFlags de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="2d5db-379">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="2d5db-380">Los valores están definidos por las constantes de PEN_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-380">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-381">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="2d5db-381">put_PenMask</span></span> 

<span data-ttu-id="2d5db-382">Establezca el PenMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-382">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="2d5db-383">[put_PenMask](#put_penmask)de HRESULT público (UINT32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="2d5db-383">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="2d5db-384">Esto corresponde a la propiedad penMask de la estructura POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="2d5db-384">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="2d5db-385">Los valores están definidos por las constantes de PEN_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-385">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-386">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="2d5db-386">put_PenPressure</span></span> 

<span data-ttu-id="2d5db-387">Establezca el PenPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-387">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="2d5db-388">[put_PenPressure](#put_penpressure)de HRESULT público (UINT32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="2d5db-388">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="2d5db-389">Esto corresponde a la propiedad de presión de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-389">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-390">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="2d5db-390">put_PenRotation</span></span> 

<span data-ttu-id="2d5db-391">Establezca el PenRotation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-391">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="2d5db-392">[put_PenRotation](#put_penrotation)de HRESULT público (UINT32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="2d5db-392">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="2d5db-393">Esto corresponde a la propiedad Rotation de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-393">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-394">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="2d5db-394">put_PenTiltX</span></span> 

<span data-ttu-id="2d5db-395">Establezca el PenTiltX del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-395">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="2d5db-396">[put_PenTiltX](#put_pentiltx)de HRESULT público (INT32 PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="2d5db-396">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="2d5db-397">Esto corresponde a la propiedad tiltX de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-397">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-398">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="2d5db-398">put_PenTiltY</span></span> 

<span data-ttu-id="2d5db-399">Establezca el PenTiltY del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-399">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="2d5db-400">[put_PenTiltY](#put_pentilty)de HRESULT público (INT32 PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="2d5db-400">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="2d5db-401">Esto corresponde a la propiedad Tilt de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-401">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-402">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="2d5db-402">put_PerformanceCount</span></span> 

<span data-ttu-id="2d5db-403">Establezca el PerformanceCount del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-403">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="2d5db-404">[put_PerformanceCount](#put_performancecount)(HRESULT) público (UINT64 PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="2d5db-404">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="2d5db-405">Esto corresponde a la propiedad PerformanceCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-405">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-406">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="2d5db-406">put_PixelLocation</span></span> 

<span data-ttu-id="2d5db-407">Establezca el PixelLocation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-407">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="2d5db-408">[put_PixelLocation](#put_pixellocation)de HRESULT público (Point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="2d5db-408">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="2d5db-409">Esto corresponde a la propiedad ptPixelLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-409">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-410">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="2d5db-410">put_PixelLocationRaw</span></span> 

<span data-ttu-id="2d5db-411">Establezca el PixelLocationRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-411">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="2d5db-412">[put_PixelLocationRaw](#put_pixellocationraw)de HRESULT público (Point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="2d5db-412">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="2d5db-413">Esto corresponde a la propiedad ptPixelLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-413">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-414">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="2d5db-414">put_PointerDeviceRect</span></span> 

<span data-ttu-id="2d5db-415">Establezca la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-415">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="2d5db-416">[put_PointerDeviceRect](#put_pointerdevicerect)de HRESULT público (Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="2d5db-416">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="2d5db-417">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="2d5db-417">put_PointerFlags</span></span> 

<span data-ttu-id="2d5db-418">Establezca el PointerFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-418">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="2d5db-419">[put_PointerFlags](#put_pointerflags)de HRESULT público (UINT32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="2d5db-419">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="2d5db-420">Esto corresponde a la propiedad pointerFlags de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="2d5db-420">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="2d5db-421">Los valores están definidos por las constantes de POINTER_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-421">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-422">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="2d5db-422">put_PointerId</span></span> 

<span data-ttu-id="2d5db-423">Establezca el PointerId del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-423">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="2d5db-424">[put_PointerId](#put_pointerid)de HRESULT público (UINT32 PointerId)</span><span class="sxs-lookup"><span data-stu-id="2d5db-424">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="2d5db-425">Esto corresponde a la propiedad pointerId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-425">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-426">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="2d5db-426">put_PointerKind</span></span> 

<span data-ttu-id="2d5db-427">Establezca el PointerKind del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-427">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="2d5db-428">[put_PointerKind](#put_pointerkind)de HRESULT público (DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="2d5db-428">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="2d5db-429">Esto corresponde a la propiedad pointerKind de la estructura POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="2d5db-429">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="2d5db-430">Los valores están definidos por la enumeración POINTER_INPUT_KIND en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-430">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="2d5db-431">Es compatible con PT_PEN y PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="2d5db-431">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="2d5db-432">put_Time</span><span class="sxs-lookup"><span data-stu-id="2d5db-432">put_Time</span></span> 

<span data-ttu-id="2d5db-433">Establezca la hora del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-433">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="2d5db-434">[put_Time](#put_time)de HRESULT público (hora de DWORD)</span><span class="sxs-lookup"><span data-stu-id="2d5db-434">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="2d5db-435">Esto corresponde a la propiedad dwTime de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-435">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-436">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="2d5db-436">put_TouchContact</span></span> 

<span data-ttu-id="2d5db-437">Establezca el TouchContact del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-437">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="2d5db-438">[put_TouchContact](#put_touchcontact)de HRESULT público (Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="2d5db-438">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="2d5db-439">Esto corresponde a la propiedad rcContact de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-439">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-440">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="2d5db-440">put_TouchContactRaw</span></span> 

<span data-ttu-id="2d5db-441">Establezca el TouchContactRaw del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-441">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="2d5db-442">[put_TouchContactRaw](#put_touchcontactraw)de HRESULT público (Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="2d5db-442">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="2d5db-443">Esto corresponde a la propiedad rcContactRaw de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-443">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-444">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="2d5db-444">put_TouchFlags</span></span> 

<span data-ttu-id="2d5db-445">Establezca el TouchFlags del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-445">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="2d5db-446">[put_TouchFlags](#put_touchflags)de HRESULT público (UINT32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="2d5db-446">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="2d5db-447">Esto corresponde a la propiedad touchFlags de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="2d5db-447">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="2d5db-448">Los valores están definidos por las constantes de TOUCH_FLAGS en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-448">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-449">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="2d5db-449">put_TouchMask</span></span> 

<span data-ttu-id="2d5db-450">Establezca el TouchMask del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-450">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="2d5db-451">[put_TouchMask](#put_touchmask)de HRESULT público (UINT32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="2d5db-451">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="2d5db-452">Esto corresponde a la propiedad touchMask de la estructura POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="2d5db-452">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="2d5db-453">Los valores están definidos por las constantes de TOUCH_MASK en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-453">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-454">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="2d5db-454">put_TouchOrientation</span></span> 

<span data-ttu-id="2d5db-455">Establezca el TouchOrientation del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-455">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="2d5db-456">[put_TouchOrientation](#put_touchorientation)de HRESULT público (UINT32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="2d5db-456">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="2d5db-457">Esto corresponde a la propiedad Orientation de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-457">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="2d5db-458">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="2d5db-458">put_TouchPressure</span></span> 

<span data-ttu-id="2d5db-459">Establezca el TouchPressure del evento de puntero.</span><span class="sxs-lookup"><span data-stu-id="2d5db-459">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="2d5db-460">[put_TouchPressure](#put_touchpressure)de HRESULT público (UINT32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="2d5db-460">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="2d5db-461">Esto corresponde a la propiedad de presión de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="2d5db-461">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>


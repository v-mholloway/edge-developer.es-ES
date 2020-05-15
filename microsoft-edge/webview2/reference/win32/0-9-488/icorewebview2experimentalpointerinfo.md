---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 2141dff54b44fe6d9a2758f571e61b81877079da
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655303"
---
# interfaz ICoreWebView2ExperimentalPointerInfo 

> [!NOTE]
> Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.488.

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

Esto representa principalmente un objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_ButtonChangeKind](#get_buttonchangekind) | Obtén la ButtonChangeKind del evento de puntero.
[get_DisplayRect](#get_displayrect) | Obtén la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).
[get_FrameId](#get_frameid) | Obtén la FrameID del evento de puntero.
[get_HimetricLocation](#get_himetriclocation) | Obtén la HimetricLocation del evento de puntero.
[get_HimetricLocationRaw](#get_himetriclocationraw) | Obtén la HimetricLocationRaw del evento de puntero.
[get_HistoryCount](#get_historycount) | Obtén la HistoryCount del evento de puntero.
[get_InputData](#get_inputdata) | Obtén la InputData del evento de puntero.
[get_KeyStates](#get_keystates) | Obtén la KeyStates del evento de puntero.
[get_PenFlags](#get_penflags) | Obtén la PenFlags del evento de puntero.
[get_PenMask](#get_penmask) | Obtén la PenMask del evento de puntero.
[get_PenPressure](#get_penpressure) | Obtén la PenPressure del evento de puntero.
[get_PenRotation](#get_penrotation) | Obtén la PenRotation del evento de puntero.
[get_PenTiltX](#get_pentiltx) | Obtén la PenTiltX del evento de puntero.
[get_PenTiltY](#get_pentilty) | Obtén la PenTiltY del evento de puntero.
[get_PerformanceCount](#get_performancecount) | Obtén la PerformanceCount del evento de puntero.
[get_PixelLocation](#get_pixellocation) | Obtén la PixelLocation del evento de puntero.
[get_PixelLocationRaw](#get_pixellocationraw) | Obtén la PixelLocationRaw del evento de puntero.
[get_PointerDeviceRect](#get_pointerdevicerect) | Obtén la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).
[get_PointerFlags](#get_pointerflags) | Obtén la PointerFlags del evento de puntero.
[get_PointerId](#get_pointerid) | Obtén la PointerId del evento de puntero.
[get_PointerKind](#get_pointerkind) | Obtén la PointerKind del evento de puntero.
[get_Time](#get_time) | Obtener la hora del evento de puntero.
[get_TouchContact](#get_touchcontact) | Obtén la TouchContact del evento de puntero.
[get_TouchContactRaw](#get_touchcontactraw) | Obtén la TouchContactRaw del evento de puntero.
[get_TouchFlags](#get_touchflags) | Obtén la TouchFlags del evento de puntero.
[get_TouchMask](#get_touchmask) | Obtén la TouchMask del evento de puntero.
[get_TouchOrientation](#get_touchorientation) | Obtén la TouchOrientation del evento de puntero.
[get_TouchPressure](#get_touchpressure) | Obtén la TouchPressure del evento de puntero.
[put_ButtonChangeKind](#put_buttonchangekind) | Establezca el ButtonChangeKind del evento de puntero.
[put_DisplayRect](#put_displayrect) | Establezca la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).
[put_FrameId](#put_frameid) | Establezca el FrameID del evento de puntero.
[put_HimetricLocation](#put_himetriclocation) | Establezca el HimetricLocation del evento de puntero.
[put_HimetricLocationRaw](#put_himetriclocationraw) | Establezca el HimetricLocationRaw del evento de puntero.
[put_HistoryCount](#put_historycount) | Establezca el HistoryCount del evento de puntero.
[put_InputData](#put_inputdata) | Establezca el InputData del evento de puntero.
[put_KeyStates](#put_keystates) | Establezca el KeyStates del evento de puntero.
[put_PenFlags](#put_penflags) | Establezca el PenFlags del evento de puntero.
[put_PenMask](#put_penmask) | Establezca el PenMask del evento de puntero.
[put_PenPressure](#put_penpressure) | Establezca el PenPressure del evento de puntero.
[put_PenRotation](#put_penrotation) | Establezca el PenRotation del evento de puntero.
[put_PenTiltX](#put_pentiltx) | Establezca el PenTiltX del evento de puntero.
[put_PenTiltY](#put_pentilty) | Establezca el PenTiltY del evento de puntero.
[put_PerformanceCount](#put_performancecount) | Establezca el PerformanceCount del evento de puntero.
[put_PixelLocation](#put_pixellocation) | Establezca el PixelLocation del evento de puntero.
[put_PixelLocationRaw](#put_pixellocationraw) | Establezca el PixelLocationRaw del evento de puntero.
[put_PointerDeviceRect](#put_pointerdevicerect) | Establezca la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).
[put_PointerFlags](#put_pointerflags) | Establezca el PointerFlags del evento de puntero.
[put_PointerId](#put_pointerid) | Establezca el PointerId del evento de puntero.
[put_PointerKind](#put_pointerkind) | Establezca el PointerKind del evento de puntero.
[put_Time](#put_time) | Establezca la hora del evento de puntero.
[put_TouchContact](#put_touchcontact) | Establezca el TouchContact del evento de puntero.
[put_TouchContactRaw](#put_touchcontactraw) | Establezca el TouchContactRaw del evento de puntero.
[put_TouchFlags](#put_touchflags) | Establezca el TouchFlags del evento de puntero.
[put_TouchMask](#put_touchmask) | Establezca el TouchMask del evento de puntero.
[put_TouchOrientation](#put_touchorientation) | Establezca el TouchOrientation del evento de puntero.
[put_TouchPressure](#put_touchpressure) | Establezca el TouchPressure del evento de puntero.

Toma campos de los tres y excluye algunos tipos de datos específicos de Win32, como HWND y HANDLE. Ten en cuenta que sourceDevice se extrae, pero esperamos que PointerDeviceRect y DisplayRect cubran los casos de uso existentes de sourceDevice. Otra diferencia importante es que se espera que cualquiera de las ubicaciones de Point o Rect estén en coordenadas físicas de WebView. Es decir, se aplican a las coordenadas relativas a la vista de WebView y sin ajuste de PPP.

## Miembros

#### get_ButtonChangeKind 

Obtén la ButtonChangeKind del evento de puntero.

> [get_ButtonChangeKind](#get_buttonchangekind)de HRESULT público (INT32 * ButtonChangeKind)

Esto corresponde a la propiedad ButtonChangeKind de la estructura POINTER_INFO. Los valores están definidos por la enumeración POINTER_BUTTON_CHANGE_KIND en el SDK de Windows (Winuser. h).

#### get_DisplayRect 

Obtén la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

> [get_DisplayRect](#get_displayrect)de HRESULT público (Rect * DisplayRect)

#### get_FrameId 

Obtén la FrameID del evento de puntero.

> [get_FrameId](#get_frameid)de HRESULT público (UINT32 * FrameId)

Esto corresponde a la propiedad frameId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_HimetricLocation 

Obtén la HimetricLocation del evento de puntero.

> [get_HimetricLocation](#get_himetriclocation)de HRESULT público (Point * HimetricLocation)

Esto corresponde a la propiedad ptHimetricLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_HimetricLocationRaw 

Obtén la HimetricLocationRaw del evento de puntero.

> [get_HimetricLocationRaw](#get_himetriclocationraw)de HRESULT público (Point * HimetricLocationRaw)

Esto corresponde a la propiedad ptHimetricLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_HistoryCount 

Obtén la HistoryCount del evento de puntero.

> [get_HistoryCount](#get_historycount)de HRESULT público (UINT32 * HistoryCount)

Esto corresponde a la propiedad historyCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_InputData 

Obtén la InputData del evento de puntero.

> [get_InputData](#get_inputdata)de HRESULT público (INT32 * InputData)

Esto corresponde a la propiedad InputData de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_KeyStates 

Obtén la KeyStates del evento de puntero.

> [get_KeyStates](#get_keystates)de HRESULT público (DWORD * KeyStates)

Esto corresponde a la propiedad dwKeyStates de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_PenFlags 

Obtén la PenFlags del evento de puntero.

> [get_PenFlags](#get_penflags)de HRESULT público (UINT32 * PenFlags)

Esto corresponde a la propiedad penFlags de la estructura POINTER_PEN_INFO. Los valores están definidos por las constantes de PEN_FLAGS en el SDK de Windows (Winuser. h).

#### get_PenMask 

Obtén la PenMask del evento de puntero.

> [get_PenMask](#get_penmask)de HRESULT público (UINT32 * PenMask)

Esto corresponde a la propiedad penMask de la estructura POINTER_PEN_INFO. Los valores están definidos por las constantes de PEN_MASK en el SDK de Windows (Winuser. h).

#### get_PenPressure 

Obtén la PenPressure del evento de puntero.

> [get_PenPressure](#get_penpressure)de HRESULT público (UINT32 * PenPressure)

Esto corresponde a la propiedad de presión de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_PenRotation 

Obtén la PenRotation del evento de puntero.

> [get_PenRotation](#get_penrotation)de HRESULT público (UINT32 * PenRotation)

Esto corresponde a la propiedad Rotation de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_PenTiltX 

Obtén la PenTiltX del evento de puntero.

> [get_PenTiltX](#get_pentiltx)de HRESULT público (INT32 * PenTiltX)

Esto corresponde a la propiedad tiltX de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_PenTiltY 

Obtén la PenTiltY del evento de puntero.

> [get_PenTiltY](#get_pentilty)de HRESULT público (INT32 * PenTiltY)

Esto corresponde a la propiedad Tilt de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_PerformanceCount 

Obtén la PerformanceCount del evento de puntero.

> [get_PerformanceCount](#get_performancecount)(HRESULT) público (UINT64 * PerformanceCount)

Esto corresponde a la propiedad PerformanceCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_PixelLocation 

Obtén la PixelLocation del evento de puntero.

> [get_PixelLocation](#get_pixellocation)de HRESULT público (Point * PixelLocation)

Esto corresponde a la propiedad ptPixelLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_PixelLocationRaw 

Obtén la PixelLocationRaw del evento de puntero.

> [get_PixelLocationRaw](#get_pixellocationraw)de HRESULT público (Point * PixelLocationRaw)

Esto corresponde a la propiedad ptPixelLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_PointerDeviceRect 

Obtén la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

> [get_PointerDeviceRect](#get_pointerdevicerect)de HRESULT público (Rect * PointerDeviceRect)

#### get_PointerFlags 

Obtén la PointerFlags del evento de puntero.

> [get_PointerFlags](#get_pointerflags)de HRESULT público (UINT32 * PointerFlags)

Esto corresponde a la propiedad pointerFlags de la estructura POINTER_INFO. Los valores están definidos por las constantes de POINTER_FLAGS en el SDK de Windows (Winuser. h).

#### get_PointerId 

Obtén la PointerId del evento de puntero.

> [get_PointerId](#get_pointerid)de HRESULT público (UINT32 * PointerId)

Esto corresponde a la propiedad pointerId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_PointerKind 

Obtén la PointerKind del evento de puntero.

> [get_PointerKind](#get_pointerkind)de HRESULT público (DWORD * PointerKind)

Esto corresponde a la propiedad pointerKind de la estructura POINTER_INFO. Los valores están definidos por la enumeración POINTER_INPUT_KIND en el SDK de Windows (Winuser. h). Es compatible con PT_PEN y PT_TOUCH.

#### get_Time 

Obtener la hora del evento de puntero.

> [get_Time](#get_time)de HRESULT público (DWORD * hora)

Esto corresponde a la propiedad dwTime de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_TouchContact 

Obtén la TouchContact del evento de puntero.

> [get_TouchContact](#get_touchcontact)de HRESULT público (Rect * TouchContact)

Esto corresponde a la propiedad rcContact de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_TouchContactRaw 

Obtén la TouchContactRaw del evento de puntero.

> [get_TouchContactRaw](#get_touchcontactraw)de HRESULT público (Rect * TouchContactRaw)

Esto corresponde a la propiedad rcContactRaw de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_TouchFlags 

Obtén la TouchFlags del evento de puntero.

> [get_TouchFlags](#get_touchflags)de HRESULT público (UINT32 * TouchFlags)

Esto corresponde a la propiedad touchFlags de la estructura POINTER_TOUCH_INFO. Los valores están definidos por las constantes de TOUCH_FLAGS en el SDK de Windows (Winuser. h).

#### get_TouchMask 

Obtén la TouchMask del evento de puntero.

> [get_TouchMask](#get_touchmask)de HRESULT público (UINT32 * TouchMask)

Esto corresponde a la propiedad touchMask de la estructura POINTER_TOUCH_INFO. Los valores están definidos por las constantes de TOUCH_MASK en el SDK de Windows (Winuser. h).

#### get_TouchOrientation 

Obtén la TouchOrientation del evento de puntero.

> [get_TouchOrientation](#get_touchorientation)de HRESULT público (UINT32 * TouchOrientation)

Esto corresponde a la propiedad Orientation de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### get_TouchPressure 

Obtén la TouchPressure del evento de puntero.

> [get_TouchPressure](#get_touchpressure)de HRESULT público (UINT32 * TouchPressure)

Esto corresponde a la propiedad de presión de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_ButtonChangeKind 

Establezca el ButtonChangeKind del evento de puntero.

> [put_ButtonChangeKind](#put_buttonchangekind)de HRESULT público (INT32 ButtonChangeKind)

Esto corresponde a la propiedad ButtonChangeKind de la estructura POINTER_INFO. Los valores están definidos por la enumeración POINTER_BUTTON_CHANGE_KIND en el SDK de Windows (Winuser. h).

#### put_DisplayRect 

Establezca la DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

> [put_DisplayRect](#put_displayrect)de HRESULT público (Rect DisplayRect)

#### put_FrameId 

Establezca el FrameID del evento de puntero.

> [put_FrameId](#put_frameid)de HRESULT público (UINT32 FrameId)

Esto corresponde a la propiedad frameId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_HimetricLocation 

Establezca el HimetricLocation del evento de puntero.

> [put_HimetricLocation](#put_himetriclocation)de HRESULT público (Point HimetricLocation)

Esto corresponde a la propiedad ptHimetricLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_HimetricLocationRaw 

Establezca el HimetricLocationRaw del evento de puntero.

> [put_HimetricLocationRaw](#put_himetriclocationraw)de HRESULT público (Point HimetricLocationRaw)

Esto corresponde a la propiedad ptHimetricLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_HistoryCount 

Establezca el HistoryCount del evento de puntero.

> [put_HistoryCount](#put_historycount)de HRESULT público (UINT32 HistoryCount)

Esto corresponde a la propiedad historyCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_InputData 

Establezca el InputData del evento de puntero.

> [put_InputData](#put_inputdata)de HRESULT público (INT32 InputData)

Esto corresponde a la propiedad InputData de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_KeyStates 

Establezca el KeyStates del evento de puntero.

> [put_KeyStates](#put_keystates)de HRESULT público (DWORD KeyStates)

Esto corresponde a la propiedad dwKeyStates de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_PenFlags 

Establezca el PenFlags del evento de puntero.

> [put_PenFlags](#put_penflags)de HRESULT público (UINT32 PenFlags)

Esto corresponde a la propiedad penFlags de la estructura POINTER_PEN_INFO. Los valores están definidos por las constantes de PEN_FLAGS en el SDK de Windows (Winuser. h).

#### put_PenMask 

Establezca el PenMask del evento de puntero.

> [put_PenMask](#put_penmask)de HRESULT público (UINT32 PenMask)

Esto corresponde a la propiedad penMask de la estructura POINTER_PEN_INFO. Los valores están definidos por las constantes de PEN_MASK en el SDK de Windows (Winuser. h).

#### put_PenPressure 

Establezca el PenPressure del evento de puntero.

> [put_PenPressure](#put_penpressure)de HRESULT público (UINT32 PenPressure)

Esto corresponde a la propiedad de presión de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_PenRotation 

Establezca el PenRotation del evento de puntero.

> [put_PenRotation](#put_penrotation)de HRESULT público (UINT32 PenRotation)

Esto corresponde a la propiedad Rotation de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_PenTiltX 

Establezca el PenTiltX del evento de puntero.

> [put_PenTiltX](#put_pentiltx)de HRESULT público (INT32 PenTiltX)

Esto corresponde a la propiedad tiltX de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_PenTiltY 

Establezca el PenTiltY del evento de puntero.

> [put_PenTiltY](#put_pentilty)de HRESULT público (INT32 PenTiltY)

Esto corresponde a la propiedad Tilt de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_PerformanceCount 

Establezca el PerformanceCount del evento de puntero.

> [put_PerformanceCount](#put_performancecount)(HRESULT) público (UINT64 PerformanceCount)

Esto corresponde a la propiedad PerformanceCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_PixelLocation 

Establezca el PixelLocation del evento de puntero.

> [put_PixelLocation](#put_pixellocation)de HRESULT público (Point PixelLocation)

Esto corresponde a la propiedad ptPixelLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_PixelLocationRaw 

Establezca el PixelLocationRaw del evento de puntero.

> [put_PixelLocationRaw](#put_pixellocationraw)de HRESULT público (Point PixelLocationRaw)

Esto corresponde a la propiedad ptPixelLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_PointerDeviceRect 

Establezca la PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

> [put_PointerDeviceRect](#put_pointerdevicerect)de HRESULT público (Rect PointerDeviceRect)

#### put_PointerFlags 

Establezca el PointerFlags del evento de puntero.

> [put_PointerFlags](#put_pointerflags)de HRESULT público (UINT32 PointerFlags)

Esto corresponde a la propiedad pointerFlags de la estructura POINTER_INFO. Los valores están definidos por las constantes de POINTER_FLAGS en el SDK de Windows (Winuser. h).

#### put_PointerId 

Establezca el PointerId del evento de puntero.

> [put_PointerId](#put_pointerid)de HRESULT público (UINT32 PointerId)

Esto corresponde a la propiedad pointerId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_PointerKind 

Establezca el PointerKind del evento de puntero.

> [put_PointerKind](#put_pointerkind)de HRESULT público (DWORD PointerKind)

Esto corresponde a la propiedad pointerKind de la estructura POINTER_INFO. Los valores están definidos por la enumeración POINTER_INPUT_KIND en el SDK de Windows (Winuser. h). Es compatible con PT_PEN y PT_TOUCH.

#### put_Time 

Establezca la hora del evento de puntero.

> [put_Time](#put_time)de HRESULT público (hora de DWORD)

Esto corresponde a la propiedad dwTime de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_TouchContact 

Establezca el TouchContact del evento de puntero.

> [put_TouchContact](#put_touchcontact)de HRESULT público (Rect TouchContact)

Esto corresponde a la propiedad rcContact de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_TouchContactRaw 

Establezca el TouchContactRaw del evento de puntero.

> [put_TouchContactRaw](#put_touchcontactraw)de HRESULT público (Rect TouchContactRaw)

Esto corresponde a la propiedad rcContactRaw de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_TouchFlags 

Establezca el TouchFlags del evento de puntero.

> [put_TouchFlags](#put_touchflags)de HRESULT público (UINT32 TouchFlags)

Esto corresponde a la propiedad touchFlags de la estructura POINTER_TOUCH_INFO. Los valores están definidos por las constantes de TOUCH_FLAGS en el SDK de Windows (Winuser. h).

#### put_TouchMask 

Establezca el TouchMask del evento de puntero.

> [put_TouchMask](#put_touchmask)de HRESULT público (UINT32 TouchMask)

Esto corresponde a la propiedad touchMask de la estructura POINTER_TOUCH_INFO. Los valores están definidos por las constantes de TOUCH_MASK en el SDK de Windows (Winuser. h).

#### put_TouchOrientation 

Establezca el TouchOrientation del evento de puntero.

> [put_TouchOrientation](#put_touchorientation)de HRESULT público (UINT32 TouchOrientation)

Esto corresponde a la propiedad Orientation de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### put_TouchPressure 

Establezca el TouchPressure del evento de puntero.

> [put_TouchPressure](#put_touchpressure)de HRESULT público (UINT32 TouchPressure)

Esto corresponde a la propiedad de presión de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).


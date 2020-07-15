---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
ms.openlocfilehash: 8a5e5f4188b5115e1c6b836f80aad69c4bf2da7e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878761"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

Esto representa principalmente un objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[ButtonChangeKind](#buttonchangekind) | El ButtonChangeKind del evento de puntero.
[DisplayRect](#displayrect) | El DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).
[FrameId](#frameid) | El FrameID del evento de puntero.
[HimetricLocation](#himetriclocation) | El HimetricLocation del evento de puntero.
[HimetricLocationRaw](#himetriclocationraw) | El HimetricLocationRaw del evento de puntero.
[HistoryCount](#historycount) | El HistoryCount del evento de puntero.
[InputData](#inputdata) | El InputData del evento de puntero.
[KeyStates](#keystates) | El KeyStates del evento de puntero.
[PenFlags](#penflags) | El PenFlags del evento de puntero.
[PenMask](#penmask) | El PenMask del evento de puntero.
[PenPressure](#penpressure) | El PenPressure del evento de puntero.
[PenRotation](#penrotation) | El PenRotation del evento de puntero.
[PenTiltX](#pentiltx) | El PenTiltX del evento de puntero.
[PenTiltY](#pentilty) | El PenTiltY del evento de puntero.
[PerformanceCount](#performancecount) | El PerformanceCount del evento de puntero.
[PixelLocation](#pixellocation) | El PixelLocation del evento de puntero.
[PixelLocationRaw](#pixellocationraw) | El PixelLocationRaw del evento de puntero.
[PointerDeviceRect](#pointerdevicerect) | El PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).
[PointerFlags](#pointerflags) | El PointerFlags del evento de puntero.
[PointerId](#pointerid) | El PointerId del evento de puntero.
[PointerKind](#pointerkind) | El PointerKind del evento de puntero.
[Tiempo](#time) | Hora del evento de puntero.
[TouchContact](#touchcontact) | El TouchContact del evento de puntero.
[TouchContactRaw](#touchcontactraw) | El TouchContactRaw del evento de puntero.
[TouchFlags](#touchflags) | El TouchFlags del evento de puntero.
[TouchMask](#touchmask) | El TouchMask del evento de puntero.
[TouchOrientation](#touchorientation) | El TouchOrientation del evento de puntero.
[TouchPressure](#touchpressure) | El TouchPressure del evento de puntero.

## Miembros

#### ButtonChangeKind 

El ButtonChangeKind del evento de puntero.

> public int [ButtonChangeKind](#buttonchangekind)

Esto corresponde a la propiedad ButtonChangeKind de la estructura POINTER_INFO. Los valores están definidos por la enumeración POINTER_BUTTON_CHANGE_KIND en el SDK de Windows (Winuser. h).

#### DisplayRect 

El DisplayRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

> Public Rect [DisplayRect](#displayrect)

#### FrameId 

El FrameID del evento de puntero.

> uint pública [FrameId](#frameid)

Esto corresponde a la propiedad frameId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### HimetricLocation 

El HimetricLocation del evento de puntero.

> Punto público [HimetricLocation](#himetriclocation)

Esto corresponde a la propiedad ptHimetricLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### HimetricLocationRaw 

El HimetricLocationRaw del evento de puntero.

> Punto público [HimetricLocationRaw](#himetriclocationraw)

Esto corresponde a la propiedad ptHimetricLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### HistoryCount 

El HistoryCount del evento de puntero.

> uint pública [HistoryCount](#historycount)

Esto corresponde a la propiedad historyCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### InputData 

El InputData del evento de puntero.

> public int [InputData](#inputdata)

Esto corresponde a la propiedad InputData de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### KeyStates 

El KeyStates del evento de puntero.

> uint pública [KeyStates](#keystates)

Esto corresponde a la propiedad dwKeyStates de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### PenFlags 

El PenFlags del evento de puntero.

> uint pública [PenFlags](#penflags)

Esto corresponde a la propiedad penFlags de la estructura POINTER_PEN_INFO. Los valores están definidos por las constantes de PEN_FLAGS en el SDK de Windows (Winuser. h).

#### PenMask 

El PenMask del evento de puntero.

> uint pública [PenMask](#penmask)

Esto corresponde a la propiedad penMask de la estructura POINTER_PEN_INFO. Los valores están definidos por las constantes de PEN_MASK en el SDK de Windows (Winuser. h).

#### PenPressure 

El PenPressure del evento de puntero.

> uint pública [PenPressure](#penpressure)

Esto corresponde a la propiedad de presión de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### PenRotation 

El PenRotation del evento de puntero.

> uint pública [PenRotation](#penrotation)

Esto corresponde a la propiedad Rotation de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### PenTiltX 

El PenTiltX del evento de puntero.

> public int [PenTiltX](#pentiltx)

Esto corresponde a la propiedad tiltX de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### PenTiltY 

El PenTiltY del evento de puntero.

> public int [PenTiltY](#pentilty)

Esto corresponde a la propiedad Tilt de la estructura POINTER_PEN_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### PerformanceCount 

El PerformanceCount del evento de puntero.

> ulong [PerformanceCount](#performancecount)

Esto corresponde a la propiedad PerformanceCount de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### PixelLocation 

El PixelLocation del evento de puntero.

> Punto público [PixelLocation](#pixellocation)

Esto corresponde a la propiedad ptPixelLocation de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### PixelLocationRaw 

El PixelLocationRaw del evento de puntero.

> Punto público [PixelLocationRaw](#pixellocationraw)

Esto corresponde a la propiedad ptPixelLocationRaw de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### PointerDeviceRect 

El PointerDeviceRect de la propiedad sourceDevice de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

> Public Rect [PointerDeviceRect](#pointerdevicerect)

#### PointerFlags 

El PointerFlags del evento de puntero.

> uint pública [PointerFlags](#pointerflags)

Esto corresponde a la propiedad pointerFlags de la estructura POINTER_INFO. Los valores están definidos por las constantes de POINTER_FLAGS en el SDK de Windows (Winuser. h).

#### PointerId 

El PointerId del evento de puntero.

> uint pública [PointerId](#pointerid)

Esto corresponde a la propiedad pointerId de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### PointerKind 

El PointerKind del evento de puntero.

> uint pública [PointerKind](#pointerkind)

Esto corresponde a la propiedad pointerKind de la estructura POINTER_INFO. Los valores están definidos por la enumeración POINTER_INPUT_KIND en el SDK de Windows (Winuser. h). Es compatible con PT_PEN y PT_TOUCH.

#### Tiempo 

Hora del evento de puntero.

> [hora](#time) uint pública

Esto corresponde a la propiedad dwTime de la estructura POINTER_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### TouchContact 

El TouchContact del evento de puntero.

> Public Rect [TouchContact](#touchcontact)

Esto corresponde a la propiedad rcContact de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### TouchContactRaw 

El TouchContactRaw del evento de puntero.

> Public Rect [TouchContactRaw](#touchcontactraw)

Esto corresponde a la propiedad rcContactRaw de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### TouchFlags 

El TouchFlags del evento de puntero.

> uint pública [TouchFlags](#touchflags)

Esto corresponde a la propiedad touchFlags de la estructura POINTER_TOUCH_INFO. Los valores están definidos por las constantes de TOUCH_FLAGS en el SDK de Windows (Winuser. h).

#### TouchMask 

El TouchMask del evento de puntero.

> uint pública [TouchMask](#touchmask)

Esto corresponde a la propiedad touchMask de la estructura POINTER_TOUCH_INFO. Los valores están definidos por las constantes de TOUCH_MASK en el SDK de Windows (Winuser. h).

#### TouchOrientation 

El TouchOrientation del evento de puntero.

> uint pública [TouchOrientation](#touchorientation)

Esto corresponde a la propiedad Orientation de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).

#### TouchPressure 

El TouchPressure del evento de puntero.

> uint pública [TouchPressure](#touchpressure)

Esto corresponde a la propiedad de presión de la estructura POINTER_TOUCH_INFO, tal como se define en el SDK de Windows (Winuser. h).


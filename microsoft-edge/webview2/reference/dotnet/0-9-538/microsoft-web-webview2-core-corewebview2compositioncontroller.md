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
ms.openlocfilehash: 33adcccc4174a4ebcbabe4a169cd430942ad8a5a
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699444"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2CompositionController 

> [!NOTE]
> Esta es una [API experimental](../../../concepts/versioning.md#experimental-apis) que se incluía con nuestra versión [de SDK 0.9.538-prerelease](../../../releasenotes.md#09538).

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft. Web. WebView2. Core. dll

Esta clase es una extensión de la clase CoreWebView2Controller para admitir el hospedaje visual.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Cursor](#cursor) | El cursor actual que la vista en WebView debe tener.
[CursorChanged](#cursorchanged) | El evento se desencadena cuando WebView considera que se debe cambiar el cursor.
[RootVisualTarget](#rootvisualtarget) | El RootVisualTarget es un objeto visual en el árbol visual de la aplicación de hospedaje.
[UIAProvider](#uiaprovider) | Devuelve el proveedor de automatización de la interfaz de usuario de WebView.
[CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid) | Una función auxiliar para convertir una pointerId recibida del sistema en un CoreWebView2ExperimentalPointerInfo.
[SendMouseInput](#sendmouseinput) | Si eventKind es CoreWebView2MouseEventKind. HorizontalWheel o CoreWebView2MouseEventKind. Wheel, mouseData especifica la cantidad de movimiento de la rueda.
[SendPointerInput](#sendpointerinput) | SendPointerInput acepta la entrada de puntero táctil o de lápiz de los tipos definidos en CoreWebView2PointerEventKind.

## Miembros

#### Cursor 

El cursor actual que la vista en WebView debe tener.

> [cursor](#cursor) IntPtr público

El cursor debe establecerse en WM_SETCURSOR a través de mouse. SetCursor o establecerse en el HWND principal/antecesor correspondiente de la vista de vista rápida a través de SetClassLongPtr. El HCURSOR se puede liberar, por lo que se recomienda CopyCursor/DestroyCursor para conservar su propia copia si hace más de lo que hay que establecer inmediatamente el cursor.

#### CursorChanged 

El evento se desencadena cuando WebView considera que se debe cambiar el cursor.

> evento público EventHandler< > [CursorChanged](#cursorchanged)

Por ejemplo, cuando el cursor del mouse es actualmente el cursor predeterminado pero, después, se desplaza por el texto, puede intentar cambiar al cursor IBeam.

#### RootVisualTarget 

El RootVisualTarget es un objeto visual en el árbol visual de la aplicación de hospedaje.

> [RootVisualTarget](#rootvisualtarget) de objeto público

Este objeto visual es el lugar donde la vista en WebView conectará su árbol visual. La aplicación usa este objeto visual para posicionar la vista en la vista previa dentro de la aplicación. La aplicación aún debe usar la propiedad Bounds para cambiar el tamaño de la vista en WebView. La propiedad RootVisualTarget puede ser una IDCompositionVisual o Windows:: UI:: Composition:: ContainerVisual. WebView conectará su árbol visual al visual proporcionado antes de volver de la propiedad Setter. La aplicación debe confirmar en su dispositivo estableciendo la propiedad RootVisualTarget. La propiedad RootVisualTarget admite establecerse en nullptr para desconectar el WebView del árbol visual de la aplicación.

#### UIAProvider 

Devuelve el proveedor de automatización de la interfaz de usuario de WebView.

> [UIAProvider](#uiaprovider) de objeto público

#### CreateCoreWebView2PointerInfoFromPointerId 

Una función auxiliar para convertir una pointerId recibida del sistema en un CoreWebView2ExperimentalPointerInfo.

> Public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(uint PointerId, IntPtr ParentWindow, Matrix4x4 Transform)

parentWindow es el HWND que contiene WebView. Puede ser cualquier HWND en el árbol HWND que contenga la vista en vista previa. El CoreWebView2Matrix4x4 es la transformación de ese HWND a la vista de ventana. El CoreWebView2ExperimentalPointerInfo devuelto se usa en SendPointerInfo. El tipo de puntero debe ser pluma o entrada táctil, o la función dará un error.

#### SendMouseInput 

Si eventKind es CoreWebView2MouseEventKind. HorizontalWheel o CoreWebView2MouseEventKind. Wheel, mouseData especifica la cantidad de movimiento de la rueda.

> public void [SendMouseInput](#sendmouseinput)([CoreWebView2MouseEventKind](./namespace-microsoft-web-webview2-core.md) eventKind, [CoreWebView2MouseEventVirtualKeys](./namespace-microsoft-web-webview2-core.md) virtualKeys, uint mouseData, Point)

Un valor positivo indica que la rueda se giró hacia adelante, alejándose del usuario; un valor negativo indica que la rueda se ha girado hacia atrás, hacia el usuario. Un clic de rueda se define como WHEEL_DELTA, que es 120. Si eventKind es CoreWebView2MouseEventKind. XButtonDoubleClick CoreWebView2MouseEventKind. XButtonDown o CoreWebView2MouseEventKind. XButtonUp, mouseData especifica qué botones X se han presionado o se han soltado. Este valor debe ser 1 si se presiona o se suelta el primer botón X y 2 si se presiona o se suelta el segundo botón X. Si eventKind es CoreWebView2MouseEventKind. Leave, virtualKeys, mouseData y Point debe ser cero. Si eventKind es cualquier otro valor, mouseData debe ser cero. Se espera que el punto se sitúe en el espacio de coordenadas del cliente de la vista Web. Para hacer un seguimiento de los eventos del mouse que se inician en la WebView y pueden moverse fuera de la aplicación WebView y host, se recomienda llamar a SetCapture y ReleaseCapture. Para descartar los elementos emergentes activables, también se recomienda enviar mensajes de WM_MOUSELEAVE.

#### SendPointerInput 

SendPointerInput acepta la entrada de puntero táctil o de lápiz de los tipos definidos en CoreWebView2PointerEventKind.

> public void [SendPointerInput](#sendpointerinput)([CoreWebView2PointerEventKind](./namespace-microsoft-web-webview2-core.md) EventType, [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) pointerInfo)

Cualquier entrada de puntero del sistema debe convertirse en un CoreWebView2ExperimentalPointerInfo en primer lugar.

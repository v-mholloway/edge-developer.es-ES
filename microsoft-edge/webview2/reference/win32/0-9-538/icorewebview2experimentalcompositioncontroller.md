---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCompositionController
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalCompositionController
ms.openlocfilehash: e2b16cfd9095d43eb01d7e6233da2857c12a04ad
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880034"
---
# interfaz ICoreWebView2ExperimentalCompositionController 

> [!NOTE]
> Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.538.

```
interface ICoreWebView2ExperimentalCompositionController
  : public IUnknown
```

Esta interfaz es una extensión de la interfaz ICoreWebView2Controller para admitir hospedajes visuales.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[add_CursorChanged](#add_cursorchanged) | Agregue un controlador de eventos para el evento CursorChanged.
[CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid) | Una función auxiliar para convertir una pointerId recibida del sistema en un [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).
[get_Cursor](#get_cursor) | El cursor actual que la vista en WebView debe tener.
[get_RootVisualTarget](#get_rootvisualtarget) | El RootVisualTarget es un objeto visual en el árbol visual de la aplicación de hospedaje.
[get_UIAProvider](#get_uiaprovider) | Devuelve el proveedor de automatización de la interfaz de usuario de WebView.
[put_RootVisualTarget](#put_rootvisualtarget) | Establezca la propiedad RootVisualTarget.
[remove_CursorChanged](#remove_cursorchanged) | Quitar un controlador de eventos agregado previamente con add_CursorChanged.
[SendMouseInput](#sendmouseinput) | Si eventKind es COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL o COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData especifica la cantidad de movimiento de la rueda.
[SendPointerInput](#sendpointerinput) | SendPointerInput acepta la entrada del puntero táctil o de lápiz de los tipos definidos en COREWEBVIEW2_POINTER_EVENT_KIND.
[COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4) | Matriz que representa una transformación 3D.
[COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) | Tipo de evento del mouse usado por SendMouseInput para transmitir el tipo de evento del mouse que se envía a WebView.
[COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) | Teclas virtuales de eventos del mouse asociadas con un COREWEBVIEW2_MOUSE_EVENT_KIND para SendMouseInput.
[COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) | Tipo de evento de puntero usado por SendPointerInput para transmitir el tipo de evento de puntero que se envía a WebView.

Un objeto que implementa la interfaz ICoreWebView2ExperimentalCompositionController también implementará ICoreWebView2Controller. Se espera que las personas que llaman usen ICoreWebView2Controller para cambiar el tamaño, la visibilidad, el foco, etc., y, después, usar ICoreWebView2ExperimentalCompositionController para conectarse a un árbol de composición y proporcionar una entrada para la vista de la vista.

## Miembros

#### add_CursorChanged 

Agregue un controlador de eventos para el evento CursorChanged.

> [add_CursorChanged](#add_cursorchanged)de HRESULT público ([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) * EventHandler, EventRegistrationToken * token)

El evento se desencadena cuando WebView considera que se debe cambiar el cursor. Por ejemplo, cuando el cursor del mouse es actualmente el cursor predeterminado pero, después, se desplaza por el texto, puede intentar cambiar al cursor IBeam.

```cpp
        // Register a handler for the CursorChanged event.
        CHECK_FAILURE(m_compositionController->add_CursorChanged(
            Callback<ICoreWebView2ExperimentalCursorChangedEventHandler>(
                [this](ICoreWebView2ExperimentalCompositionController* sender,
                       IUnknown* args) -> HRESULT {
                    HCURSOR cursor;
                    CHECK_FAILURE(sender->get_Cursor(&cursor));
                    SetClassLongPtr(m_appWindow->GetMainWindow(), GCLP_HCURSOR, (LONG_PTR)cursor);
                    return S_OK;
                })
                .Get(),
            &m_cursorChangedToken));
```

#### CreateCoreWebView2PointerInfoFromPointerId 

Una función auxiliar para convertir una pointerId recibida del sistema en un [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).

> Public HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(uint POINTERID, HWND parentWindow, struct COREWEBVIEW2_MATRIX_4X4 Transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) * * pointerInfo)

parentWindow es el HWND que contiene WebView. Puede ser cualquier HWND en el árbol HWND que contenga la vista en vista previa. El COREWEBVIEW2_MATRIX_4X4 es la transformación de ese HWND a la vista de vista. El [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) devuelto se usa en SendPointerInfo. El tipo de puntero debe ser pluma o entrada táctil, o la función dará un error.



#### get_Cursor 

El cursor actual que la vista en WebView debe tener.

> [get_Cursor](#get_cursor)de HRESULT público (cursor HCURSOR *)

El cursor debe establecerse en WM_SETCURSOR a:: SetCursor o establecerse en el HWND primario/antecesor correspondiente de la vista en:: SetClassLongPtr. El HCURSOR se puede liberar, por lo que se recomienda CopyCursor/DestroyCursor para conservar su propia copia si hace más de lo que hay que establecer inmediatamente el cursor.

#### get_RootVisualTarget 

El RootVisualTarget es un objeto visual en el árbol visual de la aplicación de hospedaje.

> [get_RootVisualTarget](#get_rootvisualtarget)de HRESULT público (IUnknown * * Target)

Este objeto visual es el lugar donde la vista en WebView conectará su árbol visual. La aplicación usa este objeto visual para posicionar la vista en la vista previa dentro de la aplicación. La aplicación aún debe usar la propiedad Bounds para cambiar el tamaño de la vista en WebView. La propiedad RootVisualTarget puede ser una IDCompositionVisual o Windows:: UI:: Composition:: ContainerVisual. WebView conectará su árbol visual al visual proporcionado antes de volver de la propiedad Setter. La aplicación debe confirmar en su dispositivo estableciendo la propiedad RootVisualTarget. La propiedad RootVisualTarget admite establecerse en nullptr para desconectar el WebView del árbol visual de la aplicación. 
```cpp
            // Set the host app visual that the WebView will connect its visual
            // tree to.
            BuildDCompTreeUsingVisual();
            CHECK_FAILURE(m_compositionController->put_RootVisualTarget(m_dcompWebViewVisual.get()));
            CHECK_FAILURE(m_dcompDevice->Commit());
```

```cpp
// Create host app visual that the WebView will connect to.
//   - Create a IDCompositionTarget for the host window
//   - Create a visual and set that as the IDCompositionTarget's root
//   - Create another visual and add that to the IDCompositionTarget's root.
//     This visual will be the visual root for the WebView.
void ViewComponent::BuildDCompTreeUsingVisual()
{
    CHECK_FAILURE_BOOL(m_dcompDevice != nullptr);

    if (m_dcompWebViewVisual == nullptr)
    {
        CHECK_FAILURE(m_dcompDevice->CreateTargetForHwnd(
            m_appWindow->GetMainWindow(), TRUE, &m_dcompHwndTarget));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompRootVisual));
        CHECK_FAILURE(m_dcompHwndTarget->SetRoot(m_dcompRootVisual.get()));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompWebViewVisual));
        CHECK_FAILURE(m_dcompRootVisual->AddVisual(m_dcompWebViewVisual.get(), TRUE, nullptr));
    }
}
```

#### get_UIAProvider 

Devuelve el proveedor de automatización de la interfaz de usuario de WebView.

> [get_UIAProvider](#get_uiaprovider)de HRESULT público (IUnknown * *)

#### put_RootVisualTarget 

Establezca la propiedad RootVisualTarget.

> [put_RootVisualTarget](#put_rootvisualtarget)de HRESULT público (IUnknown * Target)

#### remove_CursorChanged 

Quitar un controlador de eventos agregado previamente con add_CursorChanged.

> [remove_CursorChanged](#remove_cursorchanged)de HRESULT público (token EventRegistrationToken)

#### SendMouseInput 

Si eventKind es COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL o COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData especifica la cantidad de movimiento de la rueda.

> [SENDMOUSEINPUT](#sendmouseinput)HRESULT público ([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UINT32 mouseData, Point)

Un valor positivo indica que la rueda se giró hacia adelante, alejándose del usuario; un valor negativo indica que la rueda se ha girado hacia atrás, hacia el usuario. Un clic de rueda se define como WHEEL_DELTA, que es 120. Si eventKind es COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN o COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, mouseData especifica qué botones X se han presionado o se han soltado. Este valor debe ser 1 si se presiona o se suelta el primer botón X y 2 si se presiona o se suelta el segundo botón X. Si eventKind es COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, virtualKeys, mouseData y Point deben ser cero. Si eventKind es cualquier otro valor, mouseData debe ser cero. Se espera que el punto se sitúe en el espacio de coordenadas del cliente de la vista Web. Para hacer un seguimiento de los eventos del mouse que se inician en la WebView y pueden moverse fuera de la aplicación WebView y host, se recomienda llamar a SetCapture y ReleaseCapture. Para descartar los elementos emergentes activables, también se recomienda enviar mensajes de WM_MOUSELEAVE. 
```cpp
bool ViewComponent::OnMouseMessage(UINT message, WPARAM wParam, LPARAM lParam)
{
    // Manually relay mouse messages to the WebView
    if (m_dcompDevice || m_wincompHelper)
    {
        POINT point;
        POINTSTOPOINT(point, lParam);
        if (message == WM_MOUSEWHEEL || message == WM_MOUSEHWHEEL)
        {
            // Mouse wheel messages are delivered in screen coordinates.
            // SendMouseInput expects client coordinates for the WebView, so convert
            // the point from screen to client.
            ::ScreenToClient(m_appWindow->GetMainWindow(), &point);
        }
        // Send the message to the WebView if the mouse location is inside the
        // bounds of the WebView, if the message is telling the WebView the
        // mouse has left the client area, or if we are currently capturing
        // mouse events.
        bool isMouseInWebView = PtInRect(&m_webViewBounds, point);
        if (isMouseInWebView || message == WM_MOUSELEAVE || m_isCapturingMouse)
        {
            DWORD mouseData = 0;

            switch (message)
            {
            case WM_MOUSEWHEEL:
            case WM_MOUSEHWHEEL:
                mouseData = GET_WHEEL_DELTA_WPARAM(wParam);
                break;
            case WM_XBUTTONDBLCLK:
            case WM_XBUTTONDOWN:
            case WM_XBUTTONUP:
                mouseData = GET_XBUTTON_WPARAM(wParam);
                break;
            case WM_MOUSEMOVE:
                if (!m_isTrackingMouse)
                {
                    // WebView needs to know when the mouse leaves the client area
                    // so that it can dismiss hover popups. TrackMouseEvent will
                    // provide a notification when the mouse leaves the client area.
                    TrackMouseEvents(TME_LEAVE);
                    m_isTrackingMouse = true;
                }
                break;
            case WM_MOUSELEAVE:
                m_isTrackingMouse = false;
                break;
            }

            // We need to capture the mouse in case the user drags the
            // mouse outside of the window bounds and we still need to send
            // mouse messages to the WebView process. This is useful for
            // scenarios like dragging the scroll bar or panning a map.
            // This is very similar to the Pointer Message case where a
            // press started inside of the WebView.
            if (message == WM_LBUTTONDOWN || message == WM_MBUTTONDOWN ||
                message == WM_RBUTTONDOWN || message == WM_XBUTTONDOWN)
            {
                if (isMouseInWebView && ::GetCapture() != m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = true;
                    ::SetCapture(m_appWindow->GetMainWindow());
                }
            }
            else if (message == WM_LBUTTONUP || message == WM_MBUTTONUP ||
                message == WM_RBUTTONUP || message == WM_XBUTTONUP)
            {
                if (::GetCapture() == m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = false;
                    ::ReleaseCapture();
                }
            }

            // Adjust the point from app client coordinates to webview client coordinates.
            // WM_MOUSELEAVE messages don't have a point, so don't adjust the point.
            if (message != WM_MOUSELEAVE)
            {
                point.x -= m_webViewBounds.left;
                point.y -= m_webViewBounds.top;
            }

            CHECK_FAILURE(m_compositionController->SendMouseInput(
                static_cast<COREWEBVIEW2_MOUSE_EVENT_KIND>(message),
                static_cast<COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS>(GET_KEYSTATE_WPARAM(wParam)),
                mouseData, point));
            return true;
        }
        else if (message == WM_MOUSEMOVE && m_isTrackingMouse)
        {
            // When the mouse moves outside of the WebView, but still inside the app
            // turn off mouse tracking and send the WebView a leave event.
            m_isTrackingMouse = false;
            TrackMouseEvents(TME_LEAVE | TME_CANCEL);
            OnMouseMessage(WM_MOUSELEAVE, 0, 0);
        }
    }
    return false;
}
```

#### SendPointerInput 

SendPointerInput acepta la entrada del puntero táctil o de lápiz de los tipos definidos en COREWEBVIEW2_POINTER_EVENT_KIND.

> HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) EventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) * pointerInfo)

Cualquier entrada de puntero del sistema debe convertirse en un [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) en primer lugar.

#### COREWEBVIEW2_MATRIX_4X4 

Matriz que representa una transformación 3D.

> typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)

Esta transformación se usa para calcular las coordenadas correctas al llamar a CreateCoreWebView2PointerInfoFromPointerId. Es equivalente a una D2D1_MATRIX_4X4_F

#### COREWEBVIEW2_MOUSE_EVENT_KIND 

Tipo de evento del mouse usado por SendMouseInput para transmitir el tipo de evento del mouse que se envía a WebView.

> [COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL            | Evento de desplazamiento horizontal de la rueda del mouse, WM_MOUSEHWHEEL.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK            | Botón izquierdo doble clic en evento de mouse, WM_LBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN            | Botón izquierdo de un evento de mouse, WM_LBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP            | Evento de botón arriba del botón izquierdo, WM_LBUTTONUP.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE            | Evento Leave de mouse, WM_MOUSELEAVE.
COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK            | Botón central doble clic en evento de mouse, WM_MBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN            | Botón central de mouse, WM_MBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP            | Evento de botón arriba del botón central, WM_MBUTTONUP.
COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE            | Evento de movimiento del mouse, WM_MOUSEMOVE.
COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK            | Botón secundario doble clic en el evento del mouse WM_RBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN            | Botón secundario del mouse, WM_RBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP            | Evento de botón arriba del botón secundario, WM_RBUTTONUP.
COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL            | Evento scroll de la rueda del mouse, WM_MOUSEWHEEL.
COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK            | Primer o segundo botón X haga doble clic en evento del mouse, WM_XBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN            | Primer o segundo evento de mouse en el botón X presionado, WM_XBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP            | Primer o segundo evento del botón X del botón arriba, WM_XBUTTONUP.

Los valores de esta enumeración se alinean con los mensajes de ventana WM_ * coincidentes.

#### COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS 

Teclas virtuales de eventos del mouse asociadas con un COREWEBVIEW2_MOUSE_EVENT_KIND para SendMouseInput.

> [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE            | No se han presionado teclas adicionales.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON            | El botón primario del mouse está presionado, MK_LBUTTON.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON            | El botón secundario del mouse está presionado, MK_RBUTTON.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT            | La tecla Mayús está presionada, MK_SHIFT.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL            | La tecla CTRL está presionada, MK_CONTROL.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON            | El botón central del mouse está presionado, MK_MBUTTON.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1            | El primer botón X está presionado, MK_XBUTTON1.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2            | El segundo botón X está presionado, MK_XBUTTON2.

Estos valores se pueden combinar en una marca de bit si se presiona más de una tecla virtual para el evento. Los valores de esta enumeración se alinean con las teclas de mouse * MK_ *.

#### COREWEBVIEW2_POINTER_EVENT_KIND 

Tipo de evento de puntero usado por SendPointerInput para transmitir el tipo de evento de puntero que se envía a WebView.

> [COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE            | Corresponde a WM_POINTERACTIVATE.
COREWEBVIEW2_POINTER_EVENT_KIND_DOWN            | Corresponde a WM_POINTERDOWN.
COREWEBVIEW2_POINTER_EVENT_KIND_ENTER            | Corresponde a WM_POINTERENTER.
COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE            | Corresponde a WM_POINTERLEAVE.
COREWEBVIEW2_POINTER_EVENT_KIND_UP            | Corresponde a WM_POINTERUP.
COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE            | Corresponde a WM_POINTERUPDATE.

Los valores de esta enumeración se alinean con los mensajes de ventana WM_POINTER * coincidentes.


---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2Controller
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 8e0f95f8346f4c4b60b6de2676503b79c743afcb
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880825"
---
# 0.9.515: ICoreWebView2Controller 

> [!NOTE]
> Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515. Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.

```
interface ICoreWebView2Controller
  : public IUnknown
```

Esta interfaz es el propietario del objeto CoreWebView2 y proporciona compatibilidad para cambiar el tamaño, mostrar y ocultar, enfocar y otras funciones relacionadas con la ventana y la composición.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[add_AcceleratorKeyPressed](#add_acceleratorkeypressed) | Agregue un controlador de eventos para el evento AcceleratorKeyPressed.
[add_GotFocus](#add_gotfocus) | Agregue un controlador de eventos para el evento GotFocus.
[add_LostFocus](#add_lostfocus) | Agregue un controlador de eventos para el evento LostFocus.
[add_MoveFocusRequested](#add_movefocusrequested) | Agregue un controlador de eventos para el evento MoveFocusRequested.
[add_ZoomFactorChanged](#add_zoomfactorchanged) | Agregue un controlador de eventos para el evento ZoomFactorChanged.
[Cerrar](#close) | Cierra WebView y limpia la instancia de explorador subyacente.
[get_Bounds](#get_bounds) | Los límites de la vista previa.
[get_CoreWebView2](#get_corewebview2) | Obtiene el CoreWebView2 asociado a este CoreWebView2Controller.
[get_IsVisible](#get_isvisible) | La propiedad IsVisible determina si se muestra u oculta la vista en WebView.
[get_ParentWindow](#get_parentwindow) | La ventana principal proporcionada por la aplicación que esta vista previa usa para representar contenido.
[get_ZoomFactor](#get_zoomfactor) | El factor de zoom para la vista de WebView.
[MoveFocus](#movefocus) | Mover el foco a WebView.
[NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged) | Esta es una notificación independiente de los límites que informa a WebView de que se ha movido su HWND primario (o cualquier antecesor).
[put_Bounds](#put_bounds) | Establezca la propiedad Bounds.
[put_IsVisible](#put_isvisible) | Establezca la propiedad IsVisible.
[put_ParentWindow](#put_parentwindow) | Establezca la ventana principal de la vista en WebView.
[put_ZoomFactor](#put_zoomfactor) | Establezca la propiedad ZoomFactor.
[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed) | Quitar un controlador de eventos agregado previamente con add_AcceleratorKeyPressed.
[remove_GotFocus](#remove_gotfocus) | Quitar un controlador de eventos agregado previamente con add_GotFocus.
[remove_LostFocus](#remove_lostfocus) | Quitar un controlador de eventos agregado previamente con add_LostFocus.
[remove_MoveFocusRequested](#remove_movefocusrequested) | Quitar un controlador de eventos agregado previamente con add_MoveFocusRequested.
[remove_ZoomFactorChanged](#remove_zoomfactorchanged) | Quitar un controlador de eventos agregado previamente con add_ZoomFactorChanged.
[SetBoundsAndZoomFactor](#setboundsandzoomfactor) | Actualice las propiedades Bounds y ZoomFactor al mismo tiempo.

El CoreWebView2Controller es propietario de la CoreWebView2 y, si todas las referencias a CoreWebView2Controller desaparecen, se cerrará la WebView.

## Miembros

#### add_AcceleratorKeyPressed 

Agregue un controlador de eventos para el evento AcceleratorKeyPressed.

> [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)de HRESULT público ([ICoreWebView2AcceleratorKeyPressedEventHandler](icorewebview2acceleratorkeypressedeventhandler.md) * EventHandler, EventRegistrationToken * token)

AcceleratorKeyPressed se desencadena cuando se presiona o se suelta una tecla de aceleración o un combinado de teclas mientras la vista de la vista en WebView está activa. Una clave se considera un acelerador si:

1. La tecla Ctrl o Alt se está retenida actualmente, o bien

1. la tecla presionada no se asigna a un carácter. Algunas teclas específicas nunca se consideran aceleradores, como Mayús. La tecla de escape se considera siempre un acelerador.

Los eventos de teclas autorepetidos que se provocan al mantener presionada la tecla también desencadenan este evento. Puedes filtrarlos comprobando los argumentos del evento ' KeyEventLParam o PhysicalKeyStatus.

En el modo de ventana, se llama a este controlador de eventos de forma sincrónica. Hasta que llames al controlador () en los argumentos del evento o se devuelva el controlador de eventos, el proceso del explorador se bloqueará y las llamadas COM salientes entre procesos generarán un error con RPC_E_CANTCALLOUT_ININPUTSYNCCALL. Sin embargo, todos los métodos de la API de CoreWebView2 funcionarán.

En el modo sin ventana, se llama al controlador de eventos de forma asincrónica. La entrada de datos adicionales no llegará al explorador hasta que el controlador de eventos devuelva o se llame a (), pero el proceso del explorador en sí no se bloqueará y las llamadas COM salientes funcionarán normalmente.

Se recomienda que llame al controlador (TRUE) tan pronto como sepa que desea controlar la tecla de aceleración.

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_controller->add_AcceleratorKeyPressed(
        Callback<ICoreWebView2AcceleratorKeyPressedEventHandler>(
            [this](
                ICoreWebView2Controller* sender,
                ICoreWebView2AcceleratorKeyPressedEventArgs* args) -> HRESULT {
                COREWEBVIEW2_KEY_EVENT_KIND kind;
                CHECK_FAILURE(args->get_KeyEventKind(&kind));
                // We only care about key down events.
                if (kind == COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN ||
                    kind == COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN)
                {
                    UINT key;
                    CHECK_FAILURE(args->get_VirtualKey(&key));
                    // Check if the key is one we want to handle.
                    if (std::function<void()> action =
                            m_appWindow->GetAcceleratorKeyFunction(key))
                    {
                        // Keep the browser from handling this key, whether it's autorepeated or
                        // not.
                        CHECK_FAILURE(args->put_Handled(TRUE));

                        // Filter out autorepeated keys.
                        COREWEBVIEW2_PHYSICAL_KEY_STATUS status;
                        CHECK_FAILURE(args->get_PhysicalKeyStatus(&status));
                        if (!status.WasKeyDown)
                        {
                            // Perform the action asynchronously to avoid blocking the
                            // browser process's event queue.
                            m_appWindow->RunAsync(action);
                        }
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_acceleratorKeyPressedToken));
```

#### add_GotFocus 

Agregue un controlador de eventos para el evento GotFocus.

> [add_GotFocus](#add_gotfocus)de HRESULT público ([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) * EventHandler, EventRegistrationToken * token)

GotFocus se desencadena cuando WebView tiene el foco.

#### add_LostFocus 

Agregue un controlador de eventos para el evento LostFocus.

> [add_LostFocus](#add_lostfocus)de HRESULT público ([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) * EventHandler, EventRegistrationToken * token)

LostFocus se desencadena cuando WebView pierde el foco. En caso de que se inicie el evento MoveFocusRequested, el foco seguirá en la vista previa cuando se desencadene el evento MoveFocusRequested. Perder el foco solo se activa cuando el código de la aplicación o la acción predeterminada del evento MoveFocusRequested está lejos de WebView.

#### add_MoveFocusRequested 

Agregue un controlador de eventos para el evento MoveFocusRequested.

> [add_MoveFocusRequested](#add_movefocusrequested)de HRESULT público ([ICoreWebView2MoveFocusRequestedEventHandler](icorewebview2movefocusrequestedeventhandler.md) * EventHandler, EventRegistrationToken * token)

MoveFocusRequested se activa cuando el usuario intenta usar la tecla TAB fuera de la vista. El foco de la vista de WebView no ha cambiado cuando se desencadena este evento.

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_controller->add_MoveFocusRequested(
        Callback<ICoreWebView2MoveFocusRequestedEventHandler>(
            [this](
                ICoreWebView2Controller* sender,
                ICoreWebView2MoveFocusRequestedEventArgs* args) -> HRESULT {
                if (!g_autoTabHandle)
                {
                    COREWEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
                    {
                        TabBackwards(int(m_tabbableWindows.size()));
                    }
                    CHECK_FAILURE(args->put_Handled(TRUE));
                }
                return S_OK;
            })
            .Get(),
        &m_moveFocusRequestedToken));
```

#### add_ZoomFactorChanged 

Agregue un controlador de eventos para el evento ZoomFactorChanged.

> [add_ZoomFactorChanged](#add_zoomfactorchanged)de HRESULT público ([ICoreWebView2ZoomFactorChangedEventHandler](icorewebview2zoomfactorchangedeventhandler.md) * EventHandler, EventRegistrationToken * token)

El evento se desencadena cuando cambia la propiedad ZoomFactor de la vista de vista previa. El evento se podría activar porque el autor de la llamada modificó la propiedad ZoomFactor o debido a que el usuario modificaba manualmente el zoom. Cuando el autor de la llamada lo modifica a través de la propiedad ZoomFactor, el factor de zoom interno se actualiza inmediatamente y no se producirá ningún evento ZoomFactorChanged. La vista Web asocia el último factor de zoom usado para cada sitio. Por lo tanto, es posible que el factor de zoom cambie al navegar a una página diferente. Cuando el factor de zoom cambia debido a esto, el evento ZoomFactorChanged se activa justo después del evento ContentLoading.

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_controller->add_ZoomFactorChanged(
        Callback<ICoreWebView2ZoomFactorChangedEventHandler>(
            [this](ICoreWebView2Controller* sender, IUnknown* args) -> HRESULT {
                double zoomFactor;
                CHECK_FAILURE(sender->get_ZoomFactor(&zoomFactor));

                std::wstring message = L"WebView2APISample (Zoom: " +
                                       std::to_wstring(int(zoomFactor * 100)) + L"%)";
                SetWindowText(m_appWindow->GetMainWindow(), message.c_str());
                return S_OK;
            })
            .Get(),
        &m_zoomFactorChangedToken));
```

#### Cerrar 

Cierra WebView y limpia la instancia de explorador subyacente.

> HRESULT público [Close](#close)()

La limpieza de la instancia del explorador liberará los recursos que se encienden en la vista Web. La instancia del explorador se cerrará si no hay ninguna otra vista previa con ella.

Después de llamar a Close, todas las llamadas a métodos producirán errores y los controladores de eventos dejarán de activarse. Específicamente, la WebView liberará sus referencias a los controladores de eventos cuando se llama a Close.

Close se llama de forma implícita cuando CoreWebView2Controller pierde su referencia final y se destruye. Sin embargo, se recomienda llamar de forma explícita a Close para evitar cualquier ciclo de referencias entre la vista de WebView y el código de la aplicación. En concreto, si capturas una referencia a la vista de la vista en un controlador de eventos, crearás un ciclo de referencia entre la vista en WebView y el controlador de eventos. Al llamar a Close se interrumpirá este ciclo liberando todos los controladores de eventos. Pero para evitar esta situación, lo mejor es llamar explícitamente a Close en WebView y no capturar una referencia a WebView para asegurarte de que la WebView pueda limpiarse correctamente.

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView(bool cleanupUserDataFolder)
{
    DeleteAllComponents();
    if (m_controller)
    {
        m_controller->Close();
        m_controller = nullptr;
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
    if (cleanupUserDataFolder)
    {
        // For non-UWP apps, the default user data folder {Executable File Name}.WebView2
        // is in the same directory next to the app executable. If end
        // developers specify userDataFolder during WebView environment
        // creation, they would need to pass in that explicit value here.
        // For more information about userDataFolder:
        // https://docs.microsoft.com/microsoft-edge/hosting/webview2/reference/win32/0-9-488/webview2-idl#createwebview2environmentwithoptions
        WCHAR userDataFolder[MAX_PATH] = L"";
        // Obtain the absolute path for relative paths that include "./" or "../"
        _wfullpath(
            userDataFolder, GetLocalPath(L"WebView2APISample.exe.WebView2").c_str(), MAX_PATH);
        std::wstring userDataFolderPath(userDataFolder);

        std::wstring message = L"Are you sure you want to clean up the user data folder at\n";
        message += userDataFolderPath;
        message += L"\n?\nWarning: This action is not reversible.\n\n";
        message += L"Click No if there are other open WebView instances.\n";

        if (MessageBox(m_mainWindow, message.c_str(), L"Cleanup User Data Folder", MB_YESNO) ==
            IDYES)
        {
            CHECK_FAILURE(DeleteFileRecursive(userDataFolderPath));
        }
    }
}
```

#### get_Bounds 

Los límites de la vista previa.

> [get_Boundss](#get_bounds)HRESULT públicos (límites Rect *)

Los límites son relativos al identificador HWND primario. La aplicación tiene dos formas en las que puede ubicar una vista en WebView:

1. Cree un HWND secundario que sea el objeto HWND de la vista < View. Coloque esta ventana donde debería estar la vista en la vista. En este caso, use (0,0) para la Bound's esquina superior izquierda de la vista de vista previa (el desplazamiento).

1. Use la última ventana de la aplicación como el HWND primario de WebView. Establezca la Bound's esquina superior izquierda de la vista previa para que la vista de la vista en la aplicación se coloque correctamente en la aplicación. Los valores de la entrada enlazada están en el espacio de coordenadas del host.

#### get_CoreWebView2 

Obtiene el CoreWebView2 asociado a este CoreWebView2Controller.

> [get_CoreWebView2](#get_corewebview2)(HRESULT) público ([ICoreWebView2](icorewebview2.md) * * CoreWebView2)

#### get_IsVisible 

La propiedad IsVisible determina si se muestra u oculta la vista en WebView.

> HRESULT público [get_IsVisible](#get_isvisible)(bool * IsVisible)

Si IsVisible se establece en false, WebView será transparente y no se representará. Sin embargo, esto no afectará a la ventana que contenga la vista de contenido (el parámetro HWND pasado a CreateCoreWebView2Controller). Si desea que esta ventana desaparezca también, llame a ShowWindow directamente, además de modificar la propiedad IsVisible. Si la ventana superior está minimizada o restaurada, WebView no recibirá mensajes de ventana. Por motivos de rendimiento, desarrollador debe establecer el valor de la propiedad IsVisible de la WebView en falso cuando la ventana de la aplicación está minimizada y volver a ser true cuando se restaura la ventana de la aplicación. La ventana de la aplicación puede hacerlo controlando SC_MINIMIZE y SC_RESTORE comando al recibir WM_SYSCOMMAND mensaje.

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_controller->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_controller->put_IsVisible(m_isVisible);
}
```

#### get_ParentWindow 

La ventana principal proporcionada por la aplicación que esta vista previa usa para representar contenido.

> [get_ParentWindow](#get_parentwindow)de HRESULT público (HWND * topLevelWindow)

Esta API inicialmente devuelve la ventana que se pasó a CreateCoreWebView2Controller.

#### get_ZoomFactor 

El factor de zoom para la vista de WebView.

> [get_ZoomFactor](#get_zoomfactor)de HRESULT público (Double * ZoomFactor)

Ten en cuenta que cambiar el factor de zoom podría provocar un `window.innerWidth/innerHeight` cambio en el diseño de página. Un factor de zoom aplicado por el host mediante una llamada a ZoomFactor se convierte en el nuevo zoom predeterminado para la vista de la vista en WebView. Este factor de zoom se aplica en la navegación y se vuelve al factor de zoom en la vista previa cuando el usuario presiona Ctrl + 0. Cuando el usuario cambia el factor de zoom (es decir, la aplicación que recibe la ZoomFactorChanged), ese zoom solo se aplica a la página actual. Cualquier zoom aplicado a un usuario solo es para la página actual y se restablece en una navegación. No se permite especificar un zoomFactor menor o igual que 0. WebView también tiene un intervalo de factor de zoom compatible interno. Cuando un factor de zoom especificado está fuera de ese rango, se normalizará para que esté dentro del rango y se desencadenará un evento ZoomFactorChanged para el factor de zoom aplicado real. Cuando se produzca esta normalización de rango, la propiedad ZoomFactor informará sobre el factor de zoom especificado durante la modificación anterior de la propiedad ZoomFactor hasta que se reciba el evento ZoomFactorChanged después de que la vista previa aplique el factor de zoom normalizado.

#### MoveFocus 

Mover el foco a WebView.

> [MOVEFOCUS](#movefocus)HRESULT público (razón COREWEBVIEW2_MOVE_FOCUS_REASON)

La vista web obtendrá el foco y el foco se establecerá en el elemento de corresponsal de la página hospedada en la vista Web. Por motivos de programación, el foco se establece en elemento con enfoque anterior o en el elemento predeterminado si no hay ningún elemento con el foco anterior. Por el siguiente motivo, el foco se establece en el primer elemento. Por el motivo anterior, el foco se establece en el último elemento. WebView también puede obtener el foco a través de la interacción del usuario, como hacer clic en la vista previa o en la pestaña en la misma. Para la tabulación, la aplicación puede llamar a MoveFocus con la función siguiente o anterior para alinear con la tabulación y Mayús + Tab, respectivamente al decidir la vista previa del elemento tabulador. O bien, la aplicación puede llamar a IsDialogMessage como parte de su bucle de mensajes para permitir que la plataforma maneje automáticamente la tabulación. La plataforma girará en todas las ventanas con WS_TABSTOP. Cuando la vista de la vista de la vista de IsDialogMessage, coloca internamente el foco en el primer o el último elemento de Tab y Mayús + Tab, respectivamente.

```cpp
    while (GetMessage(&msg, nullptr, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            // Calling IsDialogMessage handles Tab traversal automatically. If the
            // app wants the platform to auto handle tab, then call IsDialogMessage
            // before calling TranslateMessage/DispatchMessage. If the app wants to
            // handle tabbing itself, then skip calling IsDialogMessage and call
            // TranslateMessage/DispatchMessage directly.
            if (!g_autoTabHandle || !IsDialogMessage(GetAncestor(msg.hwnd, GA_ROOT), &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }
```

```cpp
        if (wParam == VK_TAB)
        {
            // Find out if the window is one we've customized for tab handling
            for (size_t i = 0; i < m_tabbableWindows.size(); i++)
            {
                if (m_tabbableWindows[i].first == hWnd)
                {
                    if (GetKeyState(VK_SHIFT) < 0)
                    {
                        TabBackwards(i);
                    }
                    else
                    {
                        TabForwards(i);
                    }
                    return true;
                }
            }
        }
```

```cpp
void ControlComponent::TabForwards(int currentIndex)
{
    // Find first enabled window after the active one
    for (size_t i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_controller->MoveFocus(COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT);
}

void ControlComponent::TabBackwards(int currentIndex)
{
    // Find first enabled window before the active one
    for (int i = currentIndex - 1; i >= 0; i--)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    CHECK_FAILURE(m_controller->MoveFocus(COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### NotifyParentWindowPositionChanged 

Esta es una notificación independiente de los límites que informa a WebView de que se ha movido su HWND primario (o cualquier antecesor).

> [NOTIFYPARENTWINDOWPOSITIONCHANGED](#notifyparentwindowpositionchanged)HRESULT público ()

Esto es necesario para que la accesibilidad y determinados cuadros de diálogo de WebView funcionen correctamente. 
```cpp
    if (message == WM_MOVE || message == WM_MOVING)
    {
        m_controller->NotifyParentWindowPositionChanged();
        return true;
    }
```

#### put_Bounds 

Establezca la propiedad Bounds.

> [put_Bounds](#put_bounds)de HRESULT público (límites Rect)

```cpp
// Update the bounds of the WebView window to fit available space.
void ViewComponent::ResizeWebView()
{
    SIZE webViewSize = {
            LONG((m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio * m_webViewScale),
            LONG((m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio * m_webViewScale) };

    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        webViewSize.cy + m_webViewBounds.top);
    desiredBounds.right = LONG(
        webViewSize.cx + m_webViewBounds.left);

    m_controller->put_Bounds(desiredBounds);
    if (m_compositionController)
    {
        POINT webViewOffset = {m_webViewBounds.left, m_webViewBounds.top};

        if (m_dcompDevice)
        {
            CHECK_FAILURE(m_dcompRootVisual->SetOffsetX(float(webViewOffset.x)));
            CHECK_FAILURE(m_dcompRootVisual->SetOffsetY(float(webViewOffset.y)));
            CHECK_FAILURE(m_dcompRootVisual->SetClip(
                {0, 0, float(webViewSize.cx), float(webViewSize.cy)}));
            CHECK_FAILURE(m_dcompDevice->Commit());
        }
        else if (m_wincompHelper)
        {
            m_wincompHelper->UpdateSizeAndPosition(webViewOffset, webViewSize);
        }
    }
}
```

#### put_IsVisible 

Establezca la propiedad IsVisible.

> [put_IsVisible](#put_isvisible)de HRESULT público (bool IsVisible)

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_controller->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_controller->put_IsVisible(TRUE);
            }
        }
    }
```

#### put_ParentWindow 

Establezca la ventana principal de la vista en WebView.

> [put_ParentWindow](#put_parentwindow)de HRESULT público (HWND topLevelWindow)

Esto hará que la vista de ventana reorigen su ventana a la ventana recién suministrada.

#### put_ZoomFactor 

Establezca la propiedad ZoomFactor.

> [put_ZoomFactor](#put_zoomfactor)de HRESULT público (Double ZoomFactor)

#### remove_AcceleratorKeyPressed 

Quitar un controlador de eventos agregado previamente con add_AcceleratorKeyPressed.

> [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)de HRESULT público (token EventRegistrationToken)

#### remove_GotFocus 

Quitar un controlador de eventos agregado previamente con add_GotFocus.

> [remove_GotFocus](#remove_gotfocus)de HRESULT público (token EventRegistrationToken)

#### remove_LostFocus 

Quitar un controlador de eventos agregado previamente con add_LostFocus.

> [remove_LostFocus](#remove_lostfocus)de HRESULT público (token EventRegistrationToken)

#### remove_MoveFocusRequested 

Quitar un controlador de eventos agregado previamente con add_MoveFocusRequested.

> [remove_MoveFocusRequested](#remove_movefocusrequested)de HRESULT público (token EventRegistrationToken)

#### remove_ZoomFactorChanged 

Quitar un controlador de eventos agregado previamente con add_ZoomFactorChanged.

> [remove_ZoomFactorChanged](#remove_zoomfactorchanged)de HRESULT público (token EventRegistrationToken)

#### SetBoundsAndZoomFactor 

Actualice las propiedades Bounds y ZoomFactor al mismo tiempo.

> HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(rectángulos de rectángulo, doble zoomFactor)

Esta operación es atómica desde la perspectiva del anfitrión. Después de volver de esta función, las propiedades Bounds y ZoomFactor se actualizarán si la función se realiza correctamente, o no se actualizará si se produce un error en la función. Si los límites y ZoomFactor se actualizan con la misma escala (es decir, los límites y ZoomFactor están duplicados), la página no verá un cambio en la ventana. innerWidth/innerHeight y la WebView representará el contenido en el nuevo tamaño y zoom sin representaciones intermedias. Esta función también se puede usar para actualizar solo una de ZoomFactor o límites pasando el nuevo valor para uno y el valor actual para el otro.

```cpp
void ViewComponent::SetScale(float scale)
{
    RECT bounds;
    CHECK_FAILURE(m_controller->get_Bounds(&bounds));
    double scaleChange = scale / m_webViewScale;

    bounds.bottom = LONG(
        (bounds.bottom - bounds.top) * scaleChange + bounds.top);
    bounds.right = LONG(
        (bounds.right - bounds.left) * scaleChange + bounds.left);

    m_webViewScale = scale;
    m_controller->SetBoundsAndZoomFactor(bounds, scale);
}
```


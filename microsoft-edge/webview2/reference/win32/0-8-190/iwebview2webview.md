---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 5c84cfb703c8901560307b7bba8bc7887cb19377
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655078"
---
# interfaz IWebView2WebView 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface IWebView2WebView
  : public IUnknown
```

WebView2 le permite hospedar contenido web con la tecnología de explorador Web más reciente.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Settings](#get_settings) | El objeto [IWebView2Settings](IWebView2Settings.md) contiene varios valores modificables para la vista de vista de contenido para la vista de contenido.
[get_Source](#get_source) | Identificador URI del documento de nivel superior actual.
[Busque](#navigate) | Hacer que la navegación del documento de nivel superior sea la dirección URI especificada.
[MoveFocus](#movefocus) | Mover el foco a WebView.
[NavigateToString](#navigatetostring) | Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.
[add_NavigationStarting](#add_navigationstarting) | Agregue un controlador de eventos para el evento NavigationStarting.
[remove_NavigationStarting](#remove_navigationstarting) | Quitar un controlador de eventos agregado previamente con add_NavigationStarting.
[add_DocumentStateChanged](#add_documentstatechanged) | Agregue un controlador de eventos para el evento DocumentStateChanged.
[remove_DocumentStateChanged](#remove_documentstatechanged) | Quitar un controlador de eventos agregado previamente con add_DocumentStateChanged.
[add_NavigationCompleted](#add_navigationcompleted) | Agregue un controlador de eventos para el evento NavigationCompleted.
[remove_NavigationCompleted](#remove_navigationcompleted) | Quitar un controlador de eventos agregado previamente con add_NavigationCompleted.
[add_FrameNavigationStarting](#add_framenavigationstarting) | Agregue un controlador de eventos para el evento FrameNavigationStarting.
[remove_FrameNavigationStarting](#remove_framenavigationstarting) | Quitar un controlador de eventos agregado previamente con add_FrameNavigationStarting.
[add_MoveFocusRequested](#add_movefocusrequested) | Agregue un controlador de eventos para el evento MoveFocusRequested.
[remove_MoveFocusRequested](#remove_movefocusrequested) | Quitar un controlador de eventos agregado previamente con add_MoveFocusRequested.
[add_GotFocus](#add_gotfocus) | Agregue un controlador de eventos para el evento GotFocus.
[remove_GotFocus](#remove_gotfocus) | Quitar un controlador de eventos agregado previamente con add_GotFocus.
[add_LostFocus](#add_lostfocus) | Agregue un controlador de eventos para el evento LostFocus.
[remove_LostFocus](#remove_lostfocus) | Quitar un controlador de eventos agregado previamente con add_LostFocus.
[add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated) | Esta API estará en desuso; usa la nueva API de add_WebResourceRequested.
[remove_WebResourceRequested](#remove_webresourcerequested) | Quitar un controlador de eventos agregado previamente con add_WebResourceRequested.
[add_ScriptDialogOpening](#add_scriptdialogopening) | Agregue un controlador de eventos para el evento ScriptDialogOpening.
[remove_ScriptDialogOpening](#remove_scriptdialogopening) | Quitar un controlador de eventos agregado previamente con add_ScriptDialogOpening.
[add_ZoomFactorChanged](#add_zoomfactorchanged) | Agregue un controlador de eventos para el evento ZoomFactorChanged.
[remove_ZoomFactorChanged](#remove_zoomfactorchanged) | Quitar un controlador de eventos agregado previamente con add_ZoomFactorChanged.
[add_PermissionRequested](#add_permissionrequested) | Agregue un controlador de eventos para el evento PermissionRequested.
[remove_PermissionRequested](#remove_permissionrequested) | Quitar un controlador de eventos agregado previamente con add_PermissionRequested.
[add_ProcessFailed](#add_processfailed) | Agregue un controlador de eventos para el evento ProcessFailed.
[remove_ProcessFailed](#remove_processfailed) | Quitar un controlador de eventos agregado previamente con add_ProcessFailed.
[AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated) | Agregue el JavaScript proporcionado a una lista de scripts que se deben ejecutar después de que se haya creado el objeto global, pero antes de que se haya analizado el documento HTML y antes de que se ejecute cualquier otro script incluido en el documento HTML.
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | Quite el JavaScript correspondiente agregado a través de AddScriptToExecuteOnDocumentCreated.
[ExecuteScript](#executescript) | Ejecute el código JavaScript desde el parámetro de JavaScript en el documento de nivel superior actual representado en la vista de vistas en WebView.
[CapturePreview](#capturepreview) | Capture una imagen de lo que se muestra en la vista de página.
[Volver a cargar](#reload) | Volver a cargar la página actual.
[get_Bounds](#get_bounds) | Los límites de la vista previa.
[put_Bounds](#put_bounds) | Establezca la propiedad Bounds.
[get_ZoomFactor](#get_zoomfactor) | El factor de zoom para la página actual en la vista Web.
[put_ZoomFactor](#put_zoomfactor) | Establezca la propiedad ZoomFactor.
[get_IsVisible](#get_isvisible) | La propiedad IsVisible determina si se muestra u oculta la vista en WebView.
[put_IsVisible](#put_isvisible) | Establezca la propiedad IsVisible.
[PostWebMessageAsJson](#postwebmessageasjson) | Publique el mensaje webmensaje especificado en el documento de nivel superior de este [IWebView2WebView]().
[PostWebMessageAsString](#postwebmessageasstring) | Este es un auxiliar para publicar un mensaje que es una cadena simple en lugar de una representación de cadena JSON de un objeto de JavaScript.
[add_WebMessageReceived](#add_webmessagereceived) | Este evento se desencadena cuando se establece la configuración de IsWebMessageEnabled y el documento de nivel superior de las llamadas de WebView `window.chrome.webview.postMessage` .
[remove_WebMessageReceived](#remove_webmessagereceived) | Quitar un controlador de eventos agregado previamente con add_WebMessageReceived.
[Cerrar](#close) | Cierra WebView y limpia la instancia de explorador subyacente.
[CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod) | Llama a un método DevToolsProtocol asincrónico.
[add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived) | Suscribirse a un evento de DevToolsProtocol.
[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived) | Quitar un controlador de eventos agregado previamente con add_DevToolsProtocolEventReceived.
[get_BrowserProcessId](#get_browserprocessid) | El identificador de proceso del proceso del explorador que hospeda la vista Web.
[get_CanGoBack](#get_cangoback) | Puede navegar por la vista Web a la página anterior del historial de navegación.
[get_CanGoForward](#get_cangoforward) | Puede navegar por la vista Web a la página siguiente del historial de navegación.
[GoBack](#goback) | Navega por la vista Web a la página anterior del historial de navegación.
[GoForward](#goforward) | Navega por la vista Web a la página siguiente del historial de navegación.
[WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) | Formato de imagen usado por el método [IWebView2WebView:: CapturePreview](#capturepreview) .
[WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind) | Cuadro de diálogo tipo de JavaScript usado en la interfaz [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) .
[WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind) | Tipo de error de proceso usado en la interfaz de [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) .
[WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type) | El tipo de una solicitud de permiso.
[WEBVIEW2_PERMISSION_STATE](#webview2_permission_state) | Respuesta a una solicitud de permiso.
[WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) | Motivo de mover el foco.
[WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status) | Valores de estado de error para navegaciones Web.
[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) | Enumeración de contextos de solicitud de recursos Web.

## Eventos de navegación

La secuencia normal de eventos de navegación es NavigationStarting, DocumentStateChanged y, después, NavigationCompleted.

![DOT-inline-dotgraph-1. png](media/dot-inline-dotgraph-1.png)

Ten en cuenta que esto es para los eventos de navegación con el mismo evento NavigationId. Los eventos de navegación con diferentes argumentos de evento de NavigationId se pueden solapar. Por ejemplo, si inicia una espera de navegación para su evento NavigationStarting y, a continuación, inicia otra navegación, verá el NavigationStarting para la primera navegación, seguida de la NavigationStarting del segundo Navigate, seguido de la NavigationCompleted de la primera navegación y, a continuación, todos los demás eventos de navegación correspondientes para la segunda navegación. En casos de error puede haber o no un evento DocumentStateChanged dependiendo de si la navegación continúa o no en una página de error. En el caso de una redirección HTTP, habrá varios eventos NavigationStarting en una fila, y los siguientes tendrán establecido el marcador IsRedirect.

Para los submarcos dentro de WebView, el único evento de navegación desencadenado es el evento NavigationStarting, que proporciona a los host la capacidad de bloquear la navegación de los submarcos.

## Modelo de proceso

WebView2 usa el mismo modelo de proceso que el explorador Web de Edge. Hay un proceso de explorador Edge por cada directorio de datos de usuario especificado en una sesión de usuario que servirá a cualquier proceso de llamada de WebView2 que especifique el directorio de datos de usuario. Esto significa que un proceso del navegador Edge puede estar atendiendo varios procesos de llamadas y un proceso de llamada puede estar usando varios procesos de explorador.

![DOT-inline-dotgraph-2. png](media/dot-inline-dotgraph-2.png)

Fuera de un proceso de explorador, habrá varios procesos de representación. Estos se crean según sea necesario para dar servicio a varios marcos que se encuentren en diferentes vistas previas. La cantidad de procesos de representación varía en función de la característica de explorador de aislamiento del sitio y la cantidad de orígenes distintos desconectados representados en las vistas de web asociadas.

![DOT-inline-dotgraph-3. png](media/dot-inline-dotgraph-3.png)

Puede reaccionar ante los bloqueos y los bloqueos en estos procesos del explorador y el representador mediante el evento ProcessFailure.

Puede apagar de forma segura los procesos del explorador y el representador asociados con el método Close.

## Modelo de subprocesos

El WebView2 debe crearse en un subproceso de interfaz de usuario. Específicamente un hilo con un bombeo de mensajes. Todas las devoluciones de llamada se producirán en ese subproceso y las llamadas a la vista en WebView deberán realizarse en ese subproceso. No es seguro usar la vista en WebView desde otro subproceso.

Las devoluciones de llamada, incluidos los controladores de eventos y los controladores de finalización, se ejecutan en serie. Es decir, si tiene un controlador de eventos ejecutándose y comienza un bucle de mensaje, no se empezarán a ejecutar de forma reentrante otros controladores de eventos o devoluciones de llamada de finalización.

## Seguridad

Comprueba siempre la propiedad de origen de WebView antes de usar ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString o cualquier otro método para enviar información a WebView. Es posible que la vista Web haya navegado a otra página a través del usuario final interactuando con la página o script de la página que provoca la navegación. Del mismo modo, preste mucha atención a AddScriptToExecuteOnDocumentCreated. Todas las navegaciones futuras ejecutarán esta secuencia de comandos y si proporciona acceso a información dirigida únicamente a un determinado origen, cualquier documento HTML puede tener acceso.

Al examinar el resultado de una llamada a un método ExecuteScript, un evento de WebMessageReceived, comprobar siempre el origen del remitente o cualquier otro mecanismo de recepción de la información de un documento HTML en una vista previa valide el URI del documento HTML es el que espera.

Al construir un mensaje para enviarlo a un WebView, prefiere usar PostWebMessageAsJson y construir el parámetro de cadena JSON con una biblioteca JSON. Esto evitará cualquier accidente potencial de codificación de información en una cadena o script de JSON y asegúrese de que ninguna entrada controlada por el atacante pueda modificar el resto del mensaje JSON o ejecutar una secuencia de comandos arbitraria.

## Tipos de cadena

Los parámetros de salida de cadenas son LPWSTR null terminada. El destinatario de la llamada asigna la cadena con CoTaskMemAlloc. La propiedad se transfiere a la persona que llama y la persona que llama puede liberar la memoria usando CoTaskMemFree.

La cadena en los parámetros son cadenas terminadas en NULL LPCWSTR. La persona que llama garantiza que la cadena es válida durante la llamada de función sincrónica. Si el destinatario de la llamada tiene que conservar ese valor en algún punto después de que se complete la llamada de función, el destinatario de la llamada debe asignar su propia copia del valor de la cadena.

## URI y análisis de JSON

Varios métodos proporcionan o aceptan identificadores URI y JSON como cadenas. Use su propia biblioteca preferida para analizar y generar estas cadenas.

Si WinRT está disponible para tu aplicación, puedes usar `RuntimeClass_Windows_Data_Json_JsonObject` y `IJsonObjectStatics` analizar o producir cadenas JSON, o bien, `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` analizar y producir URI. Ambos funcionan en las aplicaciones Win32.

Si usas IUri y CreateUri para analizar URI, es posible que desees usar los siguientes marcadores de creación de URI para que el comportamiento de CreateUri sea más parecido al de análisis de URI en la vista de vistas en vista previa: `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## Depuración

Abra DevTools con los métodos abreviados normales: `F12` o `Ctrl+Shift+I` . Puede usar el `--auto-open-devtools-for-tabs` modificador de argumento de comando para que la ventana de DevTools se abra inmediatamente al crear una vista en vista previa. Consulte la documentación de CreateWebView para obtener información sobre cómo proporcionar argumentos de la línea de comandos adicionales para el proceso del explorador. Consulte la clave del registro LoaderOverride para probar las diferentes compilaciones de WebView2 sin modificar la aplicación en la documentación de CreateWebView.

## Control de versiones

Después de haber usado una versión determinada del SDK para compilar la aplicación, es posible que la aplicación termine de funcionar con una versión anterior o posterior de los archivos binarios instalados en el explorador. Hasta la versión 1.0.0.0 de WebView2, es posible que se produzcan cambios importantes durante las actualizaciones que impidan que el SDK funcione con diferentes versiones de los archivos binarios del explorador instalados. Después de la versión 1.0.0.0, las diferentes versiones del SDK pueden funcionar con las distintas versiones del explorador instalado siguiendo estos procedimientos recomendados:

Para tener en cuenta los cambios importantes en la API, asegúrate de comprobar si se produjo un error al llamar a la CreateWebView2Environment de exportación de DLL y al llamar a QueryInterface en cualquier objeto WebView2. Un valor devuelto de E_NOINTERFACE puede indicar que el SDK no es compatible con los archivos binarios del explorador Edge.

Comprobar si hay un error en QueryInterface también tendrá en cuenta los casos en los que el SDK es más reciente que la versión del explorador Edge y la aplicación intenta usar una interfaz de la que no está consciente el explorador Edge.

Cuando una interfaz no está disponible, puede considerar deshabilitar la característica asociada si es posible o informar al usuario final de que necesita actualizar su explorador.

## Miembros

#### get_Settings 

El objeto [IWebView2Settings](IWebView2Settings.md) contiene varios valores modificables para la vista de vista de contenido para la vista de contenido.

> [get_Settings](#get_settings)pública HRESULT (configuración de[IWebView2Settings](IWebView2Settings.md) * *)

#### get_Source 

Identificador URI del documento de nivel superior actual.

> [get_Source](#get_source)de HRESULT público (URI LPWStr *)

Este valor puede cambiar potencialmente como parte del desencadenador de eventos DocumentStateChanged en algunos casos, como navegar a un sitio o navegación de fragmentos diferentes. Permanecerá igual para otros tipos de navegación, como recargas de páginas o historial. pushState con la misma dirección URL que la página actual.

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_documentStateChangedToken));
```

#### Busque 

Hacer que la navegación del documento de nivel superior sea la dirección URI especificada.

> [desplazarse](#navigate)con HRESULT público (URI de LPCWSTR)

Para obtener más información, consulta los eventos de navegación. Ten en cuenta que esto inicia una navegación y el evento NavigationStarting correspondiente se desencadenará después de que se complete esta llamada de navegación.

```cpp
void ControlComponent::NavigateToAddressBar()
{
    WCHAR uri[2048] = L"";
    GetWindowText(m_toolbar->addressBarWindow, uri, ARRAYSIZE(uri));
    CHECK_FAILURE(m_webView->Navigate(uri));
}
```

#### MoveFocus 

Mover el foco a WebView.

> [MOVEFOCUS](#movefocus)HRESULT público (razón[WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) )

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
            for (int i = 0; i < m_tabbableWindows.size(); i++)
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
    for (int i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_NEXT);
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
    CHECK_FAILURE(m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### NavigateToString 

Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.

> HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)

El parámetro htmlContent no puede tener más de 2 MB de caracteres. El origen de la nueva página será acerca de: Blank.

```cpp
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### add_NavigationStarting 

Agregue un controlador de eventos para el evento NavigationStarting.

> [add_NavigationStarting](#add_navigationstarting)de HRESULT público ([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) * EventHandler, EventRegistrationToken * token)

NavigationStarting se desencadena cuando el marco principal de vista previa solicita permiso para navegar a otro URI. Esto también se activará para el redireccionamiento.

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            if (userInitiated)
            {
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
            }
        }
        // Changes to settings will apply at the next navigation, which includes the
        // navigation after a NavigationStarting event.  We can use this to change
        // settings according to what site we're visiting.
        if (ShouldBlockScriptForUri(uri.get()))
        {
            m_settings->put_IsScriptEnabled(FALSE);
        }
        else
        {
            m_settings->put_IsScriptEnabled(m_isScriptEnabled);
        }
        return S_OK;
    }).Get(), &m_navigationStartingToken));
```

#### remove_NavigationStarting 

Quitar un controlador de eventos agregado previamente con add_NavigationStarting.

> [remove_NavigationStarting](#remove_navigationstarting)de HRESULT público (token EventRegistrationToken)

#### add_DocumentStateChanged 

Agregue un controlador de eventos para el evento DocumentStateChanged.

> [add_DocumentStateChanged](#add_documentstatechanged)de HRESULT público ([IWebView2DocumentStateChangedEventHandler](IWebView2DocumentStateChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

DocumentStateChanged se desencadena cuando se comienza a cargar contenido nuevo en el marco principal de WebView o si se produce una navegación de la misma página (por ejemplo, a través de la navegación de fragmentos o del historial. navegación de pushState). Esto sigue el evento NavigationStarting y precede al evento NavigationCompleted.

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_documentStateChangedToken));
```

#### remove_DocumentStateChanged 

Quitar un controlador de eventos agregado previamente con add_DocumentStateChanged.

> [remove_DocumentStateChanged](#remove_documentstatechanged)de HRESULT público (token EventRegistrationToken)

#### add_NavigationCompleted 

Agregue un controlador de eventos para el evento NavigationCompleted.

> [add_NavigationCompleted](#add_navigationcompleted)de HRESULT público ([IWebView2NavigationCompletedEventHandler](IWebView2NavigationCompletedEventHandler.md) * EventHandler, EventRegistrationToken * token)

El evento NavigationCompleted se desencadena cuando WebView se ha cargado completamente (Body. onload se ha desencadenado) o se ha detenido con error.

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Back, Forward, and Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<IWebView2NavigationCompletedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }

                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);
                EnableWindow(m_toolbar->cancelWindow, FALSE);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### remove_NavigationCompleted 

Quitar un controlador de eventos agregado previamente con add_NavigationCompleted.

> [remove_NavigationCompleted](#remove_navigationcompleted)de HRESULT público (token EventRegistrationToken)

#### add_FrameNavigationStarting 

Agregue un controlador de eventos para el evento FrameNavigationStarting.

> [add_FrameNavigationStarting](#add_framenavigationstarting)de HRESULT público ([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) * EventHandler, EventRegistrationToken * token)

FrameNavigationStarting se desencadena cuando un marco secundario de la vista de vista previa solicita permiso para navegar a otro URI. Esto también se activará para el redireccionamiento.

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));
        }
        return S_OK;
    }).Get(), &m_frameNavigationStartingToken));
```

#### remove_FrameNavigationStarting 

Quitar un controlador de eventos agregado previamente con add_FrameNavigationStarting.

> [remove_FrameNavigationStarting](#remove_framenavigationstarting)de HRESULT público (token EventRegistrationToken)

#### add_MoveFocusRequested 

Agregue un controlador de eventos para el evento MoveFocusRequested.

> [add_MoveFocusRequested](#add_movefocusrequested)de HRESULT público ([IWebView2MoveFocusRequestedEventHandler](IWebView2MoveFocusRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

MoveFocusRequested se activa cuando el usuario intenta usar la tecla TAB fuera de la vista. El foco de la vista de WebView no ha cambiado cuando se desencadena este evento.

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_webView->add_MoveFocusRequested(
        Callback<IWebView2MoveFocusRequestedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2MoveFocusRequestedEventArgs* args)
                -> HRESULT {
                if (!g_autoTabHandle)
                {
                    WEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == WEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
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

#### remove_MoveFocusRequested 

Quitar un controlador de eventos agregado previamente con add_MoveFocusRequested.

> [remove_MoveFocusRequested](#remove_movefocusrequested)de HRESULT público (token EventRegistrationToken)

#### add_GotFocus 

Agregue un controlador de eventos para el evento GotFocus.

> [add_GotFocus](#add_gotfocus)de HRESULT público ([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

GotFocus se desencadena cuando WebView tiene el foco.

#### remove_GotFocus 

Quitar un controlador de eventos agregado previamente con add_GotFocus.

> [remove_GotFocus](#remove_gotfocus)de HRESULT público (token EventRegistrationToken)

#### add_LostFocus 

Agregue un controlador de eventos para el evento LostFocus.

> [add_LostFocus](#add_lostfocus)de HRESULT público ([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

LostFocus se desencadena cuando WebView pierde el foco. En caso de que se inicie el evento MoveFocusRequested, el foco seguirá en la vista previa cuando se desencadene el evento MoveFocusRequested. Perder el foco solo se activa cuando el código de la aplicación o la acción predeterminada del evento MoveFocusRequested está lejos de WebView.

#### remove_LostFocus 

Quitar un controlador de eventos agregado previamente con add_LostFocus.

> [remove_LostFocus](#remove_lostfocus)de HRESULT público (token EventRegistrationToken)

#### add_WebResourceRequested_deprecated 

Esta API estará en desuso; usa la nueva API de add_WebResourceRequested.

> [add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated)pública HRESULT (LPCWSTR * const urlFilter,[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) * const resourceContextFilter, SIZE_T filterLength,[IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Agregue un controlador de eventos para el evento WebResourceRequested. Se desencadena cuando WebView realiza cualquier solicitud HTTP. Usa urlFilter para pasar una lista con filterLength de tamaño de las direcciones URL que deseas escuchar. Cada entrada de dirección URL también admite caracteres comodín: ' * ' coincide con cero o más caracteres, y '? ' coincide exactamente con un carácter. Para cada entrada de urlFilter, proporciona una resourceContextFilter de coincidencia que representa los tipos de recursos para los que se debe activar WebResourceRequested. Si filterLength es 0, el evento se desencadenará para todas las solicitudes de red. Los contextos de recursos admitidos son: documento, hoja de estilos, imagen, multimedia, fuente, script, XHR, Fetch.

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<IWebView2WebResourceRequestedEventHandler>(
                    [this](
                        IWebView2WebView* sender,
                        IWebView2WebResourceRequestedEventArgs* args) {
                        wil::com_ptr<IWebView2WebResourceRequestedEventArgs2>
                            webResourceEventArgs2;
                        args->QueryInterface(IID_PPV_ARGS(&webResourceEventArgs2));
                        WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            webResourceEventArgs2->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<IWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### remove_WebResourceRequested 

Quitar un controlador de eventos agregado previamente con add_WebResourceRequested.

> [remove_WebResourceRequested](#remove_webresourcerequested)de HRESULT público (token EventRegistrationToken)

#### add_ScriptDialogOpening 

Agregue un controlador de eventos para el evento ScriptDialogOpening.

> [add_ScriptDialogOpening](#add_scriptdialogopening)de HRESULT público ([IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) * EventHandler, EventRegistrationToken * token)

El evento se desencadena cuando se muestra un cuadro de diálogo de JavaScript (alerta, confirmación o mensaje) para la vista de la vista en WebView. Este evento solo se desencadena si la propiedad IWebView2Settings:: AreDefaultScriptDialogsEnabled se establece en false.

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<IWebView2ScriptDialogOpeningEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<IWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            WEBVIEW2_SCRIPT_DIALOG_KIND type;
            wil::unique_cotaskmem_string message;
            wil::unique_cotaskmem_string defaultText;

            CHECK_FAILURE(eventArgs->get_Uri(&uri));
            CHECK_FAILURE(eventArgs->get_Kind(&type));
            CHECK_FAILURE(eventArgs->get_Message(&message));
            CHECK_FAILURE(eventArgs->get_DefaultText(&defaultText));

            std::wstring promptString = std::wstring(L"The page at '")
                + uri.get() + L"' says:";
            TextInputDialog dialog(
                m_appWindow->GetMainWindow(),
                L"Script Dialog",
                promptString.c_str(),
                message.get(),
                defaultText.get(),
                /* readonly */ type != WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<IWebView2Deferral> deferral;
            CHECK_FAILURE(args->GetDeferral(&deferral));
            m_completeDeferredDialog = [showDialog, deferral]
            {
                showDialog();
                CHECK_FAILURE(deferral->Complete());
            };
        }
        else
        {
            showDialog();
        }

        return S_OK;
    }).Get(), &m_scriptDialogOpeningToken));
```

#### remove_ScriptDialogOpening 

Quitar un controlador de eventos agregado previamente con add_ScriptDialogOpening.

> [remove_ScriptDialogOpening](#remove_scriptdialogopening)de HRESULT público (token EventRegistrationToken)

#### add_ZoomFactorChanged 

Agregue un controlador de eventos para el evento ZoomFactorChanged.

> [add_ZoomFactorChanged](#add_zoomfactorchanged)de HRESULT público ([IWebView2ZoomFactorChangedEventHandler](IWebView2ZoomFactorChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

El evento se desencadena cuando cambia la propiedad ZoomFactor de la vista de vista previa. El evento se podría activar porque el autor de la llamada modificó la propiedad ZoomFactor o debido a que el usuario modificaba manualmente el zoom. Cuando el autor de la llamada lo modifica a través de la propiedad ZoomFactor, el factor de zoom interno se actualiza inmediatamente y no se producirá ningún evento ZoomFactorChanged. La vista Web asocia el último factor de zoom usado para cada sitio. Por lo tanto, es posible que el factor de zoom cambie al navegar a una página diferente. Cuando el factor de zoom cambia debido a esto, el evento ZoomFactorChanged se activa justo después del evento DocumentStateChanged.

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_webView->add_ZoomFactorChanged(
        Callback<IWebView2ZoomFactorChangedEventHandler>(
            [this](IWebView2WebView* sender, IUnknown* args) -> HRESULT {
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

#### remove_ZoomFactorChanged 

Quitar un controlador de eventos agregado previamente con add_ZoomFactorChanged.

> [remove_ZoomFactorChanged](#remove_zoomfactorchanged)de HRESULT público (token EventRegistrationToken)

#### add_PermissionRequested 

Agregue un controlador de eventos para el evento PermissionRequested.

> [add_PermissionRequested](#add_permissionrequested)de HRESULT público ([IWebView2PermissionRequestedEventHandler](IWebView2PermissionRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Se desencadena cuando el contenido de una vista previa solicita permiso para acceder a algunos recursos privilegiados.

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<IWebView2PermissionRequestedEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        WEBVIEW2_PERMISSION_TYPE type = WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionType(&type));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionType(type);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? WEBVIEW2_PERMISSION_STATE_DENY
            :                     WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### remove_PermissionRequested 

Quitar un controlador de eventos agregado previamente con add_PermissionRequested.

> [remove_PermissionRequested](#remove_permissionrequested)de HRESULT público (token EventRegistrationToken)

#### add_ProcessFailed 

Agregue un controlador de eventos para el evento ProcessFailed.

> [add_ProcessFailed](#add_processfailed)de HRESULT público ([IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Se desencadena cuando un proceso WebView finaliza de forma inesperada o deja de responder.

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<IWebView2ProcessFailedEventHandler>(
            [this](IWebView2WebView* sender,
                IWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser process exited unexpectedly.  Recreate webview?",
                L"Browser process exited",
                MB_YESNO);
            if (button == IDYES)
            {
                m_appWindow->ReinitializeWebView();
            }
        }
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### remove_ProcessFailed 

Quitar un controlador de eventos agregado previamente con add_ProcessFailed.

> [remove_ProcessFailed](#remove_processfailed)de HRESULT público (token EventRegistrationToken)

#### AddScriptToExecuteOnDocumentCreated 

Agregue el JavaScript proporcionado a una lista de scripts que se deben ejecutar después de que se haya creado el objeto global, pero antes de que se haya analizado el documento HTML y antes de que se ejecute cualquier otro script incluido en el documento HTML.

> [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)de HRESULT público (LPCWSTR JavaScript,[IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) * handler)

El script insertado se aplicará a todas las navegaciones del marco secundario y el documento de primer nivel superior hasta que se elimine con RemoveScriptToExecuteOnDocumentCreated. Esto se aplica de forma asincrónica y debes esperar a que se ejecute el controlador de finalización para poder asegurarte de que el script está listo para ejecutarse en navegaciones futuras.

Tenga en cuenta que si un documento HTML contiene algún tipo de espacio aislado a través de propiedades de [espacio aislado](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) o el [encabezado HTTP de seguridad de contenido](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , esto afectará a la secuencia de comandos que se ejecuta aquí. Así, por ejemplo, si la palabra clave "Allow-modal" no se establece, se omitirán las llamadas a la `alert` función.

```cpp
// Prompt the user for some script and register it to execute whenever a new page loads.
void ScriptComponent::AddInitializeScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Add Initialize Script",
        L"Initialization Script:",
        L"Enter the JavaScript code to run as the initialization script that "
            L"runs before any script in the HTML document.",
    // This example script stops child frames from opening new windows.  Because
    // the initialization script runs before any script in the HTML document, we
    // can trust the results of our checks on window.parent and window.top.
        L"if (window.parent !== window.top) {\r\n"
        L"    delete window.open;\r\n"
        L"}");
    if (dialog.confirmed)
    {
        m_webView->AddScriptToExecuteOnDocumentCreated(
            dialog.input.c_str(),
            Callback<IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
                [this](HRESULT error, PCWSTR id) -> HRESULT
        {
            m_lastInitializeScriptId = id;
            MessageBox(nullptr, id, L"AddScriptToExecuteOnDocumentCreated Id", MB_OK);
            return S_OK;
        }).Get());

    }
}
```

#### RemoveScriptToExecuteOnDocumentCreated 

Quite el JavaScript correspondiente agregado a través de AddScriptToExecuteOnDocumentCreated.

> HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(LPCWSTR ID)

#### ExecuteScript 

Ejecute el código JavaScript desde el parámetro de JavaScript en el documento de nivel superior actual representado en la vista de vistas en WebView.

> [ExecuteScript](#executescript)de HRESULT público (LPCWSTR JavaScript,[IWebView2ExecuteScriptCompletedHandler](IWebView2ExecuteScriptCompletedHandler.md) * handler)

Esto se ejecutará de forma asincrónica y cuando se complete, si se proporciona un controlador en el parámetro ExecuteScriptCompletedHandler, se llamará a su método Invoke con el resultado de evaluar el JavaScript proporcionado. El valor del resultado es una cadena codificada por JSON. Si el resultado es no definido, contiene un ciclo de referencia o, de lo contrario, no se puede codificar en JSON, el valor de JSON NULL se devolverá como la cadena "null". Observe que una función que no tiene ningún valor explícito devuelto devuelve undefined. Si el script ejecutado inicia una excepción no controlada, el resultado es también ' null '. Este método se aplica de forma asincrónica. Si la llamada se realiza mientras la vista en la vista previa está en un documento y se realiza una navegación después de que se realiza la llamada, pero antes de que se ejecute JavaScript, no se ejecutará el script y se llamará al controlador con E_FAIL para su parámetro errorCode. ExecuteScript funcionará incluso si IsScriptEnabled se establece en FALSE.

```cpp
// Prompt the user for some script and then execute it.
void ScriptComponent::InjectScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Inject Script",
        L"Enter script code:",
        L"Enter the JavaScript code to run in the webview.",
        L"window.getComputedStyle(document.body).backgroundColor");
    if (dialog.confirmed)
    {
        m_webView->ExecuteScript(dialog.input.c_str(),
            Callback<IWebView2ExecuteScriptCompletedHandler>(
                [](HRESULT error, PCWSTR result) -> HRESULT
        {
            if (error != S_OK) {
                ShowFailure(error, L"ExecuteScript failed");
            }
            MessageBox(nullptr, result, L"ExecuteScript Result", MB_OK);
            return S_OK;
        }).Get());
    }
}
```

#### CapturePreview 

Capture una imagen de lo que se muestra en la vista de página.

> [CAPTUREPREVIEW](#capturepreview)HRESULT público ([WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) ImageFormat, IStream * imageStream,[IWebView2CapturePreviewCompletedHandler](IWebView2CapturePreviewCompletedHandler.md) * handler)

Especifique el formato de la imagen con el parámetro imageFormat. Los datos binarios de la imagen resultantes se escriben en el parámetro imageStream proporcionado. Cuando CapturePreview termina de escribir en la secuencia, se llama al método Invoke del parámetro handler proporcionado.

```cpp
// Show the user a file selection dialog, then save a screenshot of the WebView
// to the selected file.
void FileComponent::SaveScreenshot()
{
    OPENFILENAME openFileName = {};
    openFileName.lStructSize = sizeof(openFileName);
    openFileName.hwndOwner = nullptr;
    openFileName.hInstance = nullptr;
    WCHAR fileName[MAX_PATH] = L"WebView2_Screenshot.png";
    openFileName.lpstrFile = fileName;
    openFileName.lpstrFilter = L"PNG File\0*.png\0";
    openFileName.nMaxFile = ARRAYSIZE(fileName);
    openFileName.Flags = OFN_OVERWRITEPROMPT;

    if (GetSaveFileName(&openFileName))
    {
        wil::com_ptr<IStream> stream;
        CHECK_FAILURE(SHCreateStreamOnFileEx(
            fileName, STGM_READWRITE | STGM_CREATE, FILE_ATTRIBUTE_NORMAL, TRUE, nullptr,
            &stream));

        HWND mainWindow = m_appWindow->GetMainWindow();

        CHECK_FAILURE(m_webView->CapturePreview(
            WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<IWebView2CapturePreviewCompletedHandler>(
                [mainWindow](HRESULT error_code) -> HRESULT {
                    CHECK_FAILURE(error_code);

                    MessageBox(mainWindow, L"Preview Captured", L"Preview Captured", MB_OK);
                    return S_OK;
                })
                .Get()));
    }
}
```

#### Volver a cargar 

Volver a cargar la página actual.

> [recarga](#reload)pública de HRESULT ()

Esto es similar a desplazarse hasta el URI del documento de nivel superior actual, incluidos todos los eventos de navegación que desencadenan y respetan cualquier entrada de la caché HTTP. Sin embargo, el historial de atrás y reenvío no se modificará.

#### get_Bounds 

Los límites de la vista previa.

> [get_Boundss](#get_bounds)HRESULT públicos (límites Rect *)

Los límites son relativos al identificador HWND primario. La aplicación tiene dos formas en las que puede ubicar una vista en WebView:

1. Cree un HWND secundario que sea el objeto HWND de la vista < View. Coloque esta ventana donde debería estar la vista en la vista. En este caso, use (0,0) para la Bound's esquina superior izquierda de la vista de vista previa (el desplazamiento).

1. Use la última ventana de la aplicación como el HWND primario de WebView. Establezca la Bound's esquina superior izquierda de la vista previa para que la vista de la vista en la aplicación se coloque correctamente en la aplicación. Los valores de la entrada enlazada están en el espacio de coordenadas del host.

#### put_Bounds 

Establezca la propiedad Bounds.

> [put_Bounds](#put_bounds)de HRESULT público (límites Rect)

```cpp
// Update the bounds of the WebView window to fit available space.
void ViewComponent::ResizeWebView()
{
    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        (m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio + m_webViewBounds.top);
    desiredBounds.right = LONG(
        (m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio + m_webViewBounds.left);

    m_webView->put_Bounds(desiredBounds);
}
```

#### get_ZoomFactor 

El factor de zoom para la página actual en la vista Web.

> [get_ZoomFactor](#get_zoomfactor)de HRESULT público (Double * ZoomFactor)

El factor de zoom se conserva por sitio. Ten en cuenta que cambiar el factor de zoom podría provocar un `window.innerWidth/innerHeight` cambio en el diseño de página. Cuando se desplaza por la vista Web a una página de un sitio diferente, no se aplicará el factor de zoom establecido para la página anterior. Si la aplicación quiere establecer el factor de zoom para una página determinada, el primer lugar para hacerlo es el controlador de eventos DocumentStateChanged. Ten en cuenta que si lo hace, es posible que reciba un evento ZoomFactorChanged para el factor de zoom persistente antes de recibir el evento ZoomFactorChanged para el factor de zoom especificado. No se permite especificar un zoomFactor menor o igual que 0. WebView también tiene un intervalo de factor de zoom compatible interno. Cuando un factor de zoom especificado está fuera de ese rango, se normalizará para que esté dentro del rango y se desencadenará un evento ZoomFactorChanged para el factor de zoom aplicado real. Cuando se produzca esta normalización de rango, la propiedad ZoomFactor informará sobre el factor de zoom especificado durante la modificación anterior de la propiedad ZoomFactor hasta que se reciba el evento ZoomFactorChanged después de que la vista previa aplique el factor de zoom normalizado.

#### put_ZoomFactor 

Establezca la propiedad ZoomFactor.

> [put_ZoomFactor](#put_zoomfactor)de HRESULT público (Double ZoomFactor)

#### get_IsVisible 

La propiedad IsVisible determina si se muestra u oculta la vista en WebView.

> HRESULT público [get_IsVisible](#get_isvisible)(bool * IsVisible)

Si IsVisible se establece en false, WebView será transparente y no se representará. Sin embargo, esto no afectará a la ventana que contenga la vista de contenido (el parámetro HWND pasado a CreateWebView). Si desea que esta ventana desaparezca también, llame a ShowWindow directamente, además de modificar la propiedad IsVisible. Si la ventana superior está minimizada o restaurada, WebView no recibirá mensajes de ventana. Por motivos de rendimiento, desarrollador debe establecer el valor de la propiedad IsVisible de la WebView en falso cuando la ventana de la aplicación está minimizada y volver a ser true cuando se restaura la ventana de la aplicación. La ventana de la aplicación puede hacerlo controlando SC_MINIMIZE y SC_RESTORE comando al recibir WM_SYSCOMMAND mensaje.

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_webView->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_webView->put_IsVisible(m_isVisible);
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
            m_webView->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_webView->put_IsVisible(TRUE);
            }
        }
    }
```

#### PostWebMessageAsJson 

Publique el mensaje webmensaje especificado en el documento de nivel superior de este [IWebView2WebView]().

> HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)

Se desencadena el evento de mensaje de window. Chrome. WebView del documento de nivel superior. JavaScript en ese documento puede suscribirse y cancelar la suscripción al evento a través de lo siguiente: 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 El argumentos del evento es una instancia de `MessageEvent` . La opción IWebView2Settings:: IsWebMessageEnabled debe ser true o este método dará un error con E_INVALIDARG. La propiedad de datos de Arg del evento es el parámetro de cadena WebMessage analizado como una cadena JSON en un objeto de JavaScript. La propiedad Source de Arg de evento es una referencia al `window.chrome.webview` objeto. Consulte SetWebMessageReceivedEventHandler para obtener información sobre cómo enviar mensajes desde el documento HTML de la vista en WebView al host. Este mensaje se envía de forma asincrónica. Si se produce una navegación antes de que el mensaje se publique en la página, no se enviará el mensaje.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### PostWebMessageAsString 

Este es un auxiliar para publicar un mensaje que es una cadena simple en lugar de una representación de cadena JSON de un objeto de JavaScript.

> HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)

Esto se comporta exactamente de la misma manera que PostWebMessageAsJson, pero la `window.chrome.webview` propiedad data del argumento de evento de mensaje será una cadena con el mismo valor que webMessageAsString. Use este en lugar de PostWebMessageAsJson si desea comunicarse a través de cadenas simples en lugar de objetos JSON.

#### add_WebMessageReceived 

Este evento se desencadena cuando se establece la configuración de IsWebMessageEnabled y el documento de nivel superior de las llamadas de WebView `window.chrome.webview.postMessage` .

> [add_WebMessageReceived](#add_webmessagereceived)pública HRESULT (controlador[IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) *, EventRegistrationToken * token)

La función postmensaje es `void postMessage(object)` donde objeto es cualquier objeto compatible con la conversión de JSON.

```cpp
        window.chrome.webview.addEventListener('message', arg => {
            if ("SetColor" in arg.data) {
                document.getElementById("colorable").style.color = arg.data.SetColor;
            }
            if ("WindowBounds" in arg.data) {
                document.getElementById("window-bounds").value = arg.data.WindowBounds;
            }
        });

        function SetTitleText() {
            let titleText = document.getElementById("title-text");
            window.chrome.webview.postMessage(`SetTitleText ${titleText.value}`);
        }
        function GetWindowBounds() {
            window.chrome.webview.postMessage("GetWindowBounds");
        }
```

 Cuando se llama a PostMessage, se invocará el [IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) establecido a través de este método SetWebMessageReceivedEventHandler con el parámetro de objeto PostMessage convertido en una cadena JSON.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### remove_WebMessageReceived 

Quitar un controlador de eventos agregado previamente con add_WebMessageReceived.

> [remove_WebMessageReceived](#remove_webmessagereceived)de HRESULT público (token EventRegistrationToken)

#### Cerrar 

Cierra WebView y limpia la instancia de explorador subyacente.

> HRESULT público [Close](#close)()

Si limpias el explorador instace, se liberarán los recursos que encienden la vista Web. La instancia del explorador se cerrará si no hay ninguna otra vista previa con ella.

Después de llamar a Close, todas las llamadas a métodos producirán errores y los controladores de eventos dejarán de activarse. Específicamente, la WebView liberará sus referencias a los controladores de eventos cuando se llama a Close.

Se llama implícitamente a Close cuando WebView pierde su referencia final y se destruye. Sin embargo, se recomienda llamar de forma explícita a Close para evitar cualquier ciclo de referencias entre la vista de WebView y el código de la aplicación. En concreto, si capturas una referencia a la vista de la vista en un controlador de eventos, crearás un ciclo de referencia entre la vista en WebView y el controlador de eventos. Close interrumpirá este ciclo liberando todos los controladores de eventos. Pero para evitar esta situación, se recomienda llamar explícitamente a Close en WebView y no capturar una referencia a WebView para asegurarte de que la WebView pueda limpiarse correctamente.

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView()
{
    DeleteAllComponents();
    if (m_webView)
    {
        m_webView->Close();
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
}
```

#### CallDevToolsProtocolMethod 

Llama a un método DevToolsProtocol asincrónico.

> HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR NOMBREDEMÉTODO, LPCWSTR ParametersAsJson,[IWebView2CallDevToolsProtocolMethodCompletedHandler](IWebView2CallDevToolsProtocolMethodCompletedHandler.md) * handler)

Consulte el [visor de protocolos de DevTools](https://aka.ms/DevToolsProtocolDocs) para obtener una lista y una descripción de los métodos disponibles. El parámetro methodName es el nombre completo del método en el formato `{domain}.{method}` . El parámetro parametersAsJson es una cadena con formato JSON que contiene los parámetros del método correspondiente. Se llamará al método Invoke del controlador cuando se complete el método de forma asincrónica. Se llamará a Invoke con el objeto devuelto del método como una cadena JSON.

```cpp
// Prompt the user for the name and parameters of a CDP method, then call it.
void ScriptComponent::CallCdpMethod()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Call CDP Method",
        L"CDP method name:",
        L"Enter the CDP method name to call, followed by a space,\r\n"
            L"followed by the parameters in JSON format.",
        L"Runtime.evaluate {\"expression\":\"alert(\\\"test\\\")\"}");
    if (dialog.confirmed)
    {
        size_t delimiterPos = dialog.input.find(L' ');
        std::wstring methodName = dialog.input.substr(0, delimiterPos);
        std::wstring methodParams =
            (delimiterPos < dialog.input.size()
                ? dialog.input.substr(delimiterPos + 1)
                : L"{}");

        m_webView->CallDevToolsProtocolMethod(
            methodName.c_str(),
            methodParams.c_str(),
            Callback<IWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### add_DevToolsProtocolEventReceived 

Suscribirse a un evento de DevToolsProtocol.

> [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)de HRESULT público (LPCWSTR eventName,[IWebView2DevToolsProtocolEventReceivedEventHandler](IWebView2DevToolsProtocolEventReceivedEventHandler.md) * handler, EventRegistrationToken * token)

Consulte el [visor de protocolos de DevTools](https://aka.ms/DevToolsProtocolDocs) para obtener una lista y una descripción de los eventos disponibles. El parámetro eventName es el nombre completo del evento en el formato `{domain}.{event}` . Se llamará al método Invoke del controlador siempre que se desencadene el evento DevToolsProtocol correspondiente. Se llamará a Invoke con el objeto de los argumentos de un evento que contiene el objeto de parámetro CDP como una cadena JSON.

```cpp
// Prompt the user to name a CDP event, and then subscribe to that event.
void ScriptComponent::SubscribeToCdpEvent()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Subscribe to CDP Event",
        L"CDP event name:",
        L"Enter the name of the CDP event to subscribe to.\r\n"
            L"You may also have to call the \"enable\" method of the\r\n"
            L"event's domain to receive events (for example \"Log.enable\").\r\n",
        L"Log.entryAdded");
    if (dialog.confirmed)
    {
        std::wstring eventName = dialog.input;
        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(m_webView->remove_DevToolsProtocolEventReceived(
                eventName.c_str(),
                preexistingToken->second));
        }

        CHECK_FAILURE(m_webView->add_DevToolsProtocolEventReceived(
            eventName.c_str(),
            Callback<IWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](IWebView2WebView* sender,
                            IWebView2DevToolsProtocolEventReceivedEventArgs* args)
                -> HRESULT
        {
            wil::unique_cotaskmem_string parameterObjectAsJson;
            CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
            MessageBox(nullptr, parameterObjectAsJson.get(),
                       (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
            return S_OK;
        }).Get(), &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### remove_DevToolsProtocolEventReceived 

Quitar un controlador de eventos agregado previamente con add_DevToolsProtocolEventReceived.

> [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)de HRESULT público (LPCWSTR, EventRegistrationToken token)

#### get_BrowserProcessId 

El identificador de proceso del proceso del explorador que hospeda la vista Web.

> [get_BrowserProcessId](#get_browserprocessid)de HRESULT público (UINT32 * Value)

#### get_CanGoBack 

Puede navegar por la vista Web a la página anterior del historial de navegación.

> [get_CanGoBack](#get_cangoback)de HRESULT público (bool * CanGoBack)

get_CanGoBack cambiar el valor con el evento DocumentStateChanged.

#### get_CanGoForward 

Puede navegar por la vista Web a la página siguiente del historial de navegación.

> [get_CanGoForward](#get_cangoforward)de HRESULT público (bool * CanGoForward)

get_CanGoForward cambiar el valor con el evento DocumentStateChanged.

#### GoBack 

Navega por la vista Web a la página anterior del historial de navegación.

> HRESULT público [GoBack](#goback)()

#### GoForward 

Navega por la vista Web a la página siguiente del historial de navegación.

> [HRESULT público](#goforward)()

#### WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT 

Formato de imagen usado por el método [IWebView2WebView:: CapturePreview](#capturepreview) .

> [WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG            | Formato de imagen PNG.
WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG            | Formato de imagen JPEG.

#### WEBVIEW2_SCRIPT_DIALOG_KIND 

Cuadro de diálogo tipo de JavaScript usado en la interfaz [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) .

> [WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT            | Un cuadro de diálogo invocado a través de la función de JavaScript Window. Alert.
WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM            | Un cuadro de diálogo invocado a través de la función de la ventana. confirmar JavaScript.
WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT            | Un cuadro de diálogo invocado a través de la función de aviso de JavaScript.

#### WEBVIEW2_PROCESS_FAILED_KIND 

Tipo de error de proceso usado en la interfaz de [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) .

> [WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED            | Indica que el proceso del explorador ha terminado de forma inesperada.
WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED            | Indica que el proceso de representación ha terminado de forma inesperada.
WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE            | Indica que el proceso de representación deja de responder.

#### WEBVIEW2_PERMISSION_TYPE 

El tipo de una solicitud de permiso.

> [WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION            | Permiso desconocido.
WEBVIEW2_PERMISSION_TYPE_MICROPHONE            | Permiso para capturar audio.
WEBVIEW2_PERMISSION_TYPE_CAMERA            | Permiso para capturar video.
WEBVIEW2_PERMISSION_TYPE_GEOLOCATION            | Permiso para acceder a la ubicación geográfica.
WEBVIEW2_PERMISSION_TYPE_NOTIFICATIONS            | Permiso para enviar notificaciones Web.
WEBVIEW2_PERMISSION_TYPE_OTHER_SENSORS            | Permiso para acceder al sensor genérico.
WEBVIEW2_PERMISSION_TYPE_CLIPBOARD_READ            | Permiso para leer el Portapapeles del sistema sin un gesto de usuario.

#### WEBVIEW2_PERMISSION_STATE 

Respuesta a una solicitud de permiso.

> [WEBVIEW2_PERMISSION_STATE](#webview2_permission_state) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
WEBVIEW2_PERMISSION_STATE_DEFAULT            | Use el comportamiento de explorador predeterminado, que suele solicitar a los usuarios la decisión.
WEBVIEW2_PERMISSION_STATE_ALLOW            | Otorgue la solicitud de permiso.
WEBVIEW2_PERMISSION_STATE_DENY            | Denegar la solicitud de permiso.

#### WEBVIEW2_MOVE_FOCUS_REASON 

Motivo de mover el foco.

> [WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC            | El ajuste del foco a WebView.
WEBVIEW2_MOVE_FOCUS_REASON_NEXT            | Moviendo el foco debido a una resaltado de pestañas hacia adelante.
WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS            | Moviendo el foco debido a un recorrido de tabulación hacia atrás.

#### WEBVIEW2_WEB_ERROR_STATUS 

Valores de estado de error para navegaciones Web.

> [WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN            | Se ha producido un error desconocido.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT            | El nombre común del certificado SSL no coincide con la dirección Web.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED            | El certificado SSL ha expirado.
WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS            | El certificado de cliente SSL contiene errores.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED            | El certificado SSL ha sido revocado.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID            | El certificado SSL no es válido.
WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE            | No se puede comunicar con el host.
WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT            | Se agotó el tiempo de espera de la conexión.
WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE            | El servidor ha devuelto una respuesta no válida o no reconocida.
WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED            | La conexión ha sido cancelada.
WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET            | Se restableció la conexión.
WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED            | Se perdió la conexión a Internet.
WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT            | No se puede conectar al destino.
WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED            | No se pudo resolver el nombre de host proporcionado.
WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED            | Se canceló la operación.
WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED            | Error en la redirección de la solicitud.
WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR            | Se ha producido un error inesperado.

#### WEBVIEW2_WEB_RESOURCE_CONTEXT 

Enumeración de contextos de solicitud de recursos Web.

> [WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL            | Todos los recursos.
WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT            | Recursos de documentos.
WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET            | Recursos de CSS.
WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE            | Recursos de imagen.
WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA            | Otros recursos multimedia, como los vídeos.
WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT            | Recursos de fuentes.
WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT            | Recursos de script.
WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST            | Solicitudes XML HTTP.
WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH            | Capture la comunicación de la API.
WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK            | Recursos de TextTrack.
WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_PING            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER            | Otros recursos.

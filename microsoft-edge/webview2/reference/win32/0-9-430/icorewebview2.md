---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 77eb48773a963775e00d4dec50368564af5678b0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655495"
---
# interfaz ICoreWebView2 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface ICoreWebView2
  : public IUnknown
```

WebView2 le permite hospedar contenido web con la tecnología de explorador Web más reciente.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Settings](#get_settings) | El objeto ICoreWebView2Settings contiene varios valores modificables para la vista de vista de contenido para la vista de contenido.
[get_Source](#get_source) | Identificador URI del documento de nivel superior actual.
[Busque](#navigate) | Hacer que la navegación del documento de nivel superior sea la dirección URI especificada.
[NavigateToString](#navigatetostring) | Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.
[add_NavigationStarting](#add_navigationstarting) | Agregue un controlador de eventos para el evento NavigationStarting.
[remove_NavigationStarting](#remove_navigationstarting) | Quitar un controlador de eventos agregado previamente con add_NavigationStarting.
[add_ContentLoading](#add_contentloading) | Agregue un controlador de eventos para el evento ContentLoading.
[remove_ContentLoading](#remove_contentloading) | Quitar un controlador de eventos agregado previamente con add_ContentLoading.
[add_SourceChanged](#add_sourcechanged) | SourceChanged se desencadena cuando cambia la propiedad de origen.
[remove_SourceChanged](#remove_sourcechanged) | Quitar un controlador de eventos agregado previamente con add_SourceChanged.
[add_HistoryChanged](#add_historychanged) | Facturacióncambiar escuchar el cambio del historial de navegación en el documento de nivel superior.
[remove_HistoryChanged](#remove_historychanged) | Quitar un controlador de eventos agregado previamente con add_HistoryChanged.
[add_NavigationCompleted](#add_navigationcompleted) | Agregue un controlador de eventos para el evento NavigationCompleted.
[remove_NavigationCompleted](#remove_navigationcompleted) | Quitar un controlador de eventos agregado previamente con add_NavigationCompleted.
[add_FrameNavigationStarting](#add_framenavigationstarting) | Agregue un controlador de eventos para el evento FrameNavigationStarting.
[remove_FrameNavigationStarting](#remove_framenavigationstarting) | Quitar un controlador de eventos agregado previamente con add_FrameNavigationStarting.
[add_ScriptDialogOpening](#add_scriptdialogopening) | Agregue un controlador de eventos para el evento ScriptDialogOpening.
[remove_ScriptDialogOpening](#remove_scriptdialogopening) | Quitar un controlador de eventos agregado previamente con add_ScriptDialogOpening.
[add_PermissionRequested](#add_permissionrequested) | Agregue un controlador de eventos para el evento PermissionRequested.
[remove_PermissionRequested](#remove_permissionrequested) | Quitar un controlador de eventos agregado previamente con add_PermissionRequested.
[add_ProcessFailed](#add_processfailed) | Agregue un controlador de eventos para el evento ProcessFailed.
[remove_ProcessFailed](#remove_processfailed) | Quitar un controlador de eventos agregado previamente con add_ProcessFailed.
[AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated) | Agregue el JavaScript proporcionado a una lista de scripts que se deben ejecutar después de que se haya creado el objeto global, pero antes de que se haya analizado el documento HTML y antes de que se ejecute cualquier otro script incluido en el documento HTML.
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | Quite el JavaScript correspondiente agregado a través de AddScriptToExecuteOnDocumentCreated.
[ExecuteScript](#executescript) | Ejecute el código JavaScript desde el parámetro de JavaScript en el documento de nivel superior actual representado en la vista de vistas en WebView.
[CapturePreview](#capturepreview) | Capture una imagen de lo que se muestra en la vista de página.
[Volver a cargar](#reload) | Volver a cargar la página actual.
[PostWebMessageAsJson](#postwebmessageasjson) | Publique el mensaje de correo especificado en el documento de nivel superior en este WebView.
[PostWebMessageAsString](#postwebmessageasstring) | Este es un auxiliar para publicar un mensaje que es una cadena simple en lugar de una representación de cadena JSON de un objeto de JavaScript.
[add_WebMessageReceived](#add_webmessagereceived) | Este evento se desencadena cuando se establece la configuración de IsWebMessageEnabled y el documento de nivel superior de las llamadas de WebView `window.chrome.webview.postMessage` .
[remove_WebMessageReceived](#remove_webmessagereceived) | Quitar un controlador de eventos agregado previamente con add_WebMessageReceived.
[CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod) | Llama a un método DevToolsProtocol asincrónico.
[get_BrowserProcessId](#get_browserprocessid) | El identificador de proceso del proceso del explorador que hospeda la vista Web.
[get_CanGoBack](#get_cangoback) | Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.
[get_CanGoForward](#get_cangoforward) | Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.
[GoBack](#goback) | Navega por la vista Web a la página anterior del historial de navegación.
[GoForward](#goforward) | Navega por la vista Web a la página siguiente del historial de navegación.
[GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver) | Obtén un receptor de eventos de protocolo de DevTools que te permita suscribirte a un evento de protocolo de DevTools.
[Detener](#stop) | Detenga todas las navegaciones y las búsquedas de recursos pendientes.
[add_NewWindowRequested](#add_newwindowrequested) | Agregue un controlador de eventos para el evento NewWindowRequested.
[remove_NewWindowRequested](#remove_newwindowrequested) | Quitar un controlador de eventos agregado previamente con add_NewWindowRequested.
[add_DocumentTitleChanged](#add_documenttitlechanged) | Agregue un controlador de eventos para el evento DocumentTitleChanged.
[remove_DocumentTitleChanged](#remove_documenttitlechanged) | Quitar un controlador de eventos agregado previamente con add_DocumentTitleChanged.
[get_DocumentTitle](#get_documenttitle) | Título del documento de nivel superior actual.
[AddRemoteObject](#addremoteobject) | Agregue el objeto host proporcionado a la secuencia de comandos que se ejecuta en la vista Webcon el nombre especificado.
[RemoveRemoteObject](#removeremoteobject) | Quite el objeto host especificado por el nombre para que ya no se pueda tener acceso al mismo desde el código de JavaScript de la vista.
[OpenDevToolsWindow](#opendevtoolswindow) | Abre la ventana DevTools para el documento actual en la vista de vistas en WebView.
[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged) | Notifica cuando cambia la propiedad ContainsFullScreenElement.
[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged) | Quitar un controlador de eventos agregado previamente con el método de evento add_ correspondiente.
[get_ContainsFullScreenElement](#get_containsfullscreenelement) | Indica si WebView contiene un elemento HTML de pantalla completa.
[add_WebResourceRequested](#add_webresourcerequested) | Agregue un controlador de eventos para el evento WebResourceRequested.
[remove_WebResourceRequested](#remove_webresourcerequested) | Quitar un controlador de eventos agregado previamente con add_WebResourceRequested.
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.
[add_WindowCloseRequested](#add_windowcloserequested) | Agregue un controlador de eventos para el evento WindowCloseRequested.
[remove_WindowCloseRequested](#remove_windowcloserequested) | Quitar un controlador de eventos agregado previamente con add_WindowCloseRequested.
[CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) | Formato de imagen usado por el método ICoreWebView2:: CapturePreview.
[CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind) | Cuadro de diálogo tipo de JavaScript usado en la interfaz ICoreWebView2ScriptDialogOpeningEventHandler.
[CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind) | Tipo de error de proceso usado en la interfaz de ICoreWebView2ProcessFailedEventHandler.
[CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind) | El tipo de una solicitud de permiso.
[CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state) | Respuesta a una solicitud de permiso.
[CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status) | Valores de estado de error para navegaciones Web.
[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) | Enumeración de contextos de solicitud de recursos Web.

## Eventos de navegación

La secuencia normal de eventos de navegación es NavigationStarting, SourceChanged, ContentLoading y, después, NavigationCompleted.

![DOT-inline-dotgraph-1. png](media/dot-inline-dotgraph-1.png)

Ten en cuenta que esto es para los eventos de navegación con el mismo evento NavigationId. Los eventos de navegación con diferentes argumentos de evento de NavigationId se pueden solapar. Por ejemplo, si inicia una espera de navegación para su evento NavigationStarting y, a continuación, inicia otra navegación, verá el NavigationStarting para la primera navegación, seguida de la NavigationStarting del segundo Navigate, seguido de la NavigationCompleted de la primera navegación y, a continuación, todos los demás eventos de navegación correspondientes para la segunda navegación. En casos de error puede haber o no un evento ContentLoading dependiendo de si la navegación continúa o no en una página de error. En el caso de una redirección HTTP, habrá varios eventos NavigationStarting en una fila, y los siguientes tendrán establecido el marcador IsRedirect.

Para supervisar o cancelar la navegación dentro de los submarcos de la vista en WebView, use FrameNavigationStarting.

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

Abra DevTools con los métodos abreviados normales: `F12` o `Ctrl+Shift+I` . Puede usar el `--auto-open-devtools-for-tabs` modificador de argumento de comando para que la ventana de DevTools se abra inmediatamente al crear una vista en vista previa. Consulte la documentación de CreateCoreWebView2Host para obtener información sobre cómo proporcionar argumentos de la línea de comandos adicionales para el proceso del explorador. Consulte la clave del registro LoaderOverride para probar las diferentes compilaciones de WebView2 sin modificar la aplicación en la documentación de CreateCoreWebView2Host.

## Control de versiones

Después de haber usado una versión determinada del SDK para compilar la aplicación, es posible que la aplicación termine de funcionar con una versión anterior o posterior de los archivos binarios instalados en el explorador. Hasta la versión 1.0.0.0 de WebView2, es posible que se produzcan cambios importantes durante las actualizaciones que impidan que el SDK funcione con diferentes versiones de los archivos binarios del explorador instalados. Después de la versión 1.0.0.0, las diferentes versiones del SDK pueden funcionar con las distintas versiones del explorador instalado siguiendo estos procedimientos recomendados:

Para tener en cuenta los cambios importantes en la API, asegúrate de comprobar si se produjo un error al llamar a la CreateCoreWebView2Environment de exportación de DLL y al llamar a QueryInterface en cualquier objeto CoreWebView2. Un valor devuelto de E_NOINTERFACE puede indicar que el SDK no es compatible con los archivos binarios del explorador Edge.

Comprobar si hay un error en QueryInterface también tendrá en cuenta los casos en los que el SDK es más reciente que la versión del explorador Edge y la aplicación intenta usar una interfaz de la que no está consciente el explorador Edge.

Cuando una interfaz no está disponible, puede considerar deshabilitar la característica asociada si es posible o informar al usuario final de que necesita actualizar su explorador.

## Miembros

#### get_Settings 

El objeto ICoreWebView2Settings contiene varios valores modificables para la vista de vista de contenido para la vista de contenido.

> [get_Settings](#get_settings)pública HRESULT (configuración de ICoreWebView2Settings * *)

#### get_Source 

Identificador URI del documento de nivel superior actual.

> [get_Source](#get_source)de HRESULT público (URI LPWStr *)

Este valor puede cambiar potencialmente como parte del desencadenador de eventos SourceChanged en algunos casos, como navegar a un sitio o navegación de fragmentos diferentes. Permanecerá igual para otros tipos de navegación, como recargas de páginas o historial. pushState con la misma dirección URL que la página actual.

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
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
        &m_sourceChangedToken));
```

#### Busque 

Hacer que la navegación del documento de nivel superior sea la dirección URI especificada.

> [desplazarse](#navigate)con HRESULT público (URI de LPCWSTR)

Para obtener más información, consulta los eventos de navegación. Ten en cuenta que esto inicia una navegación y el evento NavigationStarting correspondiente se desencadenará después de que se complete esta llamada de navegación.

```cpp
void ControlComponent::NavigateToAddressBar()
{
    int length = GetWindowTextLength(m_toolbar->addressBarWindow);
    std::wstring uri(length, 0);
    PWSTR buffer = const_cast<PWSTR>(uri.data());
    GetWindowText(m_toolbar->addressBarWindow, buffer, length + 1);

    HRESULT hr = m_webView->Navigate(uri.c_str());
    if (hr == E_INVALIDARG)
    {
        // An invalid URI was provided.
        if (uri.find(L' ') == std::wstring::npos
            && uri.find(L'.') != std::wstring::npos)
        {
            // If it contains a dot and no spaces, try tacking http:// on the front.
            hr = m_webView->Navigate((L"http://" + uri).c_str());
        }
        else
        {
            // Otherwise treat it as a web search. We aren't bothering to escape
            // URL syntax characters such as & and #
            hr = m_webView->Navigate((L"https://bing.com/search?q=" + uri).c_str());
        }
    }
    if (hr != E_INVALIDARG) {
        CHECK_FAILURE(hr);
    }
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

> [add_NavigationStarting](#add_navigationstarting)de HRESULT público ([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) * EventHandler, EventRegistrationToken * token)

NavigationStarting se desencadena cuando el marco principal de vista previa solicita permiso para navegar a otro URI. Esto también se activará para el redireccionamiento.

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
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

#### add_ContentLoading 

Agregue un controlador de eventos para el evento ContentLoading.

> [add_ContentLoading](#add_contentloading)de HRESULT público ([ICoreWebView2ContentLoadingEventHandler](ICoreWebView2ContentLoadingEventHandler.md) * EventHandler, EventRegistrationToken * token)

ContentLoading se activa antes de que se cargue ningún contenido, incluso los scripts agregados con AddScriptToExecuteOnDocumentCreated ContentLoading no se desencadenarán si se realiza una navegación de página (por ejemplo, a través de la navegación de fragmentos o el historial. navegaciones pushState). Esto sigue los eventos NavigationStarting y SourceChanged, y precede a los eventos HistoryChanged y NavigationCompleted.

#### remove_ContentLoading 

Quitar un controlador de eventos agregado previamente con add_ContentLoading.

> [remove_ContentLoading](#remove_contentloading)de HRESULT público (token EventRegistrationToken)

#### add_SourceChanged 

SourceChanged se desencadena cuando cambia la propiedad de origen.

> [add_SourceChanged](#add_sourcechanged)de HRESULT público ([ICoreWebView2SourceChangedEventHandler](ICoreWebView2SourceChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

SourceChanged se desencadena para navegar a un sitio diferente o a navegación de fragmentos. No se desencadenará para otros tipos de navegación, como recargas de páginas o historial. pushState con la misma dirección URL que la página actual. SourceChanged se desencadena antes de ContentLoading para la navegación a un nuevo documento. Agregue un controlador de eventos para el evento SourceChanged. 

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
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
        &m_sourceChangedToken));
```

#### remove_SourceChanged 

Quitar un controlador de eventos agregado previamente con add_SourceChanged.

> [remove_SourceChanged](#remove_sourcechanged)de HRESULT público (token EventRegistrationToken)

#### add_HistoryChanged 

Facturacióncambiar escuchar el cambio del historial de navegación en el documento de nivel superior.

> [add_HistoryChanged](#add_historychanged)de HRESULT público ([ICoreWebView2HistoryChangedEventHandler](ICoreWebView2HistoryChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Usa Facturacióncambiar para comprobar si el valor get_CanGoBack/get_CanGoForward ha cambiado. HistoryChanged también se desencadena para usar GoBack/GoForward. HistoryChanged se desencadena después de SourceChanged y ContentLoading. Agregue un controlador de eventos para el evento HistoryChanged. 

```cpp
    // Register a handler for the HistoryChanged event.
    // Update the Back, Forward buttons.
    CHECK_FAILURE(m_webView->add_HistoryChanged(
        Callback<ICoreWebView2HistoryChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);

                return S_OK;
            })
            .Get(),
        &m_historyChangedToken));
```

#### remove_HistoryChanged 

Quitar un controlador de eventos agregado previamente con add_HistoryChanged.

> [remove_HistoryChanged](#remove_historychanged)de HRESULT público (token EventRegistrationToken)

#### add_NavigationCompleted 

Agregue un controlador de eventos para el evento NavigationCompleted.

> [add_NavigationCompleted](#add_navigationcompleted)de HRESULT público ([ICoreWebView2NavigationCompletedEventHandler](ICoreWebView2NavigationCompletedEventHandler.md) * EventHandler, EventRegistrationToken * token)

El evento NavigationCompleted se desencadena cuando WebView se ha cargado completamente (Body. onload se ha desencadenado) o se ha detenido con error.

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<ICoreWebView2NavigationCompletedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    CORE_WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
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

> [add_FrameNavigationStarting](#add_framenavigationstarting)de HRESULT público ([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) * EventHandler, EventRegistrationToken * token)

FrameNavigationStarting se desencadena cuando un marco secundario de la vista de vista previa solicita permiso para navegar a otro URI. Esto también se activará para el redireccionamiento.

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
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

#### add_ScriptDialogOpening 

Agregue un controlador de eventos para el evento ScriptDialogOpening.

> [add_ScriptDialogOpening](#add_scriptdialogopening)de HRESULT público ([ICoreWebView2ScriptDialogOpeningEventHandler](ICoreWebView2ScriptDialogOpeningEventHandler.md) * EventHandler, EventRegistrationToken * token)

El evento se desencadena cuando se muestra un cuadro de diálogo de JavaScript (alerta, confirmación o mensaje) para la vista de la vista en WebView. Este evento solo se desencadena si la propiedad ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled se establece en false. El evento ScriptDialogOpening se puede usar para suprimir cuadros de diálogo o reemplazar los cuadros de diálogo predeterminados con cuadros de diálogo personalizados.

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<ICoreWebView2ScriptDialogOpeningEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<ICoreWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            CORE_WEBVIEW2_SCRIPT_DIALOG_KIND type;
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
                /* readonly */ type != CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<ICoreWebView2Deferral> deferral;
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

#### add_PermissionRequested 

Agregue un controlador de eventos para el evento PermissionRequested.

> [add_PermissionRequested](#add_permissionrequested)de HRESULT público ([ICoreWebView2PermissionRequestedEventHandler](ICoreWebView2PermissionRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Se desencadena cuando el contenido de una vista previa solicita permiso para acceder a algunos recursos privilegiados.

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<ICoreWebView2PermissionRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CORE_WEBVIEW2_PERMISSION_KIND kind = CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionKind(&kind));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionKind(kind);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        CORE_WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? CORE_WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? CORE_WEBVIEW2_PERMISSION_STATE_DENY
            :                     CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### remove_PermissionRequested 

Quitar un controlador de eventos agregado previamente con add_PermissionRequested.

> [remove_PermissionRequested](#remove_permissionrequested)de HRESULT público (token EventRegistrationToken)

#### add_ProcessFailed 

Agregue un controlador de eventos para el evento ProcessFailed.

> [add_ProcessFailed](#add_processfailed)de HRESULT público ([ICoreWebView2ProcessFailedEventHandler](ICoreWebView2ProcessFailedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Se desencadena cuando un proceso WebView finaliza de forma inesperada o deja de responder.

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<ICoreWebView2ProcessFailedEventHandler>(
            [this](ICoreWebView2* sender,
                ICoreWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        CORE_WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
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
        else if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser render process has stopped responding.  Recreate webview?",
                L"Web page unresponsive", MB_YESNO);
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

> [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)de HRESULT público (LPCWSTR JavaScript,[ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) * handler)

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
            Callback<ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
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

> [ExecuteScript](#executescript)de HRESULT público (LPCWSTR JavaScript,[ICoreWebView2ExecuteScriptCompletedHandler](ICoreWebView2ExecuteScriptCompletedHandler.md) * handler)

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
            Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
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

> [CAPTUREPREVIEW](#capturepreview)HRESULT público ([CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) ImageFormat, IStream * imageStream,[ICoreWebView2CapturePreviewCompletedHandler](ICoreWebView2CapturePreviewCompletedHandler.md) * handler)

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
            CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<ICoreWebView2CapturePreviewCompletedHandler>(
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

#### PostWebMessageAsJson 

Publique el mensaje de correo especificado en el documento de nivel superior en este WebView.

> HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)

Se desencadena el evento de mensaje de window. Chrome. WebView del documento de nivel superior. JavaScript en ese documento puede suscribirse y cancelar la suscripción al evento a través de lo siguiente: 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 El argumentos del evento es una instancia de `MessageEvent` . La opción ICoreWebView2Settings:: IsWebMessageEnabled debe ser true o este método dará un error con E_INVALIDARG. La propiedad de datos de Arg del evento es el parámetro de cadena WebMessage analizado como una cadena JSON en un objeto de JavaScript. La propiedad Source de Arg de evento es una referencia al `window.chrome.webview` objeto. Consulte SetWebMessageReceivedEventHandler para obtener información sobre cómo enviar mensajes desde el documento HTML de la vista en WebView al host. Este mensaje se envía de forma asincrónica. Si se produce una navegación antes de que el mensaje se publique en la página, no se enviará el mensaje.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
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

> [add_WebMessageReceived](#add_webmessagereceived)pública HRESULT (controlador[ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) *, EventRegistrationToken * token)

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

 Cuando se llama a PostMessage, se invocará el [ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) establecido a través de este método SetWebMessageReceivedEventHandler con el parámetro de objeto PostMessage convertido en una cadena JSON.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
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

#### CallDevToolsProtocolMethod 

Llama a un método DevToolsProtocol asincrónico.

> HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR NOMBREDEMÉTODO, LPCWSTR ParametersAsJson,[ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md) * handler)

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
            Callback<ICoreWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### get_BrowserProcessId 

El identificador de proceso del proceso del explorador que hospeda la vista Web.

> [get_BrowserProcessId](#get_browserprocessid)de HRESULT público (UINT32 * Value)

#### get_CanGoBack 

Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.

> [get_CanGoBack](#get_cangoback)de HRESULT público (bool * CanGoBack)

El evento HistoryChanged se activará si get_CanGoBack cambia el valor.

#### get_CanGoForward 

Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.

> [get_CanGoForward](#get_cangoforward)de HRESULT público (bool * CanGoForward)

El evento HistoryChanged se activará si get_CanGoForward cambia el valor.

#### GoBack 

Navega por la vista Web a la página anterior del historial de navegación.

> HRESULT público [GoBack](#goback)()

#### GoForward 

Navega por la vista Web a la página siguiente del historial de navegación.

> [HRESULT público](#goforward)()

#### GetDevToolsProtocolEventReceiver 

Obtén un receptor de eventos de protocolo de DevTools que te permita suscribirte a un evento de protocolo de DevTools.

> HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName,[ICoreWebView2DevToolsProtocolEventReceiver](ICoreWebView2DevToolsProtocolEventReceiver.md) * * Receiver)

El parámetro eventName es el nombre completo del evento en el formato `{domain}.{event}` . Consulte el [visor de protocolos de DevTools](https://aka.ms/DevToolsProtocolDocs) para obtener una lista de los eventos de protocolo DevTools Descripción y los argumentos del evento.

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
        wil::com_ptr<ICoreWebView2DevToolsProtocolEventReceiver> receiver;
        CHECK_FAILURE(
            m_webView->GetDevToolsProtocolEventReceiver(eventName.c_str(), &receiver));

        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(receiver->remove_DevToolsProtocolEventReceived(
                preexistingToken->second));
        }

        CHECK_FAILURE(receiver->add_DevToolsProtocolEventReceived(
            Callback<ICoreWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](
                    ICoreWebView2* sender,
                    ICoreWebView2DevToolsProtocolEventReceivedEventArgs* args) -> HRESULT {
                    wil::unique_cotaskmem_string parameterObjectAsJson;
                    CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
                    MessageBox(
                        nullptr, parameterObjectAsJson.get(),
                        (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
                    return S_OK;
                })
                .Get(),
            &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### Detener 

Detenga todas las navegaciones y las búsquedas de recursos pendientes.

> [HRESULT público](#stop)()

No detiene las secuencias de comandos.

#### add_NewWindowRequested 

Agregue un controlador de eventos para el evento NewWindowRequested.

> [add_NewWindowRequested](#add_newwindowrequested)de HRESULT público ([ICoreWebView2NewWindowRequestedEventHandler](ICoreWebView2NewWindowRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Se desencadena cuando el contenido de la vista en WebView solicita abrir una nueva ventana, por ejemplo, a través de window. Open. La aplicación puede pasar una vista previa de destino que se considerará la ventana abierta.

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<ICoreWebView2NewWindowRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<ICoreWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));

                auto newAppWindow = new AppWindow(L"");
                newAppWindow->m_isPopupWindow = true;
                newAppWindow->m_onWebViewFirstInitialized = [args, deferral, newAppWindow]() {
                    CHECK_FAILURE(args->put_NewWindow(newAppWindow->m_webView.get()));
                    CHECK_FAILURE(args->put_Handled(TRUE));
                    CHECK_FAILURE(deferral->Complete());
                };

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_NewWindowRequested 

Quitar un controlador de eventos agregado previamente con add_NewWindowRequested.

> [remove_NewWindowRequested](#remove_newwindowrequested)de HRESULT público (token EventRegistrationToken)

#### add_DocumentTitleChanged 

Agregue un controlador de eventos para el evento DocumentTitleChanged.

> [add_DocumentTitleChanged](#add_documenttitlechanged)de HRESULT público ([ICoreWebView2DocumentTitleChangedEventHandler](ICoreWebView2DocumentTitleChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

El evento se desencadena cuando la propiedad DocumentTitle de WebView cambia y se puede activar antes o después del evento NavigationCompleted.

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<ICoreWebView2DocumentTitleChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### remove_DocumentTitleChanged 

Quitar un controlador de eventos agregado previamente con add_DocumentTitleChanged.

> [remove_DocumentTitleChanged](#remove_documenttitlechanged)de HRESULT público (token EventRegistrationToken)

#### get_DocumentTitle 

Título del documento de nivel superior actual.

> [get_DocumentTitleción](#get_documenttitle)HRESULT pública (título LPWStr *)

Si el documento no tiene un título explícito o no está vacío, de lo contrario, se usará un valor predeterminado que puede o no coincidir con el URI del documento.

#### AddRemoteObject 

Agregue el objeto host proporcionado a la secuencia de comandos que se ejecuta en la vista Webcon el nombre especificado.

> [ADDREMOTEOBJECT](#addremoteobject)HRESULT público (LPCWSTR Name, Variant * Object)

Los objetos de host se exponen como proxies de objetos remotos a través de `window.chrome.webview.remoteObjects.<name>` . Los proxies de objetos remotos son promesas y se resolverán como un objeto que represente el objeto de host. La promesa se rechaza si la aplicación no ha agregado un objeto con el nombre. Cuando el código de JavaScript tiene acceso a una propiedad o método del objeto, se devuelve una promesa, que se resolverá con el valor devuelto por el host para la propiedad o el método, o se rechazará en caso de error, como no se trata de una propiedad o método en el objeto o los parámetros no son válidos. Por ejemplo, cuando el código de la aplicación hace lo siguiente: 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 El código de JavaScript de WebView podrá acceder a appObject como sigue y, a continuación, a los atributos y métodos de appObject: 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 Tenga en cuenta que aunque se admiten tipos simples, IDispatch y matriz, no se admiten IUnknown genérico, VT_DECIMAL o VT_RECORD Variant. Los objetos remotos de JavaScript, como las funciones de devolución de llamada, se representan como una variante VT_DISPATCH con el objeto que implementa IDispatch. El método de devolución de llamada de JavaScript se puede invocar con DISPID_VALUE para el DispId. Las matrices anidadas se admiten hasta una profundidad de 3. No se admiten las matrices de los tipos de referencia. VT_EMPTY y VT_NULL se asignan a JavaScript como null. En JavaScript, los valores NULL y undefined se asignan a VT_EMPTY.

Además, todos los objetos remotos se exponen como `window.chrome.webview.remoteObjects.sync.<name>` . Aquí los objetos host se exponen como proxies de objetos remotos sincrónicos. No se trata de promesas ni llamadas a funciones o acceso a propiedad de forma sincrónica bloquear la ejecución de scripts en espera de comunicar el proceso cruzado para que se ejecute el código de host. Por consiguiente, esto puede dar lugar a problemas de confiabilidad y se recomienda usar la API asíncrona basada en Promise `window.chrome.webview.remoteObjects.<name>` descrita anteriormente.

Los proxies de objetos remotos sincrónicos y los proxies asincrónicos de objetos remotos pueden tener como proxy el mismo objeto remoto. Los cambios remotos realizados por un proxy se reflejarán en cualquier otro proxy de ese mismo objeto remoto, ya sean otros servidores proxy, sincrónicos o asíncronos.

Aunque JavaScript está bloqueado en una llamada sincrónica al código nativo, ese código nativo no puede devolver la llamada a JavaScript. Los intentos de hacerlo fallarán con HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).

Los proxies de objetos remotos son objetos proxy de JavaScript que interceptan todas las llamadas a propiedades get, Set Property y Method. Las propiedades o métodos que forman parte de la función o del prototipo de objeto se ejecutan de forma local. Además, cualquier propiedad o método de la matriz se `chrome.webview.remoteObjects.options.forceLocalProperties` ejecutará de forma local. De forma predeterminada, se incluyen métodos opcionales que tienen significado en JavaScript como `toJSON` y `Symbol.toPrimitive` . Puede agregar más a esta matriz, según sea necesario.

Hay un método que puede resultar `chrome.webview.remoteObjects.cleanupSome` más conveniente para la recolección de objetos remotos.

Los proxies de objetos remotos también tienen los siguientes métodos que se ejecutan de forma local:

* applyRemote, getRemote, setRemote: realizar una invocación de método, una propiedad get o un conjunto de propiedades en el objeto remoto. Puede usarlos para obligar a que un método o una propiedad se ejecuten de forma remota si hay una propiedad o un método local en conflicto. Por ejemplo, `proxy.toString()` ejecutará el método toString local en el objeto de proxy. Pero `proxy.applyRemote('toString')` se ejecuta `toString` en el objeto remoto a través del proxy.

* getLocal, setLocal: realizar obtención de propiedad o conjunto de propiedades de forma local. Puede usar estos métodos para forzar o establecer una propiedad en el proxy del objeto remoto, en lugar de hacerlo en el objeto remoto al que representa. Por ejemplo, `proxy.unknownProperty` obtendrá la propiedad nombrada `unknownProperty` desde el objeto remoto a través del proxy. Pero `proxy.getLocal('unknownProperty')` obtendrá el valor de la propiedad `unknownProperty` en el propio objeto proxy.

* sincronizar: los proxies de objetos remotos asincrónicos exponen un método de sincronización que devuelve una promesa de un proxy de objetos remotos sincrónico para el mismo objeto remoto. Por ejemplo, `chrome.webview.remoteObjects.sample.methodCall()` devuelve un proxy asincrónico de objeto remoto. Puede usar el `sync` método para obtener un proxy de objetos remotos sincrónico en su lugar: `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* Async: los proxies de objetos remotos sincrónicos exponen un método Async que bloquea y devuelve un proxy de objetos remotos asincrónicos para el mismo objeto remoto. Por ejemplo, `chrome.webview.remoteObjects.sync.sample.methodCall()` devuelve un proxy de objeto remoto sincrónico. Se llama al `async` método de este bloque y, a continuación, se devuelve un proxy de objeto remoto asincrónico para el mismo objeto remoto: `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* después: los proxies de objetos remotos asincrónicos tienen un método then. Esto permite que sean esperados. `then` devolverá una promesa que se resolverá con una representación del objeto remoto. Si el proxy representa un literal de JavaScript, se devuelve una copia de forma local. Si el proxy representa una función, se devuelve un proxy que no es de espera. Si el proxy representa un objeto de JavaScript con una combinación de propiedades literales y propiedades de función, se devuelve una copia del objeto con algunas propiedades como proxy de objetos remotos.

Todas las demás invocaciones a propiedades y métodos (excepto los métodos anteriores de proxy de objeto remoto, la lista de forceLocalProperties y las propiedades de los prototipos de funciones y objetos) se ejecutan de forma remota. Los proxies de objetos remotos asincrónicos devuelven una promesa que representa la finalización asincrónica de la invocación remota del método u obtiene la propiedad. La función Promise se resuelve después de que las operaciones remotas se completen y las promesas se resuelven en el valor resultante de la operación. Los proxy de objetos remotos sincrónicos funcionan de manera similar pero bloquean la ejecución remota y esperan a que se complete la operación remota.

Establecer una propiedad en un proxy de objetos remotos asincrónicos funciona de forma ligeramente distinta. El conjunto devolverá inmediatamente y el valor devuelto es el valor que se establecerá. Este es un requisito del objeto proxy de JavaScript. Si necesita esperar de forma asincrónica para que se complete el conjunto de propiedades, use el método setRemote que devuelve una promesa según se describe anteriormente. La propiedad sincrónico del conjunto de propiedades de objeto se bloquea de forma sincrónica hasta que se establece la propiedad.

Por ejemplo, supongamos que tiene un objeto COM con la siguiente interfaz

```IDL
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IRemoteObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);
    };
```

 Podemos añadir una instancia de esta interfaz a nuestro JavaScript con `AddRemoteObject` . En este caso, lo hemos denominado `sample` :

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_remoteObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddRemoteObject multiple times in a row without
            // calling RemoveRemoteObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(m_webView->AddRemoteObject(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```

 A continuación, en el documento HTML podemos usar este objeto COM mediante `chrome.webview.remoteObjects.sample` :

```js
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = await chrome.webview.remoteObjects.sample.property;
            document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
            const propertyValue = chrome.webview.remoteObjects.sync.sample.property;
            document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyAsyncInput").value;
            // The following line will work but it will return immediately before the property value has actually been set.
            // If you need to set the property and wait for the property to change value, use the setRemote function.
            chrome.webview.remoteObjects.sample.property = propertyValue;
            document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
            // If you care about waiting until the property has actually changed value use the setRemote function.
            await chrome.webview.remoteObjects.sample.setRemote("property", propertyValue);
            document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
            const propertyValue = document.getElementById("setPropertySyncInput").value;
            chrome.webview.remoteObjects.sync.sample.property = propertyValue;
            document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
            const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
            const resultValue = await chrome.webview.remoteObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
            const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
            const resultValue = chrome.webview.remoteObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
            chrome.webview.remoteObjects.sample.CallCallbackAsynchronously(() => {
                document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
            });
        });
```

#### RemoveRemoteObject 

Quite el objeto host especificado por el nombre para que ya no se pueda tener acceso al mismo desde el código de JavaScript de la vista.

> [REMOVEREMOTEOBJECT](#removeremoteobject)HRESULT público (LPCWSTR Name)

Aunque se denegarán nuevos intentos de acceso, si el código de JavaScript ya ha obtenido el objeto, el código de JavaScript seguirá teniendo acceso a ese objeto. Llamar a este método para un nombre que ya se ha quitado o no se ha agregado nunca producirá un error.

#### OpenDevToolsWindow 

Abre la ventana DevTools para el documento actual en la vista de vistas en WebView.

> [OPENDEVTOOLSWINDOW](#opendevtoolswindow)HRESULT público ()

No hace nada si se llama cuando la ventana de DevTools ya está abierta

#### add_ContainsFullScreenElementChanged 

Notifica cuando cambia la propiedad ContainsFullScreenElement.

> [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)de HRESULT público ([ICoreWebView2ContainsFullScreenElementChangedEventHandler](ICoreWebView2ContainsFullScreenElementChangedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Esto significa que un elemento HTML dentro de la vista de WebView está escribiendo Fullscreen en el tamaño de WebView o saliendo de pantalla completa. Este evento es útil cuando, por ejemplo, un elemento de vídeo solicita la pantalla completa. El agente de escucha de ContainsFullScreenElementChanged puede cambiar el tamaño de la vista en WebView en respuesta.

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<ICoreWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(
                        sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
                    if (m_containsFullscreenElement)
                    {
                        EnterFullScreen();
                    }
                    else
                    {
                        ExitFullScreen();
                    }
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_ContainsFullScreenElementChanged 

Quitar un controlador de eventos agregado previamente con el método de evento add_ correspondiente.

> [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)de HRESULT público (token EventRegistrationToken)

#### get_ContainsFullScreenElement 

Indica si WebView contiene un elemento HTML de pantalla completa.

> [get_ContainsFullScreenElement](#get_containsfullscreenelement)de HRESULT público (bool * ContainsFullScreenElement)

#### add_WebResourceRequested 

Agregue un controlador de eventos para el evento WebResourceRequested.

> [add_WebResourceRequested](#add_webresourcerequested)de HRESULT público ([ICoreWebView2WebResourceRequestedEventHandler](ICoreWebView2WebResourceRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Se desencadena cuando WebView realiza una solicitud HTTP a una dirección URL y un filtro de contexto de recursos coincidentes que se agregaron con AddWebResourceRequestedFilter. Debe agregar al menos un filtro para que se active el evento.

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<ICoreWebView2WebResourceResponse> response;
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

#### AddWebResourceRequestedFilter 

Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.

> [ADDWEBRESOURCEREQUESTEDFILTER](#addwebresourcerequestedfilter)HRESULT público (LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)

El parámetro URI puede ser una cadena comodín (' ': cero o más, '? ': exactamente uno). nullptr es equivalente a L "". Consulta CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT enum para obtener una descripción de los filtros de contexto de recursos.

#### RemoveWebResourceRequestedFilter 

Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.

> [REMOVEWEBRESOURCEREQUESTEDFILTER](#removewebresourcerequestedfilter)HRESULT público (LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const resourceContext)

Si se agregó el mismo filtro varias veces, tendrá que quitarlo tantas veces como se agregara para que la eliminación sea efectiva. Devuelve E_INVALIDARG para un filtro que nunca se ha agregado.

#### add_WindowCloseRequested 

Agregue un controlador de eventos para el evento WindowCloseRequested.

> [add_WindowCloseRequested](#add_windowcloserequested)de HRESULT público ([ICoreWebView2WindowCloseRequestedEventHandler](ICoreWebView2WindowCloseRequestedEventHandler.md) * EventHandler, EventRegistrationToken * token)

Se desencadena cuando el contenido de la vista en WebView solicita cerrar la ventana, por ejemplo, después de que se llame a Window. Close. La aplicación debe cerrar la ventana de WebView y de la aplicación relacionada si eso tiene sentido para la aplicación.

```cpp
    // Register a handler for the WindowCloseRequested event.
    // This handler will close the app window if it is not the main window.
    CHECK_FAILURE(m_webView->add_WindowCloseRequested(
        Callback<ICoreWebView2WindowCloseRequestedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) {
                if (m_isPopupWindow)
                {
                    CloseAppWindow();
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_WindowCloseRequested 

Quitar un controlador de eventos agregado previamente con add_WindowCloseRequested.

> [remove_WindowCloseRequested](#remove_windowcloserequested)de HRESULT público (token EventRegistrationToken)

#### CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT 

Formato de imagen usado por el método ICoreWebView2:: CapturePreview.

> [CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG            | Formato de imagen PNG.
CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG            | Formato de imagen JPEG.

#### CORE_WEBVIEW2_SCRIPT_DIALOG_KIND 

Cuadro de diálogo tipo de JavaScript usado en la interfaz ICoreWebView2ScriptDialogOpeningEventHandler.

> [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT            | Un cuadro de diálogo invocado a través de la función de JavaScript Window. Alert.
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM            | Un cuadro de diálogo invocado a través de la función de la ventana. confirmar JavaScript.
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT            | Un cuadro de diálogo invocado a través de la función de aviso de JavaScript.
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD            | Un cuadro de diálogo invocado a través del evento beforeunload de JavaScript.

#### CORE_WEBVIEW2_PROCESS_FAILED_KIND 

Tipo de error de proceso usado en la interfaz de ICoreWebView2ProcessFailedEventHandler.

> [CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED            | Indica que el proceso del explorador ha terminado de forma inesperada.
CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED            | Indica que el proceso de representación ha terminado de forma inesperada.
CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE            | Indica que el proceso de representación deja de responder.

#### CORE_WEBVIEW2_PERMISSION_KIND 

El tipo de una solicitud de permiso.

> [CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION            | Permiso desconocido.
CORE_WEBVIEW2_PERMISSION_KIND_MICROPHONE            | Permiso para capturar audio.
CORE_WEBVIEW2_PERMISSION_KIND_CAMERA            | Permiso para capturar video.
CORE_WEBVIEW2_PERMISSION_KIND_GEOLOCATION            | Permiso para acceder a la ubicación geográfica.
CORE_WEBVIEW2_PERMISSION_KIND_NOTIFICATIONS            | Permiso para enviar notificaciones Web.
CORE_WEBVIEW2_PERMISSION_KIND_OTHER_SENSORS            | Permiso para acceder al sensor genérico.
CORE_WEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ            | Permiso para leer el Portapapeles del sistema sin un gesto de usuario.

#### CORE_WEBVIEW2_PERMISSION_STATE 

Respuesta a una solicitud de permiso.

> [CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT            | Use el comportamiento de explorador predeterminado, que suele solicitar a los usuarios la decisión.
CORE_WEBVIEW2_PERMISSION_STATE_ALLOW            | Otorgue la solicitud de permiso.
CORE_WEBVIEW2_PERMISSION_STATE_DENY            | Denegar la solicitud de permiso.

#### CORE_WEBVIEW2_WEB_ERROR_STATUS 

Valores de estado de error para navegaciones Web.

> [CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN            | Se ha producido un error desconocido.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT            | El nombre común del certificado SSL no coincide con la dirección Web.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED            | El certificado SSL ha expirado.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS            | El certificado de cliente SSL contiene errores.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED            | El certificado SSL ha sido revocado.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID            | El certificado SSL no es válido &ndash; esto puede significar que el certificado no coincide con los pin de clave pública del nombre de host, que el certificado está firmado por una autoridad que no es de confianza o con un algoritmo de signo débil. el certificado alegó que los nombres DNS han infringido las restricciones de nombres, el certificado contiene una clave débil, el período de validez del certificado es demasiado largo, falta de información de revocación o de mecanismo de revocación, nombre de host no único, falta de información de transparencia del certificado o el certificado está encadenado a una [raíz de Symantec heredado](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).
CORE_WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE            | No se puede comunicar con el host.
CORE_WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT            | Se agotó el tiempo de espera de la conexión.
CORE_WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE            | El servidor ha devuelto una respuesta no válida o no reconocida.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED            | La conexión ha sido cancelada.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET            | Se restableció la conexión.
CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED            | Se perdió la conexión a Internet.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT            | No se puede conectar al destino.
CORE_WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED            | No se pudo resolver el nombre de host proporcionado.
CORE_WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED            | Se canceló la operación.
CORE_WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED            | Error en la redirección de la solicitud.
CORE_WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR            | Se ha producido un error inesperado.

#### CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT 

Enumeración de contextos de solicitud de recursos Web.

> [CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL            | Todos los recursos.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT            | Recursos de documentos.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET            | Recursos de CSS.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE            | Recursos de imagen.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA            | Otros recursos multimedia, como los vídeos.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT            | Recursos de fuentes.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT            | Recursos de script.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST            | Solicitudes XML HTTP.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH            | Capture la comunicación de la API.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK            | Recursos de TextTrack.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE            | Comunicación de la API de EventSource.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET            | Comunicación de API WebSocket.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST            | Manifiestos de la aplicación Web.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE            | Intercambio de HTTP firmado.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_PING            | Solicitudes de ping.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT            | Informes de violación de CSP.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER            | Otros recursos.

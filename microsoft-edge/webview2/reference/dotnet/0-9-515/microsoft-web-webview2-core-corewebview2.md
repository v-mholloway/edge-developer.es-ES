---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: ef2932ef883477a3340674f6a7b00d25bcbaad80
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885166"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2 (clase) 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

WebView2 le permite hospedar contenido web con la tecnología de explorador Web más reciente.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[BrowserProcessId](#browserprocessid) | El identificador de proceso del proceso del explorador que hospeda la vista Web.
[CanGoBack](#cangoback) | Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.
[CanGoForward](#cangoforward) | Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.
[ContainsFullScreenElement](#containsfullscreenelement) | Indica si WebView contiene un elemento HTML de pantalla completa.
[ContainsFullScreenElementChanged](#containsfullscreenelementchanged) | Notifica cuando cambia la propiedad ContainsFullScreenElement.
[ContentLoading](#contentloading) | ContentLoading se activa antes de que se cargue ningún contenido, incluso los scripts agregados con AddScriptToExecuteOnDocumentCreated ContentLoading no se desencadenarán si se realiza una navegación de página (por ejemplo, a través de la navegación de fragmentos o el historial. navegaciones pushState).
[DocumentTitle](#documenttitle) | Título del documento de nivel superior actual.
[DocumentTitleChanged](#documenttitlechanged) | El evento se desencadena cuando la propiedad DocumentTitle de WebView cambia y se puede activar antes o después del evento NavigationCompleted.
[FrameNavigationCompleted](#framenavigationcompleted) | El evento FrameNavigationCompleted se desencadena cuando se ha cargado por completo un fotograma secundario (Body. onload) o la carga se ha detenido con error.
[FrameNavigationStarting](#framenavigationstarting) | FrameNavigationStarting se desencadena cuando un marco secundario de la vista de vista previa solicita permiso para navegar a otro URI.
[HistoryChanged](#historychanged) | Facturacióncambiar escuchar el cambio del historial de navegación en el documento de nivel superior.
[NavigationCompleted](#navigationcompleted) | El evento NavigationCompleted se desencadena cuando WebView se ha cargado completamente (Body. onload se ha desencadenado) o se ha detenido con error.
[NavigationStarting](#navigationstarting) | NavigationStarting se desencadena cuando el marco principal de vista previa solicita permiso para navegar a otro URI.
[NewWindowRequested](#newwindowrequested) | Se desencadena cuando el contenido de la vista en WebView solicita abrir una nueva ventana, por ejemplo, a través de window. Open.
[PermissionRequested](#permissionrequested) | Se desencadena cuando el contenido de una vista previa solicita permiso para acceder a algunos recursos privilegiados.
[ProcessFailed](#processfailed) | Se desencadena cuando un proceso WebView finaliza de forma inesperada o deja de responder.
[ScriptDialogOpening](#scriptdialogopening) | El evento se desencadena cuando se muestra un cuadro de diálogo de JavaScript (alerta, confirmación o mensaje) para la vista de la vista en WebView.
[Configuración](#settings) | El objeto CoreWebView2Settings contiene varios valores modificables para el
[Source](#source) | Identificador URI del documento de nivel superior actual.
[SourceChanged](#sourcechanged) | SourceChanged se desencadena cuando cambia la propiedad de origen.
[WebMessageReceived](#webmessagereceived) | Este evento se desencadena cuando se establece la configuración de IsWebMessageEnabled y el documento de nivel superior de las llamadas de WebView `window.chrome.webview.postMessage` .
[WebResourceRequested](#webresourcerequested) | Se desencadena cuando WebView realiza una solicitud HTTP a una dirección URL y un filtro de contexto de recursos coincidentes que se agregaron con AddWebResourceRequestedFilter.
[WindowCloseRequested](#windowcloserequested) | Se desencadena cuando el contenido de la vista en WebView solicita cerrar la ventana, por ejemplo, después de que se llame a Window. Close.
[AddHostObjectToScript](#addhostobjecttoscript) | Agregue el objeto host proporcionado a la secuencia de comandos que se ejecuta en la vista Webcon el nombre especificado.
[AddScriptToExecuteOnDocumentCreatedAsync](#addscripttoexecuteondocumentcreatedasync) | Agregue el JavaScript proporcionado a una lista de scripts que se deben ejecutar después de que se haya creado el objeto global, pero antes de que se haya analizado el documento HTML y antes de que se ejecute cualquier otro script incluido en el documento HTML.
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.
[CallDevToolsProtocolMethodAsync](#calldevtoolsprotocolmethodasync) | Llama a un método DevToolsProtocol asincrónico.
[CapturePreviewAsync](#capturepreviewasync) | Capture una imagen de lo que se muestra en la vista de página.
[ExecuteScriptAsync](#executescriptasync) | Ejecute el código JavaScript desde el parámetro de JavaScript en el documento de nivel superior actual representado en la vista de vistas en WebView.
[GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver) | Obtén un receptor de eventos de protocolo de DevTools que te permita suscribirte a un evento de protocolo de DevTools.
[GoBack](#goback) | Navega por la vista Web a la página anterior del historial de navegación.
[GoForward](#goforward) | Navega por la vista Web a la página siguiente del historial de navegación.
[Busque](#navigate) | Hacer que la navegación del documento de nivel superior sea la dirección URI especificada.
[NavigateToString](#navigatetostring) | Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.
[OpenDevToolsWindow](#opendevtoolswindow) | Abre la ventana DevTools para el documento actual en la vista de vistas en WebView.
[PostWebMessageAsJson](#postwebmessageasjson) | Publique el mensaje de correo especificado en el documento de nivel superior en este WebView.
[PostWebMessageAsString](#postwebmessageasstring) | Este es un auxiliar para publicar un mensaje que es una cadena simple en lugar de una representación de cadena JSON de un objeto de JavaScript.
[Volver a cargar](#reload) | Volver a cargar la página actual.
[RemoveHostObjectFromScript](#removehostobjectfromscript) | Quite el objeto host especificado por el nombre para que ya no se pueda tener acceso al mismo desde el código de JavaScript de la vista.
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | Quite el JavaScript correspondiente agregado a través de AddScriptToExecuteOnDocumentCreated.
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.
[Detener](#stop) | Detenga todas las navegaciones y las búsquedas de recursos pendientes.

## Miembros

#### BrowserProcessId 

El identificador de proceso del proceso del explorador que hospeda la vista Web.

> uint pública [BrowserProcessId](#browserprocessid)

#### CanGoBack 

Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.

> Public bool [CanGoBack](#cangoback)

El evento HistoryChanged se desencadenará si CanGoBack cambia el valor.

#### CanGoForward 

Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.

> Public bool [CanGoForward](#cangoforward)

El evento HistoryChanged se desencadenará si CanGoForward cambia el valor.

#### ContainsFullScreenElement 

Indica si WebView contiene un elemento HTML de pantalla completa.

> Public bool [ContainsFullScreenElement](#containsfullscreenelement)

#### ContainsFullScreenElementChanged 

Notifica cuando cambia la propiedad ContainsFullScreenElement.

> evento público EventHandler< > [ContainsFullScreenElementChanged](#containsfullscreenelementchanged)

Esto significa que un elemento HTML dentro de la vista de WebView está escribiendo Fullscreen en el tamaño de WebView o saliendo de pantalla completa. Este evento es útil cuando, por ejemplo, un elemento de vídeo solicita la pantalla completa. El agente de escucha de ContainsFullScreenElementChanged puede cambiar el tamaño de la vista en WebView en respuesta.

#### ContentLoading 

ContentLoading se activa antes de que se cargue ningún contenido, incluso los scripts agregados con AddScriptToExecuteOnDocumentCreated ContentLoading no se desencadenarán si se realiza una navegación de página (por ejemplo, a través de la navegación de fragmentos o el historial. navegaciones pushState).

> evento público EventHandler< [CoreWebView2ContentLoadingEventArgs](microsoft-web-webview2-core-corewebview2contentloadingeventargs.md)  >  [ContentLoading](#contentloading)

Esto sigue los eventos NavigationStarting y SourceChanged, y precede a los eventos HistoryChanged y NavigationCompleted.

#### DocumentTitle 

Título del documento de nivel superior actual.

> cadena pública [DocumentTitle](#documenttitle)

Si el documento no tiene un título explícito o no está vacío, de lo contrario, se usará un valor predeterminado que puede o no coincidir con el URI del documento.

#### DocumentTitleChanged 

El evento se desencadena cuando la propiedad DocumentTitle de WebView cambia y se puede activar antes o después del evento NavigationCompleted.

> evento público EventHandler< > [DocumentTitleChanged](#documenttitlechanged)

#### FrameNavigationCompleted 

El evento FrameNavigationCompleted se desencadena cuando se ha cargado por completo un fotograma secundario (Body. onload) o la carga se ha detenido con error.

> evento público EventHandler< [CoreWebView2NavigationCompletedEventArgs](microsoft-web-webview2-core-corewebview2navigationcompletedeventargs.md)  >  [FrameNavigationCompleted](#framenavigationcompleted)

#### FrameNavigationStarting 

FrameNavigationStarting se desencadena cuando un marco secundario de la vista de vista previa solicita permiso para navegar a otro URI.

> evento público EventHandler< [CoreWebView2NavigationStartingEventArgs](microsoft-web-webview2-core-corewebview2navigationstartingeventargs.md)  >  [FrameNavigationStarting](#framenavigationstarting)

Esto también se activará para el redireccionamiento.

#### HistoryChanged 

Facturacióncambiar escuchar el cambio del historial de navegación en el documento de nivel superior.

> evento público EventHandler< > [HistoryChanged](#historychanged)

Usa Facturacióncambiar para comprobar si el valor CanGoBack/CanGoForward ha cambiado. HistoryChanged también se desencadena para usar GoBack/GoForward. HistoryChanged se desencadena después de SourceChanged y ContentLoading. Agregue un controlador de eventos para el evento HistoryChanged.

#### NavigationCompleted 

El evento NavigationCompleted se desencadena cuando WebView se ha cargado completamente (Body. onload se ha desencadenado) o se ha detenido con error.

> evento público EventHandler< [CoreWebView2NavigationCompletedEventArgs](microsoft-web-webview2-core-corewebview2navigationcompletedeventargs.md)  >  [NavigationCompleted](#navigationcompleted)

#### NavigationStarting 

NavigationStarting se desencadena cuando el marco principal de vista previa solicita permiso para navegar a otro URI.

> evento público EventHandler< [CoreWebView2NavigationStartingEventArgs](microsoft-web-webview2-core-corewebview2navigationstartingeventargs.md)  >  [NavigationStarting](#navigationstarting)

Esto también se activará para el redireccionamiento.

#### NewWindowRequested 

Se desencadena cuando el contenido de la vista en WebView solicita abrir una nueva ventana, por ejemplo, a través de window. Open.

> evento público EventHandler< [CoreWebView2NewWindowRequestedEventArgs](microsoft-web-webview2-core-corewebview2newwindowrequestedeventargs.md)  >  [NewWindowRequested](#newwindowrequested)

La aplicación puede pasar una vista previa de destino que se considerará la ventana abierta.

#### PermissionRequested 

Se desencadena cuando el contenido de una vista previa solicita permiso para acceder a algunos recursos privilegiados.

> evento público EventHandler< [CoreWebView2PermissionRequestedEventArgs](microsoft-web-webview2-core-corewebview2permissionrequestedeventargs.md)  >  [PermissionRequested](#permissionrequested)

#### ProcessFailed 

Se desencadena cuando un proceso WebView finaliza de forma inesperada o deja de responder.

> evento público EventHandler< [CoreWebView2ProcessFailedEventArgs](microsoft-web-webview2-core-corewebview2processfailedeventargs.md)  >  [ProcessFailed](#processfailed)

#### ScriptDialogOpening 

El evento se desencadena cuando se muestra un cuadro de diálogo de JavaScript (alerta, confirmación o mensaje) para la vista de la vista en WebView.

> evento público EventHandler< [CoreWebView2ScriptDialogOpeningEventArgs](microsoft-web-webview2-core-corewebview2scriptdialogopeningeventargs.md)  >  [ScriptDialogOpening](#scriptdialogopening)

Este evento solo se desencadena si la propiedad CoreWebView2Settings. AreDefaultScriptDialogsEnabled se establece en false. El evento ScriptDialogOpening se puede usar para suprimir cuadros de diálogo o reemplazar los cuadros de diálogo predeterminados con cuadros de diálogo personalizados.

#### Configuración 

El objeto CoreWebView2Settings contiene varios valores modificables para el

> [configuración](#settings) de [CoreWebView2Settings](microsoft-web-webview2-core-corewebview2settings.md) pública

#### Source 

Identificador URI del documento de nivel superior actual.

> [origen](#source) de cadena público

Este valor puede cambiar potencialmente como parte del desencadenador de eventos SourceChanged en algunos casos, como navegar a un sitio o navegación de fragmentos diferentes. Permanecerá igual para otros tipos de navegación, como recargas de páginas o historial. pushState con la misma dirección URL que la página actual.

#### SourceChanged 

SourceChanged se desencadena cuando cambia la propiedad de origen.

> evento público EventHandler< [CoreWebView2SourceChangedEventArgs](microsoft-web-webview2-core-corewebview2sourcechangedeventargs.md)  >  [SourceChanged](#sourcechanged)

SourceChanged se desencadena para navegar a un sitio diferente o a navegación de fragmentos. No se desencadenará para otros tipos de navegación, como recargas de páginas o historial. pushState con la misma dirección URL que la página actual. SourceChanged se desencadena antes de ContentLoading para la navegación a un nuevo documento. Agregue un controlador de eventos para el evento SourceChanged.

#### WebMessageReceived 

Este evento se desencadena cuando se establece la configuración de IsWebMessageEnabled y el documento de nivel superior de las llamadas de WebView `window.chrome.webview.postMessage` .

> evento público EventHandler< [CoreWebView2WebMessageReceivedEventArgs](microsoft-web-webview2-core-corewebview2webmessagereceivedeventargs.md)  >  [WebMessageReceived](#webmessagereceived)

La función postmensaje es `void postMessage(object)` donde objeto es cualquier objeto compatible con la conversión de JSON. Cuando se llama a PostMessage, el conjunto de CoreWebView2WebMessageReceivedEventHandler se invocará con el parámetro de objeto PostMessage convertido en una cadena JSON.

#### WebResourceRequested 

Se desencadena cuando WebView realiza una solicitud HTTP a una dirección URL y un filtro de contexto de recursos coincidentes que se agregaron con AddWebResourceRequestedFilter.

> evento público EventHandler< [CoreWebView2WebResourceRequestedEventArgs](microsoft-web-webview2-core-corewebview2webresourcerequestedeventargs.md)  >  [WebResourceRequested](#webresourcerequested)

Debe agregar al menos un filtro para que se active el evento.

#### WindowCloseRequested 

Se desencadena cuando el contenido de la vista en WebView solicita cerrar la ventana, por ejemplo, después de que se llame a Window. Close.

> evento público EventHandler< > [WindowCloseRequested](#windowcloserequested)

La aplicación debe cerrar la ventana de WebView y de la aplicación relacionada si eso tiene sentido para la aplicación.

#### AddHostObjectToScript 

Agregue el objeto host proporcionado a la secuencia de comandos que se ejecuta en la vista Webcon el nombre especificado.

> public void [AddHostObjectToScript](#addhostobjecttoscript)(string name, Object rawObject)

Los objetos de host se exponen como proxies de objeto de host a través de `window.chrome.webview.hostObjects.{name}` . Los proxies de objeto host son promesas y se resolverán como un objeto que representa el objeto host. El código de JavaScript de WebView podrá acceder a appObject como sigue y, a continuación, a los atributos y métodos de appObject: 
```
let app_object = await window.chrome.webview.hostObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```
 Tenga en cuenta que aunque se admiten tipos simples, IDispatch y matriz, no se admiten IUnknown genérico, VT_DECIMAL o VT_RECORD Variant. Los objetos remotos de JavaScript, como las funciones de devolución de llamada, se representan como una variante VT_DISPATCH con el objeto que implementa IDispatch. El método de devolución de llamada de JavaScript se puede invocar con DISPID_VALUE para el DispId. Las matrices anidadas se admiten hasta una profundidad de 3. No se admiten las matrices de los tipos de referencia. VT_EMPTY y VT_NULL se asignan a JavaScript como null. En JavaScript, los valores NULL y undefined se asignan a VT_EMPTY.

Además, todos los objetos host se exponen como `window.chrome.webview.hostObjects.sync.{name}` . Aquí los objetos host se exponen como proxies de objetos de host sincrónico. No se trata de promesas ni llamadas a funciones o acceso a propiedad de forma sincrónica bloquear la ejecución de scripts en espera de comunicar el proceso cruzado para que se ejecute el código de host. Por consiguiente, esto puede dar lugar a problemas de confiabilidad y se recomienda usar la API asíncrona basada en Promise `window.chrome.webview.hostObjects.{name}` descrita anteriormente.

Los proxies de objetos host sincrónicos y los proxies de objetos host asincrónicos pueden obtener el mismo objeto de host. Los cambios remotos realizados por un proxy se reflejarán en cualquier otro proxy de ese mismo objeto host, ya sean otros servidores proxy, sincrónicos o asíncronos.

Aunque JavaScript está bloqueado en una llamada sincrónica al código nativo, ese código nativo no puede devolver la llamada a JavaScript. Los intentos de hacerlo fallarán con HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).

Los proxies de objetos de hospedaje son objetos proxy de JavaScript que interceptan todas las llamadas a propiedades get, Set Property y Method. Las propiedades o métodos que forman parte de la función o del prototipo de objeto se ejecutan de forma local. Además, cualquier propiedad o método de la matriz se `chrome.webview.hostObjects.options.forceLocalProperties` ejecutará de forma local. De forma predeterminada, se incluyen métodos opcionales que tienen significado en JavaScript como `toJSON` y `Symbol.toPrimitive` . Puede agregar más a esta matriz, según sea necesario.

Hay un método que puede resultar `chrome.webview.hostObjects.cleanupSome` más conveniente para la recolección de objetos host.

Los proxies de objetos de hospedaje también tienen los siguientes métodos que se ejecutan de forma local:

* applyHostFunction, getHostProperty, setHostProperty: realizar una invocación de método, una propiedad get o un conjunto de propiedades en el objeto host. Puede usarlos para obligar a que un método o una propiedad se ejecuten de forma remota si hay una propiedad o un método local en conflicto. Por ejemplo, `proxy.toString()` ejecutará el método toString local en el objeto de proxy. Pero `proxy.applyHostFunction('toString')` se ejecuta `toString` en el objeto de proxy del host.

* getLocalProperty, setLocalProperty: propiedad get o conjunto de propiedades de forma local. Puede usar estos métodos para forzar la obtención o la configuración de una propiedad en el proxy del objeto host, en lugar de en el objeto host que representa. Por ejemplo, `proxy.unknownProperty` obtendrá la propiedad nombrada `unknownProperty` desde el objeto de proxy del host. Pero `proxy.getLocalProperty('unknownProperty')` obtendrá el valor de la propiedad `unknownProperty` en el propio objeto proxy.

* sincronizar: los servidores proxy de objetos host asincrónicos exponen un método Sync que devuelve una promesa de un proxy de objeto host sincrónico para el mismo objeto host. Por ejemplo, `chrome.webview.hostObjects.sample.methodCall()` devuelve un proxy de objeto host asincrónico. Puede usar el `sync` método para obtener un proxy de objeto host sincrónico en su lugar: `const syncProxy = await chrome.webview.hostObjects.sample.methodCall().sync()`

* Async: los proxies de objetos host sincrónicos exponen un método asincrónico que bloquea y devuelve un proxy de objeto host asincrónico para el mismo objeto host. Por ejemplo, `chrome.webview.hostObjects.sync.sample.methodCall()` devuelve un proxy de objeto host sincrónico. Se llama al `async` método de este bloque y, a continuación, se devuelve un proxy de objeto host asincrónico para el mismo objeto host: `const asyncProxy = chrome.webview.hostObjects.sync.sample.methodCall().async()`

* a continuación: los servidores proxy de objetos host asincrónicos tienen un método then. Esto permite que sean esperados. `then` devolverá una promesa que se resolverá con una representación del objeto host. Si el proxy representa un literal de JavaScript, se devuelve una copia de forma local. Si el proxy representa una función, se devuelve un proxy que no es de espera. Si el proxy representa un objeto de JavaScript con una combinación de propiedades literales y propiedades de función, se devuelve una copia del objeto con algunas propiedades como servidores proxy de objeto host.

Todas las demás invocaciones a propiedades y métodos (excepto los métodos anteriores de proxy de objeto remoto, la lista de forceLocalProperties y las propiedades de los prototipos de funciones y objetos) se ejecutan de forma remota. Los proxies de objeto de host asincrónico devuelven una promesa que representa la finalización asincrónica de la invocación remota del método u obtiene la propiedad. La función Promise se resuelve después de que las operaciones remotas se completen y las promesas se resuelven en el valor resultante de la operación. Los servidores proxy sincrónicos del objeto host funcionan de manera similar, pero bloquean la ejecución de JavaScript y espera a que se complete la operación remota.

Establecer una propiedad en un proxy de objeto de host asincrónico funciona de forma ligeramente distinta. El conjunto devolverá inmediatamente y el valor devuelto es el valor que se establecerá. Este es un requisito del objeto proxy de JavaScript. Si necesita esperar de forma asincrónica para que se complete el conjunto de propiedades, use el método setHostProperty que devuelve una promesa según se describe anteriormente. La propiedad sincrónico del conjunto de propiedades de objeto se bloquea de forma sincrónica hasta que se establece la propiedad.

#### AddScriptToExecuteOnDocumentCreatedAsync 

Agregue el JavaScript proporcionado a una lista de scripts que se deben ejecutar después de que se haya creado el objeto global, pero antes de que se haya analizado el documento HTML y antes de que se ejecute cualquier otro script incluido en el documento HTML.

> Tarea asincrónica pública< cadena > [AddScriptToExecuteOnDocumentCreatedAsync](#addscripttoexecuteondocumentcreatedasync)(cadena JavaScript)

El script insertado se aplicará a todas las navegaciones del marco secundario y el documento de primer nivel superior hasta que se elimine con RemoveScriptToExecuteOnDocumentCreated. Esto se aplica de forma asincrónica y debes esperar a que se ejecute el controlador de finalización para poder asegurarte de que el script está listo para ejecutarse en navegaciones futuras.

Tenga en cuenta que si un documento HTML contiene algún tipo de espacio aislado a través de propiedades de [espacio aislado](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) o el [encabezado HTTP de seguridad de contenido](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , esto afectará a la secuencia de comandos que se ejecuta aquí. Así, por ejemplo, si la palabra clave "Allow-modal" no se establece, se omitirán las llamadas a la `alert` función.

#### AddWebResourceRequestedFilter 

Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.

> public void [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(String URI, CoreWebView2WebResourceContext ResourceContext)

El parámetro URI puede ser una cadena comodín (' ': cero o más, '? ': exactamente uno). nullptr es equivalente a L "". Consulta la enumeración CoreWebView2WebResourceContext para obtener una descripción de los filtros de contexto de recursos.

#### CallDevToolsProtocolMethodAsync 

Llama a un método DevToolsProtocol asincrónico.

> Tarea asincrónica pública< String > [CallDevToolsProtocolMethodAsync](#calldevtoolsprotocolmethodasync)(String MethodName, String parametersAsJson)

Consulte el [visor de protocolos de DevTools](https://aka.ms/DevToolsProtocolDocs) para obtener una lista y una descripción de los métodos disponibles. El parámetro methodName es el nombre completo del método en el formato `{domain}.{method}` . El parámetro parametersAsJson es una cadena con formato JSON que contiene los parámetros del método correspondiente. Se llamará al método Invoke del controlador cuando se complete el método de forma asincrónica. Se llamará a Invoke con el objeto devuelto del método como una cadena JSON.

#### CapturePreviewAsync 

Capture una imagen de lo que se muestra en la vista de página.

> [CapturePreviewAsync](#capturepreviewasync)de tareas asincrónicas públicas (CoreWebView2CapturePreviewImageFormat ImageFormat, stream imageStream)

Especifique el formato de la imagen con el parámetro imageFormat. Los datos binarios de la imagen resultantes se escriben en el parámetro imageStream proporcionado. Cuando CapturePreview termina de escribir en la secuencia, se llama al método Invoke del parámetro handler proporcionado.

#### ExecuteScriptAsync 

Ejecute el código JavaScript desde el parámetro de JavaScript en el documento de nivel superior actual representado en la vista de vistas en WebView.

> Tarea asincrónica pública< cadena > [ExecuteScriptAsync](#executescriptasync)(cadena JavaScript)

Esto se ejecutará de forma asincrónica y cuando se complete, si se proporciona un controlador en el parámetro ExecuteScriptCompletedHandler, se llamará a su método Invoke con el resultado de evaluar el JavaScript proporcionado. El valor del resultado es una cadena codificada por JSON. Si el resultado es no definido, contiene un ciclo de referencia o, de lo contrario, no se puede codificar en JSON, el valor de JSON NULL se devolverá como la cadena "null". Observe que una función que no tiene ningún valor explícito devuelto devuelve undefined. Si el script ejecutado inicia una excepción no controlada, el resultado es también ' null '. Este método se aplica de forma asincrónica. Si se llama al método después del evento NavigationStarting durante una navegación, el script se ejecutará en el nuevo documento al cargarlo, en el momento en que se active ContentLoading. ExecuteScript funcionará incluso si IsScriptEnabled se establece en FALSE.

#### GetDevToolsProtocolEventReceiver 

Obtén un receptor de eventos de protocolo de DevTools que te permita suscribirte a un evento de protocolo de DevTools.

> Public CoreWebView2DevToolsProtocolEventReceiver [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(String eventName)

Consulte el [visor de protocolos de DevTools](https://aka.ms/DevToolsProtocolDocs) para obtener una lista y una descripción de los métodos disponibles. El parámetro methodName es el nombre completo del método en el formato `{domain}.{method}` . El parámetro parametersAsJson es una cadena con formato JSON que contiene los parámetros del método correspondiente. Se llamará al método Invoke del controlador cuando se complete el método de forma asincrónica. Se llamará a Invoke con el objeto devuelto del método como una cadena JSON.

#### GoBack 

Navega por la vista Web a la página anterior del historial de navegación.

> public void [GoBack](#goback)()

#### GoForward 

Navega por la vista Web a la página siguiente del historial de navegación.

> public void [GoForward](#goforward)()

#### Busque 

Hacer que la navegación del documento de nivel superior sea la dirección URI especificada.

> public void [Navigate](#navigate)(String URI)

Para obtener más información, consulta los eventos de navegación. Ten en cuenta que esto inicia una navegación y el evento NavigationStarting correspondiente se desencadenará después de que se complete esta llamada de navegación.

#### NavigateToString 

Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.

> public void [NavigateToString](#navigatetostring)(String htmlContent)

El parámetro htmlContent no puede tener más de 2 MB de caracteres. El origen de la nueva página será acerca de: Blank.

#### OpenDevToolsWindow 

Abre la ventana DevTools para el documento actual en la vista de vistas en WebView.

> public void [OpenDevToolsWindow](#opendevtoolswindow)()

No hace nada si se le llama cuando la ventana de DevTools ya está abierta.

#### PostWebMessageAsJson 

Publique el mensaje de correo especificado en el documento de nivel superior en este WebView.

> public void [PostWebMessageAsJson](#postwebmessageasjson)(String webMessageAsJson)

Se desencadena el evento de mensaje de window. Chrome. WebView del documento de nivel superior. JavaScript en ese documento puede suscribirse y cancelar la suscripción al evento a través de lo siguiente:

```
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

El argumentos del evento es una instancia de `MessageEvent` . La configuración de CoreWebView2Settings. IsWebMessageEnabled debe ser true o este método producirá un error con E_INVALIDARG. La propiedad de datos de Arg del evento es el parámetro de cadena WebMessage analizado como una cadena JSON en un objeto de JavaScript. La propiedad Source de Arg de evento es una referencia al `window.chrome.webview` objeto. Consulte SetWebMessageReceivedEventHandler para obtener información sobre cómo enviar mensajes desde el documento HTML de la vista en WebView al host. Este mensaje se envía de forma asincrónica. Si se produce una navegación antes de que el mensaje se publique en la página, no se enviará el mensaje.

#### PostWebMessageAsString 

Este es un auxiliar para publicar un mensaje que es una cadena simple en lugar de una representación de cadena JSON de un objeto de JavaScript.

> public void [PostWebMessageAsString](#postwebmessageasstring)(String webMessageAsString)

Esto se comporta exactamente de la misma manera que PostWebMessageAsJson, pero la `window.chrome.webview` propiedad data del argumento de evento de mensaje será una cadena con el mismo valor que webMessageAsString. Use este en lugar de PostWebMessageAsJson si desea comunicarse a través de cadenas simples en lugar de objetos JSON.

#### Volver a cargar 

Volver a cargar la página actual.

> public void [Reload](#reload)()

Esto es similar a desplazarse hasta el URI del documento de nivel superior actual, incluidos todos los eventos de navegación que desencadenan y respetan cualquier entrada de la caché HTTP. Sin embargo, el historial de atrás y reenvío no se modificará.

#### RemoveHostObjectFromScript 

Quite el objeto host especificado por el nombre para que ya no se pueda tener acceso al mismo desde el código de JavaScript de la vista.

> public void [RemoveHostObjectFromScript](#removehostobjectfromscript)(string name)

Aunque se denegarán nuevos intentos de acceso, si el código de JavaScript ya ha obtenido el objeto, el código de JavaScript seguirá teniendo acceso a ese objeto. Llamar a este método para un nombre que ya se ha quitado o no se ha agregado nunca producirá un error.

#### RemoveScriptToExecuteOnDocumentCreated 

Quite el JavaScript correspondiente agregado a través de AddScriptToExecuteOnDocumentCreated.

> public void [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(string ID)

#### RemoveWebResourceRequestedFilter 

Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.

> public void [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(String URI, [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) ResourceContext)

Si se agregó el mismo filtro varias veces, tendrá que quitarlo tantas veces como se agregara para que la eliminación sea efectiva. Devuelve E_INVALIDARG para un filtro que nunca se ha agregado.

#### Detener 

Detenga todas las navegaciones y las búsquedas de recursos pendientes.

> public void [Stop](#stop)()

No detiene las secuencias de comandos.


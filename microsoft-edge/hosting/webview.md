---
description: Hospedar contenido web en la aplicación de Windows 10 con el control WebView (EdgeHTML)
title: Vista de Microsoft Edge para aplicaciones de Windows 10
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: x-MS-WebView, MSHTMLWebViewElement, WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: aa9bef7bf214cf4f4ffdb4d68ad3a1a86ac2977b
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752209"
---
# Vista de WebView (EdgeHTML) para aplicaciones de Windows 10  

[!INCLUDE [deprecation-note](./includes/deprecation-note.md)]  

El control WebView (EdgeHTML) te permite hospedar contenido web en tu aplicación de Windows 10.  

Puedes usarlo como un elemento XAML (para aplicaciones de la [plataforma universal de Windows (UWP)](/uwp/api/Windows.UI.Xaml.Controls.WebView) y [aplicaciones de escritorio de Windows Forms y WPF](/windows/communitytoolkit/controls/wpf-winforms/webview)) o un elemento HTML (x-MS-WebView)/Dom Object (MSHTMLWebViewElement) para aplicaciones de Windows 10 basadas en JavaScript, tal y como se describe aquí.  

|  |  |  
|:--- |:--- |  
| [**Eventos**](#events) | [departingFocus](#departingfocus), [MSWebViewContainsFullScreenElementChanged](#mswebviewcontainsfullscreenelementchanged), [MSWebViewContentLoading](#mswebviewcontentloading), [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded), [MSWebViewFrameContentLoading](#mswebviewframecontentloading), [MSWebViewFrameDOMContentLoaded](#mswebviewframedomcontentloaded), [MSWebViewFrameNavigationCompleted](#mswebviewframenavigationcompleted), [MSWebViewFrameNavigationStarting](#mswebviewframenavigationstarting), [MSWebViewLongRunningScriptDetected](#mswebviewlongrunningscriptdetected), [MSWebViewNavigationCompleted, MSWebViewNavigationStarting](#mswebviewnavigationcompleted) [, MSWebViewNewWindowRequested](#mswebviewnavigationstarting) [, MSWebViewPermissionRequested](#mswebviewnewwindowrequested) [, MSWebViewProcessExited](#mswebviewpermissionrequested) [, MSWebViewWebResourceRequested](#mswebviewprocessexited) [, MSWebViewScriptNotify](#mswebviewwebresourcerequested) [, MSWebViewUnsafeContentWarningDisplaying](#mswebviewscriptnotify) [, MSWebViewUnsupportedUriSchemeIdentified](#mswebviewunsafecontentwarningdisplaying), [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified) [MSWebViewUnviewableContentIdentified](#mswebviewunsupportedurischemeidentified) |  
| [**Métodos**](#methods) | [addWebAllowedObject](#addweballowedobject), [buildlocalStreamUri](#buildlocalstreamuri), [capturePreviewToBlobAsync](#capturepreviewtoblobasync), [captureSelectedContentToDataPackageAsync](#captureselectedcontenttodatapackageasync), [invokeScriptAsync](#invokescriptasync), [getDeferredPermissionRequests](#getdeferredpermissionrequests), [getDeferredPermissionRequestById](#getdeferredpermissionrequestbyid), [GoBack](#goback), [goForward](#goforward), [Navigate](#navigate), [navigateFocus](#navigatefocus), [navigateTolocalStreamUri](#navigatetolocalstreamuri) [, navigateToString,](#navigatetostring) [navigateWithHttpRequestMessage](#navigatewithhttprequestmessage), [Refresh](#refresh), [Stop](#stop) |  
| [**Propiedades**](#properties) | [canGoBack](#cangoback), [canGoForward](#cangoforward), [containsFullScreenElement](#containsfullscreenelement), [documentTitle](#documenttitle), [height](#height), [Process](#process), [Settings](#settings), [src](#src), [width](#width) |  

## Sintaxis  

```javascript
// Feature detect for webview support
if (MSHTMLWebViewElement) {
    let wv = document.createElement('x-ms-webview'); // Use CSS to set width, height and other styles
    wv.navigate("https://www.example.com");
    document.body.appendChild(wv);
}
```  

## Observaciones  

### Vista de visualización frente a iframe  

Como un elemento HTML [iframe](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) estándar, puedes usar la vista Web para cargar páginas remotas a través de http y páginas locales (*MS-appx-Web:///*) del paquete de la aplicación.  Sin embargo, la WebView también puede:  

*   Cargue páginas y recursos de las carpetas de [ApplicationData](/uwp/api/Windows.Storage.ApplicationData) (local, roaming, temporal) (*MS-AppData:///*) y las [secuencias en memoria](/microsoft-edge/hosting/webview#buildlocalstreamuri) (*MS-local-Stream:///*)  
*   Proporcionar controles de tipo explorador: para [volver atrás](#goback) y [avanzar](#goforward) en el historial de navegación, y [detener](#stop) o [Actualizar](#refresh) la página actual.  
*   [Captura capturas de pantallas de contenido web](#capturepreviewtoblobasync) para que sea más fácil implementar el contrato para [compartir](/windows/uwp/app-to-app/share-data) aplicaciones de Windows 10.  
*   Permite que el código de JavaScript que se ejecuta en una vista webproduzca eventos personalizados ([MSWebViewScriptNotify](#mswebviewscriptnotify)) en la aplicación y permite que la aplicación ejecute JavaScript en la vista de contenido ([invokeScriptAsync](#invokescriptasync)).  
*   Proporcionarle eventos de contenido de WebView con ajuste fino:  
    
    | Evento de DOM de WebView | Descripción |  
    |:--- |:--- |  
    | [MSWebViewNavigationStarting](#mswebviewnavigationstarting) | Indica que la vista en WebView está empezando a navegar.  |  
    | [MSWebViewContentLoading](#mswebviewcontentloading) | El contenido HTML se descarga y se carga en el control.  |  
    | [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded) | Indica que los elementos DOM principales han finalizado de cargarse.  |  
    | [MSWebViewNavigationCompleted](#mswebviewnavigationcompleted) | Indica que la navegación se ha completado y todos los elementos multimedia están representados.  |  
    | [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified) | La vista en WebView encontró que el contenido no era HTML.  |  
    | [UnsafeContentWarningDisplaying](#mswebviewunsafecontentwarningdisplaying) | La vista Web muestra una página de advertencia para el contenido notificado como no seguro por el *Filtro SmartScreen*de Windows.  |  
    
    ... se incluyen [los eventos](#events) correspondientes para el contenido de iframe cargado en una vista previa (como [MSWebView**Frame**NavigationStarting](#mswebviewframenavigationstarting) , etc.). 

### Impresión  

Cuando se imprime una aplicación de Windows con JavaScript, las `<x-ms-webview>` etiquetas se transforman en `<iframe>` etiquetas antes de imprimir.  Además de la diferencia normal entre Mostrar en pantalla y representarse para impresión, los estilos CSS aplicados a `<iframe>` elementos se aplican a los elementos `<iframe>` transformados `<x-ms-webview>` .  

### Trabajadores de servicio  

A partir de la [actualización de 2018 de octubre de Windows](/windows/uwp/whats-new/windows-10-build-17763) (EdgeHTML 18), [los trabajos de servicio se admiten en el control WebView](/microsoft-edge/dev-guide#service-workers) (además de en el explorador Microsoft Edge y las aplicaciones de Windows 10 con JavaScript).  

Las arquitecturas de aplicaciones x64 requieren paquetes neutros (cualquier CPU) o x64, ya que los trabajos de servicio no son compatibles con los procesos de WoW64.  (Para ahorrar espacio en el disco, la versión de WoW de los archivos dll necesarios no se incluye de forma nativa en Windows).  

### Confiabilidad y modelo de subprocesos  

Al crear una vista previa mediante `document.createElement("x-ms-webview")` marcado o mediante marcado, se `<x-ms-webview>` crea una vista previa en un nuevo hilo único en el proceso de la aplicación.  La ejecución de un nuevo subproceso único significa que el script en ejecución prolongada de un WebView no puede bloquear la aplicación ni otras vistas de la aplicación.  Al crear una vista previa mediante el constructor, se `new MSWebView()` crea una vista previa en un proceso de WebView independiente.  Ejecutarse en un único proceso significa que además de protegerse del script de larga ejecución, la aplicación también está protegida contra contenido web que bloquea el proceso de WebView.  Crear una vista previa mediante el [`MSWebViewProcess.createWebViewAsync`](./webview/MSWebViewProcess.md#createwebviewasync) método también crea WebView en un proceso independiente, pero permite que la persona que llama tenga más control sobre la configuración de procesos y la agrupación de Webviews en procesos de WebView.  Vea `MSWebViewProcess` para obtener más información.  

### Acceso API a WinRT  

Una aplicación para UWP puede permitir que los documentos HTML dentro de las vistas previas tengan acceso a las API de WinRT.  Esto se realiza a través del atributo WindowsRuntimeAccess de los elementos secundarios Rule del elemento ApplicationContentUriRules de la AppxManifest.xml de la aplicación para UWP.  Establezca WindowsRuntimeAccess en "todos" y los documentos HTML con URI coincidentes podrán usar WinRT.  Esto es lo mismo que proporcionar acceso a WinRT a contenido HTML en aplicaciones para UWP de JavaScript, así que consulta [llamar a las API de WinRT de tu PWA](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#call-winrt-apis-from-your-pwa) para obtener más información.  

Es posible que las API de WinRT relacionadas con la interfaz de usuario no funcionen cuando se les llame desde una vista previa ejecutándose en su propio subproceso, pero puede funcionar cuando se le llama desde una vista previa que se ejecuta en un proceso WebView independiente.  Al usar una vista previa en su propio subproceso, ese subproceso no es el subproceso de la aplicación.  Algunas API de WinRT relacionadas con la interfaz de usuario deben llamarse desde el subproceso de la vista de la aplicación.  Las vistas en vista previa creadas en un proceso de WebView independiente se ejecutan en un subproceso de vista y, por lo tanto, no deberían enfrentar las mismas restricciones que la vista de WebView en su propio subproceso.  Si tienes problemas con las API de WinRT relacionadas con la interfaz de usuario en una vista previa, asegúrate de estar usando una vista previa en su propio proceso de WebView, tal y como se describe anteriormente.  

### Limitaciones de almacenamiento de AppCache  

Las aplicaciones que usan la compatibilidad de JavaScript de la API de caché de la aplicación (o AppCache), según se define en la [especificación HTML5](https://go.microsoft.com/fwlink/p/?LinkId=228542), para crear aplicaciones web sin conexión deben observar las limitaciones de almacenamiento disponibles.  Esto es especialmente cierto en dispositivos con espacio de memoria limitado.  Los límites prácticos del tamaño de las AppCache siempre son una función del espacio de almacenamiento disponible en disco.  A continuación se muestran las directrices generales.  

| Tamaño del volumen |AppCache por dominio | AppCache por usuario |  
|:--- |:--- |:--- |  
| Hasta 4 GB | 10MB | 50MB |  
| 4GB a 16 GB | 50MB | CERCA |  
| de 16 GB a 32 GB | 50MB | 1 GB |  

Todas las aplicaciones de Windows10 se han diseñado para usar el mismo modelo de cuota de AppCache, por lo que se aplica la limitación de almacenamiento en disco disponible a las aplicaciones de escritorio y de teléfono.  El es también un límite rígido después de que las páginas cargadas en la **vista** Web juntos hayan consumido 1 GB de espacio en *AppCache* ; se denegarán las solicitudes de almacenamiento adicional de *AppCache* por encima de este límite.  

Para obtener más información, consulta el [ejemplo de control WebView HTML](https://go.microsoft.com/fwlink/p/?linkid=309825) y el JSBrowser de la documentación de [control WebView](https://github.com/MicrosoftEdge/JSBrowser#harnessing-the-webview-control) .  

## Eventos  

### departingFocus  

Indica que el foco va de la **vista** web a la aplicación.  Se desencadena cuando la ventana de llamadas de nivel superior de la vista de vistas de WebView. departFocus.  Los argumentos FocusNavigationEvent en el evento departingFocus coinciden con los parámetros proporcionados a departFocus excepto que los parámetros de origen se traducen desde el espacio de coordenadas de document's de WebView al espacio de coordenadas del documento host de WebView.  Consulta el método WebView. navigateFocus y el evento de navigatingFocus de la ventana correspondiente para transferir el foco del host a la vista de ventana.  Consulte la [biblioteca de navegación dirección de TVJS](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) para obtener un ejemplo de una implementación de la navegación de foco mediante un teclado o un controlador para juegos que controla este evento.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("departingFocus", handler);
webview.removeEventListener("departingFocus", handler);
```  

#### Información del evento  

|            |      |  
|:--- |:--- |  
| **Interfaz** | [FocusNavigationEvent](./webview/FocusNavigationEvent.md) |  
| **Sincrónico** | Sí |   
| **Pase** | Sí |  
| **Cancelable** | No |  

### MSWebViewContainsFullScreenElementChanged  

Se produce cuando el estado cambia para si la **vista previa** contiene o no un elemento de pantalla completa.  Use la propiedad containsFullScreenElement para el valor actual.  Elemento de pantalla completa aquí se hace referencia a la noción de [API Dom](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) en pantalla completa de un elemento de pantalla completa a través de las funciones Element. requestFullScreen y Document. exitFullScreen Dom.  

```javascript
function containsFullScreenElementChangedHandler(eventInfo) {
    const applicationView = Windows.UI.ViewManagement.ApplicationView.getForCurrentView();
    if (webview.containsFullScreenElement) {
        webview.classList.add("fullscreen"); // Have the webview fill the app view
        applicationView.tryEnterFullScreenMode(); // Have the app view fill the screen
    }
    else {
        webview.classList.remove("fullscreen"); // Return webview to normal
        applicationView.exitFullScreenMode(); // Return app view to normal
    }
}

// addEventListener syntax
webview.addEventListener("MSWebViewContainsFullScreenElementChanged", containsFullScreenElementChangedHandler);
webview.removeEventListener("MSWebViewContainsFullScreenElementChanged", containsFullScreenElementChangedHandler);
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | **Evento** |  
| **Sincrónico** | Sí |  
| **Pase** | No |   
| **Cancelable** | No |  

### MSWebViewContentLoading  

Indica que el contenido HTML se descarga y se carga en el control.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewContentLoading", handler);
webview.removeEventListener("MSWebViewContentLoading", handler);
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Sincrónico** | Sí  |  
| **Pase** | No |   
| **Cancelable** | No |  

### MSWebViewDOMContentLoaded  

Indica que los elementos DOM principales han finalizado de cargarse.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewDOMContentLoaded", handler);
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Sincrónico** |Sí |  
| **Pase** | No |  
| **Cancelable** | No |   

### MSWebViewFrameContentLoading  

Indica que el contenido HTML descargado y se carga en el `<iframe>` control.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameContentLoading", handler);
webview.removeEventListener("MSWebViewFrameContentLoading", handler);
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Sincrónico** | Sí |  
| **Pase** | No |  
| **Cancelable** | No |   

### MSWebViewFrameDOMContentLoaded  

Indica que los elementos DOM principales han finalizado de cargarse en `<iframe>` .  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewFrameDOMContentLoaded", handler);
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Sincrónico** | Sí |  
| **Pase** | No |   
| **Cancelable** | No |  

### MSWebViewFrameNavigationCompleted  

Indica que la navegación se ha completado y todos los elementos multimedia se representan en el `<iframe>` .  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationCompleted", handler);
webview.removeEventListener("MSWebViewFrameNavigationCompleted", handler);
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | [NavigationCompletedEvent](./webview/NavigationCompletedEvent.md) |  
| **Sincrónico** | Sí |  
| **Pase** | No |   
| **Cancelable** | No |  

### MSWebViewFrameNavigationStarting  

Indica `<iframe>` que una en un **WebView** está empezando a navegar.  Esto se activa antes de obtener los recursos de la red para la navegación.  La navegación no se inicia hasta que se completan todos los controladores de eventos de MSWebViewFrameNavigationStarting.  Este evento se encuentra cancelable por medio de llamadas `eventArgs.preventDefault()` .  Si se cancela, WebView no realizará la navegación.  

```javascript
function frameNavigationStartingHandler(navigationEventArgs) {
    // Cancel all navigations that don't meet some criteria.
    if (!navigationEventArgs.uri.startsWith("https://example.com/")) {
        navigationEventArgs.preventDefault();
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationStarting", frameNavigationStartingHandler);
webview.removeEventListener("MSWebViewFrameNavigationStarting", frameNavigationStartingHandler);
```  

#### Información del evento  

|  |  |
|:--- |:--- |  
| **Interfaz** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Sincrónico** | Sí |  
| **Pase** |No |   
| **Cancelable** | Sí |  

### MSWebViewLongRunningScriptDetected  

Se produce de forma periódica durante la ejecución de scripts sin interrupciones en la **vista de WebView**y permite detener el script.  

```javascript
function handler(eventInfo) {
    const stopPageScriptThreshold = 5 * 1000;
    if (eventInfo.executionTime > stopPageScriptThreshold) {
        eventInfo.stopPageScriptExecution = true; // Stop the long running script if it goes over our threshold
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewLongRunningScriptDetected", handler);
webview.removeEventListener("MSWebViewLongRunningScriptDetected", handler);
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | [LongRunningScriptDetectedEvent](./webview/LongRunningScriptDetectedEvent.md) |  
| **Sincrónico** | Sí |  
| **Pase** | No |  
| **Cancelable** | No |  

### MSWebViewNavigationCompleted  

Indica que la navegación se ha completado y todos los elementos multimedia se han procesado o se ha producido un error de navegación.  Compruebe la propiedad argumentos de evento isSuccess para saber si la navegación se realizó correctamente y la propiedad webErrorStatus para obtener información sobre el error de navegación.  Es posible que se produzcan errores de navegación antes de obtener contenido de la red por ejemplo, si el nombre de host de un URI no se resuelve en ese caso, el evento MSWebViewNavigationStarted se desencadenará seguido del evento MSWebViewNavigationCompleted.  Los errores de navegación también pueden producirse después de recibir una página de error de un servidor Web, por ejemplo, una página de 404 de un servidor HTTP en cuyo caso todos los eventos de navegación se desencadenarán, MSWebViewNavigationStarting, MSWebViewContentLoading, MSWebViewDOMContentLoaded y MSWebViewNavigationCompleted.  Para proporcionar una página de error de navegación de la aplicación para los casos en los que el servidor Web no ha proporcionado una página de error, debe comprobar si MSWebViewContentLoading se ha activado para una navegación fallida que indica que no se ha proporcionado ninguna página de error del servidor.  

```javascript
let hasContent = false;
webview.addEventListener("MSWebViewNavigationStarting", () => { hasContent = false; });
webview.addEventListener("MSWebViewContentLoading", () => { hasContent = true; });

webview.addEventListener("MSWebViewNavigationCompleted", navigationCompletedEventArgs => {
    // Navigation failures may or may not come after getting an error page from the web server.
    // We keep track of the ContentLoading event with hasContent to tell if we have an error page from the server.
    // So we only navigate to our app error page when there's no server provided error page.
    if (!navigationCompletedEventArgs.isSuccess && !hasContent) {
        // Pass our failed URI and error details in the query and the error page script can read it as appropriate.
        webview.navigate("ms-appx-web:///appErrorPage.html?" + 
            "uri=" + encodeURIComponent(navigationCompletedEventArgs.uri) + "&" +
            "webErrorStatus=" + encodeURIComponent(navigationCompletedEventArgs.webErrorStatus));
    }
});
 
// addEventListener syntax
webview.addEventListener("MSWebViewNavigationCompleted", handler);
webview.removeEventListener("MSWebViewNavigationCompleted", handler);
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | [NavigationCompletedEvent](./webview/NavigationCompletedEvent.md) |  
| **Sincrónico** | Sí |  
| **Pase** | No |   
| **Cancelable** | No |  

### MSWebViewNavigationStarting  

Indica que la **vista en WebView** está empezando a navegar.  Esto se activa antes de obtener los recursos de la red para la navegación.  La navegación no se inicia hasta que se completan todos los controladores de eventos de MSWebViewNavigationStarting.  Este evento se encuentra cancelable por medio de llamadas `eventArgs.preventDefault()` .  Si se cancela, WebView no realizará la navegación.  

```javascript
function navigationStartingHandler(navigationEventArgs) {
    // Cancel all navigations that don't meet some criteria.
    if (!navigationEventArgs.uri.startsWith("https://example.com/")) {
        navigationEventArgs.preventDefault();
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewNavigationStarting", navigationStartingHandler);
webview.removeEventListener("MSWebViewNavigationStarting", navigationStartingHandler);
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Sincrónico** | No |  
| **Pase** | Sí |   
| **Cancelable** | Sí |  

### MSWebViewNewWindowRequested  

Se genera cuando el contenido de **WebView** está intentando abrir una nueva ventana.  Si el evento no se cancela, WebView iniciará el URI de la nueva solicitud de ventana en el explorador predeterminado del usuario.  

```javascript
function handler(eventInfo) {
    // Prevent the webview from opening URIs in the default browser.
    eventInfo.preventDefault();
    
    // Only allow https://example.com/ to open new windows.
    if (eventInfo.referer === "https://example.com/") {
        // Perform some custom handling of the URI.
        openUri(eventInfo.uri);
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewNewWindowRequested", handler);
webview.removeEventListener("MSWebViewNewWindowRequested", handler);
```  

#### Información del evento  

|  |  |  
|:---|:--- |  
| **Interfaz** | [NavigationEventWithReferrer](./webview/NavigationEventWithReferrer.md) |  
| **Sincrónico** | Sí |  
| **Pase** | No |  
| **Cancelable** | Sí |  

### MSWebViewPermissionRequested  

Indica que el contenido de la **vista en WebView** está intentando acceder a funcionalidades (como el acceso de bloqueo de puntero) que normalmente requiere permisos de usuario final.  Si no hay ningún controlador de eventos registrado o si el controlador de eventos no llama a eventArgs. permissionRequest. allow (), defer () o Deny (), se denegará la solicitud de permiso de forma predeterminada.  Si necesita decidir si el permiso está permitido o denegado de forma asincrónica por ejemplo, si necesita solicitar la intervención del usuario, use eventArgs. permissionRequest. defer ().  La solicitud de permiso se aplazará hasta que uses WebView. getDeferredPermissionRequestById o WebView. getDeferredPermissionRequests y llame a allow () o Deny () en la DeferredPermissionRequest con el valor de ID correspondiente.  

```javascript
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    switch (permissionRequest.type) {
        case "geolocation":
        case "media":
        case "pointerlock":
        case "webnotifications":
        case "screen":
        case "immersiveview":
            if (permissionRequest.uri.startsWith("https://www.example.com/")) {
                // Implicitly trust particular URI
                permissionRequest.allow();
            }
            else if (permissionRequest.uri.startsWith("https://")) {
                // Defer the request so we can ask the user to allow or deny the request
                permissionRequest.defer();
                // Later we'll need to use webview.getDeferredPermissionRequestById for this
                // request and call allow or deny.
                promptUserForDeferredPermissionRequest(
                    permissionRequest.id,
                    permissionRequest.uri,
                    permissionRequest.type);
            }
            else {
                // Implicitly deny non-https URIs
                permissionRequest.deny();
            }
            break;

        case "unlimitedIndexedDBQuota":
        default:
            permissionRequest.deny();
            break;
    }
});

// addEventListener syntax
webview.addEventListener("MSWebViewPermissionRequested", handler);
webview.removeEventListener("MSWebViewPermissionRequested", handler);
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | [PermissionRequestedEvent](./webview/PermissionRequestedEvent.md) |  
| **Sincrónico** | Sí |  
| **Pase** | No |   
| **Cancelable** | No |  

### MSWebViewProcessExited  

Indica que el proceso del componente **WebView** se bloqueó.  Esto solo es relevante para una vista previa fuera de proceso.  Vea la sección de comentarios sobre cómo crear una WebView fuera de proceso en lugar de una vista previa en proceso.  Después de que este evento se desencadene, la vista previa correspondiente se pone en un estado bloqueado.  Si llamas a la mayoría de los métodos específicos de WebView o accedes a la mayoría de las propiedades específicas de WebView en una WebView bloqueada, se iniciará una excepción.  Para recuperar a partir de este evento, quite la vista previa bloqueada del DOM y sustitúyala por una nueva vista previa.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewProcessExited", handler);
webview.removeEventListener("MSWebViewProcessExited", handler);
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | **Evento** |  
| **Sincrónico** | Sí |  
| **Pase** | No |   
| **Cancelable** | No |  

### MSWebViewWebResourceRequested  

Se genera cuando una página del elemento **WebView** solicita un recurso.  

```javascript
// A handler that completes synchronously with a custom HTTP response built from a string.
function handlerWithSyncString(webResourceRequestedEventArgs) {
    // Only provide custom HTTP responses for particular HTTP requests
    if (webResourceRequestedEventArgs.args.request.requestUri.absoluteUri === "https://www.bing.com/") {
        const Http = Windows.Web.Http;
        // Create the custom response using a string
        webResourceRequestedEventArgs.args.response = new Http.HttpResponseMessage(Http.HttpStatusCode.ok);
        webResourceRequestedEventArgs.args.response.content = new Http.HttpStringContent("<H1>Example</H1>");
    }
});

// A more complicated handler that completes asynchronously with a custom HTTP response built from a stream.
function handlerWithAsyncStream(webResourceRequestedEventArgs) {
    // Only provide custom HTTP responses for particular HTTP requests
    if (webResourceRequestedEventArgs.args.request.requestUri.absoluteUri === "https://www.bing.com/") {
        // Take a deferral on the WebResourceRequested event so that we can create the custom HTTP response asynchronously.
        const deferral = webResourceRequestedEventArgs.args.getDeferral();

        // Use fetch to get a Blob of the content of the URI
        fetch("ms-appx:///replacement.html").then(fetchResponse => {
            return fetchResponse.blob();
        }).then(fetchResponseBlob => {
            const Http = Windows.Web.Http;
            webResourceRequestedEventArgs.args.response = new Http.HttpResponseMessage(
                Http.HttpStatusCode.ok);

            // Use Blob.msDetachStream to convert the Blob to a Windows.Storage.Streams.IInputStream
            webResourceRequestedEventArgs.args.response.content = new Http.HttpStreamContent(
                fetchResponseBlob.msDetachStream());

        }).finally(() => {
            // Use a finally call to complete the deferral so even if there is an error we will unblock the event.
            deferral.complete();
        });
    }
});
 
// addEventListener syntax
webview.addEventListener("MSWebViewWebResourceRequested", handler);
webview.removeEventListener("MSWebViewWebResourceRequested", handler);
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | [WebResourceRequestedEvent](./webview/WebResourceRequestedEvent.md) |  
| **Sincrónico** | Sí |  
| **Pase** | No |   
| **Cancelable** | No |  


### MSWebViewScriptNotify  

Se genera cuando una página dentro del elemento **WebView** llama al método **window. external. Notify** .  El método window. external. Notify solo está disponible para los documentos con URI que coinciden con las reglas del manifest's ApplicationContentUriRules de la aplicación o que se ha permitido mediante programación mediante la configuración de WebView. Settings. isScriptNotifyAllowed en true.  Además, Window. external. Notify solo está disponible para el documento de nivel superior de WebView.  

```javascript
webview.addEventListener("MSWebViewScriptNotify", eventInfo => {
    console.log("The URI " + eventInfo.callingUri + 
        " has sent notification " + eventInfo.value);
});

// Allow the next URI to which we navigate access to window.external.notify
webview.settings.isScriptNotifyAllowed = true;
webview.navigate("https://example.com/");

webview.addEventListener("MSWebViewNavigationCompleted", () => {
    // Inject script to the webview that will send a notification back.
    const asyncOp = webview.invokeScriptAsync("eval", "window.external.notify('example notification')");
    asyncOp.start();
});
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | [ScriptNotifyEvent](./webview/ScriptNotifyEvent.md) |  
| **Sincrónico** | Sí |  
| **Pase** | No |  
| **Cancelable** | No |  

### MSWebViewUnsafeContentWarningDisplaying  

Se produce cuando la **vista** Web muestra una página de advertencia para el contenido notificado como no seguro por Filtro SmartScreen.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
webview.removeEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | **Evento** |  
| **Sincrónico** |Sí |  
| **Pase** |No |   
| **Cancelable** |No |  

### MSWebViewUnsupportedUriSchemeIdentified  

Se genera cuando hay navegación en un identificador de recursos uniforme (URI) que no es compatible con **WebView** .  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
webview.removeEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Sincrónico** | Sí |  
| **Pase** | No |  
| **Cancelable** | Sí |  

### MSWebViewUnviewableContentIdentified  

Se genera cuando la **vista** Web intenta navegar al contenido web con un tipo de contenido no admitido.  Por ejemplo, los documentos PDF no son compatibles actualmente con WebView y los desplazamientos a documentos PDF no se desplazarán y provocarán este evento.  

```javascript
function handler(args) {
    if (args.mediaType === "application/pdf") {
        Windows.System.Launcher.launchUriAsync(new Windows.Foundation.Uri(args.uri));
    }
}

// addEventListener syntax
webview.addEventListener("MSWebViewUnviewableContentIdentified", handler);
webview.removeEventListener("MSWebViewUnviewableContentIdentified", handler);
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | [UnviewableContentIdentifiedEvent](./webview/UnviewableContentIdentifiedEvent.md) |  
| **Sincrónico** | Sí |  
| **Pase** | No |   
| **Cancelable** | No |  

## Métodos  

### addWebAllowedObject  

Agrega un objeto de Windows Runtime nativo como un parámetro global al documento de nivel superior dentro de un **WebView**.  

El objeto no se inserta en el documento actual, sino en el siguiente documento de nivel superior al que navega la vista en la vista.  El objeto se inserta antes de que se ejecute cualquier script del documento HTML para que pueda basarse en el objeto en el script global del documento.  

Debes usar addWebAllowedObject durante un evento MSWebViewNavigationStarting o antes de llamar explícitamente a un método Navigate.  En estos casos, el objeto se inserta en el documento de la navegación correspondiente.  Si lo llama en algún otro contexto, no tiene una forma de estar seguro de qué documento inyectará.  

Al llamar a addWebAllowedObject varias veces seguidas, se insertarán varios objetos en el documento.  Si llamas antes de una llamada de navegación explícita y luego de nuevo durante el evento MSWebViewNavigationStarting correspondiente, ambas llamadas se realizarán correctamente y tendrás varios objetos inyectados.  Si llamas varias veces con el mismo parámetro de nombre, se ignorará la última llamada ganada y las llamadas anteriores con ese nombre.  

Si se produce un error en la navegación o se redirige, las llamadas de addWebAllowedObject para esa navegación se omiten.  Si deseas controlar las redirecciones, puedes suscribirte al reloj de eventos de MSWebViewNavigationStarting de redireccionamientos y llamar de addWebAllowedObject de nuevo según los criterios que sean adecuados para tu aplicación.  De forma similar, una vez que un documento se desplaza fuera de los objetos insertados a través de addWebAllowedObject para ese documento, no pasará al siguiente documento y deberá llamar explícitamente a addWebAllowedObject si desea que los pasen.  

Si llamas a addWebAllowedObject para un documento que no tiene acceso a WinRT de otro modo, o si tiene [AllowForWebOnly acceso a través de ApplicationContentUriRules](/uwp/schemas/appxpackage/uapmanifestschema/element-uap-rule) , el objeto solo se insertará si el objeto tiene el atributo Windows. Foundation. Metadata. AllowForWeb metadatos.  De lo contrario, no se producirá una inyección y se notificará un error a la consola del desarrollador de JavaScript.  Si se llama en un documento que tiene acceso completo a WinRT, el objeto se insertará independientemente del atributo AllowForWeb.  

Además, el objeto debe implementar la interfaz IAgileObject.  Esto se debe a que los elementos XAML y WebView se ejecutan en el ASTA de la aplicación y el subproceso de JavaScript de WebView es un hilo de ASTA diferente y queremos alentar a los programadores de aplicaciones para que puedan ejecutarse en el subproceso de JavaScript sin bloquear el subproceso de la vista de la aplicación, si es posible.  

El parámetro de nombre debe ser un nombre de propiedad de JavaScript válido; de lo contrario, la llamada fallará de forma silenciosa.  Si el nombre es de una propiedad que ya existe en el objeto global, esa propiedad se sobrescribe si se puede configurar la propiedad.  No se sobrescriben las propiedades no configurables del objeto global y se produce un error en la llamada de addWebAllowedObject silenciosamente.  Las propiedades de JavaScript creadas a través de addWebAllowedObject son modificables, configurables y enumerables.  

```javascript
let name = "exampleProperty";
webview.addWebAllowedObject(name, applicationObject);
webview.navigate("https://example.com/"); // applicationObject will be available as window.exampleProperty on https://example.com
```  

#### Parameters  

*name*  

*   Tipo: **cadena**  
*   El nombre del objeto que se va a exponer en el documento en la **vista de vista de vistas**.  

*applicationObject*  

*   Tipo: **objeto**  
*   Objeto que se va a exponer en el documento en la **vista de vista de vista**.  

#### Valor devuelto  

Este método no devuelve un valor.  

#### Características y requisitos adicionales  

|  |  |  
|:--- |:--- |  
| **Cliente mínimo admitido** | Windows10 (solo aplicaciones de la tienda Windows) |    
| **Servidor mínimo admitido** | Ninguna compatibilidad |   
| **Teléfono mínimo admitido** | Ninguna compatibilidad |  

### buildLocalStreamUri  

Crea un URI que puedes pasar a [navigateToLocalStreamUri](#methods).  

```javascript
var string = webview.buildLocalStreamUri(contentIdentifier, relativePath);
```  

#### Parameters  

*contentIdentifier*  

*   Tipo: **cadena**  
*   Un identificador único para el contenido al que hace referencia el URI.  Define la raíz del URI.  

*relativePath*  

*  Tipo: **cadena**  
*  La ruta de acceso al recurso, relativa a la raíz.  

#### Valor devuelto  

Tipo: **cadena**  

Identificador URI creado mediante la combinación y la normalización de *contentIdentifier* y *relativePath*.  

#### Ejemplo  

En el ejemplo siguiente se muestra un caso de uso típico.  

```javascript
var webview = document.createElement("x-ms-webview"); //Instantiate the webview element
var localStreamUri = webview.buildLocalStreamUri(contentIdentifier, relativePath); //Create URI to pass to navigateToLocalStreamUri method
webview.navigateToLocalStreamUri(localStreamUri, streamResolver); //Load the local web content 
```  

### capturePreviewToBlobAsync  

Crea una imagen del [elemento WebView](./webview.md) actual y la escribe en el elemento de imagen especificado.  

```javascript
var capturePreviewToBlobAsync = webview.capturePreviewToBlobAsync();
```  

#### Parameters  

Este método no tiene parámetros.  

#### Valor devuelto  

Escriba: **MSWebViewAsyncOperation**  

Un objeto **MSWebViewAsyncOperation** que, cuando se completa, proporciona un objeto **BLOB** que contiene la imagen.  Al usar **capturePreviewToBlobAsync**, es necesario definir controladores de éxito y error después de definir la operación.  Después de aplicar los controladores de eventos, llama al método Start del objeto [MSWebViewAsyncOperation](./webview/MSWebViewAsyncOperation.md) para ejecutar la operación.  

### captureSelectedContentToDataPackageAsync  

> [!IMPORTANT]
> Este método ha quedado obsoleto y tiene un problema conocido.  Evite usar este método en su código de producción.  

Obtiene de forma asincrónica un [paquete de paquetes](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) de contenido que contiene el contenido seleccionado en la **vista**de contenido.  

```javascript
var msWebViewAsyncOperation = webview.captureSelectedContentToDataPackageAsync();
```  

#### Parameters  

Este método no tiene parámetros.  

#### Valor devuelto  

Escriba: **MSWebViewAsyncOperation**  

Un objeto **MSWebViewAsyncOperation** que, cuando se completa, proporciona un objeto de [paquete](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) de datos que contiene la imagen.  Al usar **captureSelectedContentToDataPackageAsync**, es necesario definir controladores de éxito y error después de definir la operación.  Después de aplicar los controladores de eventos, llama al método Start del objeto MSWebViewAsyncOperation para ejecutar la operación.  

```javascript
 var operation = webview.captureSelectedContentToDataPackageAsync();
    operation.oncomplete = function () {
        // operation.result is a package object that contains the selected data.
        var url = URL.createObjectURL(operation.result, { oneTimeOnly: true });
        // After converting the package to a URI, put it in an image element.
        document.getElementById('webviewPreview').src = url;
    };
    operation.start();
```  

### invokeScriptAsync  

Como una acción asincrónica, ejecuta la función de secuencia de comandos especificada desde el código HTML cargado actualmente, con argumentos específicos.  

```javascript
webview.invokeScriptAsync(functionName, ...args)
```  

#### Parameters  

**functionName**  

*   Tipo: **cadena**  
*   Nombre de la función que se va a invocar.  Este es un nombre de propiedad en el objeto de ventana global del documento de nivel superior de WebView.  Puede ser una función global integrada como eval o abrir, o puede ser una función definida por script en el objeto de ventana global.  Solo se pueden invocar funciones en el documento de nivel superior de la vista de WebView.  

**EventArgs**  

*   Tipo: **cadena**  
*   Parámetros de cadena opcionales que se pasan a la función invocada.  Después de functionName, los parámetros adicionales para invokeScriptAsync son cadenas que se pasan a la función invocada.  

#### Valor devuelto  

Escriba: **MSWebViewAsyncOperation**  

Al usar **invokeScriptAsync**, es necesario definir controladores de éxito y error después de definir la operación.  Después de aplicar los controladores de eventos, llama a **MSWebViewAsyncOperation. Start** para ejecutar la operación.  Si el evento completo de MSWebViewAsyncOperation se desencadena, la propiedad result de MSWebViewAsyncOperation es el valor devuelto por la cadena para invocar la función.  El uso del valor devuelto por la función invocada permite que el contenido de la vista en la vista previa vuelva a comunicarse de forma sincrónica con el host de WebView.  Para que el contenido de WebView se comunique de forma asincrónica al host WebView, consulta el evento MSWebViewScriptNotify.  Si la función invocada produce una excepción no controlada, se desencadenará el evento de error del MSWebViewAsyncOperation.  

```javascript
const functionName = "eval";
const args = ["'Current URL: ' + document.location.href"];

const asyncOp = webview.invokeScriptAsync(functionName, ...args);

asyncOp.onerror = () => console.error("Error: " + asyncOp.error);
asyncOp.oncomplete = () => console.log("Result: " + asyncOp.result); // Logs 'Current URL: about:blank'
asyncOp.start();
```  

### getDeferredPermissionRequests  

Devuelve una lista de las solicitudes de permisos diferidos emitidas por el contenido en el control **WebView** .  

```javascript
var sequence<PermissionRequest> = x-ms-webview.getDeferredPermissionRequests();
```  

#### Parameters  

Este método no tiene parámetros.  

#### Valor devuelto  

Escriba: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)  

La solicitud de permisos diferidos especificada.  

#### Características y requisitos adicionales  

|  | |  
|:--- |:--- |  
| **Cliente mínimo admitido** | Windows10 (solo aplicaciones de la tienda Windows) |  
| **Servidor mínimo admitido** | Ninguna compatibilidad |  
| **Teléfono mínimo admitido** | Ninguna compatibilidad |  


### getDeferredPermissionRequestById  

Devuelve la solicitud de permiso diferido especificada.  

```javascript
var deferredPermissionRequest = x-ms-webview.getDeferredPermissionRequestById(id);
```  

#### Parameters  

*id*  

*   Tipo: **largo sin signo**  
*   IDENTIFICADOR de la solicitud de permiso diferido que desea obtener.  

#### Valor devuelto  

Escriba: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)  

La solicitud de permisos diferidos especificada.  

#### Características y requisitos adicionales  

|  |  |  
|:--- |:--- |  
| **Cliente mínimo admitido** | Windows10 (solo aplicaciones de la tienda Windows) |  
| **Servidor mínimo admitido** | Ninguna compatibilidad |  
| **Teléfono mínimo admitido** | Ninguna compatibilidad |  

### goBack  

Navega por la **vista** web a la página anterior del historial de navegación.  

```javascript
webview.goBack();
```  

#### Parameters  

Este método no tiene parámetros.  

#### Valor devuelto  

Este método no devuelve un valor.  

### goForward  

Navega por la **vista** web a la página siguiente del historial de navegación.  

```javascript
webview.goForward();
```  

#### Parameters  

Este método no tiene parámetros.  

#### Valor devuelto  

Este método no devuelve un valor.  

### navegar  

Carga el contenido HTML en el identificador uniforme de recursos (URI) especificado.  

```javascript
webview.navigate(uri);
```  

#### Parameters  

**uri**  

*   Tipo: **cadena**  
*   URI que se va a cargar.  

#### Valor devuelto  

Este método no devuelve un valor.  

### navigateFocus  

Desplaza el foco a la **vista de vistas en WebView**.  Desencadena el evento window's navigatingfocus del documento de nivel superior de WebView.  El FocusNavigationEvent args usado en el evento navigatingfocus coincide con los parámetros proporcionados a navigateFocus excepto que los parámetros de origen se traducen desde el espacio de coordenadas del documento host al espacio de coordenadas del documento de nivel superior de WebView.  Consulta el evento WebView departingFocus y el método window. departFocus correspondiente para transferir el foco de la vista en webal host.  Vea la [biblioteca de navegación de direcciones de TVJS](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) para obtener un ejemplo de una implementación de la navegación de foco mediante un teclado o un controlador para juegos que usa este método.  

```javascript
const activeElementBounds = document.activeElement.getBoundingClientRect();
const origin = { 
    originLeft: activeElementBounds.left,
    originTop: activeElementBounds.top,
    originWidth: activeElementBounds.width,
    originHeight: activeElementBounds.height
};
webview.navigateFocus(navigationReason, origin);
```  

#### Parameters  

*navigationReason*  

*   Tipo: **cadena**  
*   El motivo de la navegación.  El valor debe ser "left", "up", "Right" o "Down".  Es la dirección en la que el foco se aleja del elemento que se encuentra enfocado.  

*origen*  

*   Tipo: **objeto**  
*   El origen de la navegación.  Este es un objeto de JavaScript con las propiedades "originLeft", "originTop", "originWidth" y "originHeight".  Estos valores deben describir la posición y el tamaño del elemento que se encuentra actualmente enfocado y en el que se mueve el foco.  

#### Valor devuelto  

Este método no devuelve un valor.  

### navigateToLocalStreamUri  

Carga el contenido Web local en el URI especificado usando un [**UriToStreamResolver**](/uwp/api/windows.web.iuritostreamresolver.uritostreamasync).  

```javascript
webview.navigateToLocalStreamUri(source, streamResolver); 
```  

#### Parameters  

*origen*  

*   Tipo: **cadena**  
*   Un identificador URI MS-local-Stream que identifica el contenido HTML local que se va a cargar.  Cree esta cadena con [**buildLocalStreamUri**](/uwp/api/windows.web.ui.iwebviewcontrol.buildlocalstreamuri).  

*streamResolver*  

*   Escriba lo siguiente: cualquiera  
*   Una resolución que convierte el identificador URI en una secuencia que se va a cargar.  

#### Valor devuelto  

Este método no devuelve un valor.  

### navigateToString  

Carga el contenido HTML especificado como un documento nuevo.  

```javascript
webview.navigateToString(contents);
```  

#### Parameters  

*contenidos*  

*   Tipo: **cadena**  
*   Contenido HTML que se va a mostrar.  

#### Valor devuelto  

Este método no devuelve un valor.  

### navigateWithHttpRequestMessage  

Navega por la vista en WebView a un identificador uniforme de recursos (URI) con una solicitud POST y encabezados HTTP.  

```javascript
webview.navigateWithHttpRequestMessage(requestMessage);
```  

#### Parameters  

*requestMessage*  

*   Tipo: **HttpRequestMessage**  
*   Detalles de la solicitud HTTP.  

#### Valor devuelto  

Este método no devuelve un valor.  

#### Observaciones  

> [!WARNING]
> Si agrega encabezados adicionales a esta solicitud, como las credenciales de autenticación, recuerde que esos encabezados también se incluirán en las solicitudes secundarias subsiguientes.  Use precaución para evitar la revelación accidental de información confidencial o personal.  

### fresca  

Vuelve a cargar el contenido actual en la **vista**de contenido.  

```javascript
webview.refresh();
```  

#### Parameters  

Este método no tiene parámetros.  

#### Valor devuelto  

Este método no devuelve un valor.  

### stop  

Detiene la navegación o descarga de la **vista en WebView** actual.  

```javascript
webview.stop();
```  

#### Parameters  

Este método no tiene parámetros.  

#### Valor devuelto  

Este método no devuelve un valor.  

## Propiedades  

### canGoBack  

Obtiene un valor que indica si la **vista de vista previa** puede desplazarse hacia atrás.  

Esta propiedad es de solo lectura.  

```javascript
var canGoBack = webview.canGoBack;
```  

#### Valor de propiedad  

Tipo: **Boolean**  

**True** si la **vista en WebView** puede desplazarse hacia atrás; en caso contrario, **false**.  

### canGoForward  

Obtiene un valor que indica si la **vista previa** puede navegar hacia delante.  

Esta propiedad es de solo lectura.  

```javascript
var canGoForward = webview.canGoForward;
```  

#### Valor de propiedad  

Tipo: **Boolean**  

**True** si la **vista en WebView** puede navegar hacia delante; en caso contrario, **false**.  

### containsFullScreenElement  

Obtiene un valor que indica si la **vista** de página contiene un elemento que admite la pantalla completa.  Para obtener más información, consulta el evento MSWebViewContainsFullScreenElementChanged.  

Esta propiedad es de solo lectura.  

```javascript
var containsFullScreenElement = webview.containsFullScreenElement;
```  

#### Valor de propiedad  

Tipo: **Boolean**  

**True** **si la ventana** contiene un elemento que admite la pantalla completa; en caso contrario, **false**.  

### documentTitle  

Obtiene el título de la página que se muestra actualmente en la **vista**Web.  

Esta propiedad es de solo lectura.  

```javascript
var documentTitle = webview.documentTitle;
```  

#### Valor de propiedad  

Tipo: **cadena**  

El título de la página.  

### height  

Obtiene o establece el alto de la **vista en WebView**.  

```javascript
var height = webview.height;
webview.height = height;
```  

#### Valor de propiedad  

Tipo: **número**  

El alto de la **vista en WebView**.  

### proceso  

Obtiene el proceso de **WebView** .  

Esta propiedad es de solo lectura.  

```javascript
var process = webview.process;
webview.process = process;
```  

#### Valor de propiedad  

Escriba: [MSWebViewProcess](./webview/MSWebViewProcess.md)  

### settings  

Obtiene un objeto [MSWebViewSettings](./webview/MSWebViewSettings.md) que contiene propiedades para habilitar o deshabilitar las características de **WebView** .  

Esta propiedad es de solo lectura.  

```javascript
var settings = webview.settings;
webview.settings = settings;
```  

#### Valor de propiedad  

Escriba: [MSWebViewSettings](./webview/MSWebViewSettings.md)  

Un objeto [MSWebViewSettings](./webview/MSWebViewSettings.md) que contiene propiedades para habilitar o deshabilitar características de **WebView** .  

### src  

Obtiene o establece el origen del identificador uniforme de recursos (URI) del contenido HTML que se va a mostrar en el control **WebView** .  

```javascript
var src = webview.src;
webview.src = src;
```  

#### Valor de propiedad  

Tipo: **cadena**  

El origen de URI del contenido HTML que se muestra en el control **WebView** .  

### width  

Obtiene o establece el ancho de la **vista en WebView**.  

```javascript
var width = webview.width;
webview.width = width;
```  

#### Valor de propiedad  

Tipo: **número**  

El ancho de la **vista en WebView**.  

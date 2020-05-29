---
title: Referencia de la API de MSApp
description: Proporciona funciones auxiliares que permiten crear objetos BLOB y MSStream. Los objetos y miembros de MSApp son compatibles con las aplicaciones de Windows que usan JavaScript.
author: mattwojo
ms.author: mattwoj
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, carga de archivos, blog, MSStream, aplicaciones de Windows 10, UWP, Edge
ms.openlocfilehash: 0ed8cefa918bd44f3b2c4e8312d2c1d3b4ace8fc
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574921"
---
# MSApp

El objeto MSApp y sus miembros solo se admiten en aplicaciones de Windows que usen JavaScript (incluyendo PWAs de acceso a las características de la API de Windows). El objeto MSApp solo existe en el contexto local de un documento HTML en una aplicación de Windows que se carga mediante el esquema de URI MS-appx; de lo contrario, el objeto no existe (y, por lo tanto, ninguno de sus métodos y propiedades está disponible).

Proporciona funciones auxiliares que permiten crear objetos [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) y [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) .

```javascript
var result = MSApp.method;
```

| | |
| :--- | :--- |
| [**Métodos**](#msapp-methods) | [clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority, getHtmlPrintDocumentSource](#getcurrentpriority),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId, isTaskScheduledAtPriorityOrHigher](#getviewid) [, pageHandlesAllApplicationActivations](#istaskscheduledatpriorityorhigher) [, suppressSubdownloadCredentialPrompts, terminateApp.](#pagehandlesallapplicationactivations) [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource) [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts) [terminateApp](#terminateapp) |

| | |
| :--- | :--- |
| [**Constantes**](#msapp-constants) | [actual](#current), [alta](#high), [inactiva](#idle), [normal](#normal).|

| | |
| :--- | :--- |
| [Interfaz **MSAppAsyncOperation**](#msappasyncoperation) | [start](#start) |

## Métodos de MSApp

### clearTemporaryWebDataAsync 
Borra los datos de caché y indexedDB de la aplicación o [WebView](../../webview.md).

```javascript
var retval = MSApp.clearTemporaryWebDataAsync(#); 
```

#### Parameters
Este método no tiene parámetros.

#### Valor devuelto
Escrita[`IAsyncAction`](/uwp/api/windows.foundation.iasyncaction)

Representa una acción asincrónica.

### createBlobFromRandomAccessStream
Crea un objeto [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) a partir de un [`IRandomAccessStream`](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) objeto. Este método se debe usar cuando se trata de `IRandomAccessStream` objetos en aplicaciones para crear un objeto basado en el consorcio desde la secuencia. Una vez creado el BLOB, se puede usar con el [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), las [API de la dirección URL](https://developer.mozilla.org/docs/Web/API/URL)y [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest). 

```javascript
var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
```

#### Parameters

`type` por

|Tipo | Descripción |
|:---- |:--- |
|Cadena | Tipo de contenido de los datos. Esta cadena debe estar en el formato especificado en el símbolo de tipo multimedia definido en la sección 3,7 de RFC 2616.

`stream` por

|Tipo | Descripción |
|:---- |:--- |
|Cualquiera | [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) que se va a almacenar en el BLOB.

#### Valor devuelto
|Tipo | Descripción |
|:---- |:--- |
|Manchas | Nuevo objeto BLOB que contiene la secuencia.

#### Excepciones
|Excepción | Condición |
|:---- |:--- |
|TypeMismatchError | El tipo de nodo es incompatible con el tipo de parámetro esperado. En el caso de versiones anteriores a Internet Explorer 10, se devuelve TYPE_MISMATCH_ERR.

#### Observaciones
Crea un BLOB a partir de los tipos de Windows Runtime a través del espacio de nombres MSApp en el objeto de ventana. Este método creará un BLOB que es esencialmente un contenedor de luz sobre el objeto que se [`RandomAccessStream`](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) le proporciona. El BLOB es propietario de la duración de esta secuencia y la secuencia se cerrará cuando se destruya el BLOB. 

#### Ejemplo

```javascript
var randomAccessStream = dataPackage.GetData("image/bmp");
var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});

document.getElementById("imagetag").src = url; 
```

### createDataPackage
Convierte el intervalo especificado del usuario o la aplicación en un fragmento de HTML que se puede compartir.

```javascript
var retVal = MSApp.createDataPackage(object); 
```

#### Parameters
`object` por

|Tipo | Descripción |
|:---- |:--- |
|Cualquiera | Este rango puede crearse desde un objeto de selección, por ejemplo: `window.selection.getRangeAt(0)` , o manualmente.

#### Valor devuelto
|Tipo | Descripción |
|:---- |:--- |
|Cualquiera | Contiene el formato HTML del rango especificado.

#### Observaciones
Este método solo admite el [rango Dom (modelo de objetos de documento)](https://developer.mozilla.org/docs/Web/API/Range), no [TextRange](/uwp/api/windows.ui.xaml.documents.textrange). El paquete de datos devuelto para el intervalo especificado contiene formato HTML en el formato del portapapeles.

No hay ninguna propiedad disponible para el paquete de datos devuelto.

### createDataPackageFromSelection 
Convierte la selección del usuario o la aplicación en un fragmento HTML que se puede compartir.

```javascript
var retVal = MSApp.createDataPackageFromSelection(); 
```

#### Parameters
Este método no tiene parámetros.

#### Valor devuelto
|Tipo | Descripción |
|:---- |:--- |
|Cualquiera | Contiene el formato HTML del rango especificado.

#### Observaciones
El paquete de datos devuelto para la selección contiene marcado HTML en formato de Portapapeles. Si no hay ninguna selección del usuario en ninguna parte de la interfaz de usuario de la aplicación, `createDataPackageFromSelection` devuelve NULL.

No hay ninguna propiedad disponible para el paquete de datos devuelto.
 
### createFileFromStorageFile 
Convierte un [WinRT](/uwp/api/) [`StorageFile`](/uwp/api/windows.storage.storagefile) en un objeto estándar de W3C [`File`](https://developer.mozilla.org/docs/Web/API/File) .

```javascript
var retVal = MSApp.createFileFromStorageFile(storageFile); 
```

#### Parameters
`storageFile` por

|Tipo | Descripción |
|:---- |:--- |
|Cualquiera | Contiene el archivo de almacenamiento.

#### Excepciones
|Excepción | Condición |
|:---- |:--- |
|TypeMismatchError | La referencia del archivo W3C especificada no es válida. En el caso de versiones anteriores a Internet Explorer 10, se devuelve TYPE_MISMATCH_ERR.

### createStreamFromInputStream  

Crea una [`MSStream`](https://msdn.microsoft.com/library/hh772328) a partir de una [`InputStream`](https://msdn.microsoft.com/library/hh772327) .  


```javascript
var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
```

#### Parameters
`type` por

|Tipo | Descripción |
|:---- |:--- |
|DOMString | Tipo de contenido de los datos. Esta cadena debe estar en el formato especificado en el símbolo de tipo multimedia definido en la sección 3,7 de RFC 2616. ([Consulte tipos MIME,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types) IE. texto/sin formato, texto/HTML, image/JPEG, image/png, audio/MPEG, audio/OGG, audio/*, Video/MP4, etc.). 

`inputStream` por

|Tipo | Descripción |
|:---- |:--- |
|Cualquiera | El [`IInputStream`](/uwp/api/Windows.Storage.Streams.IInputStream) que se va a almacenar en `MSStream` .

#### Observaciones
Este método toma un tipo de contenido y la `IInputStream` referencia. El método comprueba entonces que la referencia de la secuencia que se ha pasado es una instancia de tipo `IInputStream` y, si no es así, se inicia `DOMException TYPE_MISMATCH_ERR` . Si no se produce ningún error, `createStreamFromInputStream` crea una `MSStream` (a partir de sus entradas).

#### Ejemplo
`IInputStream`Se puede usar una para crear un `MSStream` . Al igual que los `MSStreams` objetos de un solo uso, todas las direcciones URL creadas por `URL.createObjectURL` se revocan la primera vez que el elemento de imagen las resuelve. Además, se producirá un error en las solicitudes de una segunda dirección URL en este objeto después de que se haya usado la secuencia.

```javascript
var inputStream = myInputStream; //get InputStream from socket API, etc.
var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
document.getElementById("imagetag").src = URL.createObjectURL(stream); 
```

### execAsyncAtPriority 
Programa una devolución de llamada que se ejecutará en un momento posterior según la prioridad dada. 

```javascript
MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
```

#### Parameters
`asynchronousCallback` por

|Tipo | Descripción |
|:---- |:--- |
|Función | Función de devolución de llamada que se ejecuta de forma asincrónica, distribuida a la prioridad de prioridad dada.

`priority` por

|Tipo | Descripción |
|:---- |:--- |
|DOMString | El valor de prioridad contextual en el que se ejecuta la devolución de llamada de asynchronousCallback. Consulta [constantes MSApp](#msapp-constants).

`args` por

|Tipo | Descripción |
|:---- |:--- |
|Cualquiera | Una serie opcional de argumentos que se pasan a la función de devolución de llamada synchronousCallback (como parámetros 1 y on).

#### Valor devuelto
Este método no devuelve un valor.

#### Observaciones
La `asynchronousCallback` función de devolución de llamada proporcionada se ejecuta de forma asincrónica más adelante. `asynchronousCallback` se enviarán según la prioridad proporcionada. La prioridad normal es equivalente al [`setImmediate`](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) método existente. Cuando se ejecuta la devolución de llamada, la prioridad contextual actual se establece en el valor de parámetro de prioridad proporcionado para la duración de la ejecución de la devolución de llamada.

El `asynchronousCallback` parámetro callback puede ser cualquier función. Si se proporcionan argumentos después del `priority` parámetro, todos se transferirán a la función de devolución de llamada.

A diferencia `execAtPriority` de, cualquier objeto devuelto por la `asynchronousCallback` función callback se omite (y no se devuelve a través de `execAsyncAtPriority` ).

### execAtPriority 
Ejecuta la función de devolución de llamada especificada en la prioridad contextual indicada.

```javascript
var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
```

#### Parameters
`synchronousCallback` por

|Tipo | Descripción |
|:---- |:--- |
|Función | Función de devolución de llamada que se ejecuta sincrónicamente a la prioridad de prioridad dada.

`priority` por

|Tipo | Descripción |
|:---- |:--- |
|DOMString | El valor de prioridad especificado al que se establecerá el valor de prioridad contextual actual al ejecutar la `synchronousCallback` función de devolución de llamada. Consulta [constantes MSApp](#msapp-constants).

`args` por

|Tipo | Descripción |
|:---- |:--- |
|Cualquiera | Una serie opcional de argumentos que se pasan a la `synchronousCallback` función de devolución de llamada (como parámetros 1 y on).

#### Valor devuelto
|Tipo | Descripción |
|:---- |:--- |
|Cualquiera | Devuelve el valor devuelto de la `synchronousCallback` devolución de llamada (según corresponda).

#### Observaciones
El `synchronousCallback` método de devolución de llamada proporcionado se ejecuta de forma sincrónica. La prioridad actual contextual se cambia al valor de prioridad proporcionado (dado por el argumento Priority) para la duración de la función de devolución de llamada proporcionada. Una vez que la función de devolución de llamada termine de ejecutarse, la prioridad se devuelve al valor anterior antes de la `execAtPriority` llamada. El valor devuelto de `execAtPriority` es el valor devuelto del método de devolución de llamada (tal y como se proporciona).
 
El `synchronousCallback` parámetro callback puede ser cualquier función. Si se proporciona cualquier argumento después del parámetro Priority, se pasarán al método de devolución de llamada proporcionado. Si el parámetro callback devuelve un valor, este valor también se convierte en el valor devuelto `execAtPriority` .

#### Ejemplo

```javascript
var user = Windows.System.UserProfile.UserInformation;

MSApp.execAtPriority(function () { // This callback executes synchronously.
  user.getFirstNameAsync().then(function () { // Dispatches at high priority.
    return user.getLastNameAsync();
  }).done(function () { // Dispatches at high priority.
    // USEFUL CODE HERE
  });
}, MSApp.HIGH); // The second argument of the execAtPriority method.
```

### getCurrentPriority 
Devuelve la prioridad contextual actual.

```javascript
var retval = MSApp.getCurrentPriority();
```

#### Parameters
Ninguna. 

#### Valor devuelto
|Tipo | Descripción |
|:---- |:--- |
|DOMString | El valor devuelto es una de las cadenas `MSApp.HIGH` , `MSApp.NORMAL` , o `MSApp.IDLE` .

#### Observaciones
Este método devuelve la prioridad contextual actual (vea la [`MSApp Constants`](#msapp-constants) ), que puede cambiarse a través `execAtPriority` de y `execAsyncAtPriority` .

#### Ejemplo

```javascript
if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
  // YOUR CODE HERE
}
```

### getHtmlPrintDocumentSource  

API sincrónica que ha quedado obsoleta. Para Windows 10, consulte `getHtmlPrintDocumentSourceAsync` . Para las aplicaciones de Windows 8 y 8,1, consulte la entrada de MSDN para [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).  

### getHtmlPrintDocumentSourceAsync
Devuelve el contenido de origen que se va a imprimir.

#### Parameters
`htmlDoc` por

|Tipo | Descripción |
|:---- |:--- |
|Documento | Documento HTML que se va a imprimir. Puede ser el documento raíz, el documento en un iframe, un fragmento de documento o un documento SVG. Tenga en cuenta que htmlDoc debe ser un documento, no un elemento.

#### Ejemplo 1

```javascript
var printTask = event.request.createPrintTask(title, function (args) {
                var deferral = args.getDeferral();
                var getPrintDocumentSourceAsync;
                if (MSApp.getHtmlPrintDocumentSourceAsync) { // Windows 10
                    getPrintDocumentSourceAsync = MSApp.getHtmlPrintDocumentSourceAsync(document);
                } else {
                    getPrintDocumentSourceAsync = WinJS.Promise.as(MSApp.getHtmlPrintDocumentSource(document));
                }
                getPrintDocumentSourceAsync.then(function (source) {
                    args.setSource(source);
                    deferral.complete();
                }, function (error) {
                    console.error(error);
                    deferral.complete();
                });
            });
```

#### Ejemplo 2

```javascript
    function registerForPrintContract() {
            var printManager = Windows.Graphics.Printing.PrintManager.getForCurrentView();
            printManager.onprinttaskrequested = onPrintTaskRequested;
            console.log("Print Contract registered. Use the Print button to print.", "sample", "status");
    }
    
    // Variable to hold the document source to print
    var gHtmlPrintDocumentSource = null;
    
    // Print event handler for printing via the PrintManager API.
    function onPrintTaskRequested(printEvent) {
        var printTask = printEvent.request.createPrintTask("Print Sample", function (args) {
            args.setSource(gHtmlPrintDocumentSource);
    
            // Register the handler for print task completion event
            printTask.oncompleted = onPrintTaskCompleted;
        });
    }
    
    // Print Task event handler is invoked when the print job is completed.
    function onPrintTaskCompleted(printTaskCompletionEvent) {
        // Notify the user about the failure
        if (printTaskCompletionEvent.completion === Windows.Graphics.Printing.PrintTaskCompletion.failed) {
            console.log("Failed to print.", "sample", "error");
        }
    }
    
    // Executed just before printing.
    var beforePrint = function () {
        // Replace with code to be executed just before printing the current document:
    };
    
    // Executed immediately after printing.
    var afterPrint = function () {
        // Replace with code to be executed immediately after printing the current document:
    };
    
    function printButtonHandler() {
        // Optionally, functions to be executed immediately before and after printing can be configured as following:
        window.document.body.onbeforeprint = beforePrint;
        window.document.body.onafterprint = afterPrint;
    
        // Get document source to print
        MSApp.getHtmlPrintDocumentSourceAsync(document).then(function (htmlPrintDocumentSource) {
            gHtmlPrintDocumentSource = htmlPrintDocumentSource;
    
            // If the print contract is registered, the print experience is invoked.
            Windows.Graphics.Printing.PrintManager.showPrintUIAsync();
        });
    }
```

### getViewId 
Compatibilidad con varias ventanas. 

> [!NOTE] 
> En las aplicaciones para UWP con JavaScript para Windows 8.1, se admiten varias ventanas con las API de MSApp DOM que ahora son depricated. Para Windows 10, use `window.open` , `window` y el nuevo `MSApp.getViewId` .

| Descripción |Windows 10 | Windows 8.1 |  
|:---- |:---- |:--- |  
| Crear nueva ventana | [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) | [`MSApp.createNewView`](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
|Nuevo objeto de ventana | [`window`](https://developer.mozilla.org/docs/Web/API/Window) |[`MSAppView`](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  

```javascript
var retval = MSApp.getViewId(window); 
```

#### Parameters
`window`

|Tipo | Descripción |
|:---- |:--- |
|DOMString | Un objeto que representa una ventana que contiene un documento DOM. | 

#### Valor devuelto

`viewId`

|Tipo | Descripción |
|:---- |:--- |
|Número | Puede usarse con las distintas [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) API. 

#### Observaciones
Use [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) y [`window`](https://developer.mozilla.org/docs/Web/API/Window) para crear nuevas ventanas, pero después, para interactuar con las API de WinRT, agregue la `MSApp.getViewId` API. Toma un `window` objeto como parámetro y devuelve un `viewId` número que se puede usar con las distintas [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) API. 

##### Retrasar la visibilidad 
Normalmente, las vistas de WinRT se inician de forma oculta y el desarrollador final usa algo como `TryShowAsStandaloneAsync` para mostrar la vista una vez que se ha preparado por completo. En el mundo web, `window.open` muestra inmediatamente una ventana y el usuario final puede ver que el contenido se carga y se representa. Para que la nueva Windows funcione como vistas en WinRT y no se muestre inmediatamente, hemos añadido una `window.open` opción. Por ejemplo:
`let newWindow = window.open("https://example.com", null, "msHideView=yes");`

##### Diferencias entre ventanas principales
La ventana principal que inicialmente abre el sistema operativo funciona de forma diferente a la de las ventanas secundarias que abre: 

|Descripción | Principal | Secundario |
|:---- |:--- |:--- |
|Window. Open | Se permite | No permitido |
|Window. Close | Cerrar aplicación | Cerrar ventana |
| Restricciones de navegación | ACUR solo | Sin restricciones |

La restricción para no permitir la apertura de ventanas secundarias podría cambiar en el futuro en función de los [comentarios](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).

##### Restricciones de comunicación del mismo origen 
Hay un difícil problema técnico que evita que se admitan las llamadas a secuencias de comandos sincrónicas, del mismo origen y de ventana cruzada. Cuando se abre una ventana que tiene el mismo origen, se permite que la secuencia de comandos de una ventana llame directamente a las funciones de la otra ventana y se producirá un error en algunas de estas llamadas. `postMessage` las llamadas funcionan perfectamente y es la manera recomendada de hacer cosas si es posible. El trabajo para mejorar este problema está en curso.


### isTaskScheduledAtPriorityOrHigher 
Devuelve un valor de tipo Boolean que indica si hay trabajo pendiente en el nivel de prioridad dado o superior.

```javascript
var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
```

#### Parameters
`priority` por

|Tipo | Descripción |
|:---- |:--- |
|DOMString | Un valor de prioridad (vea [constantes MSApp](#msapp-constants)) que especifica el nivel de prioridad y superior para consultar cualquier trabajo pendiente en la cola.

#### Valor devuelto
|Tipo | Descripción |
|:---- |:--- |
|Booleano | Devuelve `true` si hay algún trabajo en cola en el nivel de prioridad especificado o superior, de `false` lo contrario.

#### Observaciones
El `isTaskScheduledAtPriorityOrHigher` método proporciona un medio para que el código de JavaScript determine si hay trabajo pendiente en los distintos niveles de prioridad (o posteriores) con la intención de que el código JavaScript de la llamada pueda decidir dar lugar a un trabajo de mayor prioridad.

#### Ejemplo

```javascript
function performIdleWork(array_in) {
  var idx = 0;

  function performIdleWorkHelper() {
    for (; idx < array_in.length; ++idx) {

      // USEFUL CODE HERE 

      if (MSApp.isTaskScheduledAtPriorityOrHigher(MSApp.NORMAL)) {
        MSApp.execAsyncAtPriority(performIdleWorkHelper, msPriority.IDLE);
        break;
      } // if
    } // for
  } // performIdleWorkHelper

  performIdleWorkHelper();
} // performIdleWork
```

### pageHandlesAllApplicationActivations
Se usa para evitar una actualización de la ruta de acceso de inicio (volver a cargar la página) antes de cada evento Activate (es decir, haciendo clic en una notificación o en un mosaico anclado). 

#### Parameters

|Tipo | Descripción |
|:---- |:--- |
Booleano | Use `MSApp.pageHandlesAllApplicationActivations(true)` esta para omitir siempre la actualización de la ruta de inicio (volver a cargar la página) y, en su lugar, saltar directamente al desencadenar el `WebUIApplication` evento activado. Requiere que todas las páginas manejen los eventos de activación por separado. Al definir este método como `true` , al hacer clic en un evento activado (como un notificaiton), no se activará la recarga, una de las aplicaciones básicas para las aplicaciones de una sola página que deseen evitar la recarga de la página.

#### Ejemplo 

```javascript
// Without this, the app will first refresh to the start path before every activate event
window.MSApp.pageHandlesAllApplicationActivations(true); 

// This must not be deffered so that it can receive the initial `activated` event in time
window.Windows.UI.WebUI.WebUIApplication.addEventListener(
    `activated`,
    e =>
        microsoftInterface.handleActivatedEvent(e);
    }),
    false
);
```

### suppressSubdownloadCredentialPrompts 
Controla si una aplicación suprime posibles mensajes de autenticación durante la descarga de recursos.

```javascript
MSApp.suppressSubdownloadCredentialPrompts(suppress); 
```

#### Parameters
`suppress` por

|Tipo | Descripción |
|:---- |:--- |
|Booleano | El valor true suprime las solicitudes de autenticación potenciales. El valor false no suprime ninguna solicitud de autenticación potencial del usuario.

#### Valor returado
Ninguna.

#### Observaciones
El `suppressSubdownloadCredentialPrompts` método controla si una aplicación suprime las solicitudes de autenticación potenciales durante la descarga de recursos. El comportamiento predeterminado es no suprimir las solicitudes de credenciales.

`suppressSubdownloadCredentialPrompts` está pensado para que lo usen aplicaciones que pueden cargar un número excesivo de recursos que requieren autenticación, como una aplicación de correo (que puede contener un boletín con un número de imágenes en el que cada imagen requiera autenticación).

Al suprimir las solicitudes de credenciales, los cuadros de diálogo para autenticar a los servidores no se mostrarán al acceder a los recursos que requieren autenticación, y el recurso no se descargará. Tenga en cuenta que no `suppressSubdownloadCredentialPrompts` afecta otros indicadores posibles, como la autenticación de proxy o los cuadros de diálogo de solicitud de certificación del cliente, ni afecta a XHR.

Tenga en cuenta que `suppressSubdownloadCredentialPrompts` afecta a todo el contenido de la aplicación, incluido el contenido hospedado en el `webview` elemento.
 
**Importante:**  Las decisiones de solicitud de credenciales se almacenan en caché. Por lo tanto, aunque la supresión de las solicitudes de credenciales surtirá efecto inmediatamente, es posible que sea necesario volver a cargar el documento para permitir las solicitudes de credenciales después de suprimirlas.

#### Ejemplo

```javascript
/ Set to true to suppress potenial credential prompts:
MSApp.suppressSubdownloadCredentialPrompts(true); 
// Now one can load content or navigate iframe/webview to some other site.
```

### terminateApp
Finaliza la aplicación actual y genera un informe de error. 

```javascript
MSApp.terminateApp(error); 
```

#### Parameters
`error` por

Tipo | Descripción |
|:---- |:--- |
|Error | Un `Error` objeto que se puede usar para describir el error que ha desencadenado la finalización. El `Error` objeto debe contener las propiedades Number, Description y stack; no se generará un informe de errores si el objeto no contiene estas propiedades.

#### Valor devuelto
Ninguna.

#### Observaciones
Si el problema notificado por `terminateApp` se convierte en uno de los cinco principales problemas de la aplicación, se mostrará en la página calidad de la aplicación.

#### Ejemplo
Este ejemplo llama `terminateApp` cuando se encuentra una excepción. Usa el `Error` objeto proporcionado cuando se detecta una excepción. 

```javascript
try {  
        var obj2 = null;  
        obj2.val = 5;  
    }  
    catch(e) {  
        window.MSApp.terminateApp(e);  
    }  
```

### Constantes MSApp
Valores de prioridad permitidos asociados con `execAsyncAtPriority` ,, `execAtPriority` `getCurrentPriority` y `isTaskScheduldAtPriorityOrHigher` .

#### Actual
`current`

|Tipo | Descripción |
|:---- |:--- |
|DOMString | Cuando `current` se usa con el método adecuado (vea también la sección), el método usará la prioridad contextual actual al ejecutar la operación solicitada.

#### Alto
`high`

|Tipo | Descripción |
|:---- |:--- |
|DOMString | Cuando `high` se usa con el método adecuado (vea también la sección), el método usará una prioridad mayor que la normal al ejecutar la operación solicitada y se enviará la operación antes de que se realice cualquier trabajo de prioridad normal existente.

#### Inactivo
`idle`

|Tipo | Descripción |
|:---- |:--- |
|DOMString | Cuando `ideal` se usa con el método adecuado (vea también la sección), el método usará la prioridad inferior a la normal al ejecutar la operación solicitada y se enviará la operación después de cualquier trabajo de prioridad normal existente.

#### Normal
`normal`

|Tipo | Descripción |
|:---- |:--- |
|DOMString | Cuando `normal` se usa con el método adecuado (vea también la sección), el método usará la prioridad normal existente al ejecutar la operación solicitada.

#### Ejemplo

```javascript
if (window.MSApp.CURRENT) {
  document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
}
```

#### Requisitos
|IDL | Mshtml. idl |
|:---- |:--- |

## MSAppAsyncOperation

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```

### start
Inicia el `MSAppAsyncOperation` .

```javascript
var retval = MSAppAsyncOperation.start();
```

#### Parameters
Ninguna.

#### Valor devuelto
Ninguna.

#### Propiedades
`error` propiedad

|Tipo | Descripción |
|:---- |:--- |
|DOMError | Representa un error en `MSAppAsyncOperation` .

```javascript
p = object.error
```

`oncomplete` propiedad

|Tipo | Descripción |
|:---- |:--- |
|EventHandler | Propiedad para establecer un controlador de eventos finalizado `MSAppAsyncOperation` .

```javascript
p = object.oncomplete
```

`onerror` propiedad

|Tipo | Descripción |
|:---- |:--- |
|EventHandler | Propiedad para establecer un controlador de eventos cuando se produce un error `MSAppAsyncOperation` .

```javascript
p = object.onerror
```

`readyState` propiedad

|Tipo | Descripción |
|:---- |:--- |
|Número | Representa el estado de la operación asincrónica dentro de la aplicación de Windows con JavaScript. Los valores son: iniciada [0], completada el [1], error [2].

```javascript
p = object.readyState
```

`result` propiedad

|Tipo | Descripción |
|:---- |:--- |
|Cualquiera |Representa el resultado de `MSAppAsyncOperation` .

```javascript
p = object.result
```

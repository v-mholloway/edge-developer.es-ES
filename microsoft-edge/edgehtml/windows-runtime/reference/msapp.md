---
title: Referencia de api de MSApp
description: Proporciona funciones auxiliares que permiten crear objetos Blob y MSStream.  Los objetos y miembros de MSApp son compatibles con aplicaciones de Windows con JavaScript.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, carga de archivos, Blog, MSStream, aplicaciones de Windows 10, uwp, edge
ms.date: 03/16/2021
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0607929971b1dd2956571304230f69f756497e32
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439727"
---
# <a name="msapp"></a>MSApp  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

El objeto MSApp y sus miembros solo son compatibles con aplicaciones de Windows con JavaScript \(incluidos los PWA que acceden a las características de la API de Windows\).  El objeto MSApp solo existe en el contexto local de un documento HTML en una aplicación de Windows cargada mediante el esquema uri ms-appx; de lo contrario, el objeto no existe (y, por lo tanto, ninguno de sus métodos y propiedades están disponibles).  

Proporciona funciones auxiliares que permiten crear [objetos Blob](https://developer.mozilla.org/docs/Web/API/Blob) y [MSStream.](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx)  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [Métodos](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      [clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource ,](#gethtmlprintdocumentsource)[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Constantes](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      [current](#current), [high](#high), [idle](#idle), [normal](#normal).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Interfaz MSAppAsyncOperation](#msappasyncoperation)  
   :::column-end:::
   :::column span="2":::
      [start](#start)  
   :::column-end:::
:::row-end:::  

## <a name="msapp-methods"></a>Métodos MSApp  

### <a name="cleartemporarywebdataasync"></a>clearTemporaryWebDataAsync  

:::row:::
   :::column span="":::
      Borra los datos de caché e indexedDB para la aplicación o [WebView](../../hosting/webview/index.md).  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.clearTemporaryWebDataAsync(#); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      Este método no tiene parámetros.  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**  
      
      Tipo: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)  
      
      Representa una acción asincrónica.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      Ninguna.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Por ejemplo:**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createblobfromrandomaccessstream"></a>createBlobFromRandomAccessStream  

:::row:::
   :::column span="":::
      Crea un [blob](https://developer.mozilla.org/docs/Web/API/Blob) a partir de [un objeto IRandomAccessStream.](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)  Este método debe usarse al tratar con objetos de aplicaciones para crear un objeto basado en `IRandomAccessStream` W3C a partir de la secuencia.  Una vez creado el blob, se puede usar con [filereader](https://developer.mozilla.org/docs/Web/API/FileReader), [API de dirección URL](https://developer.mozilla.org/docs/Web/API/URL)y [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `type` [in]  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Cadena | Tipo de contenido de los datos.  Esta cadena debe tener el formato especificado en el token de tipo multimedia definido en la sección 3.7 de RFC 2616.  |  
      
      `stream` [in]  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Cualquiera | [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) que se almacenará en el blob.  |  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Blob | Nuevo objeto blob que contiene la secuencia.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      | Excepción | Condición |  
      |:---- |:--- |  
      | TypeMismatchError | El tipo de nodo es incompatible con el tipo de parámetro esperado.  Para las versiones anteriores a Internet Explorer 10, TYPE_MISMATCH_ERR se devuelve.  |  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      Crea un blob a partir de tipos de Windows Runtime a través del espacio de nombres MSApp en el objeto de ventana.  Este método creará un blob que es esencialmente un contenedor de luz sobre el [objeto RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) que se le proporciona.  El blob es propietario de la duración de esta secuencia y la secuencia se cerrará cuando se destruya el blob.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Por ejemplo:**  
      
      ```javascript
      var randomAccessStream = dataPackage.GetData("image/bmp");
      var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
      var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});
      
      document.getElementById("imagetag").src = url; 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createdatapackage"></a>createDataPackage  

:::row:::
   :::column span="":::
      Convierte el intervalo especificado del usuario o de la aplicación en un fragmento HTML que se puede compartir.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackage(object); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `object` [in]  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Cualquiera | Este intervalo se puede crear a partir de un objeto de selección, por ejemplo: `window.selection.getRangeAt(0)` o manualmente.  |  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Cualquiera | Contiene el marcado HTML del intervalo especificado.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      Este método solo admite el intervalo del modelo de objetos de documento [(DOM),](https://developer.mozilla.org/docs/Web/API/Range)no [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).  El paquete de datos devuelto para el intervalo especificado contiene marcado HTML en formato portapapeles.  
      
      No hay propiedades disponibles para el paquete de datos devuelto.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Por ejemplo:**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createdatapackagefromselection"></a>createDataPackageFromSelection  

:::row:::
   :::column span="":::
      Convierte la selección del usuario o de la aplicación en un fragmento HTML que se puede compartir.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackageFromSelection(); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      Este método no tiene parámetros.  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Cualquiera | Contiene el marcado HTML del intervalo especificado.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      El paquete de datos devuelto para la selección contiene marcado HTML en formato portapapeles.  Si no hay ninguna selección de usuario en ninguna parte de la interfaz de usuario de la aplicación, `createDataPackageFromSelection` devuelve `null` .  
      
      No hay propiedades disponibles para el paquete de datos devuelto.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Por ejemplo:**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### <a name="createfilefromstoragefile"></a>createFileFromStorageFile  

:::row:::
   :::column span="":::
      Convierte un objeto [StorageFile de](/uwp/api/windows.storage.storagefile) [WinRT](/uwp/api/) en un objeto [File](https://developer.mozilla.org/docs/Web/API/File) W3C estándar.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createFileFromStorageFile(storageFile); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `storageFile` [in]
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Cualquiera | Contiene el archivo de almacenamiento.  |  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**
      
      Ninguno    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      | Excepción | Condición |  
      |:---- |:--- |  
      | TypeMismatchError | La referencia de archivo W3C especificada no es válida.  Para versiones anteriores a Internet Explorer 10, `TYPE_MISMATCH_ERR` se devuelve.  |  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      Ninguna.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Por ejemplo:**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createstreamfrominputstream"></a>createStreamFromInputStream  

:::row:::
   :::column span="":::
      Crea un [MSStream](https://msdn.microsoft.com/library/hh772328) a partir de [un InputStream](https://msdn.microsoft.com/library/hh772327).  
   :::column-end:::
   :::column span="":::
      ```javascript
      var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `type` [in]
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | Tipo de contenido de los datos.  Esta cadena debe tener el formato especificado en el token de tipo multimedia definido en la sección 3.7 de RFC 2616.  \([Ver tipos MIME,]( https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) como , , , , , , , y `text/plain` así `text/html` `image/jpeg` `image/png` `audio/mpeg` `audio/ogg` `audio/*` `video/mp4` sucesivamente\).  
      
      `inputStream` [in]
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Cualquiera | [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) que se va a almacenar en `MSStream` el archivo .  |  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**
      
      Ninguna.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      Este método toma un tipo de contenido y la `IInputStream` referencia.  A continuación, el método comprueba que la referencia de secuencia pasada es una instancia de tipo y, si `IInputStream` no es así, inicia `DOMException TYPE_MISMATCH_ERR` .  Si no se produce ningún error, `createStreamFromInputStream` crea `MSStream` un \(a partir de sus entradas\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Por ejemplo:**  
      
      An `IInputStream` se puede usar para crear un archivo `MSStream` .  Al igual que los objetos de uso único inherentes, todas las direcciones URL creadas por se revocan la primera vez que el elemento image lo `MSStreams` `URL.createObjectURL` resuelve.  Además, se producirá un error en las solicitudes de una segunda dirección URL en este objeto después de usar la secuencia.  
      
      ```javascript
      var inputStream = myInputStream; //get InputStream from socket API, and so on
      var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
      document.getElementById("imagetag").src = URL.createObjectURL(stream); 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="execasyncatpriority"></a>execAsyncAtPriority  

:::row:::
   :::column span="":::
      Programa una devolución de llamada para que se ejecute más adelante según la prioridad especificada.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `asynchronousCallback` [in]
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Función | Función de devolución de llamada para ejecutarse de forma asincrónica, enviada con la prioridad dada.  |  
      
      `priority` [in]
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | Valor de prioridad contextual en el que se ejecuta la devolución de llamada asynchronousCallback.  Vea [MSApp Constants](#msapp-constants).  |  
      
      `args` [in]
      
      | Tipo | Descripción |  
      |:---- |:--- |   
      | Cualquiera | Una serie opcional de argumentos que se pasan a la función de devolución de llamada sincrónicaCallback \(como parámetros 1 y así sucesivamente\).  |  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**  
      
      Este método no devuelve un valor.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      La función `asynchronousCallback` de devolución de llamada proporcionada se ejecuta de forma asincrónica más adelante.  `asynchronousCallback` se enviará de acuerdo con la prioridad proporcionada.  La prioridad normal es equivalente al método [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) existente.  Cuando se ejecuta la devolución de llamada, la prioridad contextual actual se establece en el valor del parámetro priority proporcionado durante la ejecución de la devolución de llamada.  
      
      El `asynchronousCallback` parámetro callback puede ser cualquier función.  Si se proporcionan argumentos después del parámetro, todos se pasarán `priority` a la función de devolución de llamada.  
      
      A diferencia de , cualquier objeto devuelto por la función de devolución de llamada se omite `execAtPriority` `asynchronousCallback` \(y no se devuelve a través `execAsyncAtPriority` de \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Por ejemplo:**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="execatpriority"></a>execAtPriority  

:::row:::
   :::column span="":::
      Ejecuta la función de devolución de llamada especificada con la prioridad contextual especificada.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `synchronousCallback` [in]  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Función | Función de devolución de llamada para ejecutarse sincrónicamente con la prioridad contextual de prioridad dada.  |  
      
      `priority` [in]  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | Valor de prioridad especificado en el que se establecerá el valor de prioridad contextual actual al ejecutar la `synchronousCallback` función de devolución de llamada.  Vea [MSApp Constants](#msapp-constants).  |  
      
      `args` [in]  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Cualquiera | Una serie opcional de argumentos que se pasan a la función de devolución de llamada `synchronousCallback` \(como parámetros 1 y así sucesivamente\).  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Cualquiera | Devuelve el valor devuelto de la `synchronousCallback` devolución de llamada \(as applicable\).  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      El método `synchronousCallback` de devolución de llamada proporcionado se ejecuta sincrónicamente.  La prioridad contextual actual se cambia al valor de prioridad proporcionado (dado por el argumento priority) durante la duración de la función de devolución de llamada proporcionada.  Una vez que la función de devolución de llamada termina de ejecutarse, se devuelve prioridad al valor anterior antes de la `execAtPriority` llamada.  El valor devuelto de `execAtPriority` es el valor devuelto del método de devolución de llamada \(como se proporciona\).  
      
      El `synchronousCallback` parámetro callback puede ser cualquier función.  Si se proporcionan argumentos después del parámetro priority, se pasarán al método de devolución de llamada proporcionado.  Si el parámetro callback devuelve un valor, este valor se convierte también en el valor `execAtPriority` devuelto.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Por ejemplo:**  
      
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
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="getcurrentpriority"></a>getCurrentPriority  

:::row:::
   :::column span="":::
      Devuelve la prioridad contextual actual.  

   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getCurrentPriority();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | El valor devuelto es una de las cadenas `MSApp.HIGH` `MSApp.NORMAL` , o `MSApp.IDLE` .  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      Este método devuelve la prioridad contextual actual \(see [MSApp Constants](#msapp-constants)\), que se puede cambiar a través `execAtPriority` de y `execAsyncAtPriority` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Por ejemplo:**  
      
      ```javascript
      if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
          // YOUR CODE HERE
      }
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="gethtmlprintdocumentsource"></a>getHtmlPrintDocumentSource  

API sincrónica que ha quedado en desuso.  Para Windows 10, consulta `getHtmlPrintDocumentSourceAsync` .  Para las aplicaciones de Windows 8 y 8.1, consulta la entrada de MSDN [para getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).  

### <a name="gethtmlprintdocumentsourceasync"></a>getHtmlPrintDocumentSourceAsync  

:::row:::
   :::column span="":::
      Devuelve el contenido de origen que se va a imprimir.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.getHtmlPrintDocumentSourceAsync(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `htmlDoc` [in]  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Documento | Documento HTML que se va a imprimir.  Puede ser el documento raíz, el documento en un iframe, un fragmento de documento o un documento SVG.  Tenga en cuenta que htmlDoc debe ser un documento, no un elemento.  |  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**
      
      Ninguna.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      Ninguna.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ejemplo 1**  
      
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
   :::column-end:::
   :::column span="":::
      **Ejemplo 2**  
      
      ```javascript
      function registerForPrintContract() {
              var printManager = Windows.Graphics.Printing.PrintManager.getForCurrentView();
              printManager.onprinttaskrequested = onPrintTaskRequested;
              console.log("Print Contract registered.  Use the Print button to print.", "sample", "status");
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
   :::column-end:::
:::row-end:::  

### <a name="getviewid"></a>getViewId  

:::row:::
   :::column span="":::
      Compatibilidad con varias ventanas.  
      
      > [!NOTE] 
      > En Win8.1, las aplicaciones para UWP de JavaScript admiten varias ventanas con LAS API dom de MSApp que ahora están depricadas.  Para Windows 10, usa `window.open` , y el nuevo `window` `MSApp.getViewId` .  
      
      | Descripción |Windows 10 | Windows 8.1 |  
      |:---- |:---- |:--- |  
      | Crear nueva ventana | [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) | [MSApp.createNewView](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |Nuevo objeto window | [ventana](https://developer.mozilla.org/docs/Web/API/Window) |[MSAppView](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getViewId(window); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `window`
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | Un objeto que representa una ventana que contiene un documento DOM.  |  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**  
      
      `viewId`
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Número | Se puede usar con las distintas [API de Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      Usa [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) y [window](https://developer.mozilla.org/docs/Web/API/Window) para crear ventanas nuevas, pero luego para interactuar con las API de WinRT, agrega la `MSApp.getViewId` API.  Toma un objeto como parámetro y devuelve un número que se puede usar con las `window` `viewId` distintas API [de Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)  
      
      *   Retrasar la visibilidad  
          
          Las vistas de WinRT normalmente comienzan ocultas y el desarrollador final usa algo parecido a mostrar la vista una vez `TryShowAsStandaloneAsync` que está totalmente preparada.  En el mundo web, muestra una ventana inmediatamente y el usuario final puede ver cómo se carga y `window.open` representa el contenido.  Para que las ventanas nuevas actúen como vistas en WinRT y no se muestren inmediatamente, hemos agregado una `window.open` opción.  Por ejemplo:  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   Diferencias de ventana principal  
          
          La ventana principal que abre inicialmente el sistema operativo actúa de forma diferente que las ventanas secundarias que se abren:  
          
          | Descripción | Principal | Secundario |  
          |:---- |:--- |:--- |  
          | window.open | Se permite | No permitido |  
          | window.close | Cerrar aplicación | Cerrar ventana |  
          | Restricciones de navegación | Solo ACUR | Sin restricciones |  
          
         <!-- The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).  -->  
      
      *   Restricciones de comunicación del mismo origen  
          
          Hay un problema técnico difícil que impide que se admitan correctamente las llamadas sincrónicas, del mismo origen, entre ventanas y scripts.  Al abrir una ventana que tiene el mismo origen, el script de una ventana puede llamar directamente a las funciones de la otra ventana y algunas de estas llamadas producirán un error.  `postMessage` las llamadas funcionan bien y es la forma recomendada de hacer las cosas si es posible.  Se está trabajando para mejorar este problema.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Por ejemplo:**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### <a name="istaskscheduledatpriorityorhigher"></a>isTaskScheduledAtPriorityOrHigher  

:::row:::
   :::column span="":::
      Devuelve un valor booleano que indica si hay trabajo pendiente en el nivel de prioridad dado o superior.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `priority` [in]
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | Valor de prioridad \(vea [MSApp Constants](#msapp-constants)\) que especifica el nivel de prioridad y superior para consultar cualquier trabajo en cola pendiente.  |  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Booleano | Devuelve si hay algún trabajo en cola en el nivel de prioridad especificado `true` o superior, de lo `false` contrario.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      El método proporciona un medio para que el código JavaScript determine si hay trabajo pendiente en los distintos niveles de prioridad \(o superior\) con la intención de que el código JavaScript que llama pueda decidir ceder al trabajo de mayor `isTaskScheduledAtPriorityOrHigher` prioridad.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Por ejemplo:**  
      
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
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="pagehandlesallapplicationactivations"></a>pageHandlesAllApplicationActivations  

:::row:::
   :::column span="":::
      Se usa para evitar una actualización de la ruta de inicio (recarga de página) antes de cada evento de activación \(como hacer clic en una notificación o en un icono anclado\).  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.pageHandlesAllApplicationActivations(boolean);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Booleano | Se usa para omitir siempre actualizar la ruta de inicio (recarga de página) y, en su lugar, saltar directamente a `MSApp.pageHandlesAllApplicationActivations(true)` activar el `WebUIApplication` evento activado.  Requiere que todas las páginas controle los eventos de activación por separado.  Al definir este método como , al hacer clic en un evento activado \(like a notification\) no se desencadenará la recarga, algo esencial para las aplicaciones de una sola página que deseen evitar las `true` recargas de página.  |  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**
      
      Ninguna.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      Ninguna.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Por ejemplo:**  
      
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
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="suppresssubdownloadcredentialprompts"></a>suppressSubdownloadCredentialPrompts  

:::row:::
   :::column span="":::
      Controla si una aplicación suprime los posibles mensajes de autenticación durante la descarga de recursos.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.suppressSubdownloadCredentialPrompts(suppress);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
     
      `suppress` [in]
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Booleano | Un valor true suprime los mensajes de autenticación potenciales.  Un valor de false no suprime los posibles mensajes de autenticación del usuario.  |  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**  
      
      Ninguna.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      El método controla si una aplicación suprime los posibles mensajes de `suppressSubdownloadCredentialPrompts` autenticación durante la descarga de recursos.  El comportamiento predeterminado es no suprimir los mensajes de credenciales.  
      
      `suppressSubdownloadCredentialPrompts` está diseñada para su uso por aplicaciones que pueden cargar un número excesivo de recursos que requieren autenticación, como una aplicación de correo \(que podría contener un boletín que contenga un número de imágenes donde cada imagen requiere autenticación\).  
      
      Cuando se suprimen los mensajes de credenciales, los cuadros de diálogo para la autenticación en los servidores no se mostrarán al obtener acceso a los recursos que requieren autenticación y el recurso no se descargará.  Tenga en cuenta que no afecta a otros mensajes posibles, como la autenticación proxy o los cuadros de diálogo de solicitud de certificación de cliente, ni afecta `suppressSubdownloadCredentialPrompts` a XHR.  
      
      Tenga en cuenta `suppressSubdownloadCredentialPrompts` que afecta a todo el contenido de la aplicación, incluido el contenido hospedado en el `webview` elemento.  
      
      > [!IMPORTANT]
      > Las decisiones de solicitud de credenciales se almacenan en caché.  Por lo tanto, mientras se suprimen los mensajes de credenciales tendrá efecto inmediatamente, para que los mensajes de credenciales después de suprimirlos necesiten una recarga del documento para que su efecto.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Por ejemplo:**  
      
      ```javascript
      // Set to true to suppress potential credential prompts:
      MSApp.suppressSubdownloadCredentialPrompts(true);
      // Now one can load content or navigate iframe/webview to some other site.
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="terminateapp"></a>terminateApp  


:::row:::
   :::column span="":::
      Termina la aplicación actual y genera un informe de errores.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.terminateApp(error);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      `error` [in]
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Error | Objeto `Error` que puede usar para describir el error que desencadenó la terminación.  El objeto debe contener el número, la descripción y las propiedades de la pila; no se generará un informe de errores si el objeto no `Error` contiene estas propiedades.  |  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**
      
      Ninguna.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      Si el problema notificado por se convierte en uno de los 5 problemas principales de la aplicación, aparecerá en la página `terminateApp` Calidad de la aplicación.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Por ejemplo:**  
      
      En este ejemplo se `terminateApp` llama cuando se encuentra una excepción.  Usa el objeto `Error` proporcionado al detectar una excepción.  
      
      ```javascript
      try {  
          var obj2 = null;  
          obj2.val = 5;  
      }  
      catch(e) {  
          window.MSApp.terminateApp(e);  
      }  
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="msapp-constants"></a>Constantes MSApp  

:::row:::
   :::column span="":::
      Valores de prioridad permitidos `execAsyncAtPriority` asociados con `execAtPriority` , , `getCurrentPriority` y `isTaskScheduldAtPriorityOrHigher` .  
   :::column-end:::
   :::column span="":::
      #### <a name="current"></a>Actual  
      
      `current`  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | When `current` is used with the appropriate method \(See also section\), the method will use the current contextual priority when executing the requested operation.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="high"></a>Alto  
      
      `high`  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | When `high` is used with the appropriate method \(See also section\), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.  |  
   :::column-end:::
   :::column span="":::
      #### <a name="idle"></a>Inactivo  
      
      `idle`  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | Cuando se usa con el método adecuado \(Vea también section\), el método usará una prioridad inferior a la normal al ejecutar la operación solicitada y se enviará la operación después de cualquier trabajo de prioridad `ideal` normal existente.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="normal"></a>Normal  
      
      `normal`  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | Cuando se usa con el método adecuado (vea también la sección), el método usará la prioridad existente normal al `normal` ejecutar la operación solicitada.  |  
   :::column-end:::
   :::column span="":::
      **Por ejemplo:**  
      
      ```javascript
      if (window.MSApp.CURRENT) {
          document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
      }
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Requisitos**  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | IDL | Mshtml.idl |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## <a name="msappasyncoperation"></a>MSAppAsyncOperation  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### <a name="start"></a>start  

:::row:::
   :::column span="":::
      Inicia `MSAppAsyncOperation` el archivo .  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSAppAsyncOperation.start();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parameters**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**
      
      Ninguna.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      
      **Propiedades**  
      
      `error` propiedad  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMError | Representa un error en `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` propiedad  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | EventHandler | Propiedad para establecer un controlador de eventos al completar `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` propiedad  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | EventHandler | Propiedad para establecer un controlador de eventos tras un error durante `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` propiedad  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Número | Representa el estado de la operación asincrónica dentro de la aplicación windows mediante JavaScript.  Los valores incluyen: `Started[0]` `Completed[1]` , , `Error[2]` .  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` propiedad  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Cualquiera |Representa el resultado de `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

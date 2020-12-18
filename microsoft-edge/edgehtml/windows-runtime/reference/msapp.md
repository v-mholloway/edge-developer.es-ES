---
title: Referencia de la API de MSApp
description: Proporciona funciones auxiliares que permiten crear objetos BLOB y MSStream.  Los objetos y miembros de MSApp son compatibles con las aplicaciones de Windows que usan JavaScript.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, carga de archivos, blog, MSStream, aplicaciones de Windows 10, UWP, Edge
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9a3ad670f61bfafa4480c538dd8f28c7013b7d7f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236198"
---
# MSApp  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

El objeto MSApp y sus miembros solo se admiten en aplicaciones de Windows que usen JavaScript \ (incluyendo PWAs de acceso a las características de la API de Windows \).  El objeto MSApp solo existe en el contexto local de un documento HTML en una aplicación de Windows que se carga mediante el esquema de URI MS-appx; de lo contrario, el objeto no existe (y, por lo tanto, ninguno de sus métodos y propiedades está disponible).  

Proporciona funciones auxiliares que permiten crear objetos [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) y [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) .  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [Métodos](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      [clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority, getHtmlPrintDocumentSource](#getcurrentpriority),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId, isTaskScheduledAtPriorityOrHigher](#getviewid) [, pageHandlesAllApplicationActivations](#istaskscheduledatpriorityorhigher) [, suppressSubdownloadCredentialPrompts, terminateApp.](#pagehandlesallapplicationactivations) [](#gethtmlprintdocumentsource) [](#suppresssubdownloadcredentialprompts) [](#terminateapp)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Constantes](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      [actual](#current), [alta](#high), [inactiva](#idle), [normal](#normal).  
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

## Métodos de MSApp  

### clearTemporaryWebDataAsync  

:::row:::
   :::column span="":::
      Borra los datos de caché y indexedDB de la aplicación o [WebView](../../hosting/webview/index.md).  
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
      
      Escriba: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)  
      
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
      **Ejemplo**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createBlobFromRandomAccessStream  

:::row:::
   :::column span="":::
      Crea un objeto [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) a partir de un objeto [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) .  Este método se debe usar cuando se trata de `IRandomAccessStream` objetos en aplicaciones para crear un objeto basado en el consorcio desde la secuencia.  Una vez creado el BLOB, se puede usar con el [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), las [API de la dirección URL](https://developer.mozilla.org/docs/Web/API/URL)y [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).  
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
      
      `type` por  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Cadena | Tipo de contenido de los datos.  Esta cadena debe estar en el formato especificado en el símbolo de tipo multimedia definido en la sección 3,7 de RFC 2616.  |  
      
      `stream` por  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Cualquiera | [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) que se va a almacenar en el BLOB.  |  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Manchas | Nuevo objeto BLOB que contiene la secuencia.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      | Excepción | Condición |  
      |:---- |:--- |  
      | TypeMismatchError | El tipo de nodo es incompatible con el tipo de parámetro esperado.  En el caso de versiones anteriores a Internet Explorer 10, se devuelve TYPE_MISMATCH_ERR.  |  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      Crea un BLOB a partir de los tipos de Windows Runtime a través del espacio de nombres MSApp en el objeto de ventana.  Este método creará un BLOB que es esencialmente un contenedor de luz sobre el objeto [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) que se proporciona.  El BLOB es propietario de la duración de esta secuencia y la secuencia se cerrará cuando se destruya el BLOB.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ejemplo**  
      
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

### createDataPackage  

:::row:::
   :::column span="":::
      Convierte el intervalo especificado del usuario o la aplicación en un fragmento de HTML que se puede compartir.  
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
      
      `object` por  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Cualquiera | Este rango puede crearse desde un objeto de selección, por ejemplo: `window.selection.getRangeAt(0)` , o manualmente.  |  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Cualquiera | Contiene el formato HTML del rango especificado.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      Este método solo admite el [rango Dom (modelo de objetos de documento)](https://developer.mozilla.org/docs/Web/API/Range), no [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).  El paquete de datos devuelto para el intervalo especificado contiene formato HTML en el formato del portapapeles.  
      
      No hay ninguna propiedad disponible para el paquete de datos devuelto.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ejemplo**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createDataPackageFromSelection  

:::row:::
   :::column span="":::
      Convierte la selección del usuario o la aplicación en un fragmento HTML que se puede compartir.  
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
      | Cualquiera | Contiene el formato HTML del rango especificado.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      El paquete de datos devuelto para la selección contiene marcado HTML en formato de Portapapeles.  Si no hay ninguna selección del usuario en ninguna parte de la interfaz de usuario de la aplicación, devuelve el número `createDataPackageFromSelection` `null` .  
      
      No hay ninguna propiedad disponible para el paquete de datos devuelto.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ejemplo**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### createFileFromStorageFile  

:::row:::
   :::column span="":::
      Convierte un [StorageFile](/uwp/api/windows.storage.storagefile) de [WinRT](/uwp/api/) en un objeto de [archivo](https://developer.mozilla.org/docs/Web/API/File) W3C estándar.  
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
      
      `storageFile` por
      
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
      | TypeMismatchError | La referencia del archivo W3C especificada no es válida.  Para las versiones anteriores a Internet Explorer 10, `TYPE_MISMATCH_ERR` se devuelve.  |  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      Ninguna.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ejemplo**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createStreamFromInputStream  

:::row:::
   :::column span="":::
      Crea un [MSStream](https://msdn.microsoft.com/library/hh772328) a partir de [InputStream](https://msdn.microsoft.com/library/hh772327).  
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
      
      `type` por
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | Tipo de contenido de los datos.  Esta cadena debe estar en el formato especificado en el símbolo de tipo multimedia definido en la sección 3,7 de RFC 2616.  \ ([Ver tipos MIME] (como https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) ,, `text/plain` `text/html` `image/jpeg` , `image/png` , `audio/mpeg` , `audio/ogg` , `audio/*` ,, etc `video/mp4` . \).  
      
      `inputStream` por
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Cualquiera | El [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) se almacena en `MSStream` .  |  
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
      
      Este método toma un tipo de contenido y la `IInputStream` referencia.  El método comprueba entonces que la referencia de la secuencia que se ha pasado es una instancia de tipo `IInputStream` y, si no es así, se inicia `DOMException TYPE_MISMATCH_ERR` .  Si no se produce ningún error, `createStreamFromInputStream` crea un `MSStream` \ (a partir de las entradas \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ejemplo**  
      
      `IInputStream`Se puede usar una para crear un `MSStream` .  Al igual que los `MSStreams` objetos de un solo uso, todas las direcciones URL creadas por `URL.createObjectURL` se revocan la primera vez que el elemento de imagen las resuelve.  Además, se producirá un error en las solicitudes de una segunda dirección URL en este objeto después de que se haya usado la secuencia.  
      
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

### execAsyncAtPriority  

:::row:::
   :::column span="":::
      Programa una devolución de llamada que se ejecutará en un momento posterior según la prioridad dada.  
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
      
      `asynchronousCallback` por
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Función | Función de devolución de llamada que se ejecuta de forma asincrónica, distribuida a la prioridad de prioridad dada.  |  
      
      `priority` por
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | El valor de prioridad contextual en el que se ejecuta la devolución de llamada de asynchronousCallback.  Consulta [constantes MSApp](#msapp-constants).  |  
      
      `args` por
      
      | Tipo | Descripción |  
      |:---- |:--- |   
      | Cualquiera | Una serie opcional de argumentos que se pasan a la función de devolución de llamada synchronousCallback \ (como parámetros 1 y así sucesivamente \).  |  
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
      
      La `asynchronousCallback` función de devolución de llamada proporcionada se ejecuta de forma asincrónica más adelante.  `asynchronousCallback` se enviarán según la prioridad proporcionada.  La prioridad normal es equivalente al método [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) existente.  Cuando se ejecuta la devolución de llamada, la prioridad contextual actual se establece en el valor de parámetro de prioridad proporcionado para la duración de la ejecución de la devolución de llamada.  
      
      El `asynchronousCallback` parámetro callback puede ser cualquier función.  Si se proporcionan argumentos después del `priority` parámetro, todos se transferirán a la función de devolución de llamada.  
      
      A diferencia `execAtPriority` de, cualquier objeto devuelto por la `asynchronousCallback` función callback se omite \ (y no se devuelve a través de `execAsyncAtPriority` \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ejemplo**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### execAtPriority  

:::row:::
   :::column span="":::
      Ejecuta la función de devolución de llamada especificada en la prioridad contextual indicada.  
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
      
      `synchronousCallback` por  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Función | Función de devolución de llamada que se ejecuta sincrónicamente a la prioridad de prioridad dada.  |  
      
      `priority` por  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | El valor de prioridad especificado al que se establecerá el valor de prioridad contextual actual al ejecutar la `synchronousCallback` función de devolución de llamada.  Consulta [constantes MSApp](#msapp-constants).  |  
      
      `args` por  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Cualquiera | Una serie opcional de argumentos que se pasan a la `synchronousCallback` función de devolución de llamada \ (como parámetros 1 y así sucesivamente).  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Cualquiera | Devuelve el valor devuelto de la `synchronousCallback` devolución de llamada \ (según corresponda \).  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      El `synchronousCallback` método de devolución de llamada proporcionado se ejecuta de forma sincrónica.  La prioridad actual contextual se cambia al valor de prioridad proporcionado (dado por el argumento Priority) para la duración de la función de devolución de llamada proporcionada.  Una vez que la función de devolución de llamada termine de ejecutarse, la prioridad se devuelve al valor anterior antes de la `execAtPriority` llamada.  El valor devuelto de `execAtPriority` es el valor devuelto del método de devolución de llamada \ (según se indica \).  
      
      El `synchronousCallback` parámetro callback puede ser cualquier función.  Si se proporciona cualquier argumento después del parámetro Priority, se pasarán al método de devolución de llamada proporcionado.  Si el parámetro callback devuelve un valor, este valor también se convierte en el valor devuelto `execAtPriority` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ejemplo**  
      
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

### getCurrentPriority  

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
      | DOMString | El valor devuelto es una de las cadenas `MSApp.HIGH` , `MSApp.NORMAL` , o `MSApp.IDLE` .  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      Este método devuelve la prioridad contextual actual \ (vea [constantes MSApp](#msapp-constants)\), que se puede cambiar mediante `execAtPriority` y `execAsyncAtPriority` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ejemplo**  
      
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

### getHtmlPrintDocumentSource  

API sincrónica que ha quedado obsoleta.  Para Windows 10, consulte `getHtmlPrintDocumentSourceAsync` .  Para las aplicaciones de Windows 8 y 8,1, consulte la entrada de MSDN para [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).  

### getHtmlPrintDocumentSourceAsync  

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
      
      `htmlDoc` por  
      
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

### getViewId  

:::row:::
   :::column span="":::
      Compatibilidad con varias ventanas.  
      
      > [!NOTE] 
      > En las aplicaciones para UWP con JavaScript para Windows 8.1, se admiten varias ventanas con las API de MSApp DOM que ahora son depricated.  Para Windows 10, use `window.open` , `window` y el nuevo `MSApp.getViewId` .  
      
      | Descripción |Windows 10 | Windows 8.1 |  
      |:---- |:---- |:--- |  
      | Crear nueva ventana | [Window. Open](https://developer.mozilla.org/docs/Web/API/Window/open) | [MSApp.createNewView](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |Nuevo objeto de ventana | [ventana](https://developer.mozilla.org/docs/Web/API/Window) |[MSAppView](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
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
      | Número | Puede usarse con las diversas API [Windows. UI. ViewManagement. ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) .  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      Usa [window. Open](https://developer.mozilla.org/docs/Web/API/Window/open) y [Window](https://developer.mozilla.org/docs/Web/API/Window) para crear nuevas ventanas, pero después, para interactuar con las API de WinRT, agrega la `MSApp.getViewId` API.  Toma un `window` objeto como parámetro y devuelve un `viewId` número que se puede usar con las distintas API de [Windows. UI. ViewManagement. ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) .  
      
      *   Retrasar la visibilidad  
          
          Normalmente, las vistas de WinRT se inician de forma oculta y el desarrollador final usa algo como `TryShowAsStandaloneAsync` para mostrar la vista una vez que se ha preparado por completo.  En el mundo web, `window.open` muestra inmediatamente una ventana y el usuario final puede ver que el contenido se carga y se representa.  Para que la nueva Windows funcione como vistas en WinRT y no se muestre inmediatamente, hemos añadido una `window.open` opción.  Por ejemplo:  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   Diferencias entre ventanas principales  
          
          La ventana principal que inicialmente abre el sistema operativo funciona de forma diferente a la de las ventanas secundarias que abre:  
          
          | Descripción | Principal | Secundario |  
          |:---- |:--- |:--- |  
          | Window. Open | Se permite | No permitido |  
          | Window. Close | Cerrar aplicación | Cerrar ventana |  
          | Restricciones de navegación | ACUR solo | Sin restricciones |  
          
          La restricción para no permitir la apertura de ventanas secundarias podría cambiar en el futuro en función de los [comentarios](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).  
      
      *   Restricciones de comunicación del mismo origen  
          
          Hay un difícil problema técnico que evita que se admitan las llamadas a secuencias de comandos sincrónicas, del mismo origen y de ventana cruzada.  Cuando se abre una ventana que tiene el mismo origen, se permite que la secuencia de comandos de una ventana llame directamente a las funciones de la otra ventana y se producirá un error en algunas de estas llamadas.  `postMessage` las llamadas funcionan perfectamente y es la manera recomendada de hacer cosas si es posible.  El trabajo para mejorar este problema está en curso.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ejemplo**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### isTaskScheduledAtPriorityOrHigher  

:::row:::
   :::column span="":::
      Devuelve un valor de tipo Boolean que indica si hay trabajo pendiente en el nivel de prioridad dado o superior.  
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
      
      `priority` por
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | Un valor de prioridad \ (vea [constantes MSApp](#msapp-constants)\) especificando el nivel de prioridad o superior para consultar cualquier trabajo pendiente en cola.  |  
   :::column-end:::
   :::column span="":::
      **Valor devuelto**  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Booleano | Devuelve `true` si hay algún trabajo en cola en el nivel de prioridad especificado o superior, de `false` lo contrario.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Excepciones**  
      
      Ninguna.  
   :::column-end:::
   :::column span="":::
      **Observaciones**  
      
      El `isTaskScheduledAtPriorityOrHigher` método proporciona un medio para que el código de JavaScript determine si hay trabajo pendiente en los distintos niveles de prioridad \ (o superior \) con la intención de que el código JavaScript de la llamada pueda decidir dar lugar a un trabajo de prioridad más alto.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ejemplo**  
      
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

### pageHandlesAllApplicationActivations  

:::row:::
   :::column span="":::
      Se usa para evitar una actualización de la ruta de inicio (volver a cargar la página) antes de cada evento Activate \ (como hacer clic en una notificación o en un mosaico anclado \).  
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
      | Booleano | Use `MSApp.pageHandlesAllApplicationActivations(true)` esta para omitir siempre la actualización de la ruta de inicio (volver a cargar la página) y, en su lugar, saltar directamente al desencadenar el `WebUIApplication` evento activado.  Requiere que todas las páginas manejen los eventos de activación por separado.  Al definir este método como `true` , al hacer clic en un evento activado \ (como una notificación \), no se activará la recarga, que es esencial para las aplicaciones de una sola página que deseen evitar la recarga de la página.  |  
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
      **Ejemplo**  
      
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

### suppressSubdownloadCredentialPrompts  

:::row:::
   :::column span="":::
      Controla si una aplicación suprime posibles mensajes de autenticación durante la descarga de recursos.  
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
     
      `suppress` por
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Booleano | El valor true suprime las solicitudes de autenticación potenciales.  El valor false no suprime ninguna solicitud de autenticación potencial del usuario.  |  
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
      
      El `suppressSubdownloadCredentialPrompts` método controla si una aplicación suprime las solicitudes de autenticación potenciales durante la descarga de recursos.  El comportamiento predeterminado es no suprimir las solicitudes de credenciales.  
      
      `suppressSubdownloadCredentialPrompts` está pensado para que lo usen las aplicaciones que pueden cargar un número excesivo de recursos que requieren autenticación, como una aplicación de correo \ (que puede contener un boletín con un número de imágenes en el que cada imagen requiera autenticación \).  
      
      Al suprimir las solicitudes de credenciales, los cuadros de diálogo para autenticar a los servidores no se mostrarán al acceder a los recursos que requieren autenticación, y el recurso no se descargará.  Tenga en cuenta que no `suppressSubdownloadCredentialPrompts` afecta otros indicadores posibles, como la autenticación de proxy o los cuadros de diálogo de solicitud de certificación del cliente, ni afecta a XHR.  
      
      Tenga en cuenta que `suppressSubdownloadCredentialPrompts` afecta a todo el contenido de la aplicación, incluido el contenido hospedado en el `webview` elemento.  
      
      > [!IMPORTANT]
      > Las decisiones de solicitud de credenciales se almacenan en caché.  Por lo tanto, aunque la supresión de las solicitudes de credenciales surtirá efecto inmediatamente, es posible que sea necesario volver a cargar el documento para permitir las solicitudes de credenciales después de suprimirlas.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ejemplo**  
      
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

### terminateApp  


:::row:::
   :::column span="":::
      Finaliza la aplicación actual y genera un informe de error.  
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
      
      `error` por
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Error | Un `Error` objeto que se puede usar para describir el error que ha desencadenado la finalización.  El `Error` objeto debe contener las propiedades Number, Description y stack; no se generará un informe de errores si el objeto no contiene estas propiedades.  |  
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
      
      Si el problema notificado por `terminateApp` se convierte en uno de los cinco principales problemas de la aplicación, se mostrará en la página calidad de la aplicación.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Ejemplo**  
      
      Este ejemplo llama `terminateApp` cuando se encuentra una excepción.  Usa el `Error` objeto proporcionado cuando se detecta una excepción.  
      
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

### Constantes MSApp  

:::row:::
   :::column span="":::
      Valores de prioridad permitidos asociados con `execAsyncAtPriority` ,, `execAtPriority` `getCurrentPriority` y `isTaskScheduldAtPriorityOrHigher` .  
   :::column-end:::
   :::column span="":::
      #### Actual  
      
      `current`  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | Cuando `current` se usa con el método adecuado \ (vea también la sección \), el método usará la prioridad contextual actual al ejecutar la operación solicitada.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### Alto  
      
      `high`  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | Cuando `high` se usa con el método adecuado \ (vea también la sección \), el método usará una prioridad mayor que la normal al ejecutar la operación solicitada y se enviará la operación antes de que se realice cualquier trabajo de prioridad normal existente.  |  
   :::column-end:::
   :::column span="":::
      #### Inactivo  
      
      `idle`  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | Cuando `ideal` se usa con el método adecuado \ (vea también la sección \), el método usará la prioridad inferior a la normal al ejecutar la operación solicitada y se enviará la operación después de cualquier trabajo de prioridad normal existente.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### Normal  
      
      `normal`  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | DOMString | Cuando `normal` se usa con el método adecuado (vea también la sección), el método usará la prioridad normal existente al ejecutar la operación solicitada.  |  
   :::column-end:::
   :::column span="":::
      **Ejemplo**  
      
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
      | IDL | Mshtml. idl |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## MSAppAsyncOperation  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### start  

:::row:::
   :::column span="":::
      Inicia el `MSAppAsyncOperation` .  
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
      | EventHandler | Propiedad para establecer un controlador de eventos finalizado `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` propiedad  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | EventHandler | Propiedad para establecer un controlador de eventos cuando se produce un error `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` propiedad  
      
      | Tipo | Descripción |  
      |:---- |:--- |  
      | Número | Representa el estado de la operación asincrónica dentro de la aplicación de Windows con JavaScript.  Entre los valores se incluyen: `Started[0]` , `Completed[1]` , `Error[2]` .  |  
      
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

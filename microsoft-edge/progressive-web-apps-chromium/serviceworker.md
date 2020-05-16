---
title: Usar trabajadores de servicio para administrar solicitudes de red y notificaciones push
description: Los trabajadores de servicios son trabajadores web que ayudan a mejorar el rendimiento, responder a las diversas condiciones de la red y aumentar la conectividad con la aplicación Web.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicaciones web progresivas, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 9bf573b668ade351716b69965f653e05857c32ec
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659303"
---
# Usar trabajadores de servicio para administrar solicitudes de red y notificaciones push

Los trabajadores de servicios son un tipo especial de trabajo web con la capacidad de interceptar, modificar y responder a todas las solicitudes de red con la `Fetch` API.  Los trabajadores del servicio pueden acceder a la `Cache` API y los almacenes de datos del cliente asincrónicos, como `IndexedDB` , para almacenar los recursos.  

## Registrar un trabajador de servicio  

Al igual que otros trabajadores web, los trabajadores de servicios deben existir en un archivo independiente. Se hace referencia a este archivo al registrar el trabajador del servicio, tal y como se muestra en el siguiente fragmento de código.  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

Los exploradores modernos proporcionan diferentes niveles de compatibilidad para los trabajadores del servicio. Por lo tanto, se recomienda comprobar la existencia del `serviceWorker` objeto antes de ejecutar cualquier código relacionado con el trabajo. En el fragmento de código anterior, un trabajador de servicio se registra con el archivo que se `serviceworker.min.js` encuentra en la raíz del sitio. Asegúrese de que el archivo JavaScript que define el trabajador del servicio existe en el directorio de mayor nivel que desea que administre \ (que se conoce como el ámbito del trabajo de servicio \).  En el fragmento de código anterior, el archivo se almacena en la raíz y el trabajo del servicio administra todas las páginas del dominio. Si el archivo de trabajo del servicio se almacenó en un `js` directorio, el ámbito del trabajador del servicio sería el `js` Directorio y los subdirectorios.  Como práctica recomendada, coloque el archivo de trabajo del servicio en la raíz de su sitio, a menos que necesite reducir el ámbito del trabajador del servicio.  

## El ciclo de vida del trabajo del servicio  

El ciclo de vida de un trabajador de servicio consta de varios pasos, con cada paso que desencadena un evento. Puede Agregar agentes de escucha a estos eventos para ejecutar el código que realiza una acción. La siguiente lista presenta una vista de alto nivel del ciclo de vida y los eventos relacionados de los trabajadores del servicio. 

1. Registrar el trabajador del servicio.  
1.  El explorador descarga el archivo JavaScript, instala el trabajo del servicio y desencadena el `install` evento. Puede usar el `install` evento para prealmacenar cualquier archivo importante y de larga duración, como archivos CSS, archivos JavaScript, imágenes de logotipos, páginas sin conexión, etc. de su sitio Web.  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  El trabajador de servicio está activado, lo que provoca el `activate` evento.  Use este evento para limpiar las memorias caché obsoletas.  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  El trabajo de servicio está listo para ejecutarse cuando se actualiza la página o cuando el usuario se desplaza a una nueva página del sitio. Si desea ejecutar el trabajo de servicio sin esperar, use el `self.skipWaiting()` método durante el `install` evento.  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  El trabajo del servicio se está ejecutando.     
    
## Usar Fetch en trabajadores de servicio  

El evento principal que se usa en un trabajador de servicio es el `fetch` evento.  El `fetch` evento se ejecuta cada vez que el explorador intenta obtener acceso al contenido dentro del ámbito del trabajador del servicio. En el siguiente fragmento de código se muestra cómo agregar un agente de escucha al evento Fetch.  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

Dentro del `fetch` controlador, puede controlar si una solicitud va a la red, se extrae de la caché y así sucesivamente.  Es probable que el método que tome varíe según el tipo de recurso que se solicita, la frecuencia con la que se actualiza y otra lógica empresarial exclusiva de la aplicación.  Estos son algunos ejemplos de lo que puede hacer:  

*   Si está disponible, devuelva una respuesta de la caché, de lo contrario, retroceder para solicitar el recurso a través de la red.  
*   Obtener un recurso de la red, almacenar en caché una copia y devolver la respuesta.
*   Permitir que el usuario especifique una preferencia para guardar los datos. 
*   Proporcione una imagen de marcador de posición para determinadas solicitudes de imágenes.  
*   Generar una respuesta directamente en el trabajo del servicio.  

## Notificaciones push  

Los trabajadores del servicio pueden insertar notificaciones a los usuarios. Las notificaciones push son útiles para pedir a los usuarios que vuelvan a participar con su aplicación después de que haya transcurrido algún tiempo. Para obtener más información, vea [tutorial y demostración de notificaciones push][AzurewebsitesWebpushdemo].  

## Consulte también  

Para obtener más información sobre los trabajos de servicio, consulte la siguiente lista de temas relacionados.  

*   [Realizar PWAs trabajar sin conexión con trabajadores de servicio][MDNPwasMakingOfflineServiceWorkers]  
*   [Cómo hacer que PWAs se pueda comunicar con las notificaciones y la inserción][MDNPwasMakeReengageablesingNotificationsPush]  

<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Notificaciones de inserción en Web |  Demostraciones de Microsoft Edge"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Realizar PWAs trabajar sin conexión con trabajadores del servicio-PWAs | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "Cómo hacer que PWAs vuelva a estar habilitado usando las notificaciones y Push-PWAs | MDN"  

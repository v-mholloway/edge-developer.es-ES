---
title: Usar los trabajadores de servicio para administrar las solicitudes de red y las notificaciones de inserción
description: Los trabajadores de servicio son trabajadores web que ayudan a mejorar el rendimiento, responder a diferentes condiciones de red y aumentar la conectividad con la aplicación web.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicaciones web progresivas, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 314acbbd5a2f423c274f92e815b2be4329ace9b8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399137"
---
# <a name="use-service-workers-to-manage-network-requests-and-push-notifications"></a>Usar los trabajadores de servicio para administrar las solicitudes de red y las notificaciones de inserción

Los trabajadores de servicio son un tipo especial de trabajo web con la capacidad de interceptar, modificar y responder a todas las solicitudes de red mediante la `Fetch` API.  Los trabajadores de servicio pueden tener acceso a la API y a los almacenes de datos asincrónicos del lado cliente, como `Cache` , para almacenar `IndexedDB` recursos.  

## <a name="registering-a-service-worker"></a>Registro de un trabajador de servicio  

Al igual que otros trabajadores web, los trabajadores de servicio deben existir en un archivo independiente. Hace referencia a este archivo al registrar el trabajador de servicio, como se muestra en el siguiente fragmento de código.  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

Los exploradores modernos proporcionan diferentes niveles de compatibilidad para los trabajadores de servicio. Por lo tanto, es una buena práctica probar la existencia del objeto antes de ejecutar cualquier código relacionado con el trabajador `serviceWorker` de servicio. En el fragmento de código anterior, se registra un trabajador de servicio con `serviceworker.min.js` el archivo ubicado en la raíz del sitio. Asegúrese de que el archivo JavaScript que define el trabajador de servicio existe en el directorio de nivel superior que desea que administre \(que se conoce como el ámbito del trabajador de servicio\).  En el fragmento de código anterior, el archivo se almacena en la raíz y el trabajador de servicio administra todas las páginas del dominio. Si el archivo de trabajo de servicio se almacenaba en un directorio, el ámbito del trabajador de servicio `js` sería el directorio y los `js` subdirectorios.  Como procedimiento recomendado, coloque el archivo de trabajo de servicio en la raíz del sitio, a menos que necesite reducir el ámbito del trabajador de servicio.  

## <a name="the-service-worker-lifecycle"></a>Ciclo de vida del trabajador de servicio  

El ciclo de vida de un trabajador de servicio consta de varios pasos, con cada paso desencadenando un evento. Puede agregar agentes de escucha a estos eventos para ejecutar código para realizar una acción. La siguiente lista presenta una vista de alto nivel del ciclo de vida y los eventos relacionados de los trabajadores del servicio. 

1.  Registre el trabajador de servicio.  
1.  El explorador descarga el archivo JavaScript, instala el trabajador de servicio y desencadena el `install` evento. Puede usar el evento para almacenar previamente en caché los archivos importantes y de larga duración, como archivos CSS, archivos JavaScript, imágenes de logotipo, páginas sin conexión, y así sucesivamente desde `install` su sitio web.  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  El trabajador de servicio está activado, lo que desencadena el `activate` evento.  Use este evento para limpiar cachés obsoletas.  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  El trabajador de servicio está listo para ejecutarse cuando se actualiza la página o cuando el usuario navega a una nueva página en el sitio. Si desea ejecutar el trabajador de servicio sin esperar, use el `self.skipWaiting()` método durante el `install` evento.  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  El trabajador de servicio se está ejecutando.     
    
## <a name="using-fetch-in-service-workers"></a>Uso de la recuperación en los trabajadores de servicio  

El evento principal que se usa en un trabajador de servicio es el `fetch` evento.  El `fetch` evento se ejecuta cada vez que el explorador intenta obtener acceso al contenido dentro del ámbito del trabajador de servicio. El siguiente fragmento de código muestra cómo agregar un agente de escucha al evento fetch.  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

Dentro del controlador, puede controlar si una solicitud va `fetch` a la red, extrae de la memoria caché, y así sucesivamente.  El enfoque que tome probablemente varía en función del tipo de recurso que se solicita, la frecuencia con la que se actualiza y otra lógica empresarial única para la aplicación.  Estos son algunos ejemplos de lo que puede hacer:  

*   Si está disponible, devuelve una respuesta de la memoria caché, de lo contrario, reserva para solicitar el recurso a través de la red.  
*   Captura un recurso de la red, almacena en caché una copia y devuelve la respuesta.
*   Permitir que los usuarios especifiquen una preferencia para guardar datos. 
*   Proporcione una imagen de marcador de posición para determinadas solicitudes de imagen.  
*   Genere una respuesta directamente en el trabajador de servicio.  
    
## <a name="push-notifications"></a>Notificaciones de inserción  

Los trabajadores del servicio pueden enviar notificaciones a los usuarios. Las notificaciones de inserción son útiles para pedir a los usuarios que vuelvan a interactuar con la aplicación una vez transcurrido algún tiempo. Para obtener más información, vaya al [tutorial y demostración de notificaciones de inserción.][AzurewebsitesWebpushdemo]  

## <a name="see-also"></a>Consulta también  

Para obtener más información sobre los trabajadores de servicio, vaya a la siguiente lista de temas relacionados.  

*   [Hacer que las PWA funcionen sin conexión con los trabajadores del servicio][MDNPwasMakingOfflineServiceWorkers]  
*   [Cómo hacer que las PWA se vuelvan a activar mediante notificaciones y inserción][MDNPwasMakeReengageablesingNotificationsPush]  
    
<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Notificaciones de inserción web |  Microsoft Edge Demos"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Hacer que las PWA funcionen sin conexión con los trabajadores de servicio: pwas | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "Cómo hacer que las PWA vuelvan a interactuar con notificaciones e inserción: pwas | MDN"  

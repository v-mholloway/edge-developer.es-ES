---
title: Compatibilidad con conectividad de red y sin conexión en aplicaciones web progresivas
description: Aprenda a usar tecnologías de soporte técnico para crear experiencias resistentes para satisfacer diferentes condiciones de red.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicaciones web progresivas, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 6b6031aac10161c16195c83496f8d8b5b842628e
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398080"
---
# <a name="offline-and-network-connectivity-support-in-progressive-web-apps"></a>Compatibilidad con conectividad de red y sin conexión en aplicaciones web progresivas

Durante muchos años, las organizaciones eran reacias a invertir mucho en software basado en web sobre software nativo porque las aplicaciones web dependían de conexiones de red estables. Hoy en día, la plataforma web ofrece ahora opciones sólidas que permiten a los usuarios seguir trabajando, incluso si la conexión de red se vuelve inestable o se desconecta completamente.

## <a name="use-the-caching-to-improve-performance-of-pwas"></a>Usar el almacenamiento en caché para mejorar el rendimiento de los PWA

Con la introducción de [Los trabajadores de servicio,][MDNServiceWorker]la plataforma web agregó la API para proporcionar `Cache` acceso a los recursos almacenados en caché administrados. Esta API basada en Promesa permite a los desarrolladores almacenar y recuperar muchos recursos web( HTML, CSS, JavaScript, imágenes, JSON, entre otros). Normalmente, la API de caché se usa en el contexto de un trabajador de servicio, pero también está disponible en el subproceso principal del `window` objeto.

Un uso común para la API es almacenar previamente en caché los recursos críticos cuando se instala un trabajador de servicio, como se muestra `Cache` en el siguiente fragmento de código.  

```javascript
self.addEventListener( "install", function( event ){
    event.waitUntil(
        caches.open( "static-cache" )
              .then(function( cache ){
            return cache.addAll([
                "/css/main.css",
                "/js/main.js",
                "/img/favicon.png",
                "/offline/"
            ]);
        })
    );
});
```  

Este código, que se ejecuta durante el evento del ciclo de vida del trabajador de servicio, abre una memoria caché denominada y, después, cuando tiene un puntero a la memoria caché, le agrega cuatro recursos mediante `install` `static-cache` el `addAll()` método.  A menudo, el enfoque se combina con la recuperación de caché durante un `fetch` evento   

```javascript
self.addEventListener( "fetch", event => {
    const request = event.request,
                    url = request.url;
    
    // If we are requesting an HTML page.
    if ( request.headers.get("Accept").includes("text/html") ) {
        event.respondWith(
            // Check the cache first to see if the asset exists, and if it does, return the cached asset.
            caches.match( request )
                  .then( cached_result => {
                if ( cached_result ) {
                    return cached_result;
                }
                // If the asset is not in the cache, fallback to a network request for the asset, and proceed to cache the result.
                return fetch( request )
                       .then( response => {
                    const copy = response.clone();
                    // Wait until the response we received is added to the cache.
                    event.waitUntil(
                        caches.open( "pages" )
                              .then( cache => {
                            return cache.put( request, response );
                        });
                    );
                    return response;
                })
                // If the network is unavailable to make a request, pull the offline page out of the cache.
                .catch(() => caches.match( "/offline/" ));
            })
        ); // end respondWith
    } // end if HTML
});
```  

El fragmento de código se ejecuta en el trabajador de servicio siempre que el explorador realiza una `fetch` solicitud para este sitio. Dentro de ese evento, hay una instrucción condicional que se ejecuta si la solicitud es para un archivo HTML. El trabajador de servicio comprueba si el archivo ya existe en cualquier caché \(usando el `match()` método\). Si la solicitud existe en la memoria caché, se devuelve el resultado almacenado en caché. Si no es así, se ejecuta una nueva para ese recurso, se almacena en caché una copia de la respuesta para más adelante y se `fetch` devuelve la respuesta. Si se `fetch` produce un error porque la red no está disponible, la página sin conexión se devuelve de la memoria caché.

Esta sencilla introducción muestra cómo usar el almacenamiento en caché en la aplicación web progresiva (PWA). Cada PWA es diferente y puede usar diferentes estrategias de almacenamiento en caché. El código puede tener un aspecto diferente y puede usar diferentes estrategias de almacenamiento en caché para distintas rutas dentro de la misma aplicación.

## <a name="use-indexeddb-in-your-pwa-to-store-structured-data"></a>Usar IndexedDB en su PWA para almacenar datos estructurados

`IndexedDB` es una API para almacenar datos estructurados. Al igual que la API, también es asincrónica, lo que significa que puede usarla en el subproceso principal o con trabajadores web como `Cache` trabajadores de servicio. Use la API para almacenar una cantidad significativa de datos estructurados en el cliente o datos `IndexedDB` binarios, como objetos multimedia cifrados. Para obtener más información, vaya a [MDN primer on using IndexedDB][MDNIndexeddbApiUsing].

## <a name="understand-storage-options-for-pwas"></a>Comprender las opciones de almacenamiento para las PWA

A veces es posible que deba almacenar pequeñas cantidades de datos para proporcionar una mejor experiencia sin conexión para los usuarios. Si ese es el caso, es posible que encuentre la simplicidad del sistema de par clave-valor del almacenamiento web según sus necesidades.  

> [!IMPORTANT]
> El almacenamiento web es un proceso sincrónico y no está disponible para su uso en subprocesos de trabajo como trabajadores de servicio. El uso intenso puede crear problemas de rendimiento para la aplicación. 


Hay 2 tipos de almacenamiento web: `localStorage` y `sessionStorage` . Cada uno se mantiene como un almacén de datos independiente aislado del dominio que lo creó. `sessionStorage` solo persiste durante la sesión de exploración (por ejemplo, mientras el explorador está abierto, que incluye actualizaciones y restauraciones). `localStorage` persiste hasta que el código, el usuario o el explorador quitan los datos (por ejemplo, cuando hay un almacenamiento limitado disponible). El siguiente fragmento de código muestra cómo usar `localStorage` , que es similar a cómo se `sessionStorage` usa.

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

Este fragmento de código captura metadatos sobre la página actual y los almacena en un objeto JavaScript. A continuación, almacena ese valor como JSON en el uso `localStorage` del método y asigna una clave igual a la dirección URL `setItem()` `window.location` actual. Puede recuperar la información del `localStorage` uso del `getItem()` método. 

El siguiente fragmento de código muestra cómo usar el almacenamiento en caché para enumerar páginas almacenadas en caché y extraer metadatos para realizar una tarea, como crear una `localstorage` lista de vínculos.

```javascript
caches.open( "pages" )
      .then( cache => {
    cache.keys()
         .then( keys => {
        if ( keys.length )
        {
            keys.forEach( insertOfflineLink );
        }
    })
});

function insertOfflineLink( request ) {
    var data = JSON.parse( localStorage.getItem( request.url ) );
    // If data exists and this page is not an offline page, assuming that offline pages have the word offline in the URL.
    if ( data && request.url.indexOf('offline') < 0  )
    {
        // Build a link and insert it into the page.
    }
}
```  

El `insertOfflineLink()` método pasa la dirección URL de la solicitud al método para recuperar los `localStorage.getItem()` metadatos almacenados. Los datos recuperados se comprueban para ver si existen y, si lo hace, se puede realizar una acción en los datos, como crear e insertar el marcado para mostrarlos.

## <a name="test-for-network-connections-in-your-pwa"></a>Probar las conexiones de red en su PWA

Además de almacenar información para uso sin conexión, es útil saber cuándo hay una conexión de red disponible para sincronizar datos o informar a los usuarios de que el estado de la red ha cambiado. Use las siguientes opciones para probar la conectividad de red.

### <a name="navigatoronline"></a>navigator.onLine  

La `navigator.onLine` propiedad es un valor booleano que le permite conocer el estado actual de la red. Si el valor es , el usuario está en línea, de lo `true` contrario, el usuario está sin conexión.

### <a name="online-and-offline-events"></a>Eventos en línea y sin conexión  

Saber si la red está disponible es útil, pero es posible que quieras tomar medidas cuando cambie la conectividad de red. En esta situación, es posible que desee escuchar y tomar medidas en respuesta a los eventos de red. Los eventos están disponibles en `window` los elementos , y como se muestra en el siguiente fragmento de `document` `document.body` código.

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## <a name="see-also"></a>Consulte también  

Para obtener más información sobre cómo administrar escenarios sin conexión, vaya a las páginas siguientes.  

*   [Memoria caché][MDNCache]  
*   [IndexedDB][MDNIndexeddbApi]  
*   [Trabajador de servicio][MDNServiceWorker]  
*   [Almacenamiento web][MDNWebStorageApi]  
*   [navigator.onLine][MDNNavigatoronline]  
*   [Eventos en línea y sin conexión][MDNNavigatoronlineOfflineEvents]  
*   [Solicitud con intención: estrategias de almacenamiento en caché en la era de los PWA][AlistapartRequestIntentCachingStrategiesAgePwas]
    
<!-- links -->  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Caché | MDN"  
[MDNIndexeddbApi]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "Api IndexedDB | MDN"  
[MDNIndexeddbApiUsing]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Uso de IndexDb: api de IndexDB | MDN"  
[MDNServiceWorker]: https://developer.mozilla.org/docs/Web/API/ServiceWorker "ServiceWorker | MDN"  
[MDNWebStorageApi]: https://developer.mozilla.org/docs/Web/API/Web_Storage_API "Api de almacenamiento web | MDN"  
[MDNNavigatoronline]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine "NavigatorOnLine | MDN"  
[MDNNavigatoronlineOfflineEvents]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine/Online_and_offline_events "Eventos en línea y sin conexión: NavigatorOnLine | MDN"  

[AbookapartGoingOffline]: https://abookapart.com/products/going-offline "Going Offline by Jeremy Keith | Un libro aparte"  

[AlistapartRequestIntentCachingStrategiesAgePwas]: https://alistapart.com/article/request-with-intent-caching-strategies-in-the-age-of-pwas "Solicitud con intención: Estrategias de almacenamiento en caché en la era de las PWA de Aaron Gustafson | Una lista aparte"  

---
title: Soporte técnico sin conexión y conectividad de red en aplicaciones web progresivas
description: Aprenda a usar las tecnologías de soporte para crear experiencias resistentes a fin de satisfacer condiciones de red diferentes.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicaciones web progresivas, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 58ffb8e9ae596dec4b99143a3061995a6598ce44
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659310"
---
# Soporte técnico sin conexión y conectividad de red en aplicaciones web progresivas

A lo largo de muchos años, las organizaciones se resisten por invertir intensamente en software basado en el software nativo porque las aplicaciones web dependen de conexiones de red estables. Hoy en día, la plataforma web ahora ofrece sólidas opciones que permiten a los usuarios seguir funcionando, incluso si la conexión de red se vuelve inestable o se desconecta por completo.

## Usar el almacenamiento en caché para mejorar el rendimiento de PWAs

Con la introducción de los [trabajadores del servicio][MDNServiceWorker], la plataforma web agregó la `Cache` API para proporcionar acceso a los recursos administrados almacenados en caché. Esta API basada en promesas permite a los desarrolladores almacenar y recuperar muchos recursos Web (HTML, CSS, JavaScript, imágenes, JSON, etc.). Normalmente, la API de caché se usa dentro del contexto de un trabajo de servicio, pero también está disponible en el subproceso principal del `window` objeto.

Un uso común de la `Cache` API es la Precaché previa de recursos críticos cuando se instala un trabajador de servicio, tal y como se muestra en el siguiente fragmento de código.  

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

Este código, que se ejecuta durante el evento de ciclo de vida del trabajador `install` de servicio, abre una memoria caché con `static-cache` el nombre y, después, cuando tiene un puntero a la caché, agrega cuatro recursos a la misma con el `addAll()` método.  A menudo, el enfoque se acopla con la recuperación de la caché durante un `fetch` evento.   

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

El fragmento de código se ejecuta dentro del trabajo de servicio siempre que el explorador realiza una `fetch` solicitud para este sitio. Dentro de ese evento, hay una instrucción condicional que se ejecuta si la solicitud es para un archivo HTML. El trabajo del servicio comprueba si el archivo ya existe en cualquier caché \ (usando el `match()` método \). Si la solicitud existe en la caché, se devuelve ese resultado almacenado en caché. Si no es así, se ejecuta una nueva `fetch` para ese recurso, una copia de la respuesta se almacena en caché para más tarde y se devuelve la respuesta. Si se `fetch` produce un error porque la red no está disponible, la página sin conexión se devuelve de la caché.

Esta introducción sencilla muestra cómo usar el almacenamiento en caché en la aplicación web progresiva (PWA). Cada PWA es diferente y puede usar estrategias de almacenamiento en caché diferentes. El código puede tener un aspecto diferente y puede usar diferentes estrategias de almacenamiento en caché para diferentes rutas dentro de la misma aplicación.

## Usar IndexedDB en PWA para almacenar datos estructurados

`IndexedDB` es una API para almacenar datos estructurados. Al igual que la `Cache` API, también es asíncrona, lo que significa que puedes usarla en el subproceso principal o en trabajadores de la web, como trabajadores de servicio. Use la `IndexedDB` API para almacenar una cantidad significativa de datos estructurados en el cliente o datos binarios, como objetos multimedia cifrados. Para obtener más información, consulte información [básica sobre el uso de IndexedDB][MDNIndexeddbApiUsing].

## Comprender las opciones de almacenamiento para PWAs

En ocasiones, es posible que necesite almacenar pequeñas cantidades de datos para ofrecer una mejor experiencia sin conexión para los usuarios. En ese caso, es posible que la simplicidad del sistema de pares clave-valor del almacenamiento web se ajuste a sus necesidades.  

> [!IMPORTANT]
> El almacenamiento web es un proceso sincrónico y no está disponible para su uso dentro de subprocesos de trabajo como trabajadores de servicio. Un uso intensivo puede crear problemas de rendimiento para la aplicación. 


Hay dos tipos de almacenamiento web: `localStorage` y `sessionStorage` . Cada uno se mantiene como un almacén de datos independiente aislado al dominio que lo creó. `sessionStorage` solo se conserva durante la duración de la sesión de exploración (por ejemplo, mientras el explorador está abierto, lo que incluye actualizar y restaurar). `localStorage` continúa hasta que el código, el usuario o el explorador quitan los datos (por ejemplo, cuando hay almacenamiento limitado disponible). En el siguiente fragmento de código se muestra cómo usar `localStorage` , que es similar a la forma en que `sessionStorage` se usa.

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

Este fragmento de código toma metadatos sobre la página actual y los almacena en un objeto de JavaScript. A continuación, almacena ese valor como JSON en `localStorage` el `setItem()` método y asigna una clave igual a la `window.location` dirección URL actual. Puede recuperar la información de `localStorage` uso del `getItem()` método. 

El siguiente fragmento de código muestra cómo usar el almacenamiento en caché con `localstorage` para enumerar páginas almacenadas en caché y extraer metadatos para realizar una tarea, como crear una lista de vínculos.

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

El `insertOfflineLink()` método pasa la dirección URL de la solicitud en el `localStorage.getItem()` método para recuperar los metadatos almacenados. Los datos recuperados se comprueban para ver si existe, y si lo hace, se puede llevar a cabo una acción en los datos, como generar e insertar el marcado para mostrarlo.

## Probar las conexiones de red en su PWA

Además de almacenar información para su uso sin conexión, resulta útil saber cuándo está disponible una conexión de red para poder sincronizar los datos o informar a los usuarios de que el estado de la red ha cambiado. Use las siguientes opciones para comprobar la conectividad de red.

### Navigator. onLine  

La `navigator.onLine` propiedad es un valor booleano que le permite conocer el estado actual de la red. Si el valor es `true` , el usuario está conectado, de lo contrario el usuario está desconectado.

### Eventos en línea y sin conexión  

Saber si la red está disponible es útil, pero es posible que desee tomar medidas cuando cambie la conectividad de red. En esta situación, es posible que desee escuchar y tomar medidas en respuesta a eventos de red. Los eventos están disponibles en los `window` `document` elementos, y, `document.body` tal y como se muestra en el siguiente fragmento de código.

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## Consulte también  

Para obtener más información sobre cómo administrar escenarios sin conexión, vea las páginas siguientes.  

*   [Memoria caché][MDNCache]  
*   [IndexedDB][MDNIndexeddbApi]  
*   [Trabajo del servicio][MDNServiceWorker]  
*   [Almacenamiento Web][MDNWebStorageApi]  
*   [Navigator. onLine][MDNNavigatoronline]  
*   [Eventos en línea y sin conexión][MDNNavigatoronlineOfflineEvents]  
*   [Solicitud con intención: estrategias de almacenamiento en caché de edad de PWAs][AlistapartRequestIntentCachingStrategiesAgePwas]

<!-- links -->  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Caché | MDN"  
[MDNIndexeddbApi]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API de IndexedDB | MDN"  
[MDNIndexeddbApiUsing]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Uso de IndexDb-IndexDB API | MDN"  
[MDNServiceWorker]: https://developer.mozilla.org/docs/Web/API/ServiceWorker "ServiceWorker | MDN"  
[MDNWebStorageApi]: https://developer.mozilla.org/docs/Web/API/Web_Storage_API "API de almacenamiento Web | MDN"  
[MDNNavigatoronline]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine "NavigatorOnLine | MDN"  
[MDNNavigatoronlineOfflineEvents]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine/Online_and_offline_events "Eventos en línea y sin conexión-NavigatorOnLine | MDN"  

[AbookapartGoingOffline]: https://abookapart.com/products/going-offline "Trabajando sin conexión por Jeremy Keith | Un libro separado"  

[AlistapartRequestIntentCachingStrategiesAgePwas]: https://alistapart.com/article/request-with-intent-caching-strategies-in-the-age-of-pwas "Solicitud con intención: las estrategias de almacenamiento en caché de Age of PWAs por Aaron Gustafson | Una lista aparte"  

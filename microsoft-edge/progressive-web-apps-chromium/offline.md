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
# <span data-ttu-id="50859-104">Soporte técnico sin conexión y conectividad de red en aplicaciones web progresivas</span><span class="sxs-lookup"><span data-stu-id="50859-104">Offline and network connectivity support in Progressive Web Apps</span></span>

<span data-ttu-id="50859-105">A lo largo de muchos años, las organizaciones se resisten por invertir intensamente en software basado en el software nativo porque las aplicaciones web dependen de conexiones de red estables.</span><span class="sxs-lookup"><span data-stu-id="50859-105">For many years organizations were reluctant to invest heavily in web-based software over native software because web applications depended on stable network connections.</span></span> <span data-ttu-id="50859-106">Hoy en día, la plataforma web ahora ofrece sólidas opciones que permiten a los usuarios seguir funcionando, incluso si la conexión de red se vuelve inestable o se desconecta por completo.</span><span class="sxs-lookup"><span data-stu-id="50859-106">Today, the web platform now offers robust options that enable users to continue working, even if the network connection becomes unstable or goes completely offline.</span></span>

## <span data-ttu-id="50859-107">Usar el almacenamiento en caché para mejorar el rendimiento de PWAs</span><span class="sxs-lookup"><span data-stu-id="50859-107">Use the caching to improve performance of PWAs</span></span>

<span data-ttu-id="50859-108">Con la introducción de los [trabajadores del servicio][MDNServiceWorker], la plataforma web agregó la `Cache` API para proporcionar acceso a los recursos administrados almacenados en caché.</span><span class="sxs-lookup"><span data-stu-id="50859-108">With the introduction of [Service Workers][MDNServiceWorker], the web platform added the `Cache` API to provide access to managed cached resources.</span></span> <span data-ttu-id="50859-109">Esta API basada en promesas permite a los desarrolladores almacenar y recuperar muchos recursos Web (HTML, CSS, JavaScript, imágenes, JSON, etc.).</span><span class="sxs-lookup"><span data-stu-id="50859-109">This Promise-based API allows developers to store and retrieve many web resources—HTML, CSS, JavaScript, images, JSON, and so on.</span></span> <span data-ttu-id="50859-110">Normalmente, la API de caché se usa dentro del contexto de un trabajo de servicio, pero también está disponible en el subproceso principal del `window` objeto.</span><span class="sxs-lookup"><span data-stu-id="50859-110">Usually, the Cache API is used within the context of a Service Worker, but it is also available in the main thread on the `window` object.</span></span>

<span data-ttu-id="50859-111">Un uso común de la `Cache` API es la Precaché previa de recursos críticos cuando se instala un trabajador de servicio, tal y como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="50859-111">One common use for the `Cache` API is to pre-cache critical resources when a Service Worker is installed, as shown in the following code snippet.</span></span>  

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

<span data-ttu-id="50859-112">Este código, que se ejecuta durante el evento de ciclo de vida del trabajador `install` de servicio, abre una memoria caché con `static-cache` el nombre y, después, cuando tiene un puntero a la caché, agrega cuatro recursos a la misma con el `addAll()` método.</span><span class="sxs-lookup"><span data-stu-id="50859-112">This code, which runs during the Service Worker `install` life cycle event, opens a cache named `static-cache` and then, when it has a pointer to the cache, adds four resources to it using the `addAll()` method.</span></span>  <span data-ttu-id="50859-113">A menudo, el enfoque se acopla con la recuperación de la caché durante un `fetch` evento.</span><span class="sxs-lookup"><span data-stu-id="50859-113">Often the approach is coupled with cache retrieval during a `fetch` event</span></span>   

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

<span data-ttu-id="50859-114">El fragmento de código se ejecuta dentro del trabajo de servicio siempre que el explorador realiza una `fetch` solicitud para este sitio.</span><span class="sxs-lookup"><span data-stu-id="50859-114">The code snippet runs within the Service Worker whenever the browser makes a `fetch` request for this site.</span></span> <span data-ttu-id="50859-115">Dentro de ese evento, hay una instrucción condicional que se ejecuta si la solicitud es para un archivo HTML.</span><span class="sxs-lookup"><span data-stu-id="50859-115">Within that event, there is a conditional statement that runs if the request is for an HTML file.</span></span> <span data-ttu-id="50859-116">El trabajo del servicio comprueba si el archivo ya existe en cualquier caché \ (usando el `match()` método \).</span><span class="sxs-lookup"><span data-stu-id="50859-116">The Service Worker checks to see if the file already exists in any cache \(using the `match()` method\).</span></span> <span data-ttu-id="50859-117">Si la solicitud existe en la caché, se devuelve ese resultado almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="50859-117">If the request exists in the cache, that cached result is returned.</span></span> <span data-ttu-id="50859-118">Si no es así, se ejecuta una nueva `fetch` para ese recurso, una copia de la respuesta se almacena en caché para más tarde y se devuelve la respuesta.</span><span class="sxs-lookup"><span data-stu-id="50859-118">If not, a new `fetch` for that resource is run, a copy of the response is cached for later, and the response is returned.</span></span> <span data-ttu-id="50859-119">Si se `fetch` produce un error porque la red no está disponible, la página sin conexión se devuelve de la caché.</span><span class="sxs-lookup"><span data-stu-id="50859-119">If the `fetch` fails because the network is unavailable, the offline page is returned from the cache.</span></span>

<span data-ttu-id="50859-120">Esta introducción sencilla muestra cómo usar el almacenamiento en caché en la aplicación web progresiva (PWA).</span><span class="sxs-lookup"><span data-stu-id="50859-120">This simple introduction shows how to use caching in your progressive web app (PWA).</span></span> <span data-ttu-id="50859-121">Cada PWA es diferente y puede usar estrategias de almacenamiento en caché diferentes.</span><span class="sxs-lookup"><span data-stu-id="50859-121">Each PWA is different and may use different caching strategies.</span></span> <span data-ttu-id="50859-122">El código puede tener un aspecto diferente y puede usar diferentes estrategias de almacenamiento en caché para diferentes rutas dentro de la misma aplicación.</span><span class="sxs-lookup"><span data-stu-id="50859-122">Your code may look different, and you may use different caching strategies for different routes within the same application.</span></span>

## <span data-ttu-id="50859-123">Usar IndexedDB en PWA para almacenar datos estructurados</span><span class="sxs-lookup"><span data-stu-id="50859-123">Use IndexedDB in your PWA to store structured data</span></span>

`IndexedDB` <span data-ttu-id="50859-124">es una API para almacenar datos estructurados.</span><span class="sxs-lookup"><span data-stu-id="50859-124">is an API for storing structured data.</span></span> <span data-ttu-id="50859-125">Al igual que la `Cache` API, también es asíncrona, lo que significa que puedes usarla en el subproceso principal o en trabajadores de la web, como trabajadores de servicio.</span><span class="sxs-lookup"><span data-stu-id="50859-125">Similar to the `Cache` API, it is also asynchronous, which means you may use it in the main thread or with Web Workers such as Service Workers.</span></span> <span data-ttu-id="50859-126">Use la `IndexedDB` API para almacenar una cantidad significativa de datos estructurados en el cliente o datos binarios, como objetos multimedia cifrados.</span><span class="sxs-lookup"><span data-stu-id="50859-126">Use the `IndexedDB` API for storing a significant amount of structured data on the client, or binary data, such as encrypted media objects.</span></span> <span data-ttu-id="50859-127">Para obtener más información, consulte información [básica sobre el uso de IndexedDB][MDNIndexeddbApiUsing].</span><span class="sxs-lookup"><span data-stu-id="50859-127">For more information, see [MDN primer on using IndexedDB][MDNIndexeddbApiUsing].</span></span>

## <span data-ttu-id="50859-128">Comprender las opciones de almacenamiento para PWAs</span><span class="sxs-lookup"><span data-stu-id="50859-128">Understand storage options for PWAs</span></span>

<span data-ttu-id="50859-129">En ocasiones, es posible que necesite almacenar pequeñas cantidades de datos para ofrecer una mejor experiencia sin conexión para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="50859-129">Sometimes you may need to store small amounts of data in order to provide a better offline experience for your users.</span></span> <span data-ttu-id="50859-130">En ese caso, es posible que la simplicidad del sistema de pares clave-valor del almacenamiento web se ajuste a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="50859-130">If that is the case, you may find the simplicity of the key-value pair system of web storage meets your needs.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="50859-131">El almacenamiento web es un proceso sincrónico y no está disponible para su uso dentro de subprocesos de trabajo como trabajadores de servicio.</span><span class="sxs-lookup"><span data-stu-id="50859-131">Web Storage is a synchronous process and is not available for use within worker threads such as Service Workers.</span></span> <span data-ttu-id="50859-132">Un uso intensivo puede crear problemas de rendimiento para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="50859-132">Heavy usage may create performance issues for your application.</span></span> 


<span data-ttu-id="50859-133">Hay dos tipos de almacenamiento web: `localStorage` y `sessionStorage` .</span><span class="sxs-lookup"><span data-stu-id="50859-133">There are 2 types of Web Storage: `localStorage` and `sessionStorage`.</span></span> <span data-ttu-id="50859-134">Cada uno se mantiene como un almacén de datos independiente aislado al dominio que lo creó.</span><span class="sxs-lookup"><span data-stu-id="50859-134">Each is maintained as a separate data store isolated to the domain that created it.</span></span> `sessionStorage` <span data-ttu-id="50859-135">solo se conserva durante la duración de la sesión de exploración (por ejemplo, mientras el explorador está abierto, lo que incluye actualizar y restaurar).</span><span class="sxs-lookup"><span data-stu-id="50859-135">persists only for the duration of the browsing session (for example, while the browser is open, which includes refresh and restores).</span></span> `localStorage` <span data-ttu-id="50859-136">continúa hasta que el código, el usuario o el explorador quitan los datos (por ejemplo, cuando hay almacenamiento limitado disponible).</span><span class="sxs-lookup"><span data-stu-id="50859-136">persists until the data is removed by the code, the user, or the browser (for example, when there is limited storage available).</span></span> <span data-ttu-id="50859-137">En el siguiente fragmento de código se muestra cómo usar `localStorage` , que es similar a la forma en que `sessionStorage` se usa.</span><span class="sxs-lookup"><span data-stu-id="50859-137">The following code snippet shows how to use `localStorage`, which is similar to how `sessionStorage` is used.</span></span>

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

<span data-ttu-id="50859-138">Este fragmento de código toma metadatos sobre la página actual y los almacena en un objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="50859-138">This code snippet grabs metadata about the current page and stores it in a JavaScript object.</span></span> <span data-ttu-id="50859-139">A continuación, almacena ese valor como JSON en `localStorage` el `setItem()` método y asigna una clave igual a la `window.location` dirección URL actual.</span><span class="sxs-lookup"><span data-stu-id="50859-139">Then it stores that value as JSON in `localStorage` using the `setItem()` method, and assigns a key equal to the current `window.location` URL.</span></span> <span data-ttu-id="50859-140">Puede recuperar la información de `localStorage` uso del `getItem()` método.</span><span class="sxs-lookup"><span data-stu-id="50859-140">You may retrieve the information from `localStorage` using the `getItem()` method.</span></span> 

<span data-ttu-id="50859-141">El siguiente fragmento de código muestra cómo usar el almacenamiento en caché con `localstorage` para enumerar páginas almacenadas en caché y extraer metadatos para realizar una tarea, como crear una lista de vínculos.</span><span class="sxs-lookup"><span data-stu-id="50859-141">The following code snippet shows how to use caching with `localstorage` to enumerate cached pages and extract metadata to perform a task, such as building a list of links.</span></span>

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

<span data-ttu-id="50859-142">El `insertOfflineLink()` método pasa la dirección URL de la solicitud en el `localStorage.getItem()` método para recuperar los metadatos almacenados.</span><span class="sxs-lookup"><span data-stu-id="50859-142">The `insertOfflineLink()` method passes the URL of the request into the `localStorage.getItem()` method to retrieve any stored metadata.</span></span> <span data-ttu-id="50859-143">Los datos recuperados se comprueban para ver si existe, y si lo hace, se puede llevar a cabo una acción en los datos, como generar e insertar el marcado para mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="50859-143">The retrieved data is checked to see if it exists, and if it does, an action can be taken on the data, such as building and inserting the markup to display it.</span></span>

## <span data-ttu-id="50859-144">Probar las conexiones de red en su PWA</span><span class="sxs-lookup"><span data-stu-id="50859-144">Test for network connections in your PWA</span></span>

<span data-ttu-id="50859-145">Además de almacenar información para su uso sin conexión, resulta útil saber cuándo está disponible una conexión de red para poder sincronizar los datos o informar a los usuarios de que el estado de la red ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="50859-145">In addition to storing information for offline use, it is helpful to know when a network connection is available in order to synchronize data or inform users that the network status has changed.</span></span> <span data-ttu-id="50859-146">Use las siguientes opciones para comprobar la conectividad de red.</span><span class="sxs-lookup"><span data-stu-id="50859-146">Use the following options to test for network connectivity.</span></span>

### <span data-ttu-id="50859-147">Navigator. onLine</span><span class="sxs-lookup"><span data-stu-id="50859-147">navigator.onLine</span></span>  

<span data-ttu-id="50859-148">La `navigator.onLine` propiedad es un valor booleano que le permite conocer el estado actual de la red.</span><span class="sxs-lookup"><span data-stu-id="50859-148">The `navigator.onLine` property is a boolean that lets you know the current status of the network.</span></span> <span data-ttu-id="50859-149">Si el valor es `true` , el usuario está conectado, de lo contrario el usuario está desconectado.</span><span class="sxs-lookup"><span data-stu-id="50859-149">If the value is `true`, the user is online, otherwise the user is offline.</span></span>

### <span data-ttu-id="50859-150">Eventos en línea y sin conexión</span><span class="sxs-lookup"><span data-stu-id="50859-150">Online and Offline Events</span></span>  

<span data-ttu-id="50859-151">Saber si la red está disponible es útil, pero es posible que desee tomar medidas cuando cambie la conectividad de red.</span><span class="sxs-lookup"><span data-stu-id="50859-151">Knowing whether the network is available is helpful, but you may want to take action  when your network connectivity changes.</span></span> <span data-ttu-id="50859-152">En esta situación, es posible que desee escuchar y tomar medidas en respuesta a eventos de red.</span><span class="sxs-lookup"><span data-stu-id="50859-152">In this situation, you may want to listen and take action in response to network events.</span></span> <span data-ttu-id="50859-153">Los eventos están disponibles en los `window` `document` elementos, y, `document.body` tal y como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="50859-153">The events are available on the `window`, `document`, and `document.body` elements as displayed in the following code snippet.</span></span>

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## <span data-ttu-id="50859-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="50859-154">See also</span></span>  

<span data-ttu-id="50859-155">Para obtener más información sobre cómo administrar escenarios sin conexión, vea las páginas siguientes.</span><span class="sxs-lookup"><span data-stu-id="50859-155">To learn more about managing offline scenarios, see the following pages.</span></span>  

*   [<span data-ttu-id="50859-156">Memoria caché</span><span class="sxs-lookup"><span data-stu-id="50859-156">Cache</span></span>][MDNCache]  
*   [<span data-ttu-id="50859-157">IndexedDB</span><span class="sxs-lookup"><span data-stu-id="50859-157">IndexedDB</span></span>][MDNIndexeddbApi]  
*   [<span data-ttu-id="50859-158">Trabajo del servicio</span><span class="sxs-lookup"><span data-stu-id="50859-158">Service Worker</span></span>][MDNServiceWorker]  
*   [<span data-ttu-id="50859-159">Almacenamiento Web</span><span class="sxs-lookup"><span data-stu-id="50859-159">Web Storage</span></span>][MDNWebStorageApi]  
*   [<span data-ttu-id="50859-160">Navigator. onLine</span><span class="sxs-lookup"><span data-stu-id="50859-160">navigator.onLine</span></span>][MDNNavigatoronline]  
*   [<span data-ttu-id="50859-161">Eventos en línea y sin conexión</span><span class="sxs-lookup"><span data-stu-id="50859-161">Online and Offline Events</span></span>][MDNNavigatoronlineOfflineEvents]  
*   [<span data-ttu-id="50859-162">Solicitud con intención: estrategias de almacenamiento en caché de edad de PWAs</span><span class="sxs-lookup"><span data-stu-id="50859-162">Request with Intent: Caching Strategies in the Age of PWAs</span></span>][AlistapartRequestIntentCachingStrategiesAgePwas]

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

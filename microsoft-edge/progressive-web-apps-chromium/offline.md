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
# <a name="offline-and-network-connectivity-support-in-progressive-web-apps"></a><span data-ttu-id="288d5-104">Compatibilidad con conectividad de red y sin conexión en aplicaciones web progresivas</span><span class="sxs-lookup"><span data-stu-id="288d5-104">Offline and network connectivity support in Progressive Web Apps</span></span>

<span data-ttu-id="288d5-105">Durante muchos años, las organizaciones eran reacias a invertir mucho en software basado en web sobre software nativo porque las aplicaciones web dependían de conexiones de red estables.</span><span class="sxs-lookup"><span data-stu-id="288d5-105">For many years organizations were reluctant to invest heavily in web-based software over native software because web applications depended on stable network connections.</span></span> <span data-ttu-id="288d5-106">Hoy en día, la plataforma web ofrece ahora opciones sólidas que permiten a los usuarios seguir trabajando, incluso si la conexión de red se vuelve inestable o se desconecta completamente.</span><span class="sxs-lookup"><span data-stu-id="288d5-106">Today, the web platform now offers robust options that enable users to continue working, even if the network connection becomes unstable or goes completely offline.</span></span>

## <a name="use-the-caching-to-improve-performance-of-pwas"></a><span data-ttu-id="288d5-107">Usar el almacenamiento en caché para mejorar el rendimiento de los PWA</span><span class="sxs-lookup"><span data-stu-id="288d5-107">Use the caching to improve performance of PWAs</span></span>

<span data-ttu-id="288d5-108">Con la introducción de [Los trabajadores de servicio,][MDNServiceWorker]la plataforma web agregó la API para proporcionar `Cache` acceso a los recursos almacenados en caché administrados.</span><span class="sxs-lookup"><span data-stu-id="288d5-108">With the introduction of [Service Workers][MDNServiceWorker], the web platform added the `Cache` API to provide access to managed cached resources.</span></span> <span data-ttu-id="288d5-109">Esta API basada en Promesa permite a los desarrolladores almacenar y recuperar muchos recursos web( HTML, CSS, JavaScript, imágenes, JSON, entre otros).</span><span class="sxs-lookup"><span data-stu-id="288d5-109">This Promise-based API allows developers to store and retrieve many web resources—HTML, CSS, JavaScript, images, JSON, and so on.</span></span> <span data-ttu-id="288d5-110">Normalmente, la API de caché se usa en el contexto de un trabajador de servicio, pero también está disponible en el subproceso principal del `window` objeto.</span><span class="sxs-lookup"><span data-stu-id="288d5-110">Usually, the Cache API is used within the context of a Service Worker, but it is also available in the main thread on the `window` object.</span></span>

<span data-ttu-id="288d5-111">Un uso común para la API es almacenar previamente en caché los recursos críticos cuando se instala un trabajador de servicio, como se muestra `Cache` en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="288d5-111">One common use for the `Cache` API is to pre-cache critical resources when a Service Worker is installed, as shown in the following code snippet.</span></span>  

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

<span data-ttu-id="288d5-112">Este código, que se ejecuta durante el evento del ciclo de vida del trabajador de servicio, abre una memoria caché denominada y, después, cuando tiene un puntero a la memoria caché, le agrega cuatro recursos mediante `install` `static-cache` el `addAll()` método.</span><span class="sxs-lookup"><span data-stu-id="288d5-112">This code, which runs during the Service Worker `install` life cycle event, opens a cache named `static-cache` and then, when it has a pointer to the cache, adds four resources to it using the `addAll()` method.</span></span>  <span data-ttu-id="288d5-113">A menudo, el enfoque se combina con la recuperación de caché durante un `fetch` evento</span><span class="sxs-lookup"><span data-stu-id="288d5-113">Often the approach is coupled with cache retrieval during a `fetch` event</span></span>   

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

<span data-ttu-id="288d5-114">El fragmento de código se ejecuta en el trabajador de servicio siempre que el explorador realiza una `fetch` solicitud para este sitio.</span><span class="sxs-lookup"><span data-stu-id="288d5-114">The code snippet runs within the Service Worker whenever the browser makes a `fetch` request for this site.</span></span> <span data-ttu-id="288d5-115">Dentro de ese evento, hay una instrucción condicional que se ejecuta si la solicitud es para un archivo HTML.</span><span class="sxs-lookup"><span data-stu-id="288d5-115">Within that event, there is a conditional statement that runs if the request is for an HTML file.</span></span> <span data-ttu-id="288d5-116">El trabajador de servicio comprueba si el archivo ya existe en cualquier caché \(usando el `match()` método\).</span><span class="sxs-lookup"><span data-stu-id="288d5-116">The Service Worker checks to see if the file already exists in any cache \(using the `match()` method\).</span></span> <span data-ttu-id="288d5-117">Si la solicitud existe en la memoria caché, se devuelve el resultado almacenado en caché.</span><span class="sxs-lookup"><span data-stu-id="288d5-117">If the request exists in the cache, that cached result is returned.</span></span> <span data-ttu-id="288d5-118">Si no es así, se ejecuta una nueva para ese recurso, se almacena en caché una copia de la respuesta para más adelante y se `fetch` devuelve la respuesta.</span><span class="sxs-lookup"><span data-stu-id="288d5-118">If not, a new `fetch` for that resource is run, a copy of the response is cached for later, and the response is returned.</span></span> <span data-ttu-id="288d5-119">Si se `fetch` produce un error porque la red no está disponible, la página sin conexión se devuelve de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="288d5-119">If the `fetch` fails because the network is unavailable, the offline page is returned from the cache.</span></span>

<span data-ttu-id="288d5-120">Esta sencilla introducción muestra cómo usar el almacenamiento en caché en la aplicación web progresiva (PWA).</span><span class="sxs-lookup"><span data-stu-id="288d5-120">This simple introduction shows how to use caching in your progressive web app (PWA).</span></span> <span data-ttu-id="288d5-121">Cada PWA es diferente y puede usar diferentes estrategias de almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="288d5-121">Each PWA is different and may use different caching strategies.</span></span> <span data-ttu-id="288d5-122">El código puede tener un aspecto diferente y puede usar diferentes estrategias de almacenamiento en caché para distintas rutas dentro de la misma aplicación.</span><span class="sxs-lookup"><span data-stu-id="288d5-122">Your code may look different, and you may use different caching strategies for different routes within the same application.</span></span>

## <a name="use-indexeddb-in-your-pwa-to-store-structured-data"></a><span data-ttu-id="288d5-123">Usar IndexedDB en su PWA para almacenar datos estructurados</span><span class="sxs-lookup"><span data-stu-id="288d5-123">Use IndexedDB in your PWA to store structured data</span></span>

`IndexedDB` <span data-ttu-id="288d5-124">es una API para almacenar datos estructurados.</span><span class="sxs-lookup"><span data-stu-id="288d5-124">is an API for storing structured data.</span></span> <span data-ttu-id="288d5-125">Al igual que la API, también es asincrónica, lo que significa que puede usarla en el subproceso principal o con trabajadores web como `Cache` trabajadores de servicio.</span><span class="sxs-lookup"><span data-stu-id="288d5-125">Similar to the `Cache` API, it is also asynchronous, which means you may use it in the main thread or with Web Workers such as Service Workers.</span></span> <span data-ttu-id="288d5-126">Use la API para almacenar una cantidad significativa de datos estructurados en el cliente o datos `IndexedDB` binarios, como objetos multimedia cifrados.</span><span class="sxs-lookup"><span data-stu-id="288d5-126">Use the `IndexedDB` API for storing a significant amount of structured data on the client, or binary data, such as encrypted media objects.</span></span> <span data-ttu-id="288d5-127">Para obtener más información, vaya a [MDN primer on using IndexedDB][MDNIndexeddbApiUsing].</span><span class="sxs-lookup"><span data-stu-id="288d5-127">For more information, navigate to [MDN primer on using IndexedDB][MDNIndexeddbApiUsing].</span></span>

## <a name="understand-storage-options-for-pwas"></a><span data-ttu-id="288d5-128">Comprender las opciones de almacenamiento para las PWA</span><span class="sxs-lookup"><span data-stu-id="288d5-128">Understand storage options for PWAs</span></span>

<span data-ttu-id="288d5-129">A veces es posible que deba almacenar pequeñas cantidades de datos para proporcionar una mejor experiencia sin conexión para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="288d5-129">Sometimes you may need to store small amounts of data in order to provide a better offline experience for your users.</span></span> <span data-ttu-id="288d5-130">Si ese es el caso, es posible que encuentre la simplicidad del sistema de par clave-valor del almacenamiento web según sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="288d5-130">If that is the case, you may find the simplicity of the key-value pair system of web storage meets your needs.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="288d5-131">El almacenamiento web es un proceso sincrónico y no está disponible para su uso en subprocesos de trabajo como trabajadores de servicio.</span><span class="sxs-lookup"><span data-stu-id="288d5-131">Web Storage is a synchronous process and is not available for use within worker threads such as Service Workers.</span></span> <span data-ttu-id="288d5-132">El uso intenso puede crear problemas de rendimiento para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="288d5-132">Heavy usage may create performance issues for your application.</span></span> 


<span data-ttu-id="288d5-133">Hay 2 tipos de almacenamiento web: `localStorage` y `sessionStorage` .</span><span class="sxs-lookup"><span data-stu-id="288d5-133">There are 2 types of Web Storage: `localStorage` and `sessionStorage`.</span></span> <span data-ttu-id="288d5-134">Cada uno se mantiene como un almacén de datos independiente aislado del dominio que lo creó.</span><span class="sxs-lookup"><span data-stu-id="288d5-134">Each is maintained as a separate data store isolated to the domain that created it.</span></span> `sessionStorage` <span data-ttu-id="288d5-135">solo persiste durante la sesión de exploración (por ejemplo, mientras el explorador está abierto, que incluye actualizaciones y restauraciones).</span><span class="sxs-lookup"><span data-stu-id="288d5-135">persists only for the duration of the browsing session (for example, while the browser is open, which includes refresh and restores).</span></span> `localStorage` <span data-ttu-id="288d5-136">persiste hasta que el código, el usuario o el explorador quitan los datos (por ejemplo, cuando hay un almacenamiento limitado disponible).</span><span class="sxs-lookup"><span data-stu-id="288d5-136">persists until the data is removed by the code, the user, or the browser (for example, when there is limited storage available).</span></span> <span data-ttu-id="288d5-137">El siguiente fragmento de código muestra cómo usar `localStorage` , que es similar a cómo se `sessionStorage` usa.</span><span class="sxs-lookup"><span data-stu-id="288d5-137">The following code snippet shows how to use `localStorage`, which is similar to how `sessionStorage` is used.</span></span>

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

<span data-ttu-id="288d5-138">Este fragmento de código captura metadatos sobre la página actual y los almacena en un objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="288d5-138">This code snippet grabs metadata about the current page and stores it in a JavaScript object.</span></span> <span data-ttu-id="288d5-139">A continuación, almacena ese valor como JSON en el uso `localStorage` del método y asigna una clave igual a la dirección URL `setItem()` `window.location` actual.</span><span class="sxs-lookup"><span data-stu-id="288d5-139">Then it stores that value as JSON in `localStorage` using the `setItem()` method, and assigns a key equal to the current `window.location` URL.</span></span> <span data-ttu-id="288d5-140">Puede recuperar la información del `localStorage` uso del `getItem()` método.</span><span class="sxs-lookup"><span data-stu-id="288d5-140">You may retrieve the information from `localStorage` using the `getItem()` method.</span></span> 

<span data-ttu-id="288d5-141">El siguiente fragmento de código muestra cómo usar el almacenamiento en caché para enumerar páginas almacenadas en caché y extraer metadatos para realizar una tarea, como crear una `localstorage` lista de vínculos.</span><span class="sxs-lookup"><span data-stu-id="288d5-141">The following code snippet shows how to use caching with `localstorage` to enumerate cached pages and extract metadata to perform a task, such as building a list of links.</span></span>

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

<span data-ttu-id="288d5-142">El `insertOfflineLink()` método pasa la dirección URL de la solicitud al método para recuperar los `localStorage.getItem()` metadatos almacenados.</span><span class="sxs-lookup"><span data-stu-id="288d5-142">The `insertOfflineLink()` method passes the URL of the request into the `localStorage.getItem()` method to retrieve any stored metadata.</span></span> <span data-ttu-id="288d5-143">Los datos recuperados se comprueban para ver si existen y, si lo hace, se puede realizar una acción en los datos, como crear e insertar el marcado para mostrarlos.</span><span class="sxs-lookup"><span data-stu-id="288d5-143">The retrieved data is checked to see if it exists, and if it does, an action can be taken on the data, such as building and inserting the markup to display it.</span></span>

## <a name="test-for-network-connections-in-your-pwa"></a><span data-ttu-id="288d5-144">Probar las conexiones de red en su PWA</span><span class="sxs-lookup"><span data-stu-id="288d5-144">Test for network connections in your PWA</span></span>

<span data-ttu-id="288d5-145">Además de almacenar información para uso sin conexión, es útil saber cuándo hay una conexión de red disponible para sincronizar datos o informar a los usuarios de que el estado de la red ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="288d5-145">In addition to storing information for offline use, it is helpful to know when a network connection is available in order to synchronize data or inform users that the network status has changed.</span></span> <span data-ttu-id="288d5-146">Use las siguientes opciones para probar la conectividad de red.</span><span class="sxs-lookup"><span data-stu-id="288d5-146">Use the following options to test for network connectivity.</span></span>

### <a name="navigatoronline"></a><span data-ttu-id="288d5-147">navigator.onLine</span><span class="sxs-lookup"><span data-stu-id="288d5-147">navigator.onLine</span></span>  

<span data-ttu-id="288d5-148">La `navigator.onLine` propiedad es un valor booleano que le permite conocer el estado actual de la red.</span><span class="sxs-lookup"><span data-stu-id="288d5-148">The `navigator.onLine` property is a boolean that lets you know the current status of the network.</span></span> <span data-ttu-id="288d5-149">Si el valor es , el usuario está en línea, de lo `true` contrario, el usuario está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="288d5-149">If the value is `true`, the user is online, otherwise the user is offline.</span></span>

### <a name="online-and-offline-events"></a><span data-ttu-id="288d5-150">Eventos en línea y sin conexión</span><span class="sxs-lookup"><span data-stu-id="288d5-150">Online and Offline Events</span></span>  

<span data-ttu-id="288d5-151">Saber si la red está disponible es útil, pero es posible que quieras tomar medidas cuando cambie la conectividad de red.</span><span class="sxs-lookup"><span data-stu-id="288d5-151">Knowing whether the network is available is helpful, but you may want to take action  when your network connectivity changes.</span></span> <span data-ttu-id="288d5-152">En esta situación, es posible que desee escuchar y tomar medidas en respuesta a los eventos de red.</span><span class="sxs-lookup"><span data-stu-id="288d5-152">In this situation, you may want to listen and take action in response to network events.</span></span> <span data-ttu-id="288d5-153">Los eventos están disponibles en `window` los elementos , y como se muestra en el siguiente fragmento de `document` `document.body` código.</span><span class="sxs-lookup"><span data-stu-id="288d5-153">The events are available on the `window`, `document`, and `document.body` elements as displayed in the following code snippet.</span></span>

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## <a name="see-also"></a><span data-ttu-id="288d5-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="288d5-154">See also</span></span>  

<span data-ttu-id="288d5-155">Para obtener más información sobre cómo administrar escenarios sin conexión, vaya a las páginas siguientes.</span><span class="sxs-lookup"><span data-stu-id="288d5-155">To learn more about managing offline scenarios, navigate to the following pages.</span></span>  

*   [<span data-ttu-id="288d5-156">Memoria caché</span><span class="sxs-lookup"><span data-stu-id="288d5-156">Cache</span></span>][MDNCache]  
*   [<span data-ttu-id="288d5-157">IndexedDB</span><span class="sxs-lookup"><span data-stu-id="288d5-157">IndexedDB</span></span>][MDNIndexeddbApi]  
*   [<span data-ttu-id="288d5-158">Trabajador de servicio</span><span class="sxs-lookup"><span data-stu-id="288d5-158">Service Worker</span></span>][MDNServiceWorker]  
*   [<span data-ttu-id="288d5-159">Almacenamiento web</span><span class="sxs-lookup"><span data-stu-id="288d5-159">Web Storage</span></span>][MDNWebStorageApi]  
*   [<span data-ttu-id="288d5-160">navigator.onLine</span><span class="sxs-lookup"><span data-stu-id="288d5-160">navigator.onLine</span></span>][MDNNavigatoronline]  
*   [<span data-ttu-id="288d5-161">Eventos en línea y sin conexión</span><span class="sxs-lookup"><span data-stu-id="288d5-161">Online and Offline Events</span></span>][MDNNavigatoronlineOfflineEvents]  
*   [<span data-ttu-id="288d5-162">Solicitud con intención: estrategias de almacenamiento en caché en la era de los PWA</span><span class="sxs-lookup"><span data-stu-id="288d5-162">Request with Intent: Caching Strategies in the Age of PWAs</span></span>][AlistapartRequestIntentCachingStrategiesAgePwas]
    
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

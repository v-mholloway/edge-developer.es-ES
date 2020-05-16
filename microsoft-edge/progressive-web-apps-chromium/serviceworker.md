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
# <span data-ttu-id="3a68a-104">Usar trabajadores de servicio para administrar solicitudes de red y notificaciones push</span><span class="sxs-lookup"><span data-stu-id="3a68a-104">Use Service Workers to manage network requests and push notifications</span></span>

<span data-ttu-id="3a68a-105">Los trabajadores de servicios son un tipo especial de trabajo web con la capacidad de interceptar, modificar y responder a todas las solicitudes de red con la `Fetch` API.</span><span class="sxs-lookup"><span data-stu-id="3a68a-105">Service Workers are a special type of Web Worker with the ability to intercept, modify, and respond to all network requests using the `Fetch` API.</span></span>  <span data-ttu-id="3a68a-106">Los trabajadores del servicio pueden acceder a la `Cache` API y los almacenes de datos del cliente asincrónicos, como `IndexedDB` , para almacenar los recursos.</span><span class="sxs-lookup"><span data-stu-id="3a68a-106">Service Workers can access the `Cache` API, and asynchronous client-side data stores, such as `IndexedDB`, to store resources.</span></span>  

## <span data-ttu-id="3a68a-107">Registrar un trabajador de servicio</span><span class="sxs-lookup"><span data-stu-id="3a68a-107">Registering a Service Worker</span></span>  

<span data-ttu-id="3a68a-108">Al igual que otros trabajadores web, los trabajadores de servicios deben existir en un archivo independiente.</span><span class="sxs-lookup"><span data-stu-id="3a68a-108">Similar to other Web Workers, Service Workers must exist in a separate file.</span></span> <span data-ttu-id="3a68a-109">Se hace referencia a este archivo al registrar el trabajador del servicio, tal y como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="3a68a-109">You reference this file when registering the Service Worker, as shown in the following code snippet.</span></span>  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

<span data-ttu-id="3a68a-110">Los exploradores modernos proporcionan diferentes niveles de compatibilidad para los trabajadores del servicio.</span><span class="sxs-lookup"><span data-stu-id="3a68a-110">Modern browsers provide different levels of support for Service Workers.</span></span> <span data-ttu-id="3a68a-111">Por lo tanto, se recomienda comprobar la existencia del `serviceWorker` objeto antes de ejecutar cualquier código relacionado con el trabajo.</span><span class="sxs-lookup"><span data-stu-id="3a68a-111">As such, it is a good practice to test for the existence of the `serviceWorker` object before running any Service Worker-related code.</span></span> <span data-ttu-id="3a68a-112">En el fragmento de código anterior, un trabajador de servicio se registra con el archivo que se `serviceworker.min.js` encuentra en la raíz del sitio.</span><span class="sxs-lookup"><span data-stu-id="3a68a-112">In the above code snippet, a Service Worker is registered using the `serviceworker.min.js` file located at the root of the site.</span></span> <span data-ttu-id="3a68a-113">Asegúrese de que el archivo JavaScript que define el trabajador del servicio existe en el directorio de mayor nivel que desea que administre \ (que se conoce como el ámbito del trabajo de servicio \).</span><span class="sxs-lookup"><span data-stu-id="3a68a-113">Ensure that the JavaScript file that defines your Service Worker exists in the highest-level directory that you want it to manage \(which is referred to as the scope of the Service Worker\).</span></span>  <span data-ttu-id="3a68a-114">En el fragmento de código anterior, el archivo se almacena en la raíz y el trabajo del servicio administra todas las páginas del dominio.</span><span class="sxs-lookup"><span data-stu-id="3a68a-114">In the above code snippet, the file is stored in the root, and the Service Worker manages all pages in the domain.</span></span> <span data-ttu-id="3a68a-115">Si el archivo de trabajo del servicio se almacenó en un `js` directorio, el ámbito del trabajador del servicio sería el `js` Directorio y los subdirectorios.</span><span class="sxs-lookup"><span data-stu-id="3a68a-115">If the Service Worker file was stored in a `js` directory, the scope of the Service Worker would be the `js` directory and any subdirectories.</span></span>  <span data-ttu-id="3a68a-116">Como práctica recomendada, coloque el archivo de trabajo del servicio en la raíz de su sitio, a menos que necesite reducir el ámbito del trabajador del servicio.</span><span class="sxs-lookup"><span data-stu-id="3a68a-116">As a best practice, place the Service Worker file in the root of your site, unless you need to reduce the scope of your Service Worker.</span></span>  

## <span data-ttu-id="3a68a-117">El ciclo de vida del trabajo del servicio</span><span class="sxs-lookup"><span data-stu-id="3a68a-117">The Service Worker lifecycle</span></span>  

<span data-ttu-id="3a68a-118">El ciclo de vida de un trabajador de servicio consta de varios pasos, con cada paso que desencadena un evento.</span><span class="sxs-lookup"><span data-stu-id="3a68a-118">The lifecycle of a Service Worker consists of multiple steps, with each step triggering an event.</span></span> <span data-ttu-id="3a68a-119">Puede Agregar agentes de escucha a estos eventos para ejecutar el código que realiza una acción.</span><span class="sxs-lookup"><span data-stu-id="3a68a-119">You can add listeners to these events to run code to perform an action.</span></span> <span data-ttu-id="3a68a-120">La siguiente lista presenta una vista de alto nivel del ciclo de vida y los eventos relacionados de los trabajadores del servicio.</span><span class="sxs-lookup"><span data-stu-id="3a68a-120">The following list presents a high-level view of the lifecycle and related events of service workers.</span></span> 

1. <span data-ttu-id="3a68a-121">Registrar el trabajador del servicio.</span><span class="sxs-lookup"><span data-stu-id="3a68a-121">Register the Service Worker.</span></span>  
1.  <span data-ttu-id="3a68a-122">El explorador descarga el archivo JavaScript, instala el trabajo del servicio y desencadena el `install` evento.</span><span class="sxs-lookup"><span data-stu-id="3a68a-122">The browser downloads the JavaScript file, installs the Service Worker, and triggers the `install` event.</span></span> <span data-ttu-id="3a68a-123">Puede usar el `install` evento para prealmacenar cualquier archivo importante y de larga duración, como archivos CSS, archivos JavaScript, imágenes de logotipos, páginas sin conexión, etc. de su sitio Web.</span><span class="sxs-lookup"><span data-stu-id="3a68a-123">You can use the `install` event to pre-cache any important and long-lived files, such as CSS files, JavaScript files, logo images, offline pages, and so on from your website.</span></span>  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  <span data-ttu-id="3a68a-124">El trabajador de servicio está activado, lo que provoca el `activate` evento.</span><span class="sxs-lookup"><span data-stu-id="3a68a-124">The Service Worker is activated, which triggers the `activate` event.</span></span>  <span data-ttu-id="3a68a-125">Use este evento para limpiar las memorias caché obsoletas.</span><span class="sxs-lookup"><span data-stu-id="3a68a-125">Use this event to clean up outdated caches.</span></span>  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  <span data-ttu-id="3a68a-126">El trabajo de servicio está listo para ejecutarse cuando se actualiza la página o cuando el usuario se desplaza a una nueva página del sitio.</span><span class="sxs-lookup"><span data-stu-id="3a68a-126">The Service Worker is ready to run when the page is refreshed or when the user navigates to a new page on the site.</span></span> <span data-ttu-id="3a68a-127">Si desea ejecutar el trabajo de servicio sin esperar, use el `self.skipWaiting()` método durante el `install` evento.</span><span class="sxs-lookup"><span data-stu-id="3a68a-127">If you want to run the Service Worker without waiting, use the `self.skipWaiting()` method during the `install` event.</span></span>  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  <span data-ttu-id="3a68a-128">El trabajo del servicio se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="3a68a-128">The Service Worker is now running.</span></span>     
    
## <span data-ttu-id="3a68a-129">Usar Fetch en trabajadores de servicio</span><span class="sxs-lookup"><span data-stu-id="3a68a-129">Using fetch in Service Workers</span></span>  

<span data-ttu-id="3a68a-130">El evento principal que se usa en un trabajador de servicio es el `fetch` evento.</span><span class="sxs-lookup"><span data-stu-id="3a68a-130">The main event that you use in a Service Worker is the `fetch` event.</span></span>  <span data-ttu-id="3a68a-131">El `fetch` evento se ejecuta cada vez que el explorador intenta obtener acceso al contenido dentro del ámbito del trabajador del servicio.</span><span class="sxs-lookup"><span data-stu-id="3a68a-131">The `fetch` event runs every time the browser attempts to access content within the scope of the Service Worker.</span></span> <span data-ttu-id="3a68a-132">En el siguiente fragmento de código se muestra cómo agregar un agente de escucha al evento Fetch.</span><span class="sxs-lookup"><span data-stu-id="3a68a-132">The following code snippet shows how to add a listener to the fetch event.</span></span>  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

<span data-ttu-id="3a68a-133">Dentro del `fetch` controlador, puede controlar si una solicitud va a la red, se extrae de la caché y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="3a68a-133">Within the `fetch` handler, you may control whether a request goes to the network, pulls from the cache, and so on.</span></span>  <span data-ttu-id="3a68a-134">Es probable que el método que tome varíe según el tipo de recurso que se solicita, la frecuencia con la que se actualiza y otra lógica empresarial exclusiva de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3a68a-134">The approach you take likely varies based upon the type of resource being requested, how frequently it is updated, and other business logic unique to your application.</span></span>  <span data-ttu-id="3a68a-135">Estos son algunos ejemplos de lo que puede hacer:</span><span class="sxs-lookup"><span data-stu-id="3a68a-135">Here are a few examples of what you may do:</span></span>  

*   <span data-ttu-id="3a68a-136">Si está disponible, devuelva una respuesta de la caché, de lo contrario, retroceder para solicitar el recurso a través de la red.</span><span class="sxs-lookup"><span data-stu-id="3a68a-136">If available, return a response from the cache, otherwise fallback to request the resource over the network.</span></span>  
*   <span data-ttu-id="3a68a-137">Obtener un recurso de la red, almacenar en caché una copia y devolver la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a68a-137">Fetch a resource from the network, cache a copy, and return the response.</span></span>
*   <span data-ttu-id="3a68a-138">Permitir que el usuario especifique una preferencia para guardar los datos.</span><span class="sxs-lookup"><span data-stu-id="3a68a-138">Allow user's to specify a preference to save data.</span></span> 
*   <span data-ttu-id="3a68a-139">Proporcione una imagen de marcador de posición para determinadas solicitudes de imágenes.</span><span class="sxs-lookup"><span data-stu-id="3a68a-139">Supply a placeholder image for certain image requests.</span></span>  
*   <span data-ttu-id="3a68a-140">Generar una respuesta directamente en el trabajo del servicio.</span><span class="sxs-lookup"><span data-stu-id="3a68a-140">Generate a response directly in the Service Worker.</span></span>  

## <span data-ttu-id="3a68a-141">Notificaciones push</span><span class="sxs-lookup"><span data-stu-id="3a68a-141">Push Notifications</span></span>  

<span data-ttu-id="3a68a-142">Los trabajadores del servicio pueden insertar notificaciones a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="3a68a-142">Service workers can push notifications to users.</span></span> <span data-ttu-id="3a68a-143">Las notificaciones push son útiles para pedir a los usuarios que vuelvan a participar con su aplicación después de que haya transcurrido algún tiempo.</span><span class="sxs-lookup"><span data-stu-id="3a68a-143">Push Notifications are helpful to prompt users to re-engage with your application after some time has elapsed.</span></span> <span data-ttu-id="3a68a-144">Para obtener más información, vea [tutorial y demostración de notificaciones push][AzurewebsitesWebpushdemo].</span><span class="sxs-lookup"><span data-stu-id="3a68a-144">For more information, see [Push Notifications walkthrough and demo][AzurewebsitesWebpushdemo].</span></span>  

## <span data-ttu-id="3a68a-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3a68a-145">See also</span></span>  

<span data-ttu-id="3a68a-146">Para obtener más información sobre los trabajos de servicio, consulte la siguiente lista de temas relacionados.</span><span class="sxs-lookup"><span data-stu-id="3a68a-146">To learn more about Service Workers, see the following list of related topics.</span></span>  

*   [<span data-ttu-id="3a68a-147">Realizar PWAs trabajar sin conexión con trabajadores de servicio</span><span class="sxs-lookup"><span data-stu-id="3a68a-147">Making PWAs work offline with Service workers</span></span>][MDNPwasMakingOfflineServiceWorkers]  
*   [<span data-ttu-id="3a68a-148">Cómo hacer que PWAs se pueda comunicar con las notificaciones y la inserción</span><span class="sxs-lookup"><span data-stu-id="3a68a-148">How to make PWAs re-engageable using Notifications and Push</span></span>][MDNPwasMakeReengageablesingNotificationsPush]  

<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Notificaciones de inserción en Web |  Demostraciones de Microsoft Edge"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Realizar PWAs trabajar sin conexión con trabajadores del servicio-PWAs | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "Cómo hacer que PWAs vuelva a estar habilitado usando las notificaciones y Push-PWAs | MDN"  

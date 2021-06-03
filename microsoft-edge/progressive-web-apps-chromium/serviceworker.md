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
# <a name="use-service-workers-to-manage-network-requests-and-push-notifications"></a><span data-ttu-id="cba77-104">Usar los trabajadores de servicio para administrar las solicitudes de red y las notificaciones de inserción</span><span class="sxs-lookup"><span data-stu-id="cba77-104">Use Service Workers to manage network requests and push notifications</span></span>

<span data-ttu-id="cba77-105">Los trabajadores de servicio son un tipo especial de trabajo web con la capacidad de interceptar, modificar y responder a todas las solicitudes de red mediante la `Fetch` API.</span><span class="sxs-lookup"><span data-stu-id="cba77-105">Service Workers are a special type of Web Worker with the ability to intercept, modify, and respond to all network requests using the `Fetch` API.</span></span>  <span data-ttu-id="cba77-106">Los trabajadores de servicio pueden tener acceso a la API y a los almacenes de datos asincrónicos del lado cliente, como `Cache` , para almacenar `IndexedDB` recursos.</span><span class="sxs-lookup"><span data-stu-id="cba77-106">Service Workers can access the `Cache` API, and asynchronous client-side data stores, such as `IndexedDB`, to store resources.</span></span>  

## <a name="registering-a-service-worker"></a><span data-ttu-id="cba77-107">Registro de un trabajador de servicio</span><span class="sxs-lookup"><span data-stu-id="cba77-107">Registering a Service Worker</span></span>  

<span data-ttu-id="cba77-108">Al igual que otros trabajadores web, los trabajadores de servicio deben existir en un archivo independiente.</span><span class="sxs-lookup"><span data-stu-id="cba77-108">Similar to other Web Workers, Service Workers must exist in a separate file.</span></span> <span data-ttu-id="cba77-109">Hace referencia a este archivo al registrar el trabajador de servicio, como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="cba77-109">You reference this file when registering the Service Worker, as shown in the following code snippet.</span></span>  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

<span data-ttu-id="cba77-110">Los exploradores modernos proporcionan diferentes niveles de compatibilidad para los trabajadores de servicio.</span><span class="sxs-lookup"><span data-stu-id="cba77-110">Modern browsers provide different levels of support for Service Workers.</span></span> <span data-ttu-id="cba77-111">Por lo tanto, es una buena práctica probar la existencia del objeto antes de ejecutar cualquier código relacionado con el trabajador `serviceWorker` de servicio.</span><span class="sxs-lookup"><span data-stu-id="cba77-111">As such, it is a good practice to test for the existence of the `serviceWorker` object before running any Service Worker-related code.</span></span> <span data-ttu-id="cba77-112">En el fragmento de código anterior, se registra un trabajador de servicio con `serviceworker.min.js` el archivo ubicado en la raíz del sitio.</span><span class="sxs-lookup"><span data-stu-id="cba77-112">In the above code snippet, a Service Worker is registered using the `serviceworker.min.js` file located at the root of the site.</span></span> <span data-ttu-id="cba77-113">Asegúrese de que el archivo JavaScript que define el trabajador de servicio existe en el directorio de nivel superior que desea que administre \(que se conoce como el ámbito del trabajador de servicio\).</span><span class="sxs-lookup"><span data-stu-id="cba77-113">Ensure that the JavaScript file that defines your Service Worker exists in the highest-level directory that you want it to manage \(which is referred to as the scope of the Service Worker\).</span></span>  <span data-ttu-id="cba77-114">En el fragmento de código anterior, el archivo se almacena en la raíz y el trabajador de servicio administra todas las páginas del dominio.</span><span class="sxs-lookup"><span data-stu-id="cba77-114">In the previous code snippet, the file is stored in the root, and the Service Worker manages all pages in the domain.</span></span> <span data-ttu-id="cba77-115">Si el archivo de trabajo de servicio se almacenaba en un directorio, el ámbito del trabajador de servicio `js` sería el directorio y los `js` subdirectorios.</span><span class="sxs-lookup"><span data-stu-id="cba77-115">If the Service Worker file was stored in a `js` directory, the scope of the Service Worker would be the `js` directory and any subdirectories.</span></span>  <span data-ttu-id="cba77-116">Como procedimiento recomendado, coloque el archivo de trabajo de servicio en la raíz del sitio, a menos que necesite reducir el ámbito del trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="cba77-116">As a best practice, place the Service Worker file in the root of your site, unless you need to reduce the scope of your Service Worker.</span></span>  

## <a name="the-service-worker-lifecycle"></a><span data-ttu-id="cba77-117">Ciclo de vida del trabajador de servicio</span><span class="sxs-lookup"><span data-stu-id="cba77-117">The Service Worker lifecycle</span></span>  

<span data-ttu-id="cba77-118">El ciclo de vida de un trabajador de servicio consta de varios pasos, con cada paso desencadenando un evento.</span><span class="sxs-lookup"><span data-stu-id="cba77-118">The lifecycle of a Service Worker consists of multiple steps, with each step triggering an event.</span></span> <span data-ttu-id="cba77-119">Puede agregar agentes de escucha a estos eventos para ejecutar código para realizar una acción.</span><span class="sxs-lookup"><span data-stu-id="cba77-119">You can add listeners to these events to run code to perform an action.</span></span> <span data-ttu-id="cba77-120">La siguiente lista presenta una vista de alto nivel del ciclo de vida y los eventos relacionados de los trabajadores del servicio.</span><span class="sxs-lookup"><span data-stu-id="cba77-120">The following list presents a high-level view of the lifecycle and related events of service workers.</span></span> 

1.  <span data-ttu-id="cba77-121">Registre el trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="cba77-121">Register the Service Worker.</span></span>  
1.  <span data-ttu-id="cba77-122">El explorador descarga el archivo JavaScript, instala el trabajador de servicio y desencadena el `install` evento.</span><span class="sxs-lookup"><span data-stu-id="cba77-122">The browser downloads the JavaScript file, installs the Service Worker, and triggers the `install` event.</span></span> <span data-ttu-id="cba77-123">Puede usar el evento para almacenar previamente en caché los archivos importantes y de larga duración, como archivos CSS, archivos JavaScript, imágenes de logotipo, páginas sin conexión, y así sucesivamente desde `install` su sitio web.</span><span class="sxs-lookup"><span data-stu-id="cba77-123">You can use the `install` event to pre-cache any important and long-lived files, such as CSS files, JavaScript files, logo images, offline pages, and so on from your website.</span></span>  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  <span data-ttu-id="cba77-124">El trabajador de servicio está activado, lo que desencadena el `activate` evento.</span><span class="sxs-lookup"><span data-stu-id="cba77-124">The Service Worker is activated, which triggers the `activate` event.</span></span>  <span data-ttu-id="cba77-125">Use este evento para limpiar cachés obsoletas.</span><span class="sxs-lookup"><span data-stu-id="cba77-125">Use this event to clean up outdated caches.</span></span>  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  <span data-ttu-id="cba77-126">El trabajador de servicio está listo para ejecutarse cuando se actualiza la página o cuando el usuario navega a una nueva página en el sitio.</span><span class="sxs-lookup"><span data-stu-id="cba77-126">The Service Worker is ready to run when the page is refreshed or when the user navigates to a new page on the site.</span></span> <span data-ttu-id="cba77-127">Si desea ejecutar el trabajador de servicio sin esperar, use el `self.skipWaiting()` método durante el `install` evento.</span><span class="sxs-lookup"><span data-stu-id="cba77-127">If you want to run the Service Worker without waiting, use the `self.skipWaiting()` method during the `install` event.</span></span>  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  <span data-ttu-id="cba77-128">El trabajador de servicio se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="cba77-128">The Service Worker is now running.</span></span>     
    
## <a name="using-fetch-in-service-workers"></a><span data-ttu-id="cba77-129">Uso de la recuperación en los trabajadores de servicio</span><span class="sxs-lookup"><span data-stu-id="cba77-129">Using fetch in Service Workers</span></span>  

<span data-ttu-id="cba77-130">El evento principal que se usa en un trabajador de servicio es el `fetch` evento.</span><span class="sxs-lookup"><span data-stu-id="cba77-130">The main event that you use in a Service Worker is the `fetch` event.</span></span>  <span data-ttu-id="cba77-131">El `fetch` evento se ejecuta cada vez que el explorador intenta obtener acceso al contenido dentro del ámbito del trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="cba77-131">The `fetch` event runs every time the browser attempts to access content within the scope of the Service Worker.</span></span> <span data-ttu-id="cba77-132">El siguiente fragmento de código muestra cómo agregar un agente de escucha al evento fetch.</span><span class="sxs-lookup"><span data-stu-id="cba77-132">The following code snippet shows how to add a listener to the fetch event.</span></span>  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

<span data-ttu-id="cba77-133">Dentro del controlador, puede controlar si una solicitud va `fetch` a la red, extrae de la memoria caché, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="cba77-133">Within the `fetch` handler, you may control whether a request goes to the network, pulls from the cache, and so on.</span></span>  <span data-ttu-id="cba77-134">El enfoque que tome probablemente varía en función del tipo de recurso que se solicita, la frecuencia con la que se actualiza y otra lógica empresarial única para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cba77-134">The approach you take likely varies based upon the type of resource being requested, how frequently it is updated, and other business logic unique to your application.</span></span>  <span data-ttu-id="cba77-135">Estos son algunos ejemplos de lo que puede hacer:</span><span class="sxs-lookup"><span data-stu-id="cba77-135">Here are a few examples of what you may do:</span></span>  

*   <span data-ttu-id="cba77-136">Si está disponible, devuelve una respuesta de la memoria caché, de lo contrario, reserva para solicitar el recurso a través de la red.</span><span class="sxs-lookup"><span data-stu-id="cba77-136">If available, return a response from the cache, otherwise fallback to request the resource over the network.</span></span>  
*   <span data-ttu-id="cba77-137">Captura un recurso de la red, almacena en caché una copia y devuelve la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cba77-137">Fetch a resource from the network, cache a copy, and return the response.</span></span>
*   <span data-ttu-id="cba77-138">Permitir que los usuarios especifiquen una preferencia para guardar datos.</span><span class="sxs-lookup"><span data-stu-id="cba77-138">Allow user's to specify a preference to save data.</span></span> 
*   <span data-ttu-id="cba77-139">Proporcione una imagen de marcador de posición para determinadas solicitudes de imagen.</span><span class="sxs-lookup"><span data-stu-id="cba77-139">Supply a placeholder image for certain image requests.</span></span>  
*   <span data-ttu-id="cba77-140">Genere una respuesta directamente en el trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="cba77-140">Generate a response directly in the Service Worker.</span></span>  
    
## <a name="push-notifications"></a><span data-ttu-id="cba77-141">Notificaciones de inserción</span><span class="sxs-lookup"><span data-stu-id="cba77-141">Push Notifications</span></span>  

<span data-ttu-id="cba77-142">Los trabajadores del servicio pueden enviar notificaciones a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="cba77-142">Service workers can push notifications to users.</span></span> <span data-ttu-id="cba77-143">Las notificaciones de inserción son útiles para pedir a los usuarios que vuelvan a interactuar con la aplicación una vez transcurrido algún tiempo.</span><span class="sxs-lookup"><span data-stu-id="cba77-143">Push Notifications are helpful to prompt users to re-engage with your application after some time has elapsed.</span></span> <span data-ttu-id="cba77-144">Para obtener más información, vaya al [tutorial y demostración de notificaciones de inserción.][AzurewebsitesWebpushdemo]</span><span class="sxs-lookup"><span data-stu-id="cba77-144">For more information, navigate to [Push Notifications walkthrough and demo][AzurewebsitesWebpushdemo].</span></span>  

## <a name="see-also"></a><span data-ttu-id="cba77-145">Consulta también</span><span class="sxs-lookup"><span data-stu-id="cba77-145">See also</span></span>  

<span data-ttu-id="cba77-146">Para obtener más información sobre los trabajadores de servicio, vaya a la siguiente lista de temas relacionados.</span><span class="sxs-lookup"><span data-stu-id="cba77-146">To learn more about Service Workers, navigate to the following list of related topics.</span></span>  

*   [<span data-ttu-id="cba77-147">Hacer que las PWA funcionen sin conexión con los trabajadores del servicio</span><span class="sxs-lookup"><span data-stu-id="cba77-147">Making PWAs work offline with Service workers</span></span>][MDNPwasMakingOfflineServiceWorkers]  
*   [<span data-ttu-id="cba77-148">Cómo hacer que las PWA se vuelvan a activar mediante notificaciones y inserción</span><span class="sxs-lookup"><span data-stu-id="cba77-148">How to make PWAs re-engageable using Notifications and Push</span></span>][MDNPwasMakeReengageablesingNotificationsPush]  
    
<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Notificaciones de inserción web |  Microsoft Edge Demos"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Hacer que las PWA funcionen sin conexión con los trabajadores de servicio: pwas | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "Cómo hacer que las PWA vuelvan a interactuar con notificaciones e inserción: pwas | MDN"  

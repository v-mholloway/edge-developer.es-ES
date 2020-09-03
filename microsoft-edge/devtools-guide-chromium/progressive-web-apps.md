---
description: Use el panel de aplicaciones para inspeccionar, modificar y depurar manifiestos de aplicaciones Web, trabajos de servicios y cachés de trabajos de servicios.
title: Depurar aplicaciones web progresivas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 7eb71d0d57d8a9227a54b921f15dfe434ad6e65b
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993607"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# <span data-ttu-id="1923f-104">Depurar aplicaciones web progresivas</span><span class="sxs-lookup"><span data-stu-id="1923f-104">Debug Progressive Web Apps</span></span>   



<span data-ttu-id="1923f-105">Use el panel de **aplicaciones** para inspeccionar, modificar y depurar manifiestos de aplicaciones Web, trabajos de servicios y cachés de trabajos de servicios.</span><span class="sxs-lookup"><span data-stu-id="1923f-105">Use the **Application** panel to inspect, modify, and debug web app manifests, service workers, and service worker caches.</span></span>  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

<span data-ttu-id="1923f-106">Esta guía solo trata las características de la aplicación web progresiva del panel de la **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="1923f-106">This guide only discusses the Progressive Web App features of the **Application** panel.</span></span>  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### <span data-ttu-id="1923f-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="1923f-107">Summary</span></span>  

*   <span data-ttu-id="1923f-108">Use el panel **manifiesto** para inspeccionar el manifiesto de la aplicación web y desencadenar agregar a eventos de pantalla Android.</span><span class="sxs-lookup"><span data-stu-id="1923f-108">Use the **Manifest** pane to inspect your web app manifest and trigger Add to Homescreen events.</span></span>  
*   <span data-ttu-id="1923f-109">Use el panel de **trabajos de servicio** para toda la gama de tareas relacionadas con los trabajos de los trabajadores, como la anulación del registro o la actualización de un servicio, la emulación de eventos de inserción, la desconexión o la detención de un trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="1923f-109">Use the **Service Workers** pane for a whole range of service-worker-related tasks, like unregistering or updating a service, emulating push events, going offline, or stopping a service worker.</span></span>  
*   <span data-ttu-id="1923f-110">Vea la caché de trabajos del servicio en el panel **almacenamiento en caché** .</span><span class="sxs-lookup"><span data-stu-id="1923f-110">View your service worker cache from the **Cache Storage** pane.</span></span>  
*   <span data-ttu-id="1923f-111">Anula el registro de un trabajador del servicio y borra todo el almacenamiento y las memorias caché con un solo clic del botón en el panel **Borrar almacenamiento** .</span><span class="sxs-lookup"><span data-stu-id="1923f-111">Unregister a service worker and clear all storage and caches with a single button click from the **Clear storage** pane.</span></span>  
    
## <span data-ttu-id="1923f-112">Manifiesto de la aplicación Web</span><span class="sxs-lookup"><span data-stu-id="1923f-112">Web app manifest</span></span>   

<span data-ttu-id="1923f-113">Si quiere que los usuarios puedan agregar la aplicación a su homescreens móvil, necesita un manifiesto de la aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="1923f-113">If you want your users to be able to add your app to their mobile homescreens, you need a web app manifest.</span></span>  <span data-ttu-id="1923f-114">El manifiesto define cómo aparece la aplicación en la pantalla Android, dónde dirigir al usuario cuando se inicia desde pantalla Android y qué aspecto tiene la aplicación al iniciar.</span><span class="sxs-lookup"><span data-stu-id="1923f-114">The manifest defines how the app appears on the homescreen, where to direct the user when launching from homescreen, and what the app looks like on launch.</span></span>  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

<span data-ttu-id="1923f-115">Una vez que tenga configurado el manifiesto, puede usar el panel de **manifiesto** del panel de **aplicaciones** para inspeccionarlo.</span><span class="sxs-lookup"><span data-stu-id="1923f-115">After you have your manifest set up, you can use the **Manifest** pane of the **Application** panel to inspect it.</span></span>  

:::image type="complex" source="./media/manifest-pane.msft.png" alt-text="El panel manifiesto" lightbox="./media/manifest-pane.msft.png":::
   <span data-ttu-id="1923f-117">El panel **manifiesto**</span><span class="sxs-lookup"><span data-stu-id="1923f-117">The **Manifest** Pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="1923f-118">Para ver el origen del manifiesto, haga clic en el vínculo debajo de la etiqueta de manifiesto de la **aplicación** \ ( `https://airhorner.com/manifest.json` en la figura anterior \).</span><span class="sxs-lookup"><span data-stu-id="1923f-118">To look at the manifest source, click the link below **App Manifest** label \(`https://airhorner.com/manifest.json` in the previous figure\).</span></span>  
<!-- *   Press the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   <span data-ttu-id="1923f-119">Las secciones **identidad** y **presentación** solo muestran campos del origen del manifiesto en una pantalla más fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="1923f-119">The **Identity** and **Presentation** sections just display fields from the manifest source in a more user-friendly display.</span></span>  
*   <span data-ttu-id="1923f-120">En la sección **iconos** se muestran todos los iconos que especificó.</span><span class="sxs-lookup"><span data-stu-id="1923f-120">The **Icons** section displays every icon that you've specified.</span></span>  
    
<!--### Simulate Add to Homescreen events   -->

<!--A web app can only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, this criteria can be inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You can test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Clicking on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="./media/io.msft.png" alt-text="Add to desktop shelf" lightbox="./media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature cannot yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you can successfully add your app to your desktop shelf, then it'll work for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you can connect a real mobile device to DevTools via **remote debugging**, and then click the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## <span data-ttu-id="1923f-121">Trabajadores de servicio</span><span class="sxs-lookup"><span data-stu-id="1923f-121">Service workers</span></span>   

<span data-ttu-id="1923f-122">Los trabajadores de servicios son una tecnología fundamental en la plataforma web futura.</span><span class="sxs-lookup"><span data-stu-id="1923f-122">Service workers are a fundamental technology in the future web platform.</span></span>  <span data-ttu-id="1923f-123">Son scripts que el explorador ejecuta en segundo plano, independientes de una página web.</span><span class="sxs-lookup"><span data-stu-id="1923f-123">They are scripts that the browser runs in the background, separate from a web page.</span></span>  <span data-ttu-id="1923f-124">Estas secuencias de comandos le permiten acceder a las características que no necesitan una página web o interacción del usuario, como las notificaciones de inserción, la sincronización en segundo plano y las experiencias sin conexión.</span><span class="sxs-lookup"><span data-stu-id="1923f-124">These scripts enable you to access features that don't need a web page or user interaction, like push notifications, background sync, and offline experiences.</span></span>  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

<span data-ttu-id="1923f-125">El panel de **trabajos de servicios** del panel de **aplicaciones** es el lugar principal en el DevTools para inspeccionar y depurar trabajos de servicio.</span><span class="sxs-lookup"><span data-stu-id="1923f-125">The **Service Workers** pane in the **Application** panel is the main place in DevTools to inspect and debug service workers.</span></span>  

:::image type="complex" source="./media/service-workers-pane.msft.png" alt-text="El panel de trabajos de servicios" lightbox="./media/service-workers-pane.msft.png":::
   <span data-ttu-id="1923f-127">El panel de **trabajos de servicios**</span><span class="sxs-lookup"><span data-stu-id="1923f-127">The **Service Workers** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="1923f-128">Si un trabajador de servicio está instalado en la página abierta actualmente, aparecerá en este panel.</span><span class="sxs-lookup"><span data-stu-id="1923f-128">If a service worker is installed to the currently open page, then you'll see it listed on this pane.</span></span>  <span data-ttu-id="1923f-129">Por ejemplo, en la ilustración anterior, hay un trabajo de servicio instalado para el ámbito de `https://weather-pwa-sample.firebaseapp.com` .</span><span class="sxs-lookup"><span data-stu-id="1923f-129">For example, in the previous figure, there is a service worker installed for the scope of `https://weather-pwa-sample.firebaseapp.com`.</span></span>  
*   <span data-ttu-id="1923f-130">La casilla de verificación **sin conexión** pone DevTools al modo sin conexión.</span><span class="sxs-lookup"><span data-stu-id="1923f-130">The **Offline** checkbox puts DevTools into offline mode.</span></span>  <span data-ttu-id="1923f-131">Es equivalente al modo sin conexión disponible en el panel **red** o a la `Go offline` opción en el [menú de comandos][DevtoolsCommandMenuIndex].</span><span class="sxs-lookup"><span data-stu-id="1923f-131">This is equivalent to the offline mode available from the **Network** panel, or the `Go offline` option in the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
*   <span data-ttu-id="1923f-132">La casilla **actualizar al volver a cargar** fuerza al trabajador del servicio a actualizar en todas las cargas de páginas.</span><span class="sxs-lookup"><span data-stu-id="1923f-132">The **Update on reload** checkbox forces the service worker to update on every page load.</span></span>  
*   <span data-ttu-id="1923f-133">La casilla **omitir para red** evita el trabajo de servicio y obliga al explorador a ir a la red para obtener los recursos solicitados.</span><span class="sxs-lookup"><span data-stu-id="1923f-133">The **Bypass for network** checkbox bypasses the service worker and forces the browser to go to the network for requested resources.</span></span>  
*   <span data-ttu-id="1923f-134">El botón **Actualizar** realiza una actualización única del trabajo de servicio especificado.</span><span class="sxs-lookup"><span data-stu-id="1923f-134">The **Update** button performs a one-time update of the specified service worker.</span></span>  
*   <span data-ttu-id="1923f-135">El botón de **comando** emula una notificación de inserción sin una carga \ (también conocida como **Tickle**\).</span><span class="sxs-lookup"><span data-stu-id="1923f-135">The **Push** button emulates a push notification without a payload \(also known as a **tickle**\).</span></span>  
*   <span data-ttu-id="1923f-136">El botón de **sincronización** emula un evento de sincronización en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="1923f-136">The **Sync** button emulates a background sync event.</span></span>  
*   <span data-ttu-id="1923f-137">El botón **anular registro** anula el registro del trabajo de servicio especificado.</span><span class="sxs-lookup"><span data-stu-id="1923f-137">The **Unregister** button unregisters the specified service worker.</span></span>  <span data-ttu-id="1923f-138">Consulte [Borrar almacenamiento](#clear-storage) para una forma de anular el registro de un trabajador de servicio y de borrar almacenamiento y memorias caché con un solo clic de botón.</span><span class="sxs-lookup"><span data-stu-id="1923f-138">Check out [Clear storage](#clear-storage) for a way to unregister a service worker and wipe storage and caches with a single button click.</span></span>  
*   <span data-ttu-id="1923f-139">La línea de **origen** le indica cuándo se instaló el trabajo de servicio actualmente en ejecución.</span><span class="sxs-lookup"><span data-stu-id="1923f-139">The **Source** line tells you when the currently running service worker was installed.</span></span>  <span data-ttu-id="1923f-140">El vínculo es el nombre del archivo de origen del trabajador del servicio.</span><span class="sxs-lookup"><span data-stu-id="1923f-140">The link is the name of the service worker's source file.</span></span>  <span data-ttu-id="1923f-141">Al hacer clic en el vínculo, se le envía a la fuente del trabajador del servicio.</span><span class="sxs-lookup"><span data-stu-id="1923f-141">Clicking on the link sends you to the service worker's source.</span></span>  
*   <span data-ttu-id="1923f-142">La línea de **Estado** indica el estado del trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="1923f-142">The **Status** line tells you the status of the service worker.</span></span>  <span data-ttu-id="1923f-143">El número de identificación situado junto al indicador de estado verde \ ( `#36` en la figura anterior \) es para el trabajador de servicios actualmente activo.</span><span class="sxs-lookup"><span data-stu-id="1923f-143">The ID number next to the green status indicator \(`#36` in previous figure\) is for the currently active Service Worker.</span></span>  <span data-ttu-id="1923f-144">Junto al estado verás un botón **iniciar** \ (si el trabajo de servicio está detenido \) o un botón **detener** \ (si el trabajo de servicio se está ejecutando \).</span><span class="sxs-lookup"><span data-stu-id="1923f-144">Next to the status you'll see a **start** button \(if the service worker is stopped\) or a **stop** button \(if the service worker is running\).</span></span>  <span data-ttu-id="1923f-145">Los trabajadores de servicios están diseñados para que el navegador los detenga y los inicie en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="1923f-145">Service workers are designed to be stopped and started by the browser at any time.</span></span>  <span data-ttu-id="1923f-146">Detener explícitamente el trabajo del servicio con el botón **detener** puede simularlo.</span><span class="sxs-lookup"><span data-stu-id="1923f-146">Explicitly stopping your service worker using the **stop** button can simulate that.</span></span>  <span data-ttu-id="1923f-147">Detener el trabajo del servicio es una excelente forma de comprobar cómo se comporta el código cuando vuelve a iniciarse el trabajo del servicio.</span><span class="sxs-lookup"><span data-stu-id="1923f-147">Stopping your service worker is a great way to test how your code behaves when the service worker starts back up again.</span></span>  <span data-ttu-id="1923f-148">Con frecuencia, revela errores a causa de suposiciones defectuosas sobre el estado global persistente.</span><span class="sxs-lookup"><span data-stu-id="1923f-148">It frequently reveals bugs due to faulty assumptions about persistent global state.</span></span>  
*   <span data-ttu-id="1923f-149">La línea **clientes** le indica el origen al que el trabajador de servicio está en el ámbito.</span><span class="sxs-lookup"><span data-stu-id="1923f-149">The **Clients** line tells you the origin that the service worker is scoped to.</span></span>  <span data-ttu-id="1923f-150">El botón **foco** es principalmente útil cuando se ha habilitado la casilla **Mostrar todo** .</span><span class="sxs-lookup"><span data-stu-id="1923f-150">The **focus** button is mostly useful when you've enabled the **show all** checkbox.</span></span>  <span data-ttu-id="1923f-151">Cuando esta casilla esté habilitada, todos los trabajos de servicio registrados aparecerán en la lista.</span><span class="sxs-lookup"><span data-stu-id="1923f-151">When that checkbox is enabled, all registered service workers are listed.</span></span>  <span data-ttu-id="1923f-152">Si hace clic en el botón **foco** junto a un trabajador de servicio que se está ejecutando en una pestaña diferente, Microsoft Edge se centra en esa pestaña.</span><span class="sxs-lookup"><span data-stu-id="1923f-152">If you click on the **focus** button next to a service worker that is running in a different tab, Microsoft Edge focuses on that tab.</span></span>  
    
<span data-ttu-id="1923f-153">Si el trabajo de servicio provoca errores, aparece una nueva etiqueta denominada **errores** .</span><span class="sxs-lookup"><span data-stu-id="1923f-153">If the service worker causes any errors, a new label called **Errors** shows up.</span></span>  

<!--  
:::image type="complex" source="./media/sw-error.msft.png" alt-text="Service worker with errors" lightbox="./media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## <span data-ttu-id="1923f-154">Cachés de trabajos del servicio</span><span class="sxs-lookup"><span data-stu-id="1923f-154">Service worker caches</span></span> 

<span data-ttu-id="1923f-155">El panel **almacenamiento en caché** proporciona una lista de solo lectura de los recursos que se han almacenado en caché con la [API de caché][MDNWebCacheAPI]\ (trabajo de servicio \).</span><span class="sxs-lookup"><span data-stu-id="1923f-155">The **Cache Storage** pane provides a read-only list of resources that have been cached using the \(service worker\) [Cache API][MDNWebCacheAPI].</span></span>  

:::image type="complex" source="./media/cache-pane-cache-storage-resources.msft.png" alt-text="Panel almacenamiento en caché" lightbox="./media/cache-pane-cache-storage-resources.msft.png":::
   <span data-ttu-id="1923f-157">Panel **almacenamiento en caché**</span><span class="sxs-lookup"><span data-stu-id="1923f-157">The **Cache Storage** Pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="1923f-158">La primera vez que abre una caché y le agrega un recurso, es posible que DevTools no detecte el cambio.</span><span class="sxs-lookup"><span data-stu-id="1923f-158">The first time you open a cache and add a resource to it, DevTools might not detect the change.</span></span>  <span data-ttu-id="1923f-159">Vuelva a cargar la página y verá la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="1923f-159">Reload the page and you should see the cache.</span></span>  

<span data-ttu-id="1923f-160">Si tiene dos o más memorias caché abiertas, las verá debajo de la lista desplegable **almacenamiento en caché** .</span><span class="sxs-lookup"><span data-stu-id="1923f-160">If you have two or more caches open, you'll see them listed below the **Cache Storage** dropdown.</span></span>  

:::image type="complex" source="./media/cache-pane-cache-storage.msft.png" alt-text="Lista desplegable de almacenamiento en caché" lightbox="./media/cache-pane-cache-storage.msft.png":::
   <span data-ttu-id="1923f-162">Lista desplegable de **almacenamiento en caché**</span><span class="sxs-lookup"><span data-stu-id="1923f-162">The **Cache Storage** dropdown</span></span>  
:::image-end:::  

## <span data-ttu-id="1923f-163">Uso de cuotas</span><span class="sxs-lookup"><span data-stu-id="1923f-163">Quota usage</span></span> 

<span data-ttu-id="1923f-164">Es posible que algunas respuestas dentro del panel **almacenamiento en caché** se marquen como "opacas".</span><span class="sxs-lookup"><span data-stu-id="1923f-164">Some responses within the **Cache Storage** pane may be flagged as being "opaque".</span></span>  <span data-ttu-id="1923f-165">Se refiere a una respuesta recuperada de un origen diferente, como en una **CDN** o una API remota, cuando [CORS][FetchHttpCorsProtocol] no está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1923f-165">This refers to a response retrieved from a different origin, like from a **CDN** or remote API, when [CORS][FetchHttpCorsProtocol] is not enabled.</span></span>  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

<span data-ttu-id="1923f-166">Para evitar la pérdida de información entre dominios, se agrega un relleno significativo al tamaño de una respuesta opaca que se usa para calcular los límites de la cuota de almacenamiento \ (por ejemplo, si `QuotaExceeded` se inicia una excepción \) y la API informa de ello `navigator.storage` .</span><span class="sxs-lookup"><span data-stu-id="1923f-166">In order to avoid leakage of cross-domain information, there's significant padding added to the size of an opaque response used for calculating storage quota limits \(for example whether a `QuotaExceeded` exception is thrown\) and reported by the `navigator.storage` API.</span></span>  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

<span data-ttu-id="1923f-167">Los detalles de este relleno varían según el explorador y el explorador, pero en Microsoft Edge, esto significa que el **tamaño mínimo** de una sola respuesta opaca en caché contribuye al uso general de almacenamiento es de [aproximadamente 7 megabytes][ChromiumIssues796060#c17].</span><span class="sxs-lookup"><span data-stu-id="1923f-167">The details of this padding vary from browser to browser, but for Microsoft Edge, this means that the **minimum size** that any single cached opaque response contributes to the overall storage usage is [approximately 7 megabytes][ChromiumIssues796060#c17].</span></span>  <span data-ttu-id="1923f-168">Debe tener esto en cuenta al determinar cuántas respuestas opacas desea almacenar en caché, ya que es posible que pueda haber superado fácilmente las limitaciones de la cuota de almacenamiento, muy pronto como cabría esperar, en función del tamaño real de los recursos opacos.</span><span class="sxs-lookup"><span data-stu-id="1923f-168">You should keep this in mind when determining how many opaque responses you want to cache, since you could easily exceeded storage quota limitations much sooner than you'd otherwise expect based on the actual size of the opaque resources.</span></span>  

<span data-ttu-id="1923f-169">Guías relacionadas:</span><span class="sxs-lookup"><span data-stu-id="1923f-169">Related Guides:</span></span>  

*   [<span data-ttu-id="1923f-170">Desbordamiento de la pila: ¿Qué limitaciones se aplican a las respuestas opacas?</span><span class="sxs-lookup"><span data-stu-id="1923f-170">Stack Overflow: What limitations apply to opaque responses?</span></span>][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## <span data-ttu-id="1923f-171">Borrar almacenamiento</span><span class="sxs-lookup"><span data-stu-id="1923f-171">Clear storage</span></span> 

<span data-ttu-id="1923f-172">El panel **Borrar almacenamiento** es una característica muy útil al desarrollar aplicaciones web progresivas.</span><span class="sxs-lookup"><span data-stu-id="1923f-172">The **Clear Storage** pane is a very useful feature when developing progressive web apps.</span></span>  <span data-ttu-id="1923f-173">Este panel le permite anular el registro de los trabajadores de los servicios y borrar todas las cachés y almacenamiento con un solo clic de botón.</span><span class="sxs-lookup"><span data-stu-id="1923f-173">This pane lets you unregister service workers and clear all caches and storage with a single button click.</span></span>  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides 

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
<!--TODO  -->

<!--  
 


-->  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ./command-menu/index.md "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Cromo problema 796060: el valor de almacenamiento en caché aumenta en cada actualización cuando el código de análisis está en HTML"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Caché-API Web | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Desbordamiento de la pila: ¿Qué limitaciones se aplican a las respuestas opacas?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> <span data-ttu-id="1923f-178">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1923f-178">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1923f-179">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="1923f-179">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1923f-181">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1923f-181">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

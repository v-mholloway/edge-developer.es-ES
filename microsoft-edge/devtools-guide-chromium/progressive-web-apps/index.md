---
description: Use el panel Aplicación para inspeccionar, modificar y depurar manifiestos de aplicaciones web, trabajadores de servicio y cachés de trabajadores de servicio.
title: Depurar aplicaciones web progresivas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: aea01d25474a030e78ac0eaeaef3954ab7f4539f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398542"
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

# <a name="debug-progressive-web-apps"></a><span data-ttu-id="6ab80-104">Depurar aplicaciones web progresivas</span><span class="sxs-lookup"><span data-stu-id="6ab80-104">Debug Progressive Web Apps</span></span>  

<span data-ttu-id="6ab80-105">Use el panel **Aplicación** para inspeccionar, modificar y depurar manifiestos de aplicaciones web, trabajadores de servicio y cachés de trabajadores de servicio.</span><span class="sxs-lookup"><span data-stu-id="6ab80-105">Use the **Application** panel to inspect, modify, and debug web app manifests, service workers, and service worker caches.</span></span>  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

<span data-ttu-id="6ab80-106">Esta guía solo analiza las características de La aplicación web progresiva **del** panel Aplicación.</span><span class="sxs-lookup"><span data-stu-id="6ab80-106">This guide only discusses the Progressive Web App features of the **Application** panel.</span></span>  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### <a name="summary"></a><span data-ttu-id="6ab80-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="6ab80-107">Summary</span></span>  

*   <span data-ttu-id="6ab80-108">Usa el **panel Manifiesto** para inspeccionar el manifiesto de la aplicación web y desencadenar los eventos Agregar a pantalla principal.</span><span class="sxs-lookup"><span data-stu-id="6ab80-108">Use the **Manifest** pane to inspect your web app manifest and trigger Add to Homescreen events.</span></span>  
*   <span data-ttu-id="6ab80-109">Use el panel **Trabajadores** de servicio para toda una gama de tareas relacionadas con el trabajo de servicio, como anular el registro o actualizar un servicio, emular eventos de inserción, desconectarse o detener a un trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="6ab80-109">Use the **Service Workers** pane for a whole range of service-worker-related tasks, like unregistering or updating a service, emulating push events, going offline, or stopping a service worker.</span></span>  
*   <span data-ttu-id="6ab80-110">Vea la memoria caché del trabajador de servicio desde el **panel Almacenamiento de caché.**</span><span class="sxs-lookup"><span data-stu-id="6ab80-110">View your service worker cache from the **Cache Storage** pane.</span></span>  
*   <span data-ttu-id="6ab80-111">Anula el registro de un trabajador de servicio y borra todo el almacenamiento y las memorias caché con un solo botón elige en el **panel Borrar** almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="6ab80-111">Unregister a service worker and clear all storage and caches with a single button choose from the **Clear storage** pane.</span></span>  
    
## <a name="web-app-manifest"></a><span data-ttu-id="6ab80-112">Manifiesto de aplicación web</span><span class="sxs-lookup"><span data-stu-id="6ab80-112">Web app manifest</span></span>  

<span data-ttu-id="6ab80-113">Si quieres que los usuarios puedan agregar la aplicación a sus pantallas de inicio móviles, necesitas un manifiesto de aplicación web.</span><span class="sxs-lookup"><span data-stu-id="6ab80-113">If you want your users to be able to add your app to their mobile homescreens, you need a web app manifest.</span></span>  <span data-ttu-id="6ab80-114">El manifiesto define cómo aparece la aplicación en la pantalla principal, dónde dirigir al usuario al iniciarse desde la pantalla principal y cómo es la aplicación al iniciarla.</span><span class="sxs-lookup"><span data-stu-id="6ab80-114">The manifest defines how the app appears on the homescreen, where to direct the user when launching from homescreen, and what the app looks like on launch.</span></span>  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

<span data-ttu-id="6ab80-115">Después de configurar el manifiesto, puede usar el **panel Manifiesto** del panel **Aplicación** para inspeccionarlo.</span><span class="sxs-lookup"><span data-stu-id="6ab80-115">After you have your manifest set up, you may use the **Manifest** pane of the **Application** panel to inspect it.</span></span>  

:::image type="complex" source="../media/manifest-pane.msft.png" alt-text="Panel de manifiesto" lightbox="../media/manifest-pane.msft.png":::
   <span data-ttu-id="6ab80-117">Panel **de** manifiesto</span><span class="sxs-lookup"><span data-stu-id="6ab80-117">The **Manifest** Pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="6ab80-118">Para ver el origen del manifiesto, elija el vínculo debajo de la etiqueta **manifiesto** de la aplicación \( `https://airhorner.com/manifest.json` en la figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="6ab80-118">To look at the manifest source, choose the link below **App Manifest** label \(`https://airhorner.com/manifest.json` in the previous figure\).</span></span>  
<!-- *   Choose the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   <span data-ttu-id="6ab80-119">Las **secciones Identity** y **Presentation** solo muestran campos del origen del manifiesto en una presentación más fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="6ab80-119">The **Identity** and **Presentation** sections just display fields from the manifest source in a more user-friendly display.</span></span>  
*   <span data-ttu-id="6ab80-120">La **sección** Iconos muestra todos los iconos especificados.</span><span class="sxs-lookup"><span data-stu-id="6ab80-120">The **Icons** section displays every icon that you've specified.</span></span>  
    
<!--### Simulate Add to Homescreen events  -->

<!--A web app may only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, the criteria is potentially inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You may test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Choosing on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="../media/io.msft.png" alt-text="Add to desktop shelf" lightbox="../media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature may not yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you may successfully add your app to your desktop shelf, then it works for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you may connect a real mobile device to DevTools via **remote debugging**, and then choose the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## <a name="service-workers"></a><span data-ttu-id="6ab80-121">Trabajadores de servicios</span><span class="sxs-lookup"><span data-stu-id="6ab80-121">Service workers</span></span>  

<span data-ttu-id="6ab80-122">Los trabajadores de servicio son una tecnología fundamental en la futura plataforma web.</span><span class="sxs-lookup"><span data-stu-id="6ab80-122">Service workers are a fundamental technology in the future web platform.</span></span>  <span data-ttu-id="6ab80-123">Son scripts que el explorador ejecuta en segundo plano, separados de una página web.</span><span class="sxs-lookup"><span data-stu-id="6ab80-123">They are scripts that the browser runs in the background, separate from a web page.</span></span>  <span data-ttu-id="6ab80-124">Los scripts permiten tener acceso a características que sin necesidad de una página web o interacción del usuario, como notificaciones de inserción, sincronización en segundo plano y experiencias sin conexión.</span><span class="sxs-lookup"><span data-stu-id="6ab80-124">The scripts allow you to access features that without the need of a web page or user interaction, like push notifications, background sync, and offline experiences.</span></span>  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

<span data-ttu-id="6ab80-125">El **panel Trabajadores de** servicio del panel **Aplicación** es el lugar principal de DevTools para inspeccionar y depurar trabajadores de servicio.</span><span class="sxs-lookup"><span data-stu-id="6ab80-125">The **Service Workers** pane in the **Application** panel is the main place in DevTools to inspect and debug service workers.</span></span>  

:::image type="complex" source="../media/service-workers-pane.msft.png" alt-text="Panel Trabajadores de servicio" lightbox="../media/service-workers-pane.msft.png":::
   <span data-ttu-id="6ab80-127">Panel **Trabajadores de** servicio</span><span class="sxs-lookup"><span data-stu-id="6ab80-127">The **Service Workers** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="6ab80-128">Si un trabajador de servicio está instalado en la página abierta actualmente, aparece en este panel.</span><span class="sxs-lookup"><span data-stu-id="6ab80-128">If a service worker is installed to the currently open page, then it is listed on this pane.</span></span>  <span data-ttu-id="6ab80-129">Por ejemplo, en la figura anterior, hay un trabajador de servicio instalado para el ámbito de `https://weather-pwa-sample.firebaseapp.com` .</span><span class="sxs-lookup"><span data-stu-id="6ab80-129">For example, in the previous figure, there is a service worker installed for the scope of `https://weather-pwa-sample.firebaseapp.com`.</span></span>  
*   <span data-ttu-id="6ab80-130">La **casilla Sin** conexión pone DevTools en modo sin conexión.</span><span class="sxs-lookup"><span data-stu-id="6ab80-130">The **Offline** checkbox puts DevTools into offline mode.</span></span>  <span data-ttu-id="6ab80-131">Esto equivale al modo sin conexión disponible en la **herramienta Red** o a la opción del `Go offline` menú [comando][DevtoolsCommandMenuIndex].</span><span class="sxs-lookup"><span data-stu-id="6ab80-131">This is equivalent to the offline mode available from the **Network** tool, or the `Go offline` option in the [Command Menu][DevtoolsCommandMenuIndex].</span></span>  
*   <span data-ttu-id="6ab80-132">La **casilla Actualizar al volver a cargar** fuerza al trabajador del servicio a actualizarse en cada carga de página.</span><span class="sxs-lookup"><span data-stu-id="6ab80-132">The **Update on reload** checkbox forces the service worker to update on every page load.</span></span>  
*   <span data-ttu-id="6ab80-133">La **casilla Omitir para red** omite al trabajador del servicio y fuerza al explorador a ir a la red en busca de recursos solicitados.</span><span class="sxs-lookup"><span data-stu-id="6ab80-133">The **Bypass for network** checkbox bypasses the service worker and forces the browser to go to the network for requested resources.</span></span>  
*   <span data-ttu-id="6ab80-134">El **botón** Actualizar realiza una actualización única del trabajador de servicio especificado.</span><span class="sxs-lookup"><span data-stu-id="6ab80-134">The **Update** button performs a one-time update of the specified service worker.</span></span>  
*   <span data-ttu-id="6ab80-135">El **botón Push** emula una notificación de inserción sin una carga \(también conocida como **tickle**\).</span><span class="sxs-lookup"><span data-stu-id="6ab80-135">The **Push** button emulates a push notification without a payload \(also known as a **tickle**\).</span></span>  
*   <span data-ttu-id="6ab80-136">El **botón Sincronizar** emula un evento de sincronización en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="6ab80-136">The **Sync** button emulates a background sync event.</span></span>  
*   <span data-ttu-id="6ab80-137">El **botón Anular registro** anula el registro del trabajador de servicio especificado.</span><span class="sxs-lookup"><span data-stu-id="6ab80-137">The **Unregister** button unregisters the specified service worker.</span></span>  <span data-ttu-id="6ab80-138">Consulte [Borrar almacenamiento para](#clear-storage) obtener una forma de anular el registro de un trabajador de servicio y borrar el almacenamiento y las memorias caché con un solo botón.</span><span class="sxs-lookup"><span data-stu-id="6ab80-138">Check out [Clear storage](#clear-storage) for a way to unregister a service worker and wipe storage and caches with a single button choose.</span></span>  
*   <span data-ttu-id="6ab80-139">La **línea Origen** indica cuándo se instaló el trabajador de servicio que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="6ab80-139">The **Source** line tells you when the currently running service worker was installed.</span></span>  <span data-ttu-id="6ab80-140">El vínculo es el nombre del archivo de origen del trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="6ab80-140">The link is the name of the source file of the service worker.</span></span>  <span data-ttu-id="6ab80-141">Al elegir en el vínculo, se envía al origen del trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="6ab80-141">Choosing on the link sends you to the source of the service worker.</span></span>  
*   <span data-ttu-id="6ab80-142">La **línea** Estado indica el estado del trabajador del servicio.</span><span class="sxs-lookup"><span data-stu-id="6ab80-142">The **Status** line tells you the status of the service worker.</span></span>  <span data-ttu-id="6ab80-143">El número de identificador junto al indicador de estado verde \( en la `#36` figura anterior\) es para el trabajador de servicio activo actualmente.</span><span class="sxs-lookup"><span data-stu-id="6ab80-143">The ID number next to the green status indicator \(`#36` in previous figure\) is for the currently active Service Worker.</span></span>  <span data-ttu-id="6ab80-144">Junto al estado,  se muestra un botón inicio \(si  el trabajador de servicio está detenido\) o un botón de detenerse \(si el trabajador de servicio se está ejecutando\).</span><span class="sxs-lookup"><span data-stu-id="6ab80-144">Next to the status, a **start** button \(if the service worker is stopped\) or a **stop** button \(if the service worker is running\) is displayed.</span></span>  <span data-ttu-id="6ab80-145">Los trabajadores de servicio están diseñados para ser detenidos e iniciados por el explorador en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="6ab80-145">Service workers are designed to be stopped and started by the browser at any time.</span></span>  <span data-ttu-id="6ab80-146">Detener explícitamente al trabajador del servicio mediante el **botón de** detención puede simularlo.</span><span class="sxs-lookup"><span data-stu-id="6ab80-146">Explicitly stopping your service worker using the **stop** button may simulate that.</span></span>  <span data-ttu-id="6ab80-147">Detener al trabajador de servicio es una excelente manera de probar cómo se comporta el código cuando el trabajador de servicio vuelve a iniciar la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6ab80-147">Stopping your service worker is a great way to test how your code behaves when the service worker starts back up again.</span></span>  <span data-ttu-id="6ab80-148">Con frecuencia, se revelan errores debido a suposiciones erróneas sobre el estado global persistente.</span><span class="sxs-lookup"><span data-stu-id="6ab80-148">It frequently reveals bugs due to faulty assumptions about persistent global state.</span></span>  
*   <span data-ttu-id="6ab80-149">La **línea Clientes** indica el origen al que está ámbito el trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="6ab80-149">The **Clients** line tells you the origin that the service worker is scoped to.</span></span>  <span data-ttu-id="6ab80-150">El **botón** de foco es principalmente útil cuando se ha habilitado la casilla **mostrar todo.**</span><span class="sxs-lookup"><span data-stu-id="6ab80-150">The **focus** button is mostly useful when you've enabled the **show all** checkbox.</span></span>  <span data-ttu-id="6ab80-151">Cuando esta casilla está habilitada, se enumeran todos los trabajadores de servicio registrados.</span><span class="sxs-lookup"><span data-stu-id="6ab80-151">When that checkbox is enabled, all registered service workers are listed.</span></span>  <span data-ttu-id="6ab80-152">Si elige en el botón **de enfoque** junto a un trabajador de servicio que se ejecuta en una pestaña diferente, Microsoft Edge se centra en esa pestaña.</span><span class="sxs-lookup"><span data-stu-id="6ab80-152">If you choose on the **focus** button next to a service worker that is running in a different tab, Microsoft Edge focuses on that tab.</span></span>  
    
<span data-ttu-id="6ab80-153">Si el trabajador del servicio provoca algún error, aparece una nueva etiqueta denominada **Errores.**</span><span class="sxs-lookup"><span data-stu-id="6ab80-153">If the service worker causes any errors, a new label called **Errors** shows up.</span></span>  

<!--  
:::image type="complex" source="../media/sw-error.msft.png" alt-text="Service worker with errors" lightbox="../media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## <a name="service-worker-caches"></a><span data-ttu-id="6ab80-154">Cachés de trabajadores de servicio</span><span class="sxs-lookup"><span data-stu-id="6ab80-154">Service worker caches</span></span>  

<span data-ttu-id="6ab80-155">El **panel Almacenamiento de** caché proporciona una lista de solo lectura de los recursos que se han almacenado en caché mediante la [API][MDNWebCacheAPI]de caché \(service worker\) .</span><span class="sxs-lookup"><span data-stu-id="6ab80-155">The **Cache Storage** pane provides a read-only list of resources that have been cached using the \(service worker\) [Cache API][MDNWebCacheAPI].</span></span>  

:::image type="complex" source="../media/cache-pane-cache-storage-resources.msft.png" alt-text="Panel de almacenamiento en caché" lightbox="../media/cache-pane-cache-storage-resources.msft.png":::
   <span data-ttu-id="6ab80-157">Panel **de almacenamiento en caché**</span><span class="sxs-lookup"><span data-stu-id="6ab80-157">The **Cache Storage** Pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="6ab80-158">La primera vez que abra una memoria caché y le agregue un recurso, Es posible que DevTools no detecte el cambio.</span><span class="sxs-lookup"><span data-stu-id="6ab80-158">The first time you open a cache and add a resource to it, DevTools may not detect the change.</span></span>  <span data-ttu-id="6ab80-159">Actualice la página y muestre la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="6ab80-159">Refresh the page and to display the cache.</span></span>  

<span data-ttu-id="6ab80-160">Si tiene dos o más cachés abiertas, las cachés se muestran en el siguiente desplegable **Almacenamiento de caché.**</span><span class="sxs-lookup"><span data-stu-id="6ab80-160">If you have two or more caches open, the caches display under the following **Cache Storage** dropdown.</span></span>  

:::image type="complex" source="../media/cache-pane-cache-storage.msft.png" alt-text="Desplegable Almacenamiento en caché" lightbox="../media/cache-pane-cache-storage.msft.png":::
   <span data-ttu-id="6ab80-162">Desplegable **Almacenamiento en caché**</span><span class="sxs-lookup"><span data-stu-id="6ab80-162">The **Cache Storage** dropdown</span></span>  
:::image-end:::  

## <a name="quota-usage"></a><span data-ttu-id="6ab80-163">Uso de cuota</span><span class="sxs-lookup"><span data-stu-id="6ab80-163">Quota usage</span></span>  

<span data-ttu-id="6ab80-164">Algunas respuestas dentro del panel **Almacenamiento de** caché pueden estar marcadas como "opacas".</span><span class="sxs-lookup"><span data-stu-id="6ab80-164">Some responses within the **Cache Storage** pane may be flagged as being "opaque".</span></span>  <span data-ttu-id="6ab80-165">Esto hace referencia a una respuesta recuperada de un origen diferente, como de una **RED CDN** o API remota, cuando [CORS][FetchHttpCorsProtocol] no está habilitado.</span><span class="sxs-lookup"><span data-stu-id="6ab80-165">This refers to a response retrieved from a different origin, like from a **CDN** or remote API, when [CORS][FetchHttpCorsProtocol] is not enabled.</span></span>  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

<span data-ttu-id="6ab80-166">Para evitar la pérdida de información entre dominios, se agrega un relleno significativo al tamaño de una respuesta opaca usada para calcular los límites de cuota de almacenamiento \(por ejemplo, si se produce una excepción\) y se notifica mediante la `QuotaExceeded` `navigator.storage` API.</span><span class="sxs-lookup"><span data-stu-id="6ab80-166">In order to avoid leakage of cross-domain information, significant padding is added to the size of an opaque response used for calculating storage quota limits \(for example whether a `QuotaExceeded` exception is thrown\) and reported by the `navigator.storage` API.</span></span>  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

<span data-ttu-id="6ab80-167">Los detalles de este relleno varían de un explorador a  otro, pero para Microsoft Edge, esto significa que el tamaño mínimo que cualquier respuesta opaca almacenada en caché contribuye al uso general de almacenamiento es de aproximadamente [7 megabytes][ChromiumIssues796060#c17].</span><span class="sxs-lookup"><span data-stu-id="6ab80-167">The details of this padding vary from browser to browser, but for Microsoft Edge, this means that the **minimum size** that any single cached opaque response contributes to the overall storage usage is [approximately 7 megabytes][ChromiumIssues796060#c17].</span></span>  <span data-ttu-id="6ab80-168">Recuerde el relleno al determinar cuántas respuestas opacas desea almacenar en caché, ya que puede superar fácilmente las limitaciones de cuota de almacenamiento mucho antes de lo que espera en función del tamaño real de los recursos opacos.</span><span class="sxs-lookup"><span data-stu-id="6ab80-168">Remember the padding when determining how many opaque responses you want to cache, since you may easily exceed storage quota limitations much sooner than you otherwise expect based on the actual size of the opaque resources.</span></span>  

<span data-ttu-id="6ab80-169">Guías relacionadas:</span><span class="sxs-lookup"><span data-stu-id="6ab80-169">Related Guides:</span></span>  

*   [<span data-ttu-id="6ab80-170">Desbordamiento de pila: ¿qué limitaciones se aplican a las respuestas opacas?</span><span class="sxs-lookup"><span data-stu-id="6ab80-170">Stack Overflow: What limitations apply to opaque responses?</span></span>][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## <a name="clear-storage"></a><span data-ttu-id="6ab80-171">Borrar almacenamiento</span><span class="sxs-lookup"><span data-stu-id="6ab80-171">Clear storage</span></span>  

<span data-ttu-id="6ab80-172">El **panel Borrar almacenamiento** es una característica muy útil al desarrollar aplicaciones web progresivas.</span><span class="sxs-lookup"><span data-stu-id="6ab80-172">The **Clear Storage** pane is a very useful feature when developing progressive web apps.</span></span>  <span data-ttu-id="6ab80-173">Este panel permite anular el registro de los trabajadores del servicio y borrar todas las cachés y el almacenamiento con un solo botón.</span><span class="sxs-lookup"><span data-stu-id="6ab80-173">This pane lets you unregister service workers and clear all caches and storage with a single button choose.</span></span>  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides   

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6ab80-174">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6ab80-174">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Chromium Issue 796060: El valor de almacenamiento en caché aumenta en cada actualización cuando el código de Analytics está en el html"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Caché: API web | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Desbordamiento de pila: ¿qué limitaciones se aplican a las respuestas opacas?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> <span data-ttu-id="6ab80-179">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6ab80-179">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6ab80-180">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="6ab80-180">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6ab80-182">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6ab80-182">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

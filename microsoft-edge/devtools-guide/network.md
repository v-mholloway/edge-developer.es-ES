---
description: Usar el panel red para supervisar y perfilar las solicitudes de recursos de página
title: DevTools-red
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, red, tiempo de carga, http, https, caché del explorador, HAR
ms.custom: seodec18
ms.openlocfilehash: 0b190f5163f9b7a9f9920877a94577177053e4f6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573798"
---
# <span data-ttu-id="8cc24-104">Red</span><span class="sxs-lookup"><span data-stu-id="8cc24-104">Network</span></span>

<span data-ttu-id="8cc24-105">Use el panel **red** para supervisar, inspeccionar y perfilar las solicitudes y respuestas enviadas a través de la conexión.</span><span class="sxs-lookup"><span data-stu-id="8cc24-105">Use the **Network** panel to monitor, inspect and profile the requests and responses sent over the wire.</span></span> <span data-ttu-id="8cc24-106">Con ella, puedes hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8cc24-106">With it, you can:</span></span>

 - <span data-ttu-id="8cc24-107">[Examinar un registro de todas las solicitudes de recursos](#network-summary) realizadas por la página</span><span class="sxs-lookup"><span data-stu-id="8cc24-107">[Browse a record of all the resource requests](#network-summary) made by the page</span></span>
 - <span data-ttu-id="8cc24-108">[Medir el tiempo de carga de su sitio](#summary-bar) para los usuarios nuevos y devueltos</span><span class="sxs-lookup"><span data-stu-id="8cc24-108">[Measure the load time of your site](#summary-bar) for new and returning users</span></span> 
 - <span data-ttu-id="8cc24-109">[Inspeccionar los encabezados, los cuerpos de los mensajes, los parámetros y las cookies](#request-details) intercambiados entre la página y la red</span><span class="sxs-lookup"><span data-stu-id="8cc24-109">[Inspect the headers, message bodies, parameters, and cookies](#request-details) exchanged between your page and the network</span></span>
 - <span data-ttu-id="8cc24-110">[Identificar los eventos de red que causan cuellos de botella](#timings) en el tiempo de carga de su sitio</span><span class="sxs-lookup"><span data-stu-id="8cc24-110">[Identify the network events causing bottlenecks](#timings) in the load time of your site</span></span>

![Panel de red de Microsoft Edge DevTools](./media/network.png)

## <span data-ttu-id="8cc24-112">Resumen de red</span><span class="sxs-lookup"><span data-stu-id="8cc24-112">Network summary</span></span>

<span data-ttu-id="8cc24-113">Al abrir DevTools, la generación de perfiles de red está activada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8cc24-113">When you open  DevTools, network profiling is turned on by default.</span></span> <span data-ttu-id="8cc24-114">Todo el tráfico de red de la ficha del explorador activo se registra en la lista de Resumen de la red, incluso mientras se trabaja en un panel de DevTools diferente del de la *red*.</span><span class="sxs-lookup"><span data-stu-id="8cc24-114">All the network traffic from your active browser tab is recorded in the network summary list, even while you are working in a different  DevTools panel than *Network*.</span></span>

![Indicador de Perfil de red en curso](./media/network_profile_indicator.png)

### <span data-ttu-id="8cc24-116">Barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="8cc24-116">Toolbar</span></span>

<span data-ttu-id="8cc24-117">La barra de herramientas proporciona controles para generar perfiles y filtrar la actividad de la red de la página.</span><span class="sxs-lookup"><span data-stu-id="8cc24-117">The toolbar provides controls for profiling and filtering the network activity of your page.</span></span> 

![Barra de herramientas de Network Profiler](./media/network_toolbar.png)

1. <span data-ttu-id="8cc24-119">**Iniciar o detener sesión de generación de perfiles**: de forma predeterminada, la generación de perfiles de red está activada y el tráfico de red se registrará en la lista del [**generador de perfiles de red**](#network-request-list) .</span><span class="sxs-lookup"><span data-stu-id="8cc24-119">**Start / Stop profiling session**: By default, network profiling is turned on, and network traffic will be logged in the [**Network profiler**](#network-request-list) list.</span></span> <span data-ttu-id="8cc24-120">Puede desactivar la captura de red con el botón **detener** ( `Ctrl+E` ).</span><span class="sxs-lookup"><span data-stu-id="8cc24-120">You can turn off network capture with the **Stop** (`Ctrl+E`) button.</span></span>

2. <span data-ttu-id="8cc24-121">**Exportar como Har**: puede guardar la sesión de perfilamiento de red actual ( `Ctrl+S` ) como un archivo [http Archive (har)](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/HAR/Overview.html) con formato JSON.</span><span class="sxs-lookup"><span data-stu-id="8cc24-121">**Export as HAR**: You can save the current network profiling session (`Ctrl+S`) as a JSON-formatted [HTTP Archive (HAR)](https://dvcs.w3.org/hg/webperf/raw-file/tip/specs/HAR/Overview.html) file.</span></span> 

3. <span data-ttu-id="8cc24-122">**Filtro de tipo de contenido**: Filtre la lista de solicitudes de red por solicitudes de contenido específicas (*documentos, hojas de estilos, imágenes, scripts, multimedia, fuentes, XHR, otros*).</span><span class="sxs-lookup"><span data-stu-id="8cc24-122">**Content type filter**: Filter the network request list by specific content requests (*Documents, Style sheets, Images, Scripts, Media, Fonts, XHR, Other*).</span></span> <span data-ttu-id="8cc24-123">De forma predeterminada, se muestran todos los tipos de contenido.</span><span class="sxs-lookup"><span data-stu-id="8cc24-123">By default all content types are shown.</span></span>

4. <span data-ttu-id="8cc24-124">**Buscar**: filtrar ( `Ctrl+F` ) la lista de solicitudes de red por nombres de entrada (rutas de recursos) que contienen una cadena de búsqueda especificada.</span><span class="sxs-lookup"><span data-stu-id="8cc24-124">**Find**: Filter (`Ctrl+F`) the network request list by entry names (resource paths) containing a specified search string.</span></span>

5. <span data-ttu-id="8cc24-125">**Actualizar siempre desde el servidor**: al presionar este botón, los recursos de página se cargarán desde la red en lugar de la caché del explorador.</span><span class="sxs-lookup"><span data-stu-id="8cc24-125">**Always refresh from server**: Depressing this button will force page resources to load from the network rather than the browser cache.</span></span> <span data-ttu-id="8cc24-126">Puede actualizar la página desde la red una sola vez pulsando `Ctrl+F5` .</span><span class="sxs-lookup"><span data-stu-id="8cc24-126">You can refresh the page from  network a single time by pressing `Ctrl+F5`.</span></span>

6. <span data-ttu-id="8cc24-127">**Omitir trabajo de servicio para todas las solicitudes de red**: deshabilite los trabajadores de servicio registrados como proxies de red.</span><span class="sxs-lookup"><span data-stu-id="8cc24-127">**Bypass Service Worker for all network requests**: Disable your registered service workers as network proxies.</span></span> 

7. <span data-ttu-id="8cc24-128">Borrar botones</span><span class="sxs-lookup"><span data-stu-id="8cc24-128">Clear buttons</span></span>

   - <span data-ttu-id="8cc24-129">**Borrar caché**: quita todos los recursos almacenados en la memoria caché del explorador (y emula una experiencia de primera vez que cargue la página).</span><span class="sxs-lookup"><span data-stu-id="8cc24-129">**Clear cache**: Removes all resources stored in the browser cache (and emulates a first-time experience loading the page).</span></span>
   - <span data-ttu-id="8cc24-130">**Borrar Cookies**: quita todas las cookies para el dominio dado (y emula una experiencia de primera hora del sitio).</span><span class="sxs-lookup"><span data-stu-id="8cc24-130">**Clear cookies**: Removes all cookies for the given domain (and emulates a first-time experience of the site).</span></span>
   - <span data-ttu-id="8cc24-131">**Borrar las entradas en**la navegación: el tráfico grabado se borra con la navegación de la página.</span><span class="sxs-lookup"><span data-stu-id="8cc24-131">**Clear entries on navigate**: Recorded traffic is cleared upon page navigation.</span></span> <span data-ttu-id="8cc24-132">Esta opción está activada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="8cc24-132">This is turned on by default.</span></span>
   - <span data-ttu-id="8cc24-133">**Borrar sesión**: borra todas las entradas de solicitud de red de la lista de **Resumen de red** .</span><span class="sxs-lookup"><span data-stu-id="8cc24-133">**Clear session**: Clears all network request entries from the **Network summary** list.</span></span>

### <span data-ttu-id="8cc24-134">Lista de solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="8cc24-134">Network request list</span></span>

<span data-ttu-id="8cc24-135">Todo el tráfico de red se graba en una lista (hasta que se borra la navegación, la desactivación manual o DevTools se cierran).</span><span class="sxs-lookup"><span data-stu-id="8cc24-135">All network traffic is recorded to a list (until cleared upon navigation, manually cleared, or  DevTools are closed).</span></span> <span data-ttu-id="8cc24-136">Al hacer clic en cualquier entrada, se abrirá una [vista más detallada de la solicitud](#request-details).</span><span class="sxs-lookup"><span data-stu-id="8cc24-136">Clicking on any entry will open a more [detailed view of the request](#request-details).</span></span>

![Lista de solicitudes de red](./media/network_request_list.png)

<span data-ttu-id="8cc24-138">La lista de solicitudes de red incluye la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="8cc24-138">The network request list includes the following info:</span></span> 

<span data-ttu-id="8cc24-139">Columna</span><span class="sxs-lookup"><span data-stu-id="8cc24-139">Column</span></span> | <span data-ttu-id="8cc24-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="8cc24-140">Description</span></span> 
:------------ | :------------- 
**<span data-ttu-id="8cc24-141">Name</span><span class="sxs-lookup"><span data-stu-id="8cc24-141">Name</span></span>** | <span data-ttu-id="8cc24-142">Nombre y dirección URL de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8cc24-142">Name and URL path of the request</span></span>
**<span data-ttu-id="8cc24-143">Protocolo</span><span class="sxs-lookup"><span data-stu-id="8cc24-143">Protocol</span></span>** |  <span data-ttu-id="8cc24-144">Tipo de protocolo para la solicitud (como *https, http/2*)</span><span class="sxs-lookup"><span data-stu-id="8cc24-144">Type of protocol for the request (such as *HTTPS, HTTP/2*)</span></span>
**<span data-ttu-id="8cc24-145">Método</span><span class="sxs-lookup"><span data-stu-id="8cc24-145">Method</span></span>** |    <span data-ttu-id="8cc24-146">[Método http](https://developer.mozilla.org/docs/Web/HTTP/Methods) usado para la solicitud</span><span class="sxs-lookup"><span data-stu-id="8cc24-146">[HTTP method](https://developer.mozilla.org/docs/Web/HTTP/Methods) used for the request</span></span>
**<span data-ttu-id="8cc24-147">Resultado</span><span class="sxs-lookup"><span data-stu-id="8cc24-147">Result</span></span>** |    <span data-ttu-id="8cc24-148">Código de [Estado de respuesta http](https://developer.mozilla.org/docs/Web/HTTP/Status)</span><span class="sxs-lookup"><span data-stu-id="8cc24-148">[HTTP response status](https://developer.mozilla.org/docs/Web/HTTP/Status)  code</span></span>
**<span data-ttu-id="8cc24-149">Tipo de contenido</span><span class="sxs-lookup"><span data-stu-id="8cc24-149">Content type</span></span>** |  <span data-ttu-id="8cc24-150">Tipo de medios solicitado ([tipo MIME](https://en.wikipedia.org/wiki/Media_type))</span><span class="sxs-lookup"><span data-stu-id="8cc24-150">Type of media requested ([MIME type](https://en.wikipedia.org/wiki/Media_type))</span></span>
**<span data-ttu-id="8cc24-151">Recibido</span><span class="sxs-lookup"><span data-stu-id="8cc24-151">Received</span></span>** | <span data-ttu-id="8cc24-152">Tamaño de la respuesta tal y como lo proporciona el servidor (no se calcula para las respuestas almacenadas en caché)</span><span class="sxs-lookup"><span data-stu-id="8cc24-152">Size of the response as delivered by the server (not calculated for cached responses)</span></span>
**<span data-ttu-id="8cc24-153">Tiempo</span><span class="sxs-lookup"><span data-stu-id="8cc24-153">Time</span></span>** |  <span data-ttu-id="8cc24-154">Tiempo para cargar la respuesta del servidor (no se calcula para las respuestas almacenadas en caché)</span><span class="sxs-lookup"><span data-stu-id="8cc24-154">Time to load the server response (not calculated for cached responses)</span></span>
**<span data-ttu-id="8cc24-155">Inició</span><span class="sxs-lookup"><span data-stu-id="8cc24-155">Initiator</span></span>** | <span data-ttu-id="8cc24-156">Subsistema responsable de iniciar la solicitud (como *analizador, redirección, script, otro*)</span><span class="sxs-lookup"><span data-stu-id="8cc24-156">Subsystem responsible for initiating the request (such as *Parser, Redirect, Script, Other*)</span></span>
**<span data-ttu-id="8cc24-157">Línea de tiempo</span><span class="sxs-lookup"><span data-stu-id="8cc24-157">Timeline</span></span>** | <span data-ttu-id="8cc24-158">Escala de tiempo visual para los eventos de red de la solicitud (como *bloqueados, resolver (DNS), conexiones (TCP), SSL, envío, espera (TTFB), descargar*).</span><span class="sxs-lookup"><span data-stu-id="8cc24-158">Visual timeline for the network events of the request (such as *Stalled, Resolving(DNS), Connecting(TCP), SSL, Sending, Waiting(TTFB), Downloading*).</span></span> <span data-ttu-id="8cc24-159">Situar el puntero sobre el gráfico proporciona un desglose más granular de los [intervalos de red](#timings)de red).</span><span class="sxs-lookup"><span data-stu-id="8cc24-159">Hovering over the chart provides the more granular breakdown of network [network timings](#timings)).</span></span>

### <span data-ttu-id="8cc24-160">Barra de Resumen</span><span class="sxs-lookup"><span data-stu-id="8cc24-160">Summary bar</span></span>

<span data-ttu-id="8cc24-161">La barra de la parte inferior del panel **red** resume el número total de errores de red http, solicitudes, datos transferidos y tiempos de carga durante la sesión de perfilamiento de red (es decir, porque DevTools se abrieron y grabaron tráfico de red).</span><span class="sxs-lookup"><span data-stu-id="8cc24-161">The bar at the bottom of **Network** panel summarizes the total number of HTTP network errors, requests, data transfered, and load times during the network profiling session (i.e., since  DevTools were opened and recording network traffic).</span></span>

![Barra de Resumen de red](./media/network_summary_bar.png)

<span data-ttu-id="8cc24-163">**Tiempo transcurrido** significa el tiempo entre el inicio de la sesión de generación de perfiles y el último recurso que se ha descargado de la red.</span><span class="sxs-lookup"><span data-stu-id="8cc24-163">**Elapsed time** means the time between the start of the profiling session and when the last resource was downloaded from the network.</span></span> <span data-ttu-id="8cc24-164">Los recursos que se capturan desde la caché del explorador no acumulan tiempo para este número.</span><span class="sxs-lookup"><span data-stu-id="8cc24-164">Resources fetched from the browser cache do not accrue time to this number.</span></span> 

<span data-ttu-id="8cc24-165">**Dom Load Time** significa el tiempo entre el inicio de la sesión de generación de perfiles y cuando se desencadena el evento [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded) para indicar que se ha cargado y analizado la estructura del documento de página (aunque no necesariamente ninguna hoja de estilos, imágenes o submarcos).</span><span class="sxs-lookup"><span data-stu-id="8cc24-165">**DOM load time** means the time between the start of the profiling session and when the [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded) event was fired to indicate that the structure of the page document has been loaded and parsed (though not necessarily any stylesheets, images or subframes).</span></span>

<span data-ttu-id="8cc24-166">Tiempo de carga de la **Página** significa el tiempo entre el inicio de la sesión de generación de perfiles y el momento en que se activó el evento de [carga](https://developer.mozilla.org/docs/Web/Events/load) para indicar que el documento de página (y todos sus recursos) se ha cargado por completo.</span><span class="sxs-lookup"><span data-stu-id="8cc24-166">**Page load time** time means the time between the start of the profiling session and when the [load](https://developer.mozilla.org/docs/Web/Events/load) event was fired to indicate that the page document (and all its resources) has been fully loaded.</span></span>

## <span data-ttu-id="8cc24-167">Detalles de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8cc24-167">Request details</span></span>

<span data-ttu-id="8cc24-168">Al hacer clic en cualquier entrada de la lista de [**Resumen de red**](#network-summary) , se abrirá el panel de detalles de la [**solicitud**](#request-details) con más información en cada una de las siguientes pestañas.</span><span class="sxs-lookup"><span data-stu-id="8cc24-168">Clicking on any entry in the [**Network summary**](#network-summary) list will open the [**Request details**](#request-details) pane with further information in each of the following tabs.</span></span>

![Panel de detalles de solicitud de red](./media/network_request_details.png)

### <span data-ttu-id="8cc24-170">Encabezados</span><span class="sxs-lookup"><span data-stu-id="8cc24-170">Headers</span></span>
<span data-ttu-id="8cc24-171">Muestra los [encabezados HTTP](https://developer.mozilla.org/docs/Web/HTTP/Headers) enviados y recibidos desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="8cc24-171">Displays the [HTTP headers](https://developer.mozilla.org/docs/Web/HTTP/Headers) sent to and received from the server.</span></span> <span data-ttu-id="8cc24-172">Haga clic con el botón derecho en cualquier entrada de encabezado para copiarla ( `Ctrl+C` ) en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="8cc24-172">Right-click on any header entry to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="8cc24-173">También puede seleccionar varias entradas manteniendo presionada la `Shift` tecla o seleccionar todo ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="8cc24-173">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

### <span data-ttu-id="8cc24-174">Body</span><span class="sxs-lookup"><span data-stu-id="8cc24-174">Body</span></span>
<span data-ttu-id="8cc24-175">Muestra los datos de cuerpo (si están disponibles) de las cargas de solicitud y respuesta.</span><span class="sxs-lookup"><span data-stu-id="8cc24-175">Displays the body data (if available) of the request and response payloads.</span></span>

<span data-ttu-id="8cc24-176">El contenido de la imagen se muestra con datos de tamaño y dimensiones.</span><span class="sxs-lookup"><span data-stu-id="8cc24-176">Image content is displayed with dimensions and size data.</span></span>

<span data-ttu-id="8cc24-177">El contenido de texto aparece en un editor (de solo lectura) con opciones para dar formato al contenido de minified con la **impresión** o el **ajuste** de texto, para facilitar la lectura.</span><span class="sxs-lookup"><span data-stu-id="8cc24-177">Text content appears in a (read-only) editor with options to format minified content with **Pretty print** and/or **Word wrap** for easier readability.</span></span>

![Pestaña cuerpo del panel Detalles de la solicitud](./media/network_details_body.png)

### <span data-ttu-id="8cc24-179">Parameters</span><span class="sxs-lookup"><span data-stu-id="8cc24-179">Parameters</span></span>
<span data-ttu-id="8cc24-180">Muestra parámetros de cadena de consulta para solicitudes GET.</span><span class="sxs-lookup"><span data-stu-id="8cc24-180">Displays query string parameters for GET requests.</span></span> <span data-ttu-id="8cc24-181">Aunque los parámetros de las solicitudes POST se envían en los encabezados, las solicitudes GET las incluyen en la URL.</span><span class="sxs-lookup"><span data-stu-id="8cc24-181">While the parameters of POST requests are sent in the headers, GET requests include them in the URL.</span></span> <span data-ttu-id="8cc24-182">Se desglosan aquí para facilitar la lectura.</span><span class="sxs-lookup"><span data-stu-id="8cc24-182">They're broken out here for easier reading.</span></span>

<span data-ttu-id="8cc24-183">Haga clic con el botón derecho en cualquier fila para copiarla ( `Ctrl+C` ) al portapapeles.</span><span class="sxs-lookup"><span data-stu-id="8cc24-183">Right-click on any row to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="8cc24-184">También puede seleccionar varias entradas manteniendo presionada la `Shift` tecla o seleccionar todo ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="8cc24-184">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

### <span data-ttu-id="8cc24-185">Cookies</span><span class="sxs-lookup"><span data-stu-id="8cc24-185">Cookies</span></span>
<span data-ttu-id="8cc24-186">Muestra las cookies enviadas o recibidas como pares de clave y valor.</span><span class="sxs-lookup"><span data-stu-id="8cc24-186">Displays cookies that are sent or received as key/value pairs.</span></span>

<span data-ttu-id="8cc24-187">Haga clic con el botón derecho en cualquier fila para copiarla ( `Ctrl+C` ) al portapapeles.</span><span class="sxs-lookup"><span data-stu-id="8cc24-187">Right-click on any row to copy it (`Ctrl+C`) to the clipboard.</span></span> <span data-ttu-id="8cc24-188">También puede seleccionar varias entradas manteniendo presionada la `Shift` tecla o seleccionar todo ( `Ctrl+A` ).</span><span class="sxs-lookup"><span data-stu-id="8cc24-188">You can also multi-select entries by holding down the `Shift` key or select all (`Ctrl+A`).</span></span>

<span data-ttu-id="8cc24-189">Puede borrar las cookies almacenadas para el dominio dado de la [barra de herramientas](#network-summary) (botón**Borrar Cookies** ).</span><span class="sxs-lookup"><span data-stu-id="8cc24-189">You can clear the stored cookies for the given domain from the [Toolbar](#network-summary) (**Clear cookies** button).</span></span> 

### <span data-ttu-id="8cc24-190">Intervalos</span><span class="sxs-lookup"><span data-stu-id="8cc24-190">Timings</span></span>

<span data-ttu-id="8cc24-191">La pestaña **intervalos** proporciona una escala de tiempo de eventos de red implicados en la carga del recurso seleccionado.</span><span class="sxs-lookup"><span data-stu-id="8cc24-191">The **Timings** tab provides a timeline of network events involved in the loading of the selected resource.</span></span> <span data-ttu-id="8cc24-192">Es similar a la información que se encuentra en la columna *escala de tiempo* de la lista de [solicitudes de red](#network-request-list), pero también incluye los eventos que llevan a la solicitud enviada a través de la conexión, como el tiempo invertido en espera (*detenido*) en la cola de solicitudes, la resolución DNS y el establecimiento de la conexión TCP.</span><span class="sxs-lookup"><span data-stu-id="8cc24-192">This is similar to the information found in the *Timeline* column of the [Network request list](#network-request-list), but also includes the events leading up to the request being sent over the wire, such as time spent waiting (*Stalled*) in the request queue, DNS resolution, and establishing the TCP connection.</span></span> 

![Pestaña intervalos del panel Detalles de la solicitud](./media/network_details_timings.png)

<span data-ttu-id="8cc24-194">Se indican redireccionamientos a/desde otros recursos y al hacer clic en el vínculo se establece el foco en ese recurso en el panel de [detalles de solicitud](#request details) de red.</span><span class="sxs-lookup"><span data-stu-id="8cc24-194">Redirections to/from other resources are noted, and clicking on the link will set focus to that resource in the network [request details](#request details) pane.</span></span>

<span data-ttu-id="8cc24-195">Los recursos cargados desde la caché no se ven afectados por la latencia de red, por lo que no se mostrará ningún gráfico de *intervalos* de red.</span><span class="sxs-lookup"><span data-stu-id="8cc24-195">Resouces loaded from the cache are not affected by network latency, so no network *Timings* chart will display.</span></span>

![Recurso Redirigido cargado desde la caché](./media/network_details_timings_cache_redirect.png)

<span data-ttu-id="8cc24-197">Estos son los distintos eventos de red que puede ver para un recurso determinado, en orden cronológico:</span><span class="sxs-lookup"><span data-stu-id="8cc24-197">Here are the different network events you might see for a given resource, in chronological order:</span></span>

#### <span data-ttu-id="8cc24-198">Paralizado</span><span class="sxs-lookup"><span data-stu-id="8cc24-198">Stalled</span></span>

<span data-ttu-id="8cc24-199">Tiempo invertido esperando una conexión de red disponible en la cola de solicitudes.</span><span class="sxs-lookup"><span data-stu-id="8cc24-199">Time spent waiting for an available network connection in the request queue.</span></span> <span data-ttu-id="8cc24-200">Para HTTP 1.0/1.1, Microsoft Edge permite un máximo de seis (6) conexiones TCP simultáneas por nombre de host.</span><span class="sxs-lookup"><span data-stu-id="8cc24-200">For HTTP 1.0/1.1, Microsoft Edge allows a maximum of six (6) simultaneous TCP connections per hostname.</span></span> 

#### <span data-ttu-id="8cc24-201">Resolver (DNS)</span><span class="sxs-lookup"><span data-stu-id="8cc24-201">Resolving (DNS)</span></span>

<span data-ttu-id="8cc24-202">Tiempo dedicado a buscar la dirección IP del nombre de host del recurso en el DNS ([sistema de nombres de dominio](https://en.wikipedia.org/wiki/Domain_Name_System)).</span><span class="sxs-lookup"><span data-stu-id="8cc24-202">Time spent looking up the IP address for the hostname of the resource in the DNS ([Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System)).</span></span>

#### <span data-ttu-id="8cc24-203">Conexión (TCP)</span><span class="sxs-lookup"><span data-stu-id="8cc24-203">Connecting (TCP)</span></span>

<span data-ttu-id="8cc24-204">Tiempo empleado en establecer la conexión TCP ([Protocolo de control de transmisión](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)).</span><span class="sxs-lookup"><span data-stu-id="8cc24-204">Time spent establishing the TCP ([Transmission Control Protocol](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)) connection.</span></span>

#### <span data-ttu-id="8cc24-205">SSL</span><span class="sxs-lookup"><span data-stu-id="8cc24-205">SSL</span></span>

<span data-ttu-id="8cc24-206">Tiempo invertido en la negociación de una conexión SSL ([capa de sockets seguros](https://en.wikipedia.org/wiki/Transport_Layer_Security)) con el [servidor proxy](https://en.wikipedia.org/wiki/Proxy_server) para el host.</span><span class="sxs-lookup"><span data-stu-id="8cc24-206">Time spent negotiating a SSL ([Secure Sockets Layer](https://en.wikipedia.org/wiki/Transport_Layer_Security))  connection with the [proxy server](https://en.wikipedia.org/wiki/Proxy_server) for the host.</span></span>

#### <span data-ttu-id="8cc24-207">Remitente</span><span class="sxs-lookup"><span data-stu-id="8cc24-207">Sending</span></span>

<span data-ttu-id="8cc24-208">Tiempo empleado en enviar la solicitud de recursos.</span><span class="sxs-lookup"><span data-stu-id="8cc24-208">Time spent sending the resource request.</span></span>

#### <span data-ttu-id="8cc24-209">Esperando (TTFB)</span><span class="sxs-lookup"><span data-stu-id="8cc24-209">Waiting (TTFB)</span></span>

<span data-ttu-id="8cc24-210">Tiempo dedicado a esperar el primer byte de la respuesta del servidor host ("tiempo en el primer byte" o *TTFB*).</span><span class="sxs-lookup"><span data-stu-id="8cc24-210">Time spent waiting for the first byte of the response from the host server ("time to first byte", or *TTFB*).</span></span>

#### <span data-ttu-id="8cc24-211">Descargar</span><span class="sxs-lookup"><span data-stu-id="8cc24-211">Downloading</span></span>

<span data-ttu-id="8cc24-212">Tiempo dedicado a leer la respuesta del servidor.</span><span class="sxs-lookup"><span data-stu-id="8cc24-212">Time spent reading the response from the server.</span></span>

## <span data-ttu-id="8cc24-213">Abreviados</span><span class="sxs-lookup"><span data-stu-id="8cc24-213">Shortcuts</span></span>

| <span data-ttu-id="8cc24-214">Acción</span><span class="sxs-lookup"><span data-stu-id="8cc24-214">Action</span></span>                         | <span data-ttu-id="8cc24-215">Método abreviado</span><span class="sxs-lookup"><span data-stu-id="8cc24-215">Shortcut</span></span>     |
|:-------------------------------|:-------------|
| <span data-ttu-id="8cc24-216">Iniciar o detener sesión de generación de perfiles</span><span class="sxs-lookup"><span data-stu-id="8cc24-216">Start / Stop profiling session</span></span> | `Ctrl` + `E` |
| <span data-ttu-id="8cc24-217">Exportar como HAR</span><span class="sxs-lookup"><span data-stu-id="8cc24-217">Export as HAR</span></span>                  | `Ctrl` + `S` |
| <span data-ttu-id="8cc24-218">Buscar</span><span class="sxs-lookup"><span data-stu-id="8cc24-218">Find</span></span>                           | `Ctrl` + `F` |
| <span data-ttu-id="8cc24-219">Copiar</span><span class="sxs-lookup"><span data-stu-id="8cc24-219">Copy</span></span>                           | `Ctrl` + `C` |

## <span data-ttu-id="8cc24-220">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="8cc24-220">Known Issues</span></span>

### <span data-ttu-id="8cc24-221">Error al iniciar el agente de recopilación de redes.</span><span class="sxs-lookup"><span data-stu-id="8cc24-221">The network collection agent failed to start.</span></span>

<span data-ttu-id="8cc24-222">Si ve este mensaje de error: **el agente de recopilación de redes no se pudo iniciar** en la herramienta red, siga estos pasos para obtener una solución alternativa.</span><span class="sxs-lookup"><span data-stu-id="8cc24-222">If you see this error message: **The network collection agent failed to start** in the Network tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="8cc24-223">Presione `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="8cc24-223">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="8cc24-224">En el cuadro de diálogo Ejecutar, escriba **Services. msc**.</span><span class="sxs-lookup"><span data-stu-id="8cc24-224">In the Run dialog, enter **services.msc**.</span></span>
![problemas conocidos-1](./media/known_issues_1.PNG)

3. <span data-ttu-id="8cc24-226">Busque el **servicio Recopilador estándar de Microsoft (R) Diagnostics Hub** y haga clic en él con el botón secundario del ratón.</span><span class="sxs-lookup"><span data-stu-id="8cc24-226">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![problemas conocidos-2](./media/known_issues_2.PNG)

4. <span data-ttu-id="8cc24-228">Reinicie el **servicio Recopilador estándar del concentrador de diagnósticos de Microsoft (R)**.</span><span class="sxs-lookup"><span data-stu-id="8cc24-228">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![problemas conocidos-3](./media/known_issues_3.PNG)

5. <span data-ttu-id="8cc24-230">Cierre las herramientas para desarrolladores de Microsoft Edge y la pestaña. Abra una nueva pestaña, vaya a la página y presione `F12` .</span><span class="sxs-lookup"><span data-stu-id="8cc24-230">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="8cc24-231">Ahora debe ver un distintivo de la reproducción junto a **red** y las solicitudes de red para su página web.</span><span class="sxs-lookup"><span data-stu-id="8cc24-231">You should now see a Play badge next to **Network** and the network requests for your webpage.</span></span>
![problemas conocidos-4](./media/known_issues_4-network.PNG)

<span data-ttu-id="8cc24-233">¿Aún tiene problemas?</span><span class="sxs-lookup"><span data-stu-id="8cc24-233">Still running into problems?</span></span> <span data-ttu-id="8cc24-234">Envíenos sus comentarios con el icono para **Enviar comentarios** .</span><span class="sxs-lookup"><span data-stu-id="8cc24-234">Please send us your feedback using the **Send feedback** icon!</span></span> 

![problemas conocidos-5](./media/known_issues_5.PNG)

### <span data-ttu-id="8cc24-236">No se pudo detener el agente de recopilación de redes.</span><span class="sxs-lookup"><span data-stu-id="8cc24-236">The network collection agent failed to stop.</span></span>

<span data-ttu-id="8cc24-237">Si ve este mensaje de error: **el agente de recopilación de redes no se pudo detener** en la herramienta red, siga estos pasos para obtener una solución alternativa.</span><span class="sxs-lookup"><span data-stu-id="8cc24-237">If you see this error message: **The network collection agent failed to stop** in the Network tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="8cc24-238">Presione `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="8cc24-238">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="8cc24-239">En el cuadro de diálogo Ejecutar, escriba **Services. msc**.</span><span class="sxs-lookup"><span data-stu-id="8cc24-239">In the Run dialog, enter **services.msc**.</span></span>
![problemas conocidos-1](./media/known_issues_1.PNG)

3. <span data-ttu-id="8cc24-241">Busque el **servicio Recopilador estándar de Microsoft (R) Diagnostics Hub** y haga clic en él con el botón secundario del ratón.</span><span class="sxs-lookup"><span data-stu-id="8cc24-241">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![problemas conocidos-2](./media/known_issues_2.PNG)

4. <span data-ttu-id="8cc24-243">Reinicie el **servicio Recopilador estándar del concentrador de diagnósticos de Microsoft (R)**.</span><span class="sxs-lookup"><span data-stu-id="8cc24-243">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![problemas conocidos-3](./media/known_issues_3.PNG)

5. <span data-ttu-id="8cc24-245">Cierre las herramientas para desarrolladores de Microsoft Edge y la pestaña. Abra una nueva pestaña, vaya a la página y presione `F12` .</span><span class="sxs-lookup"><span data-stu-id="8cc24-245">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="8cc24-246">Ahora debe ver un distintivo de la reproducción junto a **red** y las solicitudes de red para su página web.</span><span class="sxs-lookup"><span data-stu-id="8cc24-246">You should now see a Play badge next to **Network** and the network requests for your webpage.</span></span>
![problemas conocidos-4](./media/known_issues_4-network.PNG)

<span data-ttu-id="8cc24-248">¿Aún tiene problemas?</span><span class="sxs-lookup"><span data-stu-id="8cc24-248">Still running into problems?</span></span> <span data-ttu-id="8cc24-249">Envíenos sus comentarios con el icono para **Enviar comentarios** .</span><span class="sxs-lookup"><span data-stu-id="8cc24-249">Please send us your feedback using the **Send feedback** icon!</span></span> 

![problemas conocidos-5](./media/known_issues_5.PNG)

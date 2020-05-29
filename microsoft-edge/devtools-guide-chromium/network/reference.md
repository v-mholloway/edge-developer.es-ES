---
title: Referencia de análisis de red
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 460ad05983e7615e8739953ce3cb7d559492bc90
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611843"
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







# <span data-ttu-id="2be45-103">Referencia de análisis de red</span><span class="sxs-lookup"><span data-stu-id="2be45-103">Network Analysis Reference</span></span>   



<span data-ttu-id="2be45-104">Descubra nuevas formas de analizar cómo se carga su página en esta referencia completa de las características de análisis de red de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="2be45-104">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## <span data-ttu-id="2be45-105">Registrar solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="2be45-105">Record network requests</span></span>   

<span data-ttu-id="2be45-106">De forma predeterminada, DevTools registra todas las solicitudes de red en el panel red, siempre y cuando DevTools esté abierto.</span><span class="sxs-lookup"><span data-stu-id="2be45-106">By default, DevTools records all network requests in the Network panel, so long as DevTools is open.</span></span>  

> ##### <span data-ttu-id="2be45-107">Figura 1</span><span class="sxs-lookup"><span data-stu-id="2be45-107">Figure 1</span></span>  
> <span data-ttu-id="2be45-108">Panel red</span><span class="sxs-lookup"><span data-stu-id="2be45-108">The Network panel</span></span>  
> ![Panel red][ImageNetworkPanel]  

### <span data-ttu-id="2be45-110">Detener la grabación de solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="2be45-110">Stop recording network requests</span></span>   

<span data-ttu-id="2be45-111">Para detener la grabación de solicitudes:</span><span class="sxs-lookup"><span data-stu-id="2be45-111">To stop recording requests:</span></span>  

*   <span data-ttu-id="2be45-112">Seleccione **Detener grabación registro de red** ![ detener la grabación del registro ][ImageRecordOnIcon] de red en el panel **red** .</span><span class="sxs-lookup"><span data-stu-id="2be45-112">Select **Stop recording network log** ![Stop recording network log][ImageRecordOnIcon] on the **Network** panel.</span></span>  <span data-ttu-id="2be45-113">Se vuelve gris para indicar que DevTools ya no graba solicitudes.</span><span class="sxs-lookup"><span data-stu-id="2be45-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
*   <span data-ttu-id="2be45-114">Pulse `Control` + `E` \ (Windows \) o `Command` + `E` \ (MacOS \) mientras el panel **red** está en el foco.</span><span class="sxs-lookup"><span data-stu-id="2be45-114">Press `Control`+`E` \(Windows\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="2be45-115">Borrar solicitudes</span><span class="sxs-lookup"><span data-stu-id="2be45-115">Clear requests</span></span>   

<span data-ttu-id="2be45-116">Seleccione **Borrar** ![ Borrar ][ImageClearIcon] en el panel red para borrar todas las solicitudes de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="2be45-116">Select **Clear** ![Clear][ImageClearIcon] on the Network panel to clear all requests from the Requests table.</span></span>  

> ##### <span data-ttu-id="2be45-117">Figura 2</span><span class="sxs-lookup"><span data-stu-id="2be45-117">Figure 2</span></span>  
> <span data-ttu-id="2be45-118">Botón borrar</span><span class="sxs-lookup"><span data-stu-id="2be45-118">The Clear button</span></span>  
> ![Botón borrar][ImageClearButton]  

### <span data-ttu-id="2be45-120">Guardar solicitudes en la carga de páginas</span><span class="sxs-lookup"><span data-stu-id="2be45-120">Save requests across page loads</span></span>   

<span data-ttu-id="2be45-121">Para guardar las solicitudes en la carga de la página, active la casilla **conservar registro** en el panel red.</span><span class="sxs-lookup"><span data-stu-id="2be45-121">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="2be45-122">DevTools guarda todas las solicitudes hasta que Deshabilites **conservar registro**.</span><span class="sxs-lookup"><span data-stu-id="2be45-122">DevTools saves all requests until you disable **Preserve log**.</span></span>  

> ##### <span data-ttu-id="2be45-123">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="2be45-123">Figure 3</span></span>  
> <span data-ttu-id="2be45-124">Casilla de verificación conservar registro</span><span class="sxs-lookup"><span data-stu-id="2be45-124">The Preserve Log checkbox</span></span>  
> ![Casilla de verificación conservar registro][ImagePreserveLogCheckBox]  

### <span data-ttu-id="2be45-126">Capturar capturas de pantallas durante la carga de la página</span><span class="sxs-lookup"><span data-stu-id="2be45-126">Capture screenshots during page load</span></span>   

<span data-ttu-id="2be45-127">Capture las capturas de pantallas para analizar lo que los usuarios ven al esperar a que se cargue la página.</span><span class="sxs-lookup"><span data-stu-id="2be45-127">Capture screenshots to analyze what users see as they wait for your page to load.</span></span>  

<span data-ttu-id="2be45-128">Para habilitar capturas de pantalla, seleccione **configuración de red** y marque la casilla **capturar capturas** de pantalla en el panel **red** .</span><span class="sxs-lookup"><span data-stu-id="2be45-128">To enable screenshots, select **Network settings** and select **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="2be45-129">Vuelva a cargar la página mientras el panel **red** está en el foco para capturar capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="2be45-129">Reload the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="2be45-130">Después de capturar una captura de pantalla, puede interactuar con ella de las siguientes maneras.</span><span class="sxs-lookup"><span data-stu-id="2be45-130">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="2be45-131">Desplace el puntero sobre una captura de pantalla para ver el punto en el que se capturó la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="2be45-131">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="2be45-132">Aparece una línea amarilla en el panel de **información general** .</span><span class="sxs-lookup"><span data-stu-id="2be45-132">A yellow line appears on the **Overview** pane.</span></span>  
*   <span data-ttu-id="2be45-133">Seleccione la miniatura de una pantalla para filtrar las solicitudes que se produjeron después de que se capturó la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="2be45-133">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="2be45-134">Haga doble clic en una miniatura para acercarla.</span><span class="sxs-lookup"><span data-stu-id="2be45-134">Double-click a thumbnail to zoom in on it.</span></span>  

> ##### <span data-ttu-id="2be45-135">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="2be45-135">Figure 4</span></span>  
> <span data-ttu-id="2be45-136">Colocar el puntero sobre una captura de pantalla</span><span class="sxs-lookup"><span data-stu-id="2be45-136">Hovering over a screenshot</span></span>  
> ![Colocar el puntero sobre una captura de pantalla][ImageScreenshotHover]  

<!--  ### Replay XHR request   -->

<!--  To replay an XHR request, right-click the request in the Requests table and select **Replay XHR**.  -->

<!--  
> ##### Old Figure 5  
> Selecting Replay XHR  
> ![Selecting Replay XHR][ImageReplayXHR]  
-->  

## <span data-ttu-id="2be45-138">Cambiar el comportamiento de carga</span><span class="sxs-lookup"><span data-stu-id="2be45-138">Change loading behavior</span></span>  

### <span data-ttu-id="2be45-139">Emular a un primer visitante mediante la deshabilitación de la memoria caché del explorador</span><span class="sxs-lookup"><span data-stu-id="2be45-139">Emulate a first-time visitor by disabling the browser cache</span></span>   

<span data-ttu-id="2be45-140">Para emular el funcionamiento de su sitio por primera vez, active la casilla **deshabilitar la caché** .</span><span class="sxs-lookup"><span data-stu-id="2be45-140">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="2be45-141">DevTools deshabilita la caché del explorador.</span><span class="sxs-lookup"><span data-stu-id="2be45-141">DevTools disables the browser cache.</span></span>  <span data-ttu-id="2be45-142">Esto emula con más precisión la experiencia de un usuario por primera vez, ya que las solicitudes se proporcionan desde la memoria caché del explorador en las visitas repetidas.</span><span class="sxs-lookup"><span data-stu-id="2be45-142">This more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

> ##### <span data-ttu-id="2be45-143">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="2be45-143">Figure 5</span></span>  
> <span data-ttu-id="2be45-144">Casilla deshabilitar caché</span><span class="sxs-lookup"><span data-stu-id="2be45-144">The Disable Cache checkbox</span></span>  
> <span data-ttu-id="2be45-145">! [Deshabilitar la casilla de la caché] [ImageDisableCacheCheckBox]</span><span class="sxs-lookup"><span data-stu-id="2be45-145">![The Disable Cache checkbox][ImageDisableCacheCheckBox]</span></span>  

#### <span data-ttu-id="2be45-146">Deshabilitar la memoria caché del explorador en el cajón de condiciones de red</span><span class="sxs-lookup"><span data-stu-id="2be45-146">Disable the browser cache from the Network Conditions drawer</span></span>   

<span data-ttu-id="2be45-147">Si desea deshabilitar la caché mientras trabaja en otros paneles de DevTools, use el cajón de condiciones de redes.</span><span class="sxs-lookup"><span data-stu-id="2be45-147">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="2be45-148">Abra el cajón de **condiciones de redes** .</span><span class="sxs-lookup"><span data-stu-id="2be45-148">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="2be45-149">Active o desactive la casilla **deshabilitar caché** .</span><span class="sxs-lookup"><span data-stu-id="2be45-149">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="2be45-150">Borrar manualmente la memoria caché del explorador</span><span class="sxs-lookup"><span data-stu-id="2be45-150">Manually clear the browser cache</span></span>   

<span data-ttu-id="2be45-151">Para borrar manualmente la memoria caché del explorador en cualquier momento, haga clic con el botón secundario en cualquier lugar de la tabla solicitudes y seleccione **Borrar caché del explorador**.</span><span class="sxs-lookup"><span data-stu-id="2be45-151">To manually clear the browser cache at any time, right-click anywhere in the Requests table and select **Clear Browser Cache**.</span></span>  

> ##### <span data-ttu-id="2be45-152">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="2be45-152">Figure 6</span></span>  
> <span data-ttu-id="2be45-153">Selección de borrar caché del explorador</span><span class="sxs-lookup"><span data-stu-id="2be45-153">Selecting Clear Browser Cache</span></span>  
> <span data-ttu-id="2be45-154">! [Seleccionando Borrar caché del explorador] [ImageClearBrowserCache]</span><span class="sxs-lookup"><span data-stu-id="2be45-154">![Selecting Clear Browser Cache][ImageClearBrowserCache]</span></span>  

### <span data-ttu-id="2be45-155">Emular sin conexión</span><span class="sxs-lookup"><span data-stu-id="2be45-155">Emulate offline</span></span>   

<span data-ttu-id="2be45-156">Una nueva clase de aplicaciones Web, llamadas [aplicaciones web progresivas][DevtoolsProgressiveWebApps], funciona sin conexión con la ayuda de los **trabajadores de servicio**.</span><span class="sxs-lookup"><span data-stu-id="2be45-156">A new class of web apps, called [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="2be45-157">Es posible que le resulte útil simular rápidamente un dispositivo que no tiene conexión de datos cuando está creando este tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="2be45-157">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="2be45-158">Seleccione el menú desplegable **en línea** , búsqueda en **preestablecidos**y seleccione **sin conexión** para simular una experiencia de red completamente desconectada.</span><span class="sxs-lookup"><span data-stu-id="2be45-158">Select the **Online** dropdown menu, search under **Presets**, and select **Offline** to simulate a completely offline network experience.</span></span>  

> ##### <span data-ttu-id="2be45-159">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="2be45-159">Figure 7</span></span>  
> <span data-ttu-id="2be45-160">Menú desplegable desconectado</span><span class="sxs-lookup"><span data-stu-id="2be45-160">The Offline dropdown menu</span></span>  
> <span data-ttu-id="2be45-161">! [Menú desplegable desconectado] [ImageOfflineDropdown]</span><span class="sxs-lookup"><span data-stu-id="2be45-161">![The Offline dropdown menu][ImageOfflineDropdown]</span></span>  

### <span data-ttu-id="2be45-162">Emular conexiones de red lentas</span><span class="sxs-lookup"><span data-stu-id="2be45-162">Emulate slow network connections</span></span>   

<span data-ttu-id="2be45-163">Emular 3G lento, 3G rápido y otras velocidades de conexión en el menú desplegable **en línea** .</span><span class="sxs-lookup"><span data-stu-id="2be45-163">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

> ##### <span data-ttu-id="2be45-164">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="2be45-164">Figure 8</span></span>  
> <span data-ttu-id="2be45-165">El menú desplegable limitación de peticiones</span><span class="sxs-lookup"><span data-stu-id="2be45-165">The Throttling dropdown menu</span></span>  
> <span data-ttu-id="2be45-166">! [El menú desplegable de limitación de peticiones] [ImageNetworkThrottlingMenu]</span><span class="sxs-lookup"><span data-stu-id="2be45-166">![The Throttling dropdown menu][ImageNetworkThrottlingMenu]</span></span>  

<span data-ttu-id="2be45-167">Puedes elegir entre una variedad de ajustes preestablecidos, como 3G lento o 3G rápido.</span><span class="sxs-lookup"><span data-stu-id="2be45-167">You may select from a variety of presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="2be45-168">También puede agregar sus propios ajustes preestablecidos personalizados abriendo el menú de limitación y seleccionando **Custom**  >  **añadir**personalizados.</span><span class="sxs-lookup"><span data-stu-id="2be45-168">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="2be45-169">DevTools muestra un icono de advertencia junto a la pestaña **red** para recordarle que la limitación está habilitada.</span><span class="sxs-lookup"><span data-stu-id="2be45-169">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="2be45-170">Emular conexiones de red lentas del cajón de condiciones de red</span><span class="sxs-lookup"><span data-stu-id="2be45-170">Emulate slow network connections from the Network Conditions drawer</span></span>   

<span data-ttu-id="2be45-171">Si desea limitar la conexión de red mientras trabaja en otros paneles de DevTools, use el cajón de condiciones de redes.</span><span class="sxs-lookup"><span data-stu-id="2be45-171">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="2be45-172">Abra el cajón de **condiciones de redes** .</span><span class="sxs-lookup"><span data-stu-id="2be45-172">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="2be45-173">Seleccione la velocidad de conexión que desee en el menú **limitación** .</span><span class="sxs-lookup"><span data-stu-id="2be45-173">Select your desired connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="2be45-174">Borrar manualmente las cookies del explorador</span><span class="sxs-lookup"><span data-stu-id="2be45-174">Manually clear browser cookies</span></span>   

<span data-ttu-id="2be45-175">Para borrar manualmente las cookies del explorador en cualquier momento, haga clic con el botón secundario en cualquier lugar de la tabla solicitudes y seleccione **Borrar cookies del explorador**.</span><span class="sxs-lookup"><span data-stu-id="2be45-175">To manually clear browser cookies at any time, right-click anywhere in the Requests table and select **Clear Browser Cookies**.</span></span>  

> ##### <span data-ttu-id="2be45-176">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="2be45-176">Figure 9</span></span>  
> <span data-ttu-id="2be45-177">Selección de las cookies de borrar explorador</span><span class="sxs-lookup"><span data-stu-id="2be45-177">Selecting Clear Browser Cookies</span></span>  
> <span data-ttu-id="2be45-178">! [Seleccionando borrar cookies del explorador] [ImageClearBrowserCookies]</span><span class="sxs-lookup"><span data-stu-id="2be45-178">![Selecting Clear Browser Cookies][ImageClearBrowserCookies]</span></span>  

### <span data-ttu-id="2be45-179">Invalidar el agente de usuario</span><span class="sxs-lookup"><span data-stu-id="2be45-179">Override the user agent</span></span>   

<span data-ttu-id="2be45-180">Para anular manualmente el agente de usuario:</span><span class="sxs-lookup"><span data-stu-id="2be45-180">To manually override the user agent:</span></span>  

1.  <span data-ttu-id="2be45-181">Abra el cajón de **condiciones de redes** .</span><span class="sxs-lookup"><span data-stu-id="2be45-181">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="2be45-182">Desactive **seleccionar automáticamente**.</span><span class="sxs-lookup"><span data-stu-id="2be45-182">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="2be45-183">Elija una opción de agente de usuario en el menú o escriba una personalizada en el cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2be45-183">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="2be45-184">Filtrar solicitudes</span><span class="sxs-lookup"><span data-stu-id="2be45-184">Filter requests</span></span>   

### <span data-ttu-id="2be45-185">Filtrar las solicitudes por propiedades</span><span class="sxs-lookup"><span data-stu-id="2be45-185">Filter requests by properties</span></span>   

<span data-ttu-id="2be45-186">Use el cuadro de texto **filtrar** para filtrar las solicitudes por propiedades, como el dominio o el tamaño de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2be45-186">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="2be45-187">Si no ve el cuadro de texto, es probable que el panel filtros esté oculto.</span><span class="sxs-lookup"><span data-stu-id="2be45-187">If you do not see the text box, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="2be45-188">Consulte [ocultar el panel de filtros](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="2be45-188">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

> ##### <span data-ttu-id="2be45-189">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="2be45-189">Figure 10</span></span>  
> <span data-ttu-id="2be45-190">El cuadro de texto filtros</span><span class="sxs-lookup"><span data-stu-id="2be45-190">The Filters text box</span></span>  
> <span data-ttu-id="2be45-191">! [El cuadro de texto filtros] [ImageFilterTextBox]</span><span class="sxs-lookup"><span data-stu-id="2be45-191">![The Filters text box][ImageFilterTextBox]</span></span>  

<span data-ttu-id="2be45-192">Puede usar varias propiedades simultáneamente al separar cada propiedad con un espacio.</span><span class="sxs-lookup"><span data-stu-id="2be45-192">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="2be45-193">Por ejemplo, `mime-type:image/png larger-than:1K` se muestran todos los PNGs que tengan más de un kilobyte.</span><span class="sxs-lookup"><span data-stu-id="2be45-193">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than one kilobyte.</span></span>  <span data-ttu-id="2be45-194">Estos filtros de varias propiedades son equivalentes a `AND` las operaciones.</span><span class="sxs-lookup"><span data-stu-id="2be45-194">These multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="2be45-195">Actualmente no se admiten las operaciones.</span><span class="sxs-lookup"><span data-stu-id="2be45-195">operations are currently not supported.</span></span>  

<span data-ttu-id="2be45-196">La lista completa de propiedades compatibles.</span><span class="sxs-lookup"><span data-stu-id="2be45-196">The complete list of supported properties.</span></span>  

| <span data-ttu-id="2be45-197">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2be45-197">Property</span></span> | <span data-ttu-id="2be45-198">Detalles</span><span class="sxs-lookup"><span data-stu-id="2be45-198">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="2be45-199">Mostrar solo los recursos del dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="2be45-199">Only display resources from the specified domain.</span></span>  <span data-ttu-id="2be45-200">Puede usar un carácter comodín \ ( `*` \) para incluir varios dominios.</span><span class="sxs-lookup"><span data-stu-id="2be45-200">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="2be45-201">Por ejemplo, `*.com` muestra los recursos de todos los nombres de dominio que terminan en `.com` .</span><span class="sxs-lookup"><span data-stu-id="2be45-201">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="2be45-202">DevTools rellena el menú desplegable de autocompletar con todos los dominios que ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="2be45-202">DevTools populates the autocomplete dropdown menu with all of the domains it has encountered.</span></span> |  
| `has-response-header` | <span data-ttu-id="2be45-203">Mostrar los recursos que contienen el encabezado de respuesta HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="2be45-203">Show the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="2be45-204">DevTools rellena la lista desplegable de autocompletar con todos los encabezados de respuesta que ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="2be45-204">DevTools populates the autocomplete dropdown with all of the response headers that it has encountered.</span></span> |  
| `is` | <span data-ttu-id="2be45-205">Usar `is:running` para buscar `WebSocket` recursos.</span><span class="sxs-lookup"><span data-stu-id="2be45-205">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="2be45-206">Mostrar recursos mayores que el tamaño especificado, en bytes.</span><span class="sxs-lookup"><span data-stu-id="2be45-206">Show resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="2be45-207">Establecer un valor de `1000` es equivalente a establecer un valor de `1k` .</span><span class="sxs-lookup"><span data-stu-id="2be45-207">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="2be45-208">Mostrar recursos que se recuperaron en un tipo de método HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="2be45-208">Show resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="2be45-209">DevTools rellena la lista desplegable con todos los métodos HTTP que ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="2be45-209">DevTools populates the dropdown with all of the HTTP methods it has encountered.</span></span> |  
| `mime-type` | <span data-ttu-id="2be45-210">Mostrar los recursos de un tipo MIME especificado.</span><span class="sxs-lookup"><span data-stu-id="2be45-210">Show resources of a specified MIME type.</span></span>  <span data-ttu-id="2be45-211">DevTools rellena la lista desplegable con todos los tipos MIME que ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="2be45-211">DevTools populates the dropdown with all MIME types it has encountered.</span></span> |  
| `mixed-content` | <span data-ttu-id="2be45-212">Mostrar todos los recursos de contenido mixto \ ( `mixed-content:all` \) o solo los que se muestran actualmente \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="2be45-212">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="2be45-213">Mostrar los recursos recuperados en HTTP \ ( `scheme:http` \) no protegidos o en https \ ( `scheme:https` \).</span><span class="sxs-lookup"><span data-stu-id="2be45-213">Show resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="2be45-214">Mostrar los recursos que tienen un `Set-Cookie` encabezado con un `Domain` atributo que coincide con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="2be45-214">Show the resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="2be45-215">DevTools rellena el autocompletar con todos los dominios de cookies que ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="2be45-215">DevTools populates the autocomplete with all of the cookie domains that it has encountered.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="2be45-216">Mostrar los recursos que tengan un `Set-Cookie` encabezado con un nombre que coincida con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="2be45-216">Show the resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="2be45-217">DevTools rellena la autocompletar con todos los nombres de cookies que ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="2be45-217">DevTools populates the autocomplete with all of the cookie names that it has encountered.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="2be45-218">Mostrar los recursos que tienen un `Set-Cookie` encabezado con un valor que coincide con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="2be45-218">Show the resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="2be45-219">DevTools rellena el autocompletar con todos los valores de cookie que ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="2be45-219">DevTools populates the autocomplete with all of the cookie values that it has encountered.</span></span> |  
| `status-code` | <span data-ttu-id="2be45-220">Mostrar solo los recursos para los que el código de Estado HTTP coincide con el código especificado.</span><span class="sxs-lookup"><span data-stu-id="2be45-220">Show only the resources for which the HTTP status code matches the specified code.</span></span>  <span data-ttu-id="2be45-221">DevTools rellena el menú desplegable de autocompletar con todos los códigos de estado que ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="2be45-221">DevTools populates the autocomplete dropdown menu with all of the status codes it has encountered.</span></span> |  

### <span data-ttu-id="2be45-222">Filtrar solicitudes por tipo</span><span class="sxs-lookup"><span data-stu-id="2be45-222">Filter requests by type</span></span>   

<span data-ttu-id="2be45-223">Para filtrar las solicitudes según el tipo de solicitud, seleccione los botones **XHR**, **JS**, **CSS**, **IMG**, **multimedia**, **fuente**, **documento**, **WS** \ (WebSocket \), **manifiesto**u **otros** \ (cualquier otro tipo no incluido aquí \) en el panel red.</span><span class="sxs-lookup"><span data-stu-id="2be45-223">To filter requests by request type, select the **XHR**, **JS**, **CSS**, **Img**, **Media**, **Font**, **Doc**, **WS** \(WebSocket\), **Manifest**, or **Other** \(any other type not listed here\) buttons on the Network panel.</span></span>  

<span data-ttu-id="2be45-224">Si no ve estos botones, es probable que el panel filtros esté oculto.</span><span class="sxs-lookup"><span data-stu-id="2be45-224">If you do not see these buttons, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="2be45-225">Consulte [ocultar el panel de filtros](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="2be45-225">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="2be45-226">Para habilitar varios filtros de tipo al mismo tiempo, mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y, a continuación, seleccione.</span><span class="sxs-lookup"><span data-stu-id="2be45-226">To enable multiple type filters simultaneously, hold `Control` \(Windows\) or `Command` \(macOS\) and then select.</span></span>  

> ##### <span data-ttu-id="2be45-227">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="2be45-227">Figure 11</span></span>  
> <span data-ttu-id="2be45-228">Usar los filtros de tipo para mostrar los recursos JS, CSS y Document</span><span class="sxs-lookup"><span data-stu-id="2be45-228">Using the Type filters to display JS, CSS, and Document resources</span></span>  
> <span data-ttu-id="2be45-229">! [Usar los filtros de tipo para mostrar JS, CSS y recursos de documento] [ImageMultiTypeFilter]</span><span class="sxs-lookup"><span data-stu-id="2be45-229">![Using the Type filters to display JS, CSS, and Document resources][ImageMultiTypeFilter]</span></span>  

### <span data-ttu-id="2be45-230">Filtrar solicitudes por tiempo</span><span class="sxs-lookup"><span data-stu-id="2be45-230">Filter requests by time</span></span>   

<span data-ttu-id="2be45-231">Seleccione y arrastre a la izquierda o a la derecha en el panel de descripción para mostrar solo las solicitudes que estaban activas durante ese período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="2be45-231">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="2be45-232">El filtro es inclusivo.</span><span class="sxs-lookup"><span data-stu-id="2be45-232">The filter is inclusive.</span></span>  <span data-ttu-id="2be45-233">Se muestra cualquier solicitud que estuviera activa durante la hora resaltada.</span><span class="sxs-lookup"><span data-stu-id="2be45-233">Any request that was active during the highlighted time is shown.</span></span>  

> ##### <span data-ttu-id="2be45-234">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="2be45-234">Figure 12</span></span>  
> <span data-ttu-id="2be45-235">Filtrar las solicitudes inactivas en 300ms</span><span class="sxs-lookup"><span data-stu-id="2be45-235">Filtering out any requests that were inactive around 300ms</span></span>  
> <span data-ttu-id="2be45-236">! [Filtrando las solicitudes inactivas en 300ms] [ImageOverviewFilter]</span><span class="sxs-lookup"><span data-stu-id="2be45-236">![Filtering out any requests that were inactive around 300ms][ImageOverviewFilter]</span></span>  

### <span data-ttu-id="2be45-237">Ocultar direcciones URL de datos</span><span class="sxs-lookup"><span data-stu-id="2be45-237">Hide data URLs</span></span>  

<span data-ttu-id="2be45-238">Las [direcciones URL de datos][MDNHTTPDataURIs] son pequeños archivos incrustados en otros documentos.</span><span class="sxs-lookup"><span data-stu-id="2be45-238">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="2be45-239">Cualquier solicitud que vea en la tabla solicitudes que comienza por `data:` es una dirección URL de datos.</span><span class="sxs-lookup"><span data-stu-id="2be45-239">Any request that you see in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="2be45-240">Active la casilla **ocultar URLs de datos** para ocultar estas solicitudes.</span><span class="sxs-lookup"><span data-stu-id="2be45-240">Check the **Hide data URLs** checkbox to hide these requests.</span></span>  

> ##### <span data-ttu-id="2be45-241">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="2be45-241">Figure 13</span></span>  
> <span data-ttu-id="2be45-242">La casilla ocultar direcciones URL de datos</span><span class="sxs-lookup"><span data-stu-id="2be45-242">The Hide Data URLs checkbox</span></span>  
> <span data-ttu-id="2be45-243">! [Casilla ocultar direcciones URL de datos] [ImageHideDataURLsCheckBox]</span><span class="sxs-lookup"><span data-stu-id="2be45-243">![The Hide Data URLs checkbox][ImageHideDataURLsCheckBox]</span></span>  

## <span data-ttu-id="2be45-244">Ordenar solicitudes</span><span class="sxs-lookup"><span data-stu-id="2be45-244">Sort requests</span></span>  

<span data-ttu-id="2be45-245">De forma predeterminada, las solicitudes de la tabla solicitudes se ordenan por hora de inicio, pero puede ordenar la tabla mediante otros criterios.</span><span class="sxs-lookup"><span data-stu-id="2be45-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="2be45-246">Ordenar por columna</span><span class="sxs-lookup"><span data-stu-id="2be45-246">Sort by column</span></span>   

<span data-ttu-id="2be45-247">Seleccione el encabezado de cualquier columna en las solicitudes para ordenar las solicitudes por esa columna.</span><span class="sxs-lookup"><span data-stu-id="2be45-247">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="2be45-248">Ordenar por fase de actividad</span><span class="sxs-lookup"><span data-stu-id="2be45-248">Sort by activity phase</span></span>   

<span data-ttu-id="2be45-249">Para cambiar la forma en que la cascada ordena las solicitudes, haga clic con el botón secundario en el encabezado de la tabla solicitudes, desplace el puntero sobre **cascada**y seleccione una de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="2be45-249">To change how the Waterfall sorts requests, right-click the header of the Requests table, hover over **Waterfall**, and select one of the following options.</span></span>  

*   <span data-ttu-id="2be45-250">**Hora de inicio**.</span><span class="sxs-lookup"><span data-stu-id="2be45-250">**Start Time**.</span></span>  <span data-ttu-id="2be45-251">La primera solicitud iniciada se encuentra en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="2be45-251">The first request that was initiated is at the top.</span></span>  
*   <span data-ttu-id="2be45-252">**Tiempo de respuesta**.</span><span class="sxs-lookup"><span data-stu-id="2be45-252">**Response Time**.</span></span>  <span data-ttu-id="2be45-253">La primera solicitud que comenzó a descargarse está en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="2be45-253">The first request that started downloading is at the top.</span></span>  
*   <span data-ttu-id="2be45-254">**Hora de finalización**.</span><span class="sxs-lookup"><span data-stu-id="2be45-254">**End Time**.</span></span>  <span data-ttu-id="2be45-255">La primera solicitud que ha finalizado se encuentra en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="2be45-255">The first request that finished is at the top.</span></span>  
*   <span data-ttu-id="2be45-256">**Duración total**.</span><span class="sxs-lookup"><span data-stu-id="2be45-256">**Total Duration**.</span></span>  <span data-ttu-id="2be45-257">La solicitud con la configuración de conexión más corta y la solicitud o respuesta se encuentra en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="2be45-257">The request with the shortest connection setup and request / response is at the top.</span></span>  
*   <span data-ttu-id="2be45-258">**Latencia**.</span><span class="sxs-lookup"><span data-stu-id="2be45-258">**Latency**.</span></span>  <span data-ttu-id="2be45-259">La solicitud que esperó el tiempo más breve para una respuesta está en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="2be45-259">The request that waited the shortest time for a response is at the top.</span></span>  

<span data-ttu-id="2be45-260">En estas descripciones se supone que cada opción respectiva está clasificada de menor a mayor.</span><span class="sxs-lookup"><span data-stu-id="2be45-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="2be45-261">Al seleccionar el encabezado de la columna **cascada** se invierte el orden.</span><span class="sxs-lookup"><span data-stu-id="2be45-261">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

> ##### <span data-ttu-id="2be45-262">Imagen 14</span><span class="sxs-lookup"><span data-stu-id="2be45-262">Figure 14</span></span>  
> <span data-ttu-id="2be45-263">Ordenar la cascada por duración total \ (la parte más clara de cada barra está en espera y la parte más oscura es el tiempo dedicado a descargar bytes \)</span><span class="sxs-lookup"><span data-stu-id="2be45-263">Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
> <span data-ttu-id="2be45-264">! [Ordenando la cascada por duración total] [ImageWaterfallTotalDuration]</span><span class="sxs-lookup"><span data-stu-id="2be45-264">![Sorting the Waterfall by total duration][ImageWaterfallTotalDuration]</span></span>  

## <span data-ttu-id="2be45-265">Analizar solicitudes</span><span class="sxs-lookup"><span data-stu-id="2be45-265">Analyze requests</span></span>   

<span data-ttu-id="2be45-266">Siempre que DevTools esté abierto, registra todas las solicitudes en el panel de red.</span><span class="sxs-lookup"><span data-stu-id="2be45-266">So long as DevTools is open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="2be45-267">Use el panel red para analizar las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="2be45-267">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="2be45-268">Ver un registro de solicitudes</span><span class="sxs-lookup"><span data-stu-id="2be45-268">View a log of requests</span></span>   

<span data-ttu-id="2be45-269">Use la tabla solicitudes para ver un registro de todas las solicitudes realizadas mientras se ha abierto DevTools.</span><span class="sxs-lookup"><span data-stu-id="2be45-269">Use the Requests table to view a log of all requests made while DevTools has been open.</span></span>  <span data-ttu-id="2be45-270">Al seleccionar o mantener el puntero sobre solicitudes, se muestra más información sobre cada elemento.</span><span class="sxs-lookup"><span data-stu-id="2be45-270">Selecting or hovering over requests reveals more information about each item.</span></span>  

> ##### <span data-ttu-id="2be45-271">Imagen 15</span><span class="sxs-lookup"><span data-stu-id="2be45-271">Figure 15</span></span>  
> <span data-ttu-id="2be45-272">La tabla solicitudes</span><span class="sxs-lookup"><span data-stu-id="2be45-272">The Requests table</span></span>  
> <span data-ttu-id="2be45-273">! [La tabla solicitudes] [ImageRequestsTable]</span><span class="sxs-lookup"><span data-stu-id="2be45-273">![The Requests table][ImageRequestsTable]</span></span>  

<span data-ttu-id="2be45-274">De forma predeterminada, en la tabla solicitudes se muestran las siguientes columnas:</span><span class="sxs-lookup"><span data-stu-id="2be45-274">The Requests table displays the following columns by default:</span></span>  

*   <span data-ttu-id="2be45-275">**Nombre**.</span><span class="sxs-lookup"><span data-stu-id="2be45-275">**Name**.</span></span>  <span data-ttu-id="2be45-276">El nombre de archivo de un recurso o un identificador de él.</span><span class="sxs-lookup"><span data-stu-id="2be45-276">The filename of, or an identifier for, the resource.</span></span>  
*   <span data-ttu-id="2be45-277">**Estado**.</span><span class="sxs-lookup"><span data-stu-id="2be45-277">**Status**.</span></span>  <span data-ttu-id="2be45-278">El código de Estado HTTP.</span><span class="sxs-lookup"><span data-stu-id="2be45-278">The HTTP status code.</span></span>  
*   <span data-ttu-id="2be45-279">**Tipo**.</span><span class="sxs-lookup"><span data-stu-id="2be45-279">**Type**.</span></span>  <span data-ttu-id="2be45-280">Tipo MIME del recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="2be45-280">The MIME type of the requested resource.</span></span>  
*   <span data-ttu-id="2be45-281">**Iniciador**.</span><span class="sxs-lookup"><span data-stu-id="2be45-281">**Initiator**.</span></span>  <span data-ttu-id="2be45-282">Los siguientes objetos o procesos inician solicitudes:</span><span class="sxs-lookup"><span data-stu-id="2be45-282">The following objects or processes initiate requests:</span></span>  
    *   <span data-ttu-id="2be45-283">**Parser**.</span><span class="sxs-lookup"><span data-stu-id="2be45-283">**Parser**.</span></span>  <span data-ttu-id="2be45-284">El analizador HTML para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2be45-284">The HTML parser for Microsoft Edge.</span></span>  
    *   <span data-ttu-id="2be45-285">**Redirigir**.</span><span class="sxs-lookup"><span data-stu-id="2be45-285">**Redirect**.</span></span>  <span data-ttu-id="2be45-286">Una redirección de HTTP.</span><span class="sxs-lookup"><span data-stu-id="2be45-286">An HTTP redirect.</span></span>  
    *   <span data-ttu-id="2be45-287">**Script**.</span><span class="sxs-lookup"><span data-stu-id="2be45-287">**Script**.</span></span>  <span data-ttu-id="2be45-288">Una función de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2be45-288">A JavaScript function.</span></span>  
    *   <span data-ttu-id="2be45-289">**Otros**.</span><span class="sxs-lookup"><span data-stu-id="2be45-289">**Other**.</span></span>  <span data-ttu-id="2be45-290">Otro proceso o acción, como navegar hasta una página a través de un vínculo o escribir una dirección URL en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="2be45-290">Some other process or action, such as navigating to a page via a link or entering a URL in the address bar.</span></span>  
*   <span data-ttu-id="2be45-291">**Tamaño**.</span><span class="sxs-lookup"><span data-stu-id="2be45-291">**Size**.</span></span>  <span data-ttu-id="2be45-292">El tamaño combinado de los encabezados de respuesta más el cuerpo de la respuesta, tal y como lo proporciona el servidor.</span><span class="sxs-lookup"><span data-stu-id="2be45-292">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
*   <span data-ttu-id="2be45-293">**Momento**.</span><span class="sxs-lookup"><span data-stu-id="2be45-293">**Time**.</span></span>  <span data-ttu-id="2be45-294">La duración total, desde el inicio de la solicitud hasta la recepción del byte final en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2be45-294">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
*   <span data-ttu-id="2be45-295">[**Cascada**](#view-the-timing-of-requests-in-relation-to-one-another).</span><span class="sxs-lookup"><span data-stu-id="2be45-295">[**Waterfall**](#view-the-timing-of-requests-in-relation-to-one-another).</span></span>  <span data-ttu-id="2be45-296">Un desglose visual de la actividad de cada solicitud.</span><span class="sxs-lookup"><span data-stu-id="2be45-296">A visual breakdown of the activity for each request.</span></span>  

#### <span data-ttu-id="2be45-297">Agregar o quitar columnas</span><span class="sxs-lookup"><span data-stu-id="2be45-297">Add or remove columns</span></span>   

<span data-ttu-id="2be45-298">Haga clic con el botón secundario en el encabezado de la tabla solicitudes y seleccione una opción para ocultarla o mostrarla.</span><span class="sxs-lookup"><span data-stu-id="2be45-298">Right-click the header of the Requests table and select an option to hide or show it.</span></span>  <span data-ttu-id="2be45-299">Las opciones mostradas actualmente tienen marcas de verificación junto a cada elemento.</span><span class="sxs-lookup"><span data-stu-id="2be45-299">Currently displayed options have checkmarks next to each item.</span></span>  

> ##### <span data-ttu-id="2be45-300">Imagen 16</span><span class="sxs-lookup"><span data-stu-id="2be45-300">Figure 16</span></span>  
> <span data-ttu-id="2be45-301">Agregar una columna a la tabla solicitudes</span><span class="sxs-lookup"><span data-stu-id="2be45-301">Adding a column to the Requests table</span></span>  
> <span data-ttu-id="2be45-302">! [Agregando una columna a la tabla solicitudes] [ImageRequestsTableAddColumn]</span><span class="sxs-lookup"><span data-stu-id="2be45-302">![Adding a column to the Requests table][ImageRequestsTableAddColumn]</span></span>  

#### <span data-ttu-id="2be45-303">Agregar columnas personalizadas</span><span class="sxs-lookup"><span data-stu-id="2be45-303">Add custom columns</span></span>   

<span data-ttu-id="2be45-304">Para agregar una columna personalizada a la tabla solicitudes, haga clic con el botón secundario en el encabezado de la tabla solicitudes y seleccione **encabezados de respuesta**  >  **administrar columnas de encabezado**.</span><span class="sxs-lookup"><span data-stu-id="2be45-304">To add a custom column to the Requests table, right-click the header of the Requests table and select **Response Headers** > **Manage Header Columns**.</span></span>  

> ##### <span data-ttu-id="2be45-305">Imagen 17</span><span class="sxs-lookup"><span data-stu-id="2be45-305">Figure 17</span></span>  
> <span data-ttu-id="2be45-306">Agregar una columna personalizada a la tabla solicitudes</span><span class="sxs-lookup"><span data-stu-id="2be45-306">Adding a custom column to the Requests table</span></span>  
> <span data-ttu-id="2be45-307">! [Agregando una columna personalizada a la tabla solicitudes] [ImageRequestsTableCustomColumn]</span><span class="sxs-lookup"><span data-stu-id="2be45-307">![Adding a custom column to the Requests table][ImageRequestsTableCustomColumn]</span></span>  

### <span data-ttu-id="2be45-308">Ver los intervalos de solicitudes relacionados entre sí</span><span class="sxs-lookup"><span data-stu-id="2be45-308">View the timing of requests in relation to one another</span></span>   

<span data-ttu-id="2be45-309">Use la cascada para ver los intervalos de solicitudes relacionados entre sí.</span><span class="sxs-lookup"><span data-stu-id="2be45-309">Use the Waterfall to view the timing of requests in relation to one another.</span></span>  
<span data-ttu-id="2be45-310">De forma predeterminada, la cascada está organizada por la hora de inicio de las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="2be45-310">By default, the Waterfall is organized by the start time of the requests.</span></span>  
<span data-ttu-id="2be45-311">Por lo tanto, las solicitudes que se encuentren más lejanas a la izquierda iniciadas antes de las que están más lejos a la derecha.</span><span class="sxs-lookup"><span data-stu-id="2be45-311">So, requests that are farther to the left started earlier than those that are farther to the right.</span></span>  

<span data-ttu-id="2be45-312">Consulte [ordenar por fase de actividad](#sort-by-activity-phase) para ver las diferentes formas de ordenar la cascada.</span><span class="sxs-lookup"><span data-stu-id="2be45-312">See [Sort by activity phase](#sort-by-activity-phase) to see the different ways that you may sort the Waterfall.</span></span>  

> ##### <span data-ttu-id="2be45-313">Ilustración 18</span><span class="sxs-lookup"><span data-stu-id="2be45-313">Figure 18</span></span>  
> <span data-ttu-id="2be45-314">La columna cascada del panel solicitudes</span><span class="sxs-lookup"><span data-stu-id="2be45-314">The Waterfall column of the Requests pane</span></span>  
> <span data-ttu-id="2be45-315">! [La columna cascada del panel solicitudes] [ImageRequestsTableWaterfallColumn]</span><span class="sxs-lookup"><span data-stu-id="2be45-315">![The Waterfall column of the Requests pane][ImageRequestsTableWaterfallColumn]</span></span>  

<!-- ### Analyze the frames of a WebSocket Connection   -->

<!--To view the frames of a WebSocket connection:  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-click the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
> ##### Old Figure 20  
> The Frames tab  
> ![The Frames tab][ImageFrames]  
-->

<!--The table contains three columns:  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to their type:  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### <span data-ttu-id="2be45-316">Ver una vista previa del cuerpo de una respuesta</span><span class="sxs-lookup"><span data-stu-id="2be45-316">View a preview of a response body</span></span>   

<span data-ttu-id="2be45-317">Para ver una vista previa del cuerpo de una respuesta:</span><span class="sxs-lookup"><span data-stu-id="2be45-317">To view a preview of a response body:</span></span>  

1.  <span data-ttu-id="2be45-318">Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="2be45-318">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="2be45-319">Seleccione la pestaña **vista previa** .</span><span class="sxs-lookup"><span data-stu-id="2be45-319">Select the **Preview** tab.</span></span>  

<span data-ttu-id="2be45-320">Esta pestaña es principalmente útil para visualizar imágenes.</span><span class="sxs-lookup"><span data-stu-id="2be45-320">This tab is mostly useful for viewing images.</span></span>  

> ##### <span data-ttu-id="2be45-321">Ilustración 19</span><span class="sxs-lookup"><span data-stu-id="2be45-321">Figure 19</span></span>  
> <span data-ttu-id="2be45-322">La ficha vista previa</span><span class="sxs-lookup"><span data-stu-id="2be45-322">The Preview tab</span></span>  
> <span data-ttu-id="2be45-323">! [Ficha vista previa] [ImagePreview]</span><span class="sxs-lookup"><span data-stu-id="2be45-323">![The Preview tab][ImagePreview]</span></span>  

### <span data-ttu-id="2be45-324">Ver el cuerpo de una respuesta</span><span class="sxs-lookup"><span data-stu-id="2be45-324">View a response body</span></span>   

<span data-ttu-id="2be45-325">Para ver el cuerpo de la respuesta de una solicitud:</span><span class="sxs-lookup"><span data-stu-id="2be45-325">To view the response body to a request:</span></span>  

1.  <span data-ttu-id="2be45-326">Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="2be45-326">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="2be45-327">Seleccione la pestaña **respuesta** .</span><span class="sxs-lookup"><span data-stu-id="2be45-327">Select the **Response** tab.</span></span>  

> ##### <span data-ttu-id="2be45-328">Ilustración 20</span><span class="sxs-lookup"><span data-stu-id="2be45-328">Figure 20</span></span>  
> <span data-ttu-id="2be45-329">La ficha respuesta</span><span class="sxs-lookup"><span data-stu-id="2be45-329">The Response tab</span></span>  
> <span data-ttu-id="2be45-330">! [La pestaña respuesta] [ImageResponse]</span><span class="sxs-lookup"><span data-stu-id="2be45-330">![The Response tab][ImageResponse]</span></span>  

### <span data-ttu-id="2be45-331">Ver encabezados HTTP</span><span class="sxs-lookup"><span data-stu-id="2be45-331">View HTTP headers</span></span>   

<span data-ttu-id="2be45-332">Para ver los datos de encabezado HTTP sobre una solicitud:</span><span class="sxs-lookup"><span data-stu-id="2be45-332">To view HTTP header data about a request:</span></span>  

1.  <span data-ttu-id="2be45-333">Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="2be45-333">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="2be45-334">Seleccione la pestaña **encabezados** .</span><span class="sxs-lookup"><span data-stu-id="2be45-334">Select the **Headers** tab.</span></span>  

> ##### <span data-ttu-id="2be45-335">Ilustración 21</span><span class="sxs-lookup"><span data-stu-id="2be45-335">Figure 21</span></span>  
> <span data-ttu-id="2be45-336">La pestaña encabezados</span><span class="sxs-lookup"><span data-stu-id="2be45-336">The Headers tab</span></span>  
> <span data-ttu-id="2be45-337">! [Ficha encabezados] [ImageHeaders]</span><span class="sxs-lookup"><span data-stu-id="2be45-337">![The Headers tab][ImageHeaders]</span></span>  

#### <span data-ttu-id="2be45-338">Ver origen de encabezado HTTP</span><span class="sxs-lookup"><span data-stu-id="2be45-338">View HTTP header source</span></span>   

<span data-ttu-id="2be45-339">De forma predeterminada, la pestaña encabezados muestra los nombres de encabezado alfabéticamente.</span><span class="sxs-lookup"><span data-stu-id="2be45-339">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="2be45-340">Para ver los nombres de encabezado HTTP en el orden en que se recibieron:</span><span class="sxs-lookup"><span data-stu-id="2be45-340">To view the HTTP header names in the order they were received:</span></span>  

1.  <span data-ttu-id="2be45-341">Abre la pestaña **encabezados** para la solicitud que te interese.</span><span class="sxs-lookup"><span data-stu-id="2be45-341">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="2be45-342">Consulte [Ver encabezados HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="2be45-342">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="2be45-343">Seleccione **Ver origen**, junto a la sección **solicitar** encabezado o **respuesta de encabezado** .</span><span class="sxs-lookup"><span data-stu-id="2be45-343">Select **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="2be45-344">Ver parámetros de cadena de consulta</span><span class="sxs-lookup"><span data-stu-id="2be45-344">View query string parameters</span></span>   

<span data-ttu-id="2be45-345">Para ver los parámetros de cadena de consulta de una dirección URL en un formato legible:</span><span class="sxs-lookup"><span data-stu-id="2be45-345">To view the query string parameters of a URL in a human-readable format:</span></span>  

1.  <span data-ttu-id="2be45-346">Abre la pestaña **encabezados** para la solicitud que te interese.</span><span class="sxs-lookup"><span data-stu-id="2be45-346">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="2be45-347">Consulte [Ver encabezados HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="2be45-347">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="2be45-348">Vaya a la sección **parámetros de cadena de consulta** .</span><span class="sxs-lookup"><span data-stu-id="2be45-348">Go to the **Query String Parameters** section.</span></span>  

> ##### <span data-ttu-id="2be45-349">Ilustración 22</span><span class="sxs-lookup"><span data-stu-id="2be45-349">Figure 22</span></span>  
> <span data-ttu-id="2be45-350">Sección parámetros de cadena de consulta</span><span class="sxs-lookup"><span data-stu-id="2be45-350">The Query String Parameters section</span></span>  
> <span data-ttu-id="2be45-351">! [Sección de parámetros de cadena de consulta] [ImageQueryStringParameters]</span><span class="sxs-lookup"><span data-stu-id="2be45-351">![The Query String Parameters section][ImageQueryStringParameters]</span></span>  

#### <span data-ttu-id="2be45-352">Ver origen de parámetros de cadena de consulta</span><span class="sxs-lookup"><span data-stu-id="2be45-352">View query string parameters source</span></span>   

<span data-ttu-id="2be45-353">Para ver el origen de parámetro de cadena de consulta de una solicitud:</span><span class="sxs-lookup"><span data-stu-id="2be45-353">To view the query string parameter source of a request:</span></span>  

1.  <span data-ttu-id="2be45-354">Vaya a la sección parámetros de cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="2be45-354">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="2be45-355">Consulte [ver parámetros de cadena de consulta](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="2be45-355">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="2be45-356">Seleccione **Ver origen**.</span><span class="sxs-lookup"><span data-stu-id="2be45-356">Select **view source**.</span></span>  

#### <span data-ttu-id="2be45-357">Ver parámetros de cadena de consulta con codificación URL</span><span class="sxs-lookup"><span data-stu-id="2be45-357">View URL-encoded query string parameters</span></span>   

<span data-ttu-id="2be45-358">Para ver los parámetros de cadena de consulta en un formato legible, pero conservando las codificaciones:</span><span class="sxs-lookup"><span data-stu-id="2be45-358">To view query string parameters in a human-readable format, but with encodings preserved:</span></span>  

1.  <span data-ttu-id="2be45-359">Vaya a la sección parámetros de cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="2be45-359">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="2be45-360">Consulte [ver parámetros de cadena de consulta](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="2be45-360">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="2be45-361">Seleccione **Ver dirección URL codificada**.</span><span class="sxs-lookup"><span data-stu-id="2be45-361">Select **view URL encoded**.</span></span>  

### <span data-ttu-id="2be45-362">Ver cookies</span><span class="sxs-lookup"><span data-stu-id="2be45-362">View cookies</span></span>   

<span data-ttu-id="2be45-363">Para ver las cookies enviadas en el encabezado HTTP de una solicitud:</span><span class="sxs-lookup"><span data-stu-id="2be45-363">To view the cookies sent in the HTTP header of a request:</span></span>  

1.  <span data-ttu-id="2be45-364">Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="2be45-364">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="2be45-365">Seleccione la ficha **cookies** .</span><span class="sxs-lookup"><span data-stu-id="2be45-365">Select the **Cookies** tab.</span></span>  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

> ##### <span data-ttu-id="2be45-366">Ilustración 23</span><span class="sxs-lookup"><span data-stu-id="2be45-366">Figure 23</span></span>  
> <span data-ttu-id="2be45-367">La ficha cookies</span><span class="sxs-lookup"><span data-stu-id="2be45-367">The Cookies tab</span></span>  
> <span data-ttu-id="2be45-368">! [Ficha cookies] [ImageCookies]</span><span class="sxs-lookup"><span data-stu-id="2be45-368">![The Cookies tab][ImageCookies]</span></span>  

### <span data-ttu-id="2be45-369">Ver el desglose de intervalos de una solicitud</span><span class="sxs-lookup"><span data-stu-id="2be45-369">View the timing breakdown of a request</span></span>   

<span data-ttu-id="2be45-370">Para ver el desglose de intervalos de una solicitud:</span><span class="sxs-lookup"><span data-stu-id="2be45-370">To view the timing breakdown of a request:</span></span>  

1.  <span data-ttu-id="2be45-371">Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="2be45-371">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="2be45-372">Seleccione la pestaña **intervalos** .</span><span class="sxs-lookup"><span data-stu-id="2be45-372">Select the **Timing** tab.</span></span>  

<span data-ttu-id="2be45-373">Vea obtener una [vista previa de un desglose de intervalos](#preview-a-timing-breakdown) para obtener acceso a estos datos más rápidamente.</span><span class="sxs-lookup"><span data-stu-id="2be45-373">See [Preview a timing breakdown](#preview-a-timing-breakdown) for a faster way to access this data.</span></span>  

<span data-ttu-id="2be45-374">Consulte [fases de desglose de intervalos explicadas](#timing-breakdown-phases-explained) para obtener más información sobre cada una de las fases que puede ver en la pestaña intervalos.</span><span class="sxs-lookup"><span data-stu-id="2be45-374">See [Timing breakdown phases explained](#timing-breakdown-phases-explained) for more information about each of the phases that you may see in the Timing tab.</span></span>  

> ##### <span data-ttu-id="2be45-375">Ilustración 24</span><span class="sxs-lookup"><span data-stu-id="2be45-375">Figure 24</span></span>  
> <span data-ttu-id="2be45-376">La ficha intervalos</span><span class="sxs-lookup"><span data-stu-id="2be45-376">The Timing tab</span></span>  
> <span data-ttu-id="2be45-377">! [Ficha intervalos] [ImageTiming]</span><span class="sxs-lookup"><span data-stu-id="2be45-377">![The Timing tab][ImageTiming]</span></span>  

<span data-ttu-id="2be45-378">Más información sobre cada una de las fases.</span><span class="sxs-lookup"><span data-stu-id="2be45-378">More information about each of the phases.</span></span>  

<span data-ttu-id="2be45-379">Consulte [Ver desglose de intervalos](#view-the-timing-breakdown-of-a-request) para obtener acceso a esta vista.</span><span class="sxs-lookup"><span data-stu-id="2be45-379">See [View timing breakdown](#view-the-timing-breakdown-of-a-request) for another way to access this view.</span></span>  

#### <span data-ttu-id="2be45-380">Obtener una vista previa de intervalos</span><span class="sxs-lookup"><span data-stu-id="2be45-380">Preview a timing breakdown</span></span>   

<span data-ttu-id="2be45-381">Para obtener una vista previa del desglose de intervalos de una solicitud, desplace el puntero sobre la entrada de la solicitud en la columna **cascada** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="2be45-381">To view a preview of the timing breakdown of a request, hover over the entry for the request in the **Waterfall** column of the Requests table.</span></span>  

<span data-ttu-id="2be45-382">Vea [ver el desglose de intervalos de una solicitud](#view-the-timing-breakdown-of-a-request) para obtener acceso a estos datos que no requieren el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="2be45-382">See [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request) for a way to access this data that does not require hovering.</span></span>  

> ##### <span data-ttu-id="2be45-383">Ilustración 25</span><span class="sxs-lookup"><span data-stu-id="2be45-383">Figure 25</span></span>  
> <span data-ttu-id="2be45-384">Obtener una vista previa del desglose de intervalos de una solicitud</span><span class="sxs-lookup"><span data-stu-id="2be45-384">Previewing the timing breakdown of a request</span></span>  
> <span data-ttu-id="2be45-385">! [Vista previa del desglose de intervalos de una solicitud] [ImageWaterfallHover]</span><span class="sxs-lookup"><span data-stu-id="2be45-385">![Previewing the timing breakdown of a request][ImageWaterfallHover]</span></span>  

#### <span data-ttu-id="2be45-386">Explicación de fases de desglose de intervalos</span><span class="sxs-lookup"><span data-stu-id="2be45-386">Timing breakdown phases explained</span></span>   

<span data-ttu-id="2be45-387">Más información sobre cada una de las fases que puede ver en la pestaña intervalos:</span><span class="sxs-lookup"><span data-stu-id="2be45-387">More information about each of the phases you may see in the Timing tab:</span></span>  

*   <span data-ttu-id="2be45-388">**Poner en cola**.</span><span class="sxs-lookup"><span data-stu-id="2be45-388">**Queueing**.</span></span>  <span data-ttu-id="2be45-389">El explorador pone en cola las solicitudes cuando:</span><span class="sxs-lookup"><span data-stu-id="2be45-389">The browser queues requests when:</span></span>  
    *   <span data-ttu-id="2be45-390">Hay solicitudes de prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="2be45-390">There are higher priority requests.</span></span>  
    *   <span data-ttu-id="2be45-391">Ya hay seis conexiones TCP abiertas para este origen, que es el límite.</span><span class="sxs-lookup"><span data-stu-id="2be45-391">There are already six TCP connections open for this origin, which is the limit.</span></span>  <span data-ttu-id="2be45-392">Solo se aplica a HTTP/1.0 y HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="2be45-392">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
    *   <span data-ttu-id="2be45-393">El explorador está asignando un poco de espacio en la caché de disco.</span><span class="sxs-lookup"><span data-stu-id="2be45-393">The browser is briefly allocating space in the disk cache.</span></span>  
*   <span data-ttu-id="2be45-394">**Detenido**.</span><span class="sxs-lookup"><span data-stu-id="2be45-394">**Stalled**.</span></span>  <span data-ttu-id="2be45-395">La solicitud podría estar detenida por cualquiera de las razones descritas en **puesta en cola**.</span><span class="sxs-lookup"><span data-stu-id="2be45-395">The request could be stalled for any of the reasons described in **Queueing**.</span></span>  
*   <span data-ttu-id="2be45-396">**Búsqueda DNS**.</span><span class="sxs-lookup"><span data-stu-id="2be45-396">**DNS Lookup**.</span></span>  <span data-ttu-id="2be45-397">El explorador está resolviendo la dirección IP de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2be45-397">The browser is resolving the IP address for the request.</span></span>  
*   <span data-ttu-id="2be45-398">**Negociación de proxy**.</span><span class="sxs-lookup"><span data-stu-id="2be45-398">**Proxy negotiation**.</span></span>  <span data-ttu-id="2be45-399">El explorador está negociando la solicitud con un [servidor proxy][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="2be45-399">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
*   <span data-ttu-id="2be45-400">**Solicitud enviada**.</span><span class="sxs-lookup"><span data-stu-id="2be45-400">**Request sent**.</span></span>  <span data-ttu-id="2be45-401">Se está enviando la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2be45-401">The request is being sent.</span></span>  
*   <span data-ttu-id="2be45-402">**Preparación de ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="2be45-402">**ServiceWorker Preparation**.</span></span>  <span data-ttu-id="2be45-403">El explorador está iniciando el trabajo del servicio.</span><span class="sxs-lookup"><span data-stu-id="2be45-403">The browser is starting up the service worker.</span></span>  
*   <span data-ttu-id="2be45-404">**Solicitud para ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="2be45-404">**Request to ServiceWorker**.</span></span>  <span data-ttu-id="2be45-405">La solicitud se está enviando al trabajador del servicio.</span><span class="sxs-lookup"><span data-stu-id="2be45-405">The request is being sent to the service worker.</span></span>  
*   <span data-ttu-id="2be45-406">**Esperando \ (TTFB \)**.</span><span class="sxs-lookup"><span data-stu-id="2be45-406">**Waiting \(TTFB\)**.</span></span>  <span data-ttu-id="2be45-407">El explorador está esperando el primer byte de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="2be45-407">The browser is waiting for the first byte of a response.</span></span>  
  <span data-ttu-id="2be45-408">TTFB es el primer byte.</span><span class="sxs-lookup"><span data-stu-id="2be45-408">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="2be45-409">Este intervalo incluye 1 recorrido de ida y vuelta de la latencia y el tiempo que el servidor necesitó para preparar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2be45-409">This timing includes 1 round trip of latency and the time the server took to prepare the response.</span></span>  
*   <span data-ttu-id="2be45-410">**Descarga de contenido**.</span><span class="sxs-lookup"><span data-stu-id="2be45-410">**Content Download**.</span></span>  <span data-ttu-id="2be45-411">El explorador está recibiendo la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2be45-411">The browser is receiving the response.</span></span>  
*   <span data-ttu-id="2be45-412">**Recibiendo Push**.</span><span class="sxs-lookup"><span data-stu-id="2be45-412">**Receiving Push**.</span></span>  <span data-ttu-id="2be45-413">El explorador está recibiendo datos de esta respuesta a través de la inserción de servidor HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="2be45-413">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
*   <span data-ttu-id="2be45-414">**Leyendo inserción**.</span><span class="sxs-lookup"><span data-stu-id="2be45-414">**Reading Push**.</span></span>  <span data-ttu-id="2be45-415">El explorador está leyendo los datos locales recibidos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="2be45-415">The browser is reading the local data previously received.</span></span>  

### <span data-ttu-id="2be45-416">Ver iniciadores y dependencias</span><span class="sxs-lookup"><span data-stu-id="2be45-416">View initiators and dependencies</span></span>   

<span data-ttu-id="2be45-417">Para ver los iniciadores y las dependencias de una solicitud, mantenga presionado `Shift` el mouse sobre la solicitud en la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="2be45-417">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="2be45-418">Colores de DevTools: los iniciadores se muestran en verde y las dependencias en rojo.</span><span class="sxs-lookup"><span data-stu-id="2be45-418">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

> ##### <span data-ttu-id="2be45-419">Ilustración 26</span><span class="sxs-lookup"><span data-stu-id="2be45-419">Figure 26</span></span>  
> <span data-ttu-id="2be45-420">Visualización de los iniciadores y las dependencias de una solicitud</span><span class="sxs-lookup"><span data-stu-id="2be45-420">Viewing the initiators and dependencies of a request</span></span>  
> <span data-ttu-id="2be45-421">! [Visualización de los iniciadores y las dependencias de una solicitud] [ImageRequestInitiatorsDependencies]</span><span class="sxs-lookup"><span data-stu-id="2be45-421">![Viewing the initiators and dependencies of a request][ImageRequestInitiatorsDependencies]</span></span>  

<span data-ttu-id="2be45-422">Cuando la tabla solicitudes está ordenada cronológicamente, la primera solicitud verde por encima de la que está pasando es el iniciador de la dependencia.</span><span class="sxs-lookup"><span data-stu-id="2be45-422">When the Requests table is ordered chronologically, the first green request above the one you are hovering is the initiator of the dependency.</span></span>  <span data-ttu-id="2be45-423">Si aparece otra solicitud de color verde encima de esa, esa solicitud superior es el iniciador del iniciador.</span><span class="sxs-lookup"><span data-stu-id="2be45-423">If another green request appears above that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="2be45-424">Etcétera.</span><span class="sxs-lookup"><span data-stu-id="2be45-424">And so on.</span></span>  

### <span data-ttu-id="2be45-425">Ver eventos de carga</span><span class="sxs-lookup"><span data-stu-id="2be45-425">View load events</span></span>   

<span data-ttu-id="2be45-426">DevTools muestra la temporización de los `DOMContentLoaded` `load` eventos y en varios lugares del panel red.</span><span class="sxs-lookup"><span data-stu-id="2be45-426">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="2be45-427">El `DOMContentLoaded` evento está coloreado en azul y el `load` evento es rojo.</span><span class="sxs-lookup"><span data-stu-id="2be45-427">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

> ##### <span data-ttu-id="2be45-428">Ilustración 27</span><span class="sxs-lookup"><span data-stu-id="2be45-428">Figure 27</span></span>  
> <span data-ttu-id="2be45-429">Las ubicaciones de los `DOMContentLoaded` `load` eventos y en el panel red</span><span class="sxs-lookup"><span data-stu-id="2be45-429">The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
> <span data-ttu-id="2be45-430">! [Ubicaciones de la DOMContentLoaded y cargar eventos en el panel de red] [ImageNetworkPanelDOMContentLoadedLoadEvents]</span><span class="sxs-lookup"><span data-stu-id="2be45-430">![The locations of the DOMContentLoaded and load events on the Network panel][ImageNetworkPanelDOMContentLoadedLoadEvents]</span></span>  

### <span data-ttu-id="2be45-431">Ver el número total de solicitudes</span><span class="sxs-lookup"><span data-stu-id="2be45-431">View the total number of requests</span></span>   

<span data-ttu-id="2be45-432">El número total de solicitudes se muestra en el panel Resumen, en la parte inferior del panel red.</span><span class="sxs-lookup"><span data-stu-id="2be45-432">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="2be45-433">Este número solo realiza un seguimiento de las solicitudes que se han registrado desde que se abrió DevTools.</span><span class="sxs-lookup"><span data-stu-id="2be45-433">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="2be45-434">Si se han producido otras solicitudes antes de que se abriera DevTools, esas solicitudes no se cuentan.</span><span class="sxs-lookup"><span data-stu-id="2be45-434">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

> ##### <span data-ttu-id="2be45-435">Ilustración 28</span><span class="sxs-lookup"><span data-stu-id="2be45-435">Figure 28</span></span>  
> <span data-ttu-id="2be45-436">El número total de solicitudes desde que se abrió DevTools</span><span class="sxs-lookup"><span data-stu-id="2be45-436">The total number of requests since DevTools was opened</span></span>  
> <span data-ttu-id="2be45-437">! [El número total de solicitudes desde que se abrió DevTools] [ImageTotalRequests]</span><span class="sxs-lookup"><span data-stu-id="2be45-437">![The total number of requests since DevTools was opened][ImageTotalRequests]</span></span>  

### <span data-ttu-id="2be45-438">Ver el tamaño total de la descarga</span><span class="sxs-lookup"><span data-stu-id="2be45-438">View the total download size</span></span>   

<span data-ttu-id="2be45-439">El tamaño total de las solicitudes de descarga se muestra en el panel Resumen, en la parte inferior del panel red.</span><span class="sxs-lookup"><span data-stu-id="2be45-439">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="2be45-440">Este número solo realiza un seguimiento de las solicitudes que se han registrado desde que se abrió DevTools.</span><span class="sxs-lookup"><span data-stu-id="2be45-440">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="2be45-441">Si se han producido otras solicitudes antes de que se abriera DevTools, esas solicitudes no se cuentan.</span><span class="sxs-lookup"><span data-stu-id="2be45-441">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

> ##### <span data-ttu-id="2be45-442">Ilustración 29</span><span class="sxs-lookup"><span data-stu-id="2be45-442">Figure 29</span></span>  
> <span data-ttu-id="2be45-443">El tamaño total de las solicitudes de descarga</span><span class="sxs-lookup"><span data-stu-id="2be45-443">The total download size of requests</span></span>  
> <span data-ttu-id="2be45-444">! [El tamaño total de las solicitudes de descarga] [ImageTotalSize]</span><span class="sxs-lookup"><span data-stu-id="2be45-444">![The total download size of requests][ImageTotalSize]</span></span>  

<span data-ttu-id="2be45-445">Consulte [ver el tamaño descomprimido de un recurso](#view-the-uncompressed-size-of-a-resource) para ver cómo se encuentran los recursos grandes después de que el explorador descomprime cada elemento.</span><span class="sxs-lookup"><span data-stu-id="2be45-445">See [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource) to see how large resources are after the browser uncompresses each item.</span></span>  

### <span data-ttu-id="2be45-446">Ver el seguimiento de la pila que causó una solicitud</span><span class="sxs-lookup"><span data-stu-id="2be45-446">View the stack trace that caused a request</span></span>   

<span data-ttu-id="2be45-447">Después de que una instrucción de JavaScript solicite un recurso, mueva el puntero sobre la columna de **iniciador** para ver el seguimiento de la pila que se dirige a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2be45-447">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

<!-- [codepen.io/contoso/pen/yLBrOWa?editors=0010#0](https://codepen.io/contoso/pen/yLBrOWa?editors=0010#0) -->  

<!--
```javascript
function init() {
  getData();
}

function getData() {
  fetch('https:/httpbin.org/get?message=hi');
}

init();
```  
-->  

> ##### <span data-ttu-id="2be45-448">Ilustración 30</span><span class="sxs-lookup"><span data-stu-id="2be45-448">Figure 30</span></span>  
> <span data-ttu-id="2be45-449">El seguimiento de la pila que lleva a una solicitud de recursos</span><span class="sxs-lookup"><span data-stu-id="2be45-449">The stack trace leading up to a resource request</span></span>  
> <span data-ttu-id="2be45-450">! [El seguimiento de la pila llevado a una solicitud de recursos] [ImageInitiatorStack]</span><span class="sxs-lookup"><span data-stu-id="2be45-450">![The stack trace leading up to a resource request][ImageInitiatorStack]</span></span>  

### <span data-ttu-id="2be45-451">Ver el tamaño descomprimido de un recurso</span><span class="sxs-lookup"><span data-stu-id="2be45-451">View the uncompressed size of a resource</span></span>   

<span data-ttu-id="2be45-452">Seleccione la casilla **usar filas de solicitudes grandes** y, a continuación, mire el valor inferior de la columna **tamaño** .</span><span class="sxs-lookup"><span data-stu-id="2be45-452">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

> ##### <span data-ttu-id="2be45-453">Ilustración 31</span><span class="sxs-lookup"><span data-stu-id="2be45-453">Figure 31</span></span>  
> <span data-ttu-id="2be45-454">Un ejemplo de recursos sin comprimir \ (el tamaño comprimido del `jquery-3.3.1.min.js` archivo que se envió a través de la red fue `29.9 KB` , mientras que el tamaño descomprimido fue `84.9 KB` \)</span><span class="sxs-lookup"><span data-stu-id="2be45-454">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
> <span data-ttu-id="2be45-455">! [Un ejemplo de recursos no comprimidos] [ImageUncompressedResources]</span><span class="sxs-lookup"><span data-stu-id="2be45-455">![An example of uncompressed resources][ImageUncompressedResources]</span></span>  

## <span data-ttu-id="2be45-456">Exportar datos de solicitudes</span><span class="sxs-lookup"><span data-stu-id="2be45-456">Export requests data</span></span>   

### <span data-ttu-id="2be45-457">Guardar todas las solicitudes de red en un archivo HAR</span><span class="sxs-lookup"><span data-stu-id="2be45-457">Save all network requests to a HAR file</span></span>   

<span data-ttu-id="2be45-458">Para guardar todas las solicitudes de red en un archivo HAR:</span><span class="sxs-lookup"><span data-stu-id="2be45-458">To save all network requests to a HAR file:</span></span>  

1.  <span data-ttu-id="2be45-459">Haga clic con el botón secundario en cualquier solicitud de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="2be45-459">Right-click any request in the Requests table.</span></span>  
1.  <span data-ttu-id="2be45-460">Seleccione **Guardar como Har with Content**.</span><span class="sxs-lookup"><span data-stu-id="2be45-460">Select **Save as HAR with Content**.</span></span>  <span data-ttu-id="2be45-461">DevTools guarda todas las solicitudes que se han producido desde que abrió DevTools en el archivo HAR.</span><span class="sxs-lookup"><span data-stu-id="2be45-461">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="2be45-462">No hay ninguna manera de filtrar las solicitudes o de guardar una sola.</span><span class="sxs-lookup"><span data-stu-id="2be45-462">There is no way to filter requests, or to save just a single request.</span></span>  

<span data-ttu-id="2be45-463">Una vez que haya guardado un archivo HAR, podrá volver a importarlo en DevTools para analizarlo.</span><span class="sxs-lookup"><span data-stu-id="2be45-463">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="2be45-464">Simplemente arrastre y coloque el archivo HAR en la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="2be45-464">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

> ##### <span data-ttu-id="2be45-465">Ilustración 32</span><span class="sxs-lookup"><span data-stu-id="2be45-465">Figure 32</span></span>  
> <span data-ttu-id="2be45-466">Seleccionar Guardar como HAR with Content</span><span class="sxs-lookup"><span data-stu-id="2be45-466">Selecting Save as HAR with Content</span></span>  
> <span data-ttu-id="2be45-467">! [Seleccionando Guardar como HAR with Content] [ImageSaveAsHAR]</span><span class="sxs-lookup"><span data-stu-id="2be45-467">![Selecting Save as HAR with Content][ImageSaveAsHAR]</span></span>  

### <span data-ttu-id="2be45-468">Copiar una o más solicitudes en el portapapeles</span><span class="sxs-lookup"><span data-stu-id="2be45-468">Copy one or more requests to the clipboard</span></span>   

<span data-ttu-id="2be45-469">En la columna **nombre** de la tabla solicitudes, haga clic con el botón secundario en una solicitud, mueva el puntero sobre **copia**y seleccione una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="2be45-469">Under the **Name** column of the Requests table, right-click a request, hover over **Copy**, and select one of the following options:</span></span>  

*   <span data-ttu-id="2be45-470">**Copiar la dirección del vínculo**.</span><span class="sxs-lookup"><span data-stu-id="2be45-470">**Copy Link Address**.</span></span>  <span data-ttu-id="2be45-471">Copie la dirección URL de la solicitud en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="2be45-471">Copy the URL of the request to the clipboard.</span></span>  
*   <span data-ttu-id="2be45-472">**Copiar respuesta**.</span><span class="sxs-lookup"><span data-stu-id="2be45-472">**Copy Response**.</span></span>  <span data-ttu-id="2be45-473">Copie el cuerpo de la respuesta en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="2be45-473">Copy the response body to the clipboard.</span></span>  
*   <span data-ttu-id="2be45-474">**Copiar como fetch**.</span><span class="sxs-lookup"><span data-stu-id="2be45-474">**Copy as Fetch**.</span></span>  
*   <span data-ttu-id="2be45-475">**Copiar como rizo**.</span><span class="sxs-lookup"><span data-stu-id="2be45-475">**Copy as cURL**.</span></span>  <span data-ttu-id="2be45-476">Copie la solicitud como un comando de rizo.</span><span class="sxs-lookup"><span data-stu-id="2be45-476">Copy the request as a cURL command.</span></span>  
*   <span data-ttu-id="2be45-477">**Copiar todo como fetch**.</span><span class="sxs-lookup"><span data-stu-id="2be45-477">**Copy All as Fetch**.</span></span>  
*   <span data-ttu-id="2be45-478">**Copiar todos como rizo**.</span><span class="sxs-lookup"><span data-stu-id="2be45-478">**Copy All as cURL**.</span></span>  <span data-ttu-id="2be45-479">Copiar todas las solicitudes como una cadena de comandos de rizo.</span><span class="sxs-lookup"><span data-stu-id="2be45-479">Copy all requests as a chain of cURL commands.</span></span>  
*   <span data-ttu-id="2be45-480">**Copiar todo como Har**.</span><span class="sxs-lookup"><span data-stu-id="2be45-480">**Copy All as HAR**.</span></span>  <span data-ttu-id="2be45-481">Copie todas las solicitudes como datos de HAR.</span><span class="sxs-lookup"><span data-stu-id="2be45-481">Copy all requests as HAR data.</span></span>  

> ##### <span data-ttu-id="2be45-482">Ilustración 33</span><span class="sxs-lookup"><span data-stu-id="2be45-482">Figure 33</span></span>  
> <span data-ttu-id="2be45-483">Selección de copiar respuesta</span><span class="sxs-lookup"><span data-stu-id="2be45-483">Selecting Copy Response</span></span>  
> <span data-ttu-id="2be45-484">! [Seleccionando respuesta de copia] [ImageCopyResponse]</span><span class="sxs-lookup"><span data-stu-id="2be45-484">![Selecting Copy Response][ImageCopyResponse]</span></span>  

## <span data-ttu-id="2be45-485">Cambiar el diseño del panel red</span><span class="sxs-lookup"><span data-stu-id="2be45-485">Change the layout of the Network panel</span></span>  

<span data-ttu-id="2be45-486">Puede expandir o contraer secciones de la interfaz de usuario del panel red para destacar información importante.</span><span class="sxs-lookup"><span data-stu-id="2be45-486">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="2be45-487">Ocultar el panel de filtros</span><span class="sxs-lookup"><span data-stu-id="2be45-487">Hide the Filters pane</span></span>   

<span data-ttu-id="2be45-488">De forma predeterminada, DevTools muestra el **Panel filtros**.</span><span class="sxs-lookup"><span data-stu-id="2be45-488">By default, DevTools shows the **Filters pane**.</span></span>  
<span data-ttu-id="2be45-489">Seleccione filtro de **filtro** ![ ][ImageFilterIcon] para ocultarlo.</span><span class="sxs-lookup"><span data-stu-id="2be45-489">Select **Filter** ![Filter][ImageFilterIcon]  to hide it.</span></span>  

> ##### <span data-ttu-id="2be45-490">Ilustración 34</span><span class="sxs-lookup"><span data-stu-id="2be45-490">Figure 34</span></span>  
> <span data-ttu-id="2be45-491">El botón ocultar filtros</span><span class="sxs-lookup"><span data-stu-id="2be45-491">The Hide Filters button</span></span>  
> <span data-ttu-id="2be45-492">! [El botón ocultar filtros] [ImageHideFiltersButton]</span><span class="sxs-lookup"><span data-stu-id="2be45-492">![The Hide Filters button][ImageHideFiltersButton]</span></span>  

### <span data-ttu-id="2be45-493">Usar filas de solicitudes grandes</span><span class="sxs-lookup"><span data-stu-id="2be45-493">Use large request rows</span></span>   

<span data-ttu-id="2be45-494">Use filas grandes cuando desee más espacios en blanco en la tabla solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="2be45-494">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="2be45-495">Algunas columnas también proporcionan un poco más de información cuando se usan filas grandes.</span><span class="sxs-lookup"><span data-stu-id="2be45-495">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="2be45-496">Por ejemplo, el valor inferior de la columna **tamaño** es el tamaño descomprimido de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="2be45-496">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

> ##### <span data-ttu-id="2be45-497">Ilustración 35</span><span class="sxs-lookup"><span data-stu-id="2be45-497">Figure 35</span></span>  
> <span data-ttu-id="2be45-498">Ejemplo de filas de solicitudes grandes en el panel solicitudes</span><span class="sxs-lookup"><span data-stu-id="2be45-498">An example of large request rows in the Requests pane</span></span>  
> <span data-ttu-id="2be45-499">! [Un ejemplo de filas de solicitudes grandes en el panel solicitudes] [ImageLargeRequestRows]</span><span class="sxs-lookup"><span data-stu-id="2be45-499">![An example of large request rows in the Requests pane][ImageLargeRequestRows]</span></span>  

<span data-ttu-id="2be45-500">Seleccione la casilla **usar filas de solicitudes grandes** para habilitar las filas grandes.</span><span class="sxs-lookup"><span data-stu-id="2be45-500">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

> ##### <span data-ttu-id="2be45-501">Ilustración 36</span><span class="sxs-lookup"><span data-stu-id="2be45-501">Figure 36</span></span>  
> <span data-ttu-id="2be45-502">Casilla de verificación filas de solicitudes grandes</span><span class="sxs-lookup"><span data-stu-id="2be45-502">The Large Request Rows checkbox</span></span>  
> <span data-ttu-id="2be45-503">! [Casilla de verificación filas de solicitudes grandes] [ImageLargeRequestRowsCheckbox]</span><span class="sxs-lookup"><span data-stu-id="2be45-503">![The Large Request Rows checkbox][ImageLargeRequestRowsCheckbox]</span></span>  

### <span data-ttu-id="2be45-504">Ocultar el panel de información general</span><span class="sxs-lookup"><span data-stu-id="2be45-504">Hide the Overview pane</span></span>   

<span data-ttu-id="2be45-505">De forma predeterminada, DevTools muestra el **Panel de información general**.</span><span class="sxs-lookup"><span data-stu-id="2be45-505">By default, DevTools shows the **Overview pane**.</span></span>  
<span data-ttu-id="2be45-506">Anule la selección de la casilla **Mostrar información general** para ocultarla.</span><span class="sxs-lookup"><span data-stu-id="2be45-506">Deselect the **Show Overview** checkbox to hide it.</span></span>  

> ##### <span data-ttu-id="2be45-507">Ilustración 37</span><span class="sxs-lookup"><span data-stu-id="2be45-507">Figure 37</span></span>  
> <span data-ttu-id="2be45-508">La casilla Mostrar información general</span><span class="sxs-lookup"><span data-stu-id="2be45-508">The Show Overview checkbox</span></span>  
> <span data-ttu-id="2be45-509">! [La casilla Mostrar información general] [ImageHideOverviewCheckbox]</span><span class="sxs-lookup"><span data-stu-id="2be45-509">![The Show Overview checkbox][ImageHideOverviewCheckbox]</span></span>  

<!-->   -->  

  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-requests-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageHideIcon]: /microsoft-edge/devtools-guide-chromium/media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: /microsoft-edge/devtools-guide-chromium/media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: /microsoft-edge/devtools-guide-chromium/media/record-on-icon.msft.png  

[ImageNetworkPanel]: /microsoft-edge/devtools-guide-chromium/media/network-network-panel.msft.png "Ilustración 1: panel de red"  
[ImageClearButton]: /microsoft-edge/devtools-guide-chromium/media/network-network-clear-button.msft.png "Ilustración 2: el botón borrar"  
[ImagePreserveLogCheckBox]: /microsoft-edge/devtools-guide-chromium/media/network-network-preserve-log.msft.png "Figura 3: casilla de verificación conservar registro"  
[ImageScreenshotHover]: /microsoft-edge/devtools-guide-chromium/media/network-network-screenshot-hover.msft.png "Ilustración 4: mantener el puntero sobre una captura de pantalla"  
<!--[ImageReplayXHR]: /microsoft-edge/devtools-guide-chromium/media/network-replay-xhr.msft.png "Old Figure 5: Selecting Replay XHR"  -->  
[ImageDisableCacheCheckBox]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Disable-cache-CheckBox.msft.png "Figura 5: casilla deshabilitar la caché"  
[ImageClearBrowserCache]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Clear-Browser-cache.msft.png "Ilustración 6: selección de la caché de borrar explorador"  
[ImageOfflineDropdown]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-offline-DropDown.msft.png "Figura 7: menú desplegable sin conexión"  
[ImageNetworkThrottlingMenu]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-throttling-menu.msft.png "Ilustración 8: el menú de limitación de redes"  
[ImageClearBrowserCookies]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Clear-Browser-cookies.msft.png "Ilustración 9: selección de las cookies de borrar explorador"  
[ImageFilterTextBox]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-filters-TextBox.msft.png "Figura 10: el cuadro de texto filtros"  
[ImageMultiTypeFilter]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Type-filters.msft.png "ilustración 11: usar los filtros de tipo para mostrar JS, CSS y recursos de documento"  
[ImageOverviewFilter]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Overview-Filter.msft.png "Ilustración 12: filtrar las solicitudes que estaban inactivas en 300ms"  
[ImageHideDataURLsCheckBox]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Hide-Data-URLs.msft.png "ilustración 13: la casilla ocultar direcciones URL de datos"  
[ImageWaterfallTotalDuration]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Waterfall-total-Duration.msft.png "Ilustración 14: ordenar la cascada por duración total"  
[ImageRequestsTable]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Table.msft.png "Ilustración 15: la tabla solicitudes"  
[ImageRequestsTableAddColumn]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Add-Column.msft.png "Ilustración 16: agregar una columna a la tabla solicitudes"  
[ImageRequestsTableCustomColumn]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Add-Custom.msft.png "Ilustración 17: agregar una columna personalizada a la tabla solicitudes"  
[ImageRequestsTableWaterfallColumn]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Waterfall.msft.png "ilustración 18: la columna cascada del panel solicitudes"  
[ImagePreview]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Resources-Preview.msft.png "Ilustración 19: la pestaña vista previa"  
<!--[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/network-frames.msft.png "Old Figure 20: The Frames tab"  -->  
[ImageResponse]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Resources-Response.msft.png "Ilustración 20: la pestaña respuesta"  
[ImageHeaders]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Resources-headers.msft.png "ilustración 21: la pestaña encabezados"  
[ImageQueryStringParameters]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Resources-headers-Query-String-Parameters.msft.png "figura 22: sección de parámetros de cadena de consulta"  
[ImageCookies]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Resources-cookies.msft.png "Ilustración 23: la ficha cookies"  
[ImageTiming]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Resources-Timing.msft.png "Ilustración 24: ficha intervalos"  
[ImageWaterfallHover]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Resources-Waterfall-Hover.msft.png "Ilustración 25: obtener una vista previa del desglose de intervalos de una solicitud"  
[ImageRequestInitiatorsDependencies]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Resources-Initiators-dependencies.msft.png "ilustración 26: visualización de los iniciadores y las dependencias de una solicitud"  
[ImageNetworkPanelDOMContentLoadedLoadEvents]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Load-Events.msft.png "Ilustración 27: las ubicaciones de los DOMContentLoaded y cargar eventos en el panel de red"  
[ImageTotalRequests]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-total-requests.msft.png "Ilustración 28: el número total de solicitudes desde que se abrió DevTools"  
[ImageTotalSize]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-total-download-size.msft.png "Ilustración 29: el tamaño total de las solicitudes de descarga"  
[ImageInitiatorStack]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Initiator-Stack.msft.png "Ilustración 30: el seguimiento de pila que lleva a una solicitud de recurso"  
[ImageUncompressedResources]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Uncompressed-Compare.msft.png "Ilustración 31: un ejemplo de recursos sin comprimir"  
[ImageSaveAsHAR]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Save-har-Content.msft.png "ilustración 32: seleccionar Guardar como HAR with Content"  
[ImageCopyResponse]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Copy-Response.msft.png "Ilustración 33: selección de la respuesta de copia"  
[ImageHideFiltersButton]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-Resources-Hide-filters-Button.msft.png "figura 34: el botón ocultar filtros"  
[ImageLargeRequestRows]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-Large-request-Rows.msft.png "Ilustración 35: un ejemplo de filas de solicitudes grandes en el panel solicitudes"  
[ImageLargeRequestRowsCheckbox]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-use-Large-request-Rows-on.msft.png "Ilustración 36: casilla de verificación filas de gran tamaño"  
[ImageHideOverviewCheckbox]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Network-Network-requests-show-Overview-OFF.msft.png "Ilustración 37: la casilla ocultar Descripción general"  

<!-- links -->  

[DevtoolsProgressiveWebApps]: /microsoft-edge/devtools-guide-chromium/network/progressive-web-apps "Depurar aplicaciones web progresivas"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "Direcciones URL de datos | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Servidor proxy-Wikipedia"  

> [!NOTE]
> <span data-ttu-id="2be45-550">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2be45-550">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2be45-551">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/network/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="2be45-551">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2be45-553">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2be45-553">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

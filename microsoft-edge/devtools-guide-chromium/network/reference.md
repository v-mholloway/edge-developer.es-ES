---
title: Referencia de análisis de red
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: ec8969fbf7b54512f00120ac4a253b952c55768f
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844022"
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

# <span data-ttu-id="98919-103">Referencia de análisis de red</span><span class="sxs-lookup"><span data-stu-id="98919-103">Network Analysis Reference</span></span>  

<span data-ttu-id="98919-104">Descubra nuevas formas de analizar cómo se carga su página en esta referencia completa de las características de análisis de red de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="98919-104">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  Check `edge://help` to see what version of Microsoft Edge you are running.  
-->

## <span data-ttu-id="98919-105">Registrar solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="98919-105">Record network requests</span></span>  

<span data-ttu-id="98919-106">De forma predeterminada, DevTools registra todas las solicitudes de red en el panel red, siempre y cuando DevTools esté abierto.</span><span class="sxs-lookup"><span data-stu-id="98919-106">By default, DevTools records all network requests in the Network panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Panel red" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="98919-108">Ilustración 1: panel de **red**</span><span class="sxs-lookup"><span data-stu-id="98919-108">Figure 1:  The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-109">Detener la grabación de solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="98919-109">Stop recording network requests</span></span>  

<span data-ttu-id="98919-110">Siga los pasos que se indican a continuación para detener la grabación de solicitudes.</span><span class="sxs-lookup"><span data-stu-id="98919-110">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="98919-111">Seleccione **Detener grabación registro de red** ![ detener la grabación del registro ][ImageRecordOnIcon] de red en el panel **red** .</span><span class="sxs-lookup"><span data-stu-id="98919-111">Select **Stop recording network log** ![Stop recording network log][ImageRecordOnIcon] on the **Network** panel.</span></span>  <span data-ttu-id="98919-112">Se vuelve gris para indicar que DevTools ya no graba solicitudes.</span><span class="sxs-lookup"><span data-stu-id="98919-112">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="98919-113">Pulse `Control` + `E` \ (Windows \) o `Command` + `E` \ (MacOS \) mientras el panel **red** está en el foco.</span><span class="sxs-lookup"><span data-stu-id="98919-113">Press `Control`+`E` \(Windows\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="98919-114">Borrar solicitudes</span><span class="sxs-lookup"><span data-stu-id="98919-114">Clear requests</span></span>  

<span data-ttu-id="98919-115">Seleccione **Borrar** ![ Borrar ][ImageClearIcon] en el panel red para borrar todas las solicitudes de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="98919-115">Select **Clear** ![Clear][ImageClearIcon] on the Network panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Botón borrar" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="98919-117">Ilustración 2: el botón **Borrar**</span><span class="sxs-lookup"><span data-stu-id="98919-117">Figure 2:  The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-118">Guardar solicitudes en la carga de páginas</span><span class="sxs-lookup"><span data-stu-id="98919-118">Save requests across page loads</span></span>  

<span data-ttu-id="98919-119">Para guardar las solicitudes en la carga de la página, active la casilla **conservar registro** en el panel red.</span><span class="sxs-lookup"><span data-stu-id="98919-119">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="98919-120">DevTools guarda todas las solicitudes hasta que Deshabilites **conservar registro**.</span><span class="sxs-lookup"><span data-stu-id="98919-120">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Casilla de verificación conservar registro" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="98919-122">Figura 3: casilla de verificación **conservar registro**</span><span class="sxs-lookup"><span data-stu-id="98919-122">Figure 3:  The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-123">Capturar capturas de pantallas durante la carga de la página</span><span class="sxs-lookup"><span data-stu-id="98919-123">Capture screenshots during page load</span></span>  

<span data-ttu-id="98919-124">Capture las capturas de pantallas para analizar lo que los usuarios ven al esperar a que se cargue la página.</span><span class="sxs-lookup"><span data-stu-id="98919-124">Capture screenshots to analyze what users see as they wait for your page to load.</span></span>  

<span data-ttu-id="98919-125">Para habilitar capturas de pantalla, seleccione **configuración de red** y marque la casilla **capturar capturas** de pantalla en el panel **red** .</span><span class="sxs-lookup"><span data-stu-id="98919-125">To enable screenshots, select **Network settings** and select **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="98919-126">Actualice la página mientras el panel **red** está enfocado para capturar capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="98919-126">Refresh the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="98919-127">Después de capturar una captura de pantalla, puede interactuar con ella de las siguientes maneras.</span><span class="sxs-lookup"><span data-stu-id="98919-127">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="98919-128">Desplace el puntero sobre una captura de pantalla para ver el punto en el que se capturó la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="98919-128">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="98919-129">Aparece una línea amarilla en el panel de **información general** .</span><span class="sxs-lookup"><span data-stu-id="98919-129">A yellow line appears on the **Overview** pane.</span></span>  
*   <span data-ttu-id="98919-130">Seleccione la miniatura de una pantalla para filtrar las solicitudes que se produjeron después de que se capturó la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="98919-130">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="98919-131">Haga doble clic en una miniatura para acercarla.</span><span class="sxs-lookup"><span data-stu-id="98919-131">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Colocar el puntero sobre una captura de pantalla" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="98919-133">Ilustración 4: mantener el puntero sobre una captura de pantalla</span><span class="sxs-lookup"><span data-stu-id="98919-133">Figure 4:  Hovering over a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and select **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Selecting Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Old Figure 5:  Selecting Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="98919-134">Cambiar el comportamiento de carga</span><span class="sxs-lookup"><span data-stu-id="98919-134">Change loading behavior</span></span>  

### <span data-ttu-id="98919-135">Emular a un primer visitante mediante la deshabilitación de la memoria caché del explorador</span><span class="sxs-lookup"><span data-stu-id="98919-135">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="98919-136">Para emular el funcionamiento de su sitio por primera vez, active la casilla **deshabilitar la caché** .</span><span class="sxs-lookup"><span data-stu-id="98919-136">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="98919-137">DevTools deshabilita la caché del explorador.</span><span class="sxs-lookup"><span data-stu-id="98919-137">DevTools disables the browser cache.</span></span>  <span data-ttu-id="98919-138">Esto emula con más precisión la experiencia de un usuario por primera vez, ya que las solicitudes se proporcionan desde la memoria caché del explorador en las visitas repetidas.</span><span class="sxs-lookup"><span data-stu-id="98919-138">This more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Casilla deshabilitar caché" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="98919-140">Ilustración 5: la casilla de verificación **deshabilitar caché**</span><span class="sxs-lookup"><span data-stu-id="98919-140">Figure 5:  The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="98919-141">Deshabilitar la memoria caché del explorador en el cajón de condiciones de red</span><span class="sxs-lookup"><span data-stu-id="98919-141">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="98919-142">Si desea deshabilitar la caché mientras trabaja en otros paneles de DevTools, use el cajón de condiciones de redes.</span><span class="sxs-lookup"><span data-stu-id="98919-142">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="98919-143">Abra el cajón de **condiciones de redes** .</span><span class="sxs-lookup"><span data-stu-id="98919-143">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="98919-144">Active o desactive la casilla **deshabilitar caché** .</span><span class="sxs-lookup"><span data-stu-id="98919-144">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="98919-145">Borrar manualmente la memoria caché del explorador</span><span class="sxs-lookup"><span data-stu-id="98919-145">Manually clear the browser cache</span></span>  

<span data-ttu-id="98919-146">Para borrar manualmente la memoria caché del explorador en cualquier momento, abra el menú contextual \ (haga clic con el botón secundario del mouse \) en cualquier lugar de la tabla solicitudes y seleccione **Borrar caché del explorador**.</span><span class="sxs-lookup"><span data-stu-id="98919-146">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Selección de borrar caché del explorador" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="98919-148">Ilustración 6: selección de la **caché de borrar explorador**</span><span class="sxs-lookup"><span data-stu-id="98919-148">Figure 6:  Selecting **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-149">Emular sin conexión</span><span class="sxs-lookup"><span data-stu-id="98919-149">Emulate offline</span></span>  

<span data-ttu-id="98919-150">Una nueva clase de aplicaciones Web, denominada [aplicaciones web progresivas][DevtoolsProgressiveWebApps], funciona sin conexión con la ayuda de los **trabajadores de servicio**.</span><span class="sxs-lookup"><span data-stu-id="98919-150">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="98919-151">Es posible que le resulte útil simular rápidamente un dispositivo que no tiene conexión de datos cuando está creando este tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="98919-151">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="98919-152">Seleccione el menú desplegable **en línea** , búsqueda en **preestablecidos**y seleccione **sin conexión** para simular una experiencia de red completamente desconectada.</span><span class="sxs-lookup"><span data-stu-id="98919-152">Select the **Online** dropdown menu, search under **Presets**, and select **Offline** to simulate a completely offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Menú desplegable desconectado" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="98919-154">Ilustración 7: el menú desplegable **desconectado**</span><span class="sxs-lookup"><span data-stu-id="98919-154">Figure 7:  The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-155">Emular conexiones de red lentas</span><span class="sxs-lookup"><span data-stu-id="98919-155">Emulate slow network connections</span></span>  

<span data-ttu-id="98919-156">Emular 3G lento, 3G rápido y otras velocidades de conexión en el menú desplegable **en línea** .</span><span class="sxs-lookup"><span data-stu-id="98919-156">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="El menú desplegable limitación de peticiones" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="98919-158">Ilustración 8: el menú desplegable **limitación de peticiones**</span><span class="sxs-lookup"><span data-stu-id="98919-158">Figure 8:  The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="98919-159">Puedes elegir entre una variedad de ajustes preestablecidos, como 3G lento o 3G rápido.</span><span class="sxs-lookup"><span data-stu-id="98919-159">You may select from a variety of presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="98919-160">También puede agregar sus propios ajustes preestablecidos personalizados abriendo el menú de limitación y seleccionando **Custom**  >  **añadir**personalizados.</span><span class="sxs-lookup"><span data-stu-id="98919-160">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="98919-161">DevTools muestra un icono de advertencia junto a la pestaña **red** para recordarle que la limitación está habilitada.</span><span class="sxs-lookup"><span data-stu-id="98919-161">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="98919-162">Emular conexiones de red lentas del cajón de condiciones de red</span><span class="sxs-lookup"><span data-stu-id="98919-162">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="98919-163">Si desea limitar la conexión de red mientras trabaja en otros paneles de DevTools, use el cajón de condiciones de redes.</span><span class="sxs-lookup"><span data-stu-id="98919-163">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="98919-164">Abra el cajón de **condiciones de redes** .</span><span class="sxs-lookup"><span data-stu-id="98919-164">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="98919-165">Seleccione la velocidad de conexión que desee en el menú **limitación** .</span><span class="sxs-lookup"><span data-stu-id="98919-165">Select your desired connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="98919-166">Borrar manualmente las cookies del explorador</span><span class="sxs-lookup"><span data-stu-id="98919-166">Manually clear browser cookies</span></span>  

<span data-ttu-id="98919-167">Para borrar manualmente las cookies del explorador en cualquier momento, abra el menú contextual \ (haga clic con el botón secundario del mouse \) en cualquier lugar de la tabla solicitudes y seleccione **Borrar cookies del explorador**.</span><span class="sxs-lookup"><span data-stu-id="98919-167">To manually clear browser cookies at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Selección de las cookies de borrar explorador" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="98919-169">Ilustración 9: selección de las **cookies de borrar explorador**</span><span class="sxs-lookup"><span data-stu-id="98919-169">Figure 9:  Selecting **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-170">Invalidar el agente de usuario</span><span class="sxs-lookup"><span data-stu-id="98919-170">Override the user agent</span></span>  

<span data-ttu-id="98919-171">Para anular manualmente el agente de usuario:</span><span class="sxs-lookup"><span data-stu-id="98919-171">To manually override the user agent:</span></span>  

1.  <span data-ttu-id="98919-172">Abra el cajón de **condiciones de redes** .</span><span class="sxs-lookup"><span data-stu-id="98919-172">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="98919-173">Desactive **seleccionar automáticamente**.</span><span class="sxs-lookup"><span data-stu-id="98919-173">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="98919-174">Elija una opción de agente de usuario en el menú o escriba una personalizada en el cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="98919-174">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="98919-175">Filtrar solicitudes</span><span class="sxs-lookup"><span data-stu-id="98919-175">Filter requests</span></span>  

### <span data-ttu-id="98919-176">Filtrar las solicitudes por propiedades</span><span class="sxs-lookup"><span data-stu-id="98919-176">Filter requests by properties</span></span>  

<span data-ttu-id="98919-177">Use el cuadro de texto **filtrar** para filtrar las solicitudes por propiedades, como el dominio o el tamaño de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="98919-177">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="98919-178">Si no ve el cuadro de texto, es probable que el panel filtros esté oculto.</span><span class="sxs-lookup"><span data-stu-id="98919-178">If you do not see the text box, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="98919-179">Consulte [ocultar el panel de filtros](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="98919-179">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="El cuadro de texto filtro" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="98919-181">Ilustración 10: el cuadro de texto **filtro**</span><span class="sxs-lookup"><span data-stu-id="98919-181">Figure 10:  The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="98919-182">Puede usar varias propiedades simultáneamente al separar cada propiedad con un espacio.</span><span class="sxs-lookup"><span data-stu-id="98919-182">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="98919-183">Por ejemplo, `mime-type:image/png larger-than:1K` se muestran todos los PNGs que tengan más de un kilobyte.</span><span class="sxs-lookup"><span data-stu-id="98919-183">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than one kilobyte.</span></span>  <span data-ttu-id="98919-184">Estos filtros de varias propiedades son equivalentes a `AND` las operaciones.</span><span class="sxs-lookup"><span data-stu-id="98919-184">These multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="98919-185">Actualmente no se admiten las operaciones.</span><span class="sxs-lookup"><span data-stu-id="98919-185">operations are currently not supported.</span></span>  

<span data-ttu-id="98919-186">La lista completa de propiedades compatibles.</span><span class="sxs-lookup"><span data-stu-id="98919-186">The complete list of supported properties.</span></span>  

| <span data-ttu-id="98919-187">Propiedad</span><span class="sxs-lookup"><span data-stu-id="98919-187">Property</span></span> | <span data-ttu-id="98919-188">Detalles</span><span class="sxs-lookup"><span data-stu-id="98919-188">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="98919-189">Mostrar solo los recursos del dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="98919-189">Only display resources from the specified domain.</span></span>  <span data-ttu-id="98919-190">Puede usar un carácter comodín \ ( `*` \) para incluir varios dominios.</span><span class="sxs-lookup"><span data-stu-id="98919-190">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="98919-191">Por ejemplo, `*.com` muestra los recursos de todos los nombres de dominio que terminan en `.com` .</span><span class="sxs-lookup"><span data-stu-id="98919-191">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="98919-192">DevTools rellena el menú desplegable de autocompletar con todos los dominios que ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="98919-192">DevTools populates the autocomplete dropdown menu with all of the domains it has encountered.</span></span> |  
| `has-response-header` | <span data-ttu-id="98919-193">Mostrar los recursos que contienen el encabezado de respuesta HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="98919-193">Show the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="98919-194">DevTools rellena la lista desplegable de autocompletar con todos los encabezados de respuesta que ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="98919-194">DevTools populates the autocomplete dropdown with all of the response headers that it has encountered.</span></span> |  
| `is` | <span data-ttu-id="98919-195">Usar `is:running` para buscar `WebSocket` recursos.</span><span class="sxs-lookup"><span data-stu-id="98919-195">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="98919-196">Mostrar recursos mayores que el tamaño especificado, en bytes.</span><span class="sxs-lookup"><span data-stu-id="98919-196">Show resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="98919-197">Establecer un valor de `1000` es equivalente a establecer un valor de `1k` .</span><span class="sxs-lookup"><span data-stu-id="98919-197">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="98919-198">Mostrar recursos que se recuperaron en un tipo de método HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="98919-198">Show resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="98919-199">DevTools rellena la lista desplegable con todos los métodos HTTP que ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="98919-199">DevTools populates the dropdown with all of the HTTP methods it has encountered.</span></span> |  
| `mime-type` | <span data-ttu-id="98919-200">Mostrar los recursos de un tipo MIME especificado.</span><span class="sxs-lookup"><span data-stu-id="98919-200">Show resources of a specified MIME type.</span></span>  <span data-ttu-id="98919-201">DevTools rellena la lista desplegable con todos los tipos MIME que ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="98919-201">DevTools populates the dropdown with all MIME types it has encountered.</span></span> |  
| `mixed-content` | <span data-ttu-id="98919-202">Mostrar todos los recursos de contenido mixto \ ( `mixed-content:all` \) o solo los que se muestran actualmente \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="98919-202">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="98919-203">Mostrar los recursos recuperados en HTTP \ ( `scheme:http` \) no protegidos o en https \ ( `scheme:https` \).</span><span class="sxs-lookup"><span data-stu-id="98919-203">Show resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="98919-204">Mostrar los recursos que tienen un `Set-Cookie` encabezado con un `Domain` atributo que coincide con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="98919-204">Show the resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="98919-205">DevTools rellena el autocompletar con todos los dominios de cookies que ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="98919-205">DevTools populates the autocomplete with all of the cookie domains that it has encountered.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="98919-206">Mostrar los recursos que tengan un `Set-Cookie` encabezado con un nombre que coincida con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="98919-206">Show the resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="98919-207">DevTools rellena la autocompletar con todos los nombres de cookies que ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="98919-207">DevTools populates the autocomplete with all of the cookie names that it has encountered.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="98919-208">Mostrar los recursos que tienen un `Set-Cookie` encabezado con un valor que coincide con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="98919-208">Show the resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="98919-209">DevTools rellena el autocompletar con todos los valores de cookie que ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="98919-209">DevTools populates the autocomplete with all of the cookie values that it has encountered.</span></span> |  
| `status-code` | <span data-ttu-id="98919-210">Mostrar solo los recursos para los que el código de Estado HTTP coincide con el código especificado.</span><span class="sxs-lookup"><span data-stu-id="98919-210">Show only the resources for which the HTTP status code matches the specified code.</span></span>  <span data-ttu-id="98919-211">DevTools rellena el menú desplegable de autocompletar con todos los códigos de estado que ha encontrado.</span><span class="sxs-lookup"><span data-stu-id="98919-211">DevTools populates the autocomplete dropdown menu with all of the status codes it has encountered.</span></span> |  

### <span data-ttu-id="98919-212">Filtrar solicitudes por tipo</span><span class="sxs-lookup"><span data-stu-id="98919-212">Filter requests by type</span></span>  

<span data-ttu-id="98919-213">Para filtrar las solicitudes según el tipo de solicitud, seleccione los botones **XHR**, **JS**, **CSS**, **IMG**, **multimedia**, **fuente**, **documento**, **WS** \ (WebSocket \), **manifiesto**u **otros** \ (cualquier otro tipo no incluido aquí \) en el panel red.</span><span class="sxs-lookup"><span data-stu-id="98919-213">To filter requests by request type, select the **XHR**, **JS**, **CSS**, **Img**, **Media**, **Font**, **Doc**, **WS** \(WebSocket\), **Manifest**, or **Other** \(any other type not listed here\) buttons on the Network panel.</span></span>  

<span data-ttu-id="98919-214">Si no ve estos botones, es probable que el panel filtros esté oculto.</span><span class="sxs-lookup"><span data-stu-id="98919-214">If you do not see these buttons, the Filters pane is probably hidden.</span></span>  
<span data-ttu-id="98919-215">Consulte [ocultar el panel de filtros](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="98919-215">See [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="98919-216">Para habilitar varios filtros de tipo al mismo tiempo, mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y, a continuación, seleccione.</span><span class="sxs-lookup"><span data-stu-id="98919-216">To enable multiple type filters simultaneously, hold `Control` \(Windows\) or `Command` \(macOS\) and then select.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Usar los filtros de tipo para mostrar los recursos JS, CSS y Document" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="98919-218">Ilustración 11: usar los filtros de tipo para mostrar los recursos de JS, CSS y de documento</span><span class="sxs-lookup"><span data-stu-id="98919-218">Figure 11:  Using the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-219">Filtrar solicitudes por tiempo</span><span class="sxs-lookup"><span data-stu-id="98919-219">Filter requests by time</span></span>  

<span data-ttu-id="98919-220">Seleccione y arrastre a la izquierda o a la derecha en el panel de descripción para mostrar solo las solicitudes que estaban activas durante ese período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="98919-220">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="98919-221">El filtro es inclusivo.</span><span class="sxs-lookup"><span data-stu-id="98919-221">The filter is inclusive.</span></span>  <span data-ttu-id="98919-222">Se muestra cualquier solicitud que estuviera activa durante la hora resaltada.</span><span class="sxs-lookup"><span data-stu-id="98919-222">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Filtrar las solicitudes inactivas en 300ms" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="98919-224">Ilustración 12: filtrar las solicitudes que estaban inactivas en 300ms</span><span class="sxs-lookup"><span data-stu-id="98919-224">Figure 12:  Filtering out any requests that were inactive around 300ms</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-225">Ocultar direcciones URL de datos</span><span class="sxs-lookup"><span data-stu-id="98919-225">Hide data URLs</span></span>  

<span data-ttu-id="98919-226">Las [direcciones URL de datos][MDNHTTPDataURIs] son pequeños archivos incrustados en otros documentos.</span><span class="sxs-lookup"><span data-stu-id="98919-226">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="98919-227">Cualquier solicitud que vea en la tabla solicitudes que comienza por `data:` es una dirección URL de datos.</span><span class="sxs-lookup"><span data-stu-id="98919-227">Any request that you see in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="98919-228">Active la casilla **ocultar direcciones URL de datos** para ocultar las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="98919-228">Check the **Hide data URLs** checkbox to hide the requests.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="La casilla ocultar direcciones URL de datos" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="98919-230">Ilustración 13: la casilla **ocultar direcciones URL de datos**</span><span class="sxs-lookup"><span data-stu-id="98919-230">Figure 13:  The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="98919-231">Ordenar solicitudes</span><span class="sxs-lookup"><span data-stu-id="98919-231">Sort requests</span></span>  

<span data-ttu-id="98919-232">De forma predeterminada, las solicitudes de la tabla solicitudes se ordenan por hora de inicio, pero puede ordenar la tabla mediante otros criterios.</span><span class="sxs-lookup"><span data-stu-id="98919-232">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="98919-233">Ordenar por columna</span><span class="sxs-lookup"><span data-stu-id="98919-233">Sort by column</span></span>  

<span data-ttu-id="98919-234">Seleccione el encabezado de cualquier columna en las solicitudes para ordenar las solicitudes por esa columna.</span><span class="sxs-lookup"><span data-stu-id="98919-234">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="98919-235">Ordenar por fase de actividad</span><span class="sxs-lookup"><span data-stu-id="98919-235">Sort by activity phase</span></span>  

<span data-ttu-id="98919-236">Para cambiar la forma en que la cascada ordena las solicitudes, desplace el puntero sobre el encabezado de la tabla solicitudes, abra el menú contextual \ (haga clic con el botón derecho \), desplace el puntero sobre la **cascada**y seleccione una de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="98919-236">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover over **Waterfall**, and select one of the following options.</span></span>  

*   <span data-ttu-id="98919-237">**Hora de inicio**.</span><span class="sxs-lookup"><span data-stu-id="98919-237">**Start Time**.</span></span>  <span data-ttu-id="98919-238">La primera solicitud iniciada se encuentra en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="98919-238">The first request that was initiated is at the top.</span></span>  
*   <span data-ttu-id="98919-239">**Tiempo de respuesta**.</span><span class="sxs-lookup"><span data-stu-id="98919-239">**Response Time**.</span></span>  <span data-ttu-id="98919-240">La primera solicitud que comenzó a descargarse está en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="98919-240">The first request that started downloading is at the top.</span></span>  
*   <span data-ttu-id="98919-241">**Hora de finalización**.</span><span class="sxs-lookup"><span data-stu-id="98919-241">**End Time**.</span></span>  <span data-ttu-id="98919-242">La primera solicitud que ha finalizado se encuentra en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="98919-242">The first request that finished is at the top.</span></span>  
*   <span data-ttu-id="98919-243">**Duración total**.</span><span class="sxs-lookup"><span data-stu-id="98919-243">**Total Duration**.</span></span>  <span data-ttu-id="98919-244">La solicitud con la configuración de conexión más corta y la solicitud o respuesta se encuentra en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="98919-244">The request with the shortest connection setup and request / response is at the top.</span></span>  
*   <span data-ttu-id="98919-245">**Latencia**.</span><span class="sxs-lookup"><span data-stu-id="98919-245">**Latency**.</span></span>  <span data-ttu-id="98919-246">La solicitud que esperó el tiempo más breve para una respuesta está en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="98919-246">The request that waited the shortest time for a response is at the top.</span></span>  

<span data-ttu-id="98919-247">En estas descripciones se supone que cada opción respectiva está clasificada de menor a mayor.</span><span class="sxs-lookup"><span data-stu-id="98919-247">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="98919-248">Al seleccionar el encabezado de la columna **cascada** se invierte el orden.</span><span class="sxs-lookup"><span data-stu-id="98919-248">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Ordenar la cascada por duración total" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="98919-250">Ilustración 14: ordenar la cascada por duración total \ (la parte más clara de cada barra está en espera y la parte más oscura es el tiempo dedicado a descargar bytes \)</span><span class="sxs-lookup"><span data-stu-id="98919-250">Figure 14:  Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="98919-251">Analizar solicitudes</span><span class="sxs-lookup"><span data-stu-id="98919-251">Analyze requests</span></span>  

<span data-ttu-id="98919-252">Siempre que DevTools esté abierto, registra todas las solicitudes en el panel de red.</span><span class="sxs-lookup"><span data-stu-id="98919-252">So long as DevTools is open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="98919-253">Use el panel red para analizar las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="98919-253">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="98919-254">Ver un registro de solicitudes</span><span class="sxs-lookup"><span data-stu-id="98919-254">View a log of requests</span></span>  

<span data-ttu-id="98919-255">Use la tabla solicitudes para ver un registro de todas las solicitudes realizadas mientras se ha abierto DevTools.</span><span class="sxs-lookup"><span data-stu-id="98919-255">Use the Requests table to view a log of all requests made while DevTools has been open.</span></span>  <span data-ttu-id="98919-256">Al seleccionar o mantener el puntero sobre solicitudes, se muestra más información sobre cada elemento.</span><span class="sxs-lookup"><span data-stu-id="98919-256">Selecting or hovering over requests reveals more information about each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="La tabla solicitudes" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="98919-258">Ilustración 15: la tabla solicitudes</span><span class="sxs-lookup"><span data-stu-id="98919-258">Figure 15:  The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="98919-259">De forma predeterminada, en la tabla solicitudes se muestran las siguientes columnas.</span><span class="sxs-lookup"><span data-stu-id="98919-259">The Requests table displays the following columns by default.</span></span>  

*   <span data-ttu-id="98919-260">**Nombre**.</span><span class="sxs-lookup"><span data-stu-id="98919-260">**Name**.</span></span>  <span data-ttu-id="98919-261">El nombre de archivo de un recurso o un identificador de él.</span><span class="sxs-lookup"><span data-stu-id="98919-261">The filename of, or an identifier for, the resource.</span></span>  
*   <span data-ttu-id="98919-262">**Estado**.</span><span class="sxs-lookup"><span data-stu-id="98919-262">**Status**.</span></span>  <span data-ttu-id="98919-263">El código de Estado HTTP.</span><span class="sxs-lookup"><span data-stu-id="98919-263">The HTTP status code.</span></span>  
*   <span data-ttu-id="98919-264">**Tipo**.</span><span class="sxs-lookup"><span data-stu-id="98919-264">**Type**.</span></span>  <span data-ttu-id="98919-265">Tipo MIME del recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="98919-265">The MIME type of the requested resource.</span></span>  
*   <span data-ttu-id="98919-266">**Iniciador**.</span><span class="sxs-lookup"><span data-stu-id="98919-266">**Initiator**.</span></span>  <span data-ttu-id="98919-267">Los siguientes objetos o procesos inician solicitudes:</span><span class="sxs-lookup"><span data-stu-id="98919-267">The following objects or processes initiate requests:</span></span>  
    *   <span data-ttu-id="98919-268">**Parser**.</span><span class="sxs-lookup"><span data-stu-id="98919-268">**Parser**.</span></span>  <span data-ttu-id="98919-269">El analizador HTML para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="98919-269">The HTML parser for Microsoft Edge.</span></span>  
    *   <span data-ttu-id="98919-270">**Redirigir**.</span><span class="sxs-lookup"><span data-stu-id="98919-270">**Redirect**.</span></span>  <span data-ttu-id="98919-271">Una redirección de HTTP.</span><span class="sxs-lookup"><span data-stu-id="98919-271">An HTTP redirect.</span></span>  
    *   <span data-ttu-id="98919-272">**Script**.</span><span class="sxs-lookup"><span data-stu-id="98919-272">**Script**.</span></span>  <span data-ttu-id="98919-273">Una función de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="98919-273">A JavaScript function.</span></span>  
    *   <span data-ttu-id="98919-274">**Otros**.</span><span class="sxs-lookup"><span data-stu-id="98919-274">**Other**.</span></span>  <span data-ttu-id="98919-275">Otro proceso o acción, como navegar hasta una página a través de un vínculo o escribir una dirección URL en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="98919-275">Some other process or action, such as navigating to a page via a link or entering a URL in the address bar.</span></span>  
*   <span data-ttu-id="98919-276">**Tamaño**.</span><span class="sxs-lookup"><span data-stu-id="98919-276">**Size**.</span></span>  <span data-ttu-id="98919-277">El tamaño combinado de los encabezados de respuesta más el cuerpo de la respuesta, tal y como lo proporciona el servidor.</span><span class="sxs-lookup"><span data-stu-id="98919-277">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
*   <span data-ttu-id="98919-278">**Momento**.</span><span class="sxs-lookup"><span data-stu-id="98919-278">**Time**.</span></span>  <span data-ttu-id="98919-279">La duración total, desde el inicio de la solicitud hasta la recepción del byte final en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98919-279">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
*   <span data-ttu-id="98919-280">[**Cascada**](#view-the-timing-of-requests-in-relation-to-one-another).</span><span class="sxs-lookup"><span data-stu-id="98919-280">[**Waterfall**](#view-the-timing-of-requests-in-relation-to-one-another).</span></span>  <span data-ttu-id="98919-281">Un desglose visual de la actividad de cada solicitud.</span><span class="sxs-lookup"><span data-stu-id="98919-281">A visual breakdown of the activity for each request.</span></span>  

#### <span data-ttu-id="98919-282">Agregar o quitar columnas</span><span class="sxs-lookup"><span data-stu-id="98919-282">Add or remove columns</span></span>  

<span data-ttu-id="98919-283">Desplace el puntero en el encabezado de la tabla solicitudes, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione una opción para ocultarlo o mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="98919-283">Hover on the header of the Requests table, open the contextual menu \(right-click\), and select an option to hide or show it.</span></span>  <span data-ttu-id="98919-284">Las opciones mostradas actualmente tienen marcas de verificación junto a cada elemento.</span><span class="sxs-lookup"><span data-stu-id="98919-284">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Agregar una columna a la tabla solicitudes" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="98919-286">Ilustración 16: agregar una columna a la tabla solicitudes</span><span class="sxs-lookup"><span data-stu-id="98919-286">Figure 16:  Adding a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="98919-287">Agregar columnas personalizadas</span><span class="sxs-lookup"><span data-stu-id="98919-287">Add custom columns</span></span>  

<span data-ttu-id="98919-288">Para agregar una columna personalizada a la tabla solicitudes, desplace el puntero sobre el encabezado de la tabla solicitudes, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **encabezados de respuesta**para  >  **administrar columnas de encabezado**.</span><span class="sxs-lookup"><span data-stu-id="98919-288">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and select **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Agregar una columna personalizada a la tabla solicitudes" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="98919-290">Ilustración 17: agregar una columna personalizada a la tabla solicitudes</span><span class="sxs-lookup"><span data-stu-id="98919-290">Figure 17:  Adding a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-291">Ver los intervalos de solicitudes relacionados entre sí</span><span class="sxs-lookup"><span data-stu-id="98919-291">View the timing of requests in relation to one another</span></span>  

<span data-ttu-id="98919-292">Use la cascada para ver los intervalos de solicitudes relacionados entre sí.</span><span class="sxs-lookup"><span data-stu-id="98919-292">Use the Waterfall to view the timing of requests in relation to one another.</span></span>  
<span data-ttu-id="98919-293">De forma predeterminada, la cascada está organizada por la hora de inicio de las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="98919-293">By default, the Waterfall is organized by the start time of the requests.</span></span>  
<span data-ttu-id="98919-294">Por lo tanto, las solicitudes que se encuentren más lejanas a la izquierda iniciadas antes de las que están más lejos a la derecha.</span><span class="sxs-lookup"><span data-stu-id="98919-294">So, requests that are farther to the left started earlier than those that are farther to the right.</span></span>  

<span data-ttu-id="98919-295">Consulte [ordenar por fase de actividad](#sort-by-activity-phase) para ver las diferentes formas de ordenar la cascada.</span><span class="sxs-lookup"><span data-stu-id="98919-295">See [Sort by activity phase](#sort-by-activity-phase) to see the different ways that you may sort the Waterfall.</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="La columna cascada del panel solicitudes" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="98919-297">Ilustración 18: la columna cascada del panel **solicitudes**</span><span class="sxs-lookup"><span data-stu-id="98919-297">Figure 18:  The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To view the frames of a WebSocket connection:  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-select the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames tab" lightbox="../media/network-frames.msft.png":::
   Old Figure 20:  The **Frames** tab  
:::image-end:::  
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

### <span data-ttu-id="98919-298">Ver una vista previa del cuerpo de una respuesta</span><span class="sxs-lookup"><span data-stu-id="98919-298">View a preview of a response body</span></span>  

<span data-ttu-id="98919-299">Para ver una vista previa del cuerpo de una respuesta:</span><span class="sxs-lookup"><span data-stu-id="98919-299">To view a preview of a response body:</span></span>  

1.  <span data-ttu-id="98919-300">Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="98919-300">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="98919-301">Seleccione la pestaña **vista previa** .</span><span class="sxs-lookup"><span data-stu-id="98919-301">Select the **Preview** tab.</span></span>  

<span data-ttu-id="98919-302">Esta pestaña es principalmente útil para visualizar imágenes.</span><span class="sxs-lookup"><span data-stu-id="98919-302">This tab is mostly useful for viewing images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="La ficha vista previa" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="98919-304">Ilustración 19: la ficha **vista previa**</span><span class="sxs-lookup"><span data-stu-id="98919-304">Figure 19:  The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-305">Ver el cuerpo de una respuesta</span><span class="sxs-lookup"><span data-stu-id="98919-305">View a response body</span></span>  

<span data-ttu-id="98919-306">Para ver el cuerpo de la respuesta de una solicitud:</span><span class="sxs-lookup"><span data-stu-id="98919-306">To view the response body to a request:</span></span>  

1.  <span data-ttu-id="98919-307">Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="98919-307">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="98919-308">Seleccione la pestaña **respuesta** .</span><span class="sxs-lookup"><span data-stu-id="98919-308">Select the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="La ficha respuesta" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="98919-310">Ilustración 20: la pestaña **respuesta**</span><span class="sxs-lookup"><span data-stu-id="98919-310">Figure 20:  The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-311">Ver encabezados HTTP</span><span class="sxs-lookup"><span data-stu-id="98919-311">View HTTP headers</span></span>  

<span data-ttu-id="98919-312">Para ver los datos de encabezado HTTP sobre una solicitud:</span><span class="sxs-lookup"><span data-stu-id="98919-312">To view HTTP header data about a request:</span></span>  

1.  <span data-ttu-id="98919-313">Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="98919-313">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="98919-314">Seleccione la pestaña **encabezados** .</span><span class="sxs-lookup"><span data-stu-id="98919-314">Select the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="La pestaña encabezados" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="98919-316">Ilustración 21: la ficha **encabezados**</span><span class="sxs-lookup"><span data-stu-id="98919-316">Figure 21:  The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="98919-317">Ver origen de encabezado HTTP</span><span class="sxs-lookup"><span data-stu-id="98919-317">View HTTP header source</span></span>  

<span data-ttu-id="98919-318">De forma predeterminada, la pestaña encabezados muestra los nombres de encabezado alfabéticamente.</span><span class="sxs-lookup"><span data-stu-id="98919-318">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="98919-319">Para ver los nombres de encabezado HTTP en el orden en que se recibieron:</span><span class="sxs-lookup"><span data-stu-id="98919-319">To view the HTTP header names in the order they were received:</span></span>  

1.  <span data-ttu-id="98919-320">Abre la pestaña **encabezados** para la solicitud que te interese.</span><span class="sxs-lookup"><span data-stu-id="98919-320">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="98919-321">Consulte [Ver encabezados HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="98919-321">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="98919-322">Seleccione **Ver origen**, junto a la sección **solicitar** encabezado o **respuesta de encabezado** .</span><span class="sxs-lookup"><span data-stu-id="98919-322">Select **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="98919-323">Ver parámetros de cadena de consulta</span><span class="sxs-lookup"><span data-stu-id="98919-323">View query string parameters</span></span>  

<span data-ttu-id="98919-324">Para ver los parámetros de cadena de consulta de una dirección URL en un formato legible:</span><span class="sxs-lookup"><span data-stu-id="98919-324">To view the query string parameters of a URL in a human-readable format:</span></span>  

1.  <span data-ttu-id="98919-325">Abre la pestaña **encabezados** para la solicitud que te interese.</span><span class="sxs-lookup"><span data-stu-id="98919-325">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="98919-326">Consulte [Ver encabezados HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="98919-326">See [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="98919-327">Vaya a la sección **parámetros de cadena de consulta** .</span><span class="sxs-lookup"><span data-stu-id="98919-327">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Sección parámetros de cadena de consulta" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="98919-329">Ilustración 22: la sección **parámetros de cadena de consulta**</span><span class="sxs-lookup"><span data-stu-id="98919-329">Figure 22:  The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="98919-330">Ver origen de parámetros de cadena de consulta</span><span class="sxs-lookup"><span data-stu-id="98919-330">View query string parameters source</span></span>  

<span data-ttu-id="98919-331">Para ver el origen de parámetro de cadena de consulta de una solicitud:</span><span class="sxs-lookup"><span data-stu-id="98919-331">To view the query string parameter source of a request:</span></span>  

1.  <span data-ttu-id="98919-332">Vaya a la sección parámetros de cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="98919-332">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="98919-333">Consulte [ver parámetros de cadena de consulta](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="98919-333">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="98919-334">Seleccione **Ver origen**.</span><span class="sxs-lookup"><span data-stu-id="98919-334">Select **view source**.</span></span>  

#### <span data-ttu-id="98919-335">Ver parámetros de cadena de consulta con codificación URL</span><span class="sxs-lookup"><span data-stu-id="98919-335">View URL-encoded query string parameters</span></span>  

<span data-ttu-id="98919-336">Para ver los parámetros de cadena de consulta en un formato legible, pero conservando las codificaciones:</span><span class="sxs-lookup"><span data-stu-id="98919-336">To view query string parameters in a human-readable format, but with encodings preserved:</span></span>  

1.  <span data-ttu-id="98919-337">Vaya a la sección parámetros de cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="98919-337">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="98919-338">Consulte [ver parámetros de cadena de consulta](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="98919-338">See [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="98919-339">Seleccione **Ver dirección URL codificada**.</span><span class="sxs-lookup"><span data-stu-id="98919-339">Select **view URL encoded**.</span></span>  

### <span data-ttu-id="98919-340">Ver cookies</span><span class="sxs-lookup"><span data-stu-id="98919-340">View cookies</span></span>  

<span data-ttu-id="98919-341">Para ver las cookies enviadas en el encabezado HTTP de una solicitud:</span><span class="sxs-lookup"><span data-stu-id="98919-341">To view the cookies sent in the HTTP header of a request:</span></span>  

1.  <span data-ttu-id="98919-342">Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="98919-342">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="98919-343">Seleccione la ficha **cookies** .</span><span class="sxs-lookup"><span data-stu-id="98919-343">Select the **Cookies** tab.</span></span>  

<!--See [Fields][ManageDataCookiesFields] for a description of each of the columns.  -->

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->
<!--TODO: add link when section is available -->

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="La ficha cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="98919-345">Ilustración 23: la ficha cookies</span><span class="sxs-lookup"><span data-stu-id="98919-345">Figure 23:  The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-346">Ver el desglose de intervalos de una solicitud</span><span class="sxs-lookup"><span data-stu-id="98919-346">View the timing breakdown of a request</span></span>  

<span data-ttu-id="98919-347">Para ver el desglose de intervalos de una solicitud:</span><span class="sxs-lookup"><span data-stu-id="98919-347">To view the timing breakdown of a request:</span></span>  

1.  <span data-ttu-id="98919-348">Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="98919-348">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="98919-349">Seleccione la pestaña **intervalos** .</span><span class="sxs-lookup"><span data-stu-id="98919-349">Select the **Timing** tab.</span></span>  

<span data-ttu-id="98919-350">Vea obtener una [vista previa de un desglose de intervalos](#preview-a-timing-breakdown) para obtener acceso a estos datos más rápidamente.</span><span class="sxs-lookup"><span data-stu-id="98919-350">See [Preview a timing breakdown](#preview-a-timing-breakdown) for a faster way to access this data.</span></span>  

<span data-ttu-id="98919-351">Consulte [fases de desglose de intervalos explicadas](#timing-breakdown-phases-explained) para obtener más información sobre cada una de las fases que puede ver en la pestaña intervalos.</span><span class="sxs-lookup"><span data-stu-id="98919-351">See [Timing breakdown phases explained](#timing-breakdown-phases-explained) for more information about each of the phases that you may see in the Timing tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="La ficha intervalos" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="98919-353">Ilustración 24: ficha **intervalos**</span><span class="sxs-lookup"><span data-stu-id="98919-353">Figure 24:  The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="98919-354">Más información sobre cada una de las fases.</span><span class="sxs-lookup"><span data-stu-id="98919-354">More information about each of the phases.</span></span>  

<span data-ttu-id="98919-355">Consulte [Ver desglose de intervalos](#view-the-timing-breakdown-of-a-request) para obtener acceso a esta vista.</span><span class="sxs-lookup"><span data-stu-id="98919-355">See [View timing breakdown](#view-the-timing-breakdown-of-a-request) for another way to access this view.</span></span>  

#### <span data-ttu-id="98919-356">Obtener una vista previa de intervalos</span><span class="sxs-lookup"><span data-stu-id="98919-356">Preview a timing breakdown</span></span>  

<span data-ttu-id="98919-357">Para obtener una vista previa del desglose de intervalos de una solicitud, desplace el puntero sobre la entrada de la solicitud en la columna **cascada** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="98919-357">To view a preview of the timing breakdown of a request, hover over the entry for the request in the **Waterfall** column of the Requests table.</span></span>  

<span data-ttu-id="98919-358">Vea [ver el desglose de intervalos de una solicitud](#view-the-timing-breakdown-of-a-request) para obtener acceso a estos datos que no requieren el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="98919-358">See [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request) for a way to access this data that does not require hovering.</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> obtener una vista previa del desglose de intervalos de una solicitud" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="98919-360">Ilustración 25: vista previa del desglose de intervalos de una solicitud</span><span class="sxs-lookup"><span data-stu-id="98919-360">Figure 25:  Previewing the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="98919-361">Explicación de fases de desglose de intervalos</span><span class="sxs-lookup"><span data-stu-id="98919-361">Timing breakdown phases explained</span></span>  

<span data-ttu-id="98919-362">Más información sobre cada una de las fases que puede ver en la pestaña **intervalos** .</span><span class="sxs-lookup"><span data-stu-id="98919-362">More information about each of the phases you may see in the **Timing** tab.</span></span>  

*   <span data-ttu-id="98919-363">**Poner en cola**.</span><span class="sxs-lookup"><span data-stu-id="98919-363">**Queueing**.</span></span>  <span data-ttu-id="98919-364">El explorador pone en cola las solicitudes cuando:</span><span class="sxs-lookup"><span data-stu-id="98919-364">The browser queues requests when:</span></span>  
    *   <span data-ttu-id="98919-365">Hay solicitudes de prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="98919-365">There are higher priority requests.</span></span>  
    *   <span data-ttu-id="98919-366">Ya hay seis conexiones TCP abiertas para este origen, que es el límite.</span><span class="sxs-lookup"><span data-stu-id="98919-366">There are already six TCP connections open for this origin, which is the limit.</span></span>  <span data-ttu-id="98919-367">Solo se aplica a HTTP/1.0 y HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="98919-367">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
    *   <span data-ttu-id="98919-368">El explorador está asignando un poco de espacio en la caché de disco.</span><span class="sxs-lookup"><span data-stu-id="98919-368">The browser is briefly allocating space in the disk cache.</span></span>  
*   <span data-ttu-id="98919-369">**Detenido**.</span><span class="sxs-lookup"><span data-stu-id="98919-369">**Stalled**.</span></span>  <span data-ttu-id="98919-370">La solicitud podría estar detenida por cualquiera de las razones descritas en **puesta en cola**.</span><span class="sxs-lookup"><span data-stu-id="98919-370">The request could be stalled for any of the reasons described in **Queueing**.</span></span>  
*   <span data-ttu-id="98919-371">**Búsqueda DNS**.</span><span class="sxs-lookup"><span data-stu-id="98919-371">**DNS Lookup**.</span></span>  <span data-ttu-id="98919-372">El explorador está resolviendo la dirección IP de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="98919-372">The browser is resolving the IP address for the request.</span></span>  
*   <span data-ttu-id="98919-373">**Conexión inicial**.</span><span class="sxs-lookup"><span data-stu-id="98919-373">**Initial connection**.</span></span>  <span data-ttu-id="98919-374">El explorador está estableciendo una conexión que incluye protocolos de enlace TCP, reintentos de TCP y negociando un SSL.</span><span class="sxs-lookup"><span data-stu-id="98919-374">The browser is establishing a connection including TCP handshakes, TCP retries, and negotiating an SSL.</span></span>
*   <span data-ttu-id="98919-375">**Negociación de proxy**.</span><span class="sxs-lookup"><span data-stu-id="98919-375">**Proxy negotiation**.</span></span>  <span data-ttu-id="98919-376">El explorador está negociando la solicitud con un [servidor proxy][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="98919-376">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
*   <span data-ttu-id="98919-377">**Solicitud enviada**.</span><span class="sxs-lookup"><span data-stu-id="98919-377">**Request sent**.</span></span>  <span data-ttu-id="98919-378">Se está enviando la solicitud.</span><span class="sxs-lookup"><span data-stu-id="98919-378">The request is being sent.</span></span>  
*   <span data-ttu-id="98919-379">**Preparación de ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="98919-379">**ServiceWorker Preparation**.</span></span>  <span data-ttu-id="98919-380">El explorador está iniciando el trabajo del servicio.</span><span class="sxs-lookup"><span data-stu-id="98919-380">The browser is starting up the service worker.</span></span>  
*   <span data-ttu-id="98919-381">**Solicitud para ServiceWorker**.</span><span class="sxs-lookup"><span data-stu-id="98919-381">**Request to ServiceWorker**.</span></span>  <span data-ttu-id="98919-382">La solicitud se está enviando al trabajador del servicio.</span><span class="sxs-lookup"><span data-stu-id="98919-382">The request is being sent to the service worker.</span></span>  
*   <span data-ttu-id="98919-383">**Esperando \ (TTFB \)**.</span><span class="sxs-lookup"><span data-stu-id="98919-383">**Waiting \(TTFB\)**.</span></span>  <span data-ttu-id="98919-384">El explorador está esperando el primer byte de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="98919-384">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="98919-385">TTFB es el primer byte.</span><span class="sxs-lookup"><span data-stu-id="98919-385">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="98919-386">Este intervalo incluye 1 recorrido de ida y vuelta de la latencia y el tiempo que el servidor necesitó para preparar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98919-386">This timing includes 1 round trip of latency and the time the server took to prepare the response.</span></span>  
*   <span data-ttu-id="98919-387">**Descarga de contenido**.</span><span class="sxs-lookup"><span data-stu-id="98919-387">**Content Download**.</span></span>  <span data-ttu-id="98919-388">El explorador está recibiendo la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98919-388">The browser is receiving the response.</span></span>  
*   <span data-ttu-id="98919-389">**Recibiendo Push**.</span><span class="sxs-lookup"><span data-stu-id="98919-389">**Receiving Push**.</span></span>  <span data-ttu-id="98919-390">El explorador está recibiendo datos de esta respuesta a través de la inserción de servidor HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="98919-390">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
*   <span data-ttu-id="98919-391">**Leyendo inserción**.</span><span class="sxs-lookup"><span data-stu-id="98919-391">**Reading Push**.</span></span>  <span data-ttu-id="98919-392">El explorador está leyendo los datos locales recibidos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="98919-392">The browser is reading the local data previously received.</span></span>  

### <span data-ttu-id="98919-393">Ver iniciadores y dependencias</span><span class="sxs-lookup"><span data-stu-id="98919-393">View initiators and dependencies</span></span>  

<span data-ttu-id="98919-394">Para ver los iniciadores y las dependencias de una solicitud, mantenga presionado `Shift` el mouse sobre la solicitud en la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="98919-394">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="98919-395">Colores de DevTools: los iniciadores se muestran en verde y las dependencias en rojo.</span><span class="sxs-lookup"><span data-stu-id="98919-395">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Visualización de los iniciadores y las dependencias de una solicitud" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="98919-397">Ilustración 26: visualización de los iniciadores y las dependencias de una solicitud</span><span class="sxs-lookup"><span data-stu-id="98919-397">Figure 26:  Viewing the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="98919-398">Cuando la tabla solicitudes está ordenada cronológicamente, la primera solicitud verde por encima de la que está pasando es el iniciador de la dependencia.</span><span class="sxs-lookup"><span data-stu-id="98919-398">When the Requests table is ordered chronologically, the first green request above the one you are hovering is the initiator of the dependency.</span></span>  <span data-ttu-id="98919-399">Si aparece otra solicitud de color verde encima de esa, esa solicitud superior es el iniciador del iniciador.</span><span class="sxs-lookup"><span data-stu-id="98919-399">If another green request appears above that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="98919-400">Etcétera.</span><span class="sxs-lookup"><span data-stu-id="98919-400">And so on.</span></span>  

### <span data-ttu-id="98919-401">Ver eventos de carga</span><span class="sxs-lookup"><span data-stu-id="98919-401">View load events</span></span>  

<span data-ttu-id="98919-402">DevTools muestra la temporización de los `DOMContentLoaded` `load` eventos y en varios lugares del panel red.</span><span class="sxs-lookup"><span data-stu-id="98919-402">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="98919-403">El `DOMContentLoaded` evento está coloreado en azul y el `load` evento es rojo.</span><span class="sxs-lookup"><span data-stu-id="98919-403">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Las ubicaciones de la DOMContentLoaded y cargar eventos en el panel red" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="98919-405">Ilustración 27: las ubicaciones de los `DOMContentLoaded` `load` eventos y en el panel red</span><span class="sxs-lookup"><span data-stu-id="98919-405">Figure 27:  The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-406">Ver el número total de solicitudes</span><span class="sxs-lookup"><span data-stu-id="98919-406">View the total number of requests</span></span>  

<span data-ttu-id="98919-407">El número total de solicitudes se muestra en el panel Resumen, en la parte inferior del panel red.</span><span class="sxs-lookup"><span data-stu-id="98919-407">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="98919-408">Este número solo realiza un seguimiento de las solicitudes que se han registrado desde que se abrió DevTools.</span><span class="sxs-lookup"><span data-stu-id="98919-408">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="98919-409">Si se han producido otras solicitudes antes de que se abriera DevTools, esas solicitudes no se cuentan.</span><span class="sxs-lookup"><span data-stu-id="98919-409">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="El número total de solicitudes desde que se abrió DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="98919-411">Ilustración 28: el número total de solicitudes desde que se abrió DevTools</span><span class="sxs-lookup"><span data-stu-id="98919-411">Figure 28:  The total number of requests since DevTools was opened</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-412">Ver el tamaño total de la descarga</span><span class="sxs-lookup"><span data-stu-id="98919-412">View the total download size</span></span>  

<span data-ttu-id="98919-413">El tamaño total de las solicitudes de descarga se muestra en el panel Resumen, en la parte inferior del panel red.</span><span class="sxs-lookup"><span data-stu-id="98919-413">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="98919-414">Este número solo realiza un seguimiento de las solicitudes que se han registrado desde que se abrió DevTools.</span><span class="sxs-lookup"><span data-stu-id="98919-414">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="98919-415">Si se han producido otras solicitudes antes de que se abriera DevTools, no se cuentan las solicitudes anteriores.</span><span class="sxs-lookup"><span data-stu-id="98919-415">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="El tamaño total de las solicitudes de descarga" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="98919-417">Ilustración 29: el tamaño total de las solicitudes de descarga</span><span class="sxs-lookup"><span data-stu-id="98919-417">Figure 29:  The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="98919-418">Consulte [ver el tamaño descomprimido de un recurso](#view-the-uncompressed-size-of-a-resource) para ver cómo se encuentran los recursos grandes después de que el explorador descomprime cada elemento.</span><span class="sxs-lookup"><span data-stu-id="98919-418">See [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource) to see how large resources are after the browser uncompresses each item.</span></span>  

### <span data-ttu-id="98919-419">Ver el seguimiento de la pila que causó una solicitud</span><span class="sxs-lookup"><span data-stu-id="98919-419">View the stack trace that caused a request</span></span>  

<span data-ttu-id="98919-420">Después de que una instrucción de JavaScript solicite un recurso, mueva el puntero sobre la columna de **iniciador** para ver el seguimiento de la pila que se dirige a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="98919-420">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="El seguimiento de la pila que lleva a una solicitud de recursos" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="98919-422">Ilustración 30: el seguimiento de la pila que lleva a una solicitud de recursos</span><span class="sxs-lookup"><span data-stu-id="98919-422">Figure 30:  The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-423">Ver el tamaño descomprimido de un recurso</span><span class="sxs-lookup"><span data-stu-id="98919-423">View the uncompressed size of a resource</span></span>  

<span data-ttu-id="98919-424">Seleccione la casilla **usar filas de solicitudes grandes** y, a continuación, mire el valor inferior de la columna **tamaño** .</span><span class="sxs-lookup"><span data-stu-id="98919-424">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Ejemplo de recursos sin comprimir" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="98919-426">Ilustración 31: ejemplo de recursos no comprimidos \ (el tamaño comprimido del `jquery-3.3.1.min.js` archivo que se envió a través de la red fue `29.9 KB` , mientras que el tamaño descomprimido fue `84.9 KB` \)</span><span class="sxs-lookup"><span data-stu-id="98919-426">Figure 31:  An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="98919-427">Exportar datos de solicitudes</span><span class="sxs-lookup"><span data-stu-id="98919-427">Export requests data</span></span>  

### <span data-ttu-id="98919-428">Guardar todas las solicitudes de red en un archivo HAR</span><span class="sxs-lookup"><span data-stu-id="98919-428">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="98919-429">Para guardar todas las solicitudes de red en un archivo HAR, siga los pasos que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="98919-429">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="98919-430">Mantenga el mouse sobre cualquier solicitud de la tabla solicitudes y abra el menú contextual \ (haga clic con el botón derecho \).</span><span class="sxs-lookup"><span data-stu-id="98919-430">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="98919-431">Seleccione **Guardar como Har with Content**.</span><span class="sxs-lookup"><span data-stu-id="98919-431">Select **Save as HAR with Content**.</span></span>  <span data-ttu-id="98919-432">DevTools guarda todas las solicitudes que se han producido desde que abrió DevTools en el archivo HAR.</span><span class="sxs-lookup"><span data-stu-id="98919-432">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="98919-433">No hay ninguna manera de filtrar las solicitudes o de guardar una sola.</span><span class="sxs-lookup"><span data-stu-id="98919-433">There is no way to filter requests, or to save just a single request.</span></span>  

<span data-ttu-id="98919-434">Una vez que haya guardado un archivo HAR, podrá volver a importarlo en DevTools para analizarlo.</span><span class="sxs-lookup"><span data-stu-id="98919-434">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="98919-435">Simplemente arrastre y coloque el archivo HAR en la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="98919-435">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--See also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Seleccionar Guardar como HAR with Content" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="98919-437">Ilustración 32: seleccionar la opción **Guardar como Har with Content**</span><span class="sxs-lookup"><span data-stu-id="98919-437">Figure 32:  Selecting **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-438">Copiar una o más solicitudes en el portapapeles</span><span class="sxs-lookup"><span data-stu-id="98919-438">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="98919-439">En la columna **nombre** de la tabla solicitudes, desplace el puntero sobre una solicitud y abra el menú contextual \ (haga clic con el botón derecho \), mueva el puntero sobre **copiar**y seleccione una de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="98919-439">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover over **Copy**, and select one of the following options.</span></span>  

*   <span data-ttu-id="98919-440">**Copiar la dirección del vínculo**.</span><span class="sxs-lookup"><span data-stu-id="98919-440">**Copy Link Address**.</span></span>  <span data-ttu-id="98919-441">Copie la dirección URL de la solicitud en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="98919-441">Copy the URL of the request to the clipboard.</span></span>  
*   <span data-ttu-id="98919-442">**Copiar respuesta**.</span><span class="sxs-lookup"><span data-stu-id="98919-442">**Copy Response**.</span></span>  <span data-ttu-id="98919-443">Copie el cuerpo de la respuesta en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="98919-443">Copy the response body to the clipboard.</span></span>  
*   <span data-ttu-id="98919-444">**Copiar como fetch**.</span><span class="sxs-lookup"><span data-stu-id="98919-444">**Copy as Fetch**.</span></span>  
*   <span data-ttu-id="98919-445">**Copiar como rizo**.</span><span class="sxs-lookup"><span data-stu-id="98919-445">**Copy as cURL**.</span></span>  <span data-ttu-id="98919-446">Copie la solicitud como un comando de rizo.</span><span class="sxs-lookup"><span data-stu-id="98919-446">Copy the request as a cURL command.</span></span>  
*   <span data-ttu-id="98919-447">**Copiar todo como fetch**.</span><span class="sxs-lookup"><span data-stu-id="98919-447">**Copy All as Fetch**.</span></span>  
*   <span data-ttu-id="98919-448">**Copiar todos como rizo**.</span><span class="sxs-lookup"><span data-stu-id="98919-448">**Copy All as cURL**.</span></span>  <span data-ttu-id="98919-449">Copiar todas las solicitudes como una cadena de comandos de rizo.</span><span class="sxs-lookup"><span data-stu-id="98919-449">Copy all requests as a chain of cURL commands.</span></span>  
*   <span data-ttu-id="98919-450">**Copiar todo como Har**.</span><span class="sxs-lookup"><span data-stu-id="98919-450">**Copy All as HAR**.</span></span>  <span data-ttu-id="98919-451">Copie todas las solicitudes como datos de HAR.</span><span class="sxs-lookup"><span data-stu-id="98919-451">Copy all requests as HAR data.</span></span>  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Selección de copiar respuesta" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="98919-453">Ilustración 33: selección de la **respuesta de copia**</span><span class="sxs-lookup"><span data-stu-id="98919-453">Figure 33:  Selecting **Copy Response**</span></span>  
:::image-end:::  

## <span data-ttu-id="98919-454">Cambiar el diseño del panel red</span><span class="sxs-lookup"><span data-stu-id="98919-454">Change the layout of the Network panel</span></span>  

<span data-ttu-id="98919-455">Puede expandir o contraer secciones de la interfaz de usuario del panel red para destacar información importante.</span><span class="sxs-lookup"><span data-stu-id="98919-455">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="98919-456">Ocultar el panel de filtros</span><span class="sxs-lookup"><span data-stu-id="98919-456">Hide the Filters pane</span></span>  

<span data-ttu-id="98919-457">De forma predeterminada, DevTools muestra el **Panel filtros**.</span><span class="sxs-lookup"><span data-stu-id="98919-457">By default, DevTools shows the **Filters pane**.</span></span>  
<span data-ttu-id="98919-458">Seleccione filtro de **filtro** ![ ][ImageFilterIcon] para ocultarlo.</span><span class="sxs-lookup"><span data-stu-id="98919-458">Select **Filter** ![Filter][ImageFilterIcon] to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="El botón ocultar filtros" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="98919-460">Ilustración 34: botón ocultar filtros</span><span class="sxs-lookup"><span data-stu-id="98919-460">Figure 34:  The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-461">Usar filas de solicitudes grandes</span><span class="sxs-lookup"><span data-stu-id="98919-461">Use large request rows</span></span>  

<span data-ttu-id="98919-462">Use filas grandes cuando desee más espacios en blanco en la tabla solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="98919-462">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="98919-463">Algunas columnas también proporcionan un poco más de información cuando se usan filas grandes.</span><span class="sxs-lookup"><span data-stu-id="98919-463">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="98919-464">Por ejemplo, el valor inferior de la columna **tamaño** es el tamaño descomprimido de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="98919-464">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Ejemplo de filas de solicitudes grandes en el panel solicitudes" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="98919-466">Ilustración 35: un ejemplo de filas de solicitudes grandes en el panel **solicitudes**</span><span class="sxs-lookup"><span data-stu-id="98919-466">Figure 35:  An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="98919-467">Seleccione la casilla **usar filas de solicitudes grandes** para habilitar las filas grandes.</span><span class="sxs-lookup"><span data-stu-id="98919-467">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Casilla de verificación usar filas de solicitudes grandes" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="98919-469">Ilustración 36: casilla de verificación **usar filas de solicitudes grandes**</span><span class="sxs-lookup"><span data-stu-id="98919-469">Figure 36:  The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="98919-470">Ocultar el panel de información general</span><span class="sxs-lookup"><span data-stu-id="98919-470">Hide the Overview pane</span></span>  

<span data-ttu-id="98919-471">De forma predeterminada, DevTools muestra el **Panel de información general**.</span><span class="sxs-lookup"><span data-stu-id="98919-471">By default, DevTools shows the **Overview pane**.</span></span>  <span data-ttu-id="98919-472">Anule la selección de la casilla **Mostrar información general** para ocultarla.</span><span class="sxs-lookup"><span data-stu-id="98919-472">Deselect the **Show Overview** checkbox to hide it.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="La casilla Mostrar información general" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="98919-474">Ilustración 37: la casilla **Mostrar información general**</span><span class="sxs-lookup"><span data-stu-id="98919-474">Figure 37:  The **Show Overview** checkbox</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: /microsoft-edge/devtools-guide-chromium/network/progressive-web-apps "Depurar aplicaciones web progresivas"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "Direcciones URL de datos | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Servidor proxy-Wikipedia"  

> [!NOTE]
> <span data-ttu-id="98919-478">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="98919-478">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="98919-479">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/network/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="98919-479">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="98919-481">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="98919-481">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

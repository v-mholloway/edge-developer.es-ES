---
description: Una referencia completa de las características del panel de red de Microsoft Edge DevTools.
title: Referencia de análisis de red
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 758623482ab2179987c6467f8e30c72d8893d710
ms.sourcegitcommit: addfd27bb765c92880a59f259dc702f6e4e1bf28
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/30/2020
ms.locfileid: "11092317"
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

# <span data-ttu-id="13f12-104">Referencia de análisis de red</span><span class="sxs-lookup"><span data-stu-id="13f12-104">Network Analysis reference</span></span>  

<span data-ttu-id="13f12-105">Descubra nuevas formas de analizar cómo se carga su página en esta referencia completa de las características de análisis de red de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="13f12-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

<!--
> [!NOTE]
> This reference is based on Microsoft Edge 58.  If you use another version of Microsoft Edge, the UI, and features of DevTools may be different.  To verify which version of Microsoft Edge you are running, navigate to `edge://help`.  
-->

## <span data-ttu-id="13f12-106">Registrar solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="13f12-106">Record network requests</span></span>  

<span data-ttu-id="13f12-107">De forma predeterminada, DevTools graba todas las solicitudes de red en el panel red, siempre y cuando DevTools esté abierto.</span><span class="sxs-lookup"><span data-stu-id="13f12-107">By default, DevTools record all network requests in the Network panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Panel red" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="13f12-109">Panel **red**</span><span class="sxs-lookup"><span data-stu-id="13f12-109">The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-110">Detener la grabación de solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="13f12-110">Stop recording network requests</span></span>  

<span data-ttu-id="13f12-111">Siga los pasos que se indican a continuación para detener la grabación de solicitudes.</span><span class="sxs-lookup"><span data-stu-id="13f12-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="13f12-112">Seleccione **Detener grabación de registro de red** \ ( ![ Detener grabación ][ImageRecordOnIcon] de registro de red \) en el panel **red** .</span><span class="sxs-lookup"><span data-stu-id="13f12-112">Select **Stop recording network log** \(![Stop recording network log][ImageRecordOnIcon]\) on the **Network** panel.</span></span>  <span data-ttu-id="13f12-113">Se vuelve gris para indicar que DevTools ya no graba solicitudes.</span><span class="sxs-lookup"><span data-stu-id="13f12-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="13f12-114">Pulse `Control` + `E` \ (Windows \) o `Command` + `E` \ (MacOS \) mientras el panel **red** está en el foco.</span><span class="sxs-lookup"><span data-stu-id="13f12-114">Press `Control`+`E` \(Windows\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="13f12-115">Borrar solicitudes</span><span class="sxs-lookup"><span data-stu-id="13f12-115">Clear requests</span></span>  

<span data-ttu-id="13f12-116">Seleccione **Borrar** \ ( ![ Borrar ][ImageClearIcon] \) en el panel red para borrar todas las solicitudes de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="13f12-116">Select **Clear** \(![Clear][ImageClearIcon]\) on the Network panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Panel red" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="13f12-118">Botón **Borrar**</span><span class="sxs-lookup"><span data-stu-id="13f12-118">The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-119">Guardar solicitudes en la carga de páginas</span><span class="sxs-lookup"><span data-stu-id="13f12-119">Save requests across page loads</span></span>  

<span data-ttu-id="13f12-120">Para guardar las solicitudes en la carga de la página, active la casilla **conservar registro** en el panel red.</span><span class="sxs-lookup"><span data-stu-id="13f12-120">To save requests across page loads, check the **Preserve log** checkbox on the Network panel.</span></span>  <span data-ttu-id="13f12-121">DevTools guarda todas las solicitudes hasta que Deshabilites **conservar registro**.</span><span class="sxs-lookup"><span data-stu-id="13f12-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Panel red" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="13f12-123">Casilla de verificación **conservar registro**</span><span class="sxs-lookup"><span data-stu-id="13f12-123">The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-124">Capturar capturas de pantallas durante la carga de la página</span><span class="sxs-lookup"><span data-stu-id="13f12-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="13f12-125">Capture las capturas de pantallas para analizar qué se muestra para los usuarios mientras esperan la página que desea cargar.</span><span class="sxs-lookup"><span data-stu-id="13f12-125">Capture screenshots to analyze what displays for users while waiting for your page to load.</span></span>  

<span data-ttu-id="13f12-126">Para habilitar capturas de pantalla, seleccione **configuración de red** y marque la casilla **capturar capturas** de pantalla en el panel **red** .</span><span class="sxs-lookup"><span data-stu-id="13f12-126">To enable screenshots, select **Network settings** and select **Capture screenshots** checkbox on the **Network** panel.</span></span>  

<span data-ttu-id="13f12-127">Actualice la página mientras el panel **red** está enfocado para capturar capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="13f12-127">Refresh the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="13f12-128">Después de capturar una captura de pantalla, puede interactuar con ella de las siguientes maneras.</span><span class="sxs-lookup"><span data-stu-id="13f12-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="13f12-129">Desplace el puntero sobre una captura de pantalla para ver el punto en el que se capturó la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="13f12-129">Hover over a screenshot to view the point at which that screenshot was captured.</span></span>  <span data-ttu-id="13f12-130">Se muestra una línea amarilla en el panel de **información general** .</span><span class="sxs-lookup"><span data-stu-id="13f12-130">A yellow line is displayed on the **Overview** pane.</span></span>  
*   <span data-ttu-id="13f12-131">Seleccione la miniatura de una pantalla para filtrar las solicitudes que se produjeron después de que se capturó la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="13f12-131">Select the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="13f12-132">Haga doble clic en una miniatura para acercarla.</span><span class="sxs-lookup"><span data-stu-id="13f12-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Panel red" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="13f12-134">Colocar el puntero sobre una captura de pantalla</span><span class="sxs-lookup"><span data-stu-id="13f12-134">Hovering over a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and select **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Panel red" lightbox="../media/network-replay-xhr.msft.png":::
   Selecting Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="13f12-135">Cambiar el comportamiento de carga</span><span class="sxs-lookup"><span data-stu-id="13f12-135">Change loading behavior</span></span>  

### <span data-ttu-id="13f12-136">Emular a un primer visitante mediante la deshabilitación de la memoria caché del explorador</span><span class="sxs-lookup"><span data-stu-id="13f12-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="13f12-137">Para emular el funcionamiento de su sitio por primera vez, active la casilla **deshabilitar la caché** .</span><span class="sxs-lookup"><span data-stu-id="13f12-137">To emulate how a first-time user experiences your site, check the **Disable cache** checkbox.</span></span>  <span data-ttu-id="13f12-138">DevTools deshabilita la caché del explorador.</span><span class="sxs-lookup"><span data-stu-id="13f12-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="13f12-139">Esta característica emula con más precisión la experiencia de un usuario por primera vez, ya que las solicitudes se proporcionan desde la memoria caché del explorador al repetir visitas.</span><span class="sxs-lookup"><span data-stu-id="13f12-139">This feature more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Panel red" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="13f12-141">Casilla **deshabilitar caché**</span><span class="sxs-lookup"><span data-stu-id="13f12-141">The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="13f12-142">Deshabilitar la memoria caché del explorador en el cajón de condiciones de red</span><span class="sxs-lookup"><span data-stu-id="13f12-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="13f12-143">Si desea deshabilitar la caché mientras trabaja en otros paneles de DevTools, use el cajón de condiciones de redes.</span><span class="sxs-lookup"><span data-stu-id="13f12-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="13f12-144">Abra el cajón de **condiciones de redes** .</span><span class="sxs-lookup"><span data-stu-id="13f12-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="13f12-145">Active o desactive la casilla **deshabilitar caché** .</span><span class="sxs-lookup"><span data-stu-id="13f12-145">Check or uncheck the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="13f12-146">Borrar manualmente la memoria caché del explorador</span><span class="sxs-lookup"><span data-stu-id="13f12-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="13f12-147">Para borrar manualmente la memoria caché del explorador en cualquier momento, abra el menú contextual \ (haga clic con el botón secundario del mouse \) en cualquier lugar de la tabla solicitudes y seleccione **Borrar caché del explorador**.</span><span class="sxs-lookup"><span data-stu-id="13f12-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Panel red" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="13f12-149">Selección de **Borrar caché del explorador**</span><span class="sxs-lookup"><span data-stu-id="13f12-149">Selecting **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-150">Emular sin conexión</span><span class="sxs-lookup"><span data-stu-id="13f12-150">Emulate offline</span></span>  

<span data-ttu-id="13f12-151">Una nueva clase de aplicaciones Web, denominada [aplicaciones web progresivas][DevtoolsProgressiveWebApps], funciona sin conexión con la ayuda de los **trabajadores de servicio**.</span><span class="sxs-lookup"><span data-stu-id="13f12-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="13f12-152">Es posible que le resulte útil simular rápidamente un dispositivo que no tiene conexión de datos cuando está creando este tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="13f12-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="13f12-153">Seleccione el menú desplegable **en línea** , búsqueda en **preestablecidos**y seleccione **sin conexión** para simular una experiencia de red sin conexión.</span><span class="sxs-lookup"><span data-stu-id="13f12-153">Select the **Online** dropdown menu, search under **Presets**, and select **Offline** to simulate an offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Panel red" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="13f12-155">Menú desplegable **desconectado**</span><span class="sxs-lookup"><span data-stu-id="13f12-155">The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-156">Emular conexiones de red lentas</span><span class="sxs-lookup"><span data-stu-id="13f12-156">Emulate slow network connections</span></span>  

<span data-ttu-id="13f12-157">Emular 3G lento, 3G rápido y otras velocidades de conexión en el menú desplegable **en línea** .</span><span class="sxs-lookup"><span data-stu-id="13f12-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Panel red" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="13f12-159">El menú desplegable **limitación de peticiones**</span><span class="sxs-lookup"><span data-stu-id="13f12-159">The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="13f12-160">Puedes elegir entre diferentes ajustes preestablecidos, como 3G lento o 3G rápido.</span><span class="sxs-lookup"><span data-stu-id="13f12-160">You may select from different presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="13f12-161">También puede agregar sus propios ajustes preestablecidos personalizados abriendo el menú de limitación y seleccionando **Custom**  >  **añadir**personalizados.</span><span class="sxs-lookup"><span data-stu-id="13f12-161">You may also add your own custom presets by opening the Throttling menu and selecting **Custom** > **Add**.</span></span>  

<span data-ttu-id="13f12-162">DevTools muestra un icono de advertencia junto a la pestaña **red** para recordarle que la limitación está habilitada.</span><span class="sxs-lookup"><span data-stu-id="13f12-162">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="13f12-163">Emular conexiones de red lentas del cajón de condiciones de red</span><span class="sxs-lookup"><span data-stu-id="13f12-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="13f12-164">Si desea limitar la conexión de red mientras trabaja en otros paneles de DevTools, use el cajón de condiciones de redes.</span><span class="sxs-lookup"><span data-stu-id="13f12-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="13f12-165">Abra el cajón de **condiciones de redes** .</span><span class="sxs-lookup"><span data-stu-id="13f12-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="13f12-166">Seleccione la velocidad de conexión en el menú **limitación** .</span><span class="sxs-lookup"><span data-stu-id="13f12-166">Select your connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="13f12-167">Borrar manualmente las cookies del explorador</span><span class="sxs-lookup"><span data-stu-id="13f12-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="13f12-168">Para borrar manualmente las cookies del explorador en cualquier momento, abra el menú contextual \ (haga clic con el botón secundario del mouse \) en cualquier lugar de la tabla solicitudes y seleccione **Borrar cookies del explorador**.</span><span class="sxs-lookup"><span data-stu-id="13f12-168">To manually clear browser cookies at any time, open the contextual menu \(right-click\) anywhere in the Requests table and select **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Panel red" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="13f12-170">Selección de las **cookies de borrar explorador**</span><span class="sxs-lookup"><span data-stu-id="13f12-170">Selecting **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-171">Invalidar el agente de usuario</span><span class="sxs-lookup"><span data-stu-id="13f12-171">Override the user agent</span></span>  

<span data-ttu-id="13f12-172">Para anular manualmente el agente de usuario, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="13f12-172">To manually override the user agent, use the following steps.</span></span>  

1.  <span data-ttu-id="13f12-173">Abra el cajón de **condiciones de redes** .</span><span class="sxs-lookup"><span data-stu-id="13f12-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="13f12-174">Desactive **seleccionar automáticamente**.</span><span class="sxs-lookup"><span data-stu-id="13f12-174">Uncheck **Select automatically**.</span></span>  
1.  <span data-ttu-id="13f12-175">Elija una opción de agente de usuario en el menú o escriba una personalizada en el cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="13f12-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="13f12-176">Filtrar solicitudes</span><span class="sxs-lookup"><span data-stu-id="13f12-176">Filter requests</span></span>  

### <span data-ttu-id="13f12-177">Filtrar las solicitudes por propiedades</span><span class="sxs-lookup"><span data-stu-id="13f12-177">Filter requests by properties</span></span>  

<span data-ttu-id="13f12-178">Use el cuadro de texto **filtrar** para filtrar las solicitudes por propiedades, como el dominio o el tamaño de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="13f12-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="13f12-179">Si no se muestra el cuadro de texto, es probable que el panel **filtros** esté oculto.</span><span class="sxs-lookup"><span data-stu-id="13f12-179">If the text box is not displayed, the **Filters** pane is probably hidden.</span></span>  
<span data-ttu-id="13f12-180">Para obtener más información, vaya a [ocultar el panel de filtros](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="13f12-180">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Panel red" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="13f12-182">El cuadro de texto **filtro**</span><span class="sxs-lookup"><span data-stu-id="13f12-182">The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="13f12-183">Puede usar varias propiedades simultáneamente al separar cada propiedad con un espacio.</span><span class="sxs-lookup"><span data-stu-id="13f12-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="13f12-184">Por ejemplo, `mime-type:image/png larger-than:1K` se muestran todos los PNGs que tengan más de 1 kilobyte.</span><span class="sxs-lookup"><span data-stu-id="13f12-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than 1 kilobyte.</span></span>  <span data-ttu-id="13f12-185">Los filtros de varias propiedades son equivalentes a `AND` las operaciones.</span><span class="sxs-lookup"><span data-stu-id="13f12-185">The multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="13f12-186">Actualmente no se admiten las operaciones.</span><span class="sxs-lookup"><span data-stu-id="13f12-186">operations are currently not supported.</span></span>  

<span data-ttu-id="13f12-187">La lista completa de propiedades compatibles.</span><span class="sxs-lookup"><span data-stu-id="13f12-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="13f12-188">Propiedad</span><span class="sxs-lookup"><span data-stu-id="13f12-188">Property</span></span> | <span data-ttu-id="13f12-189">Detalles</span><span class="sxs-lookup"><span data-stu-id="13f12-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="13f12-190">Mostrar solo los recursos del dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="13f12-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="13f12-191">Puede usar un carácter comodín \ ( `*` \) para incluir varios dominios.</span><span class="sxs-lookup"><span data-stu-id="13f12-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="13f12-192">Por ejemplo, `*.com` muestra los recursos de todos los nombres de dominio que terminan en `.com` .</span><span class="sxs-lookup"><span data-stu-id="13f12-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="13f12-193">DevTools rellenar el menú desplegable de autocompletar con todos los dominios que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="13f12-193">DevTools populate the autocomplete dropdown menu with all of the domains that are found.</span></span> |  
| `has-response-header` | <span data-ttu-id="13f12-194">Muestra los recursos que contienen el encabezado de respuesta HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="13f12-194">Displays the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="13f12-195">DevTools rellenar la lista desplegable de autocompletar con todos los encabezados de respuesta que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="13f12-195">DevTools populate the autocomplete dropdown with all of the response headers that are found.</span></span> |  
| `is` | <span data-ttu-id="13f12-196">Usar `is:running` para buscar `WebSocket` recursos.</span><span class="sxs-lookup"><span data-stu-id="13f12-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="13f12-197">Muestra los recursos que son mayores que el tamaño especificado, en bytes.</span><span class="sxs-lookup"><span data-stu-id="13f12-197">Displays resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="13f12-198">Establecer un valor de `1000` es equivalente a establecer un valor de `1k` .</span><span class="sxs-lookup"><span data-stu-id="13f12-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="13f12-199">Muestra los recursos que se recuperaron en un tipo de método HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="13f12-199">Displays resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="13f12-200">DevTools rellenar la lista desplegable con todos los métodos HTTP que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="13f12-200">DevTools populate the dropdown with all of the HTTP methods  that are found.</span></span> |  
| `mime-type` | <span data-ttu-id="13f12-201">Muestra los recursos de un tipo MIME especificado.</span><span class="sxs-lookup"><span data-stu-id="13f12-201">Displays resources of a specified MIME type.</span></span>  <span data-ttu-id="13f12-202">DevTools rellenar la lista desplegable con todos los tipos MIME que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="13f12-202">DevTools populate the dropdown with all MIME types  that are found.</span></span> |  
| `mixed-content` | <span data-ttu-id="13f12-203">Mostrar todos los recursos de contenido mixto \ ( `mixed-content:all` \) o solo los que se muestran actualmente \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="13f12-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="13f12-204">Muestra los recursos recuperados en HTTP \ ( `scheme:http` \) no protegidos o en https \ ( `scheme:https` \).</span><span class="sxs-lookup"><span data-stu-id="13f12-204">Displays resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="13f12-205">Muestra los recursos que tienen un `Set-Cookie` encabezado con un `Domain` atributo que coincide con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="13f12-205">Displays resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="13f12-206">DevTools rellenar autocompletar con todos los dominios de cookies que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="13f12-206">DevTools populate the autocomplete with all of the cookie domains that are found.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="13f12-207">Muestra los recursos que tienen un `Set-Cookie` encabezado con un nombre que coincide con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="13f12-207">Displays resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="13f12-208">DevTools rellenar autocompletar con todos los nombres de cookies que se encuentren.</span><span class="sxs-lookup"><span data-stu-id="13f12-208">DevTools populate the autocomplete with all of the cookie names that are found.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="13f12-209">Muestra los recursos que tienen un `Set-Cookie` encabezado con un valor que coincide con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="13f12-209">Displays resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="13f12-210">DevTools rellenar autocompletar con todos los valores de las cookies que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="13f12-210">DevTools populate the autocomplete with all of the cookie values that are found.</span></span> |  
| `status-code` | <span data-ttu-id="13f12-211">Muestra los recursos que coinciden con el código de Estado HTTP específico.</span><span class="sxs-lookup"><span data-stu-id="13f12-211">Displays resources that match the specific HTTP status code.</span></span>  <span data-ttu-id="13f12-212">DevTools rellena el menú desplegable de autocompletar con todos los códigos de estado que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="13f12-212">DevTools populates the autocomplete dropdown menu with all of the status codes that are found.</span></span> |  

### <span data-ttu-id="13f12-213">Filtrar solicitudes por tipo</span><span class="sxs-lookup"><span data-stu-id="13f12-213">Filter requests by type</span></span>  

<span data-ttu-id="13f12-214">Para filtrar las solicitudes por tipo de solicitud, seleccione uno de los siguientes botones en el panel **red** .</span><span class="sxs-lookup"><span data-stu-id="13f12-214">To filter requests by request type, select the one of the following buttons on the **Network** panel.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-215">XHR</span><span class="sxs-lookup"><span data-stu-id="13f12-215">XHR</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-216">JS</span><span class="sxs-lookup"><span data-stu-id="13f12-216">JS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-217">CSS</span><span class="sxs-lookup"><span data-stu-id="13f12-217">CSS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-218">IMG</span><span class="sxs-lookup"><span data-stu-id="13f12-218">Img</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-219">Multimedia</span><span class="sxs-lookup"><span data-stu-id="13f12-219">Media</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-220">Fuente</span><span class="sxs-lookup"><span data-stu-id="13f12-220">Font</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-221">Dividir</span><span class="sxs-lookup"><span data-stu-id="13f12-221">Doc</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-222">EB</span><span class="sxs-lookup"><span data-stu-id="13f12-222">WS</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-223">WebSocket.</span><span class="sxs-lookup"><span data-stu-id="13f12-223">WebSocket.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-224">Manifiesta</span><span class="sxs-lookup"><span data-stu-id="13f12-224">Manifest</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-225">Otros</span><span class="sxs-lookup"><span data-stu-id="13f12-225">Other</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-226">Cualquier otro tipo no incluido en la lista.</span><span class="sxs-lookup"><span data-stu-id="13f12-226">Any other type not listed.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="13f12-227">Si los botones no se muestran, es posible que el panel **filtros** esté oculto.</span><span class="sxs-lookup"><span data-stu-id="13f12-227">If the buttons do not display, the **Filters** pane may be hidden.</span></span>  
<span data-ttu-id="13f12-228">Para obtener más información, vaya a [ocultar el panel de filtros](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="13f12-228">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="13f12-229">Para habilitar varios filtros de tipo al mismo tiempo, mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y, a continuación, seleccione.</span><span class="sxs-lookup"><span data-stu-id="13f12-229">To enable multiple type filters simultaneously, hold `Control` \(Windows\) or `Command` \(macOS\) and then select.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Panel red" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="13f12-231">Usar los filtros de tipo para mostrar los recursos JS, CSS y Document</span><span class="sxs-lookup"><span data-stu-id="13f12-231">Using the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-232">Filtrar solicitudes por tiempo</span><span class="sxs-lookup"><span data-stu-id="13f12-232">Filter requests by time</span></span>  

<span data-ttu-id="13f12-233">Seleccione y arrastre a la izquierda o a la derecha en el panel de descripción para mostrar solo las solicitudes que estaban activas durante ese período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="13f12-233">Select and drag left or right on the Overview pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="13f12-234">El filtro es inclusivo.</span><span class="sxs-lookup"><span data-stu-id="13f12-234">The filter is inclusive.</span></span>  <span data-ttu-id="13f12-235">Se muestra cualquier solicitud que estuviera activa durante la hora resaltada.</span><span class="sxs-lookup"><span data-stu-id="13f12-235">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Panel red" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="13f12-237">Filtrar las solicitudes que hayan estado inactivas aproximadamente 300 ms</span><span class="sxs-lookup"><span data-stu-id="13f12-237">Filtering out any requests that were inactive around 300 ms</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-238">Ocultar direcciones URL de datos</span><span class="sxs-lookup"><span data-stu-id="13f12-238">Hide data URLs</span></span>  

<span data-ttu-id="13f12-239">Las [direcciones URL de datos][MDNHTTPDataURIs] son pequeños archivos incrustados en otros documentos.</span><span class="sxs-lookup"><span data-stu-id="13f12-239">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="13f12-240">Cualquier solicitud que se muestre en la tabla solicitudes que comienza por `data:` es una dirección URL de datos.</span><span class="sxs-lookup"><span data-stu-id="13f12-240">Any request that displays in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="13f12-241">Active la casilla **ocultar direcciones URL de datos** para ocultar las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="13f12-241">Check the **Hide data URLs** checkbox to hide the requests.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Panel red" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="13f12-243">La casilla **ocultar direcciones URL de datos**</span><span class="sxs-lookup"><span data-stu-id="13f12-243">The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="13f12-244">Ordenar solicitudes</span><span class="sxs-lookup"><span data-stu-id="13f12-244">Sort requests</span></span>  

<span data-ttu-id="13f12-245">De forma predeterminada, las solicitudes de la tabla solicitudes se ordenan por hora de inicio, pero puede ordenar la tabla mediante otros criterios.</span><span class="sxs-lookup"><span data-stu-id="13f12-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="13f12-246">Ordenar por columna</span><span class="sxs-lookup"><span data-stu-id="13f12-246">Sort by column</span></span>  

<span data-ttu-id="13f12-247">Seleccione el encabezado de cualquier columna en las solicitudes para ordenar las solicitudes por esa columna.</span><span class="sxs-lookup"><span data-stu-id="13f12-247">Select the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="13f12-248">Ordenar por fase de actividad</span><span class="sxs-lookup"><span data-stu-id="13f12-248">Sort by activity phase</span></span>  

<span data-ttu-id="13f12-249">Para cambiar la forma en que la cascada ordena las solicitudes, desplace el puntero sobre el encabezado de la tabla solicitudes, abra el menú contextual \ (haga clic con el botón derecho \), desplace el puntero sobre la **cascada**y seleccione una de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="13f12-249">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover over **Waterfall**, and select one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-250">Hora de inicio</span><span class="sxs-lookup"><span data-stu-id="13f12-250">Start Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-251">La primera solicitud iniciada se encuentra en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="13f12-251">The first request that was initiated is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-252">Tiempo de respuesta</span><span class="sxs-lookup"><span data-stu-id="13f12-252">Response Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-253">La primera solicitud que comenzó a descargarse está en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="13f12-253">The first request that started downloading is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-254">Hora de finalización</span><span class="sxs-lookup"><span data-stu-id="13f12-254">End Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-255">La primera solicitud que ha finalizado se encuentra en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="13f12-255">The first request that finished is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-256">Duración total</span><span class="sxs-lookup"><span data-stu-id="13f12-256">Total Duration</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-257">La solicitud con la configuración de conexión más corta, solicitud o respuesta, se encuentra en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="13f12-257">The request with the shortest connection settings and request or response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-258">Latencia</span><span class="sxs-lookup"><span data-stu-id="13f12-258">Latency</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-259">La solicitud que esperó el tiempo más breve para una respuesta está en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="13f12-259">The request that waited the shortest time for a response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="13f12-260">En estas descripciones se supone que cada opción respectiva está clasificada de menor a mayor.</span><span class="sxs-lookup"><span data-stu-id="13f12-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="13f12-261">Al seleccionar el encabezado de la columna **cascada** se invierte el orden.</span><span class="sxs-lookup"><span data-stu-id="13f12-261">Selecting the header of the **Waterfall** column reverses the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Panel red" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="13f12-263">Ordenar la cascada por duración total \ (la parte más clara de cada barra está en espera y la parte más oscura es el tiempo dedicado a descargar bytes \)</span><span class="sxs-lookup"><span data-stu-id="13f12-263">Sorting the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="13f12-264">Analizar solicitudes</span><span class="sxs-lookup"><span data-stu-id="13f12-264">Analyze requests</span></span>  

<span data-ttu-id="13f12-265">Siempre que DevTools estén abiertos, registra todas las solicitudes en el panel red.</span><span class="sxs-lookup"><span data-stu-id="13f12-265">So long as DevTools are open, it logs all requests in the Network panel.</span></span>  
<span data-ttu-id="13f12-266">Use el panel red para analizar las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="13f12-266">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="13f12-267">Ver un registro de solicitudes</span><span class="sxs-lookup"><span data-stu-id="13f12-267">View a log of requests</span></span>  

<span data-ttu-id="13f12-268">Use la tabla solicitudes para ver un registro de todas las solicitudes realizadas mientras DevTools abierto.</span><span class="sxs-lookup"><span data-stu-id="13f12-268">Use the Requests table to view a log of all requests made while DevTools have been open.</span></span>  <span data-ttu-id="13f12-269">Al seleccionar o mantener el puntero sobre solicitudes, se muestra más información sobre cada elemento.</span><span class="sxs-lookup"><span data-stu-id="13f12-269">Selecting or hovering over requests reveals more information about each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="13f12-271">La tabla solicitudes</span><span class="sxs-lookup"><span data-stu-id="13f12-271">The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="13f12-272">De forma predeterminada, en la tabla solicitudes se muestran las siguientes columnas.</span><span class="sxs-lookup"><span data-stu-id="13f12-272">The Requests table displays the following columns by default.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-273">Nombre</span><span class="sxs-lookup"><span data-stu-id="13f12-273">Name</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-274">El nombre de archivo de un recurso o un identificador de él.</span><span class="sxs-lookup"><span data-stu-id="13f12-274">The filename of, or an identifier for, the resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-275">Estado</span><span class="sxs-lookup"><span data-stu-id="13f12-275">Status</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-276">El código de Estado HTTP.</span><span class="sxs-lookup"><span data-stu-id="13f12-276">The HTTP status code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-277">Tipo</span><span class="sxs-lookup"><span data-stu-id="13f12-277">Type</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-278">Tipo MIME del recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="13f12-278">The MIME type of the requested resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-279">Inició</span><span class="sxs-lookup"><span data-stu-id="13f12-279">Initiator</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-280">Los siguientes objetos o procesos inician solicitudes.</span><span class="sxs-lookup"><span data-stu-id="13f12-280">The following objects or processes initiate requests.</span></span>  
      
      *   <span data-ttu-id="13f12-281">**Analizador**  El analizador HTML para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="13f12-281">**Parser**  The HTML parser for Microsoft Edge.</span></span>  
      *   <span data-ttu-id="13f12-282">**Redirigir**  Una redirección de HTTP.</span><span class="sxs-lookup"><span data-stu-id="13f12-282">**Redirect**  An HTTP redirect.</span></span>  
      *   <span data-ttu-id="13f12-283">**Script**  Una función de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="13f12-283">**Script**  A JavaScript function.</span></span>  
      *   <span data-ttu-id="13f12-284">**Otros**  Otro proceso o acción, como navegar a una página con un vínculo o escribir una dirección URL en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="13f12-284">**Other**  Some other process or action, such as navigating to a page using a link or entering a URL in the address bar.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-285">Tamaño</span><span class="sxs-lookup"><span data-stu-id="13f12-285">Size</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-286">El tamaño combinado de los encabezados de respuesta más el cuerpo de la respuesta, tal y como lo proporciona el servidor.</span><span class="sxs-lookup"><span data-stu-id="13f12-286">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-287">Tiempo</span><span class="sxs-lookup"><span data-stu-id="13f12-287">Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-288">La duración total, desde el inicio de la solicitud hasta la recepción del byte final en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="13f12-288">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="13f12-289">Cascada</span><span class="sxs-lookup"><span data-stu-id="13f12-289">Waterfall</span></span>](#view-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-290">Un desglose visual de la actividad de cada solicitud.</span><span class="sxs-lookup"><span data-stu-id="13f12-290">A visual breakdown of the activity for each request.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="13f12-291">Agregar o quitar columnas</span><span class="sxs-lookup"><span data-stu-id="13f12-291">Add or remove columns</span></span>  

<span data-ttu-id="13f12-292">Desplace el puntero en el encabezado de la tabla solicitudes, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione una opción para ocultarlo o mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="13f12-292">Hover on the header of the Requests table, open the contextual menu \(right-click\), and select an option to hide or show it.</span></span>  <span data-ttu-id="13f12-293">Las opciones mostradas actualmente tienen marcas de verificación junto a cada elemento.</span><span class="sxs-lookup"><span data-stu-id="13f12-293">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="13f12-295">Agregar una columna a la tabla solicitudes</span><span class="sxs-lookup"><span data-stu-id="13f12-295">Adding a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="13f12-296">Agregar columnas personalizadas</span><span class="sxs-lookup"><span data-stu-id="13f12-296">Add custom columns</span></span>  

<span data-ttu-id="13f12-297">Para agregar una columna personalizada a la tabla solicitudes, desplace el puntero sobre el encabezado de la tabla solicitudes, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **encabezados de respuesta**para  >  **administrar columnas de encabezado**.</span><span class="sxs-lookup"><span data-stu-id="13f12-297">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and select **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="13f12-299">Agregar una columna personalizada a la tabla solicitudes</span><span class="sxs-lookup"><span data-stu-id="13f12-299">Adding a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-300">Ver la relación de sincronización de las solicitudes</span><span class="sxs-lookup"><span data-stu-id="13f12-300">View the timing relationship of requests</span></span>  

<span data-ttu-id="13f12-301">Use la cascada para ver las relaciones de temporización de las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="13f12-301">Use the Waterfall to view the timing relationships of requests.</span></span>  
<span data-ttu-id="13f12-302">La organización predeterminada de la cascada usa la hora de inicio de las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="13f12-302">The default organization of the Waterfall uses the start time of the requests.</span></span>  
<span data-ttu-id="13f12-303">Por lo tanto, las solicitudes que se encuentren más lejanas a la izquierda iniciadas antes que las solicitudes más lejanas a la derecha.</span><span class="sxs-lookup"><span data-stu-id="13f12-303">So, requests that are farther to the left started earlier than the requests that are farther to the right.</span></span>  

<span data-ttu-id="13f12-304">Para revisar las diferentes maneras en las que puede ordenar la cascada, vaya a [ordenar por fase de actividad](#sort-by-activity-phase).</span><span class="sxs-lookup"><span data-stu-id="13f12-304">To review the different ways that you may sort the Waterfall, navigate to [Sort by activity phase](#sort-by-activity-phase).</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="13f12-306">La columna cascada del panel **solicitudes**</span><span class="sxs-lookup"><span data-stu-id="13f12-306">The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To view the frames of a WebSocket connection, use the following steps.  

1.  Select the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Select the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-select the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="Panel red" lightbox="../media/network-frames.msft.png":::
   The **Frames** tab  
:::image-end:::  
-->

<!--The table contains the following three columns.  

*   **Data**.  The message payload.  If the message is plain text, it is displayed here.  For binary opcodes, this column displays the name and code of the opcode.  The following opcodes are supported: Continuation Frame, Binary Frame, Connection Close Frame, Ping Frame, and Pong Frame.  
*   **Length**.  The length of the message payload, in bytes.  
*   **Time**.  The time when the message was received or sent.  -->

<!--Messages are color-coded according to each type.  

*   Outgoing text messages are light-green.  
*   Incoming text messages are white.  
*   WebSocket opcodes are light-yellow.  
*   Errors are light-red.  -->

### <span data-ttu-id="13f12-307">Ver una vista previa del cuerpo de una respuesta</span><span class="sxs-lookup"><span data-stu-id="13f12-307">View a preview of a response body</span></span>  

<span data-ttu-id="13f12-308">Para ver una vista previa del cuerpo de una respuesta, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="13f12-308">To view a preview of a response body, use the following steps.</span></span>  

1.  <span data-ttu-id="13f12-309">Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="13f12-309">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="13f12-310">Seleccione la pestaña **vista previa** .</span><span class="sxs-lookup"><span data-stu-id="13f12-310">Select the **Preview** tab.</span></span>  

<span data-ttu-id="13f12-311">Esta pestaña es principalmente útil para visualizar imágenes.</span><span class="sxs-lookup"><span data-stu-id="13f12-311">This tab is mostly useful for viewing images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="Panel red" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="13f12-313">La ficha **vista previa**</span><span class="sxs-lookup"><span data-stu-id="13f12-313">The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-314">Ver el cuerpo de una respuesta</span><span class="sxs-lookup"><span data-stu-id="13f12-314">View a response body</span></span>  

<span data-ttu-id="13f12-315">Para ver el cuerpo de la respuesta de una solicitud, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="13f12-315">To view the response body to a request, use the following steps.</span></span>  

1.  <span data-ttu-id="13f12-316">Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="13f12-316">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="13f12-317">Seleccione la pestaña **respuesta** .</span><span class="sxs-lookup"><span data-stu-id="13f12-317">Select the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="Panel red" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="13f12-319">La ficha **respuesta**</span><span class="sxs-lookup"><span data-stu-id="13f12-319">The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-320">Ver encabezados HTTP</span><span class="sxs-lookup"><span data-stu-id="13f12-320">View HTTP headers</span></span>  

<span data-ttu-id="13f12-321">Para ver los datos del encabezado HTTP sobre una solicitud, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="13f12-321">To view HTTP header data about a request, use the following steps.</span></span>  

1.  <span data-ttu-id="13f12-322">Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="13f12-322">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="13f12-323">Seleccione la pestaña **encabezados** .</span><span class="sxs-lookup"><span data-stu-id="13f12-323">Select the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Panel red" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="13f12-325">La pestaña **encabezados**</span><span class="sxs-lookup"><span data-stu-id="13f12-325">The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="13f12-326">Ver origen de encabezado HTTP</span><span class="sxs-lookup"><span data-stu-id="13f12-326">View HTTP header source</span></span>  

<span data-ttu-id="13f12-327">De forma predeterminada, la pestaña encabezados muestra los nombres de encabezado alfabéticamente.</span><span class="sxs-lookup"><span data-stu-id="13f12-327">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="13f12-328">Para ver los nombres de encabezados HTTP en el orden recibido, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="13f12-328">To view the HTTP header names in the order received, use the following steps.</span></span>  

1.  <span data-ttu-id="13f12-329">Abre la pestaña **encabezados** para la solicitud que te interese.</span><span class="sxs-lookup"><span data-stu-id="13f12-329">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="13f12-330">Para obtener más información, vaya a [Ver encabezados HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="13f12-330">For more information, navigate to [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="13f12-331">Seleccione **Ver origen**, junto a la sección **solicitar** encabezado o **respuesta de encabezado** .</span><span class="sxs-lookup"><span data-stu-id="13f12-331">Select **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="13f12-332">Ver parámetros de cadena de consulta</span><span class="sxs-lookup"><span data-stu-id="13f12-332">View query string parameters</span></span>  

<span data-ttu-id="13f12-333">Para ver los parámetros de cadena de consulta de una dirección URL en un formato legible, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="13f12-333">To view the query string parameters of a URL in a human-readable format, use the following steps.</span></span>  

1.  <span data-ttu-id="13f12-334">Abre la pestaña **encabezados** para la solicitud que te interese.</span><span class="sxs-lookup"><span data-stu-id="13f12-334">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="13f12-335">Para obtener más información, vaya a [Ver encabezados HTTP](#view-http-headers).</span><span class="sxs-lookup"><span data-stu-id="13f12-335">For more information, navigate to [View HTTP headers](#view-http-headers).</span></span>  
1.  <span data-ttu-id="13f12-336">Vaya a la sección **parámetros de cadena de consulta** .</span><span class="sxs-lookup"><span data-stu-id="13f12-336">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Panel red" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="13f12-338">Sección **parámetros de cadena de consulta**</span><span class="sxs-lookup"><span data-stu-id="13f12-338">The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="13f12-339">Ver origen de parámetros de cadena de consulta</span><span class="sxs-lookup"><span data-stu-id="13f12-339">View query string parameters source</span></span>  

<span data-ttu-id="13f12-340">Para ver el origen de parámetro de cadena de consulta de una solicitud, realice los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="13f12-340">To view the query string parameter source of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="13f12-341">Vaya a la sección parámetros de cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="13f12-341">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="13f12-342">Para obtener más información, vaya a [ver parámetros de cadena de consulta](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="13f12-342">For more information, navigate to [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="13f12-343">Seleccione **Ver origen**.</span><span class="sxs-lookup"><span data-stu-id="13f12-343">Select **view source**.</span></span>  

#### <span data-ttu-id="13f12-344">Ver parámetros de cadena de consulta con codificación URL</span><span class="sxs-lookup"><span data-stu-id="13f12-344">View URL-encoded query string parameters</span></span>  

<span data-ttu-id="13f12-345">Para ver los parámetros de cadena de consulta en un formato legible, pero con las codificaciones conservadas, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="13f12-345">To view query string parameters in a human-readable format, but with encodings preserved, use the following steps.</span></span>  

1.  <span data-ttu-id="13f12-346">Vaya a la sección parámetros de cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="13f12-346">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="13f12-347">Para obtener más información, vaya a [ver parámetros de cadena de consulta](#view-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="13f12-347">For more information, navigate to [View query string parameters](#view-query-string-parameters).</span></span>  
1.  <span data-ttu-id="13f12-348">Seleccione **Ver dirección URL codificada**.</span><span class="sxs-lookup"><span data-stu-id="13f12-348">Select **view URL encoded**.</span></span>  

### <span data-ttu-id="13f12-349">Ver cookies</span><span class="sxs-lookup"><span data-stu-id="13f12-349">View cookies</span></span>  

<span data-ttu-id="13f12-350">Para ver las cookies enviadas en el encabezado HTTP de una solicitud, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="13f12-350">To view the cookies sent in the HTTP header of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="13f12-351">Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="13f12-351">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="13f12-352">Seleccione la ficha **cookies** .</span><span class="sxs-lookup"><span data-stu-id="13f12-352">Select the **Cookies** tab.</span></span>  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="Panel red" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="13f12-354">La ficha cookies</span><span class="sxs-lookup"><span data-stu-id="13f12-354">The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-355">Ver el desglose de intervalos de una solicitud</span><span class="sxs-lookup"><span data-stu-id="13f12-355">View the timing breakdown of a request</span></span>  

<span data-ttu-id="13f12-356">Para ver el desglose de intervalos de una solicitud, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="13f12-356">To view the timing breakdown of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="13f12-357">Seleccione la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="13f12-357">Select the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="13f12-358">Seleccione la pestaña **intervalos** .</span><span class="sxs-lookup"><span data-stu-id="13f12-358">Select the **Timing** tab.</span></span>  

<span data-ttu-id="13f12-359">Para obtener acceso a los datos de una manera más rápida, navegue para [obtener una vista previa de un desglose por intervalos](#preview-a-timing-breakdown).</span><span class="sxs-lookup"><span data-stu-id="13f12-359">For a faster way to access the data, navigate to [Preview a timing breakdown](#preview-a-timing-breakdown).</span></span>  

<span data-ttu-id="13f12-360">Para obtener más información acerca de cada una de las fases que se pueden mostrar en la pestaña **intervalos** , vaya a [fases de desglose por intervalos explicadas](#timing-breakdown-phases-explained).</span><span class="sxs-lookup"><span data-stu-id="13f12-360">For more information about each of the phases that may be displayed in the **Timing** tab, navigate to [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="Panel red" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="13f12-362">La ficha **intervalos**</span><span class="sxs-lookup"><span data-stu-id="13f12-362">The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="13f12-363">Más información sobre cada una de las fases.</span><span class="sxs-lookup"><span data-stu-id="13f12-363">More information about each of the phases.</span></span>  

<span data-ttu-id="13f12-364">Para obtener más información sobre cómo obtener acceso a la vista, vaya a [Ver desglose de intervalos](#view-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="13f12-364">For more information about accessing the view, navigate to [View timing breakdown](#view-the-timing-breakdown-of-a-request).</span></span>  

#### <span data-ttu-id="13f12-365">Obtener una vista previa de intervalos</span><span class="sxs-lookup"><span data-stu-id="13f12-365">Preview a timing breakdown</span></span>  

<span data-ttu-id="13f12-366">Para obtener una vista previa del desglose de intervalos de una solicitud, en la columna **cascada** de la tabla solicitudes, desplace el puntero sobre la entrada de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="13f12-366">To view a preview of the timing breakdown of a request, in the **Waterfall** column of the Requests table, hover on the entry for the request.</span></span>  

<span data-ttu-id="13f12-367">Para obtener más información sobre cómo obtener acceso a los datos sin mantener el mouse, navegue para [ver el desglose de intervalos de una solicitud](#view-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="13f12-367">For more information about how to access the data without hovering, navigate to [View the timing breakdown of a request](#view-the-timing-breakdown-of-a-request).</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="Panel red" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="13f12-369">Obtener una vista previa del desglose de intervalos de una solicitud</span><span class="sxs-lookup"><span data-stu-id="13f12-369">Previewing the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="13f12-370">Explicación de fases de desglose de intervalos</span><span class="sxs-lookup"><span data-stu-id="13f12-370">Timing breakdown phases explained</span></span>  

<span data-ttu-id="13f12-371">Más información sobre cada una de las fases que pueden mostrarse en la pestaña **intervalos** .</span><span class="sxs-lookup"><span data-stu-id="13f12-371">More information about each of the phases that may display in the **Timing** tab.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-372">Poner en cola</span><span class="sxs-lookup"><span data-stu-id="13f12-372">Queueing</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-373">El explorador pone en cola las solicitudes cuando cualquiera de las siguientes condiciones es verdadera.</span><span class="sxs-lookup"><span data-stu-id="13f12-373">The browser queues requests when any of the following are true.</span></span>  
      *   <span data-ttu-id="13f12-374">Hay solicitudes de prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="13f12-374">Higher priority requests exist.</span></span>  
      *   <span data-ttu-id="13f12-375">Hay seis conexiones TCP abiertas para el mismo origen, que es el límite.</span><span class="sxs-lookup"><span data-stu-id="13f12-375">Six TCP connections are open for the same origin, which is the limit.</span></span>  <span data-ttu-id="13f12-376">Solo se aplica a HTTP/1.0 y HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="13f12-376">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
      *   <span data-ttu-id="13f12-377">El explorador está asignando un poco de espacio en la caché de disco.</span><span class="sxs-lookup"><span data-stu-id="13f12-377">The browser is briefly allocating space in the disk cache.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-378">Paralizado</span><span class="sxs-lookup"><span data-stu-id="13f12-378">Stalled</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-379">La solicitud se detiene por cualquiera de las razones descritas en **puesta en cola**.</span><span class="sxs-lookup"><span data-stu-id="13f12-379">The request is stalled for any of the reasons described in **Queueing**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-380">Búsqueda de DNS</span><span class="sxs-lookup"><span data-stu-id="13f12-380">DNS Lookup</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-381">El explorador está resolviendo la dirección IP de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="13f12-381">The browser is resolving the IP address for the request.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-382">Conexión inicial</span><span class="sxs-lookup"><span data-stu-id="13f12-382">Initial connection</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-383">El explorador establece una conexión que incluye los protocolos de enlace TCP, los reintentos de TCP y negocia una capa de sockets seguros.</span><span class="sxs-lookup"><span data-stu-id="13f12-383">The browser establishes a connection including TCP handshakes, TCP retries, and negotiates a Secure Socket Layer.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-384">Negociación de proxy</span><span class="sxs-lookup"><span data-stu-id="13f12-384">Proxy negotiation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-385">El explorador está negociando la solicitud con un [servidor proxy][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="13f12-385">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-386">Solicitud enviada</span><span class="sxs-lookup"><span data-stu-id="13f12-386">Request sent</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-387">Se está enviando la solicitud.</span><span class="sxs-lookup"><span data-stu-id="13f12-387">The request is being sent.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-388">Preparación de ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="13f12-388">ServiceWorker Preparation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-389">El explorador está iniciando el trabajo del servicio.</span><span class="sxs-lookup"><span data-stu-id="13f12-389">The browser is starting the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-390">Solicitud para ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="13f12-390">Request to ServiceWorker</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-391">La solicitud se está enviando al trabajador del servicio.</span><span class="sxs-lookup"><span data-stu-id="13f12-391">The request is being sent to the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-392">Esperando \ (TTFB \)</span><span class="sxs-lookup"><span data-stu-id="13f12-392">Waiting \(TTFB\)</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-393">El explorador está esperando el primer byte de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="13f12-393">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="13f12-394">TTFB es el primer byte.</span><span class="sxs-lookup"><span data-stu-id="13f12-394">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="13f12-395">Este intervalo incluye un recorrido de ida y vuelta de la latencia y el tiempo que el servidor tomó para preparar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="13f12-395">This timing includes one round trip of latency and the time the server took to prepare the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-396">Descarga de contenido</span><span class="sxs-lookup"><span data-stu-id="13f12-396">Content Download</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-397">El explorador está recibiendo la respuesta.</span><span class="sxs-lookup"><span data-stu-id="13f12-397">The browser is receiving the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-398">Recepción de envío</span><span class="sxs-lookup"><span data-stu-id="13f12-398">Receiving Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-399">El explorador está recibiendo datos de esta respuesta a través de la inserción de servidor HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="13f12-399">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-400">Insertar inserción</span><span class="sxs-lookup"><span data-stu-id="13f12-400">Reading Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-401">El explorador está leyendo los datos locales recibidos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="13f12-401">The browser is reading the local data previously received.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="13f12-402">Ver iniciadores y dependencias</span><span class="sxs-lookup"><span data-stu-id="13f12-402">View initiators and dependencies</span></span>  

<span data-ttu-id="13f12-403">Para ver los iniciadores y las dependencias de una solicitud, mantenga presionado `Shift` el mouse sobre la solicitud en la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="13f12-403">To view the initiators and dependencies of a request, hold `Shift`and hover over the request in the Requests table.</span></span>  <span data-ttu-id="13f12-404">Colores de DevTools: los iniciadores se muestran en verde y las dependencias en rojo.</span><span class="sxs-lookup"><span data-stu-id="13f12-404">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Panel red" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="13f12-406">Visualización de los iniciadores y las dependencias de una solicitud</span><span class="sxs-lookup"><span data-stu-id="13f12-406">Viewing the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="13f12-407">Cuando la tabla solicitudes está ordenada cronológicamente, si coloca el puntero sobre una línea, la línea anterior muestra una solicitud verde.</span><span class="sxs-lookup"><span data-stu-id="13f12-407">When the Requests table is ordered chronologically, if you hover on a line, the line preceding it displays a green request.</span></span>  <span data-ttu-id="13f12-408">La solicitud verde es el iniciador de la dependencia.</span><span class="sxs-lookup"><span data-stu-id="13f12-408">The green request is the initiator of the dependency.</span></span>  <span data-ttu-id="13f12-409">Si se muestra otra solicitud verde en la línea antes de ella, esa solicitud superior es el iniciador del iniciador.</span><span class="sxs-lookup"><span data-stu-id="13f12-409">If another green request is displayed on the line before that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="13f12-410">Etcétera.</span><span class="sxs-lookup"><span data-stu-id="13f12-410">And so on.</span></span>  

### <span data-ttu-id="13f12-411">Ver eventos de carga</span><span class="sxs-lookup"><span data-stu-id="13f12-411">View load events</span></span>  

<span data-ttu-id="13f12-412">DevTools muestra la temporización de los `DOMContentLoaded` `load` eventos y en varios lugares del panel red.</span><span class="sxs-lookup"><span data-stu-id="13f12-412">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the Network panel.</span></span>  <span data-ttu-id="13f12-413">El `DOMContentLoaded` evento está coloreado en azul y el `load` evento es rojo.</span><span class="sxs-lookup"><span data-stu-id="13f12-413">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="13f12-415">Las ubicaciones de los `DOMContentLoaded` `load` eventos y en el panel red</span><span class="sxs-lookup"><span data-stu-id="13f12-415">The locations of the `DOMContentLoaded` and `load` events on the Network panel</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-416">Ver el número total de solicitudes</span><span class="sxs-lookup"><span data-stu-id="13f12-416">View the total number of requests</span></span>  

<span data-ttu-id="13f12-417">El número total de solicitudes se muestra en el panel Resumen, en la parte inferior del panel red.</span><span class="sxs-lookup"><span data-stu-id="13f12-417">The total number of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="13f12-418">Este número solo realiza un seguimiento de las solicitudes que se han registrado desde que se abrió DevTools.</span><span class="sxs-lookup"><span data-stu-id="13f12-418">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="13f12-419">Si se han producido otras solicitudes antes de que se abriera DevTools, esas solicitudes no se cuentan.</span><span class="sxs-lookup"><span data-stu-id="13f12-419">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="Panel red" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="13f12-421">El número total de solicitudes desde que DevTools se abrieron</span><span class="sxs-lookup"><span data-stu-id="13f12-421">The total number of requests since DevTools were opened</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-422">Ver el tamaño total de la descarga</span><span class="sxs-lookup"><span data-stu-id="13f12-422">View the total download size</span></span>  

<span data-ttu-id="13f12-423">El tamaño total de las solicitudes de descarga se muestra en el panel Resumen, en la parte inferior del panel red.</span><span class="sxs-lookup"><span data-stu-id="13f12-423">The total download size of requests is listed in the Summary pane, at the bottom of the Network panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="13f12-424">Este número solo realiza un seguimiento de las solicitudes que se han registrado desde que se abrió DevTools.</span><span class="sxs-lookup"><span data-stu-id="13f12-424">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="13f12-425">Si se han producido otras solicitudes antes de que se abriera DevTools, no se cuentan las solicitudes anteriores.</span><span class="sxs-lookup"><span data-stu-id="13f12-425">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="Panel red" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="13f12-427">El tamaño total de las solicitudes de descarga</span><span class="sxs-lookup"><span data-stu-id="13f12-427">The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="13f12-428">Para comprobar cómo los recursos grandes están después de que el explorador descomprime cada elemento, navegue para [ver el tamaño descomprimido de un recurso](#view-the-uncompressed-size-of-a-resource).</span><span class="sxs-lookup"><span data-stu-id="13f12-428">To verify how large resources are after the browser uncompresses each item, navigate to [View the uncompressed size of a resource](#view-the-uncompressed-size-of-a-resource).</span></span>  

### <span data-ttu-id="13f12-429">Ver el seguimiento de la pila que causó una solicitud</span><span class="sxs-lookup"><span data-stu-id="13f12-429">View the stack trace that caused a request</span></span>  

<span data-ttu-id="13f12-430">Después de que una instrucción de JavaScript solicite un recurso, mueva el puntero sobre la columna de **iniciador** para ver el seguimiento de la pila que se dirige a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="13f12-430">After a JavaScript statement requests a resource, hover over the **Initiator** column to view the stack trace leading up to the request.</span></span>  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="13f12-432">El seguimiento de la pila que lleva a una solicitud de recursos</span><span class="sxs-lookup"><span data-stu-id="13f12-432">The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-433">Ver el tamaño descomprimido de un recurso</span><span class="sxs-lookup"><span data-stu-id="13f12-433">View the uncompressed size of a resource</span></span>  

<span data-ttu-id="13f12-434">Seleccione la casilla **usar filas de solicitudes grandes** y, a continuación, mire el valor inferior de la columna **tamaño** .</span><span class="sxs-lookup"><span data-stu-id="13f12-434">Select the **Use large request rows** checkbox and then look at the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="13f12-436">Un ejemplo de recursos sin comprimir \ (el tamaño comprimido del `jquery-3.3.1.min.js` archivo que se envió a través de la red fue `29.9 KB` , mientras que el tamaño descomprimido fue `84.9 KB` \)</span><span class="sxs-lookup"><span data-stu-id="13f12-436">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="13f12-437">Exportar datos de solicitudes</span><span class="sxs-lookup"><span data-stu-id="13f12-437">Export requests data</span></span>  

### <span data-ttu-id="13f12-438">Guardar todas las solicitudes de red en un archivo HAR</span><span class="sxs-lookup"><span data-stu-id="13f12-438">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="13f12-439">Para guardar todas las solicitudes de red en un archivo HAR, siga los pasos que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="13f12-439">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="13f12-440">Mantenga el mouse sobre cualquier solicitud de la tabla solicitudes y abra el menú contextual \ (haga clic con el botón derecho \).</span><span class="sxs-lookup"><span data-stu-id="13f12-440">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="13f12-441">Seleccione **Guardar como Har with Content**.</span><span class="sxs-lookup"><span data-stu-id="13f12-441">Select **Save as HAR with Content**.</span></span>  <span data-ttu-id="13f12-442">DevTools guarda todas las solicitudes que se han producido desde que abrió DevTools en el archivo HAR.</span><span class="sxs-lookup"><span data-stu-id="13f12-442">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="13f12-443">No puedes filtrar solicitudes.</span><span class="sxs-lookup"><span data-stu-id="13f12-443">You are not able to filter requests.</span></span>  <span data-ttu-id="13f12-444">Tampoco puedes guardar una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="13f12-444">You are also not able to save a single request.</span></span>  

<span data-ttu-id="13f12-445">Una vez que haya guardado un archivo HAR, podrá volver a importarlo en DevTools para analizarlo.</span><span class="sxs-lookup"><span data-stu-id="13f12-445">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="13f12-446">Simplemente arrastre y coloque el archivo HAR en la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="13f12-446">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="13f12-448">Seleccionar **Guardar como Har with Content**</span><span class="sxs-lookup"><span data-stu-id="13f12-448">Selecting **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-449">Copiar una o más solicitudes en el portapapeles</span><span class="sxs-lookup"><span data-stu-id="13f12-449">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="13f12-450">En la columna **nombre** de la tabla solicitudes, desplace el puntero sobre una solicitud y abra el menú contextual \ (haga clic con el botón derecho \), mueva el puntero sobre **copiar**y seleccione una de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="13f12-450">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover over **Copy**, and select one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-451">Copiar dirección del vínculo</span><span class="sxs-lookup"><span data-stu-id="13f12-451">Copy Link Address</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-452">Copie la dirección URL de la solicitud en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="13f12-452">Copy the URL of the request to the clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-453">Copiar respuesta</span><span class="sxs-lookup"><span data-stu-id="13f12-453">Copy Response</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-454">Copie el cuerpo de la respuesta en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="13f12-454">Copy the response body to the clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-455">Copiar como fetch</span><span class="sxs-lookup"><span data-stu-id="13f12-455">Copy as Fetch</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-456">Copiar como rizo</span><span class="sxs-lookup"><span data-stu-id="13f12-456">Copy as cURL</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-457">Copie la solicitud como un comando de rizo.</span><span class="sxs-lookup"><span data-stu-id="13f12-457">Copy the request as a cURL command.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-458">Copiar todo como fetch</span><span class="sxs-lookup"><span data-stu-id="13f12-458">Copy All as Fetch</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-459">Copiar todo como rizo</span><span class="sxs-lookup"><span data-stu-id="13f12-459">Copy All as cURL</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-460">Copiar todas las solicitudes como una cadena de comandos de rizo.</span><span class="sxs-lookup"><span data-stu-id="13f12-460">Copy all requests as a chain of cURL commands.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="13f12-461">Copiar todo como HAR</span><span class="sxs-lookup"><span data-stu-id="13f12-461">Copy All as HAR</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="13f12-462">Copie todas las solicitudes como datos de HAR.</span><span class="sxs-lookup"><span data-stu-id="13f12-462">Copy all requests as HAR data.</span></span>  
   :::column-end:::
:::row-end:::  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="13f12-464">Selección de **copiar respuesta**</span><span class="sxs-lookup"><span data-stu-id="13f12-464">Selecting **Copy Response**</span></span>  
:::image-end:::  

## <span data-ttu-id="13f12-465">Cambiar el diseño del panel red</span><span class="sxs-lookup"><span data-stu-id="13f12-465">Change the layout of the Network panel</span></span>  

<span data-ttu-id="13f12-466">Puede expandir o contraer secciones de la interfaz de usuario del panel red para destacar información importante.</span><span class="sxs-lookup"><span data-stu-id="13f12-466">You may expand or collapse sections of the Network panel UI to focus important information.</span></span>  

### <span data-ttu-id="13f12-467">Ocultar el panel de filtros</span><span class="sxs-lookup"><span data-stu-id="13f12-467">Hide the Filters pane</span></span>  

<span data-ttu-id="13f12-468">De forma predeterminada, DevTools muestra el **Panel filtros**.</span><span class="sxs-lookup"><span data-stu-id="13f12-468">By default, DevTools show the **Filters pane**.</span></span>  
<span data-ttu-id="13f12-469">Seleccione **filtro** \ ( ![ filtro ][ImageFilterIcon] \) para ocultarlo.</span><span class="sxs-lookup"><span data-stu-id="13f12-469">Select **Filter** \(![Filter][ImageFilterIcon]\) to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="Panel red" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="13f12-471">El botón ocultar filtros</span><span class="sxs-lookup"><span data-stu-id="13f12-471">The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-472">Usar filas de solicitudes grandes</span><span class="sxs-lookup"><span data-stu-id="13f12-472">Use large request rows</span></span>  

<span data-ttu-id="13f12-473">Use filas grandes cuando desee más espacios en blanco en la tabla solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="13f12-473">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="13f12-474">Algunas columnas también proporcionan un poco más de información cuando se usan filas grandes.</span><span class="sxs-lookup"><span data-stu-id="13f12-474">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="13f12-475">Por ejemplo, el valor inferior de la columna **tamaño** es el tamaño descomprimido de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="13f12-475">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="13f12-477">Ejemplo de filas de solicitudes grandes en el panel **solicitudes**</span><span class="sxs-lookup"><span data-stu-id="13f12-477">An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="13f12-478">Seleccione la casilla **usar filas de solicitudes grandes** para habilitar las filas grandes.</span><span class="sxs-lookup"><span data-stu-id="13f12-478">Select the **Use large request rows** checkbox to enable large rows.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="13f12-480">Casilla de verificación **usar filas de solicitudes grandes**</span><span class="sxs-lookup"><span data-stu-id="13f12-480">The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="13f12-481">Ocultar el panel de información general</span><span class="sxs-lookup"><span data-stu-id="13f12-481">Hide the Overview pane</span></span>  

<span data-ttu-id="13f12-482">De forma predeterminada, DevTools muestra el **Panel de información general**.</span><span class="sxs-lookup"><span data-stu-id="13f12-482">By default, DevTools show the **Overview pane**.</span></span>  <span data-ttu-id="13f12-483">Anule la selección de la casilla **Mostrar información general** para ocultarla.</span><span class="sxs-lookup"><span data-stu-id="13f12-483">Deselect the **Show Overview** checkbox to hide it.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Panel red" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="13f12-485">La casilla **Mostrar información general**</span><span class="sxs-lookup"><span data-stu-id="13f12-485">The **Show Overview** checkbox</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps.md "Depurar aplicaciones web progresivas | Microsoft docs"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "Direcciones URL de datos | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Servidor proxy-Wikipedia"  

> [!NOTE]
> <span data-ttu-id="13f12-489">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="13f12-489">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="13f12-490">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/network/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="13f12-490">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="13f12-492">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="13f12-492">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

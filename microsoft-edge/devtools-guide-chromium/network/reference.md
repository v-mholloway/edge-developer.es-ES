---
description: Una referencia completa de las características del panel de red de Microsoft Edge DevTools.
title: Referencia de análisis de red
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: c600197ffa0e415fe42aecc704a523d1b23f8260
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230757"
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

# <span data-ttu-id="80acc-104">Referencia de análisis de red</span><span class="sxs-lookup"><span data-stu-id="80acc-104">Network Analysis reference</span></span>  

<span data-ttu-id="80acc-105">Descubra nuevas formas de analizar cómo se carga su página en esta referencia completa de las características de análisis de red de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="80acc-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

## <span data-ttu-id="80acc-106">Registrar solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="80acc-106">Record network requests</span></span>  

<span data-ttu-id="80acc-107">De forma predeterminada, DevTools graba todas las solicitudes de red en el panel **red** , siempre y cuando DevTools esté abierto.</span><span class="sxs-lookup"><span data-stu-id="80acc-107">By default, DevTools record all network requests in the **Network** panel, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Panel red" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="80acc-109">Panel **red**</span><span class="sxs-lookup"><span data-stu-id="80acc-109">The **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-110">Detener la grabación de solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="80acc-110">Stop recording network requests</span></span>  

<span data-ttu-id="80acc-111">Siga los pasos que se indican a continuación para detener la grabación de solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80acc-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="80acc-112">En el panel **red** , seleccione **Detener grabación del registro de red** \ ( ![ detener la grabación del registro de red ][ImageRecordOnIcon] \).</span><span class="sxs-lookup"><span data-stu-id="80acc-112">On the **Network** panel, choose **Stop recording network log** \(![Stop recording network log][ImageRecordOnIcon]\).</span></span>  <span data-ttu-id="80acc-113">Se vuelve gris para indicar que DevTools ya no graba solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80acc-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="80acc-114">Seleccione `Control` + `E` \ (Windows, Linux \) o `Command` + `E` \ (MacOS \) mientras el panel **red** está en el foco.</span><span class="sxs-lookup"><span data-stu-id="80acc-114">Select `Control`+`E` \(Windows, Linux\) or `Command`+`E` \(macOS\) while the **Network** panel is in focus.</span></span>  

### <span data-ttu-id="80acc-115">Borrar solicitudes</span><span class="sxs-lookup"><span data-stu-id="80acc-115">Clear requests</span></span>  

<span data-ttu-id="80acc-116">Elija **Borrar** \ ( ![ Borrar ][ImageClearIcon] \) en el panel **red** para borrar todas las solicitudes de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80acc-116">Choose **Clear** \(![Clear][ImageClearIcon]\) on the **Network** panel to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="Botón borrar" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="80acc-118">Botón **Borrar**</span><span class="sxs-lookup"><span data-stu-id="80acc-118">The **Clear** button</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-119">Guardar solicitudes en la carga de páginas</span><span class="sxs-lookup"><span data-stu-id="80acc-119">Save requests across page loads</span></span>  

<span data-ttu-id="80acc-120">Para guardar las solicitudes en la carga de la página, en el panel **red** , active la casilla **conservar registro** .</span><span class="sxs-lookup"><span data-stu-id="80acc-120">To save requests across page loads, on the **Network** panel, turn on the **Preserve log** checkbox.</span></span>  <span data-ttu-id="80acc-121">DevTools guarda todas las solicitudes hasta que Deshabilites **conservar registro**.</span><span class="sxs-lookup"><span data-stu-id="80acc-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="Casilla de verificación conservar registro" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="80acc-123">Casilla de verificación **conservar registro**</span><span class="sxs-lookup"><span data-stu-id="80acc-123">The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-124">Capturar capturas de pantallas durante la carga de la página</span><span class="sxs-lookup"><span data-stu-id="80acc-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="80acc-125">Capture las capturas de pantallas para analizar qué se muestra para los usuarios mientras esperan la página que desea cargar.</span><span class="sxs-lookup"><span data-stu-id="80acc-125">Capture screenshots to analyze what displays for users while waiting for your page to load.</span></span>  

<span data-ttu-id="80acc-126">Para habilitar las capturas de pantalla, elija **configuración de red**y, en el panel **red** , active la casilla **capturar capturas** de pantalla.</span><span class="sxs-lookup"><span data-stu-id="80acc-126">To enable screenshots, choose **Network settings**, and on the **Network** panel, turn on the **Capture screenshots** checkbox.</span></span>  

<span data-ttu-id="80acc-127">Actualice la página mientras el panel **red** está enfocado para capturar capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="80acc-127">Refresh the page while the **Network** panel is in focus to capture screenshots.</span></span>  

<span data-ttu-id="80acc-128">Después de capturar una captura de pantalla, puede interactuar con ella de las siguientes maneras.</span><span class="sxs-lookup"><span data-stu-id="80acc-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="80acc-129">Desplace el puntero sobre una captura de pantalla para mostrar el punto en el que se capturó la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="80acc-129">Hover on a screenshot to display the point at which that screenshot was captured.</span></span>  <span data-ttu-id="80acc-130">Se muestra una línea amarilla en el panel de **información general** .</span><span class="sxs-lookup"><span data-stu-id="80acc-130">A yellow line is displayed on the **Overview** pane.</span></span>  
*   <span data-ttu-id="80acc-131">Elija la miniatura de una pantalla para filtrar las solicitudes que se produjeron después de que se capturó la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="80acc-131">Choose the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="80acc-132">Haga doble clic en una miniatura para acercarla.</span><span class="sxs-lookup"><span data-stu-id="80acc-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Desplazar el puntero sobre una captura de pantalla" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="80acc-134">Desplazar el puntero sobre una captura de pantalla</span><span class="sxs-lookup"><span data-stu-id="80acc-134">Hover on a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Choose Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Choose Replay XHR  
:::image-end:::  
-->  

## <span data-ttu-id="80acc-135">Cambiar el comportamiento de carga</span><span class="sxs-lookup"><span data-stu-id="80acc-135">Change loading behavior</span></span>  

### <span data-ttu-id="80acc-136">Emular a un primer visitante mediante la deshabilitación de la memoria caché del explorador</span><span class="sxs-lookup"><span data-stu-id="80acc-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="80acc-137">Para emular la experiencia de un usuario por primera vez en su sitio, active la casilla **deshabilitar caché** .</span><span class="sxs-lookup"><span data-stu-id="80acc-137">To emulate how a first-time user experiences your site, turn on the **Disable cache** checkbox.</span></span>  <span data-ttu-id="80acc-138">DevTools deshabilita la caché del explorador.</span><span class="sxs-lookup"><span data-stu-id="80acc-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="80acc-139">Esta característica emula con más precisión la experiencia de un usuario por primera vez, ya que las solicitudes se proporcionan desde la memoria caché del explorador al repetir visitas.</span><span class="sxs-lookup"><span data-stu-id="80acc-139">This feature more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Casilla deshabilitar caché" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="80acc-141">Casilla **deshabilitar caché**</span><span class="sxs-lookup"><span data-stu-id="80acc-141">The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <span data-ttu-id="80acc-142">Deshabilitar la memoria caché del explorador en el cajón de condiciones de red</span><span class="sxs-lookup"><span data-stu-id="80acc-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="80acc-143">Si desea deshabilitar la caché mientras trabaja en otros paneles de DevTools, use el cajón de condiciones de redes.</span><span class="sxs-lookup"><span data-stu-id="80acc-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="80acc-144">Abra el cajón de **condiciones de redes** .</span><span class="sxs-lookup"><span data-stu-id="80acc-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="80acc-145">Activa \ (o desactivada) la casilla **deshabilitar caché** .</span><span class="sxs-lookup"><span data-stu-id="80acc-145">Turn on \(or off\) the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="80acc-146">Borrar manualmente la memoria caché del explorador</span><span class="sxs-lookup"><span data-stu-id="80acc-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="80acc-147">Para borrar manualmente la memoria caché del explorador en cualquier momento, abra el menú contextual \ (haga clic con el botón secundario del mouse \) en cualquier lugar de la tabla solicitudes y seleccione **Borrar caché del explorador**.</span><span class="sxs-lookup"><span data-stu-id="80acc-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and choose **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Elija Borrar caché del explorador" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="80acc-149">Elija **Borrar caché del explorador**</span><span class="sxs-lookup"><span data-stu-id="80acc-149">Choose **Clear Browser Cache**</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-150">Emular sin conexión</span><span class="sxs-lookup"><span data-stu-id="80acc-150">Emulate offline</span></span>  

<span data-ttu-id="80acc-151">Una nueva clase de aplicaciones Web, denominada [aplicaciones web progresivas][DevtoolsProgressiveWebApps], funciona sin conexión con la ayuda de los **trabajadores de servicio**.</span><span class="sxs-lookup"><span data-stu-id="80acc-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="80acc-152">Es posible que le resulte útil simular rápidamente un dispositivo que no tiene conexión de datos cuando está creando este tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="80acc-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="80acc-153">Elija el menú desplegable **en línea** , buscar en **preestablecidos**y elija **sin conexión** para simular una experiencia de red sin conexión.</span><span class="sxs-lookup"><span data-stu-id="80acc-153">Choose the **Online** dropdown menu, search under **Presets**, and choose **Offline** to simulate an offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Menú desplegable desconectado" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="80acc-155">Menú desplegable **desconectado**</span><span class="sxs-lookup"><span data-stu-id="80acc-155">The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-156">Emular conexiones de red lentas</span><span class="sxs-lookup"><span data-stu-id="80acc-156">Emulate slow network connections</span></span>  

<span data-ttu-id="80acc-157">Emular 3G lento, 3G rápido y otras velocidades de conexión en el menú desplegable **en línea** .</span><span class="sxs-lookup"><span data-stu-id="80acc-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="El menú desplegable limitación de peticiones" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="80acc-159">El menú desplegable **limitación de peticiones**</span><span class="sxs-lookup"><span data-stu-id="80acc-159">The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="80acc-160">Puedes elegir entre diferentes ajustes preestablecidos, como 3G lento o 3G rápido.</span><span class="sxs-lookup"><span data-stu-id="80acc-160">You may choose from different presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="80acc-161">Para agregar sus propios ajustes preestablecidos personalizados, abra el menú de limitación y \*\*\*\* elija  >  **Agregar**personalizado.</span><span class="sxs-lookup"><span data-stu-id="80acc-161">To add your own custom presets, open the Throttling menu, and choose **Custom** > **Add**.</span></span>  

<span data-ttu-id="80acc-162">DevTools muestra un icono de advertencia junto a la pestaña **red** para recordarle que la limitación está habilitada.</span><span class="sxs-lookup"><span data-stu-id="80acc-162">DevTools displays a warning icon next to the **Network** tab to remind you that throttling is enabled.</span></span>  

#### <span data-ttu-id="80acc-163">Emular conexiones de red lentas del cajón de condiciones de red</span><span class="sxs-lookup"><span data-stu-id="80acc-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="80acc-164">Si desea limitar la conexión de red mientras trabaja en otros paneles de DevTools, use el cajón de condiciones de redes.</span><span class="sxs-lookup"><span data-stu-id="80acc-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="80acc-165">Abra el cajón de **condiciones de redes** .</span><span class="sxs-lookup"><span data-stu-id="80acc-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="80acc-166">Elija la velocidad de conexión en el menú **limitación** .</span><span class="sxs-lookup"><span data-stu-id="80acc-166">Choose your connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <span data-ttu-id="80acc-167">Borrar manualmente las cookies del explorador</span><span class="sxs-lookup"><span data-stu-id="80acc-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="80acc-168">Para borrar manualmente las cookies del explorador en cualquier momento, mantenga el mouse en cualquier lugar de la tabla solicitudes, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **Borrar cookies del explorador**.</span><span class="sxs-lookup"><span data-stu-id="80acc-168">To manually clear browser cookies at any time, hover anywhere in the Requests table, open the contextual menu \(right-click\), and choose **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Elija Borrar cookies del explorador" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="80acc-170">Elija **Borrar cookies del explorador**</span><span class="sxs-lookup"><span data-stu-id="80acc-170">Choose **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-171">Invalidar el agente de usuario</span><span class="sxs-lookup"><span data-stu-id="80acc-171">Override the user agent</span></span>  

<span data-ttu-id="80acc-172">Para anular manualmente el agente de usuario, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="80acc-172">To manually override the user agent, use the following steps.</span></span>  

1.  <span data-ttu-id="80acc-173">Abra el cajón de **condiciones de redes** .</span><span class="sxs-lookup"><span data-stu-id="80acc-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="80acc-174">Desactive la casilla **seleccionar automáticamente** .</span><span class="sxs-lookup"><span data-stu-id="80acc-174">Turn off the **Select automatically** checkbox.</span></span>  
1.  <span data-ttu-id="80acc-175">Elija una opción de agente de usuario en el menú o escriba una personalizada en el cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="80acc-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <span data-ttu-id="80acc-176">Filtrar solicitudes</span><span class="sxs-lookup"><span data-stu-id="80acc-176">Filter requests</span></span>  

### <span data-ttu-id="80acc-177">Filtrar las solicitudes por propiedades</span><span class="sxs-lookup"><span data-stu-id="80acc-177">Filter requests by properties</span></span>  

<span data-ttu-id="80acc-178">Use el cuadro de texto **filtrar** para filtrar las solicitudes por propiedades, como el dominio o el tamaño de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="80acc-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="80acc-179">Si no se muestra el cuadro de texto, es probable que el panel **filtros** esté oculto.</span><span class="sxs-lookup"><span data-stu-id="80acc-179">If the text box is not displayed, the **Filters** pane is probably hidden.</span></span>  
<span data-ttu-id="80acc-180">Para obtener más información, vaya a [ocultar el panel de filtros](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="80acc-180">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="El cuadro de texto filtro" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="80acc-182">El cuadro de texto **filtro**</span><span class="sxs-lookup"><span data-stu-id="80acc-182">The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="80acc-183">Puede usar varias propiedades simultáneamente al separar cada propiedad con un espacio.</span><span class="sxs-lookup"><span data-stu-id="80acc-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="80acc-184">Por ejemplo, `mime-type:image/png larger-than:1K` se muestran todos los PNGs que tengan más de 1 kilobyte.</span><span class="sxs-lookup"><span data-stu-id="80acc-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than 1 kilobyte.</span></span>  <span data-ttu-id="80acc-185">Los filtros de varias propiedades son equivalentes a `AND` las operaciones.</span><span class="sxs-lookup"><span data-stu-id="80acc-185">The multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="80acc-186">Actualmente no se admiten las operaciones.</span><span class="sxs-lookup"><span data-stu-id="80acc-186">operations are currently not supported.</span></span>  

<span data-ttu-id="80acc-187">La lista completa de propiedades compatibles.</span><span class="sxs-lookup"><span data-stu-id="80acc-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="80acc-188">Propiedad</span><span class="sxs-lookup"><span data-stu-id="80acc-188">Property</span></span> | <span data-ttu-id="80acc-189">Detalles</span><span class="sxs-lookup"><span data-stu-id="80acc-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="80acc-190">Mostrar solo los recursos del dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="80acc-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="80acc-191">Puede usar un carácter comodín \ ( `*` \) para incluir varios dominios.</span><span class="sxs-lookup"><span data-stu-id="80acc-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="80acc-192">Por ejemplo, `*.com` muestra los recursos de todos los nombres de dominio que terminan en `.com` .</span><span class="sxs-lookup"><span data-stu-id="80acc-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="80acc-193">DevTools rellenar el menú desplegable de autocompletar con todos los dominios que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="80acc-193">DevTools populate the autocomplete dropdown menu with all of the domains that are found.</span></span> |  
| `has-response-header` | <span data-ttu-id="80acc-194">Muestra los recursos que contienen el encabezado de respuesta HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="80acc-194">Displays the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="80acc-195">DevTools rellenar la lista desplegable de autocompletar con todos los encabezados de respuesta que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="80acc-195">DevTools populate the autocomplete dropdown with all of the response headers that are found.</span></span> |  
| `is` | <span data-ttu-id="80acc-196">Usar `is:running` para buscar `WebSocket` recursos.</span><span class="sxs-lookup"><span data-stu-id="80acc-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="80acc-197">Muestra los recursos que son mayores que el tamaño especificado, en bytes.</span><span class="sxs-lookup"><span data-stu-id="80acc-197">Displays resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="80acc-198">Establecer un valor de `1000` es equivalente a establecer un valor de `1k` .</span><span class="sxs-lookup"><span data-stu-id="80acc-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="80acc-199">Muestra los recursos que se recuperaron en un tipo de método HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="80acc-199">Displays resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="80acc-200">DevTools rellenar la lista desplegable con todos los métodos HTTP que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="80acc-200">DevTools populate the dropdown with all of the HTTP methods  that are found.</span></span> |  
| `mime-type` | <span data-ttu-id="80acc-201">Muestra los recursos de un tipo MIME especificado.</span><span class="sxs-lookup"><span data-stu-id="80acc-201">Displays resources of a specified MIME type.</span></span>  <span data-ttu-id="80acc-202">DevTools rellenar la lista desplegable con todos los tipos MIME que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="80acc-202">DevTools populate the dropdown with all MIME types  that are found.</span></span> |  
| `mixed-content` | <span data-ttu-id="80acc-203">Mostrar todos los recursos de contenido mixto \ ( `mixed-content:all` \) o solo los que se muestran actualmente \ ( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="80acc-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="80acc-204">Muestra los recursos recuperados en HTTP \ ( `scheme:http` \) no protegidos o en https \ ( `scheme:https` \).</span><span class="sxs-lookup"><span data-stu-id="80acc-204">Displays resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="80acc-205">Muestra los recursos que tienen un `Set-Cookie` encabezado con un `Domain` atributo que coincide con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="80acc-205">Displays resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="80acc-206">DevTools rellenar autocompletar con todos los dominios de cookies que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="80acc-206">DevTools populate the autocomplete with all of the cookie domains that are found.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="80acc-207">Muestra los recursos que tienen un `Set-Cookie` encabezado con un nombre que coincide con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="80acc-207">Displays resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="80acc-208">DevTools rellenar autocompletar con todos los nombres de cookies que se encuentren.</span><span class="sxs-lookup"><span data-stu-id="80acc-208">DevTools populate the autocomplete with all of the cookie names that are found.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="80acc-209">Muestra los recursos que tienen un `Set-Cookie` encabezado con un valor que coincide con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="80acc-209">Displays resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="80acc-210">DevTools rellenar autocompletar con todos los valores de las cookies que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="80acc-210">DevTools populate the autocomplete with all of the cookie values that are found.</span></span> |  
| `status-code` | <span data-ttu-id="80acc-211">Muestra los recursos que coinciden con el código de Estado HTTP específico.</span><span class="sxs-lookup"><span data-stu-id="80acc-211">Displays resources that match the specific HTTP status code.</span></span>  <span data-ttu-id="80acc-212">DevTools rellena el menú desplegable de autocompletar con todos los códigos de estado que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="80acc-212">DevTools populates the autocomplete dropdown menu with all of the status codes that are found.</span></span> |  

### <span data-ttu-id="80acc-213">Filtrar solicitudes por tipo</span><span class="sxs-lookup"><span data-stu-id="80acc-213">Filter requests by type</span></span>  

<span data-ttu-id="80acc-214">Para filtrar las solicitudes por tipo de solicitud, elija uno de los siguientes botones en el panel **red** .</span><span class="sxs-lookup"><span data-stu-id="80acc-214">To filter requests by request type, choose the one of the following buttons on the **Network** panel.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-215">XHR</span><span class="sxs-lookup"><span data-stu-id="80acc-215">XHR</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-216">JS</span><span class="sxs-lookup"><span data-stu-id="80acc-216">JS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-217">CSS</span><span class="sxs-lookup"><span data-stu-id="80acc-217">CSS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-218">IMG</span><span class="sxs-lookup"><span data-stu-id="80acc-218">Img</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-219">Multimedia</span><span class="sxs-lookup"><span data-stu-id="80acc-219">Media</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-220">Fuente</span><span class="sxs-lookup"><span data-stu-id="80acc-220">Font</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-221">Dividir</span><span class="sxs-lookup"><span data-stu-id="80acc-221">Doc</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-222">EB</span><span class="sxs-lookup"><span data-stu-id="80acc-222">WS</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-223">WebSocket.</span><span class="sxs-lookup"><span data-stu-id="80acc-223">WebSocket.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-224">Manifiesta</span><span class="sxs-lookup"><span data-stu-id="80acc-224">Manifest</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-225">Otros</span><span class="sxs-lookup"><span data-stu-id="80acc-225">Other</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-226">Cualquier otro tipo no incluido en la lista.</span><span class="sxs-lookup"><span data-stu-id="80acc-226">Any other type not listed.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="80acc-227">Si los botones no se muestran, es posible que el panel **filtros** esté oculto.</span><span class="sxs-lookup"><span data-stu-id="80acc-227">If the buttons do not display, the **Filters** pane may be hidden.</span></span>  
<span data-ttu-id="80acc-228">Para obtener más información, vaya a [ocultar el panel de filtros](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="80acc-228">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="80acc-229">Para habilitar varios filtros de tipo simultáneamente, mantenga `Control` \ (Windows, Linux \) o `Command` \ (MacOS \) y, a continuación, elija.</span><span class="sxs-lookup"><span data-stu-id="80acc-229">To enable multiple type filters simultaneously, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Usar los filtros de tipo para mostrar los recursos JS, CSS y Document" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="80acc-231">Usar los filtros de tipo para mostrar los recursos JS, CSS y Document</span><span class="sxs-lookup"><span data-stu-id="80acc-231">Use the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-232">Filtrar solicitudes por tiempo</span><span class="sxs-lookup"><span data-stu-id="80acc-232">Filter requests by time</span></span>  

<span data-ttu-id="80acc-233">Elige y arrastra a la izquierda o a la derecha en el panel de **Descripción** para mostrar solo las solicitudes que estaban activas durante ese período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="80acc-233">Choose and drag left or right on the **Overview** pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="80acc-234">El filtro es inclusivo.</span><span class="sxs-lookup"><span data-stu-id="80acc-234">The filter is inclusive.</span></span>  <span data-ttu-id="80acc-235">Se muestra cualquier solicitud que estuviera activa durante la hora resaltada.</span><span class="sxs-lookup"><span data-stu-id="80acc-235">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Filtrar las solicitudes que hayan estado inactivas aproximadamente 300 ms" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="80acc-237">Filtrar las solicitudes que hayan estado inactivas aproximadamente 300 ms</span><span class="sxs-lookup"><span data-stu-id="80acc-237">Filter out any requests that were inactive around 300 ms</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-238">Ocultar direcciones URL de datos</span><span class="sxs-lookup"><span data-stu-id="80acc-238">Hide data URLs</span></span>  

<span data-ttu-id="80acc-239">Las [direcciones URL de datos][MDNHTTPDataURIs] son pequeños archivos incrustados en otros documentos.</span><span class="sxs-lookup"><span data-stu-id="80acc-239">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="80acc-240">Cualquier solicitud que se muestre en la tabla solicitudes que comienza por `data:` es una dirección URL de datos.</span><span class="sxs-lookup"><span data-stu-id="80acc-240">Any request that displays in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="80acc-241">Para ocultar las solicitudes, desactive la casilla **ocultar URL de datos** .</span><span class="sxs-lookup"><span data-stu-id="80acc-241">To hide the requests, turn off the **Hide data URLs** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="La casilla ocultar direcciones URL de datos" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="80acc-243">La casilla **ocultar direcciones URL de datos**</span><span class="sxs-lookup"><span data-stu-id="80acc-243">The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="80acc-244">Ordenar solicitudes</span><span class="sxs-lookup"><span data-stu-id="80acc-244">Sort requests</span></span>  

<span data-ttu-id="80acc-245">De forma predeterminada, las solicitudes de la tabla solicitudes se ordenan por hora de inicio, pero puede ordenar la tabla mediante otros criterios.</span><span class="sxs-lookup"><span data-stu-id="80acc-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <span data-ttu-id="80acc-246">Ordenar por columna</span><span class="sxs-lookup"><span data-stu-id="80acc-246">Sort by column</span></span>  

<span data-ttu-id="80acc-247">Elija el encabezado de cualquier columna en las solicitudes de ordenación de solicitudes de esa columna.</span><span class="sxs-lookup"><span data-stu-id="80acc-247">Choose the header of any column in the Requests to sort requests by that column.</span></span>  

### <span data-ttu-id="80acc-248">Ordenar por fase de actividad</span><span class="sxs-lookup"><span data-stu-id="80acc-248">Sort by activity phase</span></span>  

<span data-ttu-id="80acc-249">Para cambiar la forma en que la cascada ordena las solicitudes, desplace el puntero sobre el encabezado de la tabla solicitudes, abra el menú contextual \ (haga clic con el botón derecho \), desplace el puntero en **cascada**y elija una de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="80acc-249">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover on **Waterfall**, and choose one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-250">Hora de inicio</span><span class="sxs-lookup"><span data-stu-id="80acc-250">Start Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-251">La primera solicitud iniciada se encuentra en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="80acc-251">The first request that was initiated is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-252">Tiempo de respuesta</span><span class="sxs-lookup"><span data-stu-id="80acc-252">Response Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-253">La primera solicitud que comenzó a descargarse está en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="80acc-253">The first request that started downloading is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-254">Hora de finalización</span><span class="sxs-lookup"><span data-stu-id="80acc-254">End Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-255">La primera solicitud que ha finalizado se encuentra en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="80acc-255">The first request that finished is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-256">Duración total</span><span class="sxs-lookup"><span data-stu-id="80acc-256">Total Duration</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-257">La solicitud con la configuración de conexión más corta, solicitud o respuesta, se encuentra en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="80acc-257">The request with the shortest connection settings and request or response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-258">Latencia</span><span class="sxs-lookup"><span data-stu-id="80acc-258">Latency</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-259">La solicitud que esperó el tiempo más breve para una respuesta está en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="80acc-259">The request that waited the shortest time for a response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="80acc-260">En estas descripciones se supone que cada opción respectiva está clasificada de menor a mayor.</span><span class="sxs-lookup"><span data-stu-id="80acc-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="80acc-261">Elija el encabezado de la columna **cascada** para invertir el orden.</span><span class="sxs-lookup"><span data-stu-id="80acc-261">Choose the header of the **Waterfall** column to reverse the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Ordenar la cascada por duración total" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="80acc-263">Ordenar la cascada por duración total \ (la parte más clara de cada barra está en espera y la parte más oscura es el tiempo dedicado a descargar bytes \)</span><span class="sxs-lookup"><span data-stu-id="80acc-263">Sort the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <span data-ttu-id="80acc-264">Analizar solicitudes</span><span class="sxs-lookup"><span data-stu-id="80acc-264">Analyze requests</span></span>  

<span data-ttu-id="80acc-265">Siempre que DevTools estén abiertos, registra todas las solicitudes en el panel **red** .</span><span class="sxs-lookup"><span data-stu-id="80acc-265">So long as DevTools are open, it logs all requests in the **Network** panel.</span></span>  
<span data-ttu-id="80acc-266">Use el panel red para analizar las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80acc-266">Use the Network panel to analyze requests.</span></span>  

### <span data-ttu-id="80acc-267">Mostrar un registro de solicitudes</span><span class="sxs-lookup"><span data-stu-id="80acc-267">Display a log of requests</span></span>  

<span data-ttu-id="80acc-268">Use la tabla solicitudes para mostrar un registro de todas las solicitudes realizadas mientras DevTools abierto.</span><span class="sxs-lookup"><span data-stu-id="80acc-268">Use the Requests table to display a log of all requests made while DevTools have been open.</span></span>  <span data-ttu-id="80acc-269">Para obtener más información sobre cada elemento, elige o mantiene el mouse en las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80acc-269">To reveals more information about each item, choose or hover on requests.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="La tabla solicitudes" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="80acc-271">La tabla solicitudes</span><span class="sxs-lookup"><span data-stu-id="80acc-271">The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="80acc-272">De forma predeterminada, en la tabla solicitudes se muestran las siguientes columnas.</span><span class="sxs-lookup"><span data-stu-id="80acc-272">The Requests table displays the following columns by default.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-273">Nombre</span><span class="sxs-lookup"><span data-stu-id="80acc-273">Name</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-274">El nombre de archivo de un recurso o un identificador de él.</span><span class="sxs-lookup"><span data-stu-id="80acc-274">The filename of, or an identifier for, the resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-275">Estado</span><span class="sxs-lookup"><span data-stu-id="80acc-275">Status</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-276">El código de Estado HTTP.</span><span class="sxs-lookup"><span data-stu-id="80acc-276">The HTTP status code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-277">Tipo</span><span class="sxs-lookup"><span data-stu-id="80acc-277">Type</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-278">Tipo MIME del recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="80acc-278">The MIME type of the requested resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-279">Inició</span><span class="sxs-lookup"><span data-stu-id="80acc-279">Initiator</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-280">Los siguientes objetos o procesos inician solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80acc-280">The following objects or processes initiate requests.</span></span>  
      
      *   <span data-ttu-id="80acc-281">**Analizador**  El analizador HTML para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="80acc-281">**Parser**  The HTML parser for Microsoft Edge.</span></span>  
      *   <span data-ttu-id="80acc-282">**Redirigir**  Una redirección de HTTP.</span><span class="sxs-lookup"><span data-stu-id="80acc-282">**Redirect**  An HTTP redirect.</span></span>  
      *   <span data-ttu-id="80acc-283">**Script**  Una función de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="80acc-283">**Script**  A JavaScript function.</span></span>  
      *   <span data-ttu-id="80acc-284">**Otros**  Otro proceso o acción, como navegar a una página con un vínculo o escribir una dirección URL en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="80acc-284">**Other**  Some other process or action, such as navigating to a page using a link or entering a URL in the address bar.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-285">Tamaño</span><span class="sxs-lookup"><span data-stu-id="80acc-285">Size</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-286">El tamaño combinado de los encabezados de respuesta más el cuerpo de la respuesta, tal y como lo proporciona el servidor.</span><span class="sxs-lookup"><span data-stu-id="80acc-286">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-287">Tiempo</span><span class="sxs-lookup"><span data-stu-id="80acc-287">Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-288">La duración total, desde el inicio de la solicitud hasta la recepción del byte final en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="80acc-288">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="80acc-289">Cascada</span><span class="sxs-lookup"><span data-stu-id="80acc-289">Waterfall</span></span>](#display-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-290">Un desglose visual de la actividad de cada solicitud.</span><span class="sxs-lookup"><span data-stu-id="80acc-290">A visual breakdown of the activity for each request.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="80acc-291">Agregar o quitar columnas</span><span class="sxs-lookup"><span data-stu-id="80acc-291">Add or remove columns</span></span>  

<span data-ttu-id="80acc-292">Desplace el puntero en el encabezado de la tabla solicitudes, abra el menú contextual \ (haga clic con el botón derecho \) y elija una opción para ocultarlo o mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="80acc-292">Hover on the header of the Requests table, open the contextual menu \(right-click\), and choose an option to hide or show it.</span></span>  <span data-ttu-id="80acc-293">Las opciones mostradas actualmente tienen marcas de verificación junto a cada elemento.</span><span class="sxs-lookup"><span data-stu-id="80acc-293">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Agregar una columna a la tabla solicitudes" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="80acc-295">Agregar una columna a la tabla solicitudes</span><span class="sxs-lookup"><span data-stu-id="80acc-295">Add a column to the Requests table</span></span>  
:::image-end:::  

#### <span data-ttu-id="80acc-296">Agregar columnas personalizadas</span><span class="sxs-lookup"><span data-stu-id="80acc-296">Add custom columns</span></span>  

<span data-ttu-id="80acc-297">Para agregar una columna personalizada a la tabla solicitudes, desplace el puntero sobre el encabezado de la tabla solicitudes, abra el menú contextual \ (haga clic con el botón derecho \) y elija **encabezados de respuesta**para  >  **administrar columnas de encabezado**.</span><span class="sxs-lookup"><span data-stu-id="80acc-297">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and choose **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Agregar una columna personalizada a la tabla solicitudes" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="80acc-299">Agregar una columna personalizada a la tabla solicitudes</span><span class="sxs-lookup"><span data-stu-id="80acc-299">Add a custom column to the Requests table</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-300">Mostrar la relación de sincronización de las solicitudes</span><span class="sxs-lookup"><span data-stu-id="80acc-300">Display the timing relationship of requests</span></span>  

<span data-ttu-id="80acc-301">Use la cascada para mostrar las relaciones de temporización de las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80acc-301">Use the Waterfall to display the timing relationships of requests.</span></span>  
<span data-ttu-id="80acc-302">La organización predeterminada de la cascada usa la hora de inicio de las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80acc-302">The default organization of the Waterfall uses the start time of the requests.</span></span>  
<span data-ttu-id="80acc-303">Por lo tanto, las solicitudes que se encuentren más lejanas a la izquierda iniciadas antes que las solicitudes más lejanas a la derecha.</span><span class="sxs-lookup"><span data-stu-id="80acc-303">So, requests that are farther to the left started earlier than the requests that are farther to the right.</span></span>  

<span data-ttu-id="80acc-304">Para revisar las diferentes maneras en las que puede ordenar la cascada, vaya a [ordenar por fase de actividad](#sort-by-activity-phase).</span><span class="sxs-lookup"><span data-stu-id="80acc-304">To review the different ways that you may sort the Waterfall, navigate to [Sort by activity phase](#sort-by-activity-phase).</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="La columna cascada del panel solicitudes" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="80acc-306">La columna cascada del panel **solicitudes**</span><span class="sxs-lookup"><span data-stu-id="80acc-306">The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To review the frames of a WebSocket connection, use the following steps.  

1.  Choose the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Choose the **Frames** tab.  The table shows the last 100 frames.  

To refresh the table, re-choose the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames tab" lightbox="../media/network-frames.msft.png":::
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

### <span data-ttu-id="80acc-307">Mostrar una vista previa del cuerpo de una respuesta</span><span class="sxs-lookup"><span data-stu-id="80acc-307">Display a preview of a response body</span></span>  

<span data-ttu-id="80acc-308">Para mostrar una vista previa del cuerpo de una respuesta, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="80acc-308">To display a preview of a response body, use the following steps.</span></span>  

1.  <span data-ttu-id="80acc-309">Elija la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80acc-309">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="80acc-310">Elija la pestaña **vista previa** .</span><span class="sxs-lookup"><span data-stu-id="80acc-310">Choose the **Preview** tab.</span></span>  

<span data-ttu-id="80acc-311">La ficha vista previa es principalmente útil para mostrar imágenes.</span><span class="sxs-lookup"><span data-stu-id="80acc-311">The Preview tab is mostly useful to display images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="La ficha vista previa" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="80acc-313">La ficha **vista previa**</span><span class="sxs-lookup"><span data-stu-id="80acc-313">The **Preview** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-314">Mostrar cuerpo de respuesta</span><span class="sxs-lookup"><span data-stu-id="80acc-314">Display a response body</span></span>  

<span data-ttu-id="80acc-315">Para mostrar el cuerpo de la respuesta a una solicitud, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="80acc-315">To display the response body to a request, use the following steps.</span></span>  

1.  <span data-ttu-id="80acc-316">Elija la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80acc-316">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="80acc-317">Elija la pestaña **respuesta** .</span><span class="sxs-lookup"><span data-stu-id="80acc-317">Choose the **Response** tab.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="La ficha respuesta" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="80acc-319">La ficha **respuesta**</span><span class="sxs-lookup"><span data-stu-id="80acc-319">The **Response** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-320">Mostrar encabezados HTTP</span><span class="sxs-lookup"><span data-stu-id="80acc-320">Display HTTP headers</span></span>  

<span data-ttu-id="80acc-321">Para mostrar los datos del encabezado HTTP sobre una solicitud, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="80acc-321">To display HTTP header data about a request, use the following steps.</span></span>  

1.  <span data-ttu-id="80acc-322">Elija la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80acc-322">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="80acc-323">Elija la pestaña **encabezados** .</span><span class="sxs-lookup"><span data-stu-id="80acc-323">Choose the **Headers** tab.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="La pestaña encabezados" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="80acc-325">La pestaña **encabezados**</span><span class="sxs-lookup"><span data-stu-id="80acc-325">The **Headers** tab</span></span>  
:::image-end:::  

#### <span data-ttu-id="80acc-326">Mostrar el origen del encabezado HTTP</span><span class="sxs-lookup"><span data-stu-id="80acc-326">Display HTTP header source</span></span>  

<span data-ttu-id="80acc-327">De forma predeterminada, la pestaña encabezados muestra los nombres de encabezado alfabéticamente.</span><span class="sxs-lookup"><span data-stu-id="80acc-327">By default, the Headers tab shows header names alphabetically.</span></span>  <span data-ttu-id="80acc-328">Para deshabilitada los nombres de encabezado HTTP en el orden recibido, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="80acc-328">To dsiplay the HTTP header names in the order received, use the following steps.</span></span>  

1.  <span data-ttu-id="80acc-329">Abre la pestaña **encabezados** para la solicitud que te interese.</span><span class="sxs-lookup"><span data-stu-id="80acc-329">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="80acc-330">Para obtener más información, vaya a [Mostrar encabezados HTTP](#display-http-headers).</span><span class="sxs-lookup"><span data-stu-id="80acc-330">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="80acc-331">Elija **Ver origen**, junto a la sección **solicitar encabezado** o **respuesta de encabezado** .</span><span class="sxs-lookup"><span data-stu-id="80acc-331">Choose **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <span data-ttu-id="80acc-332">Mostrar parámetros de cadena de consulta</span><span class="sxs-lookup"><span data-stu-id="80acc-332">Display query string parameters</span></span>  

<span data-ttu-id="80acc-333">Para mostrar los parámetros de cadena de consulta de una dirección URL en un formato legible, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="80acc-333">To display the query string parameters of a URL in a human-readable format, use the following steps.</span></span>  

1.  <span data-ttu-id="80acc-334">Abre la pestaña **encabezados** para la solicitud que te interese.</span><span class="sxs-lookup"><span data-stu-id="80acc-334">Open the **Headers** tab for the request that interests you.</span></span>  <span data-ttu-id="80acc-335">Para obtener más información, vaya a [Mostrar encabezados HTTP](#display-http-headers).</span><span class="sxs-lookup"><span data-stu-id="80acc-335">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="80acc-336">Vaya a la sección **parámetros de cadena de consulta** .</span><span class="sxs-lookup"><span data-stu-id="80acc-336">Go to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Sección parámetros de cadena de consulta" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="80acc-338">Sección **parámetros de cadena de consulta**</span><span class="sxs-lookup"><span data-stu-id="80acc-338">The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <span data-ttu-id="80acc-339">Mostrar parámetros de cadena de consulta origen</span><span class="sxs-lookup"><span data-stu-id="80acc-339">Display query string parameters source</span></span>  

<span data-ttu-id="80acc-340">Para mostrar el origen de parámetro de cadena de consulta de una solicitud, realice los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="80acc-340">To display the query string parameter source of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="80acc-341">Vaya a la sección parámetros de cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="80acc-341">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="80acc-342">Para obtener más información, vaya a [Mostrar parámetros de cadena de consulta](#display-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="80acc-342">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="80acc-343">Elija **Ver origen**.</span><span class="sxs-lookup"><span data-stu-id="80acc-343">Choose **view source**.</span></span>  

#### <span data-ttu-id="80acc-344">Mostrar parámetros de cadena de consulta codificados por URL</span><span class="sxs-lookup"><span data-stu-id="80acc-344">Display URL-encoded query string parameters</span></span>  

<span data-ttu-id="80acc-345">Para mostrar parámetros de cadena de consulta en un formato legible, pero con las codificaciones conservadas, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="80acc-345">To display query string parameters in a human-readable format, but with encodings preserved, use the following steps.</span></span>  

1.  <span data-ttu-id="80acc-346">Vaya a la sección parámetros de cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="80acc-346">Go to the Query String Parameters section.</span></span>  <span data-ttu-id="80acc-347">Para obtener más información, vaya a [Mostrar parámetros de cadena de consulta](#display-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="80acc-347">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="80acc-348">Elija **Ver dirección URL codificada**.</span><span class="sxs-lookup"><span data-stu-id="80acc-348">Choose **view URL encoded**.</span></span>  

### <span data-ttu-id="80acc-349">Mostrar cookies</span><span class="sxs-lookup"><span data-stu-id="80acc-349">Display cookies</span></span>  

<span data-ttu-id="80acc-350">Para mostrar las cookies enviadas en el encabezado HTTP de una solicitud, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="80acc-350">To display the cookies sent in the HTTP header of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="80acc-351">Elija la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80acc-351">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="80acc-352">Elija la pestaña **cookies** .</span><span class="sxs-lookup"><span data-stu-id="80acc-352">Choose the **Cookies** tab.</span></span>  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="La ficha cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="80acc-354">La ficha cookies</span><span class="sxs-lookup"><span data-stu-id="80acc-354">The Cookies tab</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-355">Mostrar el desglose de intervalos de una solicitud</span><span class="sxs-lookup"><span data-stu-id="80acc-355">Display the timing breakdown of a request</span></span>  

<span data-ttu-id="80acc-356">Para mostrar el desglose de intervalos de una solicitud, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="80acc-356">To display the timing breakdown of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="80acc-357">Elija la dirección URL de la solicitud en la columna **nombre** de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80acc-357">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="80acc-358">Elija la pestaña **intervalos** .</span><span class="sxs-lookup"><span data-stu-id="80acc-358">Choose the **Timing** tab.</span></span>  

<span data-ttu-id="80acc-359">Para obtener acceso a los datos de una manera más rápida, navegue para [obtener una vista previa de un desglose por intervalos](#preview-a-timing-breakdown).</span><span class="sxs-lookup"><span data-stu-id="80acc-359">For a faster way to access the data, navigate to [Preview a timing breakdown](#preview-a-timing-breakdown).</span></span>  

<span data-ttu-id="80acc-360">Para obtener más información acerca de cada una de las fases que se pueden mostrar en la pestaña **intervalos** , vaya a [fases de desglose por intervalos explicadas](#timing-breakdown-phases-explained).</span><span class="sxs-lookup"><span data-stu-id="80acc-360">For more information about each of the phases that may be displayed in the **Timing** tab, navigate to [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="La ficha intervalos" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="80acc-362">La ficha **intervalos**</span><span class="sxs-lookup"><span data-stu-id="80acc-362">The **Timing** tab</span></span>  
:::image-end:::  

<span data-ttu-id="80acc-363">Más información sobre cada una de las fases.</span><span class="sxs-lookup"><span data-stu-id="80acc-363">More information about each of the phases.</span></span>  

<span data-ttu-id="80acc-364">Para obtener más información sobre cómo obtener acceso a la pantalla, vaya a [Mostrar desglose de intervalos](#display-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="80acc-364">For more information about accessing the display, navigate to [Display timing breakdown](#display-the-timing-breakdown-of-a-request).</span></span>  

#### <span data-ttu-id="80acc-365">Obtener una vista previa de intervalos</span><span class="sxs-lookup"><span data-stu-id="80acc-365">Preview a timing breakdown</span></span>  

<span data-ttu-id="80acc-366">Para mostrar una vista previa del desglose de intervalos de una solicitud, en la columna **cascada** de la tabla solicitudes, desplace el puntero sobre la entrada de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="80acc-366">To display a preview of the timing breakdown of a request, in the **Waterfall** column of the Requests table, hover on the entry for the request.</span></span>  

<span data-ttu-id="80acc-367">Para obtener más información sobre cómo obtener acceso a los datos sin mantener el mouse, navegue para [Mostrar el desglose de intervalos de una solicitud](#display-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="80acc-367">For more information about how to access the data without hovering, navigate to [Display the timing breakdown of a request](#display-the-timing-breakdown-of-a-request).</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> obtener una vista previa del desglose de intervalos de una solicitud" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="80acc-369">Obtener una vista previa del desglose de intervalos de una solicitud</span><span class="sxs-lookup"><span data-stu-id="80acc-369">Preview the timing breakdown of a request</span></span>  
:::image-end:::  

#### <span data-ttu-id="80acc-370">Explicación de fases de desglose de intervalos</span><span class="sxs-lookup"><span data-stu-id="80acc-370">Timing breakdown phases explained</span></span>  

<span data-ttu-id="80acc-371">Más información sobre cada una de las fases que pueden mostrarse en la pestaña **intervalos** .</span><span class="sxs-lookup"><span data-stu-id="80acc-371">More information about each of the phases that may display in the **Timing** tab.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-372">Poner en cola</span><span class="sxs-lookup"><span data-stu-id="80acc-372">Queueing</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-373">El explorador pone en cola las solicitudes cuando cualquiera de las siguientes condiciones es verdadera.</span><span class="sxs-lookup"><span data-stu-id="80acc-373">The browser queues requests when any of the following are true.</span></span>  
      
      *   <span data-ttu-id="80acc-374">Hay solicitudes de prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="80acc-374">Higher priority requests exist.</span></span>  
      *   <span data-ttu-id="80acc-375">Hay seis conexiones TCP abiertas para el mismo origen, que es el límite.</span><span class="sxs-lookup"><span data-stu-id="80acc-375">Six TCP connections are open for the same origin, which is the limit.</span></span>  <span data-ttu-id="80acc-376">Solo se aplica a HTTP/1.0 y HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="80acc-376">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
      *   <span data-ttu-id="80acc-377">El explorador está asignando un poco de espacio en la caché de disco.</span><span class="sxs-lookup"><span data-stu-id="80acc-377">The browser is briefly allocating space in the disk cache.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-378">Paralizado</span><span class="sxs-lookup"><span data-stu-id="80acc-378">Stalled</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-379">La solicitud se detiene por cualquiera de las razones descritas en **puesta en cola**.</span><span class="sxs-lookup"><span data-stu-id="80acc-379">The request is stalled for any of the reasons described in **Queueing**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-380">Búsqueda de DNS</span><span class="sxs-lookup"><span data-stu-id="80acc-380">DNS Lookup</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-381">El explorador está resolviendo la dirección IP de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="80acc-381">The browser is resolving the IP address for the request.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-382">Conexión inicial</span><span class="sxs-lookup"><span data-stu-id="80acc-382">Initial connection</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-383">El explorador establece una conexión que incluye los protocolos de enlace TCP, los reintentos de TCP y negocia una capa de sockets seguros.</span><span class="sxs-lookup"><span data-stu-id="80acc-383">The browser establishes a connection including TCP handshakes, TCP retries, and negotiates a Secure Socket Layer.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-384">Negociación de proxy</span><span class="sxs-lookup"><span data-stu-id="80acc-384">Proxy negotiation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-385">El explorador está negociando la solicitud con un [servidor proxy][WikiProxyServer].</span><span class="sxs-lookup"><span data-stu-id="80acc-385">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-386">Solicitud enviada</span><span class="sxs-lookup"><span data-stu-id="80acc-386">Request sent</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-387">Se está enviando la solicitud.</span><span class="sxs-lookup"><span data-stu-id="80acc-387">The request is being sent.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-388">Preparación de ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="80acc-388">ServiceWorker Preparation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-389">El explorador está iniciando el trabajo del servicio.</span><span class="sxs-lookup"><span data-stu-id="80acc-389">The browser is starting the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-390">Solicitud para ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="80acc-390">Request to ServiceWorker</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-391">La solicitud se está enviando al trabajador del servicio.</span><span class="sxs-lookup"><span data-stu-id="80acc-391">The request is being sent to the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-392">Esperando \ (TTFB \)</span><span class="sxs-lookup"><span data-stu-id="80acc-392">Waiting \(TTFB\)</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-393">El explorador está esperando el primer byte de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="80acc-393">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="80acc-394">TTFB es el primer byte.</span><span class="sxs-lookup"><span data-stu-id="80acc-394">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="80acc-395">Este intervalo incluye un recorrido de ida y vuelta de la latencia y el tiempo que el servidor tomó para preparar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="80acc-395">This timing includes one round trip of latency and the time the server took to prepare the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-396">Descarga de contenido</span><span class="sxs-lookup"><span data-stu-id="80acc-396">Content Download</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-397">El explorador está recibiendo la respuesta.</span><span class="sxs-lookup"><span data-stu-id="80acc-397">The browser is receiving the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-398">Recepción de envío</span><span class="sxs-lookup"><span data-stu-id="80acc-398">Receiving Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-399">El explorador está recibiendo datos de esta respuesta a través de la inserción de servidor HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="80acc-399">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="80acc-400">Insertar inserción</span><span class="sxs-lookup"><span data-stu-id="80acc-400">Reading Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="80acc-401">El explorador está leyendo los datos locales recibidos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="80acc-401">The browser is reading the local data previously received.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="80acc-402">Mostrar iniciadores y dependencias</span><span class="sxs-lookup"><span data-stu-id="80acc-402">Display initiators and dependencies</span></span>  

<span data-ttu-id="80acc-403">Para mostrar los iniciadores y las dependencias de una solicitud, mantenga presionado el `Shift` puntero en la solicitud de la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80acc-403">To display the initiators and dependencies of a request, hold `Shift`and hover on the request in the Requests table.</span></span>  <span data-ttu-id="80acc-404">Colores de DevTools: los iniciadores se muestran en verde y las dependencias en rojo.</span><span class="sxs-lookup"><span data-stu-id="80acc-404">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Mostrar los iniciadores y las dependencias de una solicitud" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="80acc-406">Mostrar los iniciadores y las dependencias de una solicitud</span><span class="sxs-lookup"><span data-stu-id="80acc-406">Display the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="80acc-407">Cuando la tabla solicitudes está ordenada cronológicamente, si coloca el puntero sobre una línea, la línea anterior muestra una solicitud verde.</span><span class="sxs-lookup"><span data-stu-id="80acc-407">When the Requests table is ordered chronologically, if you hover on a line, the line preceding it displays a green request.</span></span>  <span data-ttu-id="80acc-408">La solicitud verde es el iniciador de la dependencia.</span><span class="sxs-lookup"><span data-stu-id="80acc-408">The green request is the initiator of the dependency.</span></span>  <span data-ttu-id="80acc-409">Si se muestra otra solicitud verde en la línea antes de ella, esa solicitud superior es el iniciador del iniciador.</span><span class="sxs-lookup"><span data-stu-id="80acc-409">If another green request is displayed on the line before that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="80acc-410">Etcétera.</span><span class="sxs-lookup"><span data-stu-id="80acc-410">And so on.</span></span>  

### <span data-ttu-id="80acc-411">Mostrar eventos de carga</span><span class="sxs-lookup"><span data-stu-id="80acc-411">Display load events</span></span>  

<span data-ttu-id="80acc-412">DevTools muestra la temporización de los `DOMContentLoaded` `load` eventos y en varios lugares del panel **red** .</span><span class="sxs-lookup"><span data-stu-id="80acc-412">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the **Network** panel.</span></span>  <span data-ttu-id="80acc-413">El `DOMContentLoaded` evento está coloreado en azul y el `load` evento es rojo.</span><span class="sxs-lookup"><span data-stu-id="80acc-413">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Las ubicaciones de la DOMContentLoaded y cargar eventos en el panel red" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="80acc-415">Las ubicaciones de los `DOMContentLoaded` `load` eventos y en el panel **red**</span><span class="sxs-lookup"><span data-stu-id="80acc-415">The locations of the `DOMContentLoaded` and `load` events on the **Network** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-416">Mostrar el número total de solicitudes</span><span class="sxs-lookup"><span data-stu-id="80acc-416">Display the total number of requests</span></span>  

<span data-ttu-id="80acc-417">El número total de solicitudes se muestra en el panel **Resumen** , en la parte inferior del panel **red** .</span><span class="sxs-lookup"><span data-stu-id="80acc-417">The total number of requests is listed in the **Summary** pane, at the bottom of the **Network** panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="80acc-418">Este número solo realiza un seguimiento de las solicitudes que se han registrado desde que se abrió DevTools.</span><span class="sxs-lookup"><span data-stu-id="80acc-418">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="80acc-419">Si se han producido otras solicitudes antes de que se abriera DevTools, esas solicitudes no se cuentan.</span><span class="sxs-lookup"><span data-stu-id="80acc-419">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="El número total de solicitudes desde que DevTools se abrieron" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="80acc-421">El número total de solicitudes desde que DevTools se abrieron</span><span class="sxs-lookup"><span data-stu-id="80acc-421">The total number of requests since DevTools were opened</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-422">Mostrar el tamaño total de descarga</span><span class="sxs-lookup"><span data-stu-id="80acc-422">Display the total download size</span></span>  

<span data-ttu-id="80acc-423">El tamaño total de las solicitudes de descarga se muestra en el panel **Resumen** , en la parte inferior del panel **red** .</span><span class="sxs-lookup"><span data-stu-id="80acc-423">The total download size of requests is listed in the **Summary** pane, at the bottom of the **Network** panel.</span></span>  

> [!CAUTION]
> <span data-ttu-id="80acc-424">Este número solo realiza un seguimiento de las solicitudes que se han registrado desde que se abrió DevTools.</span><span class="sxs-lookup"><span data-stu-id="80acc-424">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="80acc-425">Si se han producido otras solicitudes antes de que se abriera DevTools, no se cuentan las solicitudes anteriores.</span><span class="sxs-lookup"><span data-stu-id="80acc-425">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="El tamaño total de las solicitudes de descarga" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="80acc-427">El tamaño total de las solicitudes de descarga</span><span class="sxs-lookup"><span data-stu-id="80acc-427">The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="80acc-428">Para comprobar cómo los recursos grandes están después de que el explorador descomprime cada elemento, navegue para [Mostrar el tamaño descomprimido de un recurso](#display-the-uncompressed-size-of-a-resource).</span><span class="sxs-lookup"><span data-stu-id="80acc-428">To verify how large resources are after the browser uncompresses each item, navigate to [display the uncompressed size of a resource](#display-the-uncompressed-size-of-a-resource).</span></span>  

### <span data-ttu-id="80acc-429">Mostrar el seguimiento de la pila que causó una solicitud</span><span class="sxs-lookup"><span data-stu-id="80acc-429">Display the stack trace that caused a request</span></span>  

<span data-ttu-id="80acc-430">Después de que una instrucción de JavaScript solicite un recurso, sitúe el puntero en la columna del **iniciador** para mostrar el seguimiento de la pila que se dirige a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="80acc-430">After a JavaScript statement requests a resource, hover on the **Initiator** column to display the stack trace leading up to the request.</span></span>  

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
   <span data-ttu-id="80acc-432">El seguimiento de la pila que lleva a una solicitud de recursos</span><span class="sxs-lookup"><span data-stu-id="80acc-432">The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-433">Mostrar el tamaño descomprimido de un recurso</span><span class="sxs-lookup"><span data-stu-id="80acc-433">Display the uncompressed size of a resource</span></span>  

<span data-ttu-id="80acc-434">Active la casilla **usar filas de solicitud grandes** y, a continuación, revise el valor inferior de la columna **tamaño** .</span><span class="sxs-lookup"><span data-stu-id="80acc-434">Turn on the **Use large request rows** checkbox and then review the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Ejemplo de recursos sin comprimir" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="80acc-436">Un ejemplo de recursos sin comprimir \ (el tamaño comprimido del `jquery-3.3.1.min.js` archivo que se envió a través de la red fue `29.9 KB` , mientras que el tamaño descomprimido fue `84.9 KB` \)</span><span class="sxs-lookup"><span data-stu-id="80acc-436">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <span data-ttu-id="80acc-437">Exportar datos de solicitudes</span><span class="sxs-lookup"><span data-stu-id="80acc-437">Export requests data</span></span>  

### <span data-ttu-id="80acc-438">Guardar todas las solicitudes de red en un archivo HAR</span><span class="sxs-lookup"><span data-stu-id="80acc-438">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="80acc-439">Para guardar todas las solicitudes de red en un archivo HAR, siga los pasos que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="80acc-439">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="80acc-440">Mantenga el mouse sobre cualquier solicitud de la tabla solicitudes y abra el menú contextual \ (haga clic con el botón derecho \).</span><span class="sxs-lookup"><span data-stu-id="80acc-440">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="80acc-441">Elija **Guardar como Har with Content**.</span><span class="sxs-lookup"><span data-stu-id="80acc-441">Choose **Save as HAR with Content**.</span></span>  <span data-ttu-id="80acc-442">DevTools guarda todas las solicitudes que se han producido desde que abrió DevTools en el archivo HAR.</span><span class="sxs-lookup"><span data-stu-id="80acc-442">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="80acc-443">No puedes filtrar solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80acc-443">You are not able to filter requests.</span></span>  <span data-ttu-id="80acc-444">Tampoco puedes guardar una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="80acc-444">You are also not able to save a single request.</span></span>  

<span data-ttu-id="80acc-445">Una vez que haya guardado un archivo HAR, podrá volver a importarlo en DevTools para analizarlo.</span><span class="sxs-lookup"><span data-stu-id="80acc-445">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="80acc-446">Simplemente arrastre y coloque el archivo HAR en la tabla solicitudes.</span><span class="sxs-lookup"><span data-stu-id="80acc-446">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Elija Guardar como HAR with Content" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="80acc-448">Elija **Guardar como Har with Content**</span><span class="sxs-lookup"><span data-stu-id="80acc-448">Choose **Save as HAR with Content**</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-449">Copiar una o más solicitudes en el portapapeles</span><span class="sxs-lookup"><span data-stu-id="80acc-449">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="80acc-450">En la columna **nombre** de la tabla solicitudes, desplace el puntero sobre una solicitud y abra el menú contextual \ (haga clic con el botón derecho \), mantenga el puntero sobre **copiar**y elija una de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="80acc-450">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover on **Copy**, and choose one of the following options.</span></span>  

| <span data-ttu-id="80acc-451">Nombre</span><span class="sxs-lookup"><span data-stu-id="80acc-451">Name</span></span> | <span data-ttu-id="80acc-452">Detalles</span><span class="sxs-lookup"><span data-stu-id="80acc-452">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="80acc-453">Copiar dirección del vínculo</span><span class="sxs-lookup"><span data-stu-id="80acc-453">Copy Link Address</span></span>** | <span data-ttu-id="80acc-454">Copie la dirección URL de la solicitud en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="80acc-454">Copy the URL of the request to the clipboard.</span></span> |  
| **<span data-ttu-id="80acc-455">Copiar respuesta</span><span class="sxs-lookup"><span data-stu-id="80acc-455">Copy Response</span></span>** | <span data-ttu-id="80acc-456">Copie el cuerpo de la respuesta en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="80acc-456">Copy the response body to the clipboard.</span></span> |  
| **<span data-ttu-id="80acc-457">Copiar como fetch</span><span class="sxs-lookup"><span data-stu-id="80acc-457">Copy as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="80acc-458">Copiar como rizo</span><span class="sxs-lookup"><span data-stu-id="80acc-458">Copy as cURL</span></span>** | <span data-ttu-id="80acc-459">Copie la solicitud como un comando de rizo.</span><span class="sxs-lookup"><span data-stu-id="80acc-459">Copy the request as a cURL command.</span></span> |  
| **<span data-ttu-id="80acc-460">Copiar todo como fetch</span><span class="sxs-lookup"><span data-stu-id="80acc-460">Copy All as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="80acc-461">Copiar todo como rizo</span><span class="sxs-lookup"><span data-stu-id="80acc-461">Copy All as cURL</span></span>** | <span data-ttu-id="80acc-462">Copiar todas las solicitudes como una cadena de comandos de rizo.</span><span class="sxs-lookup"><span data-stu-id="80acc-462">Copy all requests as a chain of cURL commands.</span></span> |  
| **<span data-ttu-id="80acc-463">Copiar todo como HAR</span><span class="sxs-lookup"><span data-stu-id="80acc-463">Copy All as HAR</span></span>** | <span data-ttu-id="80acc-464">Copie todas las solicitudes como datos de HAR.</span><span class="sxs-lookup"><span data-stu-id="80acc-464">Copy all requests as HAR data.</span></span> |  

<!--
:::row:::
   :::column span="1":::
      **Copy Link Address**  
   :::column-end:::
   :::column span="2":::
      Copy the URL of the request to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy Response**  
   :::column-end:::
   :::column span="2":::
      Copy the response body to the clipboard.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy the request as a cURL command.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as Fetch**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as cURL**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as a chain of cURL commands.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Copy All as HAR**  
   :::column-end:::
   :::column span="2":::
      Copy all requests as HAR data.  
   :::column-end:::
:::row-end:::  
-->  

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Elija copiar respuesta" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="80acc-466">Elija **copiar respuesta**</span><span class="sxs-lookup"><span data-stu-id="80acc-466">Choose **Copy Response**</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-467">Copiar JSON de respuesta con formato en el portapapeles</span><span class="sxs-lookup"><span data-stu-id="80acc-467">Copy formatted response JSON to the clipboard</span></span>  

<span data-ttu-id="80acc-468">Elija una solicitud de red y navegue hasta el panel **encabezados** .</span><span class="sxs-lookup"><span data-stu-id="80acc-468">Choose a network request and navigate to the **Headers** pane.</span></span>  <span data-ttu-id="80acc-469">Para copiar el valor JSON de una respuesta, navegue a **solicitar carga**, desplace el puntero sobre el contenido de la respuesta JSON, abra el menú contextual \ (haga clic con el botón secundario del mouse \) y seleccione **Copiar valor**.</span><span class="sxs-lookup"><span data-stu-id="80acc-469">To copy the JSON value of a response, navigate to **Request payload**, hover on the JSON response content, open the contextual menu \(right-click\), and choose **Copy Value**.</span></span>  

:::row:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-copy-property-value.msft.png" alt-text="Copiar valor en el menú contextual" lightbox="../media/network-header-copy-property-value.msft.png":::
          <span data-ttu-id="80acc-471">**Copiar valor** en el menú contextual</span><span class="sxs-lookup"><span data-stu-id="80acc-471">**Copy Value** in contextual menu</span></span>  
        :::image-end:::  
   :::column-end:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-paste-property-value.msft.png" alt-text="Código Visual Studio con JSON de respuesta con formato" lightbox="../media/network-header-paste-property-value.msft.png":::
          <span data-ttu-id="80acc-473">Pegado de JSON de respuesta con formato en código de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="80acc-473">Pasting formatted response JSON in Visual Studio Code</span></span>  
        :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="80acc-474">Copiar valores de propiedades de solicitudes de red en el portapapeles</span><span class="sxs-lookup"><span data-stu-id="80acc-474">Copy property values from network requests to your clipboard</span></span>  

<span data-ttu-id="80acc-475">Para copiar los valores de propiedad de las solicitudes de red en el portapapeles, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="80acc-475">To copy property values from network requests to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="80acc-476">Abra el panel **encabezados** .</span><span class="sxs-lookup"><span data-stu-id="80acc-476">Open the **Headers** pane.</span></span>  
1.  <span data-ttu-id="80acc-477">Abra una de las siguientes secciones de encabezado.</span><span class="sxs-lookup"><span data-stu-id="80acc-477">Open one of the following header sections.</span></span>  
    *   <span data-ttu-id="80acc-478">Solicitar carga \ (JSON \)</span><span class="sxs-lookup"><span data-stu-id="80acc-478">Request payload \(JSON\)</span></span>  
    *   <span data-ttu-id="80acc-479">Datos de formulario</span><span class="sxs-lookup"><span data-stu-id="80acc-479">Form Data</span></span>  
    *   <span data-ttu-id="80acc-480">Parámetros de cadena de consulta</span><span class="sxs-lookup"><span data-stu-id="80acc-480">Query String Parameters</span></span>  
    *   <span data-ttu-id="80acc-481">Solicitar encabezados</span><span class="sxs-lookup"><span data-stu-id="80acc-481">Request Headers</span></span>  
    *   <span data-ttu-id="80acc-482">Encabezados de respuesta</span><span class="sxs-lookup"><span data-stu-id="80acc-482">Response Headers</span></span>  
1.  <span data-ttu-id="80acc-483">Abra el menú contextual \ (haga clic con el botón derecho \) > **Copiar valor**.</span><span class="sxs-lookup"><span data-stu-id="80acc-483">Open the contextual menu \(right-click\) > **Copy value**.</span></span>  <span data-ttu-id="80acc-484">Ahora puede pegar el valor en cualquier editor para revisarlo.</span><span class="sxs-lookup"><span data-stu-id="80acc-484">You can now paste the value into any editor to review it.</span></span>  
    
## <span data-ttu-id="80acc-485">Cambiar el diseño del panel red</span><span class="sxs-lookup"><span data-stu-id="80acc-485">Change the layout of the Network panel</span></span>  

<span data-ttu-id="80acc-486">Puede expandir o contraer secciones de la interfaz de usuario del panel **red** para destacar información importante.</span><span class="sxs-lookup"><span data-stu-id="80acc-486">You may expand or collapse sections of the **Network** panel UI to focus important information.</span></span>  

### <span data-ttu-id="80acc-487">Ocultar el panel de filtros</span><span class="sxs-lookup"><span data-stu-id="80acc-487">Hide the Filters pane</span></span>  

<span data-ttu-id="80acc-488">De forma predeterminada, DevTools muestra el panel **filtros** .</span><span class="sxs-lookup"><span data-stu-id="80acc-488">By default, DevTools show the **Filters** pane.</span></span>  
<span data-ttu-id="80acc-489">Elija **filtro** \ ( ![ filtro ][ImageFilterIcon] \) para ocultarlo.</span><span class="sxs-lookup"><span data-stu-id="80acc-489">Choose **Filter** \(![Filter][ImageFilterIcon]\) to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="El botón ocultar filtros" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="80acc-491">El botón ocultar filtros</span><span class="sxs-lookup"><span data-stu-id="80acc-491">The Hide Filters button</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-492">Usar filas de solicitudes grandes</span><span class="sxs-lookup"><span data-stu-id="80acc-492">Use large request rows</span></span>  

<span data-ttu-id="80acc-493">Use filas grandes cuando desee más espacios en blanco en la tabla solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="80acc-493">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="80acc-494">Algunas columnas también proporcionan un poco más de información cuando se usan filas grandes.</span><span class="sxs-lookup"><span data-stu-id="80acc-494">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="80acc-495">Por ejemplo, el valor inferior de la columna **tamaño** es el tamaño descomprimido de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="80acc-495">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Ejemplo de filas de solicitudes grandes en el panel solicitudes" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="80acc-497">Ejemplo de filas de solicitudes grandes en el panel **solicitudes**</span><span class="sxs-lookup"><span data-stu-id="80acc-497">An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="80acc-498">Para habilitar las filas grandes, active la casilla de verificación **usar filas de solicitudes grandes** .</span><span class="sxs-lookup"><span data-stu-id="80acc-498">To enable large rows, turn on the **Use large request rows** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Casilla de verificación usar filas de solicitudes grandes" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="80acc-500">Casilla de verificación **usar filas de solicitudes grandes**</span><span class="sxs-lookup"><span data-stu-id="80acc-500">The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <span data-ttu-id="80acc-501">Ocultar el panel de información general</span><span class="sxs-lookup"><span data-stu-id="80acc-501">Hide the Overview pane</span></span>  

<span data-ttu-id="80acc-502">De forma predeterminada, DevTools muestra el panel de **información general** .</span><span class="sxs-lookup"><span data-stu-id="80acc-502">By default, DevTools displays the **Overview** pane.</span></span>  <span data-ttu-id="80acc-503">Para ocultarla, desactive la casilla **Mostrar Descripción general** .</span><span class="sxs-lookup"><span data-stu-id="80acc-503">To hide it, turn off the **Show Overview** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="La casilla Mostrar información general" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="80acc-505">La casilla **Mostrar información general**</span><span class="sxs-lookup"><span data-stu-id="80acc-505">The **Show Overview** checkbox</span></span>  
:::image-end:::  

## <span data-ttu-id="80acc-506">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="80acc-506">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureScreenshotsIcon]: ../media/capture-screenshots-icon.msft.png  
[ImageClearIcon]: ../media/clear-requests-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageHideIcon]: ../media/hide-overview-icon.msft.png  
[ImageLargeResourceRowsIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageRecordOnIcon]: ../media/record-on-icon.msft.png  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Depurar aplicaciones web progresivas | Microsoft docs"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "Direcciones URL de datos | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Servidor proxy-Wikipedia"  

> [!NOTE]
> <span data-ttu-id="80acc-510">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="80acc-510">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="80acc-511">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/network/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="80acc-511">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="80acc-513">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="80acc-513">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

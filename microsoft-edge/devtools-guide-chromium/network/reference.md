---
description: Una referencia completa de las Microsoft Edge del panel DevTools Network.
title: Referencia de análisis de red
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: bdb1145e7ee8ed7865b68f9fd632c4b1a30007e9
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564836"
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
# <a name="network-analysis-reference"></a><span data-ttu-id="250f7-104">Referencia de análisis de red</span><span class="sxs-lookup"><span data-stu-id="250f7-104">Network Analysis reference</span></span>  

<span data-ttu-id="250f7-105">Descubra nuevas formas de analizar cómo se carga la página en esta referencia completa de las Microsoft Edge de análisis de red de DevTools.</span><span class="sxs-lookup"><span data-stu-id="250f7-105">Discover new ways to analyze how your page loads in this comprehensive reference of Microsoft Edge DevTools network analysis features.</span></span>  

## <a name="record-network-requests"></a><span data-ttu-id="250f7-106">Registrar solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="250f7-106">Record network requests</span></span>  

<span data-ttu-id="250f7-107">De forma predeterminada, DevTools registra todas las solicitudes de red en la **herramienta Red,** siempre y cuando DevTools esté abierto.</span><span class="sxs-lookup"><span data-stu-id="250f7-107">By default, DevTools record all network requests in the **Network** tool, so long as DevTools is open.</span></span>  

:::image type="complex" source="../media/network-network-panel.msft.png" alt-text="Panel Red" lightbox="../media/network-network-panel.msft.png":::
   <span data-ttu-id="250f7-109">La **herramienta Red**</span><span class="sxs-lookup"><span data-stu-id="250f7-109">The **Network** tool</span></span>  
:::image-end:::  

### <a name="stop-recording-network-requests"></a><span data-ttu-id="250f7-110">Detener la grabación de solicitudes de red</span><span class="sxs-lookup"><span data-stu-id="250f7-110">Stop recording network requests</span></span>  

<span data-ttu-id="250f7-111">Para detener la grabación de solicitudes, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="250f7-111">To stop recording requests, complete the following steps.</span></span>  

1.  <span data-ttu-id="250f7-112">En la **herramienta Red,** elija **Detener registro de red de grabación** \( Detener registro de red de grabación ![ ](../media/record-on-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="250f7-112">On the **Network** tool, choose **Stop recording network log** \(![Stop recording network log](../media/record-on-icon.msft.png)\).</span></span>  <span data-ttu-id="250f7-113">Se vuelve gris para indicar que DevTools ya no está grabando solicitudes.</span><span class="sxs-lookup"><span data-stu-id="250f7-113">It turns grey to indicate that DevTools is no longer recording requests.</span></span>  
1.  <span data-ttu-id="250f7-114">Seleccione `Control` + `E` \(Windows, Linux\) o `Command` + `E` \(macOS\) mientras la **herramienta Red** está en el foco.</span><span class="sxs-lookup"><span data-stu-id="250f7-114">Select `Control`+`E` \(Windows, Linux\) or `Command`+`E` \(macOS\) while the **Network** tool is in focus.</span></span>  

### <a name="clear-requests"></a><span data-ttu-id="250f7-115">Borrar solicitudes</span><span class="sxs-lookup"><span data-stu-id="250f7-115">Clear requests</span></span>  

<span data-ttu-id="250f7-116">Elija **Borrar** \( Borrar \) en la herramienta Red para borrar todas las ![ solicitudes de la tabla ](../media/clear-requests-icon.msft.png) Solicitudes. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="250f7-116">Choose **Clear** \(![Clear](../media/clear-requests-icon.msft.png)\) on the **Network** tool to clear all requests from the Requests table.</span></span>  

:::image type="complex" source="../media/network-network-clear-button.msft.png" alt-text="El botón Borrar" lightbox="../media/network-network-clear-button.msft.png":::
   <span data-ttu-id="250f7-118">El **botón Borrar**</span><span class="sxs-lookup"><span data-stu-id="250f7-118">The **Clear** button</span></span>  
:::image-end:::  

### <a name="save-requests-across-page-loads"></a><span data-ttu-id="250f7-119">Guardar solicitudes en cargas de página</span><span class="sxs-lookup"><span data-stu-id="250f7-119">Save requests across page loads</span></span>  

<span data-ttu-id="250f7-120">Para guardar las solicitudes en cargas de página, en la **herramienta Red,** active la casilla **Conservar registro.**</span><span class="sxs-lookup"><span data-stu-id="250f7-120">To save requests across page loads, on the **Network** tool, turn on the **Preserve log** checkbox.</span></span>  <span data-ttu-id="250f7-121">DevTools guarda todas las solicitudes hasta que deshabilita **Conservar registro**.</span><span class="sxs-lookup"><span data-stu-id="250f7-121">DevTools saves all requests until you disable **Preserve log**.</span></span>  

:::image type="complex" source="../media/network-network-preserve-log.msft.png" alt-text="La casilla Conservar registro" lightbox="../media/network-network-preserve-log.msft.png":::
   <span data-ttu-id="250f7-123">La **casilla Conservar registro**</span><span class="sxs-lookup"><span data-stu-id="250f7-123">The **Preserve Log** checkbox</span></span>  
:::image-end:::  

### <a name="capture-screenshots-during-page-load"></a><span data-ttu-id="250f7-124">Capturar capturas de pantalla durante la carga de página</span><span class="sxs-lookup"><span data-stu-id="250f7-124">Capture screenshots during page load</span></span>  

<span data-ttu-id="250f7-125">Captura capturas de pantalla para analizar las pantallas de los usuarios a la espera de que se cargue la página.</span><span class="sxs-lookup"><span data-stu-id="250f7-125">Capture screenshots to analyze what displays for users while waiting for your page to load.</span></span>  

<span data-ttu-id="250f7-126">Para habilitar capturas de pantalla, elija **Configuración de red**y, en la herramienta **Red,** active la **casilla Capturar capturas de** pantalla.</span><span class="sxs-lookup"><span data-stu-id="250f7-126">To enable screenshots, choose **Network settings**, and on the **Network** tool, turn on the **Capture screenshots** checkbox.</span></span>  

<span data-ttu-id="250f7-127">Actualice la página mientras la **herramienta Red** está en el foco para capturar capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="250f7-127">Refresh the page while the **Network** tool is in focus to capture screenshots.</span></span>  

<span data-ttu-id="250f7-128">Después de capturar una captura de pantalla, interactúas con ella de las siguientes maneras.</span><span class="sxs-lookup"><span data-stu-id="250f7-128">After capturing a screenshot, you interact with it in the following ways.</span></span>  

*   <span data-ttu-id="250f7-129">Mantenga el mouse en una captura de pantalla para mostrar el punto en el que se capturó esa captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="250f7-129">Hover on a screenshot to display the point at which that screenshot was captured.</span></span>  <span data-ttu-id="250f7-130">Se muestra una línea amarilla en el **panel Información** general.</span><span class="sxs-lookup"><span data-stu-id="250f7-130">A yellow line is displayed on the **Overview** pane.</span></span>  
*   <span data-ttu-id="250f7-131">Elige la miniatura de una pantalla para filtrar las solicitudes que se produjeron después de capturar la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="250f7-131">Choose the thumbnail of a screen to filter out any requests that occurred after the screenshot was captured.</span></span>  
*   <span data-ttu-id="250f7-132">Haz doble clic en una miniatura para ampliarla.</span><span class="sxs-lookup"><span data-stu-id="250f7-132">Double-click a thumbnail to zoom into it.</span></span>  

:::image type="complex" source="../media/network-network-screenshot-hover.msft.png" alt-text="Mantener el mouse en una captura de pantalla" lightbox="../media/network-network-screenshot-hover.msft.png":::
   <span data-ttu-id="250f7-134">Mantener el mouse en una captura de pantalla</span><span class="sxs-lookup"><span data-stu-id="250f7-134">Hover on a screenshot</span></span>  
:::image-end:::  

<!--  ### Replay XHR request  -->

<!--  To replay an XHR request, hover on the request in the Requests table, open the contextual menu \(right-click\), and choose **Replay XHR**.  -->

<!--  
:::image type="complex" source="../media/network-replay-xhr.msft.png" alt-text="Choose Replay XHR" lightbox="../media/network-replay-xhr.msft.png":::
   Choose Replay XHR  
:::image-end:::  
-->  

## <a name="change-loading-behavior"></a><span data-ttu-id="250f7-135">Cambiar el comportamiento de carga</span><span class="sxs-lookup"><span data-stu-id="250f7-135">Change loading behavior</span></span>  

### <a name="emulate-a-first-time-visitor-by-disabling-the-browser-cache"></a><span data-ttu-id="250f7-136">Emular a un visitante por primera vez deshabilitando la memoria caché del explorador</span><span class="sxs-lookup"><span data-stu-id="250f7-136">Emulate a first-time visitor by disabling the browser cache</span></span>  

<span data-ttu-id="250f7-137">Para emular el modo en que un usuario por primera vez experimenta su sitio, active la casilla **Deshabilitar caché.**</span><span class="sxs-lookup"><span data-stu-id="250f7-137">To emulate how a first-time user experiences your site, turn on the **Disable cache** checkbox.</span></span>  <span data-ttu-id="250f7-138">DevTools deshabilita la memoria caché del explorador.</span><span class="sxs-lookup"><span data-stu-id="250f7-138">DevTools disables the browser cache.</span></span>  <span data-ttu-id="250f7-139">Esta característica emula con mayor precisión la experiencia de un usuario por primera vez, ya que las solicitudes se sirven desde la memoria caché del explorador en las visitas repetidas.</span><span class="sxs-lookup"><span data-stu-id="250f7-139">This feature more accurately emulates a first-time user's experience, because requests are served from the browser cache on repeat visits.</span></span>  

:::image type="complex" source="../media/network-network-disable-cache-checkbox.msft.png" alt-text="Casilla Deshabilitar caché" lightbox="../media/network-network-disable-cache-checkbox.msft.png":::
   <span data-ttu-id="250f7-141">Casilla **Deshabilitar caché**</span><span class="sxs-lookup"><span data-stu-id="250f7-141">The **Disable Cache** checkbox</span></span>  
:::image-end:::  

#### <a name="disable-the-browser-cache-from-the-network-conditions-drawer"></a><span data-ttu-id="250f7-142">Deshabilitar la memoria caché del explorador desde el cajón de condiciones de red</span><span class="sxs-lookup"><span data-stu-id="250f7-142">Disable the browser cache from the Network Conditions drawer</span></span>  

<span data-ttu-id="250f7-143">Si desea deshabilitar la memoria caché mientras trabaja en otros paneles de DevTools, use el cajón Condiciones de red.</span><span class="sxs-lookup"><span data-stu-id="250f7-143">If you want to disable the cache while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="250f7-144">Abra el **cajón Condiciones de** red.</span><span class="sxs-lookup"><span data-stu-id="250f7-144">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="250f7-145">Active \(or off\) la casilla **Deshabilitar caché.**</span><span class="sxs-lookup"><span data-stu-id="250f7-145">Turn on \(or off\) the **Disable cache** checkbox.</span></span>  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-the-browser-cache"></a><span data-ttu-id="250f7-146">Borrar manualmente la memoria caché del explorador</span><span class="sxs-lookup"><span data-stu-id="250f7-146">Manually clear the browser cache</span></span>  

<span data-ttu-id="250f7-147">Para borrar manualmente la memoria caché del explorador en cualquier momento, abra el menú contextual \(hacer clic con el botón secundario\) en cualquier lugar de la tabla Solicitudes y elija Borrar caché **del explorador**.</span><span class="sxs-lookup"><span data-stu-id="250f7-147">To manually clear the browser cache at any time, open the contextual menu \(right-click\) anywhere in the Requests table and choose **Clear Browser Cache**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cache.msft.png" alt-text="Elegir Borrar caché del explorador" lightbox="../media/network-network-clear-browser-cache.msft.png":::
   <span data-ttu-id="250f7-149">Elegir **Borrar caché del explorador**</span><span class="sxs-lookup"><span data-stu-id="250f7-149">Choose **Clear Browser Cache**</span></span>  
:::image-end:::  

### <a name="emulate-offline"></a><span data-ttu-id="250f7-150">Emular sin conexión</span><span class="sxs-lookup"><span data-stu-id="250f7-150">Emulate offline</span></span>  

<span data-ttu-id="250f7-151">Una nueva clase de aplicaciones web, denominada [Progressive Web Apps][DevtoolsProgressiveWebApps], funciona sin conexión con la ayuda de los **trabajadores del servicio.**</span><span class="sxs-lookup"><span data-stu-id="250f7-151">A new class of web apps, named [Progressive Web Apps][DevtoolsProgressiveWebApps], functions offline with the help of **service workers**.</span></span>  <span data-ttu-id="250f7-152">Puede resultar útil simular rápidamente un dispositivo que no tiene conexión de datos al compilar este tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="250f7-152">You may find it useful to quickly simulate a device that has no data connection when you are building this type of app.</span></span>  

<!--[ServiceWorkers]: /web/fundamentals/getting-started/primers/service-workers  -->

<span data-ttu-id="250f7-153">Elija el **menú desplegable En** línea, busque en **Preestablecidos**y elija **Sin** conexión para simular una experiencia de red sin conexión.</span><span class="sxs-lookup"><span data-stu-id="250f7-153">Choose the **Online** dropdown menu, search under **Presets**, and choose **Offline** to simulate an offline network experience.</span></span>  

:::image type="complex" source="../media/network-network-offline-dropdown.msft.png" alt-text="Menú desplegable Sin conexión" lightbox="../media/network-network-offline-dropdown.msft.png":::
   <span data-ttu-id="250f7-155">Menú **desplegable Sin** conexión</span><span class="sxs-lookup"><span data-stu-id="250f7-155">The **Offline** dropdown menu</span></span>  
:::image-end:::  

### <a name="emulate-slow-network-connections"></a><span data-ttu-id="250f7-156">Emular conexiones de red lentas</span><span class="sxs-lookup"><span data-stu-id="250f7-156">Emulate slow network connections</span></span>  

<span data-ttu-id="250f7-157">Emular velocidades 3G, rápidas 3G y otras velocidades de conexión desde el **menú** desplegable En línea.</span><span class="sxs-lookup"><span data-stu-id="250f7-157">Emulate Slow 3G, Fast 3G, and other connection speeds from the **Online** dropdown menu.</span></span>  

:::image type="complex" source="../media/network-network-throttling-menu.msft.png" alt-text="Menú desplegable Limitación" lightbox="../media/network-network-throttling-menu.msft.png":::
   <span data-ttu-id="250f7-159">Menú **desplegable Limitación**</span><span class="sxs-lookup"><span data-stu-id="250f7-159">The **Throttling** dropdown menu</span></span>  
:::image-end:::  

<span data-ttu-id="250f7-160">Puede elegir entre diferentes presets, como Slow 3G o Fast 3G.</span><span class="sxs-lookup"><span data-stu-id="250f7-160">You may choose from different presets, such as Slow 3G or Fast 3G.</span></span>  <span data-ttu-id="250f7-161">Para agregar sus propios ajustes preestablecidos personalizados, abra el menú Limitación y elija **Agregar**  >  **personalizado**.</span><span class="sxs-lookup"><span data-stu-id="250f7-161">To add your own custom presets, open the Throttling menu, and choose **Custom** > **Add**.</span></span>  

<span data-ttu-id="250f7-162">DevTools muestra un icono de advertencia junto a la **herramienta Red** para recordarle que la limitación está habilitada.</span><span class="sxs-lookup"><span data-stu-id="250f7-162">DevTools displays a warning icon next to the **Network** tool to remind you that throttling is enabled.</span></span>  

#### <a name="emulate-slow-network-connections-from-the-network-conditions-drawer"></a><span data-ttu-id="250f7-163">Emular conexiones de red lentas desde el cajón de condiciones de red</span><span class="sxs-lookup"><span data-stu-id="250f7-163">Emulate slow network connections from the Network Conditions drawer</span></span>  

<span data-ttu-id="250f7-164">Si desea limitar la conexión de red mientras trabaja en otros paneles de DevTools, use el cajón Condiciones de red.</span><span class="sxs-lookup"><span data-stu-id="250f7-164">If you want to throttle the network connection while working in other DevTools panels, use the Network Conditions drawer.</span></span>  

1.  <span data-ttu-id="250f7-165">Abra el **cajón Condiciones de** red.</span><span class="sxs-lookup"><span data-stu-id="250f7-165">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="250f7-166">Elija la velocidad de conexión en el menú **Limitación.**</span><span class="sxs-lookup"><span data-stu-id="250f7-166">Choose your connection speed from the **Throttling** menu.</span></span>  

<!--todo: add network condition section when available -->  

### <a name="manually-clear-browser-cookies"></a><span data-ttu-id="250f7-167">Borrar manualmente las cookies del explorador</span><span class="sxs-lookup"><span data-stu-id="250f7-167">Manually clear browser cookies</span></span>  

<span data-ttu-id="250f7-168">Para borrar manualmente las cookies del explorador en cualquier momento, mantenga el mouse en cualquier lugar de la tabla Solicitudes, abra el menú contextual \(hacer clic con el botón secundario en\) y elija **Borrar cookies del explorador**.</span><span class="sxs-lookup"><span data-stu-id="250f7-168">To manually clear browser cookies at any time, hover anywhere in the Requests table, open the contextual menu \(right-click\), and choose **Clear Browser Cookies**.</span></span>  

:::image type="complex" source="../media/network-network-clear-browser-cookies.msft.png" alt-text="Elegir Borrar cookies del explorador" lightbox="../media/network-network-clear-browser-cookies.msft.png":::
   <span data-ttu-id="250f7-170">Elegir **Borrar cookies del explorador**</span><span class="sxs-lookup"><span data-stu-id="250f7-170">Choose **Clear Browser Cookies**</span></span>  
:::image-end:::  

### <a name="override-the-user-agent"></a><span data-ttu-id="250f7-171">Invalidar el agente de usuario</span><span class="sxs-lookup"><span data-stu-id="250f7-171">Override the user agent</span></span>  

<span data-ttu-id="250f7-172">Para invalidar manualmente el agente de usuario, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="250f7-172">To manually override the user agent, use the following steps.</span></span>  

1.  <span data-ttu-id="250f7-173">Abra el **cajón Condiciones de** red.</span><span class="sxs-lookup"><span data-stu-id="250f7-173">Open the **Network Conditions** drawer.</span></span>  
1.  <span data-ttu-id="250f7-174">Desactiva la casilla **Seleccionar automáticamente.**</span><span class="sxs-lookup"><span data-stu-id="250f7-174">Turn off the **Select automatically** checkbox.</span></span>  
1.  <span data-ttu-id="250f7-175">Elija una opción de agente de usuario en el menú o escriba una personalizada en el cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="250f7-175">Choose a user agent option from the menu, or enter a custom one in the text box.</span></span>  

<!--todo: add network condition section when available -->  

## <a name="filter-requests"></a><span data-ttu-id="250f7-176">Solicitudes de filtro</span><span class="sxs-lookup"><span data-stu-id="250f7-176">Filter requests</span></span>  

### <a name="filter-requests-by-properties"></a><span data-ttu-id="250f7-177">Filtrar solicitudes por propiedades</span><span class="sxs-lookup"><span data-stu-id="250f7-177">Filter requests by properties</span></span>  

<span data-ttu-id="250f7-178">Use el **cuadro de** texto Filtrar para filtrar las solicitudes por propiedades, como el dominio o el tamaño de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="250f7-178">Use the **Filter** text box to filter requests by properties, such as the domain or size of the request.</span></span>  

<span data-ttu-id="250f7-179">Si no se muestra el cuadro de texto, es probable que el panel **Filtros** esté oculto.</span><span class="sxs-lookup"><span data-stu-id="250f7-179">If the text box is not displayed, the **Filters** pane is probably hidden.</span></span>  
<span data-ttu-id="250f7-180">Para obtener más información, vaya [a Ocultar el panel Filtros](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="250f7-180">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

:::image type="complex" source="../media/network-network-filters-textbox.msft.png" alt-text="Cuadro de texto Filtrar" lightbox="../media/network-network-filters-textbox.msft.png":::
   <span data-ttu-id="250f7-182">Cuadro **de texto** Filtrar</span><span class="sxs-lookup"><span data-stu-id="250f7-182">The **Filter** text box</span></span>  
:::image-end:::  

<span data-ttu-id="250f7-183">Puede usar varias propiedades simultáneamente separando cada propiedad con un espacio.</span><span class="sxs-lookup"><span data-stu-id="250f7-183">You may use multiple properties simultaneously by separating each property with a space.</span></span>  <span data-ttu-id="250f7-184">Por ejemplo, `mime-type:image/png larger-than:1K` muestra todos los PNG de más de 1 kilobyte.</span><span class="sxs-lookup"><span data-stu-id="250f7-184">For example, `mime-type:image/png larger-than:1K` displays all PNGs that are larger than 1 kilobyte.</span></span>  <span data-ttu-id="250f7-185">Los filtros multi-propiedad son equivalentes a `AND` las operaciones.</span><span class="sxs-lookup"><span data-stu-id="250f7-185">The multi-property filters are equivalent to `AND` operations.</span></span>  `OR` <span data-ttu-id="250f7-186">actualmente no se admiten operaciones.</span><span class="sxs-lookup"><span data-stu-id="250f7-186">operations are currently not supported.</span></span>  

<span data-ttu-id="250f7-187">Lista completa de propiedades admitidas.</span><span class="sxs-lookup"><span data-stu-id="250f7-187">The complete list of supported properties.</span></span>  

| <span data-ttu-id="250f7-188">Propiedad</span><span class="sxs-lookup"><span data-stu-id="250f7-188">Property</span></span> | <span data-ttu-id="250f7-189">Detalles</span><span class="sxs-lookup"><span data-stu-id="250f7-189">Details</span></span> |  
|:--- | :--- |  
| `domain` | <span data-ttu-id="250f7-190">Solo mostrar recursos del dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="250f7-190">Only display resources from the specified domain.</span></span>  <span data-ttu-id="250f7-191">Puede usar un carácter comodín \( `*` \) para incluir varios dominios.</span><span class="sxs-lookup"><span data-stu-id="250f7-191">You may use a wildcard character \(`*`\) to include multiple domains.</span></span>  <span data-ttu-id="250f7-192">Por ejemplo, `*.com` muestra recursos de todos los nombres de dominio que terminan en `.com` .</span><span class="sxs-lookup"><span data-stu-id="250f7-192">For example, `*.com` displays resources from all domain names ending in `.com`.</span></span>  <span data-ttu-id="250f7-193">DevTools rellena el menú desplegable de autocompletar con todos los dominios que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="250f7-193">DevTools populate the autocomplete dropdown menu with all of the domains that are found.</span></span> |  
| `has-response-header` | <span data-ttu-id="250f7-194">Muestra los recursos que contienen el encabezado de respuesta HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="250f7-194">Displays the resources that contain the specified HTTP response header.</span></span>  <span data-ttu-id="250f7-195">DevTools rellena el desplegable de autocompletar con todos los encabezados de respuesta que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="250f7-195">DevTools populate the autocomplete dropdown with all of the response headers that are found.</span></span> |  
| `is` | <span data-ttu-id="250f7-196">Se `is:running` usa para buscar `WebSocket` recursos.</span><span class="sxs-lookup"><span data-stu-id="250f7-196">Use `is:running` to find `WebSocket` resources.</span></span> |  
| `larger-than` | <span data-ttu-id="250f7-197">Muestra recursos que son mayores que el tamaño especificado, en bytes.</span><span class="sxs-lookup"><span data-stu-id="250f7-197">Displays resources that are larger than the specified size, in bytes.</span></span>  <span data-ttu-id="250f7-198">Establecer un valor de `1000` equivale a establecer un valor de `1k` .</span><span class="sxs-lookup"><span data-stu-id="250f7-198">Setting a value of `1000` is equivalent to setting a value of `1k`.</span></span> |  
| `method` | <span data-ttu-id="250f7-199">Muestra los recursos que se recuperaron a través de un tipo de método HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="250f7-199">Displays resources that were retrieved over a specified HTTP method type.</span></span>  <span data-ttu-id="250f7-200">DevTools rellena el desplegable con todos los métodos HTTP que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="250f7-200">DevTools populate the dropdown with all of the HTTP methods  that are found.</span></span> |  
| `mime-type` | <span data-ttu-id="250f7-201">Muestra recursos de un tipo MIME especificado.</span><span class="sxs-lookup"><span data-stu-id="250f7-201">Displays resources of a specified MIME type.</span></span>  <span data-ttu-id="250f7-202">DevTools rellena el desplegable con todos los tipos MIME que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="250f7-202">DevTools populate the dropdown with all MIME types  that are found.</span></span> |  
| `mixed-content` | <span data-ttu-id="250f7-203">Mostrar todos los recursos de contenido combinado \( \) o solo los que se muestran `mixed-content:all` actualmente \( `mixed-content:displayed` \).</span><span class="sxs-lookup"><span data-stu-id="250f7-203">Show all mixed content resources \(`mixed-content:all`\) or just the ones that are currently displayed \(`mixed-content:displayed`\).</span></span> |  
| `scheme` | <span data-ttu-id="250f7-204">Muestra los recursos recuperados a través de HTTP sin protección \( `scheme:http` \) o HTTPS protegido \( `scheme:https` \).</span><span class="sxs-lookup"><span data-stu-id="250f7-204">Displays resources retrieved over unprotected HTTP \(`scheme:http`\) or protected HTTPS \(`scheme:https`\).</span></span> |  
| `set-cookie-domain` | <span data-ttu-id="250f7-205">Muestra recursos que tienen un `Set-Cookie` encabezado con un atributo que coincide con el valor `Domain` especificado.</span><span class="sxs-lookup"><span data-stu-id="250f7-205">Displays resources that have a `Set-Cookie` header with a `Domain` attribute that matches the specified value.</span></span>  <span data-ttu-id="250f7-206">DevTools rellena el autocompletar con todos los dominios de cookie que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="250f7-206">DevTools populate the autocomplete with all of the cookie domains that are found.</span></span> |  
| `set-cookie-name` | <span data-ttu-id="250f7-207">Muestra recursos que tienen un `Set-Cookie` encabezado con un nombre que coincide con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="250f7-207">Displays resources that have a `Set-Cookie` header with a name that matches the specified value.</span></span>  <span data-ttu-id="250f7-208">DevTools rellena el autocompletar con todos los nombres de cookie que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="250f7-208">DevTools populate the autocomplete with all of the cookie names that are found.</span></span> |  
| `set-cookie-value` | <span data-ttu-id="250f7-209">Muestra recursos que tienen un `Set-Cookie` encabezado con un valor que coincide con el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="250f7-209">Displays resources that have a `Set-Cookie` header with a value that matches the specified value.</span></span>  <span data-ttu-id="250f7-210">DevTools rellena el autocompletar con todos los valores de cookie que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="250f7-210">DevTools populate the autocomplete with all of the cookie values that are found.</span></span> |  
| `status-code` | <span data-ttu-id="250f7-211">Muestra recursos que coinciden con el código de estado HTTP específico.</span><span class="sxs-lookup"><span data-stu-id="250f7-211">Displays resources that match the specific HTTP status code.</span></span>  <span data-ttu-id="250f7-212">DevTools rellena el menú desplegable de autocompletar con todos los códigos de estado que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="250f7-212">DevTools populates the autocomplete dropdown menu with all of the status codes that are found.</span></span> |  

### <a name="filter-requests-by-type"></a><span data-ttu-id="250f7-213">Filtrar solicitudes por tipo</span><span class="sxs-lookup"><span data-stu-id="250f7-213">Filter requests by type</span></span>  

<span data-ttu-id="250f7-214">Para filtrar las solicitudes por tipo de solicitud, elija uno de los botones siguientes en la **herramienta Red.**</span><span class="sxs-lookup"><span data-stu-id="250f7-214">To filter requests by request type, choose the one of the following buttons on the **Network** tool.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-215">XHR</span><span class="sxs-lookup"><span data-stu-id="250f7-215">XHR</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-216">JS</span><span class="sxs-lookup"><span data-stu-id="250f7-216">JS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-217">CSS</span><span class="sxs-lookup"><span data-stu-id="250f7-217">CSS</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-218">Img</span><span class="sxs-lookup"><span data-stu-id="250f7-218">Img</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-219">Multimedia</span><span class="sxs-lookup"><span data-stu-id="250f7-219">Media</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-220">Fuente</span><span class="sxs-lookup"><span data-stu-id="250f7-220">Font</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-221">Doc</span><span class="sxs-lookup"><span data-stu-id="250f7-221">Doc</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-222">WS</span><span class="sxs-lookup"><span data-stu-id="250f7-222">WS</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-223">WebSocket.</span><span class="sxs-lookup"><span data-stu-id="250f7-223">WebSocket.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-224">Manifiesto</span><span class="sxs-lookup"><span data-stu-id="250f7-224">Manifest</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-225">Otros</span><span class="sxs-lookup"><span data-stu-id="250f7-225">Other</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-226">Cualquier otro tipo que no aparezca.</span><span class="sxs-lookup"><span data-stu-id="250f7-226">Any other type not listed.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="250f7-227">Si los botones no se muestran, el **panel Filtros** puede estar oculto.</span><span class="sxs-lookup"><span data-stu-id="250f7-227">If the buttons do not display, the **Filters** pane may be hidden.</span></span>  
<span data-ttu-id="250f7-228">Para obtener más información, vaya [a Ocultar el panel Filtros](#hide-the-filters-pane).</span><span class="sxs-lookup"><span data-stu-id="250f7-228">For more information, navigate to [Hide the Filters pane](#hide-the-filters-pane).</span></span>  

<span data-ttu-id="250f7-229">Para habilitar varios filtros de tipo simultáneamente, mantenga presionado `Control` \(Windows, Linux\) o `Command` \(macOS\) y, a continuación, elija.</span><span class="sxs-lookup"><span data-stu-id="250f7-229">To enable multiple type filters simultaneously, hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and then choose.</span></span>  

:::image type="complex" source="../media/network-network-type-filters.msft.png" alt-text="Usar los filtros De tipo para mostrar recursos JS, CSS y Document" lightbox="../media/network-network-type-filters.msft.png":::
   <span data-ttu-id="250f7-231">Usar los filtros De tipo para mostrar recursos JS, CSS y Document</span><span class="sxs-lookup"><span data-stu-id="250f7-231">Use the Type filters to display JS, CSS, and Document resources</span></span>  
:::image-end:::  

### <a name="filter-requests-by-time"></a><span data-ttu-id="250f7-232">Filtrar solicitudes por tiempo</span><span class="sxs-lookup"><span data-stu-id="250f7-232">Filter requests by time</span></span>  

<span data-ttu-id="250f7-233">Elija y arrastre a la izquierda o a la derecha en **el** panel Información general para mostrar solo las solicitudes que estaban activas durante ese período de tiempo.</span><span class="sxs-lookup"><span data-stu-id="250f7-233">Choose and drag left or right on the **Overview** pane to only display requests that were active during that time frame.</span></span>  <span data-ttu-id="250f7-234">El filtro es inclusivo.</span><span class="sxs-lookup"><span data-stu-id="250f7-234">The filter is inclusive.</span></span>  <span data-ttu-id="250f7-235">Se muestra cualquier solicitud que estuvo activa durante el tiempo resaltado.</span><span class="sxs-lookup"><span data-stu-id="250f7-235">Any request that was active during the highlighted time is shown.</span></span>  

:::image type="complex" source="../media/network-network-overview-filter.msft.png" alt-text="Filtrar las solicitudes que estaban inactivas alrededor de 300 ms" lightbox="../media/network-network-overview-filter.msft.png":::
   <span data-ttu-id="250f7-237">Filtrar las solicitudes que estaban inactivas alrededor de 300 ms</span><span class="sxs-lookup"><span data-stu-id="250f7-237">Filter out any requests that were inactive around 300 ms</span></span>  
:::image-end:::  

### <a name="hide-data-urls"></a><span data-ttu-id="250f7-238">Ocultar direcciones URL de datos</span><span class="sxs-lookup"><span data-stu-id="250f7-238">Hide data URLs</span></span>  

<span data-ttu-id="250f7-239">[Las direcciones URL de datos][MDNHTTPDataURIs] son archivos pequeños incrustados en otros documentos.</span><span class="sxs-lookup"><span data-stu-id="250f7-239">[Data URLs][MDNHTTPDataURIs] are small files embedded into other documents.</span></span>  <span data-ttu-id="250f7-240">Cualquier solicitud que se muestra en la tabla Solicitudes que comienza por `data:` es una dirección URL de datos.</span><span class="sxs-lookup"><span data-stu-id="250f7-240">Any request that displays in the Requests table that starts with `data:` is a data URL.</span></span>  

<span data-ttu-id="250f7-241">Para ocultar las solicitudes, desactive la casilla Ocultar direcciones **URL de** datos.</span><span class="sxs-lookup"><span data-stu-id="250f7-241">To hide the requests, turn off the **Hide data URLs** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-hide-data-urls.msft.png" alt-text="Casilla Ocultar direcciones URL de datos" lightbox="../media/network-network-hide-data-urls.msft.png":::
   <span data-ttu-id="250f7-243">Casilla **Ocultar direcciones URL de datos**</span><span class="sxs-lookup"><span data-stu-id="250f7-243">The **Hide Data URLs** checkbox</span></span>  
:::image-end:::  

## <a name="sort-requests"></a><span data-ttu-id="250f7-244">Ordenar solicitudes</span><span class="sxs-lookup"><span data-stu-id="250f7-244">Sort requests</span></span>  

<span data-ttu-id="250f7-245">De forma predeterminada, las solicitudes de la tabla Solicitudes se ordenan por hora de inicio, pero puede ordenar la tabla con otros criterios.</span><span class="sxs-lookup"><span data-stu-id="250f7-245">By default, the requests in the Requests table are sorted by initiation time, but you may sort the table using other criteria.</span></span>  

### <a name="sort-by-column"></a><span data-ttu-id="250f7-246">Ordenar por columna</span><span class="sxs-lookup"><span data-stu-id="250f7-246">Sort by column</span></span>  

<span data-ttu-id="250f7-247">Elija el encabezado de cualquier columna de las solicitudes para ordenar las solicitudes por esa columna.</span><span class="sxs-lookup"><span data-stu-id="250f7-247">Choose the header of any column in the Requests to sort requests by that column.</span></span>  

### <a name="sort-by-activity-phase"></a><span data-ttu-id="250f7-248">Ordenar por fase de actividad</span><span class="sxs-lookup"><span data-stu-id="250f7-248">Sort by activity phase</span></span>  

<span data-ttu-id="250f7-249">Para cambiar el modo en que la cascada ordena las solicitudes, mantenga el mouse en el encabezado de la tabla Solicitudes, abra el menú contextual \(hacer clic con el botón secundario\), mantenga el mouse en **Cascada**y elija una de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="250f7-249">To change how the Waterfall sorts requests, hover on the header of the Requests table, open the contextual menu \(right-click\), hover on **Waterfall**, and choose one of the following options.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-250">Hora de inicio</span><span class="sxs-lookup"><span data-stu-id="250f7-250">Start Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-251">La primera solicitud que se inició está en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="250f7-251">The first request that was initiated is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-252">Tiempo de respuesta</span><span class="sxs-lookup"><span data-stu-id="250f7-252">Response Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-253">La primera solicitud que se inició la descarga está en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="250f7-253">The first request that started downloading is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-254">Hora de finalización</span><span class="sxs-lookup"><span data-stu-id="250f7-254">End Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-255">La primera solicitud que ha finalizado está en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="250f7-255">The first request that finished is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-256">Duración total</span><span class="sxs-lookup"><span data-stu-id="250f7-256">Total Duration</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-257">La solicitud con la configuración de conexión más corta y la solicitud o respuesta está en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="250f7-257">The request with the shortest connection settings and request or response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-258">Latencia</span><span class="sxs-lookup"><span data-stu-id="250f7-258">Latency</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-259">La solicitud que ha esperado más tiempo para obtener una respuesta está en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="250f7-259">The request that waited the shortest time for a response is at the top.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="250f7-260">Estas descripciones suponen que cada opción respectiva se clasifica de más corta a más larga.</span><span class="sxs-lookup"><span data-stu-id="250f7-260">These descriptions assume that each respective option is ranked from shortest to longest.</span></span>  <span data-ttu-id="250f7-261">Elija el encabezado de la columna **Cascada** para invertir el orden.</span><span class="sxs-lookup"><span data-stu-id="250f7-261">Choose the header of the **Waterfall** column to reverse the order.</span></span>  

:::image type="complex" source="../media/network-network-waterfall-total-duration.msft.png" alt-text="Ordenar la cascada por duración total" lightbox="../media/network-network-waterfall-total-duration.msft.png":::
   <span data-ttu-id="250f7-263">Ordenar la cascada por duración total \(La parte más ligera de cada barra es el tiempo invertido en espera y la parte más oscura es el tiempo invertido en descargar bytes\)</span><span class="sxs-lookup"><span data-stu-id="250f7-263">Sort the Waterfall by total duration  \(The lighter portion of each bar is time spent waiting and the darker portion is time spent downloading bytes\)</span></span>  
:::image-end:::  

## <a name="analyze-requests"></a><span data-ttu-id="250f7-264">Analizar solicitudes</span><span class="sxs-lookup"><span data-stu-id="250f7-264">Analyze requests</span></span>  

<span data-ttu-id="250f7-265">Mientras DevTools está abierto, registra todas las solicitudes en la **herramienta Red.**</span><span class="sxs-lookup"><span data-stu-id="250f7-265">So long as DevTools are open, it logs all requests in the **Network** tool.</span></span>  
<span data-ttu-id="250f7-266">Use el panel Red para analizar las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="250f7-266">Use the Network panel to analyze requests.</span></span>  

### <a name="display-a-log-of-requests"></a><span data-ttu-id="250f7-267">Mostrar un registro de solicitudes</span><span class="sxs-lookup"><span data-stu-id="250f7-267">Display a log of requests</span></span>  

<span data-ttu-id="250f7-268">Use la tabla Solicitudes para mostrar un registro de todas las solicitudes realizadas mientras devTools se han abierto.</span><span class="sxs-lookup"><span data-stu-id="250f7-268">Use the Requests table to display a log of all requests made while DevTools have been open.</span></span>  <span data-ttu-id="250f7-269">Para mostrar más información sobre cada elemento, elija o mantenga el mouse en las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="250f7-269">To reveals more information about each item, choose or hover on requests.</span></span>  

:::image type="complex" source="../media/network-network-requests-table.msft.png" alt-text="La tabla Solicitudes" lightbox="../media/network-network-requests-table.msft.png":::
   <span data-ttu-id="250f7-271">La tabla Solicitudes</span><span class="sxs-lookup"><span data-stu-id="250f7-271">The Requests table</span></span>  
:::image-end:::  

<span data-ttu-id="250f7-272">La tabla Solicitudes muestra las siguientes columnas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="250f7-272">The Requests table displays the following columns by default.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-273">Nombre</span><span class="sxs-lookup"><span data-stu-id="250f7-273">Name</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-274">Nombre de archivo o identificador del recurso.</span><span class="sxs-lookup"><span data-stu-id="250f7-274">The filename of, or an identifier for, the resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-275">Estado</span><span class="sxs-lookup"><span data-stu-id="250f7-275">Status</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-276">El código de estado HTTP.</span><span class="sxs-lookup"><span data-stu-id="250f7-276">The HTTP status code.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-277">Tipo</span><span class="sxs-lookup"><span data-stu-id="250f7-277">Type</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-278">Tipo MIME del recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="250f7-278">The MIME type of the requested resource.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-279">Iniciador</span><span class="sxs-lookup"><span data-stu-id="250f7-279">Initiator</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-280">Los siguientes objetos o procesos inician solicitudes.</span><span class="sxs-lookup"><span data-stu-id="250f7-280">The following objects or processes initiate requests.</span></span>  
      
      *   <span data-ttu-id="250f7-281">**Analizador**  El analizador HTML para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="250f7-281">**Parser**  The HTML parser for Microsoft Edge.</span></span>  
      *   <span data-ttu-id="250f7-282">**Redirigir**  Redireccionamiento HTTP.</span><span class="sxs-lookup"><span data-stu-id="250f7-282">**Redirect**  An HTTP redirect.</span></span>  
      *   <span data-ttu-id="250f7-283">**Script**  Una función JavaScript.</span><span class="sxs-lookup"><span data-stu-id="250f7-283">**Script**  A JavaScript function.</span></span>  
      *   <span data-ttu-id="250f7-284">**Otros**  Otro proceso o acción, como navegar a una página mediante un vínculo o escribir una dirección URL en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="250f7-284">**Other**  Some other process or action, such as navigating to a page using a link or entering a URL in the address bar.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-285">Tamaño</span><span class="sxs-lookup"><span data-stu-id="250f7-285">Size</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-286">El tamaño combinado de los encabezados de respuesta más el cuerpo de la respuesta, según lo entregado por el servidor.</span><span class="sxs-lookup"><span data-stu-id="250f7-286">The combined size of the response headers plus the response body, as delivered by the server.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-287">Tiempo</span><span class="sxs-lookup"><span data-stu-id="250f7-287">Time</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-288">La duración total, desde el inicio de la solicitud hasta la recepción del byte final en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="250f7-288">The total duration, from the start of the request to the receipt of the final byte in the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="250f7-289">Cascada</span><span class="sxs-lookup"><span data-stu-id="250f7-289">Waterfall</span></span>](#display-the-timing-relationship-of-requests)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-290">Un desglose visual de la actividad de cada solicitud.</span><span class="sxs-lookup"><span data-stu-id="250f7-290">A visual breakdown of the activity for each request.</span></span>  
   :::column-end:::
:::row-end:::  

#### <a name="add-or-remove-columns"></a><span data-ttu-id="250f7-291">Agregar o quitar columnas</span><span class="sxs-lookup"><span data-stu-id="250f7-291">Add or remove columns</span></span>  

<span data-ttu-id="250f7-292">Mantenga el mouse en el encabezado de la tabla Solicitudes, abra el menú contextual \(hacer clic con el botón secundario\) y elija una opción para ocultarla o mostrarla.</span><span class="sxs-lookup"><span data-stu-id="250f7-292">Hover on the header of the Requests table, open the contextual menu \(right-click\), and choose an option to hide or show it.</span></span>  <span data-ttu-id="250f7-293">Las opciones mostradas actualmente tienen marcas de verificación junto a cada elemento.</span><span class="sxs-lookup"><span data-stu-id="250f7-293">Currently displayed options have checkmarks next to each item.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-column.msft.png" alt-text="Agregar una columna a la tabla Solicitudes" lightbox="../media/network-network-requests-add-column.msft.png":::
   <span data-ttu-id="250f7-295">Agregar una columna a la tabla Solicitudes</span><span class="sxs-lookup"><span data-stu-id="250f7-295">Add a column to the Requests table</span></span>  
:::image-end:::  

#### <a name="add-custom-columns"></a><span data-ttu-id="250f7-296">Agregar columnas personalizadas</span><span class="sxs-lookup"><span data-stu-id="250f7-296">Add custom columns</span></span>  

<span data-ttu-id="250f7-297">Para agregar una columna personalizada a la tabla Solicitudes, mantenga el mouse en el encabezado de la \*\*\*\* tabla Solicitudes, abra el menú contextual \(clic con el botón derecho\) y elija Encabezados de respuesta Administrar columnas de  >  **encabezado**.</span><span class="sxs-lookup"><span data-stu-id="250f7-297">To add a custom column to the Requests table, hover on the header of the Requests table, open the contextual menu \(right-click\), and choose **Response Headers** > **Manage Header Columns**.</span></span>  

:::image type="complex" source="../media/network-network-requests-add-custom.msft.png" alt-text="Agregar una columna personalizada a la tabla Solicitudes" lightbox="../media/network-network-requests-add-custom.msft.png":::
   <span data-ttu-id="250f7-299">Agregar una columna personalizada a la tabla Solicitudes</span><span class="sxs-lookup"><span data-stu-id="250f7-299">Add a custom column to the Requests table</span></span>  
:::image-end:::  

### <a name="display-the-timing-relationship-of-requests"></a><span data-ttu-id="250f7-300">Mostrar la relación de tiempo de las solicitudes</span><span class="sxs-lookup"><span data-stu-id="250f7-300">Display the timing relationship of requests</span></span>  

<span data-ttu-id="250f7-301">Use la cascada para mostrar las relaciones de tiempo de las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="250f7-301">Use the Waterfall to display the timing relationships of requests.</span></span>  
<span data-ttu-id="250f7-302">La organización predeterminada de la cascada usa la hora de inicio de las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="250f7-302">The default organization of the Waterfall uses the start time of the requests.</span></span>  
<span data-ttu-id="250f7-303">Por lo tanto, las solicitudes que están más lejos de la izquierda se iniciaron antes que las solicitudes que están más lejos de la derecha.</span><span class="sxs-lookup"><span data-stu-id="250f7-303">So, requests that are farther to the left started earlier than the requests that are farther to the right.</span></span>  

<span data-ttu-id="250f7-304">Para revisar las distintas formas de ordenar la cascada, vaya a [Ordenar por fase de actividad](#sort-by-activity-phase).</span><span class="sxs-lookup"><span data-stu-id="250f7-304">To review the different ways that you may sort the Waterfall, navigate to [Sort by activity phase](#sort-by-activity-phase).</span></span>  

:::image type="complex" source="../media/network-network-requests-waterfall.msft.png" alt-text="La columna Cascada del panel Solicitudes" lightbox="../media/network-network-requests-waterfall.msft.png":::
   <span data-ttu-id="250f7-306">La columna Cascada del **panel Solicitudes**</span><span class="sxs-lookup"><span data-stu-id="250f7-306">The Waterfall column of the **Requests** pane</span></span>  
:::image-end:::  

<!-- ### Analyze the frames of a WebSocket Connection  -->

<!--To review the frames of a WebSocket connection, use the following steps.  

1.  Choose the URL of the WebSocket connection, under the **Name** column of the Requests table.  
1.  Choose the **Frames** panel.  The table shows the last 100 frames.  

To refresh the table, re-choose the name of the WebSocket connection under the **Name** column of the Requests table.  -->

<!--
:::image type="complex" source="../media/network-frames.msft.png" alt-text="The Frames panel" lightbox="../media/network-frames.msft.png":::
   The **Frames** panel  
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

### <a name="display-a-preview-of-a-response-body"></a><span data-ttu-id="250f7-307">Mostrar una vista previa de un cuerpo de respuesta</span><span class="sxs-lookup"><span data-stu-id="250f7-307">Display a preview of a response body</span></span>  

<span data-ttu-id="250f7-308">Para mostrar una vista previa de un cuerpo de respuesta, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="250f7-308">To display a preview of a response body, use the following steps.</span></span>  

1.  <span data-ttu-id="250f7-309">Elija la dirección URL de la solicitud, en la **columna Nombre** de la tabla Solicitudes.</span><span class="sxs-lookup"><span data-stu-id="250f7-309">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="250f7-310">Elija el panel **Vista** previa.</span><span class="sxs-lookup"><span data-stu-id="250f7-310">Choose the **Preview** panel.</span></span>  

<span data-ttu-id="250f7-311">La pestaña Vista previa es principalmente útil para mostrar imágenes.</span><span class="sxs-lookup"><span data-stu-id="250f7-311">The Preview tab is mostly useful to display images.</span></span>  

:::image type="complex" source="../media/network-network-resources-preview.msft.png" alt-text="El panel Vista previa" lightbox="../media/network-network-resources-preview.msft.png":::
   <span data-ttu-id="250f7-313">El panel **Vista** previa</span><span class="sxs-lookup"><span data-stu-id="250f7-313">The **Preview** panel</span></span>  
:::image-end:::  

### <a name="display-a-response-body"></a><span data-ttu-id="250f7-314">Mostrar un cuerpo de respuesta</span><span class="sxs-lookup"><span data-stu-id="250f7-314">Display a response body</span></span>  

<span data-ttu-id="250f7-315">Para mostrar el cuerpo de la respuesta a una solicitud, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="250f7-315">To display the response body to a request, use the following steps.</span></span>  

1.  <span data-ttu-id="250f7-316">Elija la dirección URL de la solicitud, en la **columna Nombre** de la tabla Solicitudes.</span><span class="sxs-lookup"><span data-stu-id="250f7-316">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="250f7-317">Elija **el** panel Respuesta.</span><span class="sxs-lookup"><span data-stu-id="250f7-317">Choose the **Response** panel.</span></span>  

:::image type="complex" source="../media/network-network-resources-response.msft.png" alt-text="El panel Respuesta" lightbox="../media/network-network-resources-response.msft.png":::
   <span data-ttu-id="250f7-319">El panel **Respuesta**</span><span class="sxs-lookup"><span data-stu-id="250f7-319">The **Response** panel</span></span>  
:::image-end:::  

### <a name="display-http-headers"></a><span data-ttu-id="250f7-320">Mostrar encabezados HTTP</span><span class="sxs-lookup"><span data-stu-id="250f7-320">Display HTTP headers</span></span>  

<span data-ttu-id="250f7-321">Para mostrar datos de encabezado HTTP sobre una solicitud, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="250f7-321">To display HTTP header data about a request, use the following steps.</span></span>  

1.  <span data-ttu-id="250f7-322">Elija la dirección URL de la solicitud, en la **columna Nombre** de la tabla Solicitudes.</span><span class="sxs-lookup"><span data-stu-id="250f7-322">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="250f7-323">Elija el **psanel headers.**</span><span class="sxs-lookup"><span data-stu-id="250f7-323">Choose the **Headers** psanel.</span></span>  

:::image type="complex" source="../media/network-resources-headers.msft.png" alt-text="Panel Encabezados" lightbox="../media/network-resources-headers.msft.png":::
   <span data-ttu-id="250f7-325">Panel **Encabezados**</span><span class="sxs-lookup"><span data-stu-id="250f7-325">The **Headers** panel</span></span>  
:::image-end:::  

#### <a name="display-http-header-source"></a><span data-ttu-id="250f7-326">Mostrar origen de encabezado HTTP</span><span class="sxs-lookup"><span data-stu-id="250f7-326">Display HTTP header source</span></span>  

<span data-ttu-id="250f7-327">De forma predeterminada, el panel **Encabezados** muestra los nombres de encabezado alfabéticamente.</span><span class="sxs-lookup"><span data-stu-id="250f7-327">By default, the **Headers** panel shows header names alphabetically.</span></span>  <span data-ttu-id="250f7-328">Para dsiplay los nombres de encabezado HTTP en el orden recibido, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="250f7-328">To dsiplay the HTTP header names in the order received, use the following steps.</span></span>  

1.  <span data-ttu-id="250f7-329">Abra el panel **Encabezados** para la solicitud que le interese.</span><span class="sxs-lookup"><span data-stu-id="250f7-329">Open the **Headers** panel for the request that interests you.</span></span>  <span data-ttu-id="250f7-330">Para obtener más información, vaya [a Mostrar encabezados HTTP](#display-http-headers).</span><span class="sxs-lookup"><span data-stu-id="250f7-330">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="250f7-331">Elija **ver origen**, junto a la sección Encabezado de **solicitud** o Encabezado **de** respuesta.</span><span class="sxs-lookup"><span data-stu-id="250f7-331">Choose **view source**, next to the **Request Header** or **Response Header** section.</span></span>  

### <a name="display-query-string-parameters"></a><span data-ttu-id="250f7-332">Mostrar parámetros de cadena de consulta</span><span class="sxs-lookup"><span data-stu-id="250f7-332">Display query string parameters</span></span>  

<span data-ttu-id="250f7-333">Para mostrar los parámetros de cadena de consulta de una dirección URL en un formato legible, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="250f7-333">To display the query string parameters of a URL in a human-readable format, use the following steps.</span></span>  

1.  <span data-ttu-id="250f7-334">Abra el panel **Encabezados** para la solicitud que le interese.</span><span class="sxs-lookup"><span data-stu-id="250f7-334">Open the **Headers** panel for the request that interests you.</span></span>  <span data-ttu-id="250f7-335">Para obtener más información, vaya [a Mostrar encabezados HTTP](#display-http-headers).</span><span class="sxs-lookup"><span data-stu-id="250f7-335">For more information, navigate to [Display HTTP headers](#display-http-headers).</span></span>  
1.  <span data-ttu-id="250f7-336">Vaya a la **sección Parámetros de cadena de** consulta.</span><span class="sxs-lookup"><span data-stu-id="250f7-336">Navigate to the **Query String Parameters** section.</span></span>  

:::image type="complex" source="../media/network-network-resources-headers-query-string-parameters.msft.png" alt-text="Sección Parámetros de cadena de consulta" lightbox="../media/network-network-resources-headers-query-string-parameters.msft.png":::
   <span data-ttu-id="250f7-338">Sección **Parámetros de cadena de** consulta</span><span class="sxs-lookup"><span data-stu-id="250f7-338">The **Query String Parameters** section</span></span>  
:::image-end:::  

#### <a name="display-query-string-parameters-source"></a><span data-ttu-id="250f7-339">Mostrar origen de parámetros de cadena de consulta</span><span class="sxs-lookup"><span data-stu-id="250f7-339">Display query string parameters source</span></span>  

<span data-ttu-id="250f7-340">Para mostrar el origen del parámetro de cadena de consulta de una solicitud, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="250f7-340">To display the query string parameter source of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="250f7-341">Vaya a la sección Parámetros de cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="250f7-341">Navigate to the Query String Parameters section.</span></span>  <span data-ttu-id="250f7-342">Para obtener más información, vaya [a Mostrar parámetros de cadena de consulta](#display-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="250f7-342">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="250f7-343">Elija **ver origen**.</span><span class="sxs-lookup"><span data-stu-id="250f7-343">Choose **view source**.</span></span>  

#### <a name="display-url-encoded-query-string-parameters"></a><span data-ttu-id="250f7-344">Mostrar parámetros de cadena de consulta con codificación URL</span><span class="sxs-lookup"><span data-stu-id="250f7-344">Display URL-encoded query string parameters</span></span>  

<span data-ttu-id="250f7-345">Para mostrar parámetros de cadena de consulta en un formato legible, pero con codificaciones conservadas, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="250f7-345">To display query string parameters in a human-readable format, but with encodings preserved, use the following steps.</span></span>  

1.  <span data-ttu-id="250f7-346">Vaya a la sección Parámetros de cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="250f7-346">Navigate to the Query String Parameters section.</span></span>  <span data-ttu-id="250f7-347">Para obtener más información, vaya [a Mostrar parámetros de cadena de consulta](#display-query-string-parameters).</span><span class="sxs-lookup"><span data-stu-id="250f7-347">For more information, navigate to [Display query string parameters](#display-query-string-parameters).</span></span>  
1.  <span data-ttu-id="250f7-348">Elija **ver dirección URL codificada**.</span><span class="sxs-lookup"><span data-stu-id="250f7-348">Choose **view URL encoded**.</span></span>  

### <a name="display-cookies"></a><span data-ttu-id="250f7-349">Mostrar cookies</span><span class="sxs-lookup"><span data-stu-id="250f7-349">Display cookies</span></span>  

<span data-ttu-id="250f7-350">Para mostrar las cookies enviadas en el encabezado HTTP de una solicitud, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="250f7-350">To display the cookies sent in the HTTP header of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="250f7-351">Elija la dirección URL de la solicitud, en la **columna Nombre** de la tabla Solicitudes.</span><span class="sxs-lookup"><span data-stu-id="250f7-351">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="250f7-352">Elija el **panel Cookies.**</span><span class="sxs-lookup"><span data-stu-id="250f7-352">Choose the **Cookies** panel.</span></span>  

<!--For more information about each of the columns, navigate to [Fields][ManageDataCookiesFields].  -->  

<!--[ManageDataCookiesFields]: manage-data/cookies#fields  -->  
<!--TODO: add link when section is available -->  

:::image type="complex" source="../media/network-network-resources-cookies.msft.png" alt-text="El panel Cookies" lightbox="../media/network-network-resources-cookies.msft.png":::
   <span data-ttu-id="250f7-354">El panel Cookies</span><span class="sxs-lookup"><span data-stu-id="250f7-354">The Cookies panel</span></span>  
:::image-end:::  

### <a name="display-the-timing-breakdown-of-a-request"></a><span data-ttu-id="250f7-355">Mostrar el desglose de tiempo de una solicitud</span><span class="sxs-lookup"><span data-stu-id="250f7-355">Display the timing breakdown of a request</span></span>  

<span data-ttu-id="250f7-356">Para mostrar el desglose de tiempo de una solicitud, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="250f7-356">To display the timing breakdown of a request, use the following steps.</span></span>  

1.  <span data-ttu-id="250f7-357">Elija la dirección URL de la solicitud, en la **columna Nombre** de la tabla Solicitudes.</span><span class="sxs-lookup"><span data-stu-id="250f7-357">Choose the URL of the request, under the **Name** column of the Requests table.</span></span>  
1.  <span data-ttu-id="250f7-358">Elija \*\*\*\* el panel Temporización.</span><span class="sxs-lookup"><span data-stu-id="250f7-358">Choose the **Timing** panel.</span></span>  

<span data-ttu-id="250f7-359">Para obtener una forma más rápida de obtener acceso a los datos, vaya [a Vista previa de un desglose de tiempo.](#preview-a-timing-breakdown)</span><span class="sxs-lookup"><span data-stu-id="250f7-359">For a faster way to access the data, navigate to [Preview a timing breakdown](#preview-a-timing-breakdown).</span></span>  

<span data-ttu-id="250f7-360">Para obtener más información acerca de cada una de las fases que se pueden mostrar en el **panel** Temporización, vaya a Fases de desglose de [tiempo explicadas.](#timing-breakdown-phases-explained)</span><span class="sxs-lookup"><span data-stu-id="250f7-360">For more information about each of the phases that may be displayed in the **Timing** panel, navigate to [Timing breakdown phases explained](#timing-breakdown-phases-explained).</span></span>  

:::image type="complex" source="../media/network-network-resources-timing.msft.png" alt-text="El panel Temporización" lightbox="../media/network-network-resources-timing.msft.png":::
   <span data-ttu-id="250f7-362">El panel **Temporización**</span><span class="sxs-lookup"><span data-stu-id="250f7-362">The **Timing** panel</span></span>  
:::image-end:::  

<span data-ttu-id="250f7-363">Más información sobre cada una de las fases.</span><span class="sxs-lookup"><span data-stu-id="250f7-363">More information about each of the phases.</span></span>  

<span data-ttu-id="250f7-364">Para obtener más información acerca del acceso a la pantalla, vaya a Mostrar desglose [de tiempo.](#display-the-timing-breakdown-of-a-request)</span><span class="sxs-lookup"><span data-stu-id="250f7-364">For more information about accessing the display, navigate to [Display timing breakdown](#display-the-timing-breakdown-of-a-request).</span></span>  

#### <a name="preview-a-timing-breakdown"></a><span data-ttu-id="250f7-365">Obtener una vista previa de un desglose de tiempo</span><span class="sxs-lookup"><span data-stu-id="250f7-365">Preview a timing breakdown</span></span>  

<span data-ttu-id="250f7-366">Para mostrar una vista previa del desglose de tiempo de una solicitud, en la columna **Cascada** de la tabla Solicitudes, mantenga el mouse sobre la entrada de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="250f7-366">To display a preview of the timing breakdown of a request, in the **Waterfall** column of the Requests table, hover on the entry for the request.</span></span>  

<span data-ttu-id="250f7-367">Para obtener más información acerca de cómo obtener acceso a los datos sin mantener el mouse, vaya [a Mostrar el desglose de tiempo de una solicitud](#display-the-timing-breakdown-of-a-request).</span><span class="sxs-lookup"><span data-stu-id="250f7-367">For more information about how to access the data without hovering, navigate to [Display the timing breakdown of a request](#display-the-timing-breakdown-of-a-request).</span></span>  

:::image type="complex" source="../media/network-network-resources-waterfall-hover.msft.png" alt-text="> vista previa del desglose de tiempo de una solicitud" lightbox="../media/network-network-resources-waterfall-hover.msft.png":::
   <span data-ttu-id="250f7-369">Obtener una vista previa del desglose de tiempo de una solicitud</span><span class="sxs-lookup"><span data-stu-id="250f7-369">Preview the timing breakdown of a request</span></span>  
:::image-end:::  

#### <a name="timing-breakdown-phases-explained"></a><span data-ttu-id="250f7-370">Fases de desglose de tiempo explicadas</span><span class="sxs-lookup"><span data-stu-id="250f7-370">Timing breakdown phases explained</span></span>  

<span data-ttu-id="250f7-371">Más información sobre cada una de las fases que se pueden mostrar en el panel **De tiempo.**</span><span class="sxs-lookup"><span data-stu-id="250f7-371">More information about each of the phases that may display in the **Timing** panel.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-372">Cola</span><span class="sxs-lookup"><span data-stu-id="250f7-372">Queueing</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-373">El explorador pone en cola las solicitudes cuando se cumple cualquiera de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="250f7-373">The browser queues requests when any of the following are true.</span></span>  
      
      *   <span data-ttu-id="250f7-374">Existen solicitudes de mayor prioridad.</span><span class="sxs-lookup"><span data-stu-id="250f7-374">Higher priority requests exist.</span></span>  
      *   <span data-ttu-id="250f7-375">Seis conexiones TCP están abiertas para el mismo origen, que es el límite.</span><span class="sxs-lookup"><span data-stu-id="250f7-375">Six TCP connections are open for the same origin, which is the limit.</span></span>  <span data-ttu-id="250f7-376">Solo se aplica a HTTP/1.0 y HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="250f7-376">Applies to HTTP/1.0 and HTTP/1.1 only.</span></span>  
      *   <span data-ttu-id="250f7-377">El explorador asigna brevemente espacio en la memoria caché de disco.</span><span class="sxs-lookup"><span data-stu-id="250f7-377">The browser is briefly allocating space in the disk cache.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-378">Detenido</span><span class="sxs-lookup"><span data-stu-id="250f7-378">Stalled</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-379">La solicitud se detiene por cualquiera de los motivos descritos en **Queueing**.</span><span class="sxs-lookup"><span data-stu-id="250f7-379">The request is stalled for any of the reasons described in **Queueing**.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-380">Búsqueda DNS</span><span class="sxs-lookup"><span data-stu-id="250f7-380">DNS Lookup</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-381">El explorador está resolviendo la dirección IP de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="250f7-381">The browser is resolving the IP address for the request.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-382">Conexión inicial</span><span class="sxs-lookup"><span data-stu-id="250f7-382">Initial connection</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-383">El explorador establece una conexión que incluye protocolos de enlace TCP, reintentos TCP y negocia una capa de socket seguro.</span><span class="sxs-lookup"><span data-stu-id="250f7-383">The browser establishes a connection including TCP handshakes, TCP retries, and negotiates a Secure Socket Layer.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-384">Negociación de proxy</span><span class="sxs-lookup"><span data-stu-id="250f7-384">Proxy negotiation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-385">El explorador está negociando la solicitud con un [servidor proxy.][WikiProxyServer]</span><span class="sxs-lookup"><span data-stu-id="250f7-385">The browser is negotiating the request with a [proxy server][WikiProxyServer].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-386">Solicitud enviada</span><span class="sxs-lookup"><span data-stu-id="250f7-386">Request sent</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-387">Se envía la solicitud.</span><span class="sxs-lookup"><span data-stu-id="250f7-387">The request is being sent.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-388">Preparación de ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="250f7-388">ServiceWorker Preparation</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-389">El explorador está iniciando el trabajador del servicio.</span><span class="sxs-lookup"><span data-stu-id="250f7-389">The browser is starting the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-390">Solicitud a ServiceWorker</span><span class="sxs-lookup"><span data-stu-id="250f7-390">Request to ServiceWorker</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-391">La solicitud se envía al trabajador del servicio.</span><span class="sxs-lookup"><span data-stu-id="250f7-391">The request is being sent to the service worker.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-392">Waiting \(TTFB\)</span><span class="sxs-lookup"><span data-stu-id="250f7-392">Waiting \(TTFB\)</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-393">El explorador está esperando el primer byte de una respuesta.</span><span class="sxs-lookup"><span data-stu-id="250f7-393">The browser is waiting for the first byte of a response.</span></span>  <span data-ttu-id="250f7-394">TTFB significa Time To First Byte.</span><span class="sxs-lookup"><span data-stu-id="250f7-394">TTFB stands for Time To First Byte.</span></span>  <span data-ttu-id="250f7-395">Este tiempo incluye un recorrido de ida y vuelta de latencia y el tiempo que el servidor tardó en preparar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="250f7-395">This timing includes one round trip of latency and the time the server took to prepare the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-396">Descarga de contenido</span><span class="sxs-lookup"><span data-stu-id="250f7-396">Content Download</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-397">El explorador recibe la respuesta.</span><span class="sxs-lookup"><span data-stu-id="250f7-397">The browser is receiving the response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-398">Recepción de inserción</span><span class="sxs-lookup"><span data-stu-id="250f7-398">Receiving Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-399">El explorador está recibiendo datos para esta respuesta a través de HTTP/2 Server Push.</span><span class="sxs-lookup"><span data-stu-id="250f7-399">The browser is receiving data for this response via HTTP/2 Server Push.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="250f7-400">Inserción de lectura</span><span class="sxs-lookup"><span data-stu-id="250f7-400">Reading Push</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="250f7-401">El explorador está leyendo los datos locales recibidos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="250f7-401">The browser is reading the local data previously received.</span></span>  
   :::column-end:::
:::row-end:::  

### <a name="display-initiators-and-dependencies"></a><span data-ttu-id="250f7-402">Mostrar iniciadores y dependencias</span><span class="sxs-lookup"><span data-stu-id="250f7-402">Display initiators and dependencies</span></span>  

<span data-ttu-id="250f7-403">Para mostrar los iniciadores y las dependencias de una solicitud, mantenga y mantenga el mouse sobre la solicitud `Shift` en la tabla Solicitudes.</span><span class="sxs-lookup"><span data-stu-id="250f7-403">To display the initiators and dependencies of a request, hold `Shift`and hover on the request in the Requests table.</span></span>  <span data-ttu-id="250f7-404">Colores de DevTools: los iniciadores se muestran en verde y las dependencias se muestran en rojo.</span><span class="sxs-lookup"><span data-stu-id="250f7-404">DevTools colors: initiators are shown in green and dependencies are shown in red.</span></span>  

:::image type="complex" source="../media/network-network-resources-initiators-dependencies.msft.png" alt-text="Mostrar los iniciadores y las dependencias de una solicitud" lightbox="../media/network-network-resources-initiators-dependencies.msft.png":::
   <span data-ttu-id="250f7-406">Mostrar los iniciadores y las dependencias de una solicitud</span><span class="sxs-lookup"><span data-stu-id="250f7-406">Display the initiators and dependencies of a request</span></span>  
:::image-end:::  

<span data-ttu-id="250f7-407">Cuando la tabla Solicitudes se ordena cronológicamente, si mantiene el mouse en una línea, la línea anterior muestra una solicitud verde.</span><span class="sxs-lookup"><span data-stu-id="250f7-407">When the Requests table is ordered chronologically, if you hover on a line, the line preceding it displays a green request.</span></span>  <span data-ttu-id="250f7-408">La solicitud verde es el iniciador de la dependencia.</span><span class="sxs-lookup"><span data-stu-id="250f7-408">The green request is the initiator of the dependency.</span></span>  <span data-ttu-id="250f7-409">Si se muestra otra solicitud verde en la línea anterior, esa solicitud superior es el iniciador del iniciador.</span><span class="sxs-lookup"><span data-stu-id="250f7-409">If another green request is displayed on the line before that, that higher request is the initiator of the initiator.</span></span>  <span data-ttu-id="250f7-410">Etcétera.</span><span class="sxs-lookup"><span data-stu-id="250f7-410">And so on.</span></span>  

### <a name="display-load-events"></a><span data-ttu-id="250f7-411">Mostrar eventos de carga</span><span class="sxs-lookup"><span data-stu-id="250f7-411">Display load events</span></span>  

<span data-ttu-id="250f7-412">DevTools muestra el tiempo de los `DOMContentLoaded` eventos y en varios lugares de la herramienta `load` **Red.**</span><span class="sxs-lookup"><span data-stu-id="250f7-412">DevTools displays the timing of the `DOMContentLoaded` and `load` events in multiple places on the **Network** tool.</span></span>  <span data-ttu-id="250f7-413">El `DOMContentLoaded` evento tiene un color azul y el evento es `load` rojo.</span><span class="sxs-lookup"><span data-stu-id="250f7-413">The `DOMContentLoaded` event is colored blue, and the `load` event is red.</span></span>  

:::image type="complex" source="../media/network-network-requests-load-events.msft.png" alt-text="Ubicaciones de los eventos DOMContentLoaded y load en el panel Red" lightbox="../media/network-network-requests-load-events.msft.png":::
   <span data-ttu-id="250f7-415">Ubicaciones de los `DOMContentLoaded` eventos y en la herramienta `load` **Red**</span><span class="sxs-lookup"><span data-stu-id="250f7-415">The locations of the `DOMContentLoaded` and `load` events on the **Network** tool</span></span>  
:::image-end:::  

### <a name="display-the-total-number-of-requests"></a><span data-ttu-id="250f7-416">Mostrar el número total de solicitudes</span><span class="sxs-lookup"><span data-stu-id="250f7-416">Display the total number of requests</span></span>  

<span data-ttu-id="250f7-417">El número total de solicitudes se muestra en el **panel Resumen,** en la parte inferior de la **herramienta Red.**</span><span class="sxs-lookup"><span data-stu-id="250f7-417">The total number of requests is listed in the **Summary** pane, at the bottom of the **Network** tool.</span></span>  

> [!CAUTION]
> <span data-ttu-id="250f7-418">Este número solo realiza un seguimiento de las solicitudes que se han registrado desde que se abrió DevTools.</span><span class="sxs-lookup"><span data-stu-id="250f7-418">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="250f7-419">Si se produjeron otras solicitudes antes de abrir DevTools, estas solicitudes no se cuentan.</span><span class="sxs-lookup"><span data-stu-id="250f7-419">If other requests occurred before DevTools was opened, those requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-requests.msft.png" alt-text="El número total de solicitudes desde que Se abrieron DevTools" lightbox="../media/network-network-total-requests.msft.png":::
   <span data-ttu-id="250f7-421">El número total de solicitudes desde que Se abrieron DevTools</span><span class="sxs-lookup"><span data-stu-id="250f7-421">The total number of requests since DevTools were opened</span></span>  
:::image-end:::  

### <a name="display-the-total-download-size"></a><span data-ttu-id="250f7-422">Mostrar el tamaño total de descarga</span><span class="sxs-lookup"><span data-stu-id="250f7-422">Display the total download size</span></span>  

<span data-ttu-id="250f7-423">El tamaño total de descarga de las solicitudes se muestra en el **panel Resumen,** en la parte inferior de la **herramienta Red.**</span><span class="sxs-lookup"><span data-stu-id="250f7-423">The total download size of requests is listed in the **Summary** pane, at the bottom of the **Network** tool.</span></span>  

> [!CAUTION]
> <span data-ttu-id="250f7-424">Este número solo realiza un seguimiento de las solicitudes que se han registrado desde que se abrió DevTools.</span><span class="sxs-lookup"><span data-stu-id="250f7-424">This number only tracks requests that have been logged since DevTools was opened.</span></span>  <span data-ttu-id="250f7-425">Si se produjeron otras solicitudes antes de abrir DevTools, las solicitudes anteriores no se cuentan.</span><span class="sxs-lookup"><span data-stu-id="250f7-425">If other requests occurred before DevTools was opened, the previous requests are not counted.</span></span>  

:::image type="complex" source="../media/network-network-total-download-size.msft.png" alt-text="El tamaño total de descarga de las solicitudes" lightbox="../media/network-network-total-download-size.msft.png":::
   <span data-ttu-id="250f7-427">El tamaño total de descarga de las solicitudes</span><span class="sxs-lookup"><span data-stu-id="250f7-427">The total download size of requests</span></span>  
:::image-end:::  

<span data-ttu-id="250f7-428">Para comprobar el tamaño de los recursos grandes después de que el explorador descomprime cada elemento, navegue para mostrar el tamaño sin [comprimir de un recurso](#display-the-uncompressed-size-of-a-resource).</span><span class="sxs-lookup"><span data-stu-id="250f7-428">To verify how large resources are after the browser uncompresses each item, navigate to [display the uncompressed size of a resource](#display-the-uncompressed-size-of-a-resource).</span></span>  

### <a name="display-the-stack-trace-that-caused-a-request"></a><span data-ttu-id="250f7-429">Mostrar el seguimiento de pila que causó una solicitud</span><span class="sxs-lookup"><span data-stu-id="250f7-429">Display the stack trace that caused a request</span></span>  

<span data-ttu-id="250f7-430">Después de que una instrucción JavaScript solicite un recurso, mantenga el mouse en la columna **Iniciador** para mostrar el seguimiento de la pila que conduce a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="250f7-430">After a JavaScript statement requests a resource, hover on the **Initiator** column to display the stack trace leading up to the request.</span></span>  

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

:::image type="complex" source="../media/network-network-requests-initiator-stack.msft.png" alt-text="Seguimiento de pila que conduce a una solicitud de recurso" lightbox="../media/network-network-requests-initiator-stack.msft.png":::
   <span data-ttu-id="250f7-432">Seguimiento de pila que conduce a una solicitud de recurso</span><span class="sxs-lookup"><span data-stu-id="250f7-432">The stack trace leading up to a resource request</span></span>  
:::image-end:::  

### <a name="display-the-uncompressed-size-of-a-resource"></a><span data-ttu-id="250f7-433">Mostrar el tamaño sin comprimir de un recurso</span><span class="sxs-lookup"><span data-stu-id="250f7-433">Display the uncompressed size of a resource</span></span>  

<span data-ttu-id="250f7-434">Active la casilla **Usar filas de solicitud grandes** y, a continuación, revise el valor inferior de la **columna** Tamaño.</span><span class="sxs-lookup"><span data-stu-id="250f7-434">Turn on the **Use large request rows** checkbox and then review the bottom value of the **Size** column.</span></span>  

:::image type="complex" source="../media/network-network-requests-uncompressed-compare.msft.png" alt-text="Un ejemplo de recursos sin comprimir" lightbox="../media/network-network-requests-uncompressed-compare.msft.png":::
   <span data-ttu-id="250f7-436">Un ejemplo de recursos sin comprimir \(El tamaño comprimido del archivo que se envió a través de la red era , mientras que el tamaño sin comprimir `jquery-3.3.1.min.js` `29.9 KB` era `84.9 KB` \)</span><span class="sxs-lookup"><span data-stu-id="250f7-436">An example of uncompressed resources  \(The compressed size of the `jquery-3.3.1.min.js` file that was sent over the network was `29.9 KB`, whereas the uncompressed size was `84.9 KB`\)</span></span>  
:::image-end:::  

## <a name="export-requests-data"></a><span data-ttu-id="250f7-437">Exportar datos de solicitudes</span><span class="sxs-lookup"><span data-stu-id="250f7-437">Export requests data</span></span>  

### <a name="save-all-network-requests-to-a-har-file"></a><span data-ttu-id="250f7-438">Guardar todas las solicitudes de red en un archivo HAR</span><span class="sxs-lookup"><span data-stu-id="250f7-438">Save all network requests to a HAR file</span></span>  

<span data-ttu-id="250f7-439">Para guardar todas las solicitudes de red en un archivo HAR, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="250f7-439">To save all network requests to a HAR file, complete the following steps.</span></span>  

1.  <span data-ttu-id="250f7-440">Mantenga el mouse sobre cualquier solicitud de la tabla Solicitudes y abra el menú contextual \(hacer clic con el botón secundario\).</span><span class="sxs-lookup"><span data-stu-id="250f7-440">Hover on any request in the Requests table and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="250f7-441">Elija **Guardar como HAR con contenido**.</span><span class="sxs-lookup"><span data-stu-id="250f7-441">Choose **Save as HAR with Content**.</span></span>  <span data-ttu-id="250f7-442">DevTools guarda todas las solicitudes que se han producido desde que abrió DevTools en el archivo HAR.</span><span class="sxs-lookup"><span data-stu-id="250f7-442">DevTools saves all requests that have occurred since you opened DevTools to the HAR file.</span></span>  <span data-ttu-id="250f7-443">No puede filtrar solicitudes.</span><span class="sxs-lookup"><span data-stu-id="250f7-443">You are not able to filter requests.</span></span>  <span data-ttu-id="250f7-444">Tampoco puede guardar una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="250f7-444">You are also not able to save a single request.</span></span>  

<span data-ttu-id="250f7-445">Una vez guardado un archivo HAR, puede volver a importarlo en DevTools para su análisis.</span><span class="sxs-lookup"><span data-stu-id="250f7-445">Once you save a HAR file, you may import it back into DevTools for analysis.</span></span>  <span data-ttu-id="250f7-446">Basta con arrastrar y colocar el archivo HAR en la tabla Solicitudes.</span><span class="sxs-lookup"><span data-stu-id="250f7-446">Just drag-and-drop the HAR file into the Requests table.</span></span>  
<!--For more information, navigate to also [HAR Analyzer][HARAnalyzer].  -->  

<!--[HARAnalyzer]: https://toolbox.alphabetapps.com/apps/har_analyzer  -->  
<!--Todo: add section link when content is available  -->  

:::image type="complex" source="../media/network-network-requests-save-har-content.msft.png" alt-text="Elija Guardar como HAR con contenido" lightbox="../media/network-network-requests-save-har-content.msft.png":::
   <span data-ttu-id="250f7-448">Elija **Guardar como HAR con contenido**</span><span class="sxs-lookup"><span data-stu-id="250f7-448">Choose **Save as HAR with Content**</span></span>  
:::image-end:::  

### <a name="copy-one-or-more-requests-to-the-clipboard"></a><span data-ttu-id="250f7-449">Copiar una o más solicitudes en el Portapapeles</span><span class="sxs-lookup"><span data-stu-id="250f7-449">Copy one or more requests to the clipboard</span></span>  

<span data-ttu-id="250f7-450">En la **columna Nombre** de la tabla Solicitudes, mantenga el mouse en una solicitud, abra el menú contextual \(clic con el botón derecho\), mantenga el mouse en **Copiar**y elija una de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="250f7-450">Under the **Name** column of the Requests table, hover on a request, open the contextual menu \(right-click\), hover on **Copy**, and choose one of the following options.</span></span>  

| <span data-ttu-id="250f7-451">Nombre</span><span class="sxs-lookup"><span data-stu-id="250f7-451">Name</span></span> | <span data-ttu-id="250f7-452">Detalles</span><span class="sxs-lookup"><span data-stu-id="250f7-452">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="250f7-453">Copiar dirección de vínculo</span><span class="sxs-lookup"><span data-stu-id="250f7-453">Copy Link Address</span></span>** | <span data-ttu-id="250f7-454">Copie la dirección URL de la solicitud en el Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="250f7-454">Copy the URL of the request to the clipboard.</span></span> |  
| **<span data-ttu-id="250f7-455">Copiar respuesta</span><span class="sxs-lookup"><span data-stu-id="250f7-455">Copy Response</span></span>** | <span data-ttu-id="250f7-456">Copie el cuerpo de la respuesta en el Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="250f7-456">Copy the response body to the clipboard.</span></span> |  
| **<span data-ttu-id="250f7-457">Copiar como captura</span><span class="sxs-lookup"><span data-stu-id="250f7-457">Copy as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="250f7-458">Copiar como cURL</span><span class="sxs-lookup"><span data-stu-id="250f7-458">Copy as cURL</span></span>** | <span data-ttu-id="250f7-459">Copie la solicitud como un comando cURL.</span><span class="sxs-lookup"><span data-stu-id="250f7-459">Copy the request as a cURL command.</span></span> |  
| **<span data-ttu-id="250f7-460">Copiar todo como captura</span><span class="sxs-lookup"><span data-stu-id="250f7-460">Copy All as Fetch</span></span>** | &nbsp; |  
| **<span data-ttu-id="250f7-461">Copiar todo como cURL</span><span class="sxs-lookup"><span data-stu-id="250f7-461">Copy All as cURL</span></span>** | <span data-ttu-id="250f7-462">Copie todas las solicitudes como una cadena de comandos cURL.</span><span class="sxs-lookup"><span data-stu-id="250f7-462">Copy all requests as a chain of cURL commands.</span></span> |  
| **<span data-ttu-id="250f7-463">Copiar todo como HAR</span><span class="sxs-lookup"><span data-stu-id="250f7-463">Copy All as HAR</span></span>** | <span data-ttu-id="250f7-464">Copie todas las solicitudes como datos de HAR.</span><span class="sxs-lookup"><span data-stu-id="250f7-464">Copy all requests as HAR data.</span></span> |  

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

:::image type="complex" source="../media/network-network-requests-copy-response.msft.png" alt-text="Elegir copiar respuesta" lightbox="../media/network-network-requests-copy-response.msft.png":::
   <span data-ttu-id="250f7-466">Elegir **copiar respuesta**</span><span class="sxs-lookup"><span data-stu-id="250f7-466">Choose **Copy Response**</span></span>  
:::image-end:::  

### <a name="copy-formatted-response-json-to-the-clipboard"></a><span data-ttu-id="250f7-467">Copiar JSON de respuesta con formato en el Portapapeles</span><span class="sxs-lookup"><span data-stu-id="250f7-467">Copy formatted response JSON to the clipboard</span></span>  

<span data-ttu-id="250f7-468">Elija una solicitud de red y vaya al **panel Encabezados.**</span><span class="sxs-lookup"><span data-stu-id="250f7-468">Choose a network request and navigate to the **Headers** pane.</span></span>  <span data-ttu-id="250f7-469">Para copiar el valor JSON de una respuesta, vaya a Carga de solicitud **,** mantenga el mouse en el contenido de la respuesta JSON, abra el menú contextual \(haga clic con el botón secundario en\) y elija **Copiar valor**.</span><span class="sxs-lookup"><span data-stu-id="250f7-469">To copy the JSON value of a response, navigate to **Request payload**, hover on the JSON response content, open the contextual menu \(right-click\), and choose **Copy Value**.</span></span>  

:::row:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-copy-property-value.msft.png" alt-text="Copiar valor en el menú contextual" lightbox="../media/network-header-copy-property-value.msft.png":::
          <span data-ttu-id="250f7-471">**Copiar valor** en el menú contextual</span><span class="sxs-lookup"><span data-stu-id="250f7-471">**Copy Value** in contextual menu</span></span>  
        :::image-end:::  
   :::column-end:::
   :::column span="":::
        :::image type="complex" source="../media/network-header-paste-property-value.msft.png" alt-text="Microsoft Visual Studio Código con JSON de respuesta con formato" lightbox="../media/network-header-paste-property-value.msft.png":::
          <span data-ttu-id="250f7-473">Pegar JSON de respuesta con formato en Microsoft Visual Studio código</span><span class="sxs-lookup"><span data-stu-id="250f7-473">Pasting formatted response JSON in Microsoft Visual Studio Code</span></span>  
        :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="copy-property-values-from-network-requests-to-your-clipboard"></a><span data-ttu-id="250f7-474">Copiar valores de propiedad de solicitudes de red en el Portapapeles</span><span class="sxs-lookup"><span data-stu-id="250f7-474">Copy property values from network requests to your clipboard</span></span>  

<span data-ttu-id="250f7-475">Para copiar valores de propiedad de solicitudes de red en el Portapapeles, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="250f7-475">To copy property values from network requests to your clipboard, complete the following actions.</span></span>  

1.  <span data-ttu-id="250f7-476">Abra el **panel Encabezados.**</span><span class="sxs-lookup"><span data-stu-id="250f7-476">Open the **Headers** pane.</span></span>  
1.  <span data-ttu-id="250f7-477">Abra una de las siguientes secciones de encabezado.</span><span class="sxs-lookup"><span data-stu-id="250f7-477">Open one of the following header sections.</span></span>  
    *   <span data-ttu-id="250f7-478">Carga de solicitud \(JSON\)</span><span class="sxs-lookup"><span data-stu-id="250f7-478">Request payload \(JSON\)</span></span>  
    *   <span data-ttu-id="250f7-479">Datos del formulario</span><span class="sxs-lookup"><span data-stu-id="250f7-479">Form Data</span></span>  
    *   <span data-ttu-id="250f7-480">Parámetros de cadena de consulta</span><span class="sxs-lookup"><span data-stu-id="250f7-480">Query String Parameters</span></span>  
    *   <span data-ttu-id="250f7-481">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="250f7-481">Request Headers</span></span>  
    *   <span data-ttu-id="250f7-482">Encabezados de respuesta</span><span class="sxs-lookup"><span data-stu-id="250f7-482">Response Headers</span></span>  
1.  <span data-ttu-id="250f7-483">Abra el menú contextual \(clic con el botón secundario\) > **Valor de copia**.</span><span class="sxs-lookup"><span data-stu-id="250f7-483">Open the contextual menu \(right-click\) > **Copy value**.</span></span>  <span data-ttu-id="250f7-484">Ahora puede pegar el valor en cualquier editor para revisarlo.</span><span class="sxs-lookup"><span data-stu-id="250f7-484">You may now paste the value into any editor to review it.</span></span>  
    
## <a name="change-the-layout-of-the-network-panel"></a><span data-ttu-id="250f7-485">Cambiar el diseño del panel Red</span><span class="sxs-lookup"><span data-stu-id="250f7-485">Change the layout of the Network panel</span></span>  

<span data-ttu-id="250f7-486">Puedes expandir o contraer secciones de la interfaz de usuario de la herramienta **de** red para centrar información importante.</span><span class="sxs-lookup"><span data-stu-id="250f7-486">You may expand or collapse sections of the **Network** tool UI to focus important information.</span></span>  

### <a name="hide-the-filters-pane"></a><span data-ttu-id="250f7-487">Ocultar el panel Filtros</span><span class="sxs-lookup"><span data-stu-id="250f7-487">Hide the Filters pane</span></span>  

<span data-ttu-id="250f7-488">De forma predeterminada, DevTools muestra el **panel Filtros.**</span><span class="sxs-lookup"><span data-stu-id="250f7-488">By default, DevTools show the **Filters** pane.</span></span>  
<span data-ttu-id="250f7-489">Elija **Filtro** \( ![ Filtro ](../media/filter-icon.msft.png) \) para ocultarlo.</span><span class="sxs-lookup"><span data-stu-id="250f7-489">Choose **Filter** \(![Filter](../media/filter-icon.msft.png)\) to hide it.</span></span>  

:::image type="complex" source="../media/network-network-resources-hide-filters-button.msft.png" alt-text="El botón Ocultar filtros" lightbox="../media/network-network-resources-hide-filters-button.msft.png":::
   <span data-ttu-id="250f7-491">El botón Ocultar filtros</span><span class="sxs-lookup"><span data-stu-id="250f7-491">The Hide Filters button</span></span>  
:::image-end:::  

### <a name="use-large-request-rows"></a><span data-ttu-id="250f7-492">Usar filas de solicitud grandes</span><span class="sxs-lookup"><span data-stu-id="250f7-492">Use large request rows</span></span>  

<span data-ttu-id="250f7-493">Use filas grandes cuando desee más espacios en blanco en la tabla de solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="250f7-493">Use large rows when you want more whitespace in your network requests table.</span></span>  <span data-ttu-id="250f7-494">Algunas columnas también proporcionan un poco más de información al usar filas grandes.</span><span class="sxs-lookup"><span data-stu-id="250f7-494">Some columns also provide a little more information when using large rows.</span></span>  <span data-ttu-id="250f7-495">Por ejemplo, el valor inferior de la **columna Size** es el tamaño sin comprimir de una solicitud.</span><span class="sxs-lookup"><span data-stu-id="250f7-495">For example, the bottom value of the **Size** column is the uncompressed size of a request.</span></span>  

:::image type="complex" source="../media/network-network-requests-large-request-rows.msft.png" alt-text="Un ejemplo de filas de solicitudes grandes en el panel Solicitudes" lightbox="../media/network-network-requests-large-request-rows.msft.png":::
   <span data-ttu-id="250f7-497">Un ejemplo de filas de solicitudes grandes en el **panel Solicitudes**</span><span class="sxs-lookup"><span data-stu-id="250f7-497">An example of large request rows in the **Requests** pane</span></span>  
:::image-end:::  

<span data-ttu-id="250f7-498">Para habilitar filas grandes, active la casilla **Usar filas de solicitud grandes.**</span><span class="sxs-lookup"><span data-stu-id="250f7-498">To enable large rows, turn on the **Use large request rows** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-use-large-request-rows-on.msft.png" alt-text="Casilla Usar filas de solicitud grandes" lightbox="../media/network-network-requests-use-large-request-rows-on.msft.png":::
   <span data-ttu-id="250f7-500">Casilla **Usar filas de solicitud grandes**</span><span class="sxs-lookup"><span data-stu-id="250f7-500">The **Use large request rows** checkbox</span></span>  
:::image-end:::  

### <a name="hide-the-overview-pane"></a><span data-ttu-id="250f7-501">Ocultar el panel Información general</span><span class="sxs-lookup"><span data-stu-id="250f7-501">Hide the Overview pane</span></span>  

<span data-ttu-id="250f7-502">De forma predeterminada, DevTools muestra el **panel Información** general.</span><span class="sxs-lookup"><span data-stu-id="250f7-502">By default, DevTools displays the **Overview** pane.</span></span>  <span data-ttu-id="250f7-503">Para ocultarlo, desactiva la casilla **Mostrar información general.**</span><span class="sxs-lookup"><span data-stu-id="250f7-503">To hide it, turn off the **Show Overview** checkbox.</span></span>  

:::image type="complex" source="../media/network-network-requests-show-overview-off.msft.png" alt-text="Casilla Mostrar información general" lightbox="../media/network-network-requests-show-overview-off.msft.png":::
   <span data-ttu-id="250f7-505">Casilla **Mostrar información general**</span><span class="sxs-lookup"><span data-stu-id="250f7-505">The **Show Overview** checkbox</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="250f7-506">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="250f7-506">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsProgressiveWebApps]: ../progressive-web-apps/index.md "Depurar aplicaciones web progresivas | Microsoft Docs"  

<!--[NetworkConditions]: /microsoft-edge/devtools-guide-chromium/network/network-conditions "Optimize Performance Under Varying Network Conditions | Microsoft Docs"  -->  

[MDNHTTPDataURIs]: https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/Data_URIs "Direcciones URL de datos | MDN"  

[WikiProxyServer]: https://en.wikipedia.org/wiki/Proxy_server "Servidor proxy- Wikipedia"  

> [!NOTE]
> <span data-ttu-id="250f7-510">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="250f7-510">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="250f7-511">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/network/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="250f7-511">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="250f7-513">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="250f7-513">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

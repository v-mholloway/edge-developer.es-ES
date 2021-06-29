---
description: Características de depuración de cuadrícula CSS, solicitudes de edición y reproducción con la consola de red y mucho más.
title: Novedades de DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 65a3fb4da235d2330bf9205b7a4a79a999559ca4
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624804"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-85"></a><span data-ttu-id="97033-104">Novedades de DevTools (Microsoft Edge 85)</span><span class="sxs-lookup"><span data-stu-id="97033-104">What's New In DevTools (Microsoft Edge 85)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="97033-105">Anuncios del equipo Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="97033-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="97033-106">Las siguientes secciones son una lista de anuncios que puede haber perdido del equipo Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="97033-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="97033-107">Echa un vistazo a los anuncios para probar nuevas características en DevTools, Microsoft Visual Studio code extensions y mucho más.</span><span class="sxs-lookup"><span data-stu-id="97033-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="97033-108">Para mantenerse al día de todas las características más recientes y más importantes de las herramientas para desarrolladores, descargue los canales de vista previa de Microsoft Edge y siga el equipo [de DevTools][EdgeDevToolsTwitterAccount]de [Microsoft Edge][MicrosoftEdgePreviewChannels] en Twitter .</span><span class="sxs-lookup"><span data-stu-id="97033-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow the Microsoft Edge DevTools team on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="css-grid-debugging-features"></a><span data-ttu-id="97033-109">Características de depuración de cuadrícula CSS</span><span class="sxs-lookup"><span data-stu-id="97033-109">CSS grid debugging features</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="97033-111">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="97033-111">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="97033-112">El Microsoft Edge de DevTools colabora con el equipo de Chrome DevTools y la comunidad de Chromium para agregar nuevas características de depuración de cuadrícula CSS a DevTools.</span><span class="sxs-lookup"><span data-stu-id="97033-112">The Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new CSS grid debugging features to DevTools.</span></span>  <span data-ttu-id="97033-113">Ahora puede mostrar números de línea de cuadrícula, espacios de cuadrícula y líneas de cuadrícula extendidas como una superposición en la página.</span><span class="sxs-lookup"><span data-stu-id="97033-113">You are now able to display grid line numbers, grid gaps, and extended grid lines as an on-page overlay.</span></span>  <span data-ttu-id="97033-114">Además, próximamente se realizarán más mejoras en las herramientas de cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="97033-114">Plus, more improvements to the grid tools are coming soon.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Características de depuración de cuadrícula CSS" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   <span data-ttu-id="97033-116">Características de depuración de cuadrícula CSS</span><span class="sxs-lookup"><span data-stu-id="97033-116">CSS grid debugging features</span></span>
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="97033-117">Para habilitar el experimento, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOn] y active la casilla situada junto a Habilitar nuevas características **de depuración de cuadrícula CSS**.</span><span class="sxs-lookup"><span data-stu-id="97033-117">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable new CSS Grid debugging features**.</span></span>  
> 
> <span data-ttu-id="97033-118">Para probar el experimento con un ejemplo, vaya al ejemplo [del planificador de cuadrícula CSS][CodepenRachelweilYzwBzKM].</span><span class="sxs-lookup"><span data-stu-id="97033-118">To try out the experiment with a sample, navigate to [CSS Grid planner example][CodepenRachelweilYzwBzKM].</span></span>  

<span data-ttu-id="97033-119">Chromium problema [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="97033-119">Chromium issue [#1047356][CR1047356]</span></span>  

### <a name="edit-and-replay-requests-with-the-network-console"></a><span data-ttu-id="97033-120">Editar y reproducir solicitudes con la consola de red</span><span class="sxs-lookup"><span data-stu-id="97033-120">Edit and Replay requests with the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="97033-122">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="97033-122">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="97033-123">Ahora puede usar Editar **y** reproducir en solicitudes en el registro de red [mediante][DevtoolsNetworkIndexLogActivity] la consola de **red.**</span><span class="sxs-lookup"><span data-stu-id="97033-123">You are now able to use **Edit and Replay** on requests in the [Network Log][DevtoolsNetworkIndexLogActivity] using the **Network Console**.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Editar y reproducir una solicitud en networklog con la consola de red" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   <span data-ttu-id="97033-125">Editar y reproducir una solicitud en [networklog][DevtoolsNetworkIndexLogActivity] con la **consola de red**</span><span class="sxs-lookup"><span data-stu-id="97033-125">Edit and Replay a request in the [NetworkLog][DevtoolsNetworkIndexLogActivity] with the **Network Console**</span></span>  
:::image-end:::  

<span data-ttu-id="97033-126">Un nuevo panel, la **consola de** red se abre en el cajón [DevTools][DevtoolsCustomizeIndexDrawer] y se rellena automáticamente con información para la solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="97033-126">A new panel, the **Network Console** opens in the [DevTools Drawer][DevtoolsCustomizeIndexDrawer] and automatically populates with information for the HTTP request.</span></span>  <span data-ttu-id="97033-127">Para mostrar la respuesta devuelta desde el servidor, edite la solicitud \(si es necesario\) y seleccione **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="97033-127">To display the response returned from the server, edit the request \(if needed\) and select **Send**.</span></span>  

<span data-ttu-id="97033-128">También puede usar la consola **de red** para crear y enviar solicitudes HTTP directamente desde DevTools.</span><span class="sxs-lookup"><span data-stu-id="97033-128">You may also use the **Network Console** to create and send HTTP requests directly from the DevTools.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Panel consola de red" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   <span data-ttu-id="97033-130">Panel **consola de red**</span><span class="sxs-lookup"><span data-stu-id="97033-130">The **Network Console** panel</span></span>  
:::image-end:::  

> [!TIP]
> <span data-ttu-id="97033-131">Para mostrar **la Consola de** red en el panel principal \(top\) en lugar del cajón [DevTools][DevtoolsCustomizeIndexDrawer], vaya a herramientas de movimiento [entre paneles](#move-tools-between-panels).</span><span class="sxs-lookup"><span data-stu-id="97033-131">To display **Network Console** in the main \(top\) panel instead of the [DevTools Drawer][DevtoolsCustomizeIndexDrawer], navigate to [moving tools between panels](#move-tools-between-panels).</span></span>  

> [!NOTE]
> <span data-ttu-id="97033-132">Para habilitar el experimento, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOn] y seleccione la casilla situada junto **a Habilitar consola de red.**</span><span class="sxs-lookup"><span data-stu-id="97033-132">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable Network Console**.</span></span>  
> 
> <span data-ttu-id="97033-133">Abra el [registro de red][DevtoolsNetworkIndexLogActivity], abra el menú contextual \(haga clic con el botón secundario\) y elija Editar y **reproducir**.</span><span class="sxs-lookup"><span data-stu-id="97033-133">Open the [Network Log][DevtoolsNetworkIndexLogActivity], open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  

<span data-ttu-id="97033-134">Chromium problema [#1093687][CR1093687]</span><span class="sxs-lookup"><span data-stu-id="97033-134">Chromium issue [#1093687][CR1093687]</span></span>  

### <a name="service-worker-respondwith-events-in-the-timing-tab"></a><span data-ttu-id="97033-135">Service worker respondWith events in the Timing tab</span><span class="sxs-lookup"><span data-stu-id="97033-135">Service worker respondWith events in the Timing tab</span></span>  

<span data-ttu-id="97033-136">La **pestaña Tiempo** de la herramienta **Red** ahora incluye eventos de trabajo `respondWith` de servicio.</span><span class="sxs-lookup"><span data-stu-id="97033-136">The **Timing** tab of the **Network** tool now includes `respondWith` service worker events.</span></span>  <span data-ttu-id="97033-137">El evento de trabajo de servicio muestra la duración del tiempo inmediatamente antes de que el controlador de eventos de trabajo de servicio comience a ejecutarse hasta el momento en que se resuelva la promesa `respondWith` `fetch` del `respondWith` `fetch` controlador.</span><span class="sxs-lookup"><span data-stu-id="97033-137">The `respondWith` service worker event shows the duration from the time immediately before the service worker `fetch` event handler starts running to the time when the `respondWith` promise of the `fetch` handler is settled.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="El evento de trabajo de servicio respondWith en la pestaña Temporización del panel Red" lightbox="../../media/2020/06/timing-tab.msft.png":::
   <span data-ttu-id="97033-139">Evento `respondWith` de trabajo de servicio en la pestaña **Temporización** de la **herramienta Red**</span><span class="sxs-lookup"><span data-stu-id="97033-139">The `respondWith` service worker event in the **Timing** tab of the **Network** tool</span></span>  
:::image-end:::  

<span data-ttu-id="97033-140">Expanda **Respuesta recibida** para mostrar información adicional de la respuesta como , y `fetch` `CacheStorageCacheName` `serviceWorkerResponseSource` `ResponseTime` .</span><span class="sxs-lookup"><span data-stu-id="97033-140">Expand **Response received** to display additional information from the `fetch` response like `CacheStorageCacheName`, `serviceWorkerResponseSource`, and `ResponseTime`.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Expandir Respuesta recibida para mostrar información adicional de la respuesta de captura" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   <span data-ttu-id="97033-142">Expandir **respuesta recibida** para mostrar información adicional de la `fetch` respuesta</span><span class="sxs-lookup"><span data-stu-id="97033-142">Expand **Response received** to display additional information from the `fetch` response</span></span>  
:::image-end:::  

<span data-ttu-id="97033-143">Chromium problema [#1066579][CR1066579]</span><span class="sxs-lookup"><span data-stu-id="97033-143">Chromium issue [#1066579][CR1066579]</span></span>  

### <a name="webhint-feedback-in-the-issues-panel"></a><span data-ttu-id="97033-144">comentarios de webhint en el panel Problemas</span><span class="sxs-lookup"><span data-stu-id="97033-144">webhint feedback in the Issues panel</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="97033-146">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="97033-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="97033-147">[webhint][WebhintMain] es una herramienta de código abierto que proporciona comentarios en tiempo real sobre la accesibilidad, compatibilidad entre exploradores, seguridad, rendimiento, PWA y otros problemas comunes de desarrollo web de sitios web.</span><span class="sxs-lookup"><span data-stu-id="97033-147">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="97033-148">Para revisar los comentarios de webhint en el panel [Problemas.][DevtoolsIssues]</span><span class="sxs-lookup"><span data-stu-id="97033-148">To review webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="comentarios de webhint en el panel Problemas" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   <span data-ttu-id="97033-150">comentarios de webhint en el panel Problemas</span><span class="sxs-lookup"><span data-stu-id="97033-150">webhint feedback in the Issues panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="97033-151">Para habilitar el experimento, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOn] y seleccione la casilla situada junto **a Habilitar webhint**.</span><span class="sxs-lookup"><span data-stu-id="97033-151">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable webhint**.</span></span>  
> 
> <span data-ttu-id="97033-152">Abra el panel [Problemas][DevtoolsIssues] para mostrar los comentarios de webhint.</span><span class="sxs-lookup"><span data-stu-id="97033-152">Open the [Issues][DevtoolsIssues] panel to display feedback from webhint.</span></span>  

<span data-ttu-id="97033-153">Chromium problema [#1070378][CR1070378]</span><span class="sxs-lookup"><span data-stu-id="97033-153">Chromium issue [#1070378][CR1070378]</span></span>  

### <a name="move-tools-between-panels"></a><span data-ttu-id="97033-154">Mover herramientas entre paneles</span><span class="sxs-lookup"><span data-stu-id="97033-154">Move tools between panels</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="97033-156">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="97033-156">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="97033-157">Normalmente, herramientas como **Elementos** y **Red** solo se pueden abrir en el panel principal \(top\) de DevTools.</span><span class="sxs-lookup"><span data-stu-id="97033-157">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="97033-158">Del mismo modo, las herramientas como **Vista 3D** y **Problemas** solo pueden abrirse en el panel \(bottom\) del cajón de DevTools.</span><span class="sxs-lookup"><span data-stu-id="97033-158">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="97033-159">Ahora puede personalizar el diseño de DevTools moviendo las herramientas entre los paneles superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="97033-159">You are now able to customize your DevTools layout by moving tools between the top and bottom panels.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Mover herramientas entre paneles" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   <span data-ttu-id="97033-161">Mover herramientas entre paneles</span><span class="sxs-lookup"><span data-stu-id="97033-161">Move tools between panels</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="97033-162">Para habilitar el experimento, vaya a Activar características [experimentales][DevtoolsExperimentalFeaturesTurnOn] y seleccione la casilla situada junto a Habilitar compatibilidad para mover **fichas entre paneles.**</span><span class="sxs-lookup"><span data-stu-id="97033-162">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable support to move tabs between panels**.</span></span>  

<span data-ttu-id="97033-163">Chromium problema [#897944][CR897944]</span><span class="sxs-lookup"><span data-stu-id="97033-163">Chromium issue [#897944][CR897944]</span></span>  

### <a name="improved-initiator-tooltip-in-the-network-panel"></a><span data-ttu-id="97033-164">Información sobre herramientas del iniciador mejorada en el panel Red</span><span class="sxs-lookup"><span data-stu-id="97033-164">Improved Initiator tooltip in the Network panel</span></span>  

<span data-ttu-id="97033-165">En Microsoft Edge 83 y 84, la información sobre herramientas de la columna Iniciador, que muestra la causa de la solicitud de recurso, en el registro de red que se muestra con una barra de desplazamiento horizontal. [][DevtoolsNetworkIndexLogActivity]</span><span class="sxs-lookup"><span data-stu-id="97033-165">In Microsoft Edge 83 and 84, tooltips for the Initiator column, which shows the cause of the resource request, in the [Network Log][DevtoolsNetworkIndexLogActivity] displayed with a horizontal scrollbar.</span></span>  <span data-ttu-id="97033-166">Solo pudo mostrar la pila de llamadas que inició la solicitud desplazándose horizontalmente en la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="97033-166">You were only able to display the call stack that initiated the request by scrolling horizontally in the tooltip.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Información sobre herramientas del iniciador en Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   <span data-ttu-id="97033-168">Información sobre herramientas del iniciador en Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="97033-168">The Initiator tooltip in Microsoft Edge 84</span></span>  
:::image-end:::  

<span data-ttu-id="97033-169">A partir Microsoft Edge 85, ahora puede mostrar la pila de llamadas del iniciador en la información sobre herramientas sin desplazarse horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="97033-169">Starting with Microsoft Edge 85, you are now able to display the Initiator call stack in the tooltip without scrolling horizontally.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Información sobre herramientas del iniciador en Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   <span data-ttu-id="97033-171">Información sobre herramientas del iniciador en Microsoft Edge 85</span><span class="sxs-lookup"><span data-stu-id="97033-171">The Initiator tooltip in Microsoft Edge 85</span></span>
:::image-end:::  

<span data-ttu-id="97033-172">Chromium problema [#1069404][CR1069404]</span><span class="sxs-lookup"><span data-stu-id="97033-172">Chromium issue [#1069404][CR1069404]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="97033-173">Anuncios del proyecto de Chromium</span><span class="sxs-lookup"><span data-stu-id="97033-173">Announcements from the Chromium project</span></span>  

<span data-ttu-id="97033-174">Las siguientes secciones anuncian características adicionales disponibles en Microsoft Edge 85 que se contribuyeron al proyecto de código Chromium abierto.</span><span class="sxs-lookup"><span data-stu-id="97033-174">The following sections announce additional features available in Microsoft Edge 85 that were contributed to the open source Chromium project.</span></span>  

### <a name="style-editing-for-css-in-js-frameworks"></a><span data-ttu-id="97033-175">Edición de estilos para marcos CSS-in-JS</span><span class="sxs-lookup"><span data-stu-id="97033-175">Style editing for CSS-in-JS frameworks</span></span>  

<span data-ttu-id="97033-176">El **panel Estilos** ahora admite mejor los estilos de edición que se crearon con las API del modelo de objetos CSS [(CSSOM).][CsswgDraftsCssom]</span><span class="sxs-lookup"><span data-stu-id="97033-176">The **Styles** pane now has better support for editing styles that were created with the [CSS Object Model (CSSOM)][CsswgDraftsCssom] APIs.</span></span>  <span data-ttu-id="97033-177">Muchos marcos y bibliotecas de CSS-in-JS usan las API cssom debajo del capó para crear estilos.</span><span class="sxs-lookup"><span data-stu-id="97033-177">Many CSS-in-JS frameworks and libraries use the CSSOM APIs under the hood to construct styles.</span></span>  

<span data-ttu-id="97033-178">Ahora puede editar los estilos agregados en JavaScript con hojas de estilos [constructables.][WicgConstructStylesheet]</span><span class="sxs-lookup"><span data-stu-id="97033-178">You are now able to edit styles added in JavaScript using [Constructable Stylesheets][WicgConstructStylesheet].</span></span>  <span data-ttu-id="97033-179">Las hojas de estilo constructables son una nueva forma de crear y distribuir estilos reutilizables al usar [Shadow DOM][MdnShadowDom].</span><span class="sxs-lookup"><span data-stu-id="97033-179">Constructable Stylesheets are a new way to create and distribute reusable styles when using [Shadow DOM][MdnShadowDom].</span></span>  

<span data-ttu-id="97033-180">Por ejemplo, los `h1` estilos agregados con `CSSStyleSheet` \(CSSOM API\) no se modificaban anteriormente.</span><span class="sxs-lookup"><span data-stu-id="97033-180">For example, the `h1` styles added with `CSSStyleSheet` \(CSSOM APIs\) were not editable previously.</span></span>  <span data-ttu-id="97033-181">Los estilos se pueden editar ahora en el panel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="97033-181">The styles are editable now in the **Styles** panel.</span></span>  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Cambiar la propiedad de fondo de los estilos h1 agregados con CSSStyleSheet de rosa a azul claro" lightbox="../../media/2020/06/css-in-js.msft.png":::
   <span data-ttu-id="97033-183">Cambiar la `background` propiedad de los estilos `h1` agregados con de a `CSSStyleSheet` `pink` `lightblue` .</span><span class="sxs-lookup"><span data-stu-id="97033-183">Changing the `background` property of the `h1` styles added with `CSSStyleSheet` from `pink` to `lightblue`.</span></span>
:::image-end:::  

<span data-ttu-id="97033-184">Pruebe esta característica con un [ejemplo que use CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span><span class="sxs-lookup"><span data-stu-id="97033-184">Give this feature a try with a [sample that uses CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span></span>

<span data-ttu-id="97033-185">Chromium problema [#946975][CR946975]</span><span class="sxs-lookup"><span data-stu-id="97033-185">Chromium issue [#946975][CR946975]</span></span>  

### <a name="lighthouse-6-in-the-lighthouse-panel"></a><span data-ttu-id="97033-186">Faro 6 en el panel Faro</span><span class="sxs-lookup"><span data-stu-id="97033-186">Lighthouse 6 in the Lighthouse panel</span></span>  

<span data-ttu-id="97033-187">El panel **Faro** está ejecutando Ahora Faro 6.</span><span class="sxs-lookup"><span data-stu-id="97033-187">The **Lighthouse** panel is now running Lighthouse 6.</span></span>  <span data-ttu-id="97033-188">Para obtener una lista completa de todos los cambios, vaya a las notas de la [versión v6.0.0][GithubGoogleChromeLighthouse600].</span><span class="sxs-lookup"><span data-stu-id="97033-188">For a full list of all changes, navigate to [v6.0.0 release notes][GithubGoogleChromeLighthouse600].</span></span>  

<span data-ttu-id="97033-189">Lighthouse 6.0 presenta tres nuevas métricas para el informe: Largest Contentful Paint \(LCP\), Cumulative Layout Shift \(CLS\) y Total Blocking Time \(TBT\).</span><span class="sxs-lookup"><span data-stu-id="97033-189">Lighthouse 6.0 introduces three new metrics to the report:  Largest Contentful Paint \(LCP\), Cumulative Layout Shift \(CLS\), and Total Blocking Time \(TBT\).</span></span>  

<span data-ttu-id="97033-190">La fórmula de puntuación de rendimiento también se ha repondido para reflejar mejor la experiencia de carga del usuario.</span><span class="sxs-lookup"><span data-stu-id="97033-190">The performance score formula has also been reweighted to better reflect the loading experience of the user.</span></span>  

<span data-ttu-id="97033-191">Chromium problema [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="97033-191">Chromium issue [#772558][CR772558]</span></span>  

#### <a name="first-meaningful-paint-deprecation"></a><span data-ttu-id="97033-192">Primera desuso Paint significativa</span><span class="sxs-lookup"><span data-stu-id="97033-192">First Meaningful Paint deprecation</span></span>  

<span data-ttu-id="97033-193">First Meaningful Paint \(FMP\) está en desuso en Lighthouse 6.0.</span><span class="sxs-lookup"><span data-stu-id="97033-193">First Meaningful Paint \(FMP\) is deprecated in Lighthouse 6.0.</span></span>  <span data-ttu-id="97033-194">FMP también se ha quitado del panel **Rendimiento.**</span><span class="sxs-lookup"><span data-stu-id="97033-194">FMP has also been removed from the **Performance** panel.</span></span>  <span data-ttu-id="97033-195">**La mayor Paint contentful** es el reemplazo recomendado para FMP.</span><span class="sxs-lookup"><span data-stu-id="97033-195">**Largest Contentful Paint** is the recommended replacement for FMP.</span></span>  <!--For an explanation of why it was deprecated, navigate to [First Meaningful Paint][WebDevFirstMeaningfulPaint].  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

<span data-ttu-id="97033-196">Chromium problema [#1096008][CR1096008]</span><span class="sxs-lookup"><span data-stu-id="97033-196">Chromium issue [#1096008][CR1096008]</span></span>  

### <a name="support-for-new-javascript-features"></a><span data-ttu-id="97033-197">Compatibilidad con nuevas características de JavaScript</span><span class="sxs-lookup"><span data-stu-id="97033-197">Support for new JavaScript features</span></span>  

<span data-ttu-id="97033-198">DevTools ahora tiene mejor compatibilidad con algunas de las características más recientes del lenguaje JavaScript.</span><span class="sxs-lookup"><span data-stu-id="97033-198">DevTools now has better support for some of the latest JavaScript language features.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="97033-199">[Autocompletion de sintaxis][V8DevOptionalChaining] de encadenamiento opcional</span><span class="sxs-lookup"><span data-stu-id="97033-199">[Optional chaining][V8DevOptionalChaining] syntax autocompletion</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="97033-200">La finalización automática de la propiedad **en la consola** ahora admite la sintaxis de encadenamiento opcional, por ejemplo, ahora funciona además de y  `name?.` `name.` `name[` .</span><span class="sxs-lookup"><span data-stu-id="97033-200">Property auto-completion in the **Console** now supports optional chaining syntax, for example,  `name?.` now works in addition to `name.` and `name[`.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="97033-201">Resaltado de sintaxis para [campos privados][V8DevClassFieldsPrivate]</span><span class="sxs-lookup"><span data-stu-id="97033-201">Syntax highlighting for [private fields][V8DevClassFieldsPrivate]</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="97033-202">Los campos de clase privada ahora están correctamente resaltados por la sintaxis y están bastante impresos en **el** panel Orígenes.</span><span class="sxs-lookup"><span data-stu-id="97033-202">private class fields are now properly syntax-highlighted and pretty-printed in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="97033-203">Resaltado de sintaxis [para el operador de conjunción Nullish][V8DevNullishCoalescing]</span><span class="sxs-lookup"><span data-stu-id="97033-203">Syntax highlighting for [Nullish coalescing operator][V8DevNullishCoalescing]</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="97033-204">Ahora DevTools imprime correctamente el operador de conjunción nulo en el panel **Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="97033-204">DevTools now properly pretty-prints the nullish coalescing operator in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="97033-205">Chromium problemas [#1073903][CR1073903], [#1083214][CR1083214] [,][CR1083797] #1083797</span><span class="sxs-lookup"><span data-stu-id="97033-205">Chromium issues [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span></span>  

### <a name="new-app-shortcut-warnings-in-the-manifest-pane"></a><span data-ttu-id="97033-206">Nuevas advertencias de acceso directo de la aplicación en el panel Manifiesto</span><span class="sxs-lookup"><span data-stu-id="97033-206">New app shortcut warnings in the Manifest pane</span></span>  

<span data-ttu-id="97033-207">**Los accesos directos de** la aplicación ayudan a los usuarios a iniciar rápidamente tareas comunes o recomendadas dentro de una aplicación web.</span><span class="sxs-lookup"><span data-stu-id="97033-207">**App shortcuts** help users quickly start common or recommended tasks within a web app.</span></span>  

<!--todo: add App shortcuts when section is live  -->  

<span data-ttu-id="97033-208">El **panel** Manifiesto ahora muestra advertencias para las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="97033-208">The **Manifest** pane now shows warnings for the following conditions.</span></span>  

* <span data-ttu-id="97033-209">Los iconos de acceso directo de la aplicación son menores que 96 x 96 píxeles</span><span class="sxs-lookup"><span data-stu-id="97033-209">The app shortcut icons are smaller than 96x96 pixels</span></span>  
* <span data-ttu-id="97033-210">Los iconos de acceso directo de la aplicación y los iconos de manifiesto no son cuadrados \(dado que los iconos se omiten\)</span><span class="sxs-lookup"><span data-stu-id="97033-210">The app shortcut icons and manifest icons are not square \(since the icons are ignored\)</span></span>  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Advertencias de acceso directo de aplicaciones" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   <span data-ttu-id="97033-212">Advertencias de acceso directo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="97033-212">App shortcut warnings</span></span>  
:::image-end:::  

<span data-ttu-id="97033-213">Chromium problema [#955497][CR955497]</span><span class="sxs-lookup"><span data-stu-id="97033-213">Chromium issue [#955497][CR955497]</span></span>  

### <a name="consistent-display-of-the-computed-pane"></a><span data-ttu-id="97033-214">Visualización coherente del panel calculado</span><span class="sxs-lookup"><span data-stu-id="97033-214">Consistent display of the Computed pane</span></span>  

<span data-ttu-id="97033-215">El **panel Calculado de** la herramienta **Elementos** ahora se muestra de forma coherente como un panel en todos los tamaños de ventanilla.</span><span class="sxs-lookup"><span data-stu-id="97033-215">The **Computed** pane in the **Elements** tool now displays consistently as a pane across all viewport sizes.</span></span>  <span data-ttu-id="97033-216">Anteriormente, el **panel Calculado** se combinaba dentro del panel **Estilos** cuando el ancho de la ventanilla de DevTools era estrecho.</span><span class="sxs-lookup"><span data-stu-id="97033-216">Previously the **Computed** pane merged inside the **Styles** pane when the width of the DevTools viewport was narrow.</span></span>  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="El panel Calculado se muestra de forma coherente como un panel independiente incluso cuando las DevTools son estrechas" lightbox="../../media/2020/06/computed-pane.msft.png":::
   <span data-ttu-id="97033-218">El **panel Calculado** se muestra de forma coherente como un panel independiente incluso cuando las DevTools son estrechas.</span><span class="sxs-lookup"><span data-stu-id="97033-218">The **Computed** pane consistently displays as a separate pane even when the DevTools are narrow.</span></span>
:::image-end:::  

<span data-ttu-id="97033-219">Chromium problema [#1073899][CR1073899]</span><span class="sxs-lookup"><span data-stu-id="97033-219">Chromium issue [#1073899][CR1073899]</span></span>  

### <a name="bytecode-offsets-for-webassembly-files"></a><span data-ttu-id="97033-220">Desplazamientos de bytecode para archivos WebAssembly</span><span class="sxs-lookup"><span data-stu-id="97033-220">Bytecode offsets for WebAssembly files</span></span>  

<span data-ttu-id="97033-221">DevTools ahora usa desplazamientos de código de bytes para mostrar números de línea de desmontaje de Wasm.</span><span class="sxs-lookup"><span data-stu-id="97033-221">DevTools now uses bytecode offsets for displaying line numbers of Wasm disassembly.</span></span>  
<span data-ttu-id="97033-222">Los números de línea hacen que sea más claro que está mirando datos binarios y es más coherente con la forma en que el tiempo de ejecución de Wasm hace referencia a las ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="97033-222">The line numbers make it clearer that you are looking at binary data, and is more consistent with how the Wasm runtime references locations.</span></span>  

<span data-ttu-id="97033-223">Chromium problema [#1071432][CR1071432]</span><span class="sxs-lookup"><span data-stu-id="97033-223">Chromium issue [#1071432][CR1071432]</span></span>  

### <a name="line-wise-copy-and-cut-in-sources-panel"></a><span data-ttu-id="97033-224">Copiar y cortar en línea en el Panel orígenes</span><span class="sxs-lookup"><span data-stu-id="97033-224">Line-wise copy and cut in Sources Panel</span></span>  

<span data-ttu-id="97033-225">Al realizar copias o cortes sin selección en el editor del [panel Orígenes,][DevtoolsSourcesIndexUsingEditorPaneToViewEditFiles]DevTools copia o corta la línea de contenido actual.</span><span class="sxs-lookup"><span data-stu-id="97033-225">When performing copy or cut with no selection in the [Sources panel editor][DevtoolsSourcesIndexUsingEditorPaneToViewEditFiles], DevTools copies or cuts the current line of content.</span></span>  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Con el cursor al final de la línea 5, copiando toda la línea desde pen.js en devTools y pegando en Visual Studio Code" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   <span data-ttu-id="97033-227">Con el cursor al final de la línea 5, copiando toda la línea desde **pen.js** en devTools y pegando en [Visual Studio Code][VisualStudioCode].</span><span class="sxs-lookup"><span data-stu-id="97033-227">With the cursor at the end of Line 5, copying the whole line from **pen.js** in the DevTools and pasting in [Visual Studio Code][VisualStudioCode].</span></span>
:::image-end:::  

<span data-ttu-id="97033-228">Chromium problema [#800028][CR800028]</span><span class="sxs-lookup"><span data-stu-id="97033-228">Chromium issue [#800028][CR800028]</span></span>

### <a name="console-settings-updates"></a><span data-ttu-id="97033-229">Actualizaciones de Configuración consola</span><span class="sxs-lookup"><span data-stu-id="97033-229">Console Settings updates</span></span>  

#### <a name="ungroup-same-console-messages"></a><span data-ttu-id="97033-230">Desagrupar los mismos mensajes de consola</span><span class="sxs-lookup"><span data-stu-id="97033-230">Ungroup same console messages</span></span>  

<span data-ttu-id="97033-231">La **alternancia Group similar** en console Configuración ahora se aplica a los mensajes duplicados.</span><span class="sxs-lookup"><span data-stu-id="97033-231">The **Group similar** toggle in Console Settings now applies to duplicate messages.</span></span>  <span data-ttu-id="97033-232">Anteriormente solo se aplicaba a mensajes similares.</span><span class="sxs-lookup"><span data-stu-id="97033-232">Previously it just applied to similar messages.</span></span>  

<span data-ttu-id="97033-233">Por ejemplo, anteriormente, DevTools no desagrupó los mensajes `hello` aunque **group similar** está desactivado.</span><span class="sxs-lookup"><span data-stu-id="97033-233">For example, previously, DevTools did not ungroup the `hello` messages even though **Group similar** is unchecked.</span></span>  <span data-ttu-id="97033-234">Ahora, los `hello` mensajes se desagrupa.</span><span class="sxs-lookup"><span data-stu-id="97033-234">Now, the `hello` messages are ungrouped.</span></span>  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Cuando group similar is unchecked, the hello messages are ungrouped" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   <span data-ttu-id="97033-236">Cuando **group similar** is unchecked, the messages are `hello` ungrouped</span><span class="sxs-lookup"><span data-stu-id="97033-236">When **Group similar** is unchecked, the `hello` messages are ungrouped</span></span>
:::image-end:::  

<span data-ttu-id="97033-237">Pruebe esta característica con un [ejemplo que envíe mensajes duplicados a la consola][CodepenZoherghadyaliZyrjgdJ].</span><span class="sxs-lookup"><span data-stu-id="97033-237">Give this feature a try with a [sample that sends duplicate messages to the Console][CodepenZoherghadyaliZyrjgdJ].</span></span>  

<span data-ttu-id="97033-238">Chromium problema [#1082963][CR1082963]</span><span class="sxs-lookup"><span data-stu-id="97033-238">Chromium issue [#1082963][CR1082963]</span></span>  

### <a name="persisting-selected-context-only-settings"></a><span data-ttu-id="97033-239">Persisting Selected context only settings</span><span class="sxs-lookup"><span data-stu-id="97033-239">Persisting Selected context only settings</span></span>  

<span data-ttu-id="97033-240">Ahora **se conserva la** configuración de solo contexto seleccionado Configuración configuración de consola.</span><span class="sxs-lookup"><span data-stu-id="97033-240">The **Selected context only** settings in Console Settings is now persisted.</span></span>  <span data-ttu-id="97033-241">Anteriormente, la configuración se restablece cada vez que se cierra y se vuelve a abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="97033-241">Previously the settings were reset every time you closed and reopened DevTools.</span></span>  <span data-ttu-id="97033-242">El cambio hace que el comportamiento de configuración sea coherente con otras opciones de configuración Configuración consola.</span><span class="sxs-lookup"><span data-stu-id="97033-242">The change makes the setting behavior consistent with other Console Settings options.</span></span>  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Configuración de solo contexto seleccionada" lightbox="../../media/2020/06/selected-context.msft.png":::
   <span data-ttu-id="97033-244">**Configuración de solo contexto** seleccionada</span><span class="sxs-lookup"><span data-stu-id="97033-244">**Selected context only** setting</span></span>  
:::image-end:::  

<span data-ttu-id="97033-245">Chromium problema [#1055875][CR1055875]</span><span class="sxs-lookup"><span data-stu-id="97033-245">Chromium issue [#1055875][CR1055875]</span></span>  

### <a name="performance-panel-updates"></a><span data-ttu-id="97033-246">Actualizaciones del panel de rendimiento</span><span class="sxs-lookup"><span data-stu-id="97033-246">Performance panel updates</span></span>  

#### <a name="javascript-compilation-cache-information-in-performance-tool"></a><span data-ttu-id="97033-247">Información de caché de compilación de JavaScript en **la herramienta** Rendimiento</span><span class="sxs-lookup"><span data-stu-id="97033-247">JavaScript compilation cache information in **Performance** tool</span></span>  

<span data-ttu-id="97033-248">[La información de caché de compilación de JavaScript][V8DevCodeCaching] ahora siempre se muestra en el panel **Resumen** de la **herramienta** Rendimiento.</span><span class="sxs-lookup"><span data-stu-id="97033-248">[JavaScript compilation cache information][V8DevCodeCaching] is now always displayed in the **Summary** panel of the **Performance** tool.</span></span>  <span data-ttu-id="97033-249">Anteriormente, DevTools no mostraba nada relacionado con el almacenamiento en caché de código si el almacenamiento en caché de código no se hacía.</span><span class="sxs-lookup"><span data-stu-id="97033-249">Previously, DevTools did not show anything related to code caching if code caching did not happen.</span></span>  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Información de caché de compilación de JavaScript" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   <span data-ttu-id="97033-251">Información de caché de compilación de JavaScript</span><span class="sxs-lookup"><span data-stu-id="97033-251">JavaScript compilation cache information</span></span>  
:::image-end:::  

<span data-ttu-id="97033-252">Chromium problema [#912581][CR912581]</span><span class="sxs-lookup"><span data-stu-id="97033-252">Chromium issue [#912581][CR912581]</span></span>  

#### <a name="navigation-timing-alignment-in-the-performance-panel"></a><span data-ttu-id="97033-253">Alineación del tiempo de navegación en el panel Rendimiento</span><span class="sxs-lookup"><span data-stu-id="97033-253">Navigation timing alignment in the Performance panel</span></span>  

<span data-ttu-id="97033-254">El \*\*\*\* panel Rendimiento usado para mostrar horas en las reglas en función del momento en que se inició la grabación.</span><span class="sxs-lookup"><span data-stu-id="97033-254">The **Performance** panel used to show times in the rulers based on when the recording started.</span></span>  <span data-ttu-id="97033-255">Ahora, el tiempo ha cambiado para las grabaciones en las que el usuario navega, donde DevTools ahora muestra los tiempos de regla relativos a la navegación.</span><span class="sxs-lookup"><span data-stu-id="97033-255">The timing has now changed for recordings where the user navigates, where DevTools now shows ruler times relative to the navigation instead.</span></span>  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Alinear el tiempo de navegación en la herramienta Rendimiento" lightbox="../../media/2020/06/nav-timing.msft.png":::
   <span data-ttu-id="97033-257">Alinear el tiempo de navegación en **la herramienta Rendimiento**</span><span class="sxs-lookup"><span data-stu-id="97033-257">Align navigation timing in **Performance** tool</span></span>  
:::image-end:::  

<span data-ttu-id="97033-258">Las horas `DOMContentLoaded` de , First Paint, First Contentful Paint y Largest Contentful Paint events se actualizan para que sean relativas al inicio de la navegación, lo que significa que el tiempo coincide con los tiempos notificados por `PerformanceObserver` .</span><span class="sxs-lookup"><span data-stu-id="97033-258">The times for `DOMContentLoaded`, First Paint, First Contentful Paint, and Largest Contentful Paint events are updated to be relative to the start of the navigation, which means the timing matches the timings reported by `PerformanceObserver`.</span></span>  

<span data-ttu-id="97033-259">Chromium problema [#974550][CR974550]</span><span class="sxs-lookup"><span data-stu-id="97033-259">Chromium issue [#974550][CR974550]</span></span>  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a><span data-ttu-id="97033-260">Nuevos iconos para puntos de interrupción, puntos de interrupción condicionales y puntos de registro</span><span class="sxs-lookup"><span data-stu-id="97033-260">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="97033-261">El panel **Orígenes** tiene nuevos diseños para puntos de interrupción, puntos de interrupción condicionales y puntos de registro.</span><span class="sxs-lookup"><span data-stu-id="97033-261">The **Sources** panel has new designs for breakpoints, conditional breakpoints, and logpoints.</span></span>  <span data-ttu-id="97033-262">Los puntos de interrupción se representan mediante un círculo rojo, al igual que [Visual Studio Code][VisualStudioCode] y [Visual Studio][VisualStudio].</span><span class="sxs-lookup"><span data-stu-id="97033-262">Breakpoints are represented by a red circle, just like [Visual Studio Code][VisualStudioCode] and [Visual Studio][VisualStudio].</span></span>  <span data-ttu-id="97033-263">Se agregan iconos para diferenciar puntos de interrupción condicionales y puntos de registro.</span><span class="sxs-lookup"><span data-stu-id="97033-263">Icons are added to differentiate conditional breakpoints and logpoints.</span></span>  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Puntos de interrupción" lightbox="../../media/2020/06/breakpoints.msft.png":::
   <span data-ttu-id="97033-265">Puntos de interrupción</span><span class="sxs-lookup"><span data-stu-id="97033-265">Breakpoints</span></span>  
:::image-end:::  

<span data-ttu-id="97033-266">Chromium problema [#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="97033-266">Chromium issue [#1041830][CR1041830]</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="97033-267">Descargar los canales de versión preliminar de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="97033-267">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="97033-268">Si está en Windows o macOS, considere la posibilidad de usar los canales [Microsoft Edge vista previa][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="97033-268">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="97033-269">Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="97033-269">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="97033-270">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="97033-270">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../../../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[DevtoolsCommandMenu]: ../../../command-menu.md "Ejecutar comandos con el Microsoft Edge de comandos DevTools | Microsoft Docs"
[DevtoolsCustomizeIndexDrawer]: ../../../customize/index.md#drawer "Drawer: personalice Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsExperimentalFeaturesTurnOn]: ../../../experimental-features/index.md#turn-on-experimental-features "Activar características experimentales: características experimentales | Microsoft Docs"  
[DevtoolsIssues]: ../../../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas | Microsoft Docs"
[DevtoolsSourcesIndexUsingEditorPaneToViewEditFiles]: ../../../sources/index.md#using-the-editor-pane-to-view-or-edit-files "Uso del panel Editor para ver o editar archivos: Información general del panel orígenes | Microsoft Docs"  
[DevtoolsNetworkIndexLogActivity]: ../../../network/index.md#log-network-activity "Actividad de red de registro: inspeccionar la actividad de red en Microsoft Edge DevTools | Microsoft Docs"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Edición de estilos para marcos CSS-in-JS | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Enviar mensajes duplicados a la consola | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Ejemplo de planificador de cuadrícula CSS | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  

[CR772558]: https://crbug.com/772558 "DevTools: actualizar a la versión más reciente de | Chromium errores"  
[CR800028]: https://crbug.com/800028 "Acceso directo de línea duplicada en el editor de Herramientas de desarrollador que no funciona después de actualizar Chrome | Chromium errores"  
[CR912581]: https://crbug.com/912581 "Exponer los scripts almacenados en caché por V8 en DevTools/about:tracing | Chromium errores"  
[CR946975]: https://crbug.com/946975 "La barra lateral de estilos de DevTools no funciona con hojas de estilos construidas | Chromium errores"  
[CR955497]: https://crbug.com/955497 "Menú contextual de icono de aplicación para PWAs | Chromium errores"  
[CR974550]: https://crbug.com/974550 "Error de coincidencia de métricas entre el panel Perf y performanceObserver | Chromium errores"  
[CR1041830]: https://crbug.com/1041830 "Mejorar los colores de los puntos de interrupción | Chromium errores"  
[CR1055875]: https://crbug.com/1055875 "El valor de la configuración de consola Solo contexto seleccionado no persiste después de cerrar y volver a abrir herramientas de | Chromium errores"  
[CR1066579]: https://crbug.com/1066579 "DevTools: mostrar la escala de tiempo de recuperación de ServiceWorkers por solicitud en el panel DevTools | Chromium errores"  
[CR1071432]: https://crbug.com/1071432 "Wasm Basic Developer Experience | Chromium errores"  
[CR1073899]: https://crbug.com/1073899 "La pestaña Estilo calculado desaparece en modo de respuesta | Chromium errores"  
[CR1073903]: https://crbug.com/1073903 "DevTools: el resaltado de sintaxis no funciona con campos privados | Chromium errores"  
[CR1082963]: https://crbug.com/1082963 "No se puede deshabilitar el comportamiento de mensajes similares de grupo de la consola | Chromium errores"  
[CR1083214]: https://crbug.com/1083214 "acorn no admite cadenas opcionales | Chromium errores"  
[CR1083797]: https://crbug.com/1083797 "Se ha roto la impresión bastante para la | Chromium errores"  
[CR1096008]: https://crbug.com/1096008 "Quitar FMP | Chromium errores"  
[CR1047356]: https://crbug.com/1047356 "Herramientas CSS Grid/Flexbox/Table | Chromium errores"  
[CR1093687]: https://crbug.com/1093687 "Crear herramienta para crear y reproducir solicitudes de red sintéticas | Chromium errores"  
[CR1070378]: https://crbug.com/1070378 "Integrar webhint en DevTools | Chromium errores"  
[CR1069404]: https://crbug.com/1069404 "Los elementos emergentes del widget [Herramientas de desarrollo] son demasiado estrechos | Chromium errores"  
[CR897944]: https://crbug.com/897944 "Paneles de devtool arrastrables | Chromium errores"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v6.0.0: GoogleChrome/lighthouse | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nuevo problema: MicrosoftDocs/edge-developer"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Uso de dom de sombra | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Canales de versiones preliminares de Microsoft Edge"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"
[VisualStudioCode]: https://code.visualstudio.com/ "Visual Studio Code"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Modelo de objetos CSS (CSSOM) | Borradores del editor de grupo de trabajo CSS de W3C"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "Cuenta de Twitter de @EdgeDevTools"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Campos de clase privada: campos de clase pública y privada | V8. Desarrollo"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Almacenamiento en caché de código para desarrolladores de JavaScript | V8. Desarrollo"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Nullish coalescing | V8. Desarrollo"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Cadenas opcionales | V8. Desarrollo"  

[WebhintMain]: https://webhint.io "webhint"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Objetos de hoja de estilos | Web Incubator CG"

<!--[WebDevLighthouseWhatsNew60]: https://web.dev/lighthouse-whats-new-6.0 "What's New in Lighthouse 6.0 | Web.Dev"  -->  
<!--[WebDevVitalsCoreWeb]: https://web.dev/vitals#core-web-vitals "Core Web Vitals - Web Vitals | Web.Dev"  -->  
<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebFundamentalComponentsShadowdom]: /web/fundamentals/web-components/shadowdom  -->  
<!--[WebDevLcp]: https://web.dev/lcp "Largest Contentful Paint (LCP) | Web.Dev"  -->  
<!--[WebDevFirstMeaningfulPaint]: https://web.dev/first-meaningful-paint "First Meaningful Paint | Web.Dev"  -->  
<!--[WhatsNew201902ConstructableStylesheets]: ../../2019/02/constructable-stylesheets.md "Constructable Stylesheets: seamless reusable styles | Microsoft Docs"  -->  

[TheWebWeWant]: https://webwewant.fyi/ "La web que queremos"  

> [!NOTE]
> <span data-ttu-id="97033-319">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="97033-319">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="97033-320">La página original se encuentra [aquí](https://developer.chrome.com/blog/new-in-devtools-85) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="97033-320">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-85) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="97033-322">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="97033-322">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

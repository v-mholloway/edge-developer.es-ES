---
title: Novedades de DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f569414a95336278c93b1bbafd57153ca902df12
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942195"
---
# <span data-ttu-id="06857-103">Novedades de DevTools (Microsoft Edge 85)</span><span class="sxs-lookup"><span data-stu-id="06857-103">What's New In DevTools (Microsoft Edge 85)</span></span>  

## <span data-ttu-id="06857-104">Anuncios del equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="06857-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="06857-105">Las secciones siguientes son una lista de anuncios que puede haber perdido del equipo Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="06857-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="06857-106">Vea los anuncios para probar nuevas características de la DevTools, extensiones de código de VS y mucho más.</span><span class="sxs-lookup"><span data-stu-id="06857-106">See the announcements to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="06857-107">Para estar al día de las características más recientes y las más recientes de las herramientas para desarrolladores, descargue los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] y [siga el equipo de Microsoft Edge DevTools en Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="06857-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow the Microsoft Edge DevTools team on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="06857-108">Características de depuración de cuadrícula CSS</span><span class="sxs-lookup"><span data-stu-id="06857-108">CSS grid debugging features</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="06857-110">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="06857-110">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="06857-111">El equipo de DevTools de Microsoft Edge está colaborando con el equipo de Chrome DevTools y la comunidad de cromo para agregar nuevas características de depuración de cuadrícula CSS a DevTools.</span><span class="sxs-lookup"><span data-stu-id="06857-111">The Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new CSS grid debugging features to DevTools.</span></span>  <span data-ttu-id="06857-112">Ahora puede mostrar los números de línea de la cuadrícula, los huecos de cuadrícula y las líneas de cuadrícula extendidas como una superposición en la página.</span><span class="sxs-lookup"><span data-stu-id="06857-112">You are now able to display grid line numbers, grid gaps, and extended grid lines as an on-page overlay.</span></span>  <span data-ttu-id="06857-113">Además, pronto estarán disponibles otras mejoras en las herramientas de cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="06857-113">Plus, more improvements to the grid tools are coming soon.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Características de depuración de cuadrícula CSS" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   <span data-ttu-id="06857-115">Características de depuración de cuadrícula CSS</span><span class="sxs-lookup"><span data-stu-id="06857-115">CSS grid debugging features</span></span>
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="06857-116">Para habilitar el experimento, vea [activar las características experimentales][DevtoolsExperimentalFeaturesTurnOn] y seleccione la casilla situada junto a **Habilitar nuevas características de depuración de la cuadrícula CSS**.</span><span class="sxs-lookup"><span data-stu-id="06857-116">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable new CSS Grid debugging features**.</span></span>  
> 
> <span data-ttu-id="06857-117">Para probar el experimento con un ejemplo, consulta [ejemplo de planeación de cuadrícula CSS][CodepenRachelweilYzwBzKM].</span><span class="sxs-lookup"><span data-stu-id="06857-117">To try out the experiment with a sample, see [CSS Grid planner example][CodepenRachelweilYzwBzKM].</span></span>  

<span data-ttu-id="06857-118">[#1047356][CR1047356] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-118">Chromium issue [#1047356][CR1047356]</span></span>  

### <span data-ttu-id="06857-119">Editar y reproducir solicitudes con la consola de red</span><span class="sxs-lookup"><span data-stu-id="06857-119">Edit and Replay requests with the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="06857-121">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="06857-121">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="06857-122">Ahora puede usar **Editar y reproducir** en las solicitudes en el [registro de red][DevtoolsNetworkIndexLogActivity] con la consola de **red**.</span><span class="sxs-lookup"><span data-stu-id="06857-122">You are now able to use **Edit and Replay** on requests in the [Network Log][DevtoolsNetworkIndexLogActivity] using the **Network Console**.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Editar y reproducir una solicitud en el NetworkLog con la consola de red" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   <span data-ttu-id="06857-124">Editar y reproducir una solicitud en el [NetworkLog][DevtoolsNetworkIndexLogActivity] con la **consola de red**</span><span class="sxs-lookup"><span data-stu-id="06857-124">Edit and Replay a request in the [NetworkLog][DevtoolsNetworkIndexLogActivity] with the **Network Console**</span></span>  
:::image-end:::  

<span data-ttu-id="06857-125">Un panel nuevo, la **consola de red** se abre en el [cajón de DevTools][DevtoolsCustomizeIndexDrawer] y se rellena automáticamente con información para la solicitud HTTP.</span><span class="sxs-lookup"><span data-stu-id="06857-125">A new panel, the **Network Console** opens in the [DevTools Drawer][DevtoolsCustomizeIndexDrawer] and automatically populates with information for the HTTP request.</span></span>  <span data-ttu-id="06857-126">Para ver la respuesta devuelta desde el servidor, edite \ (si es necesario \) y seleccione **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="06857-126">To see the response returned from the server, edit the request \(if needed\) and select **Send**.</span></span>  

<span data-ttu-id="06857-127">También puede usar la **consola de red** para crear y enviar solicitudes HTTP directamente desde el DevTools.</span><span class="sxs-lookup"><span data-stu-id="06857-127">You may also use the **Network Console** to create and send HTTP requests directly from the DevTools.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Panel de consola de red" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   <span data-ttu-id="06857-129">Panel de **consola de red**</span><span class="sxs-lookup"><span data-stu-id="06857-129">The **Network Console** panel</span></span>  
:::image-end:::  

> [!TIP]
> <span data-ttu-id="06857-130">Para ver la **consola de red** en el panel \ (superior \) en lugar del [alimentador de DevTools][DevtoolsCustomizeIndexDrawer], consulte movimiento de [herramientas entre paneles](#move-tools-between-panels).</span><span class="sxs-lookup"><span data-stu-id="06857-130">To see **Network Console** in the main \(top\) panel instead of the [DevTools Drawer][DevtoolsCustomizeIndexDrawer], see [moving tools between panels](#move-tools-between-panels).</span></span>  

> [!NOTE]
> <span data-ttu-id="06857-131">Para habilitar el experimento, consulte [activar las características experimentales][DevtoolsExperimentalFeaturesTurnOn] y seleccione la casilla que se encuentra junto a **Habilitar la consola de red**.</span><span class="sxs-lookup"><span data-stu-id="06857-131">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable Network Console**.</span></span>  
> 
> <span data-ttu-id="06857-132">Abra el [registro de red][DevtoolsNetworkIndexLogActivity], abra el menú contextual \ (haga clic con el botón derecho del ratón \) y seleccione **Editar y reproducir**.</span><span class="sxs-lookup"><span data-stu-id="06857-132">Open the [Network Log][DevtoolsNetworkIndexLogActivity], open the contextual menu \(right-click\), and select **Edit and Replay**.</span></span>  

<span data-ttu-id="06857-133">[#1093687][CR1093687] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-133">Chromium issue [#1093687][CR1093687]</span></span>  

### <span data-ttu-id="06857-134">Eventos de respondWith de trabajo de servicio en la pestaña intervalos</span><span class="sxs-lookup"><span data-stu-id="06857-134">Service worker respondWith events in the Timing tab</span></span>  

<span data-ttu-id="06857-135">La ficha **intervalos** del panel **red** ahora incluye `respondWith` eventos de trabajo de servicio.</span><span class="sxs-lookup"><span data-stu-id="06857-135">The **Timing** tab of the **Network** panel now includes `respondWith` service worker events.</span></span>  <span data-ttu-id="06857-136">El `respondWith` evento de trabajo de servicio muestra la duración desde el momento en que el `fetch` controlador de eventos de trabajo de servicio comienza a ejecutarse hasta el momento en que `respondWith` se liquida la promesa del `fetch` controlador.</span><span class="sxs-lookup"><span data-stu-id="06857-136">The `respondWith` service worker event shows the duration from the time immediately before the service worker `fetch` event handler starts running to the time when the `respondWith` promise of the `fetch` handler is settled.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="El evento de trabajo del servicio respondWith en la ficha intervalos del panel red" lightbox="../../media/2020/06/timing-tab.msft.png":::
   <span data-ttu-id="06857-138">El `respondWith` evento de trabajo de servicio en la pestaña **intervalos** del panel **red**</span><span class="sxs-lookup"><span data-stu-id="06857-138">The `respondWith` service worker event in the **Timing** tab of the **Network** panel</span></span>  
:::image-end:::  

<span data-ttu-id="06857-139">Expanda la **respuesta recibida** para ver información adicional de la `fetch` respuesta como `CacheStorageCacheName` , `serviceWorkerResponseSource` y `ResponseTime` .</span><span class="sxs-lookup"><span data-stu-id="06857-139">Expand **Response received** to see additional information from the `fetch` response like `CacheStorageCacheName`, `serviceWorkerResponseSource`, and `ResponseTime`.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Expandir respuesta recibida para ver información adicional de la respuesta de Fetch" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   <span data-ttu-id="06857-141">Expandir **respuesta recibida** para ver información adicional de la `fetch` respuesta</span><span class="sxs-lookup"><span data-stu-id="06857-141">Expand **Response received** to see additional information from the `fetch` response</span></span>  
:::image-end:::  

<span data-ttu-id="06857-142">[#1066579][CR1066579] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-142">Chromium issue [#1066579][CR1066579]</span></span>  

### <span data-ttu-id="06857-143">Comentarios sobre webhint en el panel problemas</span><span class="sxs-lookup"><span data-stu-id="06857-143">webhint feedback in the Issues panel</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="06857-145">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="06857-145">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="06857-146">[webhint][WebhintMain] es una herramienta de código abierto que proporciona comentarios en tiempo real sobre accesibilidad, compatibilidad entre exploradores, seguridad, rendimiento, PWAs y otros problemas comunes de desarrollo web de los sitios Web.</span><span class="sxs-lookup"><span data-stu-id="06857-146">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="06857-147">Ahora puede ver comentarios sobre webhint en el panel [problemas][DevtoolsIssues] .</span><span class="sxs-lookup"><span data-stu-id="06857-147">You are now able to see webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="Comentarios sobre webhint en el panel problemas" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   <span data-ttu-id="06857-149">Comentarios sobre webhint en el panel problemas</span><span class="sxs-lookup"><span data-stu-id="06857-149">webhint feedback in the Issues panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="06857-150">Para habilitar el experimento, vea [activar las características experimentales][DevtoolsExperimentalFeaturesTurnOn] y seleccione la casilla que se encuentra junto a **Habilitar webhint**.</span><span class="sxs-lookup"><span data-stu-id="06857-150">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable webhint**.</span></span>  
> 
> <span data-ttu-id="06857-151">Abra el panel [problemas][DevtoolsIssues] para ver los comentarios de webhint.</span><span class="sxs-lookup"><span data-stu-id="06857-151">Open the [Issues][DevtoolsIssues] panel to see feedback from webhint.</span></span>  

<span data-ttu-id="06857-152">[#1070378][CR1070378] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-152">Chromium issue [#1070378][CR1070378]</span></span>  

### <span data-ttu-id="06857-153">Mover herramientas entre paneles</span><span class="sxs-lookup"><span data-stu-id="06857-153">Move tools between panels</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="06857-155">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="06857-155">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="06857-156">Normalmente, las herramientas, como **los elementos** y la **red** , solo se pueden abrir en el panel \ (parte superior \) de DevTools.</span><span class="sxs-lookup"><span data-stu-id="06857-156">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="06857-157">De forma similar, las herramientas, como la **vista 3D** y los **problemas** , solo se pueden abrir en el panel del cajón \ (inferior \) de DevTools.</span><span class="sxs-lookup"><span data-stu-id="06857-157">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="06857-158">Ahora puede personalizar el diseño de DevTools moviendo las herramientas entre los paneles superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="06857-158">You are now able to customize your DevTools layout by moving tools between the top and bottom panels.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Mover pestañas entre paneles" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   <span data-ttu-id="06857-160">Mover pestañas entre paneles</span><span class="sxs-lookup"><span data-stu-id="06857-160">Moving tabs between panels</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="06857-161">Para habilitar el experimento, vea [activar las características experimentales][DevtoolsExperimentalFeaturesTurnOn] y seleccione la casilla junto a **habilitar soporte técnico para mover las tabulaciones entre los paneles**.</span><span class="sxs-lookup"><span data-stu-id="06857-161">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable support to move tabs between panels**.</span></span>  

<span data-ttu-id="06857-162">[#897944][CR897944] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-162">Chromium issue [#897944][CR897944]</span></span>  

### <span data-ttu-id="06857-163">Información sobre herramientas de iniciador mejorada en el panel red</span><span class="sxs-lookup"><span data-stu-id="06857-163">Improved Initiator tooltip in the Network panel</span></span>  

<span data-ttu-id="06857-164">En Microsoft Edge 83 y 84, información sobre herramientas para la columna Initiator, que muestra la causa de la solicitud de recursos, en el [registro de red][DevtoolsNetworkIndexLogActivity] que se muestra con una barra de desplazamiento horizontal.</span><span class="sxs-lookup"><span data-stu-id="06857-164">In Microsoft Edge 83 and 84, tooltips for the Initiator column, which shows the cause of the resource request, in the [Network Log][DevtoolsNetworkIndexLogActivity] displayed with a horizontal scrollbar.</span></span>  <span data-ttu-id="06857-165">Solo pudimos ver la pila de llamadas que inició la solicitud desplazándose horizontalmente en la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="06857-165">You were only able to see the call stack that initiated the request by scrolling horizontally in the tooltip.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Información sobre herramientas de iniciador en Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   <span data-ttu-id="06857-167">Información sobre herramientas de iniciador en Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="06857-167">The Initiator tooltip in Microsoft Edge 84</span></span>  
:::image-end:::  

<span data-ttu-id="06857-168">A partir de Microsoft Edge 85, ahora puedes ver la pila de llamadas de iniciador en la información sobre herramientas sin tener que desplazarse horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="06857-168">Starting with Microsoft Edge 85, you are now able to see the Initiator call stack in the tooltip without scrolling horizontally.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Información sobre herramientas de iniciador en Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   <span data-ttu-id="06857-170">Información sobre herramientas de iniciador en Microsoft Edge 85</span><span class="sxs-lookup"><span data-stu-id="06857-170">The Initiator tooltip in Microsoft Edge 85</span></span>
:::image-end:::  

<span data-ttu-id="06857-171">[#1069404][CR1069404] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-171">Chromium issue [#1069404][CR1069404]</span></span>  

## <span data-ttu-id="06857-172">Anuncios del proyecto de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-172">Announcements from the Chromium project</span></span>  

<span data-ttu-id="06857-173">En las siguientes secciones se anuncian características adicionales disponibles en Microsoft Edge 85 que se han contribuido al proyecto de código abierto.</span><span class="sxs-lookup"><span data-stu-id="06857-173">The following sections announce additional features available in Microsoft Edge 85 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="06857-174">Edición de estilos para marcos CSS-en-JS</span><span class="sxs-lookup"><span data-stu-id="06857-174">Style editing for CSS-in-JS frameworks</span></span>  

<span data-ttu-id="06857-175">El panel **estilos** ahora tiene mejor compatibilidad para editar los estilos que se crearon con las API del [modelo de objetos CSS (CSSOM)][CsswgDraftsCssom] .</span><span class="sxs-lookup"><span data-stu-id="06857-175">The **Styles** pane now has better support for editing styles that were created with the [CSS Object Model (CSSOM)][CsswgDraftsCssom] APIs.</span></span>  <span data-ttu-id="06857-176">Muchos marcos y bibliotecas CSS-en-JS usan las API de CSSOM en el capó para construir estilos.</span><span class="sxs-lookup"><span data-stu-id="06857-176">Many CSS-in-JS frameworks and libraries use the CSSOM APIs under the hood to construct styles.</span></span>  

<span data-ttu-id="06857-177">Ahora puede editar los estilos agregados en JavaScript con [hojas de estilo construyebles][WicgConstructStylesheet].</span><span class="sxs-lookup"><span data-stu-id="06857-177">You are now able to edit styles added in JavaScript using [Constructable Stylesheets][WicgConstructStylesheet].</span></span>  <span data-ttu-id="06857-178">Las hojas de estilo creativas son una nueva forma de crear y distribuir estilos reutilizables al usar la [sombra de Dom][MdnShadowDom].</span><span class="sxs-lookup"><span data-stu-id="06857-178">Constructable Stylesheets are a new way to create and distribute reusable styles when using [Shadow DOM][MdnShadowDom].</span></span>  

<span data-ttu-id="06857-179">Por ejemplo, los `h1` estilos agregados con `CSSStyleSheet` \ (API de CSSOM \) no se podían modificar anteriormente.</span><span class="sxs-lookup"><span data-stu-id="06857-179">For example, the `h1` styles added with `CSSStyleSheet` \(CSSOM APIs\) were not editable previously.</span></span>  <span data-ttu-id="06857-180">Ahora los estilos se pueden editar en el panel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="06857-180">The styles are editable now in the **Styles** pane.</span></span>  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Cambiar la propiedad Background de los estilos H1 agregados con CSSStyleSheet de rosa a lightblue" lightbox="../../media/2020/06/css-in-js.msft.png":::
   <span data-ttu-id="06857-182">Cambiar la `background` propiedad de los `h1` estilos agregados con `CSSStyleSheet` from `pink` a `lightblue` .</span><span class="sxs-lookup"><span data-stu-id="06857-182">Changing the `background` property of the `h1` styles added with `CSSStyleSheet` from `pink` to `lightblue`.</span></span>
:::image-end:::  

<span data-ttu-id="06857-183">Proporciona a esta característica una prueba con un [ejemplo que usa CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span><span class="sxs-lookup"><span data-stu-id="06857-183">Give this feature a try with a [sample that uses CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span></span>

<span data-ttu-id="06857-184">[#946975][CR946975] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-184">Chromium issue [#946975][CR946975]</span></span>  

### <span data-ttu-id="06857-185">Lighthouse 6 en el panel de Lighthouse</span><span class="sxs-lookup"><span data-stu-id="06857-185">Lighthouse 6 in the Lighthouse panel</span></span>  

<span data-ttu-id="06857-186">El panel de **Lighthouse** ahora se ejecuta Lighthouse 6.</span><span class="sxs-lookup"><span data-stu-id="06857-186">The **Lighthouse** panel is now running Lighthouse 6.</span></span>  <span data-ttu-id="06857-187">Para obtener una lista completa de todos los cambios, consulte las notas de la [versión v 6.0.0][GithubGoogleChromeLighthouse600].</span><span class="sxs-lookup"><span data-stu-id="06857-187">For a full list of all changes, see [v6.0.0 release notes][GithubGoogleChromeLighthouse600].</span></span>  

<span data-ttu-id="06857-188">Lighthouse 6,0 introduce tres nuevas métricas en el informe: pintura con el contenido más grande \ (LCP \), turno de distribución acumulativa \ (CLS \) y tiempo de bloqueo total \ (TBT \).</span><span class="sxs-lookup"><span data-stu-id="06857-188">Lighthouse 6.0 introduces three new metrics to the report:  Largest Contentful Paint \(LCP\), Cumulative Layout Shift \(CLS\), and Total Blocking Time \(TBT\).</span></span>  

<span data-ttu-id="06857-189">La fórmula de puntuación de rendimiento también se ha recargado para reflejar mejor la experiencia de carga del usuario.</span><span class="sxs-lookup"><span data-stu-id="06857-189">The performance score formula has also been reweighted to better reflect the loading experience of the user.</span></span>  

<span data-ttu-id="06857-190">[#772558][CR772558] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-190">Chromium issue [#772558][CR772558]</span></span>  

#### <span data-ttu-id="06857-191">Primer desuso de pintura significativo</span><span class="sxs-lookup"><span data-stu-id="06857-191">First Meaningful Paint deprecation</span></span>  

<span data-ttu-id="06857-192">La primera pintura significativa \ (FMP \) está en desuso en Lighthouse 6,0.</span><span class="sxs-lookup"><span data-stu-id="06857-192">First Meaningful Paint \(FMP\) is deprecated in Lighthouse 6.0.</span></span>  <span data-ttu-id="06857-193">FMP también se ha eliminado del panel **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="06857-193">FMP has also been removed from the **Performance** panel.</span></span>  <span data-ttu-id="06857-194">La **mayor pintura** con el contenido es el reemplazo recomendado para FMP.</span><span class="sxs-lookup"><span data-stu-id="06857-194">**Largest Contentful Paint** is the recommended replacement for FMP.</span></span>  <!--See [First Meaningful Paint][WebDevFirstMeaningfulPaint] for an explanation of why it was deprecated.  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

<span data-ttu-id="06857-195">[#1096008][CR1096008] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-195">Chromium issue [#1096008][CR1096008]</span></span>  

### <span data-ttu-id="06857-196">Compatibilidad con las nuevas características de JavaScript</span><span class="sxs-lookup"><span data-stu-id="06857-196">Support for new JavaScript features</span></span>  

<span data-ttu-id="06857-197">DevTools ahora es una mejor compatibilidad para algunas de las características más recientes del lenguaje JavaScript.</span><span class="sxs-lookup"><span data-stu-id="06857-197">DevTools now has better support for some of the latest JavaScript language features.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="06857-198">Finalización automática de sintaxis de [encadenamiento opcional][V8DevOptionalChaining]</span><span class="sxs-lookup"><span data-stu-id="06857-198">[Optional chaining][V8DevOptionalChaining] syntax autocompletion</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="06857-199">La finalización automática de la propiedad en la **consola** ahora admite la sintaxis de encadenamiento opcional; por ejemplo,  `name?.` ahora funciona además de `name.` y `name[` .</span><span class="sxs-lookup"><span data-stu-id="06857-199">Property auto-completion in the **Console** now supports optional chaining syntax, for example,  `name?.` now works in addition to `name.` and `name[`.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="06857-200">Resaltado de sintaxis para [campos privados][V8DevClassFieldsPrivate]</span><span class="sxs-lookup"><span data-stu-id="06857-200">Syntax highlighting for [private fields][V8DevClassFieldsPrivate]</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="06857-201">Ahora, los campos de clase privados se resaltan correctamente y se resaltan en el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="06857-201">private class fields are now properly syntax-highlighted and pretty-printed in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="06857-202">Resaltado de sintaxis para el [operador de fusión con valores nulos][V8DevNullishCoalescing]</span><span class="sxs-lookup"><span data-stu-id="06857-202">Syntax highlighting for [Nullish coalescing operator][V8DevNullishCoalescing]</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="06857-203">Ahora DevTools correctamente: imprime el operador de fusión de NULL en el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="06857-203">DevTools now properly pretty-prints the nullish coalescing operator in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="06857-204">Problemas de cromo [#1073903][CR1073903], [#1083214][CR1083214] [#1083797][CR1083797]</span><span class="sxs-lookup"><span data-stu-id="06857-204">Chromium issues [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span></span>  

### <span data-ttu-id="06857-205">Advertencias de nuevo acceso directo a la aplicación en el panel manifiesto</span><span class="sxs-lookup"><span data-stu-id="06857-205">New app shortcut warnings in the Manifest pane</span></span>  

<span data-ttu-id="06857-206">Los **accesos directos a aplicaciones** ayudan a los usuarios a iniciar rápidamente las tareas comunes o recomendadas dentro de una aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="06857-206">**App shortcuts** help users quickly start common or recommended tasks within a web app.</span></span>  

<!--todo: add App shortcuts when section is live  -->  

<span data-ttu-id="06857-207">En el panel **manifiesto** ahora se muestran advertencias para las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="06857-207">The **Manifest** pane now shows warnings for the following conditions.</span></span>  

* <span data-ttu-id="06857-208">Los iconos de acceso directo de la aplicación son menores que 96 píxeles</span><span class="sxs-lookup"><span data-stu-id="06857-208">The app shortcut icons are smaller than 96x96 pixels</span></span>  
* <span data-ttu-id="06857-209">Los iconos de acceso directo de la aplicación y los iconos de manifiesto no son cuadrados \ (porque los iconos se ignoran \)</span><span class="sxs-lookup"><span data-stu-id="06857-209">The app shortcut icons and manifest icons are not square \(since the icons are ignored\)</span></span>  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Advertencias de acceso directo a la aplicación" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   <span data-ttu-id="06857-211">Advertencias de acceso directo a la aplicación</span><span class="sxs-lookup"><span data-stu-id="06857-211">App shortcut warnings</span></span>  
:::image-end:::  

<span data-ttu-id="06857-212">[#955497][CR955497] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-212">Chromium issue [#955497][CR955497]</span></span>  

### <span data-ttu-id="06857-213">Visualización coherente del panel calculado</span><span class="sxs-lookup"><span data-stu-id="06857-213">Consistent display of the Computed pane</span></span>  

<span data-ttu-id="06857-214">El panel **calculado** del panel **elementos** se muestra ahora de forma coherente en todos los tamaños de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="06857-214">The **Computed** pane in the **Elements** panel now displays consistently as a pane across all viewport sizes.</span></span>  <span data-ttu-id="06857-215">Anteriormente el panel **calculado** se combinó en el panel **estilos** cuando el ancho de la ventanilla de DevTools era estrecho.</span><span class="sxs-lookup"><span data-stu-id="06857-215">Previously the **Computed** pane merged inside the **Styles** pane when the width of the DevTools viewport was narrow.</span></span>  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="El panel calculado se muestra de forma coherente como un panel independiente incluso cuando el DevTools es estrecho." lightbox="../../media/2020/06/computed-pane.msft.png":::
   <span data-ttu-id="06857-217">El panel **calculado** se muestra de forma coherente como un panel independiente incluso cuando el DevTools es estrecho.</span><span class="sxs-lookup"><span data-stu-id="06857-217">The **Computed** pane consistently displays as a separate pane even when the DevTools are narrow.</span></span>
:::image-end:::  

<span data-ttu-id="06857-218">[#1073899][CR1073899] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-218">Chromium issue [#1073899][CR1073899]</span></span>  

### <span data-ttu-id="06857-219">Desplazamientos de código de bytes para archivos webassembly</span><span class="sxs-lookup"><span data-stu-id="06857-219">Bytecode offsets for WebAssembly files</span></span>  

<span data-ttu-id="06857-220">DevTools ahora usa desplazamientos de código de byte para mostrar los números de línea de WASM desensamblador.</span><span class="sxs-lookup"><span data-stu-id="06857-220">DevTools now uses bytecode offsets for displaying line numbers of Wasm disassembly.</span></span>  
<span data-ttu-id="06857-221">Los números de línea marcan más claramente que estás buscando datos binarios y son más coherentes con el modo en que el tiempo de ejecución de WASM hace referencia a ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="06857-221">The line numbers make it clearer that you are looking at binary data, and is more consistent with how the Wasm runtime references locations.</span></span>  

<span data-ttu-id="06857-222">[#1071432][CR1071432] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-222">Chromium issue [#1071432][CR1071432]</span></span>  

### <span data-ttu-id="06857-223">Copia y corte de línea en el panel orígenes</span><span class="sxs-lookup"><span data-stu-id="06857-223">Line-wise copy and cut in Sources Panel</span></span>  

<span data-ttu-id="06857-224">Al realizar una operación de copiar o cortar sin selección en el [Editor del panel orígenes][DevtoolsSourcesEditCssJavascript], DevTools copia o corta la línea de contenido actual.</span><span class="sxs-lookup"><span data-stu-id="06857-224">When performing copy or cut with no selection in the [Sources panel editor][DevtoolsSourcesEditCssJavascript], DevTools copies or cuts the current line of content.</span></span>  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Con el cursor al final de la línea 5, copiando toda la línea desde pen.js en el DevTools y pegando en VS" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   <span data-ttu-id="06857-226">Con el cursor al final de la línea 5, copiando toda la línea desde **pen.js** en el DevTools y pegando en [vs Code][VSCode].</span><span class="sxs-lookup"><span data-stu-id="06857-226">With the cursor at the end of Line 5, copying the whole line from **pen.js** in the DevTools and pasting in [VS Code][VSCode].</span></span>
:::image-end:::  

<span data-ttu-id="06857-227">[#800028][CR800028] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-227">Chromium issue [#800028][CR800028]</span></span>

### <span data-ttu-id="06857-228">Actualizaciones de configuración de consola</span><span class="sxs-lookup"><span data-stu-id="06857-228">Console Settings updates</span></span>  

#### <span data-ttu-id="06857-229">Desagrupar los mismos mensajes de consola</span><span class="sxs-lookup"><span data-stu-id="06857-229">Ungroup same console messages</span></span>  

<span data-ttu-id="06857-230">El botón de alternancia **similar** en la configuración de la consola se aplica a los mensajes duplicados.</span><span class="sxs-lookup"><span data-stu-id="06857-230">The **Group similar** toggle in Console Settings now applies to duplicate messages.</span></span>  <span data-ttu-id="06857-231">Anteriormente se acaba de aplicar a mensajes similares.</span><span class="sxs-lookup"><span data-stu-id="06857-231">Previously it just applied to similar messages.</span></span>  

<span data-ttu-id="06857-232">Por ejemplo, anteriormente, DevTools no desagrupaba los `hello` mensajes aunque el **grupo es similar** .</span><span class="sxs-lookup"><span data-stu-id="06857-232">For example, previously, DevTools did not ungroup the `hello` messages even though **Group similar** is unchecked.</span></span>  <span data-ttu-id="06857-233">Ahora, los `hello` mensajes están desagrupados.</span><span class="sxs-lookup"><span data-stu-id="06857-233">Now, the `hello` messages are ungrouped.</span></span>  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Cuando agrupar similares está desactivado, los mensajes de saludo no se agrupan" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   <span data-ttu-id="06857-235">Cuando **agrupar similares** está desactivado, los `hello` mensajes no se agrupan.</span><span class="sxs-lookup"><span data-stu-id="06857-235">When **Group similar** is unchecked, the `hello` messages are ungrouped.</span></span>
:::image-end:::  

<span data-ttu-id="06857-236">Proporciona a esta característica una prueba con un [ejemplo que envía mensajes duplicados a la consola][CodepenZoherghadyaliZyrjgdJ].</span><span class="sxs-lookup"><span data-stu-id="06857-236">Give this feature a try with a [sample that sends duplicate messages to the Console][CodepenZoherghadyaliZyrjgdJ].</span></span>  

<span data-ttu-id="06857-237">[#1082963][CR1082963] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-237">Chromium issue [#1082963][CR1082963]</span></span>  

### <span data-ttu-id="06857-238">Conservar la configuración de solo contexto seleccionada</span><span class="sxs-lookup"><span data-stu-id="06857-238">Persisting Selected context only settings</span></span>  

<span data-ttu-id="06857-239">La configuración de **contexto seleccionada solo** en la configuración de la consola se conserva.</span><span class="sxs-lookup"><span data-stu-id="06857-239">The **Selected context only** settings in Console Settings is now persisted.</span></span>  <span data-ttu-id="06857-240">Anteriormente, la configuración se restableció cada vez que cerraste y reabros DevTools.</span><span class="sxs-lookup"><span data-stu-id="06857-240">Previously the settings were reset every time you closed and reopened DevTools.</span></span>  <span data-ttu-id="06857-241">El cambio hace que el ajuste del comportamiento sea coherente con otras opciones de configuración de la consola.</span><span class="sxs-lookup"><span data-stu-id="06857-241">The change makes the setting behavior consistent with other Console Settings options.</span></span>  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Configuración de contexto seleccionado únicamente" lightbox="../../media/2020/06/selected-context.msft.png":::
   <span data-ttu-id="06857-243">Configuración de **contexto seleccionado únicamente**</span><span class="sxs-lookup"><span data-stu-id="06857-243">**Selected context only** setting</span></span>  
:::image-end:::  

<span data-ttu-id="06857-244">[#1055875][CR1055875] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-244">Chromium issue [#1055875][CR1055875]</span></span>  

### <span data-ttu-id="06857-245">Actualizaciones del panel de rendimiento</span><span class="sxs-lookup"><span data-stu-id="06857-245">Performance panel updates</span></span>  

#### <span data-ttu-id="06857-246">Información de caché de compilación de JavaScript en el panel rendimiento</span><span class="sxs-lookup"><span data-stu-id="06857-246">JavaScript compilation cache information in Performance panel</span></span>  

<span data-ttu-id="06857-247">La información de la [caché de compilación de JavaScript][V8DevCodeCaching] se muestra ahora siempre en la pestaña Resumen del panel rendimiento.</span><span class="sxs-lookup"><span data-stu-id="06857-247">[JavaScript compilation cache information][V8DevCodeCaching] is now always displayed in the Summary tab of the Performance panel.</span></span>  <span data-ttu-id="06857-248">Anteriormente, DevTools no mostraba nada relacionado con el almacenamiento en caché del código si no se produjera el almacenamiento en caché de código.</span><span class="sxs-lookup"><span data-stu-id="06857-248">Previously, DevTools did not show anything related to code caching if code caching did not happen.</span></span>  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Información de caché de compilación de JavaScript" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   <span data-ttu-id="06857-250">Información de caché de compilación de JavaScript</span><span class="sxs-lookup"><span data-stu-id="06857-250">JavaScript compilation cache information</span></span>  
:::image-end:::  

<span data-ttu-id="06857-251">[#912581][CR912581] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-251">Chromium issue [#912581][CR912581]</span></span>  

#### <span data-ttu-id="06857-252">Alineación de la navegación en el panel rendimiento</span><span class="sxs-lookup"><span data-stu-id="06857-252">Navigation timing alignment in the Performance panel</span></span>  

<span data-ttu-id="06857-253">El panel de **rendimiento** que se usa para mostrar las horas en las reglas en función del inicio de la grabación.</span><span class="sxs-lookup"><span data-stu-id="06857-253">The **Performance** panel used to show times in the rulers based on when the recording started.</span></span>  <span data-ttu-id="06857-254">Ahora se ha cambiado el intervalo de tiempo para las grabaciones en las que el usuario navega, donde DevTools ahora muestra las horas relacionadas con la navegación.</span><span class="sxs-lookup"><span data-stu-id="06857-254">The timing has now changed for recordings where the user navigates, where DevTools now shows ruler times relative to the navigation instead.</span></span>  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Alinear los intervalos de navegación en el panel rendimiento" lightbox="../../media/2020/06/nav-timing.msft.png":::
   <span data-ttu-id="06857-256">Alinear los intervalos de navegación en el panel **rendimiento**</span><span class="sxs-lookup"><span data-stu-id="06857-256">Align navigation timing in **Performance** panel</span></span>  
:::image-end:::  

<span data-ttu-id="06857-257">Las horas de `DOMContentLoaded` , primera pintura con control de contenido y los mayores eventos de pintura con contenido se actualizan para que sean relativas al inicio de la navegación, lo que significa que los intervalos coinciden con los intervalos que informaron `PerformanceObserver` .</span><span class="sxs-lookup"><span data-stu-id="06857-257">The times for `DOMContentLoaded`, First Paint, First Contentful Paint, and Largest Contentful Paint events are updated to be relative to the start of the navigation, which means the timing matches the timings reported by `PerformanceObserver`.</span></span>  

<span data-ttu-id="06857-258">[#974550][CR974550] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-258">Chromium issue [#974550][CR974550]</span></span>  

### <span data-ttu-id="06857-259">Nuevos iconos para puntos de interrupción, puntos de interrupción condicionales y logpoints</span><span class="sxs-lookup"><span data-stu-id="06857-259">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="06857-260">El panel **orígenes** tiene nuevos diseños para puntos de interrupción, puntos de interrupción condicionales y logpoints.</span><span class="sxs-lookup"><span data-stu-id="06857-260">The **Sources** panel has new designs for breakpoints, conditional breakpoints, and logpoints.</span></span>  <span data-ttu-id="06857-261">Los puntos de interrupción están representados por un círculo rojo, como [vs Code][VSCode] y [Visual Studio][VS].</span><span class="sxs-lookup"><span data-stu-id="06857-261">Breakpoints are represented by a red circle, just like [VS Code][VSCode] and [Visual Studio][VS].</span></span>  <span data-ttu-id="06857-262">Se agregan iconos para diferenciar los puntos de interrupción y logpoints.</span><span class="sxs-lookup"><span data-stu-id="06857-262">Icons are added to differentiate conditional breakpoints and logpoints.</span></span>  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Puntos de interrupción" lightbox="../../media/2020/06/breakpoints.msft.png":::
   <span data-ttu-id="06857-264">Puntos de interrupción</span><span class="sxs-lookup"><span data-stu-id="06857-264">Breakpoints</span></span>  
:::image-end:::  

<span data-ttu-id="06857-265">[#1041830][CR1041830] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="06857-265">Chromium issue [#1041830][CR1041830]</span></span>  

## <span data-ttu-id="06857-266">Descargar los canales de Microsoft Edge Preview</span><span class="sxs-lookup"><span data-stu-id="06857-266">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="06857-267">Si está en Windows o macOS, considere la posibilidad de usar los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="06857-267">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="06857-268">Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="06857-268">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="06857-269">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="06857-269">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Cajón-personalizar Microsoft Edge DevTools | Microsoft docs"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activar características experimentales: características experimentales | Microsoft docs"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Buscar y solucionar problemas con la herramienta de problemas de Microsoft Edge DevTools | Microsoft docs"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Información general del panel editar CSS y JavaScript | Microsoft docs"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Registrar actividad de red: inspeccionar actividad de red en Microsoft Edge DevTools | Microsoft docs"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Edición de estilos para marcos CSS-en-JS | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Enviar mensajes duplicados a la consola | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Ejemplo de programador de cuadrícula CSS | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de cromo"  

[CR772558]: https://crbug.com/772558 "DevTools: actualizar a la última versión de Lighthouse | Errores de cromo"  
[CR800028]: https://crbug.com/800028 "El método abreviado de línea duplicado en el editor herramientas de desarrollo no funciona después de la actualización Chrome | Errores de cromo"  
[CR912581]: https://crbug.com/912581 "Exponga qué scripts se almacenaron en caché de código en V8 en DevTools/acerca de: Tracing | Errores de cromo"  
[CR946975]: https://crbug.com/946975 "La barra lateral estilos de DevTools no funciona con hojas de estilos construidas | Errores de cromo"  
[CR955497]: https://crbug.com/955497 "Menú contextual del icono de la aplicación para PWAs | Errores de cromo"  
[CR974550]: https://crbug.com/974550 "La métrica entre el panel de rendimiento y performanceObserver | Errores de cromo"  
[CR1041830]: https://crbug.com/1041830 "Mejorar los colores de los puntos de interrupción | Errores de cromo"  
[CR1055875]: https://crbug.com/1055875 "El valor de la configuración de la consola solo de contexto seleccionado no se conserva después de cerrar y volver a abrir las herramientas de desarrollo | Errores de cromo"  
[CR1066579]: https://crbug.com/1066579 "DevTools: Mostrar la escala de tiempo de captura de ServiceWorkers por solicitud en el panel red | Errores de cromo"  
[CR1071432]: https://crbug.com/1071432 "Experiencia de desarrollador básica de WASM | Errores de cromo"  
[CR1073899]: https://crbug.com/1073899 "La pestaña de estilo calculado desaparece en modo de respuesta | Errores de cromo"  
[CR1073903]: https://crbug.com/1073903 "DevTools: el resaltado de sintaxis no funciona con los campos privados | Errores de cromo"  
[CR1082963]: https://crbug.com/1082963 "No se puede deshabilitar el grupo de consola de mensajes similares comportamiento | Errores de cromo"  
[CR1083214]: https://crbug.com/1083214 "ACORN no admite el encadenamiento opcional | Errores de cromo"  
[CR1083797]: https://crbug.com/1083797 "Impresión con sangría dañada para la combinación nula | Errores de cromo"  
[CR1096008]: https://crbug.com/1096008 "Quitar FMP | Errores de cromo"  
[CR1047356]: https://crbug.com/1047356 "Herramientas CSS/Flexbox/tables de CSS | Errores de cromo"  
[CR1093687]: https://crbug.com/1093687 "Herramienta crear y reproducir solicitudes de red sintéticas | Errores de cromo"  
[CR1070378]: https://crbug.com/1070378 "Integrar webhint en DevTools | Errores de cromo"  
[CR1069404]: https://crbug.com/1069404 "Las ventanas emergentes de widgets de [dev Tools] son demasiado limitadas | Errores de cromo"  
[CR897944]: https://crbug.com/897944 "Paneles de devtool arrastrables | Errores de cromo"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v 6.0.0-GoogleChrome/Lighthouse | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nuevo problema: MicrosoftDocs/Edge-Developer"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Usar DOM de sombra | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Canales de Microsoft Edge Preview"  

[VS]: https://visualstudio.microsoft.com/ "Visual Studio"
[VSCode]: https://code.visualstudio.com/ "Código de Visual Studio"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Modelo de objetos CSS (CSSOM) | Borradores del editor del grupo de trabajo CSS W3C"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools cuenta de Twitter"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Campos de clase privados: campos de clase pública y privada | V8. Desarrolladores"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Almacenamiento en caché de código para desarrolladores de JavaScript | V8. Desarrolladores"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Fusión nula | V8. Desarrolladores"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Encadenamiento opcional | V8. Desarrolladores"  

[WebhintMain]: https://webhint.io "sugerencia"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Objetos de hoja de estilos que se construyen | Autoincubadora CG"

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
> <span data-ttu-id="06857-318">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="06857-318">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="06857-319">La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/06/devtools/index) y está creada por [Jecelyn Yeen][JecelynYeen] \ (defensor para desarrolladores, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="06857-319">The original page is found [here](https://developers.google.com/web/updates/2020/06/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="06857-321">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="06857-321">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
description: Las últimas características experimentales de Microsoft Edge DevTools
title: Características experimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/04/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, experiment
ms.openlocfilehash: 32eaa3e8d41efefa669142297891e7c62cf4eb5b
ms.sourcegitcommit: d53421b7219ad87fa9d58f601d9c61ee44c2e43a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313468"
---
# <span data-ttu-id="b69d3-104">Características experimentales</span><span class="sxs-lookup"><span data-stu-id="b69d3-104">Experimental features</span></span>  

<span data-ttu-id="b69d3-105">Las DevTools de Microsoft Edge proporcionan acceso a características experimentales que aún están en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="b69d3-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="b69d3-106">Puedes probar y [proporcionar comentarios antes de](#providing-feedback-on-experimental-features) que se lanza cada característica.</span><span class="sxs-lookup"><span data-stu-id="b69d3-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="b69d3-107">Aunque las características experimentales están disponibles en todos los canales de Microsoft Edge, puede obtener las últimas características experimentales con el canal Canary de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b69d3-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <span data-ttu-id="b69d3-108">Activar características experimentales</span><span class="sxs-lookup"><span data-stu-id="b69d3-108">Turn on experimental features</span></span>  

<span data-ttu-id="b69d3-109">Para activar \(o desactivar\) las características experimentales en Microsoft Edge, sigue estos pasos.</span><span class="sxs-lookup"><span data-stu-id="b69d3-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="b69d3-110">[Abra DevTools][DevtoolsOpenMain].</span><span class="sxs-lookup"><span data-stu-id="b69d3-110">[Open DevTools][DevtoolsOpenMain].</span></span>  
    *   <span data-ttu-id="b69d3-111">Selecciona `Control` + `Shift` + `I` \(Windows, Linux\) o `Command` + `Option` + `I` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="b69d3-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="b69d3-112">Para obtener más información, vaya a [los métodos abreviados de teclado de DevTools de Microsoft Edge.][DevToolsShortcuts]</span><span class="sxs-lookup"><span data-stu-id="b69d3-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="b69d3-113">Abra el [panel][DevToolsCustomizeIndexSettings] Configuración.</span><span class="sxs-lookup"><span data-stu-id="b69d3-113">Open the [Settings][DevToolsCustomizeIndexSettings] pane.</span></span>  
    *   <span data-ttu-id="b69d3-114">Seleccione `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="b69d3-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="b69d3-115">Para obtener más información, vaya a [los métodos abreviados de teclado de DevTools de Microsoft Edge.][DevToolsShortcuts]</span><span class="sxs-lookup"><span data-stu-id="b69d3-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="b69d3-116">En el lado izquierdo del **panel** Configuración, elija la **sección** Experimentos.</span><span class="sxs-lookup"><span data-stu-id="b69d3-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="La página Experimentos en Configuración" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="b69d3-118">La **página Experimentos** en **Configuración**</span><span class="sxs-lookup"><span data-stu-id="b69d3-118">The **Experiments** page in **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b69d3-119">En la **página Experimentos, desplázate** por la lista de todas las características experimentales disponibles y elige la casilla junto a cada característica que quieras probar.</span><span class="sxs-lookup"><span data-stu-id="b69d3-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="b69d3-120">Cierre y vuelva a abrir Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="b69d3-121">Las características experimentales se actualizan constantemente y pueden causar problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b69d3-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="b69d3-122">Para desactivar una característica experimental, abre la página **Experimentos** y desactiva la casilla de la característica experimental que quieres desactivar.</span><span class="sxs-lookup"><span data-stu-id="b69d3-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <span data-ttu-id="b69d3-123">Características experimentales resaltadas</span><span class="sxs-lookup"><span data-stu-id="b69d3-123">Highlighted experimental features</span></span>  

<span data-ttu-id="b69d3-124">En las secciones siguientes se describen las nuevas características experimentales que están disponibles en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b69d3-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="b69d3-125">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="b69d3-125">Experimental feature</span></span> | <span data-ttu-id="b69d3-126">Versión de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b69d3-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="b69d3-127">Habilitar webhint</span><span class="sxs-lookup"><span data-stu-id="b69d3-127">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="b69d3-128">85 o posterior</span><span class="sxs-lookup"><span data-stu-id="b69d3-128">85 or later</span></span> |  
| [<span data-ttu-id="b69d3-129">Habilitar consola de red</span><span class="sxs-lookup"><span data-stu-id="b69d3-129">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="b69d3-130">85 o posterior</span><span class="sxs-lookup"><span data-stu-id="b69d3-130">85 or later</span></span> |  
| [<span data-ttu-id="b69d3-131">Visor de pedidos de origen</span><span class="sxs-lookup"><span data-stu-id="b69d3-131">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="b69d3-132">86 o posterior</span><span class="sxs-lookup"><span data-stu-id="b69d3-132">86 or later</span></span> |  
| [<span data-ttu-id="b69d3-133">Habilitar el editor de métodos abreviados de teclado</span><span class="sxs-lookup"><span data-stu-id="b69d3-133">Enable keyboard shortcut editor</span></span>](#enable-keyboard-shortcut-editor) | <span data-ttu-id="b69d3-134">87 o posterior</span><span class="sxs-lookup"><span data-stu-id="b69d3-134">87 or later</span></span> |  
| [<span data-ttu-id="b69d3-135">Habilitar capas compuestas en la vista 3D</span><span class="sxs-lookup"><span data-stu-id="b69d3-135">Enable Composited Layers in 3D View</span></span>](#enable-composited-layers-in-3d-view) | <span data-ttu-id="b69d3-136">87 o posterior</span><span class="sxs-lookup"><span data-stu-id="b69d3-136">87 or later</span></span> |  
| [<span data-ttu-id="b69d3-137">Habilitar la nueva herramienta Editor de fuentes en el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="b69d3-137">Enable new Font Editor tool within the Styles pane</span></span>](#enable-new-font-editor-tool-within-the-styles-pane) | <span data-ttu-id="b69d3-138">89 o posterior</span><span class="sxs-lookup"><span data-stu-id="b69d3-138">89 or later</span></span> |  
| [<span data-ttu-id="b69d3-139">Habilitar nuevas características de depuración de CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="b69d3-139">Enable new CSS Flexbox debugging features</span></span>](#enable-new-css-flexbox-debugging-features) | <span data-ttu-id="b69d3-140">89 o posterior</span><span class="sxs-lookup"><span data-stu-id="b69d3-140">89 or later</span></span> |  
| [<span data-ttu-id="b69d3-141">Habilitar los menús de la pestaña + botón para abrir más herramientas</span><span class="sxs-lookup"><span data-stu-id="b69d3-141">Enable + button tab menus to open more tools</span></span>](#enable--button-tab-menus-to-open-more-tools) | <span data-ttu-id="b69d3-142">89 o posterior</span><span class="sxs-lookup"><span data-stu-id="b69d3-142">89 or later</span></span> |  
| [<span data-ttu-id="b69d3-143">Habilitar la pestaña de bienvenida</span><span class="sxs-lookup"><span data-stu-id="b69d3-143">Enable Welcome tab</span></span>](#enable-welcome-tool) | <span data-ttu-id="b69d3-144">89 o posterior</span><span class="sxs-lookup"><span data-stu-id="b69d3-144">89 or later</span></span> |  

### <span data-ttu-id="b69d3-145">Habilitar nuevas características de depuración de cuadrícula CSS</span><span class="sxs-lookup"><span data-stu-id="b69d3-145">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="b69d3-146">Esta característica experimental proporciona una serie de visualizaciones nuevas que te ayudarán a depurar diseños de cuadrícula CSS.</span><span class="sxs-lookup"><span data-stu-id="b69d3-146">This experimental feature provides a number of new visualizations to help you debug CSS grid layouts.</span></span>  <span data-ttu-id="b69d3-147">Para obtener una vista previa de las características experimentales más recientes, [habilita este experimento](#turn-on-experimental-features) y vuelve a cargar DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-147">To preview the latest experimental features, [enable this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  <span data-ttu-id="b69d3-148">Este experimento está en modo predeterminado en Microsoft Edge versión 87 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b69d3-148">This experiment is on by default in Microsoft Edge version 87 or later.</span></span>  

#### <span data-ttu-id="b69d3-149">Visualización de superposiciones de cuadrícula activa con la herramienta Inspeccionar</span><span class="sxs-lookup"><span data-stu-id="b69d3-149">Viewing on-hover grid overlays with the Inspect tool</span></span>  

<span data-ttu-id="b69d3-150">La **herramienta Inspect** proporciona una forma rápida de identificar y visualizar diseños de cuadrícula CSS en un sitio web al pasar el puntero sobre ellos con el mouse.</span><span class="sxs-lookup"><span data-stu-id="b69d3-150">The **Inspect** tool provides a quick way to identify and visualize CSS Grid layouts in a website by hovering over them with the mouse.</span></span>  <span data-ttu-id="b69d3-151">Elija el **icono Inspeccionar** \( Inspeccionar \) en la esquina superior izquierda ![ de ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-151">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="b69d3-152">A continuación, mantenga el mouse sobre un elemento Grid en el sitio web que está depurando.</span><span class="sxs-lookup"><span data-stu-id="b69d3-152">Then, hover over a Grid element on the website you are debugging.</span></span>  <span data-ttu-id="b69d3-153">Los contornos se muestran alrededor de la cuadrícula y el sombreado indica la ubicación de las separaciones de cuadrícula si están presentes.</span><span class="sxs-lookup"><span data-stu-id="b69d3-153">Outlines are displayed around the grid, and shading indicates the location of grid gaps if present.</span></span>  

:::image type="complex" source="../media/grid-inspect.msft.png" alt-text="Visualización de cuadrículas con la herramienta Inspeccionar" lightbox="../media/grid-inspect.msft.png":::
   <span data-ttu-id="b69d3-155">Visualización de cuadrículas con la **herramienta Inspeccionar**</span><span class="sxs-lookup"><span data-stu-id="b69d3-155">Viewing grids with the **Inspect** tool</span></span>  
:::image-end:::  

#### <span data-ttu-id="b69d3-156">Visualización de superposiciones de cuadrícula persistentes</span><span class="sxs-lookup"><span data-stu-id="b69d3-156">Viewing persistent grid overlays</span></span>  

<span data-ttu-id="b69d3-157">En Microsoft Edge versión 86 o posterior, la característica experimental de cuadrícula CSS también ofrece la opción de habilitar las superposiciones de cuadrícula persistentes.</span><span class="sxs-lookup"><span data-stu-id="b69d3-157">In Microsoft Edge version 86 or later, the experimental CSS grid feature also offers the option to enable persistent Grid overlays.</span></span>  <span data-ttu-id="b69d3-158">Las superposiciones persistentes proporcionan varias ventajas.</span><span class="sxs-lookup"><span data-stu-id="b69d3-158">The persistent overlays provide several benefits.</span></span>  

*   <span data-ttu-id="b69d3-159">Las superposiciones persistentes permanecen visibles en la página mientras se desplaza, mueve el mouse y usa otras características de DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-159">The persistent overlays remain visible on the page as you scroll, move your mouse, and use other features of the DevTools.</span></span>  
*   <span data-ttu-id="b69d3-160">Se pueden habilitar varias superposiciones persistentes al mismo tiempo, lo que te permite revisar varios diseños de cuadrícula a la vez.</span><span class="sxs-lookup"><span data-stu-id="b69d3-160">Multiple persistent overlays can be enabled at the same time, allowing you to review several grid layouts at once.</span></span>  
*   <span data-ttu-id="b69d3-161">Las superposiciones persistentes ofrecen muchas opciones de configuración, como ocultar o mostrar nombres en el área de cuadrícula, intervalos de cuadrícula, tamaños de pista, entre otros.</span><span class="sxs-lookup"><span data-stu-id="b69d3-161">Persistent overlays offer many configuration options, such as hiding or showing names in the grid area, grid gaps, track sizes, and so on.</span></span>  
    
<span data-ttu-id="b69d3-162">Las dos formas de alternar una superposición de cuadrícula persistente.</span><span class="sxs-lookup"><span data-stu-id="b69d3-162">The two ways to toggle a persistent grid overlay.</span></span>  

*   <span data-ttu-id="b69d3-163">Elige el **icono de** óvalo De cuadrícula junto a cualquier elemento Grid que se muestra en el árbol DOM de la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="b69d3-163">Choose the **Grid** oval icon next to any Grid element shown in the DOM tree of the **Elements** tool.</span></span>  
    
    :::image type="complex" source="../media/grid-adorner.msft.png" alt-text="Icono de óvalo de cuadrícula en la herramienta Elementos" lightbox="../media/grid-adorner.msft.png":::
       <span data-ttu-id="b69d3-165">Icono de óvalo de cuadrícula en **la herramienta** Elementos</span><span class="sxs-lookup"><span data-stu-id="b69d3-165">Grid oval icon in **Elements** tool</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="b69d3-166">Abre el nuevo panel **Diseño** ubicado en la herramienta Elementos y elige la casilla junto a cada elemento grid que quieras resaltar.</span><span class="sxs-lookup"><span data-stu-id="b69d3-166">Open the new **Layout** panel located in the Elements tool, and choose the checkbox next to each Grid element you want to highlight.</span></span>  
    
    :::image type="complex" source="../media/grid-layout-zoom.msft.png" alt-text="Panel de diseño en DevTools" lightbox="../media/grid-layout-zoom.msft.png":::
       <span data-ttu-id="b69d3-168">Panel **de** diseño en DevTools</span><span class="sxs-lookup"><span data-stu-id="b69d3-168">**Layout** panel in DevTools</span></span>  
    :::image-end:::  
    
#### <span data-ttu-id="b69d3-169">Configuración de superposiciones persistentes</span><span class="sxs-lookup"><span data-stu-id="b69d3-169">Configuring persistent overlays</span></span>  

<span data-ttu-id="b69d3-170">En Microsoft Edge versión 86 o posterior, el \*\*\*\* **nuevo** panel \*\*\*\* Diseño se encuentra en la herramienta Elementos junto con las pestañas **Estilos** y Calculados.</span><span class="sxs-lookup"><span data-stu-id="b69d3-170">In Microsoft Edge version 86 or later, the new **Layout** panel is located in the **Elements** tool alongside the **Styles** and **Computed** tabs.</span></span>  <span data-ttu-id="b69d3-171">El panel **Diseño** muestra las opciones de configuración de las superposiciones persistentes.</span><span class="sxs-lookup"><span data-stu-id="b69d3-171">The **Layout** panel surfaces configuration options for persistent overlays.</span></span>  

:::image type="complex" source="../media/experiments-grid.msft.png" alt-text="Característica de depuración de cuadrícula CSS" lightbox="../media/experiments-grid.msft.png":::
   <span data-ttu-id="b69d3-173">Característica de depuración de cuadrícula CSS</span><span class="sxs-lookup"><span data-stu-id="b69d3-173">CSS grid debugging feature</span></span>  
:::image-end:::  

### <span data-ttu-id="b69d3-174">Habilitar la compatibilidad para mover fichas entre paneles</span><span class="sxs-lookup"><span data-stu-id="b69d3-174">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="b69d3-175">Normalmente, herramientas como **Elementos** y **Red** solo se pueden abrir en el panel principal que se encuentra en la parte superior de Las DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-175">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="b69d3-176">Herramientas como **vista 3D** y **problemas** que normalmente solo se abren en el **panel** de cajón que se encuentra en la parte inferior de DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-176">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="b69d3-177">Después de elegir el experimento, puedes mover herramientas entre los paneles superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="b69d3-177">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="b69d3-178">Para mover una herramienta, mantenga el mouse sobre la pestaña, abra \*\*\*\* el menú contextual \(haga clic con el botón secundario\) y elija Mover a la parte superior o **Mover a la parte inferior.**</span><span class="sxs-lookup"><span data-stu-id="b69d3-178">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="b69d3-179">Este experimento te permite personalizar el diseño de DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-179">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="b69d3-180">Para mostrar u ocultar el panel **Del cajón,** seleccione `Escape` .</span><span class="sxs-lookup"><span data-stu-id="b69d3-180">To display or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Mover fichas entre paneles" lightbox="../media/experiments-move-panels.msft.png":::
   <span data-ttu-id="b69d3-182">Mover fichas entre paneles</span><span class="sxs-lookup"><span data-stu-id="b69d3-182">Moving tabs between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="b69d3-183">Habilitar webhint</span><span class="sxs-lookup"><span data-stu-id="b69d3-183">Enable webhint</span></span>  

<span data-ttu-id="b69d3-184">[webhint es][WebhintMain] una herramienta de código abierto que proporciona comentarios en tiempo real para sitios web y páginas web locales.</span><span class="sxs-lookup"><span data-stu-id="b69d3-184">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="b69d3-185">El tipo de comentarios proporcionados por [webhint][WebhintMain].</span><span class="sxs-lookup"><span data-stu-id="b69d3-185">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="b69d3-186">accesibilidad</span><span class="sxs-lookup"><span data-stu-id="b69d3-186">accessibility</span></span>  
*   <span data-ttu-id="b69d3-187">compatibilidad entre exploradores</span><span class="sxs-lookup"><span data-stu-id="b69d3-187">cross-browser compatibility</span></span>  
*   <span data-ttu-id="b69d3-188">seguridad</span><span class="sxs-lookup"><span data-stu-id="b69d3-188">security</span></span>  
*   <span data-ttu-id="b69d3-189">rendimiento</span><span class="sxs-lookup"><span data-stu-id="b69d3-189">performance</span></span>  
*   <span data-ttu-id="b69d3-190">Aplicaciones web progresivas (PDA)</span><span class="sxs-lookup"><span data-stu-id="b69d3-190">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="b69d3-191">otros problemas comunes de desarrollo web</span><span class="sxs-lookup"><span data-stu-id="b69d3-191">other common web development issues</span></span>  
    
<span data-ttu-id="b69d3-192">El [experimento de webhint][WebhintMain] muestra los comentarios de webhint en el panel [Problemas.][DevtoolsIssues]</span><span class="sxs-lookup"><span data-stu-id="b69d3-192">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="b69d3-193">Elija un problema para mostrar la documentación de la solución y una lista de los recursos afectados en su sitio web.</span><span class="sxs-lookup"><span data-stu-id="b69d3-193">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="b69d3-194">Elige un vínculo de recurso para abrir el panel **Red,** **Orígenes**o **Elementos** relevante en DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-194">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="comentarios de webhint en el panel Problemas" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="b69d3-196">comentarios de webhint en el panel **Problemas**</span><span class="sxs-lookup"><span data-stu-id="b69d3-196">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="b69d3-197">Habilitar consola de red</span><span class="sxs-lookup"><span data-stu-id="b69d3-197">Enable Network Console</span></span>  

<span data-ttu-id="b69d3-198">**Consola de** red es el título de trabajo de un experimento para realizar solicitudes de red sintéticas a través de HTTP.</span><span class="sxs-lookup"><span data-stu-id="b69d3-198">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="b69d3-199">Puedes usar el experimento **de consola de** red para enviar solicitudes de API web.</span><span class="sxs-lookup"><span data-stu-id="b69d3-199">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="b69d3-200">Después de activar el experimento, asegúrate de reiniciar DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-200">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="b69d3-201">Para usar la **Consola de red,** siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="b69d3-201">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="b69d3-202">Abra el **panel** Red.</span><span class="sxs-lookup"><span data-stu-id="b69d3-202">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="b69d3-203">Busque la solicitud de red que desea cambiar y volver a enviar.</span><span class="sxs-lookup"><span data-stu-id="b69d3-203">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="b69d3-204">Abra el menú contextual \(right-click\) y elija **Editar y reproducir.**</span><span class="sxs-lookup"><span data-stu-id="b69d3-204">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="b69d3-205">Cuando se **abra la consola de** red, edite la información de solicitud de red.</span><span class="sxs-lookup"><span data-stu-id="b69d3-205">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="b69d3-206">Elija **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="b69d3-206">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Consola de red en el cajón de la consola" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="b69d3-208">**Consola de red** en el **cajón de la** consola</span><span class="sxs-lookup"><span data-stu-id="b69d3-208">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <span data-ttu-id="b69d3-209">Visor de pedidos de origen</span><span class="sxs-lookup"><span data-stu-id="b69d3-209">Source Order Viewer</span></span>  

<span data-ttu-id="b69d3-210">**El Visor de orden de** origen es un experimento que muestra el orden de los elementos en el origen de la página web.</span><span class="sxs-lookup"><span data-stu-id="b69d3-210">**Source Order Viewer** is an experiment that displays the order of elements in the webpage source.</span></span>  <span data-ttu-id="b69d3-211">El orden de visualización en pantalla puede diferir del orden del origen, lo que confunde a los usuarios de lector de pantalla y teclado.</span><span class="sxs-lookup"><span data-stu-id="b69d3-211">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="b69d3-212">Usa el **experimento Visor de pedidos de** origen para encontrar las diferencias entre el orden de visualización en pantalla y el orden del origen.</span><span class="sxs-lookup"><span data-stu-id="b69d3-212">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="b69d3-213">Después de activar el experimento, asegúrate de reiniciar DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-213">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="b69d3-214">Para usar el **Visor de pedidos de origen,** siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="b69d3-214">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="b69d3-215">Abra la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="b69d3-215">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="b69d3-216">Abra el **panel Accesibilidad** en el panel del cajón \(inferior\).</span><span class="sxs-lookup"><span data-stu-id="b69d3-216">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="b69d3-217">En la **sección Visor de pedidos de** origen, seleccione la casilla Mostrar pedido **de** origen.</span><span class="sxs-lookup"><span data-stu-id="b69d3-217">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="b69d3-218">Resalte cualquier elemento HTML para mostrar una superposición según el orden en el origen de la página web.</span><span class="sxs-lookup"><span data-stu-id="b69d3-218">Highlight any HTML element to display an overlay that the order in the webpage source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Visor de pedidos de origen en el panel Accesibilidad" lightbox="../media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="b69d3-220">**Visor de pedidos de origen** en el panel **Accesibilidad**</span><span class="sxs-lookup"><span data-stu-id="b69d3-220">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <span data-ttu-id="b69d3-221">Habilitar el editor de métodos abreviados de teclado</span><span class="sxs-lookup"><span data-stu-id="b69d3-221">Enable keyboard shortcut editor</span></span>

<span data-ttu-id="b69d3-222">Con el **experimento Habilitar el editor de** métodos abreviados de teclado activado, puedes personalizar los métodos abreviados de teclado para cualquier acción en DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-222">With the **Enable keyboard shortcut editor** experiment turned on, you may customize keyboard shortcuts for any action in the DevTools.</span></span>  <span data-ttu-id="b69d3-223">Para personalizar el método abreviado de teclado para una acción específica, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="b69d3-223">To customize the keyboard shortcut for a specific action, complete the following steps.</span></span>  

1.  <span data-ttu-id="b69d3-224">[Abra DevTools][DevtoolsOpenMain].</span><span class="sxs-lookup"><span data-stu-id="b69d3-224">[Open DevTools][DevtoolsOpenMain].</span></span>  
1.  <span data-ttu-id="b69d3-225">Abra [Configuración.][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="b69d3-225">Open [Settings][DevToolsCustomizeIndexSettings].</span></span>  
    *   <span data-ttu-id="b69d3-226">Seleccione `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="b69d3-226">Select `Shift`+`?`.</span></span>  
1.  <span data-ttu-id="b69d3-227">Vaya a la **página Accesos directos.**</span><span class="sxs-lookup"><span data-stu-id="b69d3-227">Navigate to the **Shortcuts** page.</span></span>  
1.  <span data-ttu-id="b69d3-228">Elija la acción que desea personalizar.</span><span class="sxs-lookup"><span data-stu-id="b69d3-228">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="b69d3-229">Elija el **icono** Editar \( ![ EditKeyboardShortcut ](../media/edit-keyboard-shortcut-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="b69d3-229">Choose the **Edit** \(![EditKeyboardShortcut](../media/edit-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Elija la acción que desea personalizar en la página Accesos directos en Configuración" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       <span data-ttu-id="b69d3-231">Elija la acción que desea personalizar en la página **Accesos directos** en [Configuración][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="b69d3-231">Choose the action to customize from the **Shortcuts** page in [Settings][DevToolsCustomizeIndexSettings]</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b69d3-232">En el teclado, selecciona las teclas para enlazar a la acción.</span><span class="sxs-lookup"><span data-stu-id="b69d3-232">On the keyboard, select the keys to bind to the action.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Seleccionar las claves para asignar a la acción" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="b69d3-234">Seleccionar las claves para asignar a la acción</span><span class="sxs-lookup"><span data-stu-id="b69d3-234">Select the keys to assign to the action</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b69d3-235">Para guardar el nuevo método abreviado de teclado, elija la marca de verificación \(</span><span class="sxs-lookup"><span data-stu-id="b69d3-235">To save your new keyboard shortcut, choose the checkmark \(</span></span>![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)<span data-ttu-id="b69d3-237">Icono \).</span><span class="sxs-lookup"><span data-stu-id="b69d3-237">\) icon.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Elija el icono de marca de verificación para guardar el nuevo método abreviado de teclado" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="b69d3-239">Elija el icono de marca de verificación para guardar el nuevo método abreviado de teclado</span><span class="sxs-lookup"><span data-stu-id="b69d3-239">Choose the checkmark icon to save your new keyboard shortcut</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b69d3-240">Selecciona el nuevo método abreviado de teclado para desencadenar la acción en DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-240">Select your new keyboard shortcut to trigger the action in the DevTools.</span></span>  
    
<span data-ttu-id="b69d3-241">En la **página Accesos directos,** el icono **de** método abreviado de teclado personalizado \( ![ CustomKeyboardShortcut \) muestra los ](../media/custom-keyboard-shortcut-icon.msft.png) métodos abreviados de teclado personalizados.</span><span class="sxs-lookup"><span data-stu-id="b69d3-241">On the **Shortcuts** page, the **Custom Keyboard Shortcut** \(![CustomKeyboardShortcut](../media/custom-keyboard-shortcut-icon.msft.png)\) icon displays keyboard shortcuts you customized.</span></span>  <span data-ttu-id="b69d3-242">Para restablecer todos los accesos directos, elija **Restaurar accesos directos predeterminados.**</span><span class="sxs-lookup"><span data-stu-id="b69d3-242">To reset all shortcuts, choose **Restore default shortcuts**.</span></span>  

<span data-ttu-id="b69d3-243">Para descartar los cambios mientras edita los métodos abreviados de teclado para una acción, elija el icono X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="b69d3-243">To discard your changes while you edit the keyboard shortcuts for an action, choose the X \(![XKeyboardShortcut](../media/discard-changes-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="b69d3-244">Para quitar accesos directos de una acción específica, elija el icono Eliminar acceso directo **\(** ![ DeleteKeyboardShortcut ](../media/delete-keyboard-shortcut-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="b69d3-244">To remove shortcuts for a specific action, choose the **Delete shortcut** \(![DeleteKeyboardShortcut](../media/delete-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="b69d3-245">Para agregar varios accesos directos para una acción, elija **Agregar un acceso directo.**</span><span class="sxs-lookup"><span data-stu-id="b69d3-245">To add multiple shortcuts for an action, choose **Add a shortcut**.</span></span>  

> [!NOTE]
> <span data-ttu-id="b69d3-246">Si un método abreviado de teclado está asignado actualmente a otra acción, es posible que no lo guarde para una nueva acción.</span><span class="sxs-lookup"><span data-stu-id="b69d3-246">If a keyboard shortcut is currently assigned to another action, you may not save it for a new action.</span></span>  <span data-ttu-id="b69d3-247">Primero debe eliminar el método abreviado de teclado de la acción anterior y, a continuación, agregarlo a la nueva acción.</span><span class="sxs-lookup"><span data-stu-id="b69d3-247">You must first delete the keyboard shortcut for the previous action and then add it to the new action.</span></span>  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <span data-ttu-id="b69d3-248">Habilitar capas compuestas en la vista 3D</span><span class="sxs-lookup"><span data-stu-id="b69d3-248">Enable Composited Layers in 3D View</span></span>  

<span data-ttu-id="b69d3-249">Ahora puede visualizar capas junto a índices z y el modelo de objetos de documento \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="b69d3-249">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="b69d3-250">Esta característica le ayuda a depurar sin cambiar de contexto con tanta frecuencia.</span><span class="sxs-lookup"><span data-stu-id="b69d3-250">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="b69d3-251">Identificaste que la reducción del cambio de contexto era un punto difícil.</span><span class="sxs-lookup"><span data-stu-id="b69d3-251">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="b69d3-252">No siempre está claro cómo afecta el código que escribe a la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="b69d3-252">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="b69d3-253">Para obtener una experiencia de depuración visual completa, ahora se combinan la vista 3D y las Capas compuestas.</span><span class="sxs-lookup"><span data-stu-id="b69d3-253">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  

<span data-ttu-id="b69d3-254">Después de activar el experimento, asegúrate de reiniciar DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-254">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="b69d3-255">Para usar **capas compuestas,** siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="b69d3-255">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="b69d3-256">En el cajón, elija la **herramienta Vista 3D.**</span><span class="sxs-lookup"><span data-stu-id="b69d3-256">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="b69d3-257">Abra el **panel Capas compuestas.**</span><span class="sxs-lookup"><span data-stu-id="b69d3-257">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="b69d3-258">Se muestran todas las capas pintadas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b69d3-258">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="b69d3-259">Pruebe esta característica con sus propias aplicaciones web.</span><span class="sxs-lookup"><span data-stu-id="b69d3-259">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Panel Capas compuestas" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="b69d3-261">Panel **Capas compuestas**</span><span class="sxs-lookup"><span data-stu-id="b69d3-261">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <span data-ttu-id="b69d3-262">Habilitar la nueva herramienta Editor de fuentes en el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="b69d3-262">Enable new Font Editor tool within the Styles pane</span></span>  

<span data-ttu-id="b69d3-263">Ahora puede usar el nuevo Editor de [fuentes][DevtoolsInspectStylesEditFonts] visual para editar fuentes.</span><span class="sxs-lookup"><span data-stu-id="b69d3-263">You may now use the new visual [Font Editor][DevtoolsInspectStylesEditFonts] to edit fonts.</span></span>  <span data-ttu-id="b69d3-264">Úselo para definir fuentes y características de fuente.</span><span class="sxs-lookup"><span data-stu-id="b69d3-264">Use it define fonts and font characteristics.</span></span>  <span data-ttu-id="b69d3-265">El Editor **de fuentes visual** le ayuda a completar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="b69d3-265">The visual **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="b69d3-266">Cambiar entre unidades para distintas propiedades de fuente</span><span class="sxs-lookup"><span data-stu-id="b69d3-266">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="b69d3-267">Cambiar entre palabras clave para distintas propiedades de fuente</span><span class="sxs-lookup"><span data-stu-id="b69d3-267">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="b69d3-268">Convertir unidades</span><span class="sxs-lookup"><span data-stu-id="b69d3-268">Convert units</span></span>  
*   <span data-ttu-id="b69d3-269">Generar código CSS preciso</span><span class="sxs-lookup"><span data-stu-id="b69d3-269">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="b69d3-270">Después de activar el experimento, asegúrate de reiniciar DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-270">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="b69d3-271">Para usar el nuevo Editor de **fuentes visual,** siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="b69d3-271">To use the new visual **Font Editor**, complete the following steps.</span></span>  

1.  <span data-ttu-id="b69d3-272">Abra la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="b69d3-272">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="b69d3-273">Abra el **panel Estilos.**</span><span class="sxs-lookup"><span data-stu-id="b69d3-273">Open the **Styles** pane.</span></span>  
1.  <span data-ttu-id="b69d3-274">Elija el icono **del Editor de** fuentes.</span><span class="sxs-lookup"><span data-stu-id="b69d3-274">Choose the **Font Editor** icon.</span></span>  
    
<span data-ttu-id="b69d3-275">Para obtener más información acerca del nuevo **Editor**de fuentes visual, vaya a Editar estilos y configuraciones de fuente CSS en el panel Estilos [de DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="b69d3-275">For more information about the new visual **Font Editor**, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="El panel Editor de fuentes visual está resaltado" lightbox="../media/font-editor-open.msft.png":::
   <span data-ttu-id="b69d3-277">El panel **Editor de fuentes** visual está resaltado</span><span class="sxs-lookup"><span data-stu-id="b69d3-277">The visual **Font Editor** pane is highlighted</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <span data-ttu-id="b69d3-278">Habilitar nuevas características de depuración de CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="b69d3-278">Enable new CSS Flexbox debugging features</span></span>  

<span data-ttu-id="b69d3-279">Esta característica experimental proporciona muchas visualizaciones nuevas que le ayudarán a depurar diseños CSS Flexbox.</span><span class="sxs-lookup"><span data-stu-id="b69d3-279">This experimental feature provides many new visualizations to help you debug CSS Flexbox layouts.</span></span>  <span data-ttu-id="b69d3-280">Para obtener una vista previa de las características experimentales más recientes, [activa este experimento](#turn-on-experimental-features) y vuelve a cargar DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-280">To preview the latest experimental features, [turn on this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  

#### <span data-ttu-id="b69d3-281">Mostrar superposiciones persistentes en diseños de Flexbox con la herramienta Inspeccionar</span><span class="sxs-lookup"><span data-stu-id="b69d3-281">Display persistent overlays on Flexbox layouts with the Inspect tool</span></span>  

<span data-ttu-id="b69d3-282">La **herramienta Inspect** proporciona una forma rápida de identificar y visualizar diseños CSS Flexbox en un sitio web al mantener el puntero sobre ellos con el mouse.</span><span class="sxs-lookup"><span data-stu-id="b69d3-282">The **Inspect** tool provides a quick way to identify and visualize CSS Flexbox layouts in a website by hovering on them with the mouse.</span></span>  <span data-ttu-id="b69d3-283">Elija el **icono Inspeccionar** \( Inspeccionar \) en la esquina superior izquierda ![ de ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-283">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="b69d3-284">A continuación, al depurar el sitio web, mantenga el puntero sobre un contenedor flexible para mostrar esquemas alrededor del contenedor flex.</span><span class="sxs-lookup"><span data-stu-id="b69d3-284">Then, while debugging the website, hover on a flex container to display outlines around the flex container.</span></span>  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Mostrar contenedores de Flexbox con la herramienta Inspeccionar" lightbox="../media/flexbox-hover.msft.png":::
   <span data-ttu-id="b69d3-286">Mostrar contenedores de Flexbox con la **herramienta Inspeccionar**</span><span class="sxs-lookup"><span data-stu-id="b69d3-286">Display Flexbox containers with the **Inspect** tool</span></span>  
:::image-end:::  

#### <span data-ttu-id="b69d3-287">Mostrar superposiciones persistentes en diseños de Flexbox</span><span class="sxs-lookup"><span data-stu-id="b69d3-287">Display persistent overlays on Flexbox layouts</span></span>  

<span data-ttu-id="b69d3-288">En Microsoft Edge versión 89 o posterior, la característica experimental CSS Flexbox también ofrece la opción de activar superposiciones persistentes en diseños de Flexbox.</span><span class="sxs-lookup"><span data-stu-id="b69d3-288">In Microsoft Edge version 89 or later, the experimental CSS Flexbox feature also offers the option to turn on persistent overlays on Flexbox layouts.</span></span>  <span data-ttu-id="b69d3-289">Las superposiciones persistentes proporcionan las siguientes ventajas.</span><span class="sxs-lookup"><span data-stu-id="b69d3-289">Persistent overlays provide the following benefits.</span></span>  

*   <span data-ttu-id="b69d3-290">Las superposiciones persistentes permanecen visibles en la página web mientras se desplaza, mueve el mouse y usa otras características de DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-290">Persistent overlays remain visible on the webpage as you scroll, move your mouse, and use other features of the DevTools.</span></span>
*   <span data-ttu-id="b69d3-291">Se pueden usar varias superposiciones persistentes al mismo tiempo, para permitirle revisar varios diseños de Flexbox a la vez.</span><span class="sxs-lookup"><span data-stu-id="b69d3-291">Multiple persistent overlays may be used at the same time, to allow you to review several Flexbox layouts at once.</span></span>  
*   <span data-ttu-id="b69d3-292">Las superposiciones persistentes ofrecen opciones de configuración de color.</span><span class="sxs-lookup"><span data-stu-id="b69d3-292">Persistent overlays offer color configuration options.</span></span>  
    
<span data-ttu-id="b69d3-293">Para alternar las superposiciones persistentes en el diseño de Flexbox, usa una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="b69d3-293">To toggle persistent overlays on Flexbox layout, use one of following actions.</span></span>  

*   <span data-ttu-id="b69d3-294">Elija el icono del óvalo de **Flexbox** junto a cualquier contenedor de Flexbox que se muestra en el árbol DOM de la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="b69d3-294">Choose the **Flexbox** oval icon next to any Flexbox container displayed in the DOM tree of the **Elements** tool.</span></span>  
*   <span data-ttu-id="b69d3-295">Abre el nuevo panel **diseño** que se encuentra en la herramienta **Elementos** y elige la casilla junto a cada contenedor de Flexbox que quieras resaltar.</span><span class="sxs-lookup"><span data-stu-id="b69d3-295">Open the new **Layout** panel located in the **Elements** tool, and choose the checkbox next to each Flexbox container you want to highlight.</span></span>  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Iconos flexibles y panel diseño en DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   <span data-ttu-id="b69d3-297">Iconos flexibles y panel **diseño** en DevTools</span><span class="sxs-lookup"><span data-stu-id="b69d3-297">Flex icons and **Layout** panel in DevTools</span></span>  
:::image-end:::  

#### <span data-ttu-id="b69d3-298">Configurar superposiciones persistentes</span><span class="sxs-lookup"><span data-stu-id="b69d3-298">Configure persistent overlays</span></span>  

<span data-ttu-id="b69d3-299">Para configurar las opciones de las superposiciones persistentes para cuadrículas CSS o diseños de Flexbox, usa el **panel** Diseño.</span><span class="sxs-lookup"><span data-stu-id="b69d3-299">To configure options for persistent overlays for CSS grids or Flexbox layouts, use the **Layout** pane.</span></span>  <span data-ttu-id="b69d3-300">El **panel** Diseño se encuentra en la herramienta **Elementos** junto a los paneles **Estilos** **y Calculados.**</span><span class="sxs-lookup"><span data-stu-id="b69d3-300">The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.</span></span>  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Panel de diseño" lightbox="../media/flexbox-layout.msft.png":::
   <span data-ttu-id="b69d3-302">Panel de diseño</span><span class="sxs-lookup"><span data-stu-id="b69d3-302">Layout panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <span data-ttu-id="b69d3-303">Habilitar los menús de la pestaña + botón para abrir más herramientas</span><span class="sxs-lookup"><span data-stu-id="b69d3-303">Enable + button tab menus to open more tools</span></span>  

<span data-ttu-id="b69d3-304">Ahora puede abrir más herramientas con el nuevo icono **Más herramientas** \( `+` \).</span><span class="sxs-lookup"><span data-stu-id="b69d3-304">You may now open more tools using the new **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="b69d3-305">Después de activar los **menús** de la pestaña Habilitar + botón para abrir más herramientas y volver a cargar DevTools, se muestra un signo más \( \) a la derecha del grupo de pestañas en la parte superior de `+` DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-305">After you turn on the **Enable + button tab menus to open more tools** experiment and reload DevTools, a plus sign \(`+`\) displays to the right of the tab group at the top of the DevTools.</span></span>  <span data-ttu-id="b69d3-306">Para mostrar una lista de otras herramientas que puede agregar a la barra de pestañas, elija el nuevo icono **Más** herramientas \( `+` \).</span><span class="sxs-lookup"><span data-stu-id="b69d3-306">To display a list of other tools that you may add to the tab bar, choose the new **More Tools** \(`+`\) icon.</span></span>  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Más herramientas en el panel superior" lightbox="../media/experiments-more-tools-button.msft.png":::
   <span data-ttu-id="b69d3-308">**Más herramientas** en el panel superior</span><span class="sxs-lookup"><span data-stu-id="b69d3-308">**More Tools** in the top pane</span></span>
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <span data-ttu-id="b69d3-309">Habilitar herramienta de bienvenida</span><span class="sxs-lookup"><span data-stu-id="b69d3-309">Enable Welcome tool</span></span>

<span data-ttu-id="b69d3-310">Este experimento reemplaza la **herramienta Novedades** por la nueva **herramienta de** bienvenida.</span><span class="sxs-lookup"><span data-stu-id="b69d3-310">This experiment replaces the **What's New** tool with the new **Welcome** tool.</span></span>  <span data-ttu-id="b69d3-311">Muestra un diseño actualizado para el siguiente contenido.</span><span class="sxs-lookup"><span data-stu-id="b69d3-311">It displays a refreshed design for the following content.</span></span>  

*   <span data-ttu-id="b69d3-312">Vínculos a documentos para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="b69d3-312">Links to developer docs</span></span>  
*   <span data-ttu-id="b69d3-313">las características más recientes</span><span class="sxs-lookup"><span data-stu-id="b69d3-313">the latest features</span></span>  
*   <span data-ttu-id="b69d3-314">notas de la versión</span><span class="sxs-lookup"><span data-stu-id="b69d3-314">release notes</span></span>  
*   <span data-ttu-id="b69d3-315">Opción para ponerse en contacto con el equipo de DevTools de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b69d3-315">Option to contact the Microsoft Edge DevTools team</span></span>  
    
<span data-ttu-id="b69d3-316">La **herramienta de** bienvenida se abre automáticamente después de cada actualización de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b69d3-316">The **Welcome** tool opens automatically after each update to Microsoft Edge.</span></span>  <span data-ttu-id="b69d3-317">Para evitar que se muestre la herramienta **de** bienvenida después de cada actualización, desactive la casilla situada junto a la pestaña **Abrir** después de cada actualización bajo el título **de** la herramienta de bienvenida.</span><span class="sxs-lookup"><span data-stu-id="b69d3-317">To prevent the display of the **Welcome** tool after each update, clear the checkbox next to **Open tab after each update** under the **Welcome** tool title.</span></span>  

<span data-ttu-id="b69d3-318">Si prefieres la **herramienta** Novedades original, ve a Experimentos de configuración y quita la casilla junto a [][DevtoolsCustomizeIndexSettings]  >  \*\*\*\* Habilitar **pestaña de bienvenida.**</span><span class="sxs-lookup"><span data-stu-id="b69d3-318">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Herramienta de bienvenida" lightbox="../media/experiments-welcome.msft.png":::
   <span data-ttu-id="b69d3-320">**Herramienta de** bienvenida</span><span class="sxs-lookup"><span data-stu-id="b69d3-320">**Welcome** tool</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <span data-ttu-id="b69d3-321">Características experimentales anteriores</span><span class="sxs-lookup"><span data-stu-id="b69d3-321">Previous experimental features</span></span>  

*   <span data-ttu-id="b69d3-322">[La vista 3D][Devtools3dViewIndex] ahora está disponible y activada de forma predeterminada en Microsoft Edge versión 83 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b69d3-322">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="b69d3-323">[Activar la compatibilidad para mover fichas][DevtoolsMoveTabs] entre paneles ya está disponible y activado de forma predeterminada en Microsoft Edge versión 85 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b69d3-323">[Turn on support to move tabs between panels][DevtoolsMoveTabs] is now available and turned on by default in Microsoft Edge version 85 or later.</span></span>  
*   <span data-ttu-id="b69d3-324">[Personalizar los métodos abreviados de][DevtoolsCustomKeyboardShortcuts] teclado ahora está disponible y activado de forma predeterminada en Microsoft Edge versión 86 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b69d3-324">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  
*   <span data-ttu-id="b69d3-325">[Emulación: el modo de pantalla dual compatible][DevtoolsDeviceModeDualScreenAndFoldables] ahora está disponible y activado de forma predeterminada en Microsoft Edge versión 89 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b69d3-325">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="b69d3-326">[Activar las nuevas características de depuración de][DevtoolsCssGrid] cuadrícula CSS ya está disponible y activada de forma predeterminada en Microsoft Edge versión 89 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b69d3-326">[Turn on new CSS grid debugging features][DevtoolsCssGrid] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
    
## <span data-ttu-id="b69d3-327">Proporcionar comentarios sobre las características experimentales</span><span class="sxs-lookup"><span data-stu-id="b69d3-327">Providing feedback on experimental features</span></span>  

<span data-ttu-id="b69d3-328">Para proporcionar comentarios sobre los experimentos de Microsoft Edge DevTools o cualquier otra cosa relacionada con DevTools.</span><span class="sxs-lookup"><span data-stu-id="b69d3-328">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="b69d3-329">Envía tus comentarios mediante el icono **Enviar** comentarios en DevTools</span><span class="sxs-lookup"><span data-stu-id="b69d3-329">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="b69d3-330">Tweet en [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="b69d3-330">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="El icono Enviar comentarios en Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="b69d3-332">El **icono Enviar comentarios** en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b69d3-332">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Vista 3D | Microsoft Docs"  
[DevtoolsCssGrid]: ../css/grid.md "Inspeccionar la cuadrícula CSS en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsMoveTabs]: ../customize/index.md "Personalizar las devTools de Microsoft Edge | Microsoft Docs"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Edite la configuración y los estilos de fuente CSS en el panel Estilos de DevTools | Microsoft Docs"  
[DevtoolsIssues]: ../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas de Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsShortcuts]: ../shortcuts/index.md "Métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Personalizar los métodos abreviados de teclado en las DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsOpenMain]: ../open/index.md "Abra las DevTools de Microsoft Edge | Microsoft Docs"  

[DualScreenWebIndex]: /dual-screen/web/index "Experiencias web de pantalla doble | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtener el emulador de Surface Duo | Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con la seam: introducción a los dispositivos de pantalla doble | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Usa el emulador de Surface Duo | Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Característica de pantalla multimedia CSS para la detección de pantalla doble | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "La API de JavaScript getWindowSegments para dispositivos de pantalla doble | Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clientes de Escritorio remoto | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "| Samsung"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Emular dispositivos de doble pantalla y plegado en Microsoft Edge DevTools | Microsoft Docs"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  

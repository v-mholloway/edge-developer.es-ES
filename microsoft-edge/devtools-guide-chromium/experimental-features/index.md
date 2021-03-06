---
description: Las últimas características experimentales de Microsoft Edge DevTools
title: Características experimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, experiment
ms.openlocfilehash: b366cfeccafe874bc9e76d3b66659122c5d07c69
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398682"
---
# <a name="experimental-features"></a><span data-ttu-id="2f208-104">Características experimentales</span><span class="sxs-lookup"><span data-stu-id="2f208-104">Experimental features</span></span>  

<span data-ttu-id="2f208-105">Microsoft Edge DevTools proporciona acceso a características experimentales que aún están en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="2f208-105">Microsoft Edge DevTools provide access to experimental features that are still in development.</span></span>  <span data-ttu-id="2f208-106">Puede probar y [proporcionar comentarios antes](#providing-feedback-on-experimental-features) de publicar cada característica.</span><span class="sxs-lookup"><span data-stu-id="2f208-106">You may test and [provide feedback](#providing-feedback-on-experimental-features) before each feature is released.</span></span>  

<span data-ttu-id="2f208-107">Aunque las características experimentales están disponibles en todos los canales de Microsoft Edge, es posible que obtenga las características experimentales más recientes con el canal de Microsoft Edge Canary.</span><span class="sxs-lookup"><span data-stu-id="2f208-107">While experimental features are available in all channels of Microsoft Edge, you may get the latest experimental features using the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="2f208-108">Activar características experimentales</span><span class="sxs-lookup"><span data-stu-id="2f208-108">Turn on experimental features</span></span>  

<span data-ttu-id="2f208-109">Para activar las características experimentales \(or off\) en Microsoft Edge, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="2f208-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  

1.  <span data-ttu-id="2f208-110">[Abra DevTools][DevtoolsOpenMain].</span><span class="sxs-lookup"><span data-stu-id="2f208-110">[Open DevTools][DevtoolsOpenMain].</span></span>  
    *   <span data-ttu-id="2f208-111">Seleccione `Control` + `Shift` + `I` \(Windows, Linux\) o `Command` + `Option` + `I` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="2f208-111">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\).</span></span>  <span data-ttu-id="2f208-112">Para obtener más información, vaya a [Métodos abreviados de teclado de Microsoft Edge DevTools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="2f208-112">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="2f208-113">Abra el [panel][DevToolsCustomizeIndexSettings] Configuración.</span><span class="sxs-lookup"><span data-stu-id="2f208-113">Open the [Settings][DevToolsCustomizeIndexSettings] pane.</span></span>  
    *   <span data-ttu-id="2f208-114">Seleccione `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="2f208-114">Select `Shift`+`?`.</span></span>  <span data-ttu-id="2f208-115">Para obtener más información, vaya a [Métodos abreviados de teclado de Microsoft Edge DevTools][DevToolsShortcuts].</span><span class="sxs-lookup"><span data-stu-id="2f208-115">For more information, navigate to [Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].</span></span>  
1.  <span data-ttu-id="2f208-116">En el lado izquierdo del **panel Configuración,** elija la **sección** Experimentos.</span><span class="sxs-lookup"><span data-stu-id="2f208-116">On the left side of the **Settings** pane, choose the **Experiments** section.</span></span>  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="La página Experimentos en Configuración" lightbox="../media/experiments-devtools.msft.png":::
       <span data-ttu-id="2f208-118">La **página Experimentos** en **Configuración**</span><span class="sxs-lookup"><span data-stu-id="2f208-118">The **Experiments** page in **Settings**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f208-119">En la **página Experimentos,** desplácese por la lista de todas las características experimentales disponibles y elija la casilla junto a cada característica que desee probar.</span><span class="sxs-lookup"><span data-stu-id="2f208-119">On the **Experiments** page, scroll through the list of all available experimental features and choose the checkbox next to each feature that you want to test.</span></span>  
1.  <span data-ttu-id="2f208-120">Cierre y vuelva a abrir Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-120">Close and reopen Microsoft Edge DevTools.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="2f208-121">Las características experimentales se actualizan constantemente y pueden causar problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="2f208-121">Experimental features are constantly being updated and may cause performance issues.</span></span>  <span data-ttu-id="2f208-122">Para desactivar una característica experimental, abra la página **Experimentos** y desactive la casilla de la característica experimental que desea desactivar.</span><span class="sxs-lookup"><span data-stu-id="2f208-122">To turn off an experimental feature, open the **Experiments** page and clear the checkbox of the experimental feature that you want to turn off.</span></span>  

## <a name="highlighted-experimental-features"></a><span data-ttu-id="2f208-123">Características experimentales resaltadas</span><span class="sxs-lookup"><span data-stu-id="2f208-123">Highlighted experimental features</span></span>  

<span data-ttu-id="2f208-124">En las secciones siguientes se describen las nuevas características experimentales que están disponibles en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2f208-124">The following sections describe the new experimental features that are available in Microsoft Edge.</span></span>  

| <span data-ttu-id="2f208-125">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="2f208-125">Experimental feature</span></span> | <span data-ttu-id="2f208-126">Versión de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2f208-126">Microsoft Edge version</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="2f208-127">Habilitar webhint</span><span class="sxs-lookup"><span data-stu-id="2f208-127">Enable webhint</span></span>](#enable-webhint) | <span data-ttu-id="2f208-128">85 o posterior</span><span class="sxs-lookup"><span data-stu-id="2f208-128">85 or later</span></span> |  
| [<span data-ttu-id="2f208-129">Habilitar consola de red</span><span class="sxs-lookup"><span data-stu-id="2f208-129">Enable Network Console</span></span>](#enable-network-console) | <span data-ttu-id="2f208-130">85 o posterior</span><span class="sxs-lookup"><span data-stu-id="2f208-130">85 or later</span></span> |  
| [<span data-ttu-id="2f208-131">Visor de pedidos de origen</span><span class="sxs-lookup"><span data-stu-id="2f208-131">Source Order Viewer</span></span>](#source-order-viewer) | <span data-ttu-id="2f208-132">86 o posterior</span><span class="sxs-lookup"><span data-stu-id="2f208-132">86 or later</span></span> |  
| [<span data-ttu-id="2f208-133">Habilitar el editor de métodos abreviados de teclado</span><span class="sxs-lookup"><span data-stu-id="2f208-133">Enable keyboard shortcut editor</span></span>](#enable-keyboard-shortcut-editor) | <span data-ttu-id="2f208-134">87 o posterior</span><span class="sxs-lookup"><span data-stu-id="2f208-134">87 or later</span></span> |  
| [<span data-ttu-id="2f208-135">Habilitar capas compuestas en la vista 3D</span><span class="sxs-lookup"><span data-stu-id="2f208-135">Enable Composited Layers in 3D View</span></span>](#enable-composited-layers-in-3d-view) | <span data-ttu-id="2f208-136">87 o posterior</span><span class="sxs-lookup"><span data-stu-id="2f208-136">87 or later</span></span> |  
| [<span data-ttu-id="2f208-137">Habilitar la nueva herramienta Editor de fuentes en el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="2f208-137">Enable new Font Editor tool within the Styles pane</span></span>](#enable-new-font-editor-tool-within-the-styles-pane) | <span data-ttu-id="2f208-138">89 o posterior</span><span class="sxs-lookup"><span data-stu-id="2f208-138">89 or later</span></span> |  
| [<span data-ttu-id="2f208-139">Habilitar nuevas características de depuración de CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="2f208-139">Enable new CSS Flexbox debugging features</span></span>](#enable-new-css-flexbox-debugging-features) | <span data-ttu-id="2f208-140">89 o posterior</span><span class="sxs-lookup"><span data-stu-id="2f208-140">89 or later</span></span> |  
| [<span data-ttu-id="2f208-141">Habilitar menús de pestañas + botón para abrir más herramientas</span><span class="sxs-lookup"><span data-stu-id="2f208-141">Enable + button tab menus to open more tools</span></span>](#enable--button-tab-menus-to-open-more-tools) | <span data-ttu-id="2f208-142">89 o posterior</span><span class="sxs-lookup"><span data-stu-id="2f208-142">89 or later</span></span> |  
| [<span data-ttu-id="2f208-143">Pestaña Habilitar bienvenida</span><span class="sxs-lookup"><span data-stu-id="2f208-143">Enable Welcome tab</span></span>](#enable-welcome-tool) | <span data-ttu-id="2f208-144">89 o posterior</span><span class="sxs-lookup"><span data-stu-id="2f208-144">89 or later</span></span> |  

### <a name="enable-new-css-grid-debugging-features"></a><span data-ttu-id="2f208-145">Habilitar nuevas características de depuración de cuadrícula CSS</span><span class="sxs-lookup"><span data-stu-id="2f208-145">Enable new CSS grid debugging features</span></span>  

<span data-ttu-id="2f208-146">Esta característica experimental proporciona una serie de visualizaciones nuevas que le ayudarán a depurar diseños de cuadrícula CSS.</span><span class="sxs-lookup"><span data-stu-id="2f208-146">This experimental feature provides a number of new visualizations to help you debug CSS grid layouts.</span></span>  <span data-ttu-id="2f208-147">Para obtener una vista previa de las características experimentales más recientes, [habilite este experimento](#turn-on-experimental-features) y vuelva a cargar DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-147">To preview the latest experimental features, [enable this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  <span data-ttu-id="2f208-148">Este experimento está en la versión 87 o posterior de Microsoft Edge de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2f208-148">This experiment is on by default in Microsoft Edge version 87 or later.</span></span>  

#### <a name="viewing-on-hover-grid-overlays-with-the-inspect-tool"></a><span data-ttu-id="2f208-149">Visualización de superposiciones de cuadrícula activa con la herramienta Inspeccionar</span><span class="sxs-lookup"><span data-stu-id="2f208-149">Viewing on-hover grid overlays with the Inspect tool</span></span>  

<span data-ttu-id="2f208-150">La **herramienta Inspeccionar** proporciona una forma rápida de identificar y visualizar diseños de cuadrícula CSS en un sitio web al pasar el puntero sobre ellos con el mouse.</span><span class="sxs-lookup"><span data-stu-id="2f208-150">The **Inspect** tool provides a quick way to identify and visualize CSS Grid layouts in a website by hovering over them with the mouse.</span></span>  <span data-ttu-id="2f208-151">Elija el **icono Inspeccionar** \( Inspeccionar \) en la esquina superior izquierda ![ de ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-151">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="2f208-152">A continuación, mantenga el `Grid` mouse en un elemento de la página web que está depurando.</span><span class="sxs-lookup"><span data-stu-id="2f208-152">Then, hover on a `Grid` element on the webpage you are debugging.</span></span>  <span data-ttu-id="2f208-153">Los contornos se muestran alrededor de la cuadrícula y el sombreado indica la ubicación de los espacios de cuadrícula si están presentes.</span><span class="sxs-lookup"><span data-stu-id="2f208-153">Outlines are displayed around the grid, and hatching indicates the location of grid gaps if present.</span></span>  

:::image type="complex" source="../media/grid-inspect.msft.png" alt-text="Visualización de cuadrículas con la herramienta Inspeccionar" lightbox="../media/grid-inspect.msft.png":::
   <span data-ttu-id="2f208-155">Visualización de cuadrículas con la **herramienta Inspeccionar**</span><span class="sxs-lookup"><span data-stu-id="2f208-155">Viewing grids with the **Inspect** tool</span></span>  
:::image-end:::  

#### <a name="viewing-persistent-grid-overlays"></a><span data-ttu-id="2f208-156">Visualización de superposiciones de cuadrícula persistentes</span><span class="sxs-lookup"><span data-stu-id="2f208-156">Viewing persistent grid overlays</span></span>  

<span data-ttu-id="2f208-157">En Microsoft Edge versión 86 o posterior, la característica de cuadrícula CSS experimental también ofrece la opción de habilitar las superposiciones de cuadrícula persistentes.</span><span class="sxs-lookup"><span data-stu-id="2f208-157">In Microsoft Edge version 86 or later, the experimental CSS grid feature also offers the option to enable persistent Grid overlays.</span></span>  <span data-ttu-id="2f208-158">Las superposiciones persistentes proporcionan varias ventajas.</span><span class="sxs-lookup"><span data-stu-id="2f208-158">The persistent overlays provide several benefits.</span></span>  

*   <span data-ttu-id="2f208-159">Las superposiciones persistentes permanecen visibles en la página a medida que se desplaza, mueve el mouse y usa otras características de DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-159">The persistent overlays remain visible on the page as you scroll, move your mouse, and use other features of the DevTools.</span></span>  
*   <span data-ttu-id="2f208-160">Varias superposiciones persistentes pueden estar activadas al mismo tiempo, lo que te permite revisar varios diseños de cuadrícula a la vez.</span><span class="sxs-lookup"><span data-stu-id="2f208-160">Multiple persistent overlays may be turned on at the same time, allowing you to review several grid layouts at once.</span></span>  
*   <span data-ttu-id="2f208-161">Las superposiciones persistentes ofrecen muchas opciones de configuración, como ocultar o mostrar nombres en el área de cuadrícula, espacios de cuadrícula, tamaños de pista, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="2f208-161">Persistent overlays offer many configuration options, such as hiding or showing names in the grid area, grid gaps, track sizes, and so on.</span></span>  
    
<span data-ttu-id="2f208-162">Las dos formas de alternar una superposición de cuadrícula persistente.</span><span class="sxs-lookup"><span data-stu-id="2f208-162">The two ways to toggle a persistent grid overlay.</span></span>  

*   <span data-ttu-id="2f208-163">Elija el **icono** óvalo Cuadrícula junto a cualquier elemento Grid que se muestra en el árbol DOM de la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="2f208-163">Choose the **Grid** oval icon next to any Grid element shown in the DOM tree of the **Elements** tool.</span></span>  
    
    :::image type="complex" source="../media/grid-adorner.msft.png" alt-text="Icono ovalado de cuadrícula en la herramienta Elementos" lightbox="../media/grid-adorner.msft.png":::
       <span data-ttu-id="2f208-165">Icono ovalado de cuadrícula en **la herramienta** Elementos</span><span class="sxs-lookup"><span data-stu-id="2f208-165">Grid oval icon in **Elements** tool</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="2f208-166">Abra el nuevo panel **Diseño** ubicado en la herramienta Elementos y seleccione la casilla situada junto a cada elemento Grid que desee resaltar.</span><span class="sxs-lookup"><span data-stu-id="2f208-166">Open the new **Layout** panel located in the Elements tool, and choose the checkbox next to each Grid element you want to highlight.</span></span>  
    
    :::image type="complex" source="../media/grid-layout-zoom.msft.png" alt-text="Panel Diseño en DevTools" lightbox="../media/grid-layout-zoom.msft.png":::
       <span data-ttu-id="2f208-168">**Panel Diseño** en DevTools</span><span class="sxs-lookup"><span data-stu-id="2f208-168">**Layout** panel in DevTools</span></span>  
    :::image-end:::  
    
#### <a name="configuring-persistent-overlays"></a><span data-ttu-id="2f208-169">Configuración de superposiciones persistentes</span><span class="sxs-lookup"><span data-stu-id="2f208-169">Configuring persistent overlays</span></span>  

<span data-ttu-id="2f208-170">En Microsoft Edge versión 86 o posterior, el **nuevo** panel Diseño se encuentra en la herramienta **Elementos** junto con los paneles **Estilos** **y Calculados.**</span><span class="sxs-lookup"><span data-stu-id="2f208-170">In Microsoft Edge version 86 or later, the new **Layout** panel is located in the **Elements** tool alongside the **Styles** and **Computed** panels.</span></span>  <span data-ttu-id="2f208-171">El panel **Diseño** muestra las opciones de configuración de las superposiciones persistentes.</span><span class="sxs-lookup"><span data-stu-id="2f208-171">The **Layout** panel surfaces configuration options for persistent overlays.</span></span>  

:::image type="complex" source="../media/experiments-grid.msft.png" alt-text="Característica de depuración de cuadrícula CSS" lightbox="../media/experiments-grid.msft.png":::
   <span data-ttu-id="2f208-173">Característica de depuración de cuadrícula CSS</span><span class="sxs-lookup"><span data-stu-id="2f208-173">CSS grid debugging feature</span></span>  
:::image-end:::  

### <a name="enable-support-to-move-tabs-between-panels"></a><span data-ttu-id="2f208-174">Habilitar la compatibilidad para mover pestañas entre paneles</span><span class="sxs-lookup"><span data-stu-id="2f208-174">Enable support to move tabs between panels</span></span>  

<span data-ttu-id="2f208-175">Normalmente, herramientas como \*\*\*\* Elementos **y** Red solo se pueden abrir en el panel principal que se encuentra en la parte superior de DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-175">Normally, tools such as **Elements** and **Network** may only open in the main panel that is located at the top of the DevTools.</span></span>  <span data-ttu-id="2f208-176">Herramientas como **vista 3D** y problemas que normalmente solo se abren en el panel \*\*\*\* **DevTools** que se encuentra en la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="2f208-176">Tools like **3D View** and **Issues** which normally only open in the **Drawer** panel that is located at the bottom of the DevTools.</span></span>  <span data-ttu-id="2f208-177">Después de elegir el experimento, puede mover herramientas entre los paneles superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="2f208-177">After you choose the experiment, you may move tools between the top and bottom panels.</span></span>  <span data-ttu-id="2f208-178">Para mover una herramienta, mantenga el mouse en la pestaña, abra el menú contextual \(hacer clic con el botón secundario\) y elija Mover a la parte superior **o** Mover a la **parte inferior**.</span><span class="sxs-lookup"><span data-stu-id="2f208-178">To move a tool, hover on the tab, open the contextual menu \(right-click\), and choose **Move to top** or **Move to bottom**.</span></span>   <span data-ttu-id="2f208-179">Este experimento le permite personalizar el diseño de DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-179">This experiment allows you to customize your DevTools layout.</span></span>  <span data-ttu-id="2f208-180">Para mostrar u ocultar el panel **De cajón,** seleccione `Escape` .</span><span class="sxs-lookup"><span data-stu-id="2f208-180">To display or hide the **Drawer** panel, select `Escape`.</span></span>  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Mover herramientas entre paneles" lightbox="../media/experiments-move-panels.msft.png":::
   <span data-ttu-id="2f208-182">Mover herramientas entre paneles</span><span class="sxs-lookup"><span data-stu-id="2f208-182">Moving tools between panels</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-webhint"></a><span data-ttu-id="2f208-183">Habilitar webhint</span><span class="sxs-lookup"><span data-stu-id="2f208-183">Enable webhint</span></span>  

<span data-ttu-id="2f208-184">[webhint][WebhintMain] es una herramienta de código abierto que proporciona comentarios en tiempo real para sitios web y páginas web locales.</span><span class="sxs-lookup"><span data-stu-id="2f208-184">[webhint][WebhintMain] is an open-source tool that provides real-time feedback for websites and local webpages.</span></span>  <span data-ttu-id="2f208-185">El tipo de comentarios proporcionados [por webhint][WebhintMain].</span><span class="sxs-lookup"><span data-stu-id="2f208-185">The type of feedback provided by [webhint][WebhintMain].</span></span>  

*   <span data-ttu-id="2f208-186">accesibilidad</span><span class="sxs-lookup"><span data-stu-id="2f208-186">accessibility</span></span>  
*   <span data-ttu-id="2f208-187">compatibilidad entre exploradores</span><span class="sxs-lookup"><span data-stu-id="2f208-187">cross-browser compatibility</span></span>  
*   <span data-ttu-id="2f208-188">seguridad</span><span class="sxs-lookup"><span data-stu-id="2f208-188">security</span></span>  
*   <span data-ttu-id="2f208-189">rendimiento</span><span class="sxs-lookup"><span data-stu-id="2f208-189">performance</span></span>  
*   <span data-ttu-id="2f208-190">Aplicaciones web progresivas (PWA)</span><span class="sxs-lookup"><span data-stu-id="2f208-190">Progressive Web Apps (PWAs)</span></span>  
*   <span data-ttu-id="2f208-191">otros problemas comunes de desarrollo web</span><span class="sxs-lookup"><span data-stu-id="2f208-191">other common web development issues</span></span>  
    
<span data-ttu-id="2f208-192">El [experimento webhint][WebhintMain] muestra los comentarios de webhint en el panel [Problemas.][DevtoolsIssues]</span><span class="sxs-lookup"><span data-stu-id="2f208-192">The [webhint][WebhintMain] experiment displays the webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  <span data-ttu-id="2f208-193">Elija un problema para mostrar la documentación de la solución y una lista de los recursos afectados en su sitio web.</span><span class="sxs-lookup"><span data-stu-id="2f208-193">Choose an issue to display solution documentation and a list of the affected resources on your website.</span></span>  <span data-ttu-id="2f208-194">Elija un vínculo de recurso para abrir el panel **Network**, **Sources**o **Elements** relevante en DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-194">Choose a resource link to open the relevant **Network**, **Sources**, or **Elements** pane in DevTools.</span></span>  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="comentarios de webhint en el panel Problemas" lightbox="../media/experiments-webhint.msft.png":::
   <span data-ttu-id="2f208-196">comentarios de webhint en el panel **Problemas**</span><span class="sxs-lookup"><span data-stu-id="2f208-196">webhint feedback in the **Issues** panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-network-console"></a><span data-ttu-id="2f208-197">Habilitar consola de red</span><span class="sxs-lookup"><span data-stu-id="2f208-197">Enable Network Console</span></span>  

<span data-ttu-id="2f208-198">**Consola de** red es el título de trabajo de un experimento para realizar solicitudes de red sintéticas a través de HTTP.</span><span class="sxs-lookup"><span data-stu-id="2f208-198">**Network Console** is the working title of an experiment to make synthetic network requests over HTTP.</span></span>  <span data-ttu-id="2f208-199">Puede usar el experimento **consola de** red para enviar solicitudes de API web.</span><span class="sxs-lookup"><span data-stu-id="2f208-199">You may use the **Network Console** experiment to send web API requests.</span></span>  

<span data-ttu-id="2f208-200">Después de activar el experimento, asegúrese de reiniciar DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-200">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="2f208-201">Para usar la **consola de red,** siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="2f208-201">To use the **Network Console**, complete the following steps.</span></span>  

1.  <span data-ttu-id="2f208-202">Abra el **panel** Red.</span><span class="sxs-lookup"><span data-stu-id="2f208-202">Open the **Network** pane.</span></span>  
1.  <span data-ttu-id="2f208-203">Busque la solicitud de red que desea cambiar y reenviar.</span><span class="sxs-lookup"><span data-stu-id="2f208-203">Find the network request that you want to change and resend.</span></span>  
1.  <span data-ttu-id="2f208-204">Abra el menú contextual \(right-click\) y elija **Editar y reproducir**.</span><span class="sxs-lookup"><span data-stu-id="2f208-204">Open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  
1.  <span data-ttu-id="2f208-205">Cuando se **abra la consola de** red, edite la información de solicitud de red.</span><span class="sxs-lookup"><span data-stu-id="2f208-205">When the **Network Console** opens, edit the network request information.</span></span>  
1.  <span data-ttu-id="2f208-206">Elija **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="2f208-206">Choose **Send**.</span></span>  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Consola de red en el cajón de la consola" lightbox="../media/network-network-console.msft.png":::
   <span data-ttu-id="2f208-208">**Consola de red** en el **cajón de la** consola</span><span class="sxs-lookup"><span data-stu-id="2f208-208">**Network Console** in the **Console** drawer</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="source-order-viewer"></a><span data-ttu-id="2f208-209">Visor de pedidos de origen</span><span class="sxs-lookup"><span data-stu-id="2f208-209">Source Order Viewer</span></span>  

<span data-ttu-id="2f208-210">**El Visor de pedidos de** origen es un experimento que muestra el orden de los elementos en el origen de la página web.</span><span class="sxs-lookup"><span data-stu-id="2f208-210">**Source Order Viewer** is an experiment that displays the order of elements in the webpage source.</span></span>  <span data-ttu-id="2f208-211">El orden de visualización en pantalla puede diferir del orden del origen, lo que confunde el lector de pantalla y los usuarios de teclado.</span><span class="sxs-lookup"><span data-stu-id="2f208-211">The on-screen display order may differ from the order of the source, which confuses screen reader and keyboard users.</span></span>  <span data-ttu-id="2f208-212">Use el **experimento Visor de pedidos de** origen para encontrar las diferencias entre el orden de visualización en pantalla y el orden del origen.</span><span class="sxs-lookup"><span data-stu-id="2f208-212">Use the **Source Order Viewer** experiment to find the differences between on-screen display order and the order of the source.</span></span>  

<span data-ttu-id="2f208-213">Después de activar el experimento, asegúrese de reiniciar DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-213">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="2f208-214">Para usar **el Visor de pedidos de origen,** siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="2f208-214">To use **Source Order Viewer**, complete the following steps.</span></span>  

1.  <span data-ttu-id="2f208-215">Abra la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="2f208-215">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="2f208-216">Abra el **panel Accesibilidad** en el panel \(bottom\) del cajón.</span><span class="sxs-lookup"><span data-stu-id="2f208-216">Open the **Accessibility** pane in the drawer \(bottom\) panel.</span></span>  
1.  <span data-ttu-id="2f208-217">En la **sección Visor de pedidos de** origen, elija la casilla Mostrar orden **de** origen.</span><span class="sxs-lookup"><span data-stu-id="2f208-217">Under the **Source Order Viewer** section, choose the **Show Source Order** checkbox.</span></span>  
1.  <span data-ttu-id="2f208-218">Resalte cualquier elemento HTML para mostrar una superposición que el orden en el origen de la página web.</span><span class="sxs-lookup"><span data-stu-id="2f208-218">Highlight any HTML element to display an overlay that the order in the webpage source.</span></span>  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Visor de pedidos de origen en el panel Accesibilidad" lightbox="../media/experiments-source-order-viewer.msft.png":::
   <span data-ttu-id="2f208-220">**Visor de pedidos de origen** en el panel **Accesibilidad**</span><span class="sxs-lookup"><span data-stu-id="2f208-220">**Source Order Viewer** in the **Accessibility** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <a name="enable-keyboard-shortcut-editor"></a><span data-ttu-id="2f208-221">Habilitar el editor de métodos abreviados de teclado</span><span class="sxs-lookup"><span data-stu-id="2f208-221">Enable keyboard shortcut editor</span></span>

<span data-ttu-id="2f208-222">Con el **experimento Habilitar editor de métodos** abreviados de teclado activado, puedes personalizar los métodos abreviados de teclado para cualquier acción en DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-222">With the **Enable keyboard shortcut editor** experiment turned on, you may customize keyboard shortcuts for any action in the DevTools.</span></span>  <span data-ttu-id="2f208-223">Para personalizar el método abreviado de teclado de una acción específica, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="2f208-223">To customize the keyboard shortcut for a specific action, complete the following steps.</span></span>  

1.  <span data-ttu-id="2f208-224">[Abra DevTools][DevtoolsOpenMain].</span><span class="sxs-lookup"><span data-stu-id="2f208-224">[Open DevTools][DevtoolsOpenMain].</span></span>  
1.  <span data-ttu-id="2f208-225">Abra [Configuración][DevToolsCustomizeIndexSettings].</span><span class="sxs-lookup"><span data-stu-id="2f208-225">Open [Settings][DevToolsCustomizeIndexSettings].</span></span>  
    *   <span data-ttu-id="2f208-226">Seleccione `Shift` + `?` .</span><span class="sxs-lookup"><span data-stu-id="2f208-226">Select `Shift`+`?`.</span></span>  
1.  <span data-ttu-id="2f208-227">Vaya a la **página Accesos directos.**</span><span class="sxs-lookup"><span data-stu-id="2f208-227">Navigate to the **Shortcuts** page.</span></span>  
1.  <span data-ttu-id="2f208-228">Elija la acción que desea personalizar.</span><span class="sxs-lookup"><span data-stu-id="2f208-228">Choose the action you want to customize.</span></span>  
1.  <span data-ttu-id="2f208-229">Elija el **icono Editar** \( ![ EditKeyboardShortcut ](../media/edit-keyboard-shortcut-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="2f208-229">Choose the **Edit** \(![EditKeyboardShortcut](../media/edit-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Elija la acción que desea personalizar en la página Accesos directos de Configuración" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       <span data-ttu-id="2f208-231">Elija la acción que desea personalizar en la página **Accesos directos** de [Configuración][DevToolsCustomizeIndexSettings]</span><span class="sxs-lookup"><span data-stu-id="2f208-231">Choose the action to customize from the **Shortcuts** page in [Settings][DevToolsCustomizeIndexSettings]</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f208-232">En el teclado, seleccione las teclas que se enlazarán a la acción.</span><span class="sxs-lookup"><span data-stu-id="2f208-232">On the keyboard, select the keys to bind to the action.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Elija las claves que desea asignar a la acción" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="2f208-234">Elija las claves que desea asignar a la acción</span><span class="sxs-lookup"><span data-stu-id="2f208-234">Choose the keys you want to assign to the action</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f208-235">Para guardar el nuevo método abreviado de teclado, elija la marca de verificación \(</span><span class="sxs-lookup"><span data-stu-id="2f208-235">To save your new keyboard shortcut, choose the checkmark \(</span></span>![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)<span data-ttu-id="2f208-237">\) icono.</span><span class="sxs-lookup"><span data-stu-id="2f208-237">\) icon.</span></span>  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Elija el icono de marca de verificación para guardar el nuevo método abreviado de teclado" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       <span data-ttu-id="2f208-239">Elija el icono de marca de verificación para guardar el nuevo método abreviado de teclado</span><span class="sxs-lookup"><span data-stu-id="2f208-239">Choose the checkmark icon to save your new keyboard shortcut</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2f208-240">Seleccione el nuevo método abreviado de teclado para desencadenar la acción en DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-240">Select your new keyboard shortcut to trigger the action in the DevTools.</span></span>  
    
<span data-ttu-id="2f208-241">En la **página Accesos directos,** el icono **Método** abreviado de teclado personalizado \( ![ CustomKeyboardShortcut \) muestra los ](../media/custom-keyboard-shortcut-icon.msft.png) métodos abreviados de teclado personalizados.</span><span class="sxs-lookup"><span data-stu-id="2f208-241">On the **Shortcuts** page, the **Custom Keyboard Shortcut** \(![CustomKeyboardShortcut](../media/custom-keyboard-shortcut-icon.msft.png)\) icon displays keyboard shortcuts you customized.</span></span>  <span data-ttu-id="2f208-242">Para restablecer todos los accesos directos, elija **Restaurar métodos abreviados predeterminados.**</span><span class="sxs-lookup"><span data-stu-id="2f208-242">To reset all shortcuts, choose **Restore default shortcuts**.</span></span>  

<span data-ttu-id="2f208-243">Para descartar los cambios mientras edita los métodos abreviados de teclado para una acción, elija el icono X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="2f208-243">To discard your changes while you edit the keyboard shortcuts for an action, choose the X \(![XKeyboardShortcut](../media/discard-changes-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="2f208-244">Para quitar accesos directos para una acción específica, elija el icono Eliminar **acceso directo** \( ![ DeleteKeyboardShortcut ](../media/delete-keyboard-shortcut-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="2f208-244">To remove shortcuts for a specific action, choose the **Delete shortcut** \(![DeleteKeyboardShortcut](../media/delete-keyboard-shortcut-icon.msft.png)\) icon.</span></span>  <span data-ttu-id="2f208-245">Para agregar varios métodos abreviados para una acción, elija **Agregar un acceso directo.**</span><span class="sxs-lookup"><span data-stu-id="2f208-245">To add multiple shortcuts for an action, choose **Add a shortcut**.</span></span>  

> [!NOTE]
> <span data-ttu-id="2f208-246">Si un método abreviado de teclado está asignado actualmente a otra acción, es posible que no lo guarde para una nueva acción.</span><span class="sxs-lookup"><span data-stu-id="2f208-246">If a keyboard shortcut is currently assigned to another action, you may not save it for a new action.</span></span>  <span data-ttu-id="2f208-247">Primero debe eliminar el método abreviado de teclado de la acción anterior y, a continuación, agregarlo a la nueva acción.</span><span class="sxs-lookup"><span data-stu-id="2f208-247">You must first delete the keyboard shortcut for the previous action and then add it to the new action.</span></span>  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-composited-layers-in-3d-view"></a><span data-ttu-id="2f208-248">Habilitar capas compuestas en la vista 3D</span><span class="sxs-lookup"><span data-stu-id="2f208-248">Enable Composited Layers in 3D View</span></span>  

<span data-ttu-id="2f208-249">Ahora puede visualizar capas junto con índices z y el modelo de objetos de documento \(DOM\).</span><span class="sxs-lookup"><span data-stu-id="2f208-249">You may now visualize Layers alongside z-indexes and the Document Object Model \(DOM\).</span></span>  <span data-ttu-id="2f208-250">Esta característica le ayuda a depurar sin cambiar de contexto con tanta frecuencia.</span><span class="sxs-lookup"><span data-stu-id="2f208-250">This feature helps you debug without switching contexts as often.</span></span>  <span data-ttu-id="2f208-251">Identificó que la reducción del cambio de contexto era un punto de dolor importante.</span><span class="sxs-lookup"><span data-stu-id="2f208-251">You identified that reducing context-switching was a major pain point.</span></span>  <span data-ttu-id="2f208-252">No siempre está claro cómo el código que escribe afecta a la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="2f208-252">It is not always clear how the code you write affects your web app.</span></span>  <span data-ttu-id="2f208-253">Para obtener una experiencia de depuración visual completa, ahora se combinan la vista 3D y las Capas compuestas.</span><span class="sxs-lookup"><span data-stu-id="2f208-253">For a comprehensive visual debugging experience, the 3D View and Composited Layers are now combined.</span></span>  

<span data-ttu-id="2f208-254">Después de activar el experimento, asegúrese de reiniciar DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-254">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="2f208-255">Para usar **capas compuestas,** siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="2f208-255">To use **Composited Layers**, complete the following steps.</span></span>  

1.  <span data-ttu-id="2f208-256">En el cajón, elija la **herramienta Vista 3D.**</span><span class="sxs-lookup"><span data-stu-id="2f208-256">On the drawer, choose the **3D View** tool.</span></span>  
1.  <span data-ttu-id="2f208-257">Abra el **panel Capas compuestas.**</span><span class="sxs-lookup"><span data-stu-id="2f208-257">Open the **Composited Layers** pane.</span></span>  
1.  <span data-ttu-id="2f208-258">Se muestran todas las capas pintadas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f208-258">All of the painted layers of the app are displayed.</span></span>  <span data-ttu-id="2f208-259">Pruebe esta característica con sus propias aplicaciones web.</span><span class="sxs-lookup"><span data-stu-id="2f208-259">Try this feature with your own web apps.</span></span>  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Panel Capas compuestas" lightbox="../media/experiments-layers.msft.png":::
   <span data-ttu-id="2f208-261">Panel **Capas compuestas**</span><span class="sxs-lookup"><span data-stu-id="2f208-261">**Composited Layers** pane</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-new-font-editor-tool-within-the-styles-pane"></a><span data-ttu-id="2f208-262">Habilitar la nueva herramienta Editor de fuentes en el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="2f208-262">Enable new Font Editor tool within the Styles pane</span></span>  

<span data-ttu-id="2f208-263">Ahora puede usar el nuevo Editor de [fuentes][DevtoolsInspectStylesEditFonts] visual para editar fuentes.</span><span class="sxs-lookup"><span data-stu-id="2f208-263">You may now use the new visual [Font Editor][DevtoolsInspectStylesEditFonts] to edit fonts.</span></span>  <span data-ttu-id="2f208-264">Úselo para definir fuentes y características de fuente.</span><span class="sxs-lookup"><span data-stu-id="2f208-264">Use it define fonts and font characteristics.</span></span>  <span data-ttu-id="2f208-265">El Editor **de fuentes visual** le ayuda a completar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="2f208-265">The visual **Font Editor** helps you complete the following actions.</span></span>  

*   <span data-ttu-id="2f208-266">Cambiar entre unidades para distintas propiedades de fuente</span><span class="sxs-lookup"><span data-stu-id="2f208-266">Switch between units for different font properties</span></span>  
*   <span data-ttu-id="2f208-267">Cambiar entre palabras clave para distintas propiedades de fuente</span><span class="sxs-lookup"><span data-stu-id="2f208-267">Switch between keywords for different font properties</span></span>  
*   <span data-ttu-id="2f208-268">Convertir unidades</span><span class="sxs-lookup"><span data-stu-id="2f208-268">Convert units</span></span>  
*   <span data-ttu-id="2f208-269">Generar código CSS preciso</span><span class="sxs-lookup"><span data-stu-id="2f208-269">Generate accurate CSS code</span></span>  
    
<span data-ttu-id="2f208-270">Después de activar el experimento, asegúrese de reiniciar DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-270">After you turn on the experiment, ensure you restart the DevTools.</span></span>  <span data-ttu-id="2f208-271">Para usar el nuevo Editor de **fuentes visuales,** siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="2f208-271">To use the new visual **Font Editor**, complete the following steps.</span></span>  

1.  <span data-ttu-id="2f208-272">Abra la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="2f208-272">Open the **Elements** tool.</span></span>  
1.  <span data-ttu-id="2f208-273">Abra el **panel Estilos.**</span><span class="sxs-lookup"><span data-stu-id="2f208-273">Open the **Styles** pane.</span></span>  
1.  <span data-ttu-id="2f208-274">Elija el **icono Editor de** fuentes.</span><span class="sxs-lookup"><span data-stu-id="2f208-274">Choose the **Font Editor** icon.</span></span>  
    
<span data-ttu-id="2f208-275">Para obtener más información sobre el nuevo **Editor**de fuentes visual, vaya a Editar estilos y configuraciones de fuentes CSS en el panel Estilos [en DevTools][DevtoolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="2f208-275">For more information about the new visual **Font Editor**, navigate to [Edit CSS font styles and settings in the Styles pane in DevTools][DevtoolsInspectStylesEditFonts].</span></span>  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Se resalta el panel Editor de fuentes visuales" lightbox="../media/font-editor-open.msft.png":::
   <span data-ttu-id="2f208-277">Se resalta **el panel Editor de** fuentes visuales</span><span class="sxs-lookup"><span data-stu-id="2f208-277">The visual **Font Editor** pane is highlighted</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-new-css-flexbox-debugging-features"></a><span data-ttu-id="2f208-278">Habilitar nuevas características de depuración de CSS Flexbox</span><span class="sxs-lookup"><span data-stu-id="2f208-278">Enable new CSS Flexbox debugging features</span></span>  

<span data-ttu-id="2f208-279">Esta característica experimental proporciona muchas visualizaciones nuevas que le ayudarán a depurar diseños de CSS Flexbox.</span><span class="sxs-lookup"><span data-stu-id="2f208-279">This experimental feature provides many new visualizations to help you debug CSS Flexbox layouts.</span></span>  <span data-ttu-id="2f208-280">Para obtener una vista previa de las características experimentales más recientes, [activa este experimento](#turn-on-experimental-features) y vuelve a cargar DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-280">To preview the latest experimental features, [turn on this experiment](#turn-on-experimental-features) and reload DevTools.</span></span>  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a><span data-ttu-id="2f208-281">Mostrar superposiciones persistentes en diseños de Flexbox con la herramienta Inspeccionar</span><span class="sxs-lookup"><span data-stu-id="2f208-281">Display persistent overlays on Flexbox layouts with the Inspect tool</span></span>  

<span data-ttu-id="2f208-282">La **herramienta Inspeccionar** proporciona una forma rápida de identificar y visualizar diseños de CSS Flexbox en un sitio web activando el mouse sobre ellos.</span><span class="sxs-lookup"><span data-stu-id="2f208-282">The **Inspect** tool provides a quick way to identify and visualize CSS Flexbox layouts in a website by hovering on them with the mouse.</span></span>  <span data-ttu-id="2f208-283">Elija el **icono Inspeccionar** \( Inspeccionar \) en la esquina superior izquierda ![ de ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-283">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  <span data-ttu-id="2f208-284">A continuación, mientras depura el sitio web, mantenga el mouse en un contenedor flexible para mostrar los contornos alrededor del contenedor flexible.</span><span class="sxs-lookup"><span data-stu-id="2f208-284">Then, while debugging the website, hover on a flex container to display outlines around the flex container.</span></span>  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Mostrar contenedores de Flexbox con la herramienta Inspeccionar" lightbox="../media/flexbox-hover.msft.png":::
   <span data-ttu-id="2f208-286">Mostrar contenedores de Flexbox con **la herramienta Inspeccionar**</span><span class="sxs-lookup"><span data-stu-id="2f208-286">Display Flexbox containers with the **Inspect** tool</span></span>  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a><span data-ttu-id="2f208-287">Mostrar superposiciones persistentes en diseños de Flexbox</span><span class="sxs-lookup"><span data-stu-id="2f208-287">Display persistent overlays on Flexbox layouts</span></span>  

<span data-ttu-id="2f208-288">En Microsoft Edge versión 89 o posterior, la característica experimental CSS Flexbox también ofrece la opción de activar superposiciones persistentes en diseños de Flexbox.</span><span class="sxs-lookup"><span data-stu-id="2f208-288">In Microsoft Edge version 89 or later, the experimental CSS Flexbox feature also offers the option to turn on persistent overlays on Flexbox layouts.</span></span>  <span data-ttu-id="2f208-289">Las superposiciones persistentes proporcionan las siguientes ventajas.</span><span class="sxs-lookup"><span data-stu-id="2f208-289">Persistent overlays provide the following benefits.</span></span>  

*   <span data-ttu-id="2f208-290">Las superposiciones persistentes permanecen visibles en la página web a medida que se desplaza, mueve el mouse y usa otras características de DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-290">Persistent overlays remain visible on the webpage as you scroll, move your mouse, and use other features of the DevTools.</span></span>
*   <span data-ttu-id="2f208-291">Se pueden usar varias superposiciones persistentes al mismo tiempo, para permitirle revisar varios diseños de Flexbox a la vez.</span><span class="sxs-lookup"><span data-stu-id="2f208-291">Multiple persistent overlays may be used at the same time, to allow you to review several Flexbox layouts at once.</span></span>  
*   <span data-ttu-id="2f208-292">Las superposiciones persistentes ofrecen opciones de configuración de color.</span><span class="sxs-lookup"><span data-stu-id="2f208-292">Persistent overlays offer color configuration options.</span></span>  
    
<span data-ttu-id="2f208-293">Para alternar las superposiciones persistentes en el diseño de Flexbox, use una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="2f208-293">To toggle persistent overlays on Flexbox layout, use one of following actions.</span></span>  

*   <span data-ttu-id="2f208-294">Elija el **icono oval de Flexbox** junto a cualquier contenedor de Flexbox que se muestre en el árbol DOM de la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="2f208-294">Choose the **Flexbox** oval icon next to any Flexbox container displayed in the DOM tree of the **Elements** tool.</span></span>  
*   <span data-ttu-id="2f208-295">Abra el nuevo panel **Diseño** ubicado en la **herramienta Elementos** y seleccione la casilla situada junto a cada contenedor de Flexbox que desee resaltar.</span><span class="sxs-lookup"><span data-stu-id="2f208-295">Open the new **Layout** panel located in the **Elements** tool, and choose the checkbox next to each Flexbox container you want to highlight.</span></span>  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Iconos de Flex y panel Diseño en DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   <span data-ttu-id="2f208-297">Iconos de Flex y panel **Diseño** en DevTools</span><span class="sxs-lookup"><span data-stu-id="2f208-297">Flex icons and **Layout** panel in DevTools</span></span>  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a><span data-ttu-id="2f208-298">Configurar superposiciones persistentes</span><span class="sxs-lookup"><span data-stu-id="2f208-298">Configure persistent overlays</span></span>  

<span data-ttu-id="2f208-299">Para configurar opciones para superposiciones persistentes para cuadrículas CSS o diseños de Flexbox, use el **panel** Diseño.</span><span class="sxs-lookup"><span data-stu-id="2f208-299">To configure options for persistent overlays for CSS grids or Flexbox layouts, use the **Layout** pane.</span></span>  <span data-ttu-id="2f208-300">El **panel** Diseño se encuentra en la **herramienta Elementos** junto a los paneles **Estilos** **y** Calculados.</span><span class="sxs-lookup"><span data-stu-id="2f208-300">The **Layout** pane is located in the **Elements** tool next to the **Styles** and **Computed** panes.</span></span>  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Panel Diseño" lightbox="../media/flexbox-layout.msft.png":::
   <span data-ttu-id="2f208-302">Panel Diseño</span><span class="sxs-lookup"><span data-stu-id="2f208-302">Layout panel</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable--button-tab-menus-to-open-more-tools"></a><span data-ttu-id="2f208-303">Habilitar menús de pestañas + botón para abrir más herramientas</span><span class="sxs-lookup"><span data-stu-id="2f208-303">Enable + button tab menus to open more tools</span></span>  

<span data-ttu-id="2f208-304">Ahora puede abrir más herramientas con el nuevo icono **Más herramientas** \( `+` \).</span><span class="sxs-lookup"><span data-stu-id="2f208-304">You may now open more tools using the new **More Tools** \(`+`\) icon.</span></span>  <span data-ttu-id="2f208-305">Después de activar los menús de la pestaña Habilitar + botón para abrir más herramientas experimentar y volver a cargar DevTools, se muestra un signo más \( \) a la derecha del grupo de **pestañas** en la parte superior `+` de DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-305">After you turn on the **Enable + button tab menus to open more tools** experiment and reload DevTools, a plus sign \(`+`\) displays to the right of the tab group at the top of the DevTools.</span></span>  <span data-ttu-id="2f208-306">Para mostrar una lista de otras herramientas que puede agregar a la barra de pestañas, elija el nuevo icono **Más** herramientas \( `+` \).</span><span class="sxs-lookup"><span data-stu-id="2f208-306">To display a list of other tools that you may add to the tab bar, choose the new **More Tools** \(`+`\) icon.</span></span>  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Más herramientas en el panel superior" lightbox="../media/experiments-more-tools-button.msft.png":::
   <span data-ttu-id="2f208-308">**Más herramientas** en el panel superior</span><span class="sxs-lookup"><span data-stu-id="2f208-308">**More Tools** in the top pane</span></span>
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-welcome-tool"></a><span data-ttu-id="2f208-309">Habilitar herramienta de bienvenida</span><span class="sxs-lookup"><span data-stu-id="2f208-309">Enable Welcome tool</span></span>

<span data-ttu-id="2f208-310">Este experimento reemplaza la herramienta **Novedades** por la nueva **herramienta De** bienvenida.</span><span class="sxs-lookup"><span data-stu-id="2f208-310">This experiment replaces the **What's New** tool with the new **Welcome** tool.</span></span>  <span data-ttu-id="2f208-311">Muestra un diseño actualizado para el siguiente contenido.</span><span class="sxs-lookup"><span data-stu-id="2f208-311">It displays a refreshed design for the following content.</span></span>  

*   <span data-ttu-id="2f208-312">Vínculos a documentos para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="2f208-312">Links to developer docs</span></span>  
*   <span data-ttu-id="2f208-313">las características más recientes</span><span class="sxs-lookup"><span data-stu-id="2f208-313">the latest features</span></span>  
*   <span data-ttu-id="2f208-314">notas de la versión</span><span class="sxs-lookup"><span data-stu-id="2f208-314">release notes</span></span>  
*   <span data-ttu-id="2f208-315">Opción para ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2f208-315">Option to contact the Microsoft Edge DevTools team</span></span>  
    
<span data-ttu-id="2f208-316">La **herramienta De** bienvenida se abre automáticamente después de cada actualización de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2f208-316">The **Welcome** tool opens automatically after each update to Microsoft Edge.</span></span>  <span data-ttu-id="2f208-317">Para evitar que se muestre la herramienta **de** bienvenida después de cada actualización, desactive la casilla situada junto a la pestaña Abrir después de cada **actualización** en el **título de** la herramienta de bienvenida.</span><span class="sxs-lookup"><span data-stu-id="2f208-317">To prevent the display of the **Welcome** tool after each update, clear the checkbox next to **Open tab after each update** under the **Welcome** tool title.</span></span>  

<span data-ttu-id="2f208-318">Si prefiere la herramienta **novedades** original, [][DevtoolsCustomizeIndexSettings]vaya a Experimentos de configuración y quite la casilla situada junto a  >  \*\*\*\* La pestaña Habilitar **bienvenida**.</span><span class="sxs-lookup"><span data-stu-id="2f208-318">If you prefer the original **What's New** tool, navigate to [Settings][DevtoolsCustomizeIndexSettings] > **Experiments** and remove the checkbox next to **Enable Welcome tab**.</span></span>  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Herramienta de bienvenida" lightbox="../media/experiments-welcome.msft.png":::
   <span data-ttu-id="2f208-320">**Herramienta de** bienvenida</span><span class="sxs-lookup"><span data-stu-id="2f208-320">**Welcome** tool</span></span>  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a><span data-ttu-id="2f208-321">Características experimentales anteriores</span><span class="sxs-lookup"><span data-stu-id="2f208-321">Previous experimental features</span></span>  

*   <span data-ttu-id="2f208-322">[La vista 3D][Devtools3dViewIndex] ya está disponible y activada de forma predeterminada en Microsoft Edge versión 83 o posterior.</span><span class="sxs-lookup"><span data-stu-id="2f208-322">[3D View][Devtools3dViewIndex] is now available and turned on by default in Microsoft Edge version 83 or later.</span></span>  
*   <span data-ttu-id="2f208-323">[Activar la compatibilidad para mover pestañas][DevtoolsMoveTabs] entre paneles ya está disponible y activada de forma predeterminada en Microsoft Edge versión 85 o posterior.</span><span class="sxs-lookup"><span data-stu-id="2f208-323">[Turn on support to move tabs between panels][DevtoolsMoveTabs] is now available and turned on by default in Microsoft Edge version 85 or later.</span></span>  
*   <span data-ttu-id="2f208-324">[Personalizar métodos abreviados de][DevtoolsCustomKeyboardShortcuts] teclado ahora está disponible y activado de forma predeterminada en Microsoft Edge versión 86 o posterior.</span><span class="sxs-lookup"><span data-stu-id="2f208-324">[Customize Keyboard Shortcuts][DevtoolsCustomKeyboardShortcuts] is now available and turned on by default in Microsoft Edge version 86 or later.</span></span>  
*   <span data-ttu-id="2f208-325">[Emulación: el modo de pantalla dual ya][DevtoolsDeviceModeDualScreenAndFoldables] está disponible y activado de forma predeterminada en Microsoft Edge versión 89 o posterior.</span><span class="sxs-lookup"><span data-stu-id="2f208-325">[Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
*   <span data-ttu-id="2f208-326">[Activar nuevas características de depuración de][DevtoolsCssGrid] cuadrícula CSS ahora está disponible y activada de forma predeterminada en Microsoft Edge versión 89 o posterior.</span><span class="sxs-lookup"><span data-stu-id="2f208-326">[Turn on new CSS grid debugging features][DevtoolsCssGrid] is now available and turned on by default in Microsoft Edge version 89 or later.</span></span>  
    
## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="2f208-327">Proporcionar comentarios sobre características experimentales</span><span class="sxs-lookup"><span data-stu-id="2f208-327">Providing feedback on experimental features</span></span>  

<span data-ttu-id="2f208-328">Para proporcionar comentarios sobre los experimentos de Microsoft Edge DevTools o cualquier otra cosa relacionada con DevTools.</span><span class="sxs-lookup"><span data-stu-id="2f208-328">To provide feedback on Microsoft Edge DevTools experiments, or anything else related to DevTools.</span></span>  

*   <span data-ttu-id="2f208-329">Enviar sus comentarios con el icono **Enviar comentarios** en DevTools</span><span class="sxs-lookup"><span data-stu-id="2f208-329">Send your feedback using the **Send Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="2f208-330">Tweet en [@EdgeDevTools][TwitterEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="2f208-330">Tweet at [@EdgeDevTools][TwitterEdgedevtools]</span></span>  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="El icono Enviar comentarios en Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="2f208-332">El **icono Enviar comentarios** en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2f208-332">The **Send Feedback** icon in Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Vista 3D | Microsoft Docs"  
[DevtoolsCssGrid]: ../css/grid.md "Inspeccionar CSS Grid en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsMoveTabs]: ../customize/index.md "Personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móviles con modo de dispositivo en Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Editar estilos y configuraciones de fuentes CSS en el panel Estilos de DevTools | Microsoft Docs"  
[DevtoolsIssues]: ../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas de Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsShortcuts]: ../shortcuts/index.md "Métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Personalización de métodos abreviados de teclado en las herramientas de desarrollo de Microsoft Edge | Microsoft Docs"  
[DevtoolsOpenMain]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  

[DualScreenWebIndex]: /dual-screen/web/index "Experiencias web de pantalla doble | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtener el emulador de Surface Duo | Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con la costura: introducción a los dispositivos de pantalla doble | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Usa el emulador de Surface Duo | Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Característica de pantalla de medios CSS para la detección de pantalla doble | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "La API de JavaScript getWindowSegments para dispositivos de pantalla doble | Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clientes de Escritorio remoto | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Galaxy Fold | Samsung"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Emular dispositivos de pantalla doble y plegables en Microsoft Edge DevTools | Microsoft Docs"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  

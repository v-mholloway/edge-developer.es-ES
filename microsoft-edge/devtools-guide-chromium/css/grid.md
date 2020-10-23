---
description: Aprenda a usar Microsoft Edge DevTools para ver y cambiar la CSS de una página CSS.
title: Inspeccionar cuadrícula CSS en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 150aea57aa676580b554cc74292671ed567a0a2c
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/23/2020
ms.locfileid: "11134199"
---
# <span data-ttu-id="306ba-104">Inspeccionar cuadrícula CSS</span><span class="sxs-lookup"><span data-stu-id="306ba-104">Inspect CSS Grid</span></span>  

<span data-ttu-id="306ba-105">Este artículo le muestra cómo identificar las cuadrículas CSS en un sitio web y cómo depurar problemas de diseño de cuadrícula con superposiciones de cuadrícula personalizables.</span><span class="sxs-lookup"><span data-stu-id="306ba-105">This article walks you through identifying CSS grids on a website and debugging grid layout issues using customizable grid overlays.</span></span>  

<span data-ttu-id="306ba-106">Los ejemplos que se usan en las figuras de este artículo se han tomado de las siguientes páginas Web.</span><span class="sxs-lookup"><span data-stu-id="306ba-106">The examples used in the figures in this article are taken from the following webpages.</span></span>  

*   [<span data-ttu-id="306ba-107">Cuadro de frutas</span><span class="sxs-lookup"><span data-stu-id="306ba-107">Fruit box</span></span>][JecFyiDemoCssGridFruit]  
*   [<span data-ttu-id="306ba-108">Cuadro de bocadillo</span><span class="sxs-lookup"><span data-stu-id="306ba-108">Snack box</span></span>][JecFyiDemoCssGridSnack]  

## <span data-ttu-id="306ba-109">Antes de comenzar</span><span class="sxs-lookup"><span data-stu-id="306ba-109">Before you begin</span></span>  

<span data-ttu-id="306ba-110">CSS Grid es un versátil paradigma de diseño para la Web.</span><span class="sxs-lookup"><span data-stu-id="306ba-110">CSS Grid is a powerful layout paradigm for the web.</span></span>  <span data-ttu-id="306ba-111">Un excelente lugar para comenzar a aprender sobre CSS Grid y las numerosas características es la [Guía de diseño de cuadrícula CSS][MdnCssGridLayout] en MDN.</span><span class="sxs-lookup"><span data-stu-id="306ba-111">A great place to get started learning about CSS Grid and the many features is the [CSS Grid Layout guide][MdnCssGridLayout] on MDN.</span></span>  

## <span data-ttu-id="306ba-112">Descubrir cuadrículas CSS</span><span class="sxs-lookup"><span data-stu-id="306ba-112">Discover CSS grids</span></span>  

<span data-ttu-id="306ba-113">Cuando un elemento HTML de la página se tiene o se le `display: grid` `display: inline-grid` aplica, `grid` se muestra un distintivo junto a él en el panel [elementos][DevtoolsGuideChromiumOpen] .</span><span class="sxs-lookup"><span data-stu-id="306ba-113">When an HTML element on your page has `display: grid` or `display: inline-grid` applied to it, a `grid` badge is displayed next to it in the [Elements][DevtoolsGuideChromiumOpen] panel.</span></span>  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Descubrir cuadrícula" lightbox="../media/grid-discover-grid.msft.png":::
   <span data-ttu-id="306ba-115">Descubrir cuadrícula</span><span class="sxs-lookup"><span data-stu-id="306ba-115">Discover grid</span></span>  
:::image-end:::  

<span data-ttu-id="306ba-116">Seleccione el distintivo para alternar la visualización de una superposición de cuadrícula en la página.</span><span class="sxs-lookup"><span data-stu-id="306ba-116">Select the badge to toggle the display of a grid overlay on the page.</span></span>  <span data-ttu-id="306ba-117">La superposición aparece sobre el elemento, dispuestos como una cuadrícula para mostrar la posición de las líneas de la cuadrícula y las pistas:</span><span class="sxs-lookup"><span data-stu-id="306ba-117">The overlay appears over the element, laid out like a grid to display the position of the grid lines and tracks:</span></span>  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Descubrir cuadrícula" lightbox="../media/grid-highlight-grid.msft.png":::
   <span data-ttu-id="306ba-119">Activar distintivo de cuadrícula</span><span class="sxs-lookup"><span data-stu-id="306ba-119">Toggle grid badge</span></span>  
:::image-end:::  

<span data-ttu-id="306ba-120">Abrir el panel **diseño** .</span><span class="sxs-lookup"><span data-stu-id="306ba-120">Open the **Layout** pane.</span></span>  <span data-ttu-id="306ba-121">Cuando se incluyen cuadrículas en una página, el panel de **diseño** incluye una sección de **cuadrícula** que contiene varias opciones para ver las cuadrículas.</span><span class="sxs-lookup"><span data-stu-id="306ba-121">When grids are included on a page, the **Layout** pane includes a **Grid** section containing a number of options for viewing the grids.</span></span>  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Descubrir cuadrícula" lightbox="../media/grid-layout-pane.msft.png":::
   <span data-ttu-id="306ba-123">Panel de **diseño**</span><span class="sxs-lookup"><span data-stu-id="306ba-123">**Layout** pane</span></span>  
:::image-end:::  

<span data-ttu-id="306ba-124">La sección de **cuadrícula** en el panel de **diseño** contiene las siguientes 2 subsecciones.</span><span class="sxs-lookup"><span data-stu-id="306ba-124">The **Grid** section in the **Layout** pane contains the following 2 sub-sections.</span></span>  

*   <span data-ttu-id="306ba-125">Configuración de superposición</span><span class="sxs-lookup"><span data-stu-id="306ba-125">Overlay display settings</span></span>  
*   <span data-ttu-id="306ba-126">Superposiciones de cuadrícula</span><span class="sxs-lookup"><span data-stu-id="306ba-126">Grid overlays</span></span>  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## <span data-ttu-id="306ba-127">Configuración de superposición</span><span class="sxs-lookup"><span data-stu-id="306ba-127">Overlay display settings</span></span>  

<span data-ttu-id="306ba-128">La **configuración de la pantalla de superposición** consta de dos partes:</span><span class="sxs-lookup"><span data-stu-id="306ba-128">The **Overlay display settings** consists of following 2 parts.</span></span>  

*   <span data-ttu-id="306ba-129">Elija una de las siguientes opciones en el menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="306ba-129">Choose one of the following options from the dropdown menu.</span></span>  
    
    | <span data-ttu-id="306ba-130">Opción de línea</span><span class="sxs-lookup"><span data-stu-id="306ba-130">Line option</span></span> | <span data-ttu-id="306ba-131">Detalles</span><span class="sxs-lookup"><span data-stu-id="306ba-131">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="306ba-132">Ocultar etiquetas de línea</span><span class="sxs-lookup"><span data-stu-id="306ba-132">Hide line labels</span></span>** | <span data-ttu-id="306ba-133">Oculte las etiquetas de las líneas de cada superposición de cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="306ba-133">Hide the labels of the lines for each grid overlay.</span></span> |  
    | **<span data-ttu-id="306ba-134">Mostrar números de línea</span><span class="sxs-lookup"><span data-stu-id="306ba-134">Show line numbers</span></span>** | <span data-ttu-id="306ba-135">Mostrar los números de las líneas de cada superposición de cuadrícula \ (seleccionado de forma predeterminada \).</span><span class="sxs-lookup"><span data-stu-id="306ba-135">Display the numbers of the lines for each grid overlay \(selected by default\).</span></span> |  
    | **<span data-ttu-id="306ba-136">Mostrar nombres de línea</span><span class="sxs-lookup"><span data-stu-id="306ba-136">Show line names</span></span>** | <span data-ttu-id="306ba-137">Mostrar los nombres de las líneas de cada cuadrícula superpuestas cuando se proporcionen nombres.</span><span class="sxs-lookup"><span data-stu-id="306ba-137">Display the names of the lines for each grid overlay when names are provided.</span></span> |  
    
*  <span data-ttu-id="306ba-138">Seleccione la casilla junto a las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="306ba-138">Choose the checkbox next the following options.</span></span>  
    
    | <span data-ttu-id="306ba-139">Opción</span><span class="sxs-lookup"><span data-stu-id="306ba-139">Option</span></span> | <span data-ttu-id="306ba-140">Detalles</span><span class="sxs-lookup"><span data-stu-id="306ba-140">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="306ba-141">Mostrar tamaños de seguimiento</span><span class="sxs-lookup"><span data-stu-id="306ba-141">Show track sizes</span></span>**  | <span data-ttu-id="306ba-142">Mostrar \ (u ocultar \) el tamaño de las pistas.</span><span class="sxs-lookup"><span data-stu-id="306ba-142">Display \(or hide\) the sizes of the tracks.</span></span> |  
    | **<span data-ttu-id="306ba-143">Mostrar nombres de área</span><span class="sxs-lookup"><span data-stu-id="306ba-143">Show area names</span></span>** | <span data-ttu-id="306ba-144">Mostrar \ (u ocultar \) los nombres del área, cuando se proporcionen nombres.</span><span class="sxs-lookup"><span data-stu-id="306ba-144">Display \(or hide\) the names of the area, when names are provided.</span></span> |  
    | **<span data-ttu-id="306ba-145">Extender las líneas de la cuadrícula</span><span class="sxs-lookup"><span data-stu-id="306ba-145">Extend grid lines</span></span>** | <span data-ttu-id="306ba-146">Muestra \ (u oculta \) las extensiones de las dimensiones de la cuadrícula a lo largo de cada eje.</span><span class="sxs-lookup"><span data-stu-id="306ba-146">Displays \(or hides\) the extensions of the grid dimensions along each axis.</span></span>  <span data-ttu-id="306ba-147">De forma predeterminada, las líneas de cuadrícula solo se muestran dentro del elemento con `display: grid` o `display: inline-grid` CSS establecido.</span><span class="sxs-lookup"><span data-stu-id="306ba-147">By default, grid lines are only shown inside the element with `display: grid` or `display: inline-grid` CSS set on it.</span></span> |  
    
<span data-ttu-id="306ba-148">En las siguientes secciones se proporcionan detalles para cada una de las **Opciones de superposición de pantalla**.</span><span class="sxs-lookup"><span data-stu-id="306ba-148">The following sections provide details for each of the **Overlay display settings**.</span></span>  

### <span data-ttu-id="306ba-149">Mostrar números de línea</span><span class="sxs-lookup"><span data-stu-id="306ba-149">Show line numbers</span></span>  

<span data-ttu-id="306ba-150">De forma predeterminada, los números de línea positivos y negativos se muestran en la superposición de la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="306ba-150">By default, the positive and negative line numbers are displayed on the grid overlay.</span></span>  

<span data-ttu-id="306ba-151">Para obtener más información sobre números negativos en la superposición de cuadrícula, vaya a [ubicación basada en líneas con cuadrícula CSS][MdnLineBasedPlacementCssGrid].</span><span class="sxs-lookup"><span data-stu-id="306ba-151">For more information about negative numbers in the grid overlay, navigate to [Line-based placement with CSS Grid][MdnLineBasedPlacementCssGrid].</span></span>  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Descubrir cuadrícula" lightbox="../media/grid-show-line-numbers.msft.png":::
   <span data-ttu-id="306ba-153">Mostrar números de línea</span><span class="sxs-lookup"><span data-stu-id="306ba-153">Display line numbers</span></span>  
:::image-end:::  

### <span data-ttu-id="306ba-154">Ocultar etiquetas de línea</span><span class="sxs-lookup"><span data-stu-id="306ba-154">Hide line labels</span></span>  

<span data-ttu-id="306ba-155">Seleccione **ocultar etiquetas de línea** para ocultar los números de línea.</span><span class="sxs-lookup"><span data-stu-id="306ba-155">Select **Hide line labels** to hide the line numbers.</span></span>  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Descubrir cuadrícula" lightbox="../media/grid-hide-line-labels.msft.png":::
   <span data-ttu-id="306ba-157">Ocultar etiquetas de línea</span><span class="sxs-lookup"><span data-stu-id="306ba-157">Hide line labels</span></span>  
:::image-end:::  

### <span data-ttu-id="306ba-158">Mostrar nombres de línea</span><span class="sxs-lookup"><span data-stu-id="306ba-158">Show line names</span></span>  

<!--todo: @rachel verify the link and text for line name -->  
<span data-ttu-id="306ba-159">Para obtener más información sobre los nombres de línea en la superposición de cuadrícula, desplácese al [diseño mediante líneas de cuadrícula con nombre][MdnLayoutUsingNamedGridLines].</span><span class="sxs-lookup"><span data-stu-id="306ba-159">For more information about line names in the grid overlay, navigate to [Layout using named grid lines][MdnLayoutUsingNamedGridLines].</span></span>  

<span data-ttu-id="306ba-160">Seleccione **Mostrar nombres de línea** para ver los nombres de línea en lugar de los números.</span><span class="sxs-lookup"><span data-stu-id="306ba-160">Select **Show line names** to view the line names instead of numbers.</span></span>  <span data-ttu-id="306ba-161">En el ejemplo, cuatro líneas tienen nombres: `left` , `middle1` , `middle2` y `right` .</span><span class="sxs-lookup"><span data-stu-id="306ba-161">In the example, 4 lines have names: `left`, `middle1`, `middle2`, and `right`.</span></span>  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Descubrir cuadrícula" lightbox="../media/grid-show-line-names.msft.png":::
   **<span data-ttu-id="306ba-163">Mostrar nombres de línea</span><span class="sxs-lookup"><span data-stu-id="306ba-163">Show line names</span></span>**  
:::image-end:::  

### <span data-ttu-id="306ba-164">Mostrar tamaños de seguimiento</span><span class="sxs-lookup"><span data-stu-id="306ba-164">Show track sizes</span></span>  

<span data-ttu-id="306ba-165">Active la casilla **Mostrar tamaños de seguimiento** para ver los tamaños de las pistas de la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="306ba-165">Enable the **Show track sizes** checkbox to view the track sizes of the grid.</span></span>  

<span data-ttu-id="306ba-166">DevTools muestra `[authored size]` y `[computed size]` en cada etiqueta de línea.</span><span class="sxs-lookup"><span data-stu-id="306ba-166">DevTools displays `[authored size]` and `[computed size]` in each line label.</span></span>  

| <span data-ttu-id="306ba-167">Tamaño</span><span class="sxs-lookup"><span data-stu-id="306ba-167">Size</span></span> | <span data-ttu-id="306ba-168">Detalles</span><span class="sxs-lookup"><span data-stu-id="306ba-168">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="306ba-169">tamaño creado</span><span class="sxs-lookup"><span data-stu-id="306ba-169">authored size</span></span>** | <span data-ttu-id="306ba-170">El tamaño definido en la hoja de estilos \ (se omite si no se define \).</span><span class="sxs-lookup"><span data-stu-id="306ba-170">The size defined in stylesheet \(omitted if not defined\).</span></span> |  
| **<span data-ttu-id="306ba-171">tamaño calculado</span><span class="sxs-lookup"><span data-stu-id="306ba-171">computed size</span></span>** | <span data-ttu-id="306ba-172">Tamaño real en pantalla.</span><span class="sxs-lookup"><span data-stu-id="306ba-172">The actual size on screen.</span></span> |  

<span data-ttu-id="306ba-173">En la demostración, el `snack-box` tamaño de las columnas se define en la `grid-template-columns:1fr 2fr;` CSS.</span><span class="sxs-lookup"><span data-stu-id="306ba-173">In the demo, the `snack-box` column sizes are defined in the `grid-template-columns:1fr 2fr;` CSS.</span></span>  <span data-ttu-id="306ba-174">Por lo tanto, las etiquetas de las líneas de columna muestran tanto los tamaños de los usuarios como los calculados.</span><span class="sxs-lookup"><span data-stu-id="306ba-174">Therefore, the column line labels display both authored and computed sizes.</span></span>  

| <span data-ttu-id="306ba-175">Tamaño de la pista</span><span class="sxs-lookup"><span data-stu-id="306ba-175">Track size</span></span> | <span data-ttu-id="306ba-176">Tamaño creado</span><span class="sxs-lookup"><span data-stu-id="306ba-176">Authored size</span></span> | <span data-ttu-id="306ba-177">Tamaño calculado</span><span class="sxs-lookup"><span data-stu-id="306ba-177">Computed size</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="306ba-178">**1fr** &#x2022; **96.66 PX**</span><span class="sxs-lookup"><span data-stu-id="306ba-178">**1fr** &#x2022; **96.66px**</span></span> | <span data-ttu-id="306ba-179">1fr</span><span class="sxs-lookup"><span data-stu-id="306ba-179">1fr</span></span> | <span data-ttu-id="306ba-180">96.66 PX</span><span class="sxs-lookup"><span data-stu-id="306ba-180">96.66px</span></span> |  
| <span data-ttu-id="306ba-181">**2fr** &#x2022; **193.32 PX**</span><span class="sxs-lookup"><span data-stu-id="306ba-181">**2fr** &#x2022; **193.32px**</span></span> | <span data-ttu-id="306ba-182">2fr</span><span class="sxs-lookup"><span data-stu-id="306ba-182">2fr</span></span> | <span data-ttu-id="306ba-183">193.32 PX</span><span class="sxs-lookup"><span data-stu-id="306ba-183">193.32px</span></span> |  

<span data-ttu-id="306ba-184">Las etiquetas de línea de fila muestran solo los tamaños calculados, ya que no hay tamaños de fila definidos en la hoja de estilos.</span><span class="sxs-lookup"><span data-stu-id="306ba-184">The row line labels display only computed sizes, since there are no row sizes defined in the stylesheet.</span></span>  

| <span data-ttu-id="306ba-185">Tamaño de la pista</span><span class="sxs-lookup"><span data-stu-id="306ba-185">Track size</span></span> | <span data-ttu-id="306ba-186">Tamaño creado</span><span class="sxs-lookup"><span data-stu-id="306ba-186">Authored size</span></span> | <span data-ttu-id="306ba-187">Tamaño calculado</span><span class="sxs-lookup"><span data-stu-id="306ba-187">Computed size</span></span> |  
|:--- |:--- |:--- |  
| **<span data-ttu-id="306ba-188">80px</span><span class="sxs-lookup"><span data-stu-id="306ba-188">80px</span></span>** | &nbsp;| <span data-ttu-id="306ba-189">80px</span><span class="sxs-lookup"><span data-stu-id="306ba-189">80px</span></span> |  
| **<span data-ttu-id="306ba-190">80px</span><span class="sxs-lookup"><span data-stu-id="306ba-190">80px</span></span>** | &nbsp;| <span data-ttu-id="306ba-191">80px</span><span class="sxs-lookup"><span data-stu-id="306ba-191">80px</span></span> |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Descubrir cuadrícula" lightbox="../media/grid-show-track-sizes.msft.png":::
   **<span data-ttu-id="306ba-193">Mostrar tamaños de seguimiento</span><span class="sxs-lookup"><span data-stu-id="306ba-193">Show track sizes</span></span>**  
:::image-end:::  

### <span data-ttu-id="306ba-194">Mostrar nombres de área</span><span class="sxs-lookup"><span data-stu-id="306ba-194">Show area names</span></span>  

<span data-ttu-id="306ba-195">Para ver los nombres de las áreas, active la casilla **Mostrar nombres de área** .</span><span class="sxs-lookup"><span data-stu-id="306ba-195">To view the area names, enable the **Show area names** checkbox.</span></span>  <span data-ttu-id="306ba-196">En el ejemplo, hay 3 áreas en la cuadrícula: **Top**, **bottom1** y **bottom2**.</span><span class="sxs-lookup"><span data-stu-id="306ba-196">In the example, there are 3 areas in the grid: **top**, **bottom1** and **bottom2**.</span></span>  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Descubrir cuadrícula" lightbox="../media/grid-show-area-names.msft.png":::
   **<span data-ttu-id="306ba-198">Mostrar nombres de área</span><span class="sxs-lookup"><span data-stu-id="306ba-198">Show area names</span></span>**  
:::image-end:::  

### <span data-ttu-id="306ba-199">Extender las líneas de la cuadrícula</span><span class="sxs-lookup"><span data-stu-id="306ba-199">Extend grid lines</span></span>  

<span data-ttu-id="306ba-200">Active la casilla **extender líneas de cuadrícula** para extender las líneas de la cuadrícula al borde de la ventanilla a lo largo de cada eje.</span><span class="sxs-lookup"><span data-stu-id="306ba-200">Enable the **Extend grid lines** checkbox to extend the grid lines to the edge of the viewport along each axis.</span></span>  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Descubrir cuadrícula" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **<span data-ttu-id="306ba-202">Extender las líneas de la cuadrícula</span><span class="sxs-lookup"><span data-stu-id="306ba-202">Extend grid lines</span></span>**  
:::image-end:::  

## <span data-ttu-id="306ba-203">Superposiciones de cuadrícula</span><span class="sxs-lookup"><span data-stu-id="306ba-203">Grid overlays</span></span>  

<span data-ttu-id="306ba-204">La sección de **superposiciones de cuadrícula** contiene una lista de cuadrículas que están presentes en la página, cada una con una casilla, junto con varias opciones.</span><span class="sxs-lookup"><span data-stu-id="306ba-204">The **Grid overlays** section contains a list of grids that are present on the page, each with a checkbox, along with various options.</span></span>  

### <span data-ttu-id="306ba-205">Habilitar vistas superpuestas de varias cuadrículas</span><span class="sxs-lookup"><span data-stu-id="306ba-205">Enable overlay views of multiple grids</span></span>  

<!--todo: @zoher verify and provide updates -->  

<span data-ttu-id="306ba-206">Para mostrar la cuadrícula de superposición para varias cuadrículas, seleccione la casilla junto a cada nombre de la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="306ba-206">To display the overlay grid for multiple grids, choose the checkbox next to each name of the grid.</span></span>  <span data-ttu-id="306ba-207">En el ejemplo, se han habilitado dos superposiciones de cuadrícula que se representan con distintos colores.</span><span class="sxs-lookup"><span data-stu-id="306ba-207">In the example, there are 2 grid overlays enabled that are each represented with different colors.</span></span>  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Descubrir cuadrícula" lightbox="../media/grid-grid-overlays.msft.png":::
   <span data-ttu-id="306ba-209">Habilitar vistas superpuestas de varias cuadrículas</span><span class="sxs-lookup"><span data-stu-id="306ba-209">Enable overlay views of multiple grids</span></span>  
:::image-end:::  

### <span data-ttu-id="306ba-210">Personalizar el color de superposición de cuadrícula</span><span class="sxs-lookup"><span data-stu-id="306ba-210">Customize the grid overlay color</span></span>  

<span data-ttu-id="306ba-211">Para abrir el selector de colores y personalizar el color de superposición de cuadrícula, seleccione el cuadro situado junto al nombre de la superposición de cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="306ba-211">To open the color picker and customize the grid overlay color, choose the box next to the name of the grid overlay.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Descubrir cuadrícula" lightbox="../media/grid-grid-overlays-color.msft.png":::
   <span data-ttu-id="306ba-213">Personalizar el color de superposición de cuadrícula</span><span class="sxs-lookup"><span data-stu-id="306ba-213">Customize the grid overlay color</span></span>  
:::image-end:::  

### <span data-ttu-id="306ba-214">Resaltar la cuadrícula</span><span class="sxs-lookup"><span data-stu-id="306ba-214">Highlight the grid</span></span>  

<span data-ttu-id="306ba-215">Para resaltar el elemento HTML en el panel **elementos** y desplazarse hasta él en la página web, elija el **elemento Mostrar en el panel elementos** \ ( ![ elemento Mostrar en el icono del panel elementos ][ImageShowElementInElementsPanelIcon] ).</span><span class="sxs-lookup"><span data-stu-id="306ba-215">To highlight the HTML element in the **Elements** panel and scroll to it on the webpage, choose the **Show element in the Elements panel** \(![Show element in the Elements panel icon][ImageShowElementInElementsPanelIcon]\) icon.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Descubrir cuadrícula" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   <span data-ttu-id="306ba-217">Resaltar la cuadrícula</span><span class="sxs-lookup"><span data-stu-id="306ba-217">Highlight the grid</span></span>  
:::image-end:::  

## <span data-ttu-id="306ba-218">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="306ba-218">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageShowElementInElementsPanelIcon]: ../media/show-element-in-element-panel-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Abrir Microsoft Edge DevTools | Microsoft docs"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "Cuadrícula CSS | JEC. FYI"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "Cuadrícula CSS | JEC. FYI"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Diseño de cuadrícula CSS | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Diseño usando líneas de cuadrícula con nombre | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Ubicación basada en líneas con CSS Grid | MDN"  

> [!NOTE]
> <span data-ttu-id="306ba-225">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="306ba-225">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="306ba-226">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/grid) y está creada por [Jecelyn Yeen][JecelynYeen] \ (defensor para desarrolladores, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="306ba-226">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/grid) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="306ba-228">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="306ba-228">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

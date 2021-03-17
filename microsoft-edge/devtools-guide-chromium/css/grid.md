---
description: Obtenga información sobre cómo usar Microsoft Edge DevTools para ver y cambiar el CSS de una página CSS.
title: Inspeccionar css grid en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 034fbdf82ddba39fc0818bc6f3add8824c6bb3ac
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439264"
---
# <a name="inspect-css-grid"></a><span data-ttu-id="5b085-104">Inspeccionar cuadrícula CSS</span><span class="sxs-lookup"><span data-stu-id="5b085-104">Inspect CSS Grid</span></span>  

<span data-ttu-id="5b085-105">En este artículo se le guía a través de la identificación de cuadrículas CSS en un sitio web y la depuración de problemas de diseño de cuadrícula mediante superposiciones de cuadrícula personalizables.</span><span class="sxs-lookup"><span data-stu-id="5b085-105">This article walks you through identifying CSS grids on a website and debugging grid layout issues using customizable grid overlays.</span></span>  

<span data-ttu-id="5b085-106">Los ejemplos usados en las figuras de este artículo se toman de las siguientes páginas web.</span><span class="sxs-lookup"><span data-stu-id="5b085-106">The examples used in the figures in this article are taken from the following webpages.</span></span>  

*   [<span data-ttu-id="5b085-107">Cuadro de frutas</span><span class="sxs-lookup"><span data-stu-id="5b085-107">Fruit box</span></span>][JecFyiDemoCssGridFruit]  
*   [<span data-ttu-id="5b085-108">Caja de refrigerio</span><span class="sxs-lookup"><span data-stu-id="5b085-108">Snack box</span></span>][JecFyiDemoCssGridSnack]  

## <a name="before-you-begin"></a><span data-ttu-id="5b085-109">Antes de comenzar</span><span class="sxs-lookup"><span data-stu-id="5b085-109">Before you begin</span></span>  

<span data-ttu-id="5b085-110">CSS Grid es un poderoso paradigma de diseño para la web.</span><span class="sxs-lookup"><span data-stu-id="5b085-110">CSS Grid is a powerful layout paradigm for the web.</span></span>  <span data-ttu-id="5b085-111">Un excelente lugar para empezar a aprender sobre CSS Grid y las muchas características es la [guía css grid layout][MdnCssGridLayout] en MDN.</span><span class="sxs-lookup"><span data-stu-id="5b085-111">A great place to get started learning about CSS Grid and the many features is the [CSS Grid Layout guide][MdnCssGridLayout] on MDN.</span></span>  

## <a name="discover-css-grids"></a><span data-ttu-id="5b085-112">Detectar cuadrículas CSS</span><span class="sxs-lookup"><span data-stu-id="5b085-112">Discover CSS grids</span></span>  

<span data-ttu-id="5b085-113">Cuando un elemento HTML de la página tiene o se ha aplicado, se muestra un distintivo junto a él `display: grid` `display: inline-grid` en el panel `grid` [Elementos.][DevtoolsGuideChromiumOpen]</span><span class="sxs-lookup"><span data-stu-id="5b085-113">When an HTML element on your page has `display: grid` or `display: inline-grid` applied to it, a `grid` badge is displayed next to it in the [Elements][DevtoolsGuideChromiumOpen] panel.</span></span>  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Descubrir cuadrícula" lightbox="../media/grid-discover-grid.msft.png":::
   <span data-ttu-id="5b085-115">Descubrir cuadrícula</span><span class="sxs-lookup"><span data-stu-id="5b085-115">Discover grid</span></span>  
:::image-end:::  

<span data-ttu-id="5b085-116">Elija el distintivo para alternar la visualización de una superposición de cuadrícula en la página.</span><span class="sxs-lookup"><span data-stu-id="5b085-116">Choose the badge to toggle the display of a grid overlay on the page.</span></span>  <span data-ttu-id="5b085-117">La superposición aparece sobre el elemento, establecida como una cuadrícula para mostrar la posición de las líneas de cuadrícula y las pistas:</span><span class="sxs-lookup"><span data-stu-id="5b085-117">The overlay appears over the element, laid out like a grid to display the position of the grid lines and tracks:</span></span>  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Distintivo de cuadrícula de alternancia" lightbox="../media/grid-highlight-grid.msft.png":::
   <span data-ttu-id="5b085-119">Distintivo de cuadrícula de alternancia</span><span class="sxs-lookup"><span data-stu-id="5b085-119">Toggle grid badge</span></span>  
:::image-end:::  

<span data-ttu-id="5b085-120">Abra el **panel Diseño.**</span><span class="sxs-lookup"><span data-stu-id="5b085-120">Open the **Layout** pane.</span></span>  <span data-ttu-id="5b085-121">Cuando se incluyen cuadrículas en \*\*\*\* una página, el panel Diseño incluye una sección **Cuadrícula** que contiene varias opciones para ver las cuadrículas.</span><span class="sxs-lookup"><span data-stu-id="5b085-121">When grids are included on a page, the **Layout** pane includes a **Grid** section containing a number of options for viewing the grids.</span></span>  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Panel Diseño" lightbox="../media/grid-layout-pane.msft.png":::
   <span data-ttu-id="5b085-123">**Panel Diseño**</span><span class="sxs-lookup"><span data-stu-id="5b085-123">**Layout** pane</span></span>  
:::image-end:::  

<span data-ttu-id="5b085-124">La **sección Cuadrícula** del panel **Diseño** contiene las 2 subsecciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="5b085-124">The **Grid** section in the **Layout** pane contains the following 2 sub-sections.</span></span>  

*   <span data-ttu-id="5b085-125">Configuración de visualización de superposición</span><span class="sxs-lookup"><span data-stu-id="5b085-125">Overlay display settings</span></span>  
*   <span data-ttu-id="5b085-126">Superposiciones de cuadrícula</span><span class="sxs-lookup"><span data-stu-id="5b085-126">Grid overlays</span></span>  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## <a name="overlay-display-settings"></a><span data-ttu-id="5b085-127">Configuración de visualización de superposición</span><span class="sxs-lookup"><span data-stu-id="5b085-127">Overlay display settings</span></span>  

<span data-ttu-id="5b085-128">La **configuración de visualización de superposición** consta de 2 partes siguientes.</span><span class="sxs-lookup"><span data-stu-id="5b085-128">The **Overlay display settings** consists of following 2 parts.</span></span>  

*   <span data-ttu-id="5b085-129">Elija una de las siguientes opciones en el menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="5b085-129">Choose one of the following options from the dropdown menu.</span></span>  
    
    | <span data-ttu-id="5b085-130">Opción Línea</span><span class="sxs-lookup"><span data-stu-id="5b085-130">Line option</span></span> | <span data-ttu-id="5b085-131">Detalles</span><span class="sxs-lookup"><span data-stu-id="5b085-131">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="5b085-132">Ocultar etiquetas de línea</span><span class="sxs-lookup"><span data-stu-id="5b085-132">Hide line labels</span></span>** | <span data-ttu-id="5b085-133">Ocultar las etiquetas de las líneas de cada superposición de cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="5b085-133">Hide the labels of the lines for each grid overlay.</span></span> |  
    | **<span data-ttu-id="5b085-134">Mostrar números de línea</span><span class="sxs-lookup"><span data-stu-id="5b085-134">Show line numbers</span></span>** | <span data-ttu-id="5b085-135">Muestra los números de las líneas de cada superposición de cuadrícula \(seleccionada de forma predeterminada\).</span><span class="sxs-lookup"><span data-stu-id="5b085-135">Display the numbers of the lines for each grid overlay \(selected by default\).</span></span> |  
    | **<span data-ttu-id="5b085-136">Mostrar nombres de línea</span><span class="sxs-lookup"><span data-stu-id="5b085-136">Show line names</span></span>** | <span data-ttu-id="5b085-137">Muestra los nombres de las líneas de cada superposición de cuadrícula cuando se proporcionan nombres.</span><span class="sxs-lookup"><span data-stu-id="5b085-137">Display the names of the lines for each grid overlay when names are provided.</span></span> |  
    
*  <span data-ttu-id="5b085-138">Seleccione la casilla siguiente de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="5b085-138">Choose the checkbox next the following options.</span></span>  
    
    | <span data-ttu-id="5b085-139">Opción</span><span class="sxs-lookup"><span data-stu-id="5b085-139">Option</span></span> | <span data-ttu-id="5b085-140">Detalles</span><span class="sxs-lookup"><span data-stu-id="5b085-140">Details</span></span> |  
    |:--- |:--- |  
    | **<span data-ttu-id="5b085-141">Mostrar tamaños de pista</span><span class="sxs-lookup"><span data-stu-id="5b085-141">Show track sizes</span></span>**  | <span data-ttu-id="5b085-142">Muestra \(u hide\) los tamaños de las pistas.</span><span class="sxs-lookup"><span data-stu-id="5b085-142">Display \(or hide\) the sizes of the tracks.</span></span> |  
    | **<span data-ttu-id="5b085-143">Mostrar nombres de área</span><span class="sxs-lookup"><span data-stu-id="5b085-143">Show area names</span></span>** | <span data-ttu-id="5b085-144">Muestra \(u hide\) los nombres del área, cuando se proporcionan nombres.</span><span class="sxs-lookup"><span data-stu-id="5b085-144">Display \(or hide\) the names of the area, when names are provided.</span></span> |  
    | **<span data-ttu-id="5b085-145">Ampliar líneas de cuadrícula</span><span class="sxs-lookup"><span data-stu-id="5b085-145">Extend grid lines</span></span>** | <span data-ttu-id="5b085-146">Muestra \(u oculta\) las extensiones de las dimensiones de cuadrícula a lo largo de cada eje.</span><span class="sxs-lookup"><span data-stu-id="5b085-146">Displays \(or hides\) the extensions of the grid dimensions along each axis.</span></span>  <span data-ttu-id="5b085-147">De forma predeterminada, las líneas de cuadrícula solo se muestran dentro del elemento con `display: grid` o CSS establecido en `display: inline-grid` él.</span><span class="sxs-lookup"><span data-stu-id="5b085-147">By default, grid lines are only shown inside the element with `display: grid` or `display: inline-grid` CSS set on it.</span></span> |  
    
<span data-ttu-id="5b085-148">En las secciones siguientes se proporcionan detalles para cada una de las **opciones de visualización De superposición.**</span><span class="sxs-lookup"><span data-stu-id="5b085-148">The following sections provide details for each of the **Overlay display settings**.</span></span>  

### <a name="show-line-numbers"></a><span data-ttu-id="5b085-149">Mostrar números de línea</span><span class="sxs-lookup"><span data-stu-id="5b085-149">Show line numbers</span></span>  

<span data-ttu-id="5b085-150">De forma predeterminada, los números de línea positivos y negativos se muestran en la superposición de cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="5b085-150">By default, the positive and negative line numbers are displayed on the grid overlay.</span></span>  

<span data-ttu-id="5b085-151">Para obtener más información acerca de los números negativos en la superposición de cuadrícula, vaya a [Ubicación basada en línea con CSS Grid][MdnLineBasedPlacementCssGrid].</span><span class="sxs-lookup"><span data-stu-id="5b085-151">For more information about negative numbers in the grid overlay, navigate to [Line-based placement with CSS Grid][MdnLineBasedPlacementCssGrid].</span></span>  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Mostrar números de línea" lightbox="../media/grid-show-line-numbers.msft.png":::
   <span data-ttu-id="5b085-153">Mostrar números de línea</span><span class="sxs-lookup"><span data-stu-id="5b085-153">Display line numbers</span></span>  
:::image-end:::  

### <a name="hide-line-labels"></a><span data-ttu-id="5b085-154">Ocultar etiquetas de línea</span><span class="sxs-lookup"><span data-stu-id="5b085-154">Hide line labels</span></span>  

<span data-ttu-id="5b085-155">Elija **Ocultar etiquetas de línea** para ocultar los números de línea.</span><span class="sxs-lookup"><span data-stu-id="5b085-155">Choose **Hide line labels** to hide the line numbers.</span></span>  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Ocultar etiquetas de línea" lightbox="../media/grid-hide-line-labels.msft.png":::
   <span data-ttu-id="5b085-157">Ocultar etiquetas de línea</span><span class="sxs-lookup"><span data-stu-id="5b085-157">Hide line labels</span></span>  
:::image-end:::  

### <a name="show-line-names"></a><span data-ttu-id="5b085-158">Mostrar nombres de línea</span><span class="sxs-lookup"><span data-stu-id="5b085-158">Show line names</span></span>  

<span data-ttu-id="5b085-159">Para obtener más información acerca de los nombres de línea en la superposición de cuadrícula, vaya a [Diseño con líneas de cuadrícula con nombre.][MdnLayoutUsingNamedGridLines]</span><span class="sxs-lookup"><span data-stu-id="5b085-159">For more information about line names in the grid overlay, navigate to [Layout using named grid lines][MdnLayoutUsingNamedGridLines].</span></span>  

<span data-ttu-id="5b085-160">Elija **Mostrar nombres de línea** para ver los nombres de línea en lugar de números.</span><span class="sxs-lookup"><span data-stu-id="5b085-160">Choose **Show line names** to view the line names instead of numbers.</span></span>  <span data-ttu-id="5b085-161">En el ejemplo, 4 líneas tienen nombres: `left` , `middle1` , y `middle2` `right` .</span><span class="sxs-lookup"><span data-stu-id="5b085-161">In the example, 4 lines have names: `left`, `middle1`, `middle2`, and `right`.</span></span>  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Mostrar nombres de línea" lightbox="../media/grid-show-line-names.msft.png":::
   **<span data-ttu-id="5b085-163">Mostrar nombres de línea</span><span class="sxs-lookup"><span data-stu-id="5b085-163">Show line names</span></span>**  
:::image-end:::  

### <a name="show-track-sizes"></a><span data-ttu-id="5b085-164">Mostrar tamaños de pista</span><span class="sxs-lookup"><span data-stu-id="5b085-164">Show track sizes</span></span>  

<span data-ttu-id="5b085-165">Active la casilla **Mostrar tamaños de** pista para ver los tamaños de pista de la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="5b085-165">Enable the **Show track sizes** checkbox to view the track sizes of the grid.</span></span>  

<span data-ttu-id="5b085-166">DevTools muestra `[authored size]` y en cada etiqueta de `[computed size]` línea.</span><span class="sxs-lookup"><span data-stu-id="5b085-166">DevTools displays `[authored size]` and `[computed size]` in each line label.</span></span>  

| <span data-ttu-id="5b085-167">Tamaño</span><span class="sxs-lookup"><span data-stu-id="5b085-167">Size</span></span> | <span data-ttu-id="5b085-168">Detalles</span><span class="sxs-lookup"><span data-stu-id="5b085-168">Details</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="5b085-169">tamaño de autor</span><span class="sxs-lookup"><span data-stu-id="5b085-169">authored size</span></span>** | <span data-ttu-id="5b085-170">El tamaño definido en la hoja de estilos \(omitido si no está definido\).</span><span class="sxs-lookup"><span data-stu-id="5b085-170">The size defined in stylesheet \(omitted if not defined\).</span></span> |  
| **<span data-ttu-id="5b085-171">tamaño calculado</span><span class="sxs-lookup"><span data-stu-id="5b085-171">computed size</span></span>** | <span data-ttu-id="5b085-172">Tamaño real en pantalla.</span><span class="sxs-lookup"><span data-stu-id="5b085-172">The actual size on screen.</span></span> |  

<span data-ttu-id="5b085-173">En la demostración, los tamaños de columna `snack-box` se definen en el `grid-template-columns:1fr 2fr;` CSS.</span><span class="sxs-lookup"><span data-stu-id="5b085-173">In the demo, the `snack-box` column sizes are defined in the `grid-template-columns:1fr 2fr;` CSS.</span></span>  <span data-ttu-id="5b085-174">Por lo tanto, las etiquetas de línea de columna muestran tamaños escritos y calculados.</span><span class="sxs-lookup"><span data-stu-id="5b085-174">Therefore, the column line labels display both authored and computed sizes.</span></span>  

| <span data-ttu-id="5b085-175">Tamaño de la pista</span><span class="sxs-lookup"><span data-stu-id="5b085-175">Track size</span></span> | <span data-ttu-id="5b085-176">Tamaño de creación</span><span class="sxs-lookup"><span data-stu-id="5b085-176">Authored size</span></span> | <span data-ttu-id="5b085-177">Tamaño calculado</span><span class="sxs-lookup"><span data-stu-id="5b085-177">Computed size</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="5b085-178">**1fr** &#x2022; **96,66px**</span><span class="sxs-lookup"><span data-stu-id="5b085-178">**1fr** &#x2022; **96.66px**</span></span> | <span data-ttu-id="5b085-179">1fr</span><span class="sxs-lookup"><span data-stu-id="5b085-179">1fr</span></span> | <span data-ttu-id="5b085-180">96,66 píxeles</span><span class="sxs-lookup"><span data-stu-id="5b085-180">96.66px</span></span> |  
| <span data-ttu-id="5b085-181">**2fr** &#x2022; **193,32px**</span><span class="sxs-lookup"><span data-stu-id="5b085-181">**2fr** &#x2022; **193.32px**</span></span> | <span data-ttu-id="5b085-182">2fr</span><span class="sxs-lookup"><span data-stu-id="5b085-182">2fr</span></span> | <span data-ttu-id="5b085-183">193,32px</span><span class="sxs-lookup"><span data-stu-id="5b085-183">193.32px</span></span> |  

<span data-ttu-id="5b085-184">Las etiquetas de línea de fila solo muestran tamaños calculados, ya que no hay ningún tamaño de fila definido en la hoja de estilos.</span><span class="sxs-lookup"><span data-stu-id="5b085-184">The row line labels display only computed sizes, since there are no row sizes defined in the stylesheet.</span></span>  

| <span data-ttu-id="5b085-185">Tamaño de la pista</span><span class="sxs-lookup"><span data-stu-id="5b085-185">Track size</span></span> | <span data-ttu-id="5b085-186">Tamaño de creación</span><span class="sxs-lookup"><span data-stu-id="5b085-186">Authored size</span></span> | <span data-ttu-id="5b085-187">Tamaño calculado</span><span class="sxs-lookup"><span data-stu-id="5b085-187">Computed size</span></span> |  
|:--- |:--- |:--- |  
| **<span data-ttu-id="5b085-188">80px</span><span class="sxs-lookup"><span data-stu-id="5b085-188">80px</span></span>** | &nbsp;| <span data-ttu-id="5b085-189">80px</span><span class="sxs-lookup"><span data-stu-id="5b085-189">80px</span></span> |  
| **<span data-ttu-id="5b085-190">80px</span><span class="sxs-lookup"><span data-stu-id="5b085-190">80px</span></span>** | &nbsp;| <span data-ttu-id="5b085-191">80px</span><span class="sxs-lookup"><span data-stu-id="5b085-191">80px</span></span> |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Mostrar tamaños de pista" lightbox="../media/grid-show-track-sizes.msft.png":::
   **<span data-ttu-id="5b085-193">Mostrar tamaños de pista</span><span class="sxs-lookup"><span data-stu-id="5b085-193">Show track sizes</span></span>**  
:::image-end:::  

### <a name="show-area-names"></a><span data-ttu-id="5b085-194">Mostrar nombres de área</span><span class="sxs-lookup"><span data-stu-id="5b085-194">Show area names</span></span>  

<span data-ttu-id="5b085-195">Para ver los nombres de área, active la casilla **Mostrar nombres de** área.</span><span class="sxs-lookup"><span data-stu-id="5b085-195">To view the area names, enable the **Show area names** checkbox.</span></span>  <span data-ttu-id="5b085-196">En el ejemplo, hay 3 áreas en la cuadrícula: **superior**, **inferior1** e **inferior2**.</span><span class="sxs-lookup"><span data-stu-id="5b085-196">In the example, there are 3 areas in the grid: **top**, **bottom1** and **bottom2**.</span></span>  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Mostrar nombres de área" lightbox="../media/grid-show-area-names.msft.png":::
   **<span data-ttu-id="5b085-198">Mostrar nombres de área</span><span class="sxs-lookup"><span data-stu-id="5b085-198">Show area names</span></span>**  
:::image-end:::  

### <a name="extend-grid-lines"></a><span data-ttu-id="5b085-199">Ampliar líneas de cuadrícula</span><span class="sxs-lookup"><span data-stu-id="5b085-199">Extend grid lines</span></span>  

<span data-ttu-id="5b085-200">Active la **casilla Extender líneas de cuadrícula** para extender las líneas de cuadrícula al borde de la ventanilla a lo largo de cada eje.</span><span class="sxs-lookup"><span data-stu-id="5b085-200">Enable the **Extend grid lines** checkbox to extend the grid lines to the edge of the viewport along each axis.</span></span>  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Ampliar líneas de cuadrícula" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **<span data-ttu-id="5b085-202">Ampliar líneas de cuadrícula</span><span class="sxs-lookup"><span data-stu-id="5b085-202">Extend grid lines</span></span>**  
:::image-end:::  

## <a name="grid-overlays"></a><span data-ttu-id="5b085-203">Superposiciones de cuadrícula</span><span class="sxs-lookup"><span data-stu-id="5b085-203">Grid overlays</span></span>  

<span data-ttu-id="5b085-204">La **sección Superposiciones de cuadrícula** contiene una lista de cuadrículas que están presentes en la página, cada una con una casilla, junto con varias opciones.</span><span class="sxs-lookup"><span data-stu-id="5b085-204">The **Grid overlays** section contains a list of grids that are present on the page, each with a checkbox, along with various options.</span></span>  

### <a name="enable-overlay-views-of-multiple-grids"></a><span data-ttu-id="5b085-205">Habilitar vistas superpuestas de varias cuadrículas</span><span class="sxs-lookup"><span data-stu-id="5b085-205">Enable overlay views of multiple grids</span></span>  

<span data-ttu-id="5b085-206">Para mostrar la cuadrícula superpuesta para varias cuadrículas, elija la casilla situada junto a cada nombre de la cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="5b085-206">To display the overlay grid for multiple grids, choose the checkbox next to each name of the grid.</span></span>  <span data-ttu-id="5b085-207">En el ejemplo, hay 2 superposiciones de cuadrícula habilitadas que se representan con colores diferentes.</span><span class="sxs-lookup"><span data-stu-id="5b085-207">In the example, there are 2 grid overlays enabled that are each represented with different colors.</span></span>  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Habilitar vistas superpuestas de varias cuadrículas" lightbox="../media/grid-grid-overlays.msft.png":::
   <span data-ttu-id="5b085-209">Habilitar vistas superpuestas de varias cuadrículas</span><span class="sxs-lookup"><span data-stu-id="5b085-209">Enable overlay views of multiple grids</span></span>  
:::image-end:::  

### <a name="customize-the-grid-overlay-color"></a><span data-ttu-id="5b085-210">Personalizar el color de superposición de cuadrícula</span><span class="sxs-lookup"><span data-stu-id="5b085-210">Customize the grid overlay color</span></span>  

<span data-ttu-id="5b085-211">Para abrir el selector de color y personalizar el color de superposición de cuadrícula, elija el cuadro situado junto al nombre de la superposición de cuadrícula.</span><span class="sxs-lookup"><span data-stu-id="5b085-211">To open the color picker and customize the grid overlay color, choose the box next to the name of the grid overlay.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Personalizar el color de superposición de cuadrícula" lightbox="../media/grid-grid-overlays-color.msft.png":::
   <span data-ttu-id="5b085-213">Personalizar el color de superposición de cuadrícula</span><span class="sxs-lookup"><span data-stu-id="5b085-213">Customize the grid overlay color</span></span>  
:::image-end:::  

### <a name="highlight-the-grid"></a><span data-ttu-id="5b085-214">Resaltar la cuadrícula</span><span class="sxs-lookup"><span data-stu-id="5b085-214">Highlight the grid</span></span>  

<span data-ttu-id="5b085-215">Para resaltar el elemento HTML en la herramienta **Elementos** y desplazarse hasta él en la página web, elija el elemento **Mostrar** en el panel Elementos \( Mostrar elemento en el icono del panel Elementos ![ ](../media/show-element-in-element-panel-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="5b085-215">To highlight the HTML element in the **Elements** tool and scroll to it on the webpage, choose the **Show element in the Elements panel** \(![Show element in the Elements panel icon](../media/show-element-in-element-panel-icon.msft.png)\) icon.</span></span>  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Resaltar la cuadrícula" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   <span data-ttu-id="5b085-217">Resaltar la cuadrícula</span><span class="sxs-lookup"><span data-stu-id="5b085-217">Highlight the grid</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="5b085-218">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5b085-218">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "Cuadrícula CSS | jec.fyi"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "Cuadrícula CSS | jec.fyi"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Css Grid Layout | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Diseño con líneas de cuadrícula con nombre | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Colocación basada en línea con css grid | MDN"  

> [!NOTE]
> <span data-ttu-id="5b085-225">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5b085-225">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5b085-226">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/grid) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="5b085-226">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/grid) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5b085-228">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5b085-228">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

---
description: Los usuarios esperan páginas interactivas y suaves.  Cada fase de la canalización de píxeles representa una oportunidad de introducir Jank.  Obtenga más información sobre las herramientas y estrategias para identificar y solucionar problemas comunes que ralentizan el rendimiento del tiempo de ejecución.
title: Analizar el rendimiento en tiempo de ejecución
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: d42ac5e7a7456971d48198a1f362eebe7156bbce
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230610"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <span data-ttu-id="44f11-106">Analizar el rendimiento en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="44f11-106">Analyze runtime performance</span></span> 

<span data-ttu-id="44f11-107">Los usuarios esperan páginas interactivas y suaves.</span><span class="sxs-lookup"><span data-stu-id="44f11-107">Users expects interactive and smooth pages.</span></span>  <span data-ttu-id="44f11-108">Cada fase de la canalización de píxeles representa una oportunidad de introducir Jank.</span><span class="sxs-lookup"><span data-stu-id="44f11-108">Each stage in the pixel pipeline represents an opportunity to introduce jank.</span></span>  <span data-ttu-id="44f11-109">Obtenga más información sobre las herramientas y estrategias para identificar y solucionar problemas comunes que ralentizan el rendimiento del tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="44f11-109">Learn about tools and strategies to identify and fix common problems that slow down runtime performance.</span></span>  

### <span data-ttu-id="44f11-110">Resumen</span><span class="sxs-lookup"><span data-stu-id="44f11-110">Summary</span></span>  

*   <span data-ttu-id="44f11-111">No escriba JavaScript que obligue al explorador a volver a calcular el diseño.</span><span class="sxs-lookup"><span data-stu-id="44f11-111">Do not write JavaScript that forces the browser to recalculate layout.</span></span>  <span data-ttu-id="44f11-112">Funciones de lectura y escritura distintas y realice lecturas en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="44f11-112">Separate read and write functions, and perform reads first.</span></span>  
*   <span data-ttu-id="44f11-113">No complica demasiado tu CSS.</span><span class="sxs-lookup"><span data-stu-id="44f11-113">Do not over-complicate your CSS.</span></span>  <span data-ttu-id="44f11-114">Usa menos CSS y conserva tus selectores de CSS.</span><span class="sxs-lookup"><span data-stu-id="44f11-114">Use less CSS and keep your CSS selectors simple.</span></span>  
*   <span data-ttu-id="44f11-115">Evite el diseño tanto como sea posible.</span><span class="sxs-lookup"><span data-stu-id="44f11-115">Avoid layout as much as possible.</span></span>  <span data-ttu-id="44f11-116">Elija CSS que no desencadene el diseño.</span><span class="sxs-lookup"><span data-stu-id="44f11-116">Choose CSS that does not trigger layout at all.</span></span>  
*   <span data-ttu-id="44f11-117">La pintura puede tardar más tiempo que cualquier otra actividad de representación.</span><span class="sxs-lookup"><span data-stu-id="44f11-117">Painting may take up more time than any other rendering activity.</span></span>  <span data-ttu-id="44f11-118">Mire los cuellos de botella de pintura.</span><span class="sxs-lookup"><span data-stu-id="44f11-118">Watch out for paint bottlenecks.</span></span>  
    
## <span data-ttu-id="44f11-119">JavaScript</span><span class="sxs-lookup"><span data-stu-id="44f11-119">JavaScript</span></span>  

<span data-ttu-id="44f11-120">Los cálculos de JavaScript, especialmente aquellos que desencadenan cambios visuales extensivos, pueden detener el rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="44f11-120">JavaScript calculations, especially ones that trigger extensive visual changes, may stall application performance.</span></span>  <span data-ttu-id="44f11-121">No permita que los JavaScript con tiempos inesperados o de ejecución prolongada interfieran con las interacciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="44f11-121">Do not let badly-timed or long-running JavaScript interfere with user interactions.</span></span>  

### <span data-ttu-id="44f11-122">JavaScript: herramientas</span><span class="sxs-lookup"><span data-stu-id="44f11-122">JavaScript: Tools</span></span>  

<span data-ttu-id="44f11-123">Toma una grabación en el panel **rendimiento** y busca eventos que sean sospechosos `Evaluate Script` .</span><span class="sxs-lookup"><span data-stu-id="44f11-123">Take a recording in the **Performance** panel and look for suspiciously long `Evaluate Script` events.</span></span>  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

<span data-ttu-id="44f11-124">Si recibes bastante Jank en tu código JavaScript, es posible que necesites llevar el análisis al siguiente nivel y recopilar un perfil de CPU de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="44f11-124">f you noticing quite a bit of jank in your JavaScript, you may need to take your analysis to the next level and collect a JavaScript CPU profile.</span></span>  <span data-ttu-id="44f11-125">Los perfiles de CPU muestran dónde se gasta el motor en tiempo de ejecución dentro de las funciones de la página.</span><span class="sxs-lookup"><span data-stu-id="44f11-125">CPU profiles show where runtime is spent within the functions of your page.</span></span>  <span data-ttu-id="44f11-126">Aprenda a crear perfiles de CPU para [acelerar el tiempo de ejecución de JavaScript][DevtoolsRenderingToolsJavascriptRuntime].</span><span class="sxs-lookup"><span data-stu-id="44f11-126">Learn how to create CPU profiles in [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].</span></span>

### <span data-ttu-id="44f11-127">JavaScript: problemas</span><span class="sxs-lookup"><span data-stu-id="44f11-127">JavaScript: Problems</span></span>  

<span data-ttu-id="44f11-128">En la siguiente tabla se describen algunos problemas comunes de JavaScript y posibles soluciones:</span><span class="sxs-lookup"><span data-stu-id="44f11-128">The following table describes some common JavaScript problems and potential solutions:</span></span>  

| <span data-ttu-id="44f11-129">Problema</span><span class="sxs-lookup"><span data-stu-id="44f11-129">Problem</span></span> | <span data-ttu-id="44f11-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="44f11-130">Example</span></span> | <span data-ttu-id="44f11-131">Solución</span><span class="sxs-lookup"><span data-stu-id="44f11-131">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="44f11-132">Controladores de entrada caros que afectan a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="44f11-132">Expensive input handlers affecting response or animation.</span></span>  | <span data-ttu-id="44f11-133">Táctil, desplazamiento de Parallax.</span><span class="sxs-lookup"><span data-stu-id="44f11-133">Touch, parallax scrolling.</span></span>  | <span data-ttu-id="44f11-134">Deje que el explorador controle la entrada táctil y se desplace, o enlace el agente de escucha lo más tarde posible.</span><span class="sxs-lookup"><span data-stu-id="44f11-134">Let the browser handle touch and scrolls, or bind the listener as late as possible.</span></span>  <span data-ttu-id="44f11-135">Consulte [controladores de entrada costosos en la lista de comprobación de rendimiento en tiempo de ejecución de Paul Lewis][WebPerformanceCalendarRuntimeChecklist].</span><span class="sxs-lookup"><span data-stu-id="44f11-135">See [Expensive Input Handlers in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  
| <span data-ttu-id="44f11-136">La respuesta, la animación y la carga de JavaScript es muy incorrecta.</span><span class="sxs-lookup"><span data-stu-id="44f11-136">Badly-timed JavaScript affecting response, animation, load.</span></span>  | <span data-ttu-id="44f11-137">El usuario se desplaza a la derecha después de cargar la página, setTimeout/setInterval.</span><span class="sxs-lookup"><span data-stu-id="44f11-137">User scrolls right after page load, setTimeout / setInterval.</span></span>  | <span data-ttu-id="44f11-138">Optimizar tiempo de ejecución de JavaScript: uso `requestAnimationFrame` , manipulación de Dom de propagación sobre marcos, uso de [trabajadores web][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="44f11-138">Optimize JavaScript runtime: use `requestAnimationFrame`, spread DOM manipulation over frames, use [Web Workers][MDNUsingWebWorkers].</span></span>  |  
| <span data-ttu-id="44f11-139">JavaScript de ejecución prolongada que afecta a la respuesta.</span><span class="sxs-lookup"><span data-stu-id="44f11-139">Long-running JavaScript affecting response.</span></span>  | <span data-ttu-id="44f11-140">El [evento DOMContentLoaded][MDNUsingWebWorkers] se detiene porque está inundado con el trabajo de JS.</span><span class="sxs-lookup"><span data-stu-id="44f11-140">The [DOMContentLoaded event][MDNUsingWebWorkers] stalls as it is swamped with JS work.</span></span>  | <span data-ttu-id="44f11-141">Mover trabajo de cálculo puro a los [trabajadores web][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="44f11-141">Move pure computational work to [Web Workers][MDNUsingWebWorkers].</span></span>  <span data-ttu-id="44f11-142">Si necesita acceso a DOM, use `requestAnimationFrame` .</span><span class="sxs-lookup"><span data-stu-id="44f11-142">If you need DOM access, use `requestAnimationFrame`.</span></span>  <!--See also [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| <span data-ttu-id="44f11-143">Scripts de elementos no utilizados que afectan a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="44f11-143">Garbage-y scripts affecting response or animation.</span></span>  | <span data-ttu-id="44f11-144">La recolección de elementos no utilizados puede producirse en cualquier lugar.</span><span class="sxs-lookup"><span data-stu-id="44f11-144">Garbage collection may happen anywhere.</span></span>  | <span data-ttu-id="44f11-145">Escribir menos scripts y de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="44f11-145">Write less garbage-y scripts.</span></span>  <span data-ttu-id="44f11-146">Consulte recolección [de elementos no utilizados en la animación de la lista de comprobación de rendimiento en tiempo de ejecución de Paul Lewis][WebPerformanceCalendarRuntimeChecklist].</span><span class="sxs-lookup"><span data-stu-id="44f11-146">See [Garbage Collection in Animation in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <span data-ttu-id="44f11-147">Estilo</span><span class="sxs-lookup"><span data-stu-id="44f11-147">Style</span></span>  

<span data-ttu-id="44f11-148">Los cambios de estilo son costosos, especialmente si esos cambios afectan a más de un elemento en el DOM.</span><span class="sxs-lookup"><span data-stu-id="44f11-148">Style changes are costly, especially if those changes affect more than one element in the DOM.</span></span>  <span data-ttu-id="44f11-149">Cada vez que se aplican estilos a un elemento, el explorador determina el impacto en todos los elementos relacionados, vuelve a calcular el diseño y el redibujado.</span><span class="sxs-lookup"><span data-stu-id="44f11-149">Any time you apply styles to an element, the browser figures out the impact on all related elements, recalculates the layout, and repaints.</span></span>  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <span data-ttu-id="44f11-150">Estilo: herramientas</span><span class="sxs-lookup"><span data-stu-id="44f11-150">Style: Tools</span></span>  

<span data-ttu-id="44f11-151">Realizar una grabación en el panel **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="44f11-151">Take a recording in the **Performance** panel.</span></span>  <span data-ttu-id="44f11-152">Compruebe la grabación de `Recalculate Style` eventos grandes \ (mostrada en color púrpura \).</span><span class="sxs-lookup"><span data-stu-id="44f11-152">Check the recording for large `Recalculate Style` events \(displayed in purple\).</span></span>  

<!--todo: add Recording section when available  -->  

<span data-ttu-id="44f11-153">Haga clic en un `Recalculate Style` evento para ver más información sobre él en el panel de **detalles** .</span><span class="sxs-lookup"><span data-stu-id="44f11-153">Click on a `Recalculate Style` event to view more information about it in the **Details** pane.</span></span>  <span data-ttu-id="44f11-154">Si los cambios de estilo están tardando mucho, eso es un impacto en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="44f11-154">If the style changes are taking a long time, that is a performance hit.</span></span>  <span data-ttu-id="44f11-155">Si los cálculos de estilo afectan a un gran número de elementos, se trata de otra área con espacio para mejorarlo.</span><span class="sxs-lookup"><span data-stu-id="44f11-155">If the style calculations are affecting a large number of elements, that is another area with room for improvement.</span></span>  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Recalcular largo estilo" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="44f11-157">Recalcular largo estilo</span><span class="sxs-lookup"><span data-stu-id="44f11-157">Long recalculate style</span></span>  
:::image-end:::  

<span data-ttu-id="44f11-158">Para reducir el impacto de `Recalculate Style` los eventos:</span><span class="sxs-lookup"><span data-stu-id="44f11-158">To reduce the impact of `Recalculate Style` events:</span></span>  

*   <span data-ttu-id="44f11-159">Use los [desencadenadores de CSS][CssTriggers] para saber qué propiedades de CSS desencadenan diseño, pintura y composición.</span><span class="sxs-lookup"><span data-stu-id="44f11-159">Use the [CSS Triggers][CssTriggers] to learn which CSS properties trigger layout, paint, and composite.</span></span>  <span data-ttu-id="44f11-160">Estas propiedades tienen el peor impacto en el rendimiento de la representación.</span><span class="sxs-lookup"><span data-stu-id="44f11-160">These properties have the worst impact on rendering performance.</span></span>  
*   <span data-ttu-id="44f11-161">Cambiar a propiedades que tienen menos impacto.</span><span class="sxs-lookup"><span data-stu-id="44f11-161">Switch to properties that have less impact.</span></span>  <!--See [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties] for more guidance.  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <span data-ttu-id="44f11-162">Estilo: problemas</span><span class="sxs-lookup"><span data-stu-id="44f11-162">Style: Problems</span></span>  

<span data-ttu-id="44f11-163">En la siguiente tabla se describen algunos problemas de estilo comunes y posibles soluciones:</span><span class="sxs-lookup"><span data-stu-id="44f11-163">The following table describes some common style problems and potential solutions:</span></span>  

| <span data-ttu-id="44f11-164">Problema</span><span class="sxs-lookup"><span data-stu-id="44f11-164">Problem</span></span> | <span data-ttu-id="44f11-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="44f11-165">Example</span></span> | <span data-ttu-id="44f11-166">Solución</span><span class="sxs-lookup"><span data-stu-id="44f11-166">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="44f11-167">Cálculos de estilo caros que afectan a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="44f11-167">Expensive style calculations affecting response or animation.</span></span>  | <span data-ttu-id="44f11-168">Cualquier propiedad de CSS que cambie la geometría de un elemento, como el ancho, alto o posición; el explorador comprueba el resto de los elementos y vuelve a calcular el diseño.</span><span class="sxs-lookup"><span data-stu-id="44f11-168">Any CSS property that changes the geometry of an element, like the width, height, or position; the browser checks all other elements and recalculates the layout.</span></span>  | <span data-ttu-id="44f11-169">Evitar CSS que desencadenan diseños</span><span class="sxs-lookup"><span data-stu-id="44f11-169">Avoid CSS that triggers layouts</span></span> |  
| <span data-ttu-id="44f11-170">Selectores complejos que afectan a la respuesta o a la animación.</span><span class="sxs-lookup"><span data-stu-id="44f11-170">Complex selectors affecting response or animation.</span></span>  | <span data-ttu-id="44f11-171">Los selectores anidados obligan al explorador a conocer todo el resto de los elementos, incluidos los elementos primarios y secundarios.</span><span class="sxs-lookup"><span data-stu-id="44f11-171">Nested selectors force the browser to know everything about all the other elements, including parents and children.</span></span>  | <span data-ttu-id="44f11-172">Haga referencia a un elemento de su CSS con solo una clase.</span><span class="sxs-lookup"><span data-stu-id="44f11-172">Reference an element in your CSS with just a class.</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <span data-ttu-id="44f11-173">Diseño</span><span class="sxs-lookup"><span data-stu-id="44f11-173">Layout</span></span>  

<span data-ttu-id="44f11-174">Diseño (o redistribución en Firefox) es el proceso por el cual el explorador calcula las posiciones y los tamaños de todos los elementos de una página.</span><span class="sxs-lookup"><span data-stu-id="44f11-174">Layout (or reflow in Firefox) is the process by which the browser calculates the positions and sizes of all the elements on a page.</span></span>  <span data-ttu-id="44f11-175">El modelo de diseño de la web significa que un elemento puede afectar a otros; por ejemplo, el ancho del `<body>` elemento afecta normalmente a los anchos de los elementos secundarios, y así sucesivamente, todo el recorrido hacia arriba y hacia abajo en el árbol.</span><span class="sxs-lookup"><span data-stu-id="44f11-175">The layout model of the web means that one element may affect others; for example, the width of the `<body>` element typically affects the widths of any child elements, and so on, all the way up and down the tree.</span></span>  <span data-ttu-id="44f11-176">El proceso puede estar bastante implicado para el explorador.</span><span class="sxs-lookup"><span data-stu-id="44f11-176">The process may be quite involved for the browser.</span></span>  

<span data-ttu-id="44f11-177">Como regla general, si solicita un valor geométrico al DOM antes de que se complete un marco, se encontrará con "diseños sincrónicos forzados", que puede ser un gran cuello de botella de rendimiento si se repite con frecuencia o se realiza para un gran árbol de DOM.</span><span class="sxs-lookup"><span data-stu-id="44f11-177">As a general rule of thumb, if you ask for a geometric value back from the DOM before a frame is complete, you are going to find yourself with "forced synchronous layouts", which may be a big performance bottleneck if repeated frequently or performed for a large DOM tree.</span></span>  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <span data-ttu-id="44f11-178">Diseño: herramientas</span><span class="sxs-lookup"><span data-stu-id="44f11-178">Layout: Tools</span></span>  

<span data-ttu-id="44f11-179">El panel **rendimiento** identifica cuando una página provoca diseños sincrónicos forzados.</span><span class="sxs-lookup"><span data-stu-id="44f11-179">The **Performance** pane identifies when a page causes forced synchronous layouts.</span></span>  <span data-ttu-id="44f11-180">Estos `Layout` eventos se marcan con barras rojas.</span><span class="sxs-lookup"><span data-stu-id="44f11-180">These `Layout` events are marked with red bars.</span></span>  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Diseño sincrónico forzado" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="44f11-182">Diseño sincrónico forzado</span><span class="sxs-lookup"><span data-stu-id="44f11-182">Forced synchronous layout</span></span>  
:::image-end:::  

<span data-ttu-id="44f11-183">"La hiperpaginación de diseño" es una repetición de las condiciones de diseño sincrónico forzado.</span><span class="sxs-lookup"><span data-stu-id="44f11-183">"Layout thrashing" is a repetition of forced synchronous layout conditions.</span></span>  <span data-ttu-id="44f11-184">Esto se produce cuando JavaScript escribe y Lee de forma repetida desde el DOM, lo que obliga al explorador a volver a calcular el diseño una y otra vez.</span><span class="sxs-lookup"><span data-stu-id="44f11-184">This occurs when JavaScript writes and reads from the DOM repeatedly, which forces the browser to recalculate the layout over and over.</span></span>  <span data-ttu-id="44f11-185">Para identificar la hiperpaginación de la distribución, busque un patrón de advertencias de diseño sincrónico forzado.</span><span class="sxs-lookup"><span data-stu-id="44f11-185">To identify layout thrashing, look for a pattern of multiple forced synchronous layout warnings.</span></span>  <span data-ttu-id="44f11-186">Vea la ilustración anterior.</span><span class="sxs-lookup"><span data-stu-id="44f11-186">See the previous figure.</span></span>  

### <span data-ttu-id="44f11-187">Diseño: problemas</span><span class="sxs-lookup"><span data-stu-id="44f11-187">Layout: Problems</span></span>  

<span data-ttu-id="44f11-188">En la siguiente tabla se describen algunos problemas de diseño comunes y posibles soluciones:</span><span class="sxs-lookup"><span data-stu-id="44f11-188">The following table describes some common layout problems and potential solutions:</span></span>  

| <span data-ttu-id="44f11-189">Problema</span><span class="sxs-lookup"><span data-stu-id="44f11-189">Problem</span></span> | <span data-ttu-id="44f11-190">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="44f11-190">Example</span></span> | <span data-ttu-id="44f11-191">Solución</span><span class="sxs-lookup"><span data-stu-id="44f11-191">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="44f11-192">Diseño sincrónico forzado que afecta a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="44f11-192">Forced synchronous layout affecting response or animation.</span></span>  | <span data-ttu-id="44f11-193">Obligar al explorador a realizar el diseño anteriormente en la canalización de píxeles, lo que da como resultado pasos repetitivos en el proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="44f11-193">Forcing the browser to perform layout earlier in the pixel pipeline, resulting in repeating steps in the rendering process.</span></span>  | <span data-ttu-id="44f11-194">Por lotes el estilo se lee en primer lugar y luego realiza cualquier escritura.</span><span class="sxs-lookup"><span data-stu-id="44f11-194">Batch your style reads first, then do any writes.</span></span>  <!--See also [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| <span data-ttu-id="44f11-195">La hiperpaginación de diseño afecta a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="44f11-195">Layout thrashing affecting response or animation.</span></span>  | <span data-ttu-id="44f11-196">Un bucle que pone el explorador en un ciclo de lectura y escritura (lectura y escritura), lo que obliga al explorador a volver a calcular la presentación una y otra vez.</span><span class="sxs-lookup"><span data-stu-id="44f11-196">A loop that puts the browser into a read-write-read-write cycle, forcing the browser to recalculate layout over and over again.</span></span>  | <span data-ttu-id="44f11-197">Procesar automáticamente las operaciones de lectura y escritura con la [biblioteca FastDom][GitHubWilsonpageFastdom].</span><span class="sxs-lookup"><span data-stu-id="44f11-197">Automatically batch read-write operations using [FastDom library][GitHubWilsonpageFastdom].</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <span data-ttu-id="44f11-198">Pintura y composición</span><span class="sxs-lookup"><span data-stu-id="44f11-198">Paint and composite</span></span>  

<span data-ttu-id="44f11-199">Paint es el proceso de rellenar píxeles.</span><span class="sxs-lookup"><span data-stu-id="44f11-199">Paint is the process of filling in pixels.</span></span>  <span data-ttu-id="44f11-200">Suele ser la parte más costosa del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="44f11-200">It is often the most costly part of the rendering process.</span></span>  <span data-ttu-id="44f11-201">Si se ha dado cuenta de que la página se Janky de ninguna manera, es posible que tenga problemas de pintura.</span><span class="sxs-lookup"><span data-stu-id="44f11-201">If you noticed that your page is janky in any way, it is likely that you have paint problems.</span></span>  

<span data-ttu-id="44f11-202">La composición es el lugar donde se agrupan las partes pintadas de la página para mostrarse en pantalla.</span><span class="sxs-lookup"><span data-stu-id="44f11-202">Compositing is where the painted parts of the page are put together for displaying on screen.</span></span>  <span data-ttu-id="44f11-203">En su mayor parte, si se fija en las propiedades solo de compositor y se evita que se pinte por completo, debería apreciarse una mejora importante en el rendimiento, pero debe tener cuidado con el recuento excesivo de capas.</span><span class="sxs-lookup"><span data-stu-id="44f11-203">For the most part, if you stick to compositor-only properties and avoid paint altogether, you should see a major improvement in performance, but you need to watch out for excessive layer counts.</span></span>  <!--See also [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <span data-ttu-id="44f11-204">Pintura y composición: herramientas</span><span class="sxs-lookup"><span data-stu-id="44f11-204">Paint and composite: Tools</span></span>  

<span data-ttu-id="44f11-205">¿Quiere saber cuánto tarda el pintado o la frecuencia con la que se produce la pintura?</span><span class="sxs-lookup"><span data-stu-id="44f11-205">Want to know how long painting takes or how often painting occurs?</span></span>  <span data-ttu-id="44f11-206">Active la opción [Habilitar el instrumental de pintura avanzada][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] en el panel **rendimiento** y, después, realice una grabación.</span><span class="sxs-lookup"><span data-stu-id="44f11-206">Check the [Enable advanced paint instrumentation][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] setting in the **Performance** panel and then take a recording.</span></span>  <span data-ttu-id="44f11-207">Si se gasta la mayor parte del tiempo de procesamiento, tiene problemas de pintura.</span><span class="sxs-lookup"><span data-stu-id="44f11-207">If most of your rendering time is spent painting, you have paint problems.</span></span>  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <span data-ttu-id="44f11-208">Pintura y composición: problemas</span><span class="sxs-lookup"><span data-stu-id="44f11-208">Paint and composite: Problems</span></span>  

<span data-ttu-id="44f11-209">En la siguiente tabla se describen algunos problemas comunes de Paint y compuestos y posibles soluciones:</span><span class="sxs-lookup"><span data-stu-id="44f11-209">The following table describes some common paint and composite problems and potential solutions:</span></span>  

| <span data-ttu-id="44f11-210">Problema</span><span class="sxs-lookup"><span data-stu-id="44f11-210">Problem</span></span> | <span data-ttu-id="44f11-211">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="44f11-211">Example</span></span> | <span data-ttu-id="44f11-212">Solución</span><span class="sxs-lookup"><span data-stu-id="44f11-212">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="44f11-213">Las tormentas de pintura afectan a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="44f11-213">Paint storms affecting response or animation.</span></span>  | <span data-ttu-id="44f11-214">Grandes áreas de pintura o pinturas caras que afectan a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="44f11-214">Big paint areas or expensive paints affecting response or animation.</span></span>  | <span data-ttu-id="44f11-215">Evite pintar, promocionar elementos que estén desplazándose a su propia capa, usar transformaciones y opacidad.</span><span class="sxs-lookup"><span data-stu-id="44f11-215">Avoid paint, promote elements that are moving to their own layer, use transforms and opacity.</span></span>  <!--See [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| <span data-ttu-id="44f11-216">Explosiones de capas que afectan a las animaciones.</span><span class="sxs-lookup"><span data-stu-id="44f11-216">Layer explosions affecting animations.</span></span>  | <span data-ttu-id="44f11-217">Exceso de la promoción de demasiados elementos con el rendimiento de la `translateZ(0)` animación.</span><span class="sxs-lookup"><span data-stu-id="44f11-217">Overpromotion of too many elements with `translateZ(0)` greatly affects animation performance.</span></span>  | <span data-ttu-id="44f11-218">Promueve a capas con moderación, y solo cuando sepa que ofrece mejoras tangibles.</span><span class="sxs-lookup"><span data-stu-id="44f11-218">Promote to layers sparingly, and only when you know it offers tangible improvements.</span></span>  <!--See [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## <span data-ttu-id="44f11-219">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="44f11-219">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Acelerar el tiempo de ejecución de JavaScript | Microsoft docs"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#turn-on-advanced-paint-instrumentation "Activar el instrumental de pintura avanzado-referencia para el análisis de rendimiento | Microsoft docs"

<!--[DevtoolsRenderingToolsForcedSynchronousLayouts]: ./rendering-tools/forced-synchronous-layouts.md "Diagnose Forced Synchronous Layouts | Microsoft Docs"  -->  

<!-- The Timeline Tool page is deprecated  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfileJavascript]: ../evaluate-performance/timeline-tool#profile-javascript "Profile JavaScript - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfilePainting]: ../evaluate-performance/timeline-tool#profile-painting "Profile painting - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRecording]: ../evaluate-performance/timeline-tool#make-a-recording "Make a recording - How to Use the Timeline Tool | Microsoft Docs"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRenderingSettings]: ../evaluate-performance/timeline-tool#rendering-settings "Rendering settings - How to Use the Timeline Tool | Microsoft Docs"  -->  

<!--[WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing "Avoid Large, Complex Layouts, and Layout Thrashing"  -->  
<!--[WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime]: /web/fundamentals/performance/rendering/optimize-javascript-execution "Optimize JavaScript Runtime"  -->  
<!--[WebFundamentalsPerformanceRenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations "Reduce the Scope and Complexity of Style Calculations"  -->  
<!--[WebFundamentalsPerformanceRenderingSimplifyPaintComplexity]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas "Simplify Paint Complexity and Reduce Paint Areas"  -->  
<!--[WebFundamentalsPerformanceRenderingCompositorOnlyProperties]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count "Stick to Compositor-Only Properties and Manage Layer Count"  -->  

[CssTriggers]: https://csstriggers.com "Desencadenadores de CSS"  

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Usar los usuarios de Web | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Lista de comprobación de rendimiento en tiempo de ejecución-calendario de rendimiento web"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> <span data-ttu-id="44f11-226">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="44f11-226">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="44f11-227">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \) y [Meggin Kearney][MegginKearney] \ (Tech Writer \).</span><span class="sxs-lookup"><span data-stu-id="44f11-227">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="44f11-229">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="44f11-229">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

---
title: Analizar el rendimiento en tiempo de ejecución
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 7705428dba2ca368eb8f61b13bb96901756b081f
ms.sourcegitcommit: 0342d99bf8d3212068890bab0e1e960afa507c02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611867"
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





# <span data-ttu-id="d0024-103">Analizar el rendimiento en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="d0024-103">Analyze Runtime Performance</span></span>   




<span data-ttu-id="d0024-104">Los usuarios esperan páginas interactivas y suaves.</span><span class="sxs-lookup"><span data-stu-id="d0024-104">Users expects interactive and smooth pages.</span></span>  <span data-ttu-id="d0024-105">Cada fase de la canalización de píxeles representa una oportunidad de introducir Jank.</span><span class="sxs-lookup"><span data-stu-id="d0024-105">Each stage in the pixel pipeline represents an opportunity to introduce jank.</span></span>  <span data-ttu-id="d0024-106">Obtenga más información sobre las herramientas y estrategias para identificar y solucionar problemas comunes que ralentizan el rendimiento del tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d0024-106">Learn about tools and strategies to identify and fix common problems that slow down runtime performance.</span></span>  

### <span data-ttu-id="d0024-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="d0024-107">Summary</span></span>  

*   <span data-ttu-id="d0024-108">No escriba JavaScript que obligue al explorador a volver a calcular el diseño.</span><span class="sxs-lookup"><span data-stu-id="d0024-108">Do not write JavaScript that forces the browser to recalculate layout.</span></span>  <span data-ttu-id="d0024-109">Funciones de lectura y escritura distintas y realice lecturas en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="d0024-109">Separate read and write functions, and perform reads first.</span></span>  
*   <span data-ttu-id="d0024-110">No complica demasiado tu CSS.</span><span class="sxs-lookup"><span data-stu-id="d0024-110">Do not over-complicate your CSS.</span></span>  <span data-ttu-id="d0024-111">Usa menos CSS y conserva tus selectores de CSS.</span><span class="sxs-lookup"><span data-stu-id="d0024-111">Use less CSS and keep your CSS selectors simple.</span></span>  
*   <span data-ttu-id="d0024-112">Evite el diseño tanto como sea posible.</span><span class="sxs-lookup"><span data-stu-id="d0024-112">Avoid layout as much as possible.</span></span>  <span data-ttu-id="d0024-113">Elija CSS que no desencadene el diseño.</span><span class="sxs-lookup"><span data-stu-id="d0024-113">Choose CSS that does not trigger layout at all.</span></span>  
*   <span data-ttu-id="d0024-114">La pintura puede tardar más tiempo que cualquier otra actividad de representación.</span><span class="sxs-lookup"><span data-stu-id="d0024-114">Painting may take up more time than any other rendering activity.</span></span>  <span data-ttu-id="d0024-115">Mire los cuellos de botella de pintura.</span><span class="sxs-lookup"><span data-stu-id="d0024-115">Watch out for paint bottlenecks.</span></span>  

## <span data-ttu-id="d0024-116">JavaScript</span><span class="sxs-lookup"><span data-stu-id="d0024-116">JavaScript</span></span>  

<span data-ttu-id="d0024-117">Los cálculos de JavaScript, especialmente aquellos que desencadenan cambios visuales extensivos, pueden detener el rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d0024-117">JavaScript calculations, especially ones that trigger extensive visual changes, may stall application performance.</span></span>  <span data-ttu-id="d0024-118">No permita que los JavaScript con tiempos inesperados o de ejecución prolongada interfieran con las interacciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="d0024-118">Do not let badly-timed or long-running JavaScript interfere with user interactions.</span></span>  

### <span data-ttu-id="d0024-119">JavaScript: herramientas</span><span class="sxs-lookup"><span data-stu-id="d0024-119">JavaScript: Tools</span></span>  

<span data-ttu-id="d0024-120">Toma una grabación en el panel **rendimiento** y busca eventos que sean sospechosos `Evaluate Script` .</span><span class="sxs-lookup"><span data-stu-id="d0024-120">Take a recording in the **Performance** panel and look for suspiciously long `Evaluate Script` events.</span></span>  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

<span data-ttu-id="d0024-121">Si recibes bastante Jank en tu código JavaScript, es posible que necesites llevar el análisis al siguiente nivel y recopilar un perfil de CPU de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d0024-121">f you noticing quite a bit of jank in your JavaScript, you may need to take your analysis to the next level and collect a JavaScript CPU profile.</span></span>  <span data-ttu-id="d0024-122">Los perfiles de CPU muestran dónde se gasta el motor en tiempo de ejecución dentro de las funciones de la página.</span><span class="sxs-lookup"><span data-stu-id="d0024-122">CPU profiles show where runtime is spent within the functions of your page.</span></span>  <span data-ttu-id="d0024-123">Aprenda a crear perfiles de CPU para [acelerar el tiempo de ejecución de JavaScript][DevtoolsRenderingToolsJavascriptRuntime].</span><span class="sxs-lookup"><span data-stu-id="d0024-123">Learn how to create CPU profiles in [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].</span></span>

### <span data-ttu-id="d0024-124">JavaScript: problemas</span><span class="sxs-lookup"><span data-stu-id="d0024-124">JavaScript: Problems</span></span>  

<span data-ttu-id="d0024-125">En la siguiente tabla se describen algunos problemas comunes de JavaScript y posibles soluciones:</span><span class="sxs-lookup"><span data-stu-id="d0024-125">The following table describes some common JavaScript problems and potential solutions:</span></span>  

| <span data-ttu-id="d0024-126">Problema</span><span class="sxs-lookup"><span data-stu-id="d0024-126">Problem</span></span> | <span data-ttu-id="d0024-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0024-127">Example</span></span> | <span data-ttu-id="d0024-128">Solución</span><span class="sxs-lookup"><span data-stu-id="d0024-128">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="d0024-129">Controladores de entrada caros que afectan a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="d0024-129">Expensive input handlers affecting response or animation.</span></span>  | <span data-ttu-id="d0024-130">Táctil, desplazamiento de Parallax.</span><span class="sxs-lookup"><span data-stu-id="d0024-130">Touch, parallax scrolling.</span></span>  | <span data-ttu-id="d0024-131">Deje que el explorador controle la entrada táctil y se desplace, o enlace el agente de escucha lo más tarde posible.</span><span class="sxs-lookup"><span data-stu-id="d0024-131">Let the browser handle touch and scrolls, or bind the listener as late as possible.</span></span>  <span data-ttu-id="d0024-132">Consulte [controladores de entrada costosos en la lista de comprobación de rendimiento en tiempo de ejecución de Paul Lewis][WebPerformanceCalendarRuntimeChecklist].</span><span class="sxs-lookup"><span data-stu-id="d0024-132">See [Expensive Input Handlers in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  
| <span data-ttu-id="d0024-133">La respuesta, la animación y la carga de JavaScript es muy incorrecta.</span><span class="sxs-lookup"><span data-stu-id="d0024-133">Badly-timed JavaScript affecting response, animation, load.</span></span>  | <span data-ttu-id="d0024-134">El usuario se desplaza a la derecha después de cargar la página, setTimeout/setInterval.</span><span class="sxs-lookup"><span data-stu-id="d0024-134">User scrolls right after page load, setTimeout / setInterval.</span></span>  | <span data-ttu-id="d0024-135">Optimizar tiempo de ejecución de JavaScript: uso `requestAnimationFrame` , manipulación de Dom de propagación sobre marcos, uso de [trabajadores web][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="d0024-135">Optimize JavaScript runtime: use `requestAnimationFrame`, spread DOM manipulation over frames, use [Web Workers][MDNUsingWebWorkers].</span></span>  |  
| <span data-ttu-id="d0024-136">JavaScript de ejecución prolongada que afecta a la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0024-136">Long-running JavaScript affecting response.</span></span>  | <span data-ttu-id="d0024-137">El [evento DOMContentLoaded][MDNUsingWebWorkers] se detiene porque está inundado con el trabajo de JS.</span><span class="sxs-lookup"><span data-stu-id="d0024-137">The [DOMContentLoaded event][MDNUsingWebWorkers] stalls as it is swamped with JS work.</span></span>  | <span data-ttu-id="d0024-138">Mover trabajo de cálculo puro a los [trabajadores web][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="d0024-138">Move pure computational work to [Web Workers][MDNUsingWebWorkers].</span></span>  <span data-ttu-id="d0024-139">Si necesita acceso a DOM, use `requestAnimationFrame` .</span><span class="sxs-lookup"><span data-stu-id="d0024-139">If you need DOM access, use `requestAnimationFrame`.</span></span>  <!--See also [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| <span data-ttu-id="d0024-140">Scripts de elementos no utilizados que afectan a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="d0024-140">Garbage-y scripts affecting response or animation.</span></span>  | <span data-ttu-id="d0024-141">La recolección de elementos no utilizados puede producirse en cualquier lugar.</span><span class="sxs-lookup"><span data-stu-id="d0024-141">Garbage collection may happen anywhere.</span></span>  | <span data-ttu-id="d0024-142">Escribir menos scripts y de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="d0024-142">Write less garbage-y scripts.</span></span>  <span data-ttu-id="d0024-143">Consulte recolección [de elementos no utilizados en la animación de la lista de comprobación de rendimiento en tiempo de ejecución de Paul Lewis][WebPerformanceCalendarRuntimeChecklist].</span><span class="sxs-lookup"><span data-stu-id="d0024-143">See [Garbage Collection in Animation in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <span data-ttu-id="d0024-144">Estilo</span><span class="sxs-lookup"><span data-stu-id="d0024-144">Style</span></span>  

<span data-ttu-id="d0024-145">Los cambios de estilo son costosos, especialmente si esos cambios afectan a más de un elemento en el DOM.</span><span class="sxs-lookup"><span data-stu-id="d0024-145">Style changes are costly, especially if those changes affect more than one element in the DOM.</span></span>  <span data-ttu-id="d0024-146">Cada vez que se aplican estilos a un elemento, el explorador determina el impacto en todos los elementos relacionados, vuelve a calcular el diseño y el redibujado.</span><span class="sxs-lookup"><span data-stu-id="d0024-146">Any time you apply styles to an element, the browser figures out the impact on all related elements, recalculates the layout, and repaints.</span></span>  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <span data-ttu-id="d0024-147">Estilo: herramientas</span><span class="sxs-lookup"><span data-stu-id="d0024-147">Style: Tools</span></span>  

<span data-ttu-id="d0024-148">Realizar una grabación en el panel **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="d0024-148">Take a recording in the **Performance** panel.</span></span>  <span data-ttu-id="d0024-149">Compruebe la grabación de `Recalculate Style` eventos grandes \ (mostrada en color púrpura \).</span><span class="sxs-lookup"><span data-stu-id="d0024-149">Check the recording for large `Recalculate Style` events \(displayed in purple\).</span></span>  

<!--todo: add Recording section when available  -->  

<span data-ttu-id="d0024-150">Haga clic en un `Recalculate Style` evento para ver más información sobre él en el panel de **detalles** .</span><span class="sxs-lookup"><span data-stu-id="d0024-150">Click on a `Recalculate Style` event to view more information about it in the **Details** pane.</span></span>  <span data-ttu-id="d0024-151">Si los cambios de estilo están tardando mucho, eso es un impacto en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d0024-151">If the style changes are taking a long time, that is a performance hit.</span></span>  <span data-ttu-id="d0024-152">Si los cálculos de estilo afectan a un gran número de elementos, se trata de otra área con espacio para mejorarlo.</span><span class="sxs-lookup"><span data-stu-id="d0024-152">If the style calculations are affecting a large number of elements, that is another area with room for improvement.</span></span>  

> ##### <span data-ttu-id="d0024-153">Figura 1</span><span class="sxs-lookup"><span data-stu-id="d0024-153">Figure 1</span></span>  
> <span data-ttu-id="d0024-154">Recalcular largo estilo</span><span class="sxs-lookup"><span data-stu-id="d0024-154">Long recalculate style</span></span>  
> ![Recalcular largo estilo][ImageLongRecalculateStyle]

<span data-ttu-id="d0024-156">Para reducir el impacto de `Recalculate Style` los eventos:</span><span class="sxs-lookup"><span data-stu-id="d0024-156">To reduce the impact of `Recalculate Style` events:</span></span>  

*   <span data-ttu-id="d0024-157">Use los [desencadenadores de CSS][CssTriggers] para saber qué propiedades de CSS desencadenan diseño, pintura y composición.</span><span class="sxs-lookup"><span data-stu-id="d0024-157">Use the [CSS Triggers][CssTriggers] to learn which CSS properties trigger layout, paint, and composite.</span></span>  <span data-ttu-id="d0024-158">Estas propiedades tienen el peor impacto en el rendimiento de la representación.</span><span class="sxs-lookup"><span data-stu-id="d0024-158">These properties have the worst impact on rendering performance.</span></span>  
*   <span data-ttu-id="d0024-159">Cambiar a propiedades que tienen menos impacto.</span><span class="sxs-lookup"><span data-stu-id="d0024-159">Switch to properties that have less impact.</span></span>  <!--See [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties] for more guidance.  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <span data-ttu-id="d0024-160">Estilo: problemas</span><span class="sxs-lookup"><span data-stu-id="d0024-160">Style: Problems</span></span>  

<span data-ttu-id="d0024-161">En la siguiente tabla se describen algunos problemas de estilo comunes y posibles soluciones:</span><span class="sxs-lookup"><span data-stu-id="d0024-161">The following table describes some common style problems and potential solutions:</span></span>  

| <span data-ttu-id="d0024-162">Problema</span><span class="sxs-lookup"><span data-stu-id="d0024-162">Problem</span></span> | <span data-ttu-id="d0024-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0024-163">Example</span></span> | <span data-ttu-id="d0024-164">Solución</span><span class="sxs-lookup"><span data-stu-id="d0024-164">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="d0024-165">Cálculos de estilo caros que afectan a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="d0024-165">Expensive style calculations affecting response or animation.</span></span>  | <span data-ttu-id="d0024-166">Cualquier propiedad de CSS que cambie la geometría de un elemento, como el ancho, alto o posición; el explorador comprueba el resto de los elementos y vuelve a calcular el diseño.</span><span class="sxs-lookup"><span data-stu-id="d0024-166">Any CSS property that changes the geometry of an element, like the width, height, or position; the browser checks all other elements and recalculates the layout.</span></span>  | <span data-ttu-id="d0024-167">Evitar CSS que desencadenan diseños</span><span class="sxs-lookup"><span data-stu-id="d0024-167">Avoid CSS that triggers layouts</span></span> |  
| <span data-ttu-id="d0024-168">Selectores complejos que afectan a la respuesta o a la animación.</span><span class="sxs-lookup"><span data-stu-id="d0024-168">Complex selectors affecting response or animation.</span></span>  | <span data-ttu-id="d0024-169">Los selectores anidados obligan al explorador a conocer todo el resto de los elementos, incluidos los elementos primarios y secundarios.</span><span class="sxs-lookup"><span data-stu-id="d0024-169">Nested selectors force the browser to know everything about all the other elements, including parents and children.</span></span>  | <span data-ttu-id="d0024-170">Haga referencia a un elemento de su CSS con solo una clase.</span><span class="sxs-lookup"><span data-stu-id="d0024-170">Reference an element in your CSS with just a class.</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <span data-ttu-id="d0024-171">Diseño</span><span class="sxs-lookup"><span data-stu-id="d0024-171">Layout</span></span>  

<span data-ttu-id="d0024-172">Diseño (o redistribución en Firefox) es el proceso por el cual el explorador calcula las posiciones y los tamaños de todos los elementos de una página.</span><span class="sxs-lookup"><span data-stu-id="d0024-172">Layout (or reflow in Firefox) is the process by which the browser calculates the positions and sizes of all the elements on a page.</span></span>  <span data-ttu-id="d0024-173">El modelo de diseño de la web significa que un elemento puede afectar a otros; por ejemplo, el ancho del `<body>` elemento afecta normalmente a los anchos de los elementos secundarios, y así sucesivamente, todo el recorrido hacia arriba y hacia abajo en el árbol.</span><span class="sxs-lookup"><span data-stu-id="d0024-173">The layout model of the web means that one element may affect others; for example, the width of the `<body>` element typically affects the widths of any child elements, and so on, all the way up and down the tree.</span></span>  <span data-ttu-id="d0024-174">El proceso puede estar bastante implicado para el explorador.</span><span class="sxs-lookup"><span data-stu-id="d0024-174">The process may be quite involved for the browser.</span></span>  

<span data-ttu-id="d0024-175">Como regla general, si solicita un valor geométrico al DOM antes de que se complete un marco, se encontrará con "diseños sincrónicos forzados", que puede ser un gran cuello de botella de rendimiento si se repite con frecuencia o se realiza para un gran árbol de DOM.</span><span class="sxs-lookup"><span data-stu-id="d0024-175">As a general rule of thumb, if you ask for a geometric value back from the DOM before a frame is complete, you are going to find yourself with "forced synchronous layouts", which may be a big performance bottleneck if repeated frequently or performed for a large DOM tree.</span></span>  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <span data-ttu-id="d0024-176">Diseño: herramientas</span><span class="sxs-lookup"><span data-stu-id="d0024-176">Layout: Tools</span></span>  

<span data-ttu-id="d0024-177">El panel **rendimiento** identifica cuando una página provoca diseños sincrónicos forzados.</span><span class="sxs-lookup"><span data-stu-id="d0024-177">The **Performance** pane identifies when a page causes forced synchronous layouts.</span></span>  <span data-ttu-id="d0024-178">Estos `Layout` eventos se marcan con barras rojas.</span><span class="sxs-lookup"><span data-stu-id="d0024-178">These `Layout` events are marked with red bars.</span></span>  

> ##### <span data-ttu-id="d0024-179">Figura 2</span><span class="sxs-lookup"><span data-stu-id="d0024-179">Figure 2</span></span>  
> <span data-ttu-id="d0024-180">Diseño sincrónico forzado</span><span class="sxs-lookup"><span data-stu-id="d0024-180">Forced synchronous layout</span></span>  
> ![Diseño sincrónico forzado][ImageForcedSynchronousLayout]  

<span data-ttu-id="d0024-182">"La hiperpaginación de diseño" es una repetición de las condiciones de diseño sincrónico forzado.</span><span class="sxs-lookup"><span data-stu-id="d0024-182">"Layout thrashing" is a repetition of forced synchronous layout conditions.</span></span>  <span data-ttu-id="d0024-183">Esto se produce cuando JavaScript escribe y Lee de forma repetida desde el DOM, lo que obliga al explorador a volver a calcular el diseño una y otra vez.</span><span class="sxs-lookup"><span data-stu-id="d0024-183">This occurs when JavaScript writes and reads from the DOM repeatedly, which forces the browser to recalculate the layout over and over.</span></span>  <span data-ttu-id="d0024-184">Para identificar la hiperpaginación de la distribución, busque un patrón de advertencias de diseño sincrónico forzado.</span><span class="sxs-lookup"><span data-stu-id="d0024-184">To identify layout thrashing, look for a pattern of multiple forced synchronous layout warnings.</span></span>  <span data-ttu-id="d0024-185">Consulte la [ilustración 2](#figure-2).</span><span class="sxs-lookup"><span data-stu-id="d0024-185">See [Figure 2](#figure-2).</span></span>  

### <span data-ttu-id="d0024-186">Diseño: problemas</span><span class="sxs-lookup"><span data-stu-id="d0024-186">Layout: Problems</span></span>  

<span data-ttu-id="d0024-187">En la siguiente tabla se describen algunos problemas de diseño comunes y posibles soluciones:</span><span class="sxs-lookup"><span data-stu-id="d0024-187">The following table describes some common layout problems and potential solutions:</span></span>  

| <span data-ttu-id="d0024-188">Problema</span><span class="sxs-lookup"><span data-stu-id="d0024-188">Problem</span></span> | <span data-ttu-id="d0024-189">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0024-189">Example</span></span> | <span data-ttu-id="d0024-190">Solución</span><span class="sxs-lookup"><span data-stu-id="d0024-190">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="d0024-191">Diseño sincrónico forzado que afecta a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="d0024-191">Forced synchronous layout affecting response or animation.</span></span>  | <span data-ttu-id="d0024-192">Obligar al explorador a realizar el diseño anteriormente en la canalización de píxeles, lo que da como resultado pasos repetitivos en el proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="d0024-192">Forcing the browser to perform layout earlier in the pixel pipeline, resulting in repeating steps in the rendering process.</span></span>  | <span data-ttu-id="d0024-193">Por lotes el estilo se lee en primer lugar y luego realiza cualquier escritura.</span><span class="sxs-lookup"><span data-stu-id="d0024-193">Batch your style reads first, then do any writes.</span></span>  <!--See also [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| <span data-ttu-id="d0024-194">La hiperpaginación de diseño afecta a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="d0024-194">Layout thrashing affecting response or animation.</span></span>  | <span data-ttu-id="d0024-195">Un bucle que pone el explorador en un ciclo de lectura y escritura (lectura y escritura), lo que obliga al explorador a volver a calcular la presentación una y otra vez.</span><span class="sxs-lookup"><span data-stu-id="d0024-195">A loop that puts the browser into a read-write-read-write cycle, forcing the browser to recalculate layout over and over again.</span></span>  | <span data-ttu-id="d0024-196">Procesar automáticamente las operaciones de lectura y escritura con la [biblioteca FastDom][GitHubWilsonpageFastdom].</span><span class="sxs-lookup"><span data-stu-id="d0024-196">Automatically batch read-write operations using [FastDom library][GitHubWilsonpageFastdom].</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <span data-ttu-id="d0024-197">Pintura y composición</span><span class="sxs-lookup"><span data-stu-id="d0024-197">Paint and composite</span></span>  

<span data-ttu-id="d0024-198">Paint es el proceso de rellenar píxeles.</span><span class="sxs-lookup"><span data-stu-id="d0024-198">Paint is the process of filling in pixels.</span></span>  <span data-ttu-id="d0024-199">Suele ser la parte más costosa del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="d0024-199">It is often the most costly part of the rendering process.</span></span>  <span data-ttu-id="d0024-200">Si se ha dado cuenta de que la página se Janky de ninguna manera, es posible que tenga problemas de pintura.</span><span class="sxs-lookup"><span data-stu-id="d0024-200">If you noticed that your page is janky in any way, it is likely that you have paint problems.</span></span>  

<span data-ttu-id="d0024-201">La composición es el lugar donde se agrupan las partes pintadas de la página para mostrarse en pantalla.</span><span class="sxs-lookup"><span data-stu-id="d0024-201">Compositing is where the painted parts of the page are put together for displaying on screen.</span></span>  <span data-ttu-id="d0024-202">En su mayor parte, si se fija en las propiedades solo de compositor y se evita que se pinte por completo, debería apreciarse una mejora importante en el rendimiento, pero debe tener cuidado con el recuento excesivo de capas.</span><span class="sxs-lookup"><span data-stu-id="d0024-202">For the most part, if you stick to compositor-only properties and avoid paint altogether, you should see a major improvement in performance, but you need to watch out for excessive layer counts.</span></span>  <!--See also [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <span data-ttu-id="d0024-203">Pintura y composición: herramientas</span><span class="sxs-lookup"><span data-stu-id="d0024-203">Paint and composite: Tools</span></span>  

<span data-ttu-id="d0024-204">¿Quiere saber cuánto tarda el pintado o la frecuencia con la que se produce la pintura?</span><span class="sxs-lookup"><span data-stu-id="d0024-204">Want to know how long painting takes or how often painting occurs?</span></span>  <span data-ttu-id="d0024-205">Active la opción [Habilitar el instrumental de pintura avanzada][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] en el panel **rendimiento** y, después, realice una grabación.</span><span class="sxs-lookup"><span data-stu-id="d0024-205">Check the [Enable advanced paint instrumentation][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] setting in the **Performance** panel and then take a recording.</span></span>  <span data-ttu-id="d0024-206">Si se gasta la mayor parte del tiempo de procesamiento, tiene problemas de pintura.</span><span class="sxs-lookup"><span data-stu-id="d0024-206">If most of your rendering time is spent painting, you have paint problems.</span></span>  

<!--
> ##### Old Figure 3  
> Long paint times in timeline recording  
> ![Long paint times in timeline recording][ImageLongPaintTimes]  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <span data-ttu-id="d0024-207">Pintura y composición: problemas</span><span class="sxs-lookup"><span data-stu-id="d0024-207">Paint and composite: Problems</span></span>  

<span data-ttu-id="d0024-208">En la siguiente tabla se describen algunos problemas comunes de Paint y compuestos y posibles soluciones:</span><span class="sxs-lookup"><span data-stu-id="d0024-208">The following table describes some common paint and composite problems and potential solutions:</span></span>  

| <span data-ttu-id="d0024-209">Problema</span><span class="sxs-lookup"><span data-stu-id="d0024-209">Problem</span></span> | <span data-ttu-id="d0024-210">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0024-210">Example</span></span> | <span data-ttu-id="d0024-211">Solución</span><span class="sxs-lookup"><span data-stu-id="d0024-211">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="d0024-212">Las tormentas de pintura afectan a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="d0024-212">Paint storms affecting response or animation.</span></span>  | <span data-ttu-id="d0024-213">Grandes áreas de pintura o pinturas caras que afectan a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="d0024-213">Big paint areas or expensive paints affecting response or animation.</span></span>  | <span data-ttu-id="d0024-214">Evite pintar, promocionar elementos que estén desplazándose a su propia capa, usar transformaciones y opacidad.</span><span class="sxs-lookup"><span data-stu-id="d0024-214">Avoid paint, promote elements that are moving to their own layer, use transforms and opacity.</span></span>  <!--See [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| <span data-ttu-id="d0024-215">Explosiones de capas que afectan a las animaciones.</span><span class="sxs-lookup"><span data-stu-id="d0024-215">Layer explosions affecting animations.</span></span>  | <span data-ttu-id="d0024-216">Exceso de la promoción de demasiados elementos con el rendimiento de la `translateZ(0)` animación.</span><span class="sxs-lookup"><span data-stu-id="d0024-216">Overpromotion of too many elements with `translateZ(0)` greatly affects animation performance.</span></span>  | <span data-ttu-id="d0024-217">Promueve a capas con moderación, y solo cuando sepa que ofrece mejoras tangibles.</span><span class="sxs-lookup"><span data-stu-id="d0024-217">Promote to layers sparingly, and only when you know it offers tangible improvements.</span></span>  <!--See [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

<!--## Feedback   -->  



<!-- image links -->  

[ImageLongRecalculateStyle]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-performance-recalculate-style-summary.msft.png "Ilustración 1: estilo Long recalculate"  
[ImageForcedSynchronousLayout]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-jank-performance-recalculate-style-summary.msft.png "Ilustración 2: diseño sincrónico forzado"  
<!--[ImageLongPaintTimes]: /microsoft-edge/devtools-guide-chromium/media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png "Old Figure 3: Long paint times in timeline recording"  -->  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Acelerar el tiempo de ejecución de JavaScript"  

[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#enable-advanced-paint-instrumentation "Habilitar el instrumental de pintura avanzado-referencia de análisis de rendimiento"

<!--[DevtoolsRenderingToolsForcedSynchronousLayouts]: /microsoft-edge/devtools-guide-chromium/rendering-tools/forced-synchronous-layouts "Diagnose Forced Synchronous Layouts"  -->  

<!-- The Timeline Tool page is deprecated  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfileJavascript]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/timeline-tool#profile-javascript "Profile JavaScript - How to Use the Timeline Tool"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolProfilePainting]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/timeline-tool#profile-painting "Profile painting - How to Use the Timeline Tool"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRecording]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/timeline-tool#make-a-recording "Make a recording - How to Use the Timeline Tool"  -->  
<!--[DevtoolsEvaluatePerformanceTimelineToolRenderingSettings]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/timeline-tool#rendering-settings "Rendering settings - How to Use the Timeline Tool"  -->  

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
> <span data-ttu-id="d0024-226">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d0024-226">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d0024-227">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \) y [Meggin Kearney][MegginKearney] \ (Tech Writer \).</span><span class="sxs-lookup"><span data-stu-id="d0024-227">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d0024-229">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d0024-229">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

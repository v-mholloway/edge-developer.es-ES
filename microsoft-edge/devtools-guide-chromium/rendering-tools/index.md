---
description: Los usuarios esperan páginas interactivas y suaves.  Cada fase de la canalización de píxeles representa una oportunidad para introducir jank.  Obtenga información sobre herramientas y estrategias para identificar y corregir problemas comunes que ralentizan el rendimiento en tiempo de ejecución.
title: Analizar el rendimiento en tiempo de ejecución
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: d5c37c188ae9038a7baafc936d2a02299def6366
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564710"
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
# <a name="analyze-runtime-performance"></a><span data-ttu-id="7619b-106">Analizar el rendimiento en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="7619b-106">Analyze runtime performance</span></span>  

<span data-ttu-id="7619b-107">Los usuarios esperan páginas interactivas y suaves.</span><span class="sxs-lookup"><span data-stu-id="7619b-107">Users expects interactive and smooth pages.</span></span>  <span data-ttu-id="7619b-108">Cada fase de la canalización de píxeles representa una oportunidad para introducir jank.</span><span class="sxs-lookup"><span data-stu-id="7619b-108">Each stage in the pixel pipeline represents an opportunity to introduce jank.</span></span>  <span data-ttu-id="7619b-109">Obtenga información sobre herramientas y estrategias para identificar y corregir problemas comunes que ralentizan el rendimiento en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="7619b-109">Learn about tools and strategies to identify and fix common problems that slow down runtime performance.</span></span>  

### <a name="summary"></a><span data-ttu-id="7619b-110">Resumen</span><span class="sxs-lookup"><span data-stu-id="7619b-110">Summary</span></span>  

*   <span data-ttu-id="7619b-111">No escriba JavaScript que fuerza al explorador a volver a calcular el diseño.</span><span class="sxs-lookup"><span data-stu-id="7619b-111">Do not write JavaScript that forces the browser to recalculate layout.</span></span>  <span data-ttu-id="7619b-112">Separe las funciones de lectura y escritura y realice primero lecturas.</span><span class="sxs-lookup"><span data-stu-id="7619b-112">Separate read and write functions, and perform reads first.</span></span>  
*   <span data-ttu-id="7619b-113">No complique en exceso su CSS.</span><span class="sxs-lookup"><span data-stu-id="7619b-113">Do not over-complicate your CSS.</span></span>  <span data-ttu-id="7619b-114">Use menos CSS y mantenga los selectores CSS sencillos.</span><span class="sxs-lookup"><span data-stu-id="7619b-114">Use less CSS and keep your CSS selectors simple.</span></span>  
*   <span data-ttu-id="7619b-115">Evite el diseño tanto como sea posible.</span><span class="sxs-lookup"><span data-stu-id="7619b-115">Avoid layout as much as possible.</span></span>  <span data-ttu-id="7619b-116">Elija CSS que no desencadene el diseño en absoluto.</span><span class="sxs-lookup"><span data-stu-id="7619b-116">Choose CSS that does not trigger layout at all.</span></span>  
*   <span data-ttu-id="7619b-117">La pintura puede tardar más tiempo que cualquier otra actividad de representación.</span><span class="sxs-lookup"><span data-stu-id="7619b-117">Painting may take up more time than any other rendering activity.</span></span>  <span data-ttu-id="7619b-118">Cuidado con los cuellos de botella de pintura.</span><span class="sxs-lookup"><span data-stu-id="7619b-118">Watch out for paint bottlenecks.</span></span>  
    
## <a name="javascript"></a><span data-ttu-id="7619b-119">JavaScript</span><span class="sxs-lookup"><span data-stu-id="7619b-119">JavaScript</span></span>  

<span data-ttu-id="7619b-120">Los cálculos de JavaScript, especialmente los que desencadenan grandes cambios visuales, pueden detener el rendimiento de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="7619b-120">JavaScript calculations, especially ones that trigger extensive visual changes, may stall application performance.</span></span>  <span data-ttu-id="7619b-121">No permita que JavaScript con un tiempo mal definido o de ejecución larga interfiera con las interacciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="7619b-121">Do not let badly-timed or long-running JavaScript interfere with user interactions.</span></span>  

### <a name="javascript-tools"></a><span data-ttu-id="7619b-122">JavaScript: herramientas</span><span class="sxs-lookup"><span data-stu-id="7619b-122">JavaScript: Tools</span></span>  

<span data-ttu-id="7619b-123">Haga una grabación en la **herramienta Rendimiento** y busque eventos sospechosamente `Evaluate Script` largos.</span><span class="sxs-lookup"><span data-stu-id="7619b-123">Take a recording in the **Performance** tool and look for suspiciously long `Evaluate Script` events.</span></span>  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

<span data-ttu-id="7619b-124">si nota un poco de jank en JavaScript, es posible que deba llevar el análisis al siguiente nivel y recopilar un perfil de CPU de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7619b-124">f you noticing quite a bit of jank in your JavaScript, you may need to take your analysis to the next level and collect a JavaScript CPU profile.</span></span>  <span data-ttu-id="7619b-125">Los perfiles de CPU muestran dónde se usa el tiempo de ejecución dentro de las funciones de la página.</span><span class="sxs-lookup"><span data-stu-id="7619b-125">CPU profiles show where runtime is spent within the functions of your page.</span></span>  <span data-ttu-id="7619b-126">Obtenga información sobre cómo crear perfiles de CPU en [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].</span><span class="sxs-lookup"><span data-stu-id="7619b-126">Learn how to create CPU profiles in [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJavascriptRuntime].</span></span>

### <a name="javascript-problems"></a><span data-ttu-id="7619b-127">JavaScript: problemas</span><span class="sxs-lookup"><span data-stu-id="7619b-127">JavaScript: Problems</span></span>  

<span data-ttu-id="7619b-128">En la tabla siguiente se describen algunos problemas comunes de JavaScript y posibles soluciones.</span><span class="sxs-lookup"><span data-stu-id="7619b-128">The following table describes some common JavaScript problems and potential solutions.</span></span>  

| <span data-ttu-id="7619b-129">Problema</span><span class="sxs-lookup"><span data-stu-id="7619b-129">Problem</span></span> | <span data-ttu-id="7619b-130">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="7619b-130">Example</span></span> | <span data-ttu-id="7619b-131">Solución</span><span class="sxs-lookup"><span data-stu-id="7619b-131">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="7619b-132">Controladores de entrada caros que afectan a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="7619b-132">Expensive input handlers affecting response or animation.</span></span>  | <span data-ttu-id="7619b-133">Desplazamiento táctil y paralaje.</span><span class="sxs-lookup"><span data-stu-id="7619b-133">Touch, parallax scrolling.</span></span>  | <span data-ttu-id="7619b-134">Permitir que el explorador controle los desplazamientos y los contactos táctiles, o enlazar el agente de escucha lo más tarde posible.</span><span class="sxs-lookup"><span data-stu-id="7619b-134">Let the browser handle touch and scrolls, or bind the listener as late as possible.</span></span>  <span data-ttu-id="7619b-135">Vaya a [Controladores de entrada caros en la][WebPerformanceCalendarRuntimeChecklist]lista de comprobación de rendimiento en tiempo de ejecución de Paul Lewis .</span><span class="sxs-lookup"><span data-stu-id="7619b-135">Navigate to [Expensive Input Handlers in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  
| <span data-ttu-id="7619b-136">JavaScript mal timed que afecta a la respuesta, animación, carga.</span><span class="sxs-lookup"><span data-stu-id="7619b-136">Badly-timed JavaScript affecting response, animation, load.</span></span>  | <span data-ttu-id="7619b-137">El usuario se desplaza justo después de la carga de página, setTimeout / setInterval.</span><span class="sxs-lookup"><span data-stu-id="7619b-137">User scrolls right after page load, setTimeout / setInterval.</span></span>  | <span data-ttu-id="7619b-138">Optimizar el tiempo de ejecución de JavaScript: use `requestAnimationFrame` , extienda la manipulación de DOM en fotogramas, use [Trabajadores web][MDNUsingWebWorkers].</span><span class="sxs-lookup"><span data-stu-id="7619b-138">Optimize JavaScript runtime: use `requestAnimationFrame`, spread DOM manipulation over frames, use [Web Workers][MDNUsingWebWorkers].</span></span>  |  
| <span data-ttu-id="7619b-139">JavaScript de ejecución larga que afecta a la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7619b-139">Long-running JavaScript affecting response.</span></span>  | <span data-ttu-id="7619b-140">El [evento DOMContentLoaded][MDNUsingWebWorkers] se detiene cuando está saturado de trabajo de JS.</span><span class="sxs-lookup"><span data-stu-id="7619b-140">The [DOMContentLoaded event][MDNUsingWebWorkers] stalls as it is swamped with JS work.</span></span>  | <span data-ttu-id="7619b-141">Mover el trabajo computacional puro a [Trabajadores web.][MDNUsingWebWorkers]</span><span class="sxs-lookup"><span data-stu-id="7619b-141">Move pure computational work to [Web Workers][MDNUsingWebWorkers].</span></span>  <span data-ttu-id="7619b-142">Si necesita acceso DOM, use `requestAnimationFrame` .</span><span class="sxs-lookup"><span data-stu-id="7619b-142">If you need DOM access, use `requestAnimationFrame`.</span></span>  <!--Navigate to [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| <span data-ttu-id="7619b-143">Scripts de elementos no utilizados que afectan a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="7619b-143">Garbage-y scripts affecting response or animation.</span></span>  | <span data-ttu-id="7619b-144">La recolección de elementos no utilizados puede producirse en cualquier lugar.</span><span class="sxs-lookup"><span data-stu-id="7619b-144">Garbage collection may happen anywhere.</span></span>  | <span data-ttu-id="7619b-145">Escribir menos scripts de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="7619b-145">Write less garbage-y scripts.</span></span>  <span data-ttu-id="7619b-146">Vaya a [Recolección de elementos no utilizados en Animación en la lista][WebPerformanceCalendarRuntimeChecklist]de comprobación de rendimiento en tiempo de ejecución de Paul Lewis .</span><span class="sxs-lookup"><span data-stu-id="7619b-146">Navigate to [Garbage Collection in Animation in Paul Lewis' runtime performance checklist][WebPerformanceCalendarRuntimeChecklist].</span></span>  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <a name="style"></a><span data-ttu-id="7619b-147">Estilo</span><span class="sxs-lookup"><span data-stu-id="7619b-147">Style</span></span>  

<span data-ttu-id="7619b-148">Los cambios de estilo son costosos, especialmente si esos cambios afectan a más de un elemento del DOM.</span><span class="sxs-lookup"><span data-stu-id="7619b-148">Style changes are costly, especially if those changes affect more than one element in the DOM.</span></span>  <span data-ttu-id="7619b-149">Cada vez que se aplican estilos a un elemento, el explorador calcula el impacto en todos los elementos relacionados, vuelve a calcular el diseño y vuelve a pintar.</span><span class="sxs-lookup"><span data-stu-id="7619b-149">Any time you apply styles to an element, the browser figures out the impact on all related elements, recalculates the layout, and repaints.</span></span>  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <a name="style-tools"></a><span data-ttu-id="7619b-150">Estilo: herramientas</span><span class="sxs-lookup"><span data-stu-id="7619b-150">Style: Tools</span></span>  

<span data-ttu-id="7619b-151">Realizar una grabación en la **herramienta** Rendimiento.</span><span class="sxs-lookup"><span data-stu-id="7619b-151">Take a recording in the **Performance** tool.</span></span>  <span data-ttu-id="7619b-152">Compruebe en la grabación si hay `Recalculate Style` eventos grandes \(mostrados en púrpura\).</span><span class="sxs-lookup"><span data-stu-id="7619b-152">Check the recording for large `Recalculate Style` events \(displayed in purple\).</span></span>  

<!--todo: add Recording section when available  -->  

<span data-ttu-id="7619b-153">Elija un `Recalculate Style` evento para ver más información sobre él en el **panel** Detalles.</span><span class="sxs-lookup"><span data-stu-id="7619b-153">Choose a `Recalculate Style` event to view more information about it in the **Details** pane.</span></span>  <span data-ttu-id="7619b-154">Si los cambios de estilo tardan mucho tiempo, es un éxito de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="7619b-154">If the style changes are taking a long time, that is a performance hit.</span></span>  <span data-ttu-id="7619b-155">Si los cálculos de estilo afectan a un gran número de elementos, ese es otro área con espacio para mejorar.</span><span class="sxs-lookup"><span data-stu-id="7619b-155">If the style calculations are affecting a large number of elements, that is another area with room for improvement.</span></span>  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Estilo de recálculo largo" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="7619b-157">Estilo de recálculo largo</span><span class="sxs-lookup"><span data-stu-id="7619b-157">Long recalculate style</span></span>  
:::image-end:::  

<span data-ttu-id="7619b-158">Para reducir el impacto de los `Recalculate Style` eventos:</span><span class="sxs-lookup"><span data-stu-id="7619b-158">To reduce the impact of `Recalculate Style` events:</span></span>  

*   <span data-ttu-id="7619b-159">Usa los [desencadenadores CSS][CssTriggers] para saber qué propiedades CSS desencadenan el diseño, la pintura y la composición.</span><span class="sxs-lookup"><span data-stu-id="7619b-159">Use the [CSS Triggers][CssTriggers] to learn which CSS properties trigger layout, paint, and composite.</span></span>  <span data-ttu-id="7619b-160">Estas propiedades tienen el peor impacto en el rendimiento de representación.</span><span class="sxs-lookup"><span data-stu-id="7619b-160">These properties have the worst impact on rendering performance.</span></span>  
*   <span data-ttu-id="7619b-161">Cambie a las propiedades que tienen menos impacto.</span><span class="sxs-lookup"><span data-stu-id="7619b-161">Switch to properties that have less impact.</span></span>  <!--For more guidance, navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <a name="style-problems"></a><span data-ttu-id="7619b-162">Estilo: problemas</span><span class="sxs-lookup"><span data-stu-id="7619b-162">Style: Problems</span></span>  

<span data-ttu-id="7619b-163">En la tabla siguiente se describen algunos problemas de estilo comunes y posibles soluciones.</span><span class="sxs-lookup"><span data-stu-id="7619b-163">The following table describes some common style problems and potential solutions.</span></span>  

| <span data-ttu-id="7619b-164">Problema</span><span class="sxs-lookup"><span data-stu-id="7619b-164">Problem</span></span> | <span data-ttu-id="7619b-165">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="7619b-165">Example</span></span> | <span data-ttu-id="7619b-166">Solución</span><span class="sxs-lookup"><span data-stu-id="7619b-166">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="7619b-167">Cálculos de estilo caros que afectan a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="7619b-167">Expensive style calculations affecting response or animation.</span></span>  | <span data-ttu-id="7619b-168">Cualquier propiedad CSS que cambie la geometría de un elemento, como el ancho, alto o posición; el explorador comprueba todos los demás elementos y vuelve a calcular el diseño.</span><span class="sxs-lookup"><span data-stu-id="7619b-168">Any CSS property that changes the geometry of an element, like the width, height, or position; the browser checks all other elements and recalculates the layout.</span></span>  | <span data-ttu-id="7619b-169">Evitar CSS que desencadena diseños</span><span class="sxs-lookup"><span data-stu-id="7619b-169">Avoid CSS that triggers layouts</span></span> |  
| <span data-ttu-id="7619b-170">Selectores complejos que afectan a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="7619b-170">Complex selectors affecting response or animation.</span></span>  | <span data-ttu-id="7619b-171">Los selectores anidados fuerzan al explorador a saber todo sobre todos los demás elementos, incluidos los elementos principales y los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="7619b-171">Nested selectors force the browser to know everything about all the other elements, including parents and children.</span></span>  | <span data-ttu-id="7619b-172">Haga referencia a un elemento de su CSS con solo una clase.</span><span class="sxs-lookup"><span data-stu-id="7619b-172">Reference an element in your CSS with just a class.</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <a name="layout"></a><span data-ttu-id="7619b-173">Diseño</span><span class="sxs-lookup"><span data-stu-id="7619b-173">Layout</span></span>  

<span data-ttu-id="7619b-174">El diseño (o reflujo en Firefox) es el proceso mediante el cual el explorador calcula las posiciones y tamaños de todos los elementos de una página.</span><span class="sxs-lookup"><span data-stu-id="7619b-174">Layout (or reflow in Firefox) is the process by which the browser calculates the positions and sizes of all the elements on a page.</span></span>  <span data-ttu-id="7619b-175">El modelo de diseño de la web significa que un elemento puede afectar a otros; por ejemplo, el ancho del elemento suele afectar a los anchos de los elementos secundarios, y así sucesivamente, hasta arriba y `<body>` abajo del árbol.</span><span class="sxs-lookup"><span data-stu-id="7619b-175">The layout model of the web means that one element may affect others; for example, the width of the `<body>` element typically affects the widths of any child elements, and so on, all the way up and down the tree.</span></span>  <span data-ttu-id="7619b-176">El proceso puede estar bastante implicado para el explorador.</span><span class="sxs-lookup"><span data-stu-id="7619b-176">The process may be quite involved for the browser.</span></span>  

<span data-ttu-id="7619b-177">Como regla general, si solicita un valor geométrico del DOM antes de que se complete un marco, se encontrará con "diseños sincrónicos forzados", lo que puede ser un gran cuello de botella de rendimiento si se repite con frecuencia o se realiza para un árbol DOM grande.</span><span class="sxs-lookup"><span data-stu-id="7619b-177">As a general rule of thumb, if you ask for a geometric value back from the DOM before a frame is complete, you are going to find yourself with "forced synchronous layouts", which may be a big performance bottleneck if repeated frequently or performed for a large DOM tree.</span></span>  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <a name="layout-tools"></a><span data-ttu-id="7619b-178">Diseño: Herramientas</span><span class="sxs-lookup"><span data-stu-id="7619b-178">Layout: Tools</span></span>  

<span data-ttu-id="7619b-179">El **panel** Rendimiento identifica cuándo una página provoca diseños sincrónicos forzados.</span><span class="sxs-lookup"><span data-stu-id="7619b-179">The **Performance** pane identifies when a page causes forced synchronous layouts.</span></span>  <span data-ttu-id="7619b-180">Estos `Layout` eventos se marcan con barras rojas.</span><span class="sxs-lookup"><span data-stu-id="7619b-180">These `Layout` events are marked with red bars.</span></span>  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Diseño sincrónico forzado" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   <span data-ttu-id="7619b-182">Diseño sincrónico forzado</span><span class="sxs-lookup"><span data-stu-id="7619b-182">Forced synchronous layout</span></span>  
:::image-end:::  

<span data-ttu-id="7619b-183">"Thrashing de diseño" es una repetición de condiciones de diseño sincrónica forzadas.</span><span class="sxs-lookup"><span data-stu-id="7619b-183">"Layout thrashing" is a repetition of forced synchronous layout conditions.</span></span>  <span data-ttu-id="7619b-184">Esto ocurre cuando JavaScript escribe y lee el DOM repetidamente, lo que fuerza al explorador a volver a calcular el diseño una y otra vez.</span><span class="sxs-lookup"><span data-stu-id="7619b-184">This occurs when JavaScript writes and reads from the DOM repeatedly, which forces the browser to recalculate the layout over and over.</span></span>  <span data-ttu-id="7619b-185">Para identificar la thrashing de diseño, busque un patrón de varias advertencias de diseño sincrónico forzado.</span><span class="sxs-lookup"><span data-stu-id="7619b-185">To identify layout thrashing, look for a pattern of multiple forced synchronous layout warnings.</span></span>  <span data-ttu-id="7619b-186">Revise la figura anterior.</span><span class="sxs-lookup"><span data-stu-id="7619b-186">Review the previous figure.</span></span>  

### <a name="layout-problems"></a><span data-ttu-id="7619b-187">Diseño: problemas</span><span class="sxs-lookup"><span data-stu-id="7619b-187">Layout: Problems</span></span>  

<span data-ttu-id="7619b-188">En la tabla siguiente se describen algunos problemas comunes de diseño y posibles soluciones.</span><span class="sxs-lookup"><span data-stu-id="7619b-188">The following table describes some common layout problems and potential solutions.</span></span>  

| <span data-ttu-id="7619b-189">Problema</span><span class="sxs-lookup"><span data-stu-id="7619b-189">Problem</span></span> | <span data-ttu-id="7619b-190">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="7619b-190">Example</span></span> | <span data-ttu-id="7619b-191">Solución</span><span class="sxs-lookup"><span data-stu-id="7619b-191">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="7619b-192">Diseño sincrónico forzado que afecta a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="7619b-192">Forced synchronous layout affecting response or animation.</span></span>  | <span data-ttu-id="7619b-193">Forzar al explorador a realizar el diseño anteriormente en la canalización de píxeles, lo que da como resultado la repetición de pasos en el proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="7619b-193">Forcing the browser to perform layout earlier in the pixel pipeline, resulting in repeating steps in the rendering process.</span></span>  | <span data-ttu-id="7619b-194">Primero se lee por lotes el estilo y, a continuación, se hacen las escrituras.</span><span class="sxs-lookup"><span data-stu-id="7619b-194">Batch your style reads first, then do any writes.</span></span>  <!--Navigate to [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| <span data-ttu-id="7619b-195">Diseño thrashing que afecta a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="7619b-195">Layout thrashing affecting response or animation.</span></span>  | <span data-ttu-id="7619b-196">Bucle que coloca al explorador en un ciclo de lectura y escritura y lectura, lo que obliga al explorador a volver a calcular el diseño una y otra vez.</span><span class="sxs-lookup"><span data-stu-id="7619b-196">A loop that puts the browser into a read-write-read-write cycle, forcing the browser to recalculate layout over and over again.</span></span>  | <span data-ttu-id="7619b-197">Procesar por lotes automáticamente operaciones de lectura y escritura con [la biblioteca FastDom][GitHubWilsonpageFastdom].</span><span class="sxs-lookup"><span data-stu-id="7619b-197">Automatically batch read-write operations using [FastDom library][GitHubWilsonpageFastdom].</span></span>  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <a name="paint-and-composite"></a><span data-ttu-id="7619b-198">Paint y compuesto</span><span class="sxs-lookup"><span data-stu-id="7619b-198">Paint and composite</span></span>  

<span data-ttu-id="7619b-199">Paint es el proceso de relleno en píxeles.</span><span class="sxs-lookup"><span data-stu-id="7619b-199">Paint is the process of filling in pixels.</span></span>  <span data-ttu-id="7619b-200">Suele ser la parte más costosa del proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="7619b-200">It is often the most costly part of the rendering process.</span></span>  <span data-ttu-id="7619b-201">Si notó que la página no funciona como está diseñada de ninguna manera, es probable que tenga problemas de pintura.</span><span class="sxs-lookup"><span data-stu-id="7619b-201">If you noticed that your page is not working as designed in any way, it is likely that you have paint problems.</span></span>  

<span data-ttu-id="7619b-202">La composición es donde se reúnen las partes de la página que se pintan para mostrarse en pantalla.</span><span class="sxs-lookup"><span data-stu-id="7619b-202">Compositing is where the painted parts of the page are put together for displaying on screen.</span></span>  <span data-ttu-id="7619b-203">En la mayoría de los casos, si te atener a las propiedades de compositor y evitas pintar por completo, deberías observar una mejora importante en el rendimiento, pero debes tener cuidado con los recuentos excesivos de capas.</span><span class="sxs-lookup"><span data-stu-id="7619b-203">For the most part, if you stick to compositor-only properties and avoid paint altogether, you should notice a major improvement in performance, but you need to watch out for excessive layer counts.</span></span>  <!--Navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <a name="paint-and-composite-tools"></a><span data-ttu-id="7619b-204">Paint y compuesto: Herramientas</span><span class="sxs-lookup"><span data-stu-id="7619b-204">Paint and composite: Tools</span></span>  

<span data-ttu-id="7619b-205">¿Quiere saber cuánto tarda la pintura o con qué frecuencia se produce la pintura?</span><span class="sxs-lookup"><span data-stu-id="7619b-205">Want to know how long painting takes or how often painting occurs?</span></span>  <span data-ttu-id="7619b-206">Compruebe la [configuración Habilitar instrumentación avanzada de][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] pintura en el panel Rendimiento y, a continuación, haga una grabación. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7619b-206">Check the [Enable advanced paint instrumentation][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] setting in the **Performance** panel and then take a recording.</span></span>  <span data-ttu-id="7619b-207">Si la mayor parte del tiempo de representación se dedica a pintar, tiene problemas de pintura.</span><span class="sxs-lookup"><span data-stu-id="7619b-207">If most of your rendering time is spent painting, you have paint problems.</span></span>  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <a name="paint-and-composite-problems"></a><span data-ttu-id="7619b-208">Paint y compuesto: Problemas</span><span class="sxs-lookup"><span data-stu-id="7619b-208">Paint and composite: Problems</span></span>  

<span data-ttu-id="7619b-209">En la tabla siguiente se describen algunos problemas comunes de pintura y compuestos y posibles soluciones.</span><span class="sxs-lookup"><span data-stu-id="7619b-209">The following table describes some common paint and composite problems and potential solutions.</span></span>  

| <span data-ttu-id="7619b-210">Problema</span><span class="sxs-lookup"><span data-stu-id="7619b-210">Problem</span></span> | <span data-ttu-id="7619b-211">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="7619b-211">Example</span></span> | <span data-ttu-id="7619b-212">Solución</span><span class="sxs-lookup"><span data-stu-id="7619b-212">Solution</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="7619b-213">Paint tormentas que afectan a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="7619b-213">Paint storms affecting response or animation.</span></span>  | <span data-ttu-id="7619b-214">Áreas de pintura grandes o pinturas costosas que afectan a la respuesta o animación.</span><span class="sxs-lookup"><span data-stu-id="7619b-214">Big paint areas or expensive paints affecting response or animation.</span></span>  | <span data-ttu-id="7619b-215">Evite la pintura, promueva los elementos que se mueven a su propia capa, use transformaciones y opacidad.</span><span class="sxs-lookup"><span data-stu-id="7619b-215">Avoid paint, promote elements that are moving to their own layer, use transforms and opacity.</span></span>  <!--Navigate to [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| <span data-ttu-id="7619b-216">Explosiones de capas que afectan a animaciones.</span><span class="sxs-lookup"><span data-stu-id="7619b-216">Layer explosions affecting animations.</span></span>  | <span data-ttu-id="7619b-217">La sobrepromoción de demasiados elementos afecta en gran medida `translateZ(0)` al rendimiento de la animación.</span><span class="sxs-lookup"><span data-stu-id="7619b-217">Overpromotion of too many elements with `translateZ(0)` greatly affects animation performance.</span></span>  | <span data-ttu-id="7619b-218">Promover a las capas con moderación y solo cuando sepa que ofrece mejoras tangibles.</span><span class="sxs-lookup"><span data-stu-id="7619b-218">Promote to layers sparingly, and only when you know it offers tangible improvements.</span></span>  <!--Navigate to [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="7619b-219">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7619b-219">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Acelerar el tiempo de ejecución de JavaScript | Microsoft Docs"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#turn-on-advanced-paint-instrumentation "Activar instrumentación de pintura avanzada: referencia de análisis de rendimiento | Microsoft Docs"

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

[CssTriggers]: https://csstriggers.com "Desencadenadores CSS"  

[MDNUsingWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Uso de trabajadores web | MDN"  

[WebPerformanceCalendarRuntimeChecklist]: https://calendar.perfplanet.com/2013/the-runtime-performance-checklist/ "Lista de comprobación de rendimiento en tiempo de ejecución: calendario de rendimiento web"  

[GitHubWilsonpageFastdom]: https://github.com/wilsonpage/fastdom "wilsonpage/fastdom | GitHub"  

> [!NOTE]
> <span data-ttu-id="7619b-226">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7619b-226">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7619b-227">La página original [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) se encuentra aquí y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) y [Meggin Kearney][MegginKearney] \(Tech Writer\).</span><span class="sxs-lookup"><span data-stu-id="7619b-227">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7619b-229">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7619b-229">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  

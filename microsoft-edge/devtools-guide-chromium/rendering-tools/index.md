---
description: Los usuarios esperan páginas interactivas y suaves.  Cada fase de la canalización de píxeles representa una oportunidad de introducir Jank.  Obtenga más información sobre las herramientas y estrategias para identificar y solucionar problemas comunes que ralentizan el rendimiento del tiempo de ejecución.
title: Analizar el rendimiento en tiempo de ejecución
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f7ca848712268110700fac2c5fb75fe1751812bf
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992711"
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

# Analizar el rendimiento en tiempo de ejecución 

Los usuarios esperan páginas interactivas y suaves.  Cada fase de la canalización de píxeles representa una oportunidad de introducir Jank.  Obtenga más información sobre las herramientas y estrategias para identificar y solucionar problemas comunes que ralentizan el rendimiento del tiempo de ejecución.  

### Resumen  

*   No escriba JavaScript que obligue al explorador a volver a calcular el diseño.  Funciones de lectura y escritura distintas y realice lecturas en primer lugar.  
*   No complica demasiado tu CSS.  Usa menos CSS y conserva tus selectores de CSS.  
*   Evite el diseño tanto como sea posible.  Elija CSS que no desencadene el diseño.  
*   La pintura puede tardar más tiempo que cualquier otra actividad de representación.  Mire los cuellos de botella de pintura.  
    
## JavaScript  

Los cálculos de JavaScript, especialmente aquellos que desencadenan cambios visuales extensivos, pueden detener el rendimiento de la aplicación.  No permita que los JavaScript con tiempos inesperados o de ejecución prolongada interfieran con las interacciones del usuario.  

### JavaScript: herramientas  

Toma una grabación en el panel **rendimiento** y busca eventos que sean sospechosos `Evaluate Script` .  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

Si recibes bastante Jank en tu código JavaScript, es posible que necesites llevar el análisis al siguiente nivel y recopilar un perfil de CPU de JavaScript.  Los perfiles de CPU muestran dónde se gasta el motor en tiempo de ejecución dentro de las funciones de la página.  Aprenda a crear perfiles de CPU para [acelerar el tiempo de ejecución de JavaScript][DevtoolsRenderingToolsJavascriptRuntime].

### JavaScript: problemas  

En la siguiente tabla se describen algunos problemas comunes de JavaScript y posibles soluciones:  

| Problema | Ejemplo | Solución |  
|:--- |:--- |:--- |  
| Controladores de entrada caros que afectan a la respuesta o animación.  | Táctil, desplazamiento de Parallax.  | Deje que el explorador controle la entrada táctil y se desplace, o enlace el agente de escucha lo más tarde posible.  Consulte [controladores de entrada costosos en la lista de comprobación de rendimiento en tiempo de ejecución de Paul Lewis][WebPerformanceCalendarRuntimeChecklist].  |  
| La respuesta, la animación y la carga de JavaScript es muy incorrecta.  | El usuario se desplaza a la derecha después de cargar la página, setTimeout/setInterval.  | Optimizar tiempo de ejecución de JavaScript: uso `requestAnimationFrame` , manipulación de Dom de propagación sobre marcos, uso de [trabajadores web][MDNUsingWebWorkers].  |  
| JavaScript de ejecución prolongada que afecta a la respuesta.  | El [evento DOMContentLoaded][MDNUsingWebWorkers] se detiene porque está inundado con el trabajo de JS.  | Mover trabajo de cálculo puro a los [trabajadores web][MDNUsingWebWorkers].  Si necesita acceso a DOM, use `requestAnimationFrame` .  <!--See also [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| Scripts de elementos no utilizados que afectan a la respuesta o animación.  | La recolección de elementos no utilizados puede producirse en cualquier lugar.  | Escribir menos scripts y de elementos no utilizados.  Consulte recolección [de elementos no utilizados en la animación de la lista de comprobación de rendimiento en tiempo de ejecución de Paul Lewis][WebPerformanceCalendarRuntimeChecklist].  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## Estilo  

Los cambios de estilo son costosos, especialmente si esos cambios afectan a más de un elemento en el DOM.  Cada vez que se aplican estilos a un elemento, el explorador determina el impacto en todos los elementos relacionados, vuelve a calcular el diseño y el redibujado.  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### Estilo: herramientas  

Realizar una grabación en el panel **rendimiento** .  Compruebe la grabación de `Recalculate Style` eventos grandes \ (mostrada en color púrpura \).  

<!--todo: add Recording section when available  -->  

Haga clic en un `Recalculate Style` evento para ver más información sobre él en el panel de **detalles** .  Si los cambios de estilo están tardando mucho, eso es un impacto en el rendimiento.  Si los cálculos de estilo afectan a un gran número de elementos, se trata de otra área con espacio para mejorarlo.  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Recalcular largo estilo" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   Recalcular largo estilo  
:::image-end:::  

Para reducir el impacto de `Recalculate Style` los eventos:  

*   Use los [desencadenadores de CSS][CssTriggers] para saber qué propiedades de CSS desencadenan diseño, pintura y composición.  Estas propiedades tienen el peor impacto en el rendimiento de la representación.  
*   Cambiar a propiedades que tienen menos impacto.  <!--See [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties] for more guidance.  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### Estilo: problemas  

En la siguiente tabla se describen algunos problemas de estilo comunes y posibles soluciones:  

| Problema | Ejemplo | Solución |  
|:--- |:--- |:--- |  
| Cálculos de estilo caros que afectan a la respuesta o animación.  | Cualquier propiedad de CSS que cambie la geometría de un elemento, como el ancho, alto o posición; el explorador comprueba el resto de los elementos y vuelve a calcular el diseño.  | Evitar CSS que desencadenan diseños |  
| Selectores complejos que afectan a la respuesta o a la animación.  | Los selectores anidados obligan al explorador a conocer todo el resto de los elementos, incluidos los elementos primarios y secundarios.  | Haga referencia a un elemento de su CSS con solo una clase.  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## Diseño  

Diseño (o redistribución en Firefox) es el proceso por el cual el explorador calcula las posiciones y los tamaños de todos los elementos de una página.  El modelo de diseño de la web significa que un elemento puede afectar a otros; por ejemplo, el ancho del `<body>` elemento afecta normalmente a los anchos de los elementos secundarios, y así sucesivamente, todo el recorrido hacia arriba y hacia abajo en el árbol.  El proceso puede estar bastante implicado para el explorador.  

Como regla general, si solicita un valor geométrico al DOM antes de que se complete un marco, se encontrará con "diseños sincrónicos forzados", que puede ser un gran cuello de botella de rendimiento si se repite con frecuencia o se realiza para un gran árbol de DOM.  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### Diseño: herramientas  

El panel **rendimiento** identifica cuando una página provoca diseños sincrónicos forzados.  Estos `Layout` eventos se marcan con barras rojas.  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Diseño sincrónico forzado" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   Diseño sincrónico forzado  
:::image-end:::  

"La hiperpaginación de diseño" es una repetición de las condiciones de diseño sincrónico forzado.  Esto se produce cuando JavaScript escribe y Lee de forma repetida desde el DOM, lo que obliga al explorador a volver a calcular el diseño una y otra vez.  Para identificar la hiperpaginación de la distribución, busque un patrón de advertencias de diseño sincrónico forzado.  Vea la ilustración anterior.  

### Diseño: problemas  

En la siguiente tabla se describen algunos problemas de diseño comunes y posibles soluciones:  

| Problema | Ejemplo | Solución |  
|:--- |:--- |:--- |  
| Diseño sincrónico forzado que afecta a la respuesta o animación.  | Obligar al explorador a realizar el diseño anteriormente en la canalización de píxeles, lo que da como resultado pasos repetitivos en el proceso de representación.  | Por lotes el estilo se lee en primer lugar y luego realiza cualquier escritura.  <!--See also [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| La hiperpaginación de diseño afecta a la respuesta o animación.  | Un bucle que pone el explorador en un ciclo de lectura y escritura (lectura y escritura), lo que obliga al explorador a volver a calcular la presentación una y otra vez.  | Procesar automáticamente las operaciones de lectura y escritura con la [biblioteca FastDom][GitHubWilsonpageFastdom].  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## Pintura y composición  

Paint es el proceso de rellenar píxeles.  Suele ser la parte más costosa del proceso de representación.  Si se ha dado cuenta de que la página se Janky de ninguna manera, es posible que tenga problemas de pintura.  

La composición es el lugar donde se agrupan las partes pintadas de la página para mostrarse en pantalla.  En su mayor parte, si se fija en las propiedades solo de compositor y se evita que se pinte por completo, debería apreciarse una mejora importante en el rendimiento, pero debe tener cuidado con el recuento excesivo de capas.  <!--See also [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### Pintura y composición: herramientas  

¿Quiere saber cuánto tarda el pintado o la frecuencia con la que se produce la pintura?  Active la opción [Habilitar el instrumental de pintura avanzada][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] en el panel **rendimiento** y, después, realice una grabación.  Si se gasta la mayor parte del tiempo de procesamiento, tiene problemas de pintura.  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### Pintura y composición: problemas  

En la siguiente tabla se describen algunos problemas comunes de Paint y compuestos y posibles soluciones:  

| Problema | Ejemplo | Solución |  
|:--- |:--- |:--- |  
| Las tormentas de pintura afectan a la respuesta o animación.  | Grandes áreas de pintura o pinturas caras que afectan a la respuesta o animación.  | Evite pintar, promocionar elementos que estén desplazándose a su propia capa, usar transformaciones y opacidad.  <!--See [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| Explosiones de capas que afectan a las animaciones.  | Exceso de la promoción de demasiados elementos con el rendimiento de la `translateZ(0)` animación.  | Promueve a capas con moderación, y solo cuando sepa que ofrece mejoras tangibles.  <!--See [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsRenderingToolsJavascriptRuntime]: ./js-runtime.md "Acelerar el tiempo de ejecución de JavaScript | Microsoft docs"  
[DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation]: ../evaluate-performance/reference.md#enable-advanced-paint-instrumentation "Habilitar instrumentación de pintura avanzada-referencia de análisis de rendimiento | Microsoft docs"

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
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \) y [Meggin Kearney][MegginKearney] \ (Tech Writer \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

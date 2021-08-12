---
description: Los usuarios esperan páginas interactivas y suaves.  Cada fase de la canalización de píxeles representa una oportunidad para introducir jank.  Obtenga información sobre herramientas y estrategias para identificar y corregir problemas comunes que ralentizan el rendimiento en tiempo de ejecución.
title: Analizar el rendimiento en tiempo de ejecución
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: c8060b20e3b25d40fcf7a90102d19cde483d64001f7fcb8998c3fbafe4b862df
ms.sourcegitcommit: 8a3c6e6f69a4b5419f857b9e9fc983e573fd956c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/09/2021
ms.locfileid: "11810533"
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
# <a name="analyze-runtime-performance"></a>Analizar el rendimiento en tiempo de ejecución  

Los usuarios esperan páginas interactivas y suaves.  Cada fase de la canalización de píxeles representa una oportunidad para introducir jank.  Obtenga información sobre herramientas y estrategias para identificar y corregir problemas comunes que ralentizan el rendimiento en tiempo de ejecución.  

### <a name="summary"></a>Resumen  

*   No escriba JavaScript que fuerza al explorador a volver a calcular el diseño.  Separe las funciones de lectura y escritura y realice primero lecturas.  
*   No complique en exceso su CSS.  Use menos CSS y mantenga los selectores CSS sencillos.  
*   Evite el diseño tanto como sea posible.  Elija CSS que no desencadene el diseño en absoluto.  
*   La pintura puede tardar más tiempo que cualquier otra actividad de representación.  Cuidado con los cuellos de botella de pintura.  
    
## <a name="javascript"></a>JavaScript  

Los cálculos de JavaScript, especialmente los que desencadenan grandes cambios visuales, pueden detener el rendimiento de las aplicaciones.  No permita que JavaScript con un tiempo mal definido o de ejecución larga interfiera con las interacciones del usuario.  

### <a name="javascript-tools"></a>JavaScript: herramientas  

Haga una grabación en la **herramienta Rendimiento** y busque eventos sospechosamente `Evaluate Script` largos.  <!--If you find any, you are able to enable the **JS Profiler** and re-do your recording to get more detailed information about exactly which JavaScript functions were used and how long each took.  -->  

<!--todo: add Recording section when available  -->  
<!--todo: add Profile JavaScript (JS Profiler) section when available  -->  

Si observa bastante jank (interrupciones de representación) en JavaScript, es posible que deba llevar el análisis al siguiente nivel y recopilar un perfil de CPU de JavaScript.  Los perfiles de CPU muestran dónde se usa el tiempo de ejecución dentro de las funciones de la página.  Obtenga información sobre cómo crear perfiles de CPU en [Speed up JavaScript runtime][DevtoolsRenderingToolsJavascriptRuntime].

### <a name="javascript-problems"></a>JavaScript: problemas  

En la tabla siguiente se describen algunos problemas comunes de JavaScript y posibles soluciones.  

| Problema | Por ejemplo: | Solución |  
|:--- |:--- |:--- |  
| Controladores de entrada caros que afectan a la respuesta o animación.  | Desplazamiento táctil y paralaje.  | Permitir que el explorador controle los desplazamientos y los contactos táctiles, o enlazar el agente de escucha lo más tarde posible.  Vaya a [Controladores de entrada caros en la][WebPerformanceCalendarRuntimeChecklist]lista de comprobación de rendimiento en tiempo de ejecución de Paul Lewis .  |  
| JavaScript mal timed que afecta a la respuesta, animación, carga.  | El usuario se desplaza justo después de la carga de página, setTimeout / setInterval.  | Optimizar el tiempo de ejecución de JavaScript: use `requestAnimationFrame` , extienda la manipulación de DOM en fotogramas, use [Trabajadores web][MDNUsingWebWorkers].  |  
| JavaScript de ejecución larga que afecta a la respuesta.  | El [evento DOMContentLoaded][MDNUsingWebWorkers] se detiene cuando está saturado de trabajo de JS.  | Mover el trabajo computacional puro a [Trabajadores web.][MDNUsingWebWorkers]  Si necesita acceso DOM, use `requestAnimationFrame` .  <!--Navigate to [Optimize JavaScript Execution][WebFundamentalsPerformanceRenderingOptimizeJavascriptRuntime].  -->  |  
| Scripts de elementos no utilizados que afectan a la respuesta o animación.  | La recolección de elementos no utilizados puede producirse en cualquier lugar.  | Escribir menos scripts de elementos no utilizados.  Vaya a [Recolección de elementos no utilizados en Animación en la lista][WebPerformanceCalendarRuntimeChecklist]de comprobación de rendimiento en tiempo de ejecución de Paul Lewis .  |  

<!--todo: add Optimize JavaScript runtime section when available  -->  

## <a name="style"></a>Estilo  

Los cambios de estilo son costosos, especialmente si esos cambios afectan a más de un elemento del DOM.  Cada vez que se aplican estilos a un elemento, el explorador calcula el impacto en todos los elementos relacionados, vuelve a calcular el diseño y vuelve a pintar.  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  
-->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

### <a name="style-tools"></a>Estilo: herramientas  

Realizar una grabación en la **herramienta** Rendimiento.  Compruebe en la grabación si hay `Recalculate Style` eventos grandes \(mostrados en púrpura\).  

<!--todo: add Recording section when available  -->  

Elija un `Recalculate Style` evento para ver más información sobre él en el **panel** Detalles.  Si los cambios de estilo tardan mucho tiempo, es un éxito de rendimiento.  Si los cálculos de estilo afectan a un gran número de elementos, ese es otro área con espacio para mejorar.  

:::image type="complex" source="../media/rendering-tools-performance-recalculate-style-summary.msft.png" alt-text="Estilo de recálculo largo" lightbox="../media/rendering-tools-performance-recalculate-style-summary.msft.png":::
   Estilo de recálculo largo  
:::image-end:::  

Para reducir el impacto de los `Recalculate Style` eventos:  

*   Usa los [desencadenadores CSS][CssTriggers] para saber qué propiedades CSS desencadenan el diseño, la pintura y la composición.  Estas propiedades tienen el peor impacto en el rendimiento de representación.  
*   Cambie a las propiedades que tienen menos impacto.  <!--For more guidance, navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  
    
<!--todo: add Stick to compositor-only properties and manage layer count section when available -->  

### <a name="style-problems"></a>Estilo: problemas  

En la tabla siguiente se describen algunos problemas de estilo comunes y posibles soluciones.  

| Problema | Por ejemplo: | Solución |  
|:--- |:--- |:--- |  
| Cálculos de estilo caros que afectan a la respuesta o animación.  | Cualquier propiedad CSS que cambie la geometría de un elemento, como el ancho, alto o posición; el explorador comprueba todos los demás elementos y vuelve a calcular el diseño.  | Evitar CSS que desencadena diseños |  
| Selectores complejos que afectan a la respuesta o animación.  | Los selectores anidados fuerzan al explorador a saber todo sobre todos los demás elementos, incluidos los elementos principales y los elementos secundarios.  | Haga referencia a un elemento de su CSS con solo una clase.  |  

<!--todo: add Avoid CSS that triggers layouts section when available -->  
<!--todo: add Reduce the Scope and Complexity of Styles Calculations (Reference an element in your CSS with just a class) section when available -->  

<!--Related Guides:  

*   [Reduce the Scope and Complexity of Styles Calculations][WebFundamentalsPerformanceRenderingReduceScope]  -->  

<!--todo: add Reduce the Scope and Complexity of Styles Calculations section when available -->  

## <a name="layout"></a>Diseño  

El diseño (o reflujo en Firefox) es el proceso mediante el cual el explorador calcula las posiciones y tamaños de todos los elementos de una página.  El modelo de diseño de la web significa que un elemento puede afectar a otros; por ejemplo, el ancho del elemento suele afectar a los anchos de los elementos secundarios, y así sucesivamente, hasta arriba y `<body>` abajo del árbol.  El proceso puede estar bastante implicado para el explorador.  

Como regla general, si solicita un valor geométrico del DOM antes de que se complete un marco, se encontrará con "diseños sincrónicos forzados", lo que puede ser un gran cuello de botella de rendimiento si se repite con frecuencia o se realiza para un árbol DOM grande.  

<!--Related Guides:  

*   [Avoid Layout Thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts]  
*   [Diagnose Forced Synchronous Layouts][DevtoolsRenderingToolsForcedSynchronousLayouts]  -->  

<!--todo: add Avoid CSS that triggers layouts (Avoid Layout Thrashing) section when available -->  
<!--todo: add Diagnose Forced Synchronous Layouts section when available  -->  

### <a name="layout-tools"></a>Diseño: Herramientas  

El **panel** Rendimiento identifica cuándo una página provoca diseños sincrónicos forzados.  Estos `Layout` eventos se marcan con barras rojas.  

:::image type="complex" source="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png" alt-text="Diseño sincrónico forzado" lightbox="../media/rendering-tools-jank-performance-recalculate-style-summary.msft.png":::
   Diseño sincrónico forzado  
:::image-end:::  

"Thrashing de diseño" es una repetición de condiciones de diseño sincrónica forzadas.  Esto ocurre cuando JavaScript escribe y lee el DOM repetidamente, lo que fuerza al explorador a volver a calcular el diseño una y otra vez.  Para identificar la thrashing de diseño, busque un patrón de varias advertencias de diseño sincrónico forzado.  Revise la figura anterior.  

### <a name="layout-problems"></a>Diseño: problemas  

En la tabla siguiente se describen algunos problemas comunes de diseño y posibles soluciones.  

| Problema | Por ejemplo: | Solución |  
|:--- |:--- |:--- |  
| Diseño sincrónico forzado que afecta a la respuesta o animación.  | Forzar al explorador a realizar el diseño anteriormente en la canalización de píxeles, lo que da como resultado la repetición de pasos en el proceso de representación.  | Primero se lee por lotes el estilo y, a continuación, se hacen las escrituras.  <!--Navigate to [Avoid large, complex layouts and layout thrashing][WebFundamentalsPerformanceRenderingAvoidLargeComplexLayouts].  -->  |  
| Diseño thrashing que afecta a la respuesta o animación.  | Bucle que coloca al explorador en un ciclo de lectura y escritura y lectura, lo que obliga al explorador a volver a calcular el diseño una y otra vez.  | Procesar por lotes automáticamente operaciones de lectura y escritura con [la biblioteca FastDom][GitHubWilsonpageFastdom].  |  

<!--todo: add Avoid CSS that triggers layouts (Avoid large, complex layouts and layout thrashing) section when available -->  

## <a name="paint-and-composite"></a>Paint y compuesto  

Paint es el proceso de relleno en píxeles.  Suele ser la parte más costosa del proceso de representación.  Si notó que la página no funciona como está diseñada de ninguna manera, es probable que tenga problemas de pintura.  

La composición es donde se reúnen las partes de la página que se pintan para mostrarse en pantalla.  En la mayoría de los casos, si te atener a las propiedades de compositor y evitas pintar por completo, deberías observar una mejora importante en el rendimiento, pero debes tener cuidado con los recuentos excesivos de capas.  <!--Navigate to [Stick to compositor-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  

<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

### <a name="paint-and-composite-tools"></a>Paint y compuesto: Herramientas  

¿Quiere saber cuánto tarda la pintura o con qué frecuencia se produce la pintura?  Compruebe la [configuración Habilitar instrumentación avanzada de][DevtoolsChromiumEvaluatePerformanceReferenceEnableadvancedpaintinstrumentation] pintura en el panel Rendimiento y, a continuación, haga una grabación. ****  Si la mayor parte del tiempo de representación se dedica a pintar, tiene problemas de pintura.  

<!--
:::image type="complex" source="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png" alt-text="Long paint times in timeline recording" lightbox="../media/rendering-tools-jank-performance-advanced-paint-instrumentation-summary.msft.png":::
   Long paint times in timeline recording  
:::image-end:::  
-->  

<!--
Check out the **Rendering** panel for further configurations that are able to help you diagnose paint problems.  -->  

<!--todo: link Rendering panel in ../evaluate-performance/timeline-tool  sub-section when live  -->  

### <a name="paint-and-composite-problems"></a>Paint y compuesto: Problemas  

En la tabla siguiente se describen algunos problemas comunes de pintura y compuestos y posibles soluciones.  

| Problema | Por ejemplo: | Solución |  
|:--- |:--- |:--- |  
| Paint tormentas que afectan a la respuesta o animación.  | Áreas de pintura grandes o pinturas costosas que afectan a la respuesta o animación.  | Evite la pintura, promueva los elementos que se mueven a su propia capa, use transformaciones y opacidad.  <!--Navigate to [Simplify paint complexity and reduce paint areas][WebFundamentalsPerformanceRenderingSimplifyPaintComplexity].  -->  |  
| Explosiones de capas que afectan a animaciones.  | La sobrepromoción de demasiados elementos afecta en gran medida `translateZ(0)` al rendimiento de la animación.  | Promover a las capas con moderación y solo cuando sepa que ofrece mejoras tangibles.  <!--Navigate to [Stick to composite-only properties and manage layer count][WebFundamentalsPerformanceRenderingCompositorOnlyProperties].  -->  |  

<!--todo: add Simplify paint complexity and reduce paint areas section when available  -->  
<!--todo: add Stick to compositor-only properties and manage layer count section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

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
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/index) se encuentra aquí y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) y [Meggin Kearney][MegginKearney] \(Tech Writer\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  

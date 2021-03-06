---
description: Obtenga información sobre cómo evaluar el rendimiento del tiempo de ejecución en Microsoft Edge DevTools.
title: Introducción al análisis del rendimiento en tiempo de ejecución
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 074c112b99abb4689cac2274338f2276bc46b4ae
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398724"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="get-started-with-analyzing-runtime-performance"></a>Introducción al análisis del rendimiento en tiempo de ejecución  

> [!NOTE]
> Para obtener información sobre cómo hacer que las páginas se carguen más rápido, vaya a [Optimizar la velocidad del sitio web][DevtoolsSpeedGetStarted].  

El rendimiento en tiempo de ejecución es el rendimiento de la página cuando se ejecuta, en lugar de cargarse.  El siguiente artículo tutorial le enseña a usar el panel Rendimiento de Microsoft Edge DevTools para analizar el rendimiento en tiempo de ejecución.  En cuanto al modelo **RAIL,** las habilidades que aprendas en este tutorial son útiles para analizar las fases respuesta, animación e inactividad de la página.  

<!--todo: add rail link when section is ready -->  

## <a name="get-started"></a>Introducción  

En el siguiente tutorial, abra DevTools en una página en directo y use el **panel** Rendimiento para encontrar un cuello de botella de rendimiento en la página.  

1.  Abra Microsoft Edge en **modo InPrivate**.  El modo InPrivate garantiza que Microsoft Edge se ejecute en un estado limpio.  Por ejemplo, si tiene muchas extensiones instaladas, las extensiones pueden crear ruido en las medidas de rendimiento.  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  Cargue la página siguiente en la ventana InPrivate.  La página es la demostración a la que se va a crear el perfil.  La página muestra un montón de pequeños iconos que se mueven hacia arriba y hacia abajo.  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  Seleccione `Control` + `Shift` + `I` \(Windows, Linux\) o `Command` + `Option` + `I` \(macOS\) para abrir DevTools.  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="La demostración a la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       La demostración a la izquierda y DevTools a la derecha  
    :::image-end:::  
    
    > [!NOTE]
    > Para el resto de las figuras, DevTools se desacopla a una ventana [independiente][DevtoolsCustomizePlacement] para centrarse mejor en el contenido.  
    
### <a name="simulate-a-mobile-cpu"></a>Simular una CPU móvil  

Los dispositivos móviles tienen mucha menos potencia de CPU que los equipos de escritorio y portátiles.  Siempre que perfiles una página, usa la limitación de CPU para simular el rendimiento de la página en dispositivos móviles.  

1.  En DevTools, elija la **herramienta** Rendimiento.  
1.  Asegúrese de que la casilla **Capturas de pantalla** está habilitada.  
1.  Elija **Configuración de captura** \(![ Configuración de captura][ImageCaptureSettingsIcon]\).  DevTools muestra la configuración relacionada con la forma en que captura las métricas de rendimiento.  
1.  Para **CPU,** elija **4x slowdown**.  DevTools limita la CPU para que sea 4 veces más lenta de lo habitual.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="Limitación de CPU" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       Limitación de CPU  
    :::image-end:::  
    
    > [!NOTE]
    > Al probar otras páginas; si desea asegurarse de que cada página funciona bien en dispositivos móviles de gama baja, establezca la limitación de CPU en **6x de ralentización.**  La demostración no funciona bien con una ralentización de 6x, por lo que solo usa 4x de ralentización para fines informativos.  
    
### <a name="set-up-the-demo"></a>Configurar la demostración  

Es difícil crear una demostración de rendimiento en tiempo de ejecución que funcione de forma coherente para todos los lectores del sitio web.  La siguiente sección te permite personalizar la demostración para asegurarte de que tu experiencia sea relativamente coherente con las capturas de pantalla y las descripciones, independientemente de tu configuración en particular.

1.  Elija el **botón Agregar 10** hasta que los iconos azules se muevan de forma notablemente más lenta que antes.  En una máquina de gama alta, puede elegirla unas 20 veces.  
1.  Elija **Optimizar**.  Los iconos azules deben moverse más rápido y sin problemas.  
    
    > [!NOTE]
    > Para mostrar mejor una diferencia entre las versiones optimizadas y las no optimizadas, elija el botón **Restar 10** unas cuantas veces e inténtelo de nuevo.  
    > Si agrega demasiados iconos azules, puede que la CPU sea máxima y, a continuación, puede que no observe una diferencia importante en los resultados de las dos versiones.  
    
1.  Elija **Un-Optimize**.  Los iconos azules se mueven más lentos y con más lentitud de nuevo.  
    
### <a name="record-runtime-performance"></a>Rendimiento del tiempo de ejecución de registro  

Cuando se ejecutó la versión optimizada de la página, los iconos azules se mueven más rápido.  ¿Por qué?  Se supone que ambas versiones mueven los iconos la misma cantidad de espacio en la misma cantidad de tiempo.  Haga una grabación en el panel Rendimiento para obtener información sobre cómo detectar el cuello de botella de rendimiento en la versión no optimizada.  

1.  En DevTools, elija **Record** \(![ Record][ImageRecordIcon]\).  DevTools captura métricas de rendimiento a medida que se ejecuta la página.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Perfil de la página" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       Perfil de la página  
    :::image-end:::  
    
1.  Espere unos segundos.  
1.  Elija **Detener**.  DevTools deja de grabar, procesa los datos y, a continuación, muestra los resultados en el panel Rendimiento.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Los resultados del perfil" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       Los resultados del perfil  
    :::image-end:::  
    
Wow, es una cantidad abrumadora de datos.  no se preocupe, pronto el proceso tiene más sentido.  

## <a name="analyze-the-results"></a>Analizar los resultados  

Después de registrar el rendimiento de la página, mida la calidad del rendimiento de la página y busque las causas.  

### <a name="analyze-frames-per-second"></a>Analizar fotogramas por segundo  

La métrica principal para medir el rendimiento de cualquier animación es fotogramas por segundo \(FPS\).  Los usuarios están contentos cuando las animaciones se ejecutan a 60 FPS.  

1.  Revise el **gráfico FPS.**  Cada vez que se muestra una barra roja encima de **FPS,** significa que la velocidad de fotogramas se ha reducido tan bajo que probablemente está dañando la experiencia del usuario.  En general, cuanto mayor sea la barra verde, mayor será el FPS.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="Gráfico de FPS" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       Gráfico **de FPS**  
    :::image-end:::  
    
1.  Debajo del **gráfico FPS,** se muestra el gráfico **de CPU.**  Los colores del gráfico **de CPU** corresponden a los colores del **panel** Resumen, en la parte inferior del panel Rendimiento.  El hecho de que el **gráfico de CPU** esté lleno de color significa que la CPU se ha maximizado durante la grabación.  Cada vez que la CPU se ha maximizado durante períodos largos, es un indicador de que debe encontrar formas de hacer menos trabajo.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="Gráfico de CPU y panel Resumen" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       Gráfico **de CPU** y panel **Resumen**  
    :::image-end:::  
    
1.  Mantenga el mouse en **los gráficos FPS,** **CPU**o **NET.**  DevTools muestra una captura de pantalla de la página en ese momento.  Mueva el mouse a la izquierda y a la derecha para reproducir la grabación.  La acción se hace referencia como depuración y resulta útil para analizar manualmente la progresión de las animaciones.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Ver una captura de pantalla de la página alrededor de la marca de 2500 ms de la grabación" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       Ver una captura de pantalla de la página alrededor de la marca de 2500 ms de la grabación  
    :::image-end:::  
    
1.  En la **sección** Marcos, mantenga el mouse en uno de los cuadrados verdes.  DevTools muestra los FPS de ese fotograma en particular.  Cada fotograma probablemente esté muy por debajo del objetivo de 60 FPS.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Mantener el mouse en un marco" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       Mantener el mouse en un marco  
    :::image-end:::  
    
Por supuesto, la pantalla indica que la página web no está funcionando bien.  Pero en escenarios reales, puede que no sea tan claro, por lo que tener todas las herramientas para realizar mediciones resulta útil.  

#### <a name="bonus-open-the-fps-meter"></a>Bonificación: abrir el contador de FPS  

Otra herramienta práctica es el medidor fps, que proporciona estimaciones en tiempo real de FPS a medida que se ejecuta la página.  

1.  Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para abrir el **menú de comandos**.  
1.  Empiece a `Rendering` escribir en el menú **comando** y elija **Mostrar representación**.  
1.  En la **herramienta De representación,** habilite **Fps Meter**.  Aparece una nueva superposición en la parte superior derecha de la ventanilla.  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="El medidor fps" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       El **medidor fps**  
        :::image-end:::  
    
1.  Desactiva el **fps meter** y selecciona para cerrar la herramienta `Escape` **de** representación.  No estás usando **fps meter** en este tutorial.  
    
### <a name="find-the-bottleneck"></a>Buscar el cuello de botella  

Después de medir y comprobar que la animación no funciona bien, el siguiente paso es responder a la pregunta "¿por qué?".  

1.  Cuando no se elige ningún evento, el panel **Resumen** muestra un desglose de la actividad.  La página pasó la mayor parte del tiempo en representarse.  Dado que el rendimiento es el arte de hacer menos trabajo, el objetivo es reducir la cantidad de tiempo dedicado a realizar el trabajo de representación.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="El panel Resumen" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       El **panel Resumen**  
    :::image-end:::  
    
1.  Expanda la **sección** Principal.  DevTools muestra un gráfico de actividad de llama en el subproceso principal, con el tiempo.  El eje X representa la grabación, con el tiempo.  Cada barra representa un evento.  Una barra más ancha significa que el evento tardó más tiempo.  El eje Y representa la pila de llamadas.  Cuando los eventos se apilan entre sí, significa que los eventos superiores provocaron los eventos inferiores.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="Sección Principal" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       Sección **** Principal  
    :::image-end:::  
    
1.  Hay una gran cantidad de datos en la grabación.  Para acercar un solo evento; elija, mantenga y arrastre el cursor sobre overview **,** que es la sección que incluye los gráficos **FPS,** **CPU**y **NET.**  La **sección** Principal y el panel **Resumen** solo muestran información para la parte elegida de la grabación.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Acercar un evento" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       Acercar un evento  
    :::image-end:::  
    
    > [!NOTE]
    > Otra forma de acercar, centrar la **sección Principal,** elegir el fondo o un evento y seleccionar `W` , , o `A` `S` `D` .  
    
    1.  Céntrate en el triángulo rojo de la parte superior derecha del evento Fotograma de animación **desencadenado.**  Cada vez que se muestra un triángulo rojo, es una advertencia de que puede haber un problema relacionado con el evento.  
    
    > [!NOTE]
    > El **evento Animation Frame Fired** se produce siempre que se ejecuta una [ `requestAnimationFrame()` devolución][MDNWebRequestAnimationFrame] de llamada.  
    
1.  Elija el **evento Fotograma de** animación desencadenado.  El **panel Resumen** ahora muestra información sobre ese evento.  Tenga en cuenta **el vínculo** Revelar.  Después de elegirla, DevTools resaltará el evento que inició el **evento Animation Frame Fired.**  Además, céntrate en **el vínculoapp.js:95.**  Después de elegirla, se muestra la línea relevante en el código fuente.
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Más información sobre el evento Animation Frame Fired" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       Más información sobre el evento **Animation Frame Fired**  
    :::image-end:::  
    
    > [!NOTE]
    > Después de elegir un evento, usa las teclas de flecha para seleccionar los eventos junto a él.  
    
1.  En el **evento app.update,** hay un montón de eventos púrpura.  Si cada evento púrpura era más ancho, parece que cada uno puede tener un triángulo rojo.  
1.  Elija uno de los eventos **layout púrpura.**  DevTools proporciona más información sobre el evento en el panel **Resumen.**  De hecho, hay una advertencia sobre los flujos forzados \(otra palabra para layout\).  
    
1.  En el **panel** Resumen, elija el ** vínculoapp.js:71** en **Diseño forzado**.  DevTools te lleva a la línea de código que forzó el diseño.  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="La línea de código que provocó el diseño forzado" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       La línea de código que provocó el diseño forzado  
    :::image-end:::  
    
    > [!NOTE]
    > El problema con el código es que, en cada fotograma de animación, cambia el estilo de cada icono y, a continuación, consulta la posición de cada icono en la página.  Dado que los estilos cambiaron, el explorador no sabe si cada posición de icono cambió, por lo que debe volver a diseño el icono para calcular la nueva posición.  <!--  > To learn more, navigate to [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts].  -->
    
<!-- todo: add layouts section when available -->

Eso era mucho que aprender.  Ahora tiene una base sólida en el flujo de trabajo básico para analizar el rendimiento en tiempo de ejecución.  Buen trabajo.  

### <a name="bonus-analyze-the-optimized-version"></a>Bonus: Analizar la versión optimizada  

Con los flujos de trabajo y las herramientas que acaba de aprender, elija **Optimizar** en la demostración para habilitar el código optimizado, realizar otra grabación de rendimiento y, a continuación, analizar los resultados.  Desde la velocidad de fotogramas mejorada hasta la **** reducción de eventos en el gráfico de llamas en la sección Principal, la versión optimizada de la aplicación hace mucho menos trabajo, lo que resulta en un mejor rendimiento.  

> [!NOTE]
> Incluso la versión optimizada no es excelente, ya que manipula la `top` propiedad de cada icono.  Un enfoque mejor es seguir las propiedades que solo afectan a la composición.  <!--  > For more information, navigate to [Use transform and opacity changes for animations][RenderingCompositor].  -->  

<!--todo: add rendering section when available -->

## <a name="next-steps"></a>Pasos siguientes

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
To learn more, navigate to [Measure Performance With The RAIL Model][RAIL].  -->  

Para sentirse más cómodo con la **herramienta Rendimiento,** la práctica hace que sea perfecto.  Intente generar perfiles de las páginas y analizar los resultados.  Si tienes alguna pregunta sobre los **** resultados, usa el icono Enviar comentarios, selecciona `Alt` + `Shift` + `I` \(Windows, Linux\), `Option` + `Shift` + `I` selecciona \(macOS\) o [tuitea][TwitterEdgeDevtools]el equipo de DevTools .  Incluya capturas de pantalla o vínculos a páginas reproducibles, si es posible.  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="El icono **Comentarios** en Microsoft Edge DevTools" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   El **icono Enviar comentarios** en Microsoft Edge DevTools  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

Por último, hay muchas formas de mejorar el rendimiento en tiempo de ejecución.  Este artículo se ha centrado en un cuello de botella de animación determinado para ofrecerte un recorrido centrado a través del panel Rendimiento, pero solo es uno de los muchos cuellos de botella que puedes encontrar.  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Cambiar la ubicación de Microsoft Edge DevTools (desacoplar, acoplar a abajo, acoplar a la izquierda)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimizar la velocidad del sitio web con Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools: publicar un mensaje de | Twitter"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window.requestAnimationFrame\(\) | MDN"  

<!--[InPrivate]: https://support.microsoft.com/help/4026200/microsoft-edge-browse-inprivate "Browse InPrivate in Microsoft Edge"  -->

<!--[FrameAnatomy]: https://aerotwist.com/blog/the-anatomy-of-a-frame  -->  

<!--[RAIL]: /web/fundamentals/performance/rail  -->  
<!--[RenderingAvoidSynchronousLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing#avoid_forced_synchronous_layouts  -->  
<!--[RenderingAvoidThrashing]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing  -->  
<!--[RenderingCompositor]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count#use_transform_and_opacity_changes_for_animations  -->  
<!--[RenderingDebounceInputs]: /web/fundamentals/performance/rendering/debounce-your-input-handlers  -->
<!--[RenderingManageLayers]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count  -->  
<!--[RenderingOptimizeJS]: /web/fundamentals/performance/rendering/optimize-javascript-execution  -->  
<!--[RenderingPerformance]: /web/fundamentals/performance/rendering  -->  
<!--[RenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations  -->  
<!--[RenderingSimplifyPaint]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas  -->  

<!--[StackOverflowAlphabetBrowserDevtools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser - Stack Overflow"  -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

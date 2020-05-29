---
title: Empezar a analizar el rendimiento en tiempo de ejecución
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: bff2d2fb0ff8424303289183ca8c5935ef477381
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611744"
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







# Empezar a analizar el rendimiento en tiempo de ejecución   



> [!NOTE]
> Consulte [optimizar la velocidad del sitio web][DevtoolsSpeedGetStarted] para obtener más información sobre cómo hacer que las páginas se carguen más rápido.  

El rendimiento en tiempo de ejecución es el funcionamiento de la página cuando se está ejecutando, en lugar de cargarlo.  Este tutorial le enseña a usar el panel de rendimiento de Microsoft Edge DevTools para analizar el rendimiento en tiempo de ejecución.  En cuanto al modelo de **raíl** , las habilidades que aprende en este tutorial son útiles para analizar la respuesta, la animación y las fases inactivas de la página.  

<!--todo: add rail link when section is ready -->  

## Comenzar   

En este tutorial, abre DevTools en una página en vivo y usa el panel rendimiento para encontrar un cuello de botella de rendimiento en la página.  

1.  Abre Microsoft Edge en **modo InPrivate**.  El modo InPrivate garantiza que Microsoft Edge se ejecuta en un estado limpio.  Por ejemplo, si tiene una gran cantidad de extensiones instaladas, esas extensiones podrían crear ruido en las medidas de rendimiento.  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  Cargue la siguiente página en la ventana InPrivate.  Esta es la demostración que te va a perfilar.  La página muestra una serie de pequeños iconos moviéndose hacia arriba y hacia abajo.  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/jank/
    ```  
    
1.  Pulse `Control` + `Shift` + `I` \ (Windows \) o `Command` + `Option` + `I` \ (MacOS \) para abrir DevTools.  
    
    > ###### Figura 1  
    > La demostración de la izquierda y DevTools a la derecha  
    > ![La demostración de la izquierda y DevTools a la derecha][ImageGetStarted]  
    
    > [!NOTE]
    > Para el resto de las capturas de pantalla, DevTools se [desacopla en una ventana independiente][DevtoolsCustomizePlacement] para que puedas ver mejor el contenido.  
    
### Simular una CPU móvil  

Los dispositivos móviles tienen mucha menos energía de CPU que los equipos de escritorio y portátiles.  Cada vez que perfile una página, use el límite de CPU para simular cómo se ejecuta la página en dispositivos móviles.  

1.  En DevTools, haga clic en la pestaña **rendimiento** .  
1.  Asegúrese de que la casilla **capturas de pantallas** esté habilitada.  
1.  Haga clic en **capturar** configuración de ![ captura ][ImageCaptureSettingsIcon] .  DevTools revela la configuración relacionada con el modo en que captura las métricas de rendimiento.  
1.  En **CPU**, seleccione **deceleración 4**.  DevTools acelera tu CPU para que sea cuatro veces más lenta de lo normal.  
    
    > ###### Figura 2  
    > Límite de CPU  
    > ![Límite de CPU][ImageCPUThrottling]  
    
    > [!NOTE]
    > Cuando pruebe otras páginas, si desea asegurarse de que funcionan bien en dispositivos móviles de low-end, establezca el límite de CPU en **6X lentitud**.  Esta demostración no funciona bien con una ralentización de 6 veces, por lo que solo usa una ralentización 4x para fines instructivos.  
    
### Configurar la demostración  

Es difícil crear una demostración de rendimiento de tiempo de ejecución que funcione de forma coherente en todos los lectores de este sitio Web.  Esta sección le permite personalizar la demostración para asegurarse de que su experiencia es relativamente coherente con las capturas de pantallas y descripciones que se observan en este tutorial, independientemente de su configuración particular.

1.  Siga haciendo clic en **Agregar 10** hasta que los iconos azules se muevan notablemente más lento que antes.  En un equipo de gama alta, puede demorar unos 20 clics.  
1.  Haga clic en **optimizar**.  Los iconos azules deberían moverse más rápido y de forma más sencilla.  

    > [!NOTE]
    > Si no ve una diferencia notable entre las versiones optimizada y no optimizada, pruebe a hacer clic en **restar 10** varias veces e inténtelo de nuevo.  
    > Si agrega demasiados iconos azules, simplemente va a maximizar la CPU y no va a ver una diferencia importante en los resultados de las dos versiones.  

1.  Haga clic en **quitar la optimización**.  Los iconos azules se mueven más lentamente y con más Jank de nuevo.  

### Registrar el rendimiento en tiempo de ejecución   

Cuando ejecutó la versión optimizada de la página, los iconos azules se mueven más rápido.  
¿Por qué?  Se supone que ambas versiones mueven los iconos con la misma cantidad de espacio en la misma cantidad de tiempo.  Realice una grabación en el panel rendimiento para obtener información sobre cómo detectar el cuello de botella de rendimiento en la versión no optimizada.  

1.  En DevTools **, haga clic en grabar** ![ Registro ][ImageRecordIcon] .  
    DevTools captura métricas de rendimiento a medida que se ejecuta la página.  
    
    > ###### Imagen 3 
    > Perfilar la página  
    > ![Perfilar la página][ImagePageProfiling]  
    
1.  Espere unos segundos.  
1.  Haga clic en **detener**.  DevTools detiene la grabación, procesa los datos y, a continuación, muestra los resultados en el panel rendimiento.  
    
    > ###### Imagen 4  
    > Los resultados del perfil  
    > ![Los resultados del perfil][ImageProfileResults]  

Wow, eso es una cantidad abrumadora de datos.  No te preocupes, pronto hará más sentido.  

## Analizar los resultados   

Una vez que haya realizado una grabación del rendimiento de la página, puede medir cuál es el rendimiento de la página y encontrar las causas.  

### Analizar fotogramas por segundo  

La métrica principal para medir el rendimiento de cualquier animación es fotogramas por segundo \ (FPS \).  Los usuarios están satisfechos cuando las animaciones se ejecutan a 60 FPS.  

1.  Fíjese en el gráfico de **fps** .  Cada vez que vea una barra roja encima de **fps**, significa que la velocidad de la fotogramas se ha colocado tan poco que es probable que dañe la experiencia del usuario.  En general, cuanto más alto sea la barra verde, mayor será el valor de FPS.  
    
    > ###### Imagen 5  
    > El gráfico de FPS  
    > ![El gráfico de FPS][ImageFPSChart]  

1.  Debajo del gráfico de **fps** , verá el gráfico de **CPU** .  Los colores del gráfico de la **CPU** se corresponden con los colores de la pestaña **Resumen** , en la parte inferior del panel rendimiento.  El hecho de que el gráfico de la **CPU** esté lleno de color significa que la CPU se ha agotado durante el tiempo de grabación.  Cada vez que se agote la CPU durante períodos prolongados, es una señal para encontrar formas de realizar menos trabajo.  
    
    > ###### Imagen 6  
    > Pestaña gráfico de CPU y Resumen  
    > ![Pestaña gráfico de CPU y Resumen][ImageCPUSummary]  

1.  Mantenga el mouse sobre los gráficos de **fps**, **CPU**o **net** .  DevTools muestra una captura de pantalla de la página en ese momento.  Mueva el mouse hacia la izquierda y la derecha para reproducir la grabación.  Esto se conoce como limpieza y es útil para analizar manualmente el avance de las animaciones.  
    
    > ###### Imagen 7  
    > Ver una captura de pantalla de la página en la 2500ms marca de la grabación  
    > ![Ver una captura de pantalla de la página en la 2500ms marca de la grabación][ImageViewingScreenshot]  

1.  En la sección **Marcos** , sitúe el mouse sobre uno de los cuadrados verdes.  DevTools muestra los FPS para ese fotograma en particular.  Es probable que cada fotograma sea muy bajo el objetivo de 60 FPS.  
    
    > ###### Imagen 8  
    > Mantener el puntero sobre un marco  
    > ![Mantener el puntero sobre un marco][ImageFrameHover]  

Por supuesto, con esta demostración es bastante obvio que la página no funciona correctamente.  Pero en escenarios reales es posible que no esté tan claro, así que tener todas estas herramientas para hacer que las medidas sean útiles.  

#### Bonificación: abrir el medidor de FPS  

Otra herramienta útil es el medidor de FPS, que proporciona estimaciones en tiempo real para FPS a medida que se ejecuta la página.  

1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.  
1.  Empiece `Rendering` a escribir en el menú de comandos y seleccione **Mostrar procesamiento**.  
1.  En la pestaña **representación** , habilita el **medidor de fps**.  Aparece una nueva superposición en la parte superior derecha de la ventanilla.  
    
    > ###### Imagen 9  
    > El medidor de FPS  
    > ![El medidor de FPS][ImageFPSMeter]  

1.  Deshabilite el **medidor de fps** y pulse `Escape` para cerrar la pestaña **representación** .  No lo usaremos en este tutorial.  

### Encontrar el cuello de botella  

Ahora que ya ha medido y verificado que la animación no se realiza correctamente, la siguiente pregunta que debe responder es: ¿por qué?  

1.  Observe la pestaña Resumen.  Cuando no se selecciona ningún evento, en esta pestaña se muestra un desglose de la actividad.  La página dedicó la mayor parte de su tiempo de procesamiento.  Puesto que el rendimiento es el arte de hacer menos trabajo, su objetivo es reducir la cantidad de tiempo dedicado al trabajo de representación.  
    
    > ###### Imagen 10  
    > La pestaña Resumen  
    > ![La pestaña Resumen][ImageSummaryTab]  

1.  Expanda la sección **principal** .  DevTools muestra un gráfico de llamas de la actividad en el hilo principal, a lo largo del tiempo.  El eje x representa la grabación, a lo largo del tiempo.  Cada barra representa un evento.  Una barra más ancha significa que el evento ha tardado más tiempo.  El eje y representa la pila de llamadas.  Cuando ve eventos apilados unos sobre otros, significa que los eventos superiores provocan los eventos menores.  
    
    > ##### Imagen 11  
    > La sección principal  
    > ![La sección principal][ImageMainSection]  

1.  Hay una gran cantidad de datos en la grabación.  Para acercar un solo evento, haga clic, mantenga presionado y arrastre el mouse sobre la **información general**, que es la sección que incluye los gráficos de **fps**, **CPU**y **net** .  En la sección **principal** y en la pestaña **Resumen** solo se muestra información de la parte seleccionada de la grabación.  
    
    > ###### Imagen 12  
    > Acercar un solo evento  
    > ![Acercar un evento][ImageZoomedAnimation]  
    
    > [!NOTE]
    > Otra forma de acercar la vista es resaltar la sección **principal** haciendo clic en el fondo o seleccionando un evento y, a continuación, presionando las `W` teclas,, `A` `S` y `D` .  
    
    1.  Ten en cuenta que el triángulo rojo de la parte superior derecha del **fotograma de animación desencadenado** .  Siempre que vea un triángulo rojo, es una advertencia que puede haber un problema relacionado con este evento.  
    
    > [!NOTE]
    > El evento de **marco de animación desencadenado** se produce cada vez que se ejecuta una [ `requestAnimationFrame()` devolución de llamada][MDNWebRequestAnimationFrame] .  
    
1.  Haga clic en el evento de **marco de animación desencadenado** .  La pestaña **Resumen** ahora muestra información sobre el evento.  Observe el vínculo **Mostrar** .  Al hacer clic, se resalta el evento que inició el evento de **fotograma de animación desencadenado** .  Observe también el vínculo **app. js: 95** .  Haga clic en para ir a la línea correspondiente en el código fuente.
    
    > ##### Imagen 13  
    > Más información sobre el evento de marco de animación desencadenado  
    > ![Más información sobre el evento de marco de animación desencadenado][ImageAnimationFrameFired]  
    
    > [!NOTE]
    > Después de seleccionar un evento, use las teclas de dirección para seleccionar los eventos que hay junto a él.  

1.  En el evento **app. Update** , hay un montón de eventos púrpura.  Si fuesen más anchos, parece que cada uno de ellos puede tener un triángulo rojo.  Haga clic en uno de los eventos de **diseño** morados ahora.  DevTools proporciona más información sobre el evento en la pestaña **Resumen** .  De hecho, hay una advertencia sobre los reflujos forzados \ (otra palabra para el diseño \).  

1.  En la pestaña **Resumen** , haga clic en el vínculo **app. js: 71** del **diseño forzado**.  DevTools le lleva a la línea de código que forzó el diseño.  
    
    > ##### Imagen 14  
    > La línea de código que causó el diseño forzado  
    > ![La línea de código que causó el diseño forzado][ImageForcedLayoutSRC]  
    
    > [!NOTE]
    > El problema con este código es que, en cada marco de animación, cambia el estilo de cada icono y, después, consulta la posición de cada icono de la página.  Como los estilos han cambiado, el explorador no sabe si cada posición de icono ha cambiado, por lo que tiene que volver a distribuir el icono para calcular su posición.  <!--  See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->

<!-- todo: add layouts section when available -->

Phew!  Eso fue mucho para llevarlo, pero ahora tiene una base sólida en el flujo de trabajo básico para analizar el rendimiento en tiempo de ejecución.  Buen trabajo.  

### Bonificación: analizar la versión optimizada  

Con los flujos de trabajo y las herramientas que acaba de aprender, haga clic en **optimizar** en la demostración para habilitar el código optimizado, realice otra grabación de rendimiento y, a continuación, analice los resultados.  Desde la velocidad de fotogramas mejorada hasta la reducción en eventos en el gráfico de llamas de la sección **principal** , puede ver que la versión optimizada de la aplicación hace mucho menos trabajo, lo que da como resultado un mejor rendimiento.  

> [!NOTE]
> Incluso esta versión "optimizada" no es tan buena, ya que sigue manipulando la `top` propiedad de cada icono.  Un mejor enfoque es ceñirse a las propiedades que solo afectan a la composición.  
<!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## Pasos siguientes

<!--The foundation for understanding performance is the RAIL model.  This model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

Para estar más familiarizado con el panel rendimiento, la práctica es ideal.  Pruebe a generar perfiles de sus propias páginas y analizar los resultados.  Si tiene alguna pregunta sobre los resultados, use el icono de **comentarios** , pulse `Alt`  +  `Shift`  +  `I` en Windows ( `Option`  +  `Shift`  +  `I` en MacOS) o en [Tweet][TwitterEdgeDevtools].  Incluya capturas de pantallas o vínculos a páginas reproducibles, si es posible.

> ##### Imagen 15
> El icono de **comentarios** en el DevTools de Microsoft Edge  
> ![El icono * * comentarios * * en Microsoft Edge DevTools][ImageFeedbackIcon]

<!-- To really master runtime performance, you've got to learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

Por último, hay muchas maneras de mejorar el rendimiento en tiempo de ejecución.  Este tutorial se centró en un cuello de botella de animación para darle un recorrido centrado en el panel rendimiento, pero es solo uno de los muchos cuellos de botella que puede encontrar.  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  

[ImageGetStarted]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-get-started-side-by-side.msft.png "Ilustración 1: la demostración de la izquierda y DevTools a la derecha"  
[ImageCPUThrottling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings.msft.png "Ilustración 2: límite de CPU"  
[ImagePageProfiling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-profiling.msft.png "Ilustración 3: generación de perfiles de la página"  
[ImageProfileResults]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-results.msft.png "Ilustración 4: los resultados del perfil"  
[ImageFPSChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-chart.msft.png "Ilustración 5: gráfico de FPS"  
[ImageCPUSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-cpu-chart.msft.png "Ilustración 6: el gráfico de la CPU y la pestaña Resumen, resaltados en azul"  
[ImageViewingScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshot-hover.msft.png "Ilustración 7: ver una captura de pantalla de la página en la 2500ms marca de la grabación"  
[ImageFrameHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frame-hover.msft.png "Ilustración 8: mantener el puntero sobre un marco"  
[ImageFPSMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-fps-meter-overlay.msft.png "Ilustración 9: el medidor de FPS"  
[ImageSummaryTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-tab.msft.png "Ilustración 10: la pestaña Resumen"  
[ImageMainSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main.msft.png "Ilustración 11: la sección principal"  
[ImageZoomedAnimation]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Ilustración 12: zoom en un único marco de animación que se desencadena evento"  
[ImageAnimationFrameFired]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-animation-frame-fired.msft.png "Ilustración 13: más información sobre el evento de marco de animación desencadenado"  
[ImageForcedLayoutSRC]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-sources-app-update.msft.png "Ilustración 14: la línea de código que causó el diseño forzado"  
[ImageFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-feedback-icon.msft.png "Ilustración 15: el icono * * comentarios * * en Microsoft Edge DevTools"

<!-- links -->

[DevtoolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Optimizar la velocidad del sitio web con Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools: envía un tweet | Twitter"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window. requestAnimationFrame \ (\) | MDN"  

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
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

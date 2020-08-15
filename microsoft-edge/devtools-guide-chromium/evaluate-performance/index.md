---
title: Empezar a analizar el rendimiento en tiempo de ejecución
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 94753c7024c2f4f4c96d560c815d310b1f9643a1
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931192"
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
> Para obtener más información sobre cómo hacer que las páginas se carguen más rápido, consulte [optimizar la velocidad del sitio web][DevtoolsSpeedGetStarted].  

El rendimiento en tiempo de ejecución es el funcionamiento de la página cuando se está ejecutando, en lugar de cargarlo.  En el siguiente artículo de tutorial aprenderá a usar el panel de rendimiento de Microsoft Edge DevTools para analizar el rendimiento en tiempo de ejecución.  En cuanto al modelo de **raíl** , las habilidades que aprende en este tutorial son útiles para analizar la respuesta, la animación y las fases inactivas de la página.  

<!--todo: add rail link when section is ready -->  

## Comenzar  

En el siguiente tutorial, abra DevTools en una página en vivo y use el panel **rendimiento** para encontrar un cuello de botella de rendimiento en la página.  

1.  Abre Microsoft Edge en **modo InPrivate**.  El modo InPrivate garantiza que Microsoft Edge se ejecuta en un estado limpio.  Por ejemplo, si tiene una gran cantidad de extensiones instaladas, las extensiones pueden crear ruido en las medidas de rendimiento.  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  Cargue la siguiente página en la ventana InPrivate.  La página es la demostración que va a perfilar.  La página muestra una serie de pequeños iconos moviéndose hacia arriba y hacia abajo.  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  Seleccione `Control` + `Shift` + `I` \ (Windows \) o `Command` + `Option` + `I` \ (MacOS \) para abrir DevTools.  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="La demostración de la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       La demostración de la izquierda y DevTools a la derecha  
    :::image-end:::  
    
    > [!NOTE]
    > Para el resto de las figuras, DevTools se [desacopla en una ventana independiente][DevtoolsCustomizePlacement] para centrarse mejor en el contenido.  
    
### Simular una CPU móvil  

Los dispositivos móviles tienen mucha menos energía de CPU que los equipos de escritorio y portátiles.  Cada vez que perfile una página, use el límite de CPU para simular cómo se ejecuta la página en dispositivos móviles.  

1.  En DevTools, elija la pestaña **rendimiento** .  
1.  Asegúrese de que la casilla **capturas de pantallas** esté habilitada.  
1.  Elija **configuración de captura** \ (! [ Configuración de capturas] [ImageCaptureSettingsIcon] \).  DevTools revela la configuración relacionada con el modo en que captura las métricas de rendimiento.  
1.  En **CPU**, seleccione **deceleración 4**.  DevTools acelera tu CPU para que sea cuatro veces más lenta de lo normal.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="Limitación de CPU" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       Limitación de CPU  
    :::image-end:::  
    
    > [!NOTE]
    > Al probar otras páginas; Si quiere asegurarse de que cada página funciona correctamente en dispositivos móviles de low-end, establezca el límite de CPU en **6X lentitud**.  La demostración no funciona bien con una ralentización de 6 veces, por lo que solo usa una ralentización 4x para fines instructivos.  
    
### Configurar la demostración  

Es difícil crear una demostración de rendimiento de tiempo de ejecución que funcione de forma coherente en todos los lectores del sitio Web.  La siguiente sección le permite personalizar la demostración para asegurarse de que su experiencia es relativamente coherente con las capturas de pantallas y las descripciones, independientemente de su configuración particular.

1.  Elija el botón **Agregar 10** hasta que los iconos azules se muevan notablemente más lentos que antes.  En un equipo de gama alta, puedes elegirlo aproximadamente 20 veces.  
1.  Elija **optimizar**.  Los iconos azules deberían moverse más rápido y de forma más sencilla.  
    
    > [!NOTE]
    > Para mostrar mejor una diferencia entre las versiones optimizada y no optimizada, elija el botón **restar 10** varias veces e inténtelo de nuevo.  
    > Si agrega demasiados iconos azules, puede maximizar la CPU y, a continuación, no puede observar una diferencia importante en los resultados de las dos versiones.  
    
1.  Elija **desoptimizar**.  Los iconos azules se mueven más lentamente y con más lentitud.  
    
### Registrar el rendimiento en tiempo de ejecución  

Cuando ejecutó la versión optimizada de la página, los iconos azules se mueven más rápido.  ¿Por qué?  Se supone que ambas versiones mueven los iconos con la misma cantidad de espacio en la misma cantidad de tiempo.  Realice una grabación en el panel rendimiento para obtener información sobre cómo detectar el cuello de botella de rendimiento en la versión no optimizada.  

1.  En DevTools, elija **grabar** \ (! [ Record] [ImageRecordIcon] \).  DevTools captura métricas de rendimiento a medida que se ejecuta la página.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Perfilar la página" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       Perfilar la página  
    :::image-end:::  
    
1.  Espere unos segundos.  
1.  Elija **detener**.  DevTools detiene la grabación, procesa los datos y, a continuación, muestra los resultados en el panel rendimiento.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Los resultados del perfil" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       Los resultados del perfil  
    :::image-end:::  
    
Wow, eso es una cantidad abrumadora de datos.  no se preocupe, pronto el proceso tiene más sentido.  

## Analizar los resultados  

Después de grabar el rendimiento de la página, mida la calidad del rendimiento de la página y busque las causas posibles.  

### Analizar fotogramas por segundo  

La métrica principal para medir el rendimiento de cualquier animación es fotogramas por segundo \ (FPS \).  Los usuarios están satisfechos cuando las animaciones se ejecutan a 60 FPS.  

1.  Fíjese en el gráfico de **fps** .  Cada vez que vea una barra roja encima de **fps**, significa que la velocidad de la fotogramas se ha colocado tan poco que es probable que dañe la experiencia del usuario.  En general, cuanto más alto sea la barra verde, mayor será el valor de FPS.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="El gráfico de FPS" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       El gráfico de **fps**  
    :::image-end:::  
    
1.  Debajo del gráfico de **fps** , verá el gráfico de **CPU** .  Los colores del gráfico de la **CPU** se corresponden con los colores de la pestaña **Resumen** , en la parte inferior del panel rendimiento.  El hecho de que el gráfico de la **CPU** esté lleno de color significa que la CPU se ha agotado durante el tiempo de grabación.  Cada vez que se agote la CPU durante períodos prolongados, es una señal para encontrar formas de realizar menos trabajo.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="Pestaña gráfico de CPU y Resumen" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       Pestaña gráfico de **CPU** y **Resumen**  
    :::image-end:::  
    
1.  Mantenga el mouse sobre los gráficos de **fps**, **CPU**o **net** .  DevTools muestra una captura de pantalla de la página en ese momento.  Mueva el mouse hacia la izquierda y la derecha para reproducir la grabación.  Se hace referencia a la acción como limpieza y es útil para analizar manualmente el avance de las animaciones.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Ver una captura de pantalla de la página en la marca de 2500ms de la grabación" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       Ver una captura de pantalla de la página en la marca de 2500ms de la grabación  
    :::image-end:::  
    
1.  En la sección **Marcos** , desplace el puntero sobre uno de los cuadrados verdes.  DevTools muestra los FPS para ese fotograma en particular.  Es probable que cada fotograma sea muy bajo el objetivo de 60 FPS.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Desplazar el puntero sobre un marco" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       Desplazar el puntero sobre un marco  
    :::image-end:::  
    
Por supuesto, debería ver que la página no funciona bien.  Pero en escenarios reales es posible que no esté tan claro, así que tener todas las herramientas para hacer que las medidas sean útiles.  

#### Bonificación: abrir el medidor de FPS  

Otra herramienta útil es el medidor de FPS, que proporciona estimaciones en tiempo real para FPS a medida que se ejecuta la página.  

1.  Seleccione `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.  
1.  Empiece `Rendering` a escribir en el **menú de comandos** y seleccione **Mostrar procesamiento**.  
1.  En la pestaña **representación** , habilita el **medidor de fps**.  Aparece una nueva superposición en la parte superior derecha de la ventanilla.  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="El medidor de FPS" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       El **medidor de fps**  
        :::image-end:::  
    
1.  Deshabilite el **medidor de fps** y seleccione `Escape` para cerrar la pestaña **representación** .  No usa el **medidor de fps** en este tutorial.  
    
### Encontrar el cuello de botella  

Después de medir y verificar que la animación no se realiza correctamente, el siguiente paso es responder a la pregunta "¿por qué?".  

1.  Cuando no se selecciona ningún evento, la pestaña **Resumen** muestra un desglose de actividad.  La página dedicó la mayor parte de la representación de tiempo.  Puesto que el rendimiento es el arte de hacer menos trabajo, su objetivo es reducir la cantidad de tiempo dedicado al trabajo de representación.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="La pestaña Resumen" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       La pestaña **Resumen**  
    :::image-end:::  
    
1.  Expanda la sección **principal** .  DevTools muestra un gráfico de llamas de la actividad en el hilo principal, a lo largo del tiempo.  El eje x representa la grabación, a lo largo del tiempo.  Cada barra representa un evento.  Una barra más ancha significa que el evento ha tardado más tiempo.  El eje y representa la pila de llamadas.  Cuando ve eventos apilados unos sobre otros, significa que los eventos superiores provocan los eventos menores.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="La sección principal" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       La sección **principal**  
    :::image-end:::  
    
1.  Hay una gran cantidad de datos en la grabación.  Para acercar un solo evento; Elija, mantenga presionado y arrastre el cursor sobre la **información general**, que es la sección que incluye los gráficos de **fps**, **CPU**y **net** .  En la sección **principal** y en la pestaña **Resumen** solo se muestra información de la parte seleccionada de la grabación.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Acercar un evento" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       Acercar un evento  
    :::image-end:::  
    
    > [!NOTE]
    > Otra forma de hacer zoom, centrarse en la sección **principal** , elegir el fondo o un evento, y seleccionar `W` ,, `A` `S` o `D` .  
    
    1.  Céntrese en el triángulo rojo de la parte superior derecha del **fotograma de animación desencadenado** .  Siempre que vea un triángulo rojo, es una advertencia que puede haber un problema relacionado con el evento.  
    
    > [!NOTE]
    > El evento de **marco de animación desencadenado** se produce cada vez que se ejecuta una [ `requestAnimationFrame()` devolución de llamada][MDNWebRequestAnimationFrame] .  
    
1.  Elija el evento de **fotograma de animación desencadenado** .  La pestaña **Resumen** ahora muestra información sobre el evento.  Observe el vínculo **Mostrar** .  Después de elegirlo, DevTools para resaltar el evento que inició el evento de **fotograma de animación desencadenado** .  Además, céntrese en el vínculo **app.js:95** .  Después de elegirlo, se muestra la línea correspondiente en el código fuente.
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Más información sobre el evento de marco de animación desencadenado" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       Más información sobre el evento de **marco de animación desencadenado**  
    :::image-end:::  
    
    > [!NOTE]
    > Después de seleccionar un evento, use las teclas de dirección para seleccionar los eventos que hay junto a él.  
    
1.  En el evento **app. Update** , hay un montón de eventos púrpura.  Si cada evento morado era más ancho, parece que cada uno de ellos puede tener un triángulo rojo.  
1.  Elija uno de los eventos de **diseño** púrpura.  DevTools proporciona más información sobre el evento en la pestaña **Resumen** .  De hecho, hay una advertencia sobre los reflujos forzados \ (otra palabra para el diseño \).  
    
1.  En la pestaña **Resumen** , elija el vínculo **app.js:71** en **diseño forzado**.  DevTools le lleva a la línea de código que forzó el diseño.  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="La línea de código que causó el diseño forzado" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       La línea de código que causó el diseño forzado  
    :::image-end:::  
    
    > [!NOTE]
    > El problema con el código es que, en cada marco de animación, cambia el estilo de cada icono y, después, consulta la posición de cada icono de la página.  Dado que los estilos han cambiado, el explorador no sabe si ha cambiado la posición de cada icono, por lo que tiene que volver a distribuir el icono para calcular la nueva posición.  <!--  > See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->
    
<!-- todo: add layouts section when available -->

Eso fue mucho para aprender.  Ahora tiene una base sólida en el flujo de trabajo básico para analizar el rendimiento en tiempo de ejecución.  Buen trabajo.  

### Bonificación: analizar la versión optimizada  

Usando los flujos de trabajo y las herramientas que acaba de aprender, elija **optimizar** en la demostración para habilitar el código optimizado, tomar otra grabación de rendimiento y analizar los resultados.  Desde la velocidad de fotogramas mejorada hasta la reducción en eventos en el gráfico de llamas de la sección **principal** , podrá ver que la versión optimizada de la aplicación hace mucho menos trabajo, lo que da como resultado un mejor rendimiento.  

> [!NOTE]
> Incluso la versión optimizada no es genial, porque manipula la `top` propiedad de todos los iconos.  Un mejor enfoque es ceñirse a las propiedades que solo afectan a la composición.  <!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## Pasos siguientes

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

Para estar más familiarizado con el panel rendimiento, la práctica es ideal.  Pruebe a generar perfiles de las páginas y analizar los resultados.  Si tiene preguntas sobre los resultados, use el icono para **Enviar comentarios** , seleccione `Alt` + `Shift` + `I` \ (Windows \), seleccione `Option` + `Shift` + `I` \ (MacOS \) o [Tweet el equipo de DevTools][TwitterEdgeDevtools].  Incluya capturas de pantallas o vínculos a páginas reproducibles, si es posible.  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="El icono * * comentarios * * en Microsoft Edge DevTools" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   El icono **Enviar comentarios** en el DevTools de Microsoft Edge  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

Por último, hay muchas maneras de mejorar el rendimiento en tiempo de ejecución.  Este artículo se centró en un cuello de botella de animación para darle un recorrido centrado en el panel rendimiento, pero es sólo uno de los muchos cuellos de botella que puede encontrar.  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimizar la velocidad del sitio web con Microsoft Edge DevTools"  

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

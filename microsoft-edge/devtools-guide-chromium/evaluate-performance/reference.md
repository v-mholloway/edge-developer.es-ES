---
description: Una referencia sobre todas las formas de registrar y analizar el rendimiento en Microsoft Edge DevTools.
title: Referencia de análisis de rendimiento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 0e81cb89f0e690533bdd9c8fdbfce272610be783
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992907"
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







# Referencia de análisis de rendimiento   



Esta página es una referencia completa de las características de Microsoft Edge DevTools relacionadas con el análisis del rendimiento.  

Vea [empezar a analizar el rendimiento en tiempo de ejecución][DevtoolsEvaluatePerformanceGettingStarted] para obtener un tutorial guiado sobre cómo analizar el rendimiento de una página con [Microsoft Edge DevTools][MicrosoftEdgeDevTools].  

## Registrar el rendimiento   

### Registrar el rendimiento en tiempo de ejecución   

Grabe el rendimiento en tiempo de ejecución cuando desee analizar el rendimiento de una página mientras se está ejecutando, en lugar de cargarlo.  

1.  Vaya a la página que desea analizar.  
1.  Haga clic en la pestaña **rendimiento** en DevTools.  
1.  Haga clic en **grabar** \ ( ![ grabar ][ImageRecordIcon] \).  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Grabar" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **Grabar**  
    :::image-end:::  
    
1.  Interactúe con la página.  DevTools registra toda la actividad de la página que se produce como resultado de las interacciones.  
1.  Vuelva a hacer clic en **grabar** o haga clic en **detener** para detener la grabación.  
    
### Registrar el rendimiento de la carga   

Registre el rendimiento de la carga cuando desee analizar el rendimiento de una página mientras se está cargando, en lugar de ejecutarse.  

1.  Vaya a la página que desea analizar.  
1.  Abra el panel **rendimiento** de DevTools.  
1.  Haga clic en **Actualizar página** \ ( ![ Actualizar página ][ImageRefreshPageIcon] \).  DevTools registra las métricas de rendimiento mientras se actualiza la página y, a continuación, detiene automáticamente la grabación un par de segundos después de que finalice la carga.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Actualizar página" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **Actualizar página**  
    :::image-end:::  
    
DevTools automáticamente acerca de la parte de la grabación donde se produjo la mayor parte de la actividad.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Una grabación de página" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   Una grabación de página  
:::image-end:::  

### Capturar capturas de pantallas durante la grabación   

Active la casilla **capturas** de pantalla para capturar una captura de pantalla de cada fotograma mientras graba.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="La casilla de verificación capturas de pantallas" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   La casilla de verificación **capturas de pantallas**  
:::image-end:::  

Consulte [ver una captura de pantalla](#view-a-screenshot) para obtener información sobre cómo interactuar con capturas de pantalla.  

### Forzar recolección de elementos no utilizados al grabar   

Mientras graba una página, haga clic en **recopilar basura** \ ( ![ recopilar basura ][ImageCollectGarbageIcon] \) para forzar la recolección de elementos no utilizados.  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Recopilar basura" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   Recopilar basura  
:::image-end:::  

### Mostrar configuración de grabación   

Haga clic en **configuración de captura** \ ( ![ capturar configuración ][ImageCaptureSettingsIcon] \) para exponer más opciones de configuración relacionadas con el modo en que DevTools captura las grabaciones de rendimiento.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="La sección configuración de captura" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   La sección **configuración de captura**  
:::image-end:::  

### Deshabilitar ejemplos de JavaScript   

De forma predeterminada, la sección **principal** de una grabación muestra las pilas de llamadas detalladas de las funciones de JavaScript a las que se llamó durante la grabación.  Para deshabilitar estas pilas de llamadas:  

1.  Abra el menú de **configuración de captura** .  Consulte [Mostrar configuración de grabación](#show-recording-settings).  
1.  Active la casilla **deshabilitar ejemplos de JavaScript** .  
1.  Realizar una grabación de la página.  
    
Las 2 figuras siguientes muestran la diferencia entre deshabilitar y habilitar muestras de JavaScript.  La sección **principal** de la grabación es mucho más corta cuando el muestreo está deshabilitado, porque omite todas las pilas de llamadas de JavaScript.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Ejemplo de una grabación cuando se deshabilitan los ejemplos de JS" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         Ejemplo de una grabación cuando se deshabilitan los ejemplos de JS  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Ejemplo de una grabación cuando se habilitan ejemplos de JS" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         Ejemplo de una grabación cuando se habilitan ejemplos de JS  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### Limitar la red durante la grabación   

Para limitar la red durante la grabación:  

1.  Abra el menú de **configuración de captura** .  Consulte [Mostrar configuración de grabación](#show-recording-settings).  
1.  Establezca **red** en el nivel deseado de limitación.  
    
### Limitar la CPU durante la grabación   

Para limitar la CPU durante la grabación:  

1.  Abra el menú de **configuración de captura** .  Consulte [Mostrar configuración de grabación](#show-recording-settings).  
1.  Establezca la **CPU** en el nivel deseado de limitación.  
    
El límite es relativo a las capacidades de su equipo.  Por ejemplo, la opción **2x ralentización** hace que la CPU funcione 2 veces más lentas de lo normal.  DevTools no simulan verdaderamente las CPU de los dispositivos móviles, porque la arquitectura de los dispositivos móviles es muy diferente de la de los equipos de escritorio y portátiles.  

### Habilitar la instrumentación avanzada de pintura   

Para ver la instrumentación de pintura detallada:  

1.  Abra el menú de **configuración de captura** .  Consulte [Mostrar configuración de grabación](#show-recording-settings).  
1.  Active la casilla **Habilitar el instrumental de pintura avanzada (lento)** .  

Para obtener información sobre cómo interactuar con la información de las pinturas, consulte [Ver capas](#view-layers-information) y [Ver generador de perfiles de pintura](#view-paint-profiler).  

## Guardar una grabación   

Para guardar una grabación, haga clic con el botón derecho y seleccione **Guardar perfil**.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Guardar perfil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **Guardar perfil**  
:::image-end:::  

## Cargar una grabación   

Para cargar una grabación, haga clic con el botón derecho y seleccione **cargar perfil**.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Cargar perfil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **Cargar perfil**  
:::image-end:::  

## Borrar la grabación anterior   

Después de realizar una grabación, presione **Borrar grabación** \ ( ![ Borrar grabación ][ImageClearRecordingIcon] \) para borrar esa grabación en el panel **rendimiento** .  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Borrar grabación" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **Borrar grabación**  
:::image-end:::  

## Analizar una grabación de rendimiento   

Después de [grabar el rendimiento en tiempo de ejecución](#record-runtime-performance) o el rendimiento de la [carga de registros](#record-load-performance), el panel **rendimiento** proporciona una gran cantidad de datos para analizar el rendimiento de lo que sucedió.  

### Seleccionar una parte de una grabación   

Arrastre el ratón hacia la izquierda o hacia la derecha en la **información general** para seleccionar una parte de una grabación.  La **información general** es la sección que contiene los gráficos de **fps**, **CPU**y **net** .  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Arrastre el mouse por la información general para aplicar zoom" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   Arrastre el mouse por la **información general** para aplicar zoom  
:::image-end:::  

Para seleccionar una parte con el teclado:  

1.  Haga clic en el fondo de la sección **principal** o en cualquiera de las secciones que hay junto a ella, como **interacciones**, **red**o **GPU**.  Este flujo de trabajo de teclado solo funciona cuando una de estas secciones está en el foco.  
1.  Use las `W` teclas,, `A` `S` , `D` para acercar, mover a la izquierda, alejar y desplazar a la derecha, respectivamente.  

Para seleccionar una parte con un panel táctil:  

1.  Mantenga el mouse sobre la sección **Descripción general** o en la sección de **detalles** .  La sección de **información general** es el área que contiene los gráficos de **fps**, **CPU**y **net** .  La sección de **detalles** es el área que contiene la sección **principal** , la sección **interacciones** , etc.  
1.  Con dos dedos, deslice el dedo hacia arriba para alejar, deslice el dedo hacia la izquierda, deslice el dedo hacia abajo y deslice el dedo hacia la derecha para desplazarse hacia la derecha.  

Para desplazarse por un gráfico de llamas largo en la sección **principal** o en cualquiera de los vecinos, haga clic y mantenga presionado mientras arrastra hacia arriba o hacia abajo.  Arrastre hacia la izquierda y hacia la derecha para mover qué parte de la grabación está seleccionada.  

### Buscar actividades   

Pulse `Control` + `F` \ (Windows \) o `Command` + `F` \ (MacOS \) para abrir el cuadro de búsqueda en la parte inferior del panel **rendimiento** .  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="El cuadro de búsqueda" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   El cuadro de búsqueda  
:::image-end:::  

Para navegar por las actividades que coinciden con la consulta:  

*   Use los **Previous** botones \ ( ![ anterior ][ImagePreviousIcon] \) y **siguiente** \ ( ![ siguiente ][ImageNextIcon] \) anteriores.  
*   Pulse `Shift` + `Enter` para seleccionar la anterior o `Enter` para seleccionar la siguiente.  

Para modificar la configuración de la consulta:  

*   Presione **distinción de mayúsculas y minúsculas** \ ( ![ distingue mayúsculas de minúsculas ][ImageSearchCaseIcon] \) para hacer distinción entre mayúsculas y minúsculas.  
*   Presione **Regex** \ ( ![ regex ][ImageSearchRegexIcon] \) para usar una expresión regular en la consulta.  

Para ocultar el cuadro de búsqueda, presione **Cancelar**.  

### Ver actividad de subproceso principal   

Use la sección **principal** para ver la actividad que se produjo en el subproceso principal de la página.  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="La sección principal" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   La sección **principal**  
:::image-end:::  

Haga clic en un evento para ver más información sobre él en la pestaña **Resumen** .  DevTools describe el evento seleccionado.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Más información sobre la función anónima en la pestaña Resumen" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   Más información sobre la `anonymous` función en la pestaña **Resumen**  
:::image-end:::  

DevTools representa la actividad principal del subproceso con un gráfico de llama.  El eje x representa la grabación a lo largo del tiempo.  El eje y representa la pila de llamadas.  Los eventos en la parte superior provocan los eventos que se encuentran por debajo.  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Un gráfico de llamas" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   Un gráfico de llamas  
:::image-end:::  

En la ilustración anterior, un `click` evento produjo un `Function Call` en `activitytabs.js` en la línea 53.  A continuación `Function Call` , verá que se llamó a una función anónima.  La función anónima a la que se llamó, a la que llamó `a` `wait` `Minor GC` .  

DevTools asigna scripts a colores aleatorios.  En la ilustración anterior, las llamadas de función de un script se muestran coloreadas en verde.  Las llamadas desde otra secuencia de comandos tienen color beige.  El amarillo más oscuro representa la actividad de scripting y el evento morado representa la actividad de representación.  Estos eventos amarillos y amarillos más oscuros son coherentes en todas las grabaciones.  

Consulte [deshabilitar muestras de JavaScript](#disable-javascript-samples) si desea ocultar el gráfico detallado de llamadas de JavaScript.  Cuando se deshabilitan los ejemplos de JS, solo verá eventos de alto nivel, como `Event: click` y `Function Call` de la ilustración anterior.  

### Ver actividades en una tabla   

Después de grabar una página, no es necesario basarse únicamente en la sección **principal** para analizar las actividades.  DevTools también proporciona tres vistas tabulares para analizar actividades.  Cada vista le ofrece una perspectiva diferente en las actividades:  

*   Cuando desee ver las actividades raíz que producen el mayor trabajo, use [la pestaña árbol de llamadas](#the-call-tree-tab).  
*   Cuando desee ver las actividades en las que el más tiempo se dedicó directamente, use [la pestaña de la parte inferior](#the-bottom-up-tab).  
*   Cuando desee ver las actividades en el orden en el que se produjeron durante la grabación, use [la pestaña registro de eventos](#the-event-log-tab).  
    
> [!NOTE]
> Las tres secciones siguientes hacen referencia a la misma demostración.  Ejecute la demostración usted mismo en la [demostración de pestañas de actividad][ActivityTabsDemo].  

#### Actividades raíz   

A continuación se explica el concepto de **actividades raíz** que se menciona en las secciones **árbol de llamadas** , pestaña **ascendente** y registro de **eventos** .  

Las actividades raíz son aquellas que hacen que el explorador realice algún trabajo.  Por ejemplo, al hacer clic en una página, el explorador desencadena una `Event` actividad como la actividad raíz.  Esto `Event` puede hacer que se ejecute un controlador, y así sucesivamente.  

En el gráfico de llamas de la sección **principal** , las actividades raíz se encuentran en la parte superior del gráfico.  En las pestañas **árbol de llamadas** y **registro de eventos** , las actividades raíz son los elementos de nivel superior.  

Para obtener un ejemplo de actividades raíz, consulte [la ficha árbol de llamadas](#the-call-tree-tab) .  

#### La ficha árbol de llamadas   

Use la pestaña **árbol de llamadas** para ver qué actividades de [raíz](#root-activities) hacen la mayor parte del trabajo.  

La pestaña **árbol de llamadas** solo muestra actividades durante la parte seleccionada de la grabación.  Para obtener más información sobre cómo seleccionar partes, vea [seleccionar una parte de una grabación](#select-a-portion-of-a-recording) .  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="La ficha árbol de llamadas" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   La ficha **árbol de llamadas**  
:::image-end:::  

En la ilustración anterior, el nivel superior de los elementos de la columna **actividad** , como `Evaluate Script` y `Parse HTML` son las actividades raíz.  El anidamiento representa la pila de llamadas.  Por ejemplo, en la ilustración anterior, `Parse HTML` que causó el origen `Evaluate Script` `Compile Script` y el `(anonymous)` .  

El **tiempo propio** representa el tiempo que pasa directamente en esa actividad.  **Tiempo total** representa el tiempo invertido en esa actividad o en cualquiera de los elementos secundarios.  

Haga clic en **tiempo propio**, en **tiempo total**o en **actividad** para ordenar la tabla por esa columna.  

Use el cuadro de texto **filtrar** para filtrar eventos por nombre de actividad.  

De forma predeterminada, el menú **agrupar** se establece en **sin agrupar**.  Use el menú **agrupar** para ordenar la tabla actividad según varios criterios.  

Haga clic en **Mostrar pila más pesado** \ ( ![ Mostrar pila más pesada ][ImageShowHeaviestStackIcon] \) para mostrar otra tabla a la derecha de la tabla **actividad** .  Haga clic en una actividad para rellenar la tabla de **pila más intensa** .  La tabla **pila más pesada** muestra qué elementos secundarios de la actividad seleccionada tardaron más tiempo en ejecutarse.  

#### La pestaña abajo   

Use la pestaña **de abajo** para ver las actividades que se ocuparon directamente la mayor parte del tiempo en el agregado.  

La pestaña de la **parte inferior** solo muestra actividades durante la parte seleccionada de la grabación.  Para obtener más información sobre cómo seleccionar partes, vea [seleccionar una parte de una grabación](#select-a-portion-of-a-recording) .  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="La pestaña abajo" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   La pestaña **abajo**  
:::image-end:::  

En el diagrama de llamas de la sección **principal** de la ilustración anterior, vea que casi prácticamente todo el tiempo se dedicó a ejecutarse `Parse HTML` .  La actividad superior de la pestaña de la **parte inferior** de la figura anterior es `Parse HTML` .  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  Consulte en la pestaña de la **parte inferior** , la actividad más costosa es `Layout` .  

La columna **Self Time** representa el tiempo agregado directamente en esa actividad, en todas las apariciones.  

La columna **tiempo total** representa el tiempo agregado invertido en esa actividad o en cualquiera de los elementos secundarios.  

#### La ficha registro de eventos   

Use la pestaña **registro de eventos** para ver las actividades en el orden en el que se produjeron durante la grabación.  

La pestaña **registro de eventos** solo muestra actividades durante la parte seleccionada de la grabación.  Para obtener más información sobre cómo seleccionar partes, vea [seleccionar una parte de una grabación](#select-a-portion-of-a-recording) .  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="La ficha registro de eventos" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   La ficha **registro de eventos**  
:::image-end:::  

La columna **hora de inicio** representa el punto en el que se inició la actividad, en relación con el inicio de la grabación.  Por ejemplo, la hora de inicio del `175.7 ms` elemento seleccionado en la figura anterior significa que la actividad comenzó el 175,7 ms después de que se iniciara la grabación.  

La columna **Self Time** representa el tiempo invertido directamente en esa actividad.  

La columna **tiempo total** representa el tiempo invertido directamente en esa actividad o en cualquiera de los elementos secundarios.  

Haga clic en **hora de inicio**, tiempo **propio**o **tiempo total** para ordenar la tabla por esa columna.

Use el cuadro de texto **filtrar** para filtrar las actividades por nombre.  

Use el menú **duración** para filtrar todas las actividades que hayan tardado menos de 1 ms o de 15 ms.  De forma predeterminada, el menú **duración** se establece en **todos**, lo que significa que se muestran todas las actividades.  

Deshabilite las casillas de verificación **cargar**, **scripting**, **procesamiento**o **pintura** para filtrar todas las actividades de esas categorías.  

### Ver actividad de la GPU   

Ver la actividad de la GPU en la sección **GPU** .  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="La sección GPU" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   La sección **GPU**  
:::image-end:::  

### Ver actividad rasterizada   

Ver la actividad rasterizada en la sección de **trama** .  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="La sección trama" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   La sección **trama**  
:::image-end:::  

### Ver interacciones   

Use la sección **interacciones** para buscar y analizar las interacciones del usuario que se produjeron durante la grabación.  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="La sección interacciones" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   La sección **interacciones**  
:::image-end:::  

Una línea roja en la parte inferior de una interacción representa el tiempo dedicado a esperar el subproceso principal.  

Haga clic en una interacción para ver más información sobre ella en la pestaña **Resumen** .  

### Analizar fotogramas por segundo (FPS)   

DevTools proporciona numerosas formas de analizar fotogramas por segundo:  

*   Use [el gráfico de fps](#the-fps-chart) para obtener una visión general de los FPS durante la grabación.  
*   Use [la sección Marcos](#the-frames-section) para ver cuánto tarda un marco en particular.  
*   Use el **medidor de fps** para una estimación en tiempo real de fps a medida que se ejecuta la página.  Consulte [Ver fotogramas por segundo en tiempo real con el medidor de fps](#view-frames-per-second-in-realtime-with-the-fps-meter).  
    
#### El gráfico de FPS   

El gráfico **fps** proporciona una descripción general de la velocidad de fotogramas en toda la duración de una grabación.  En general, cuanto más alto sea la barra verde, mejor será la velocidad de fotogramas.  

Una barra roja encima del gráfico de **fps** es una advertencia de que la velocidad de fotogramas ha disminuido tan poco que probablemente se ha dañado la experiencia del usuario.  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="El gráfico de FPS" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   El gráfico de **fps**  
:::image-end:::  

#### La sección marcos   

La sección **Marcos** le indica exactamente cuánto tarda un marco en particular.  

Mantenga el mouse sobre un marco para ver una información sobre herramientas con más información sobre ella.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Desplazar el puntero sobre un marco" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   Desplazar el puntero sobre un marco  
:::image-end:::  

Haga clic en un marco para ver más información sobre el marco en la pestaña **Resumen** .  DevTools esquematiza el fotograma seleccionado en azul.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Ver un marco en la pestaña Resumen" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   Ver un marco en la pestaña **Resumen**  
:::image-end:::  

### Ver solicitudes de red   

Expanda la sección **red** para ver una cascada de solicitudes de red que se produjeron durante la grabación.  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="La sección red" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   La sección **red**  
:::image-end:::  

Las solicitudes se codifican en colores de la siguiente manera:  

*   HTML: azul  
*   CSS: morado  
*   JS: amarillo  
*   Imágenes: verde  
    
Haga clic en una solicitud para ver más información sobre ella en la pestaña **Resumen** .  Por ejemplo, en la ilustración anterior, la pestaña **Resumen** muestra más información sobre la solicitud azul seleccionada en la sección **red** .  

Un cuadrado de color azul más oscuro en la parte superior izquierda de una solicitud significa que es una solicitud de mayor prioridad.  Un cuadrado más claro significa menor prioridad.  Por ejemplo, en la ilustración anterior, el azul, la solicitud seleccionada es de mayor prioridad y el verde que está debajo es de menor prioridad.  

En el 1º de los siguientes valores, la solicitud de `www.bing.com` se representa mediante una línea a la izquierda, una barra en el centro con una parte oscura y una parte oscura y una línea a la derecha.  En la segunda de las siguientes figuras, se muestra la representación correspondiente de la misma solicitud en la ficha **intervalos** del panel **red** .  A continuación se muestra cómo se asignan entre sí estas dos representaciones:

*   La línea izquierda es todo hasta el `Connection Start` grupo de eventos, ambos incluidos.  En otras palabras, es todo lo antes `Request Sent` y exclusivo.  
*   La parte clara de la barra es `Request Sent` y `Waiting (TTFB)` .  
*   La parte oscura de la barra es `Content Download` .  
*   Esencialmente, la línea adecuada es el tiempo dedicado a esperar el hilo principal.  Esto no se representa en la pestaña **intervalos** .  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="La representación de barra de línea de la solicitud www.bing.com" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         Representación de barra de línea de la `www.bing.com` solicitud  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="La sección red" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         La sección **red**  
::: Image-end:::  
   :::column-end:::
:::row-end:::

### Ver métricas de memoria   

Active la casilla **memoria** para ver las métricas de memoria de la última grabación.  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="La casilla memoria" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   La casilla **memoria**  
:::image-end:::  

DevTools muestra un nuevo gráfico de **memoria** , encima de la pestaña **Resumen** .  También hay un nuevo gráfico debajo del gráfico **net** , denominado **montón**.  El gráfico de **montones** proporciona la misma información que la línea de **montón JS** en el gráfico de **memoria** .  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Métricas de memoria" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   Métricas de memoria  
:::image-end:::  

Las líneas de color del gráfico se asignan a las casillas coloreadas encima del gráfico.  
Desactive una casilla para ocultar la categoría en el gráfico.  

El gráfico solo muestra la región de la grabación que está seleccionada actualmente.  Por ejemplo, en la ilustración anterior, el gráfico de **memoria** solo muestra el uso de memoria de aproximadamente la marca de MS 400 a la marca de 1750 ms.  

### Ver la duración de una parte de una grabación   

Al analizar una sección como la **red** o **Main**, a veces necesitarás una estimación más precisa de cuánto tiempo han tardado determinados eventos.  Espera `Shift` , haga clic y mantenga presionado y arrastre hacia la izquierda o la derecha para seleccionar una parte de la grabación.  En la parte inferior de la selección, DevTools muestra cuánto tiempo duró esa parte.  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Ver la duración de una parte de una grabación" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   Ver la duración de una parte de una grabación  
:::image-end:::  

### Ver una captura de pantalla   

Consulte [capturar capturas de pantallas mientras graba](#capture-screenshots-while-recording) para obtener información sobre cómo habilitar capturas de pantallas.  

Pase el puntero por la **información general** para ver una captura de pantalla de cómo se vio la página durante ese momento de la grabación.  La **información general** es la sección que contiene los gráficos de **CPU**, **fps**y **net** .  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Ver una captura de pantalla" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   Ver una captura de pantalla  
:::image-end:::  

También puede ver capturas de pantallas haciendo clic en un marco de la sección **Marcos** .  DevTools muestra una versión reducida de la captura de pantalla en la pestaña **Resumen** .  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Ver una captura de pantalla en la pestaña Resumen" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   Ver una captura de pantalla en la pestaña **Resumen**  
:::image-end:::  

Para acercar la captura de pantalla, haga clic en la miniatura de la pestaña **Resumen** .  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Ampliar la captura de pantalla desde la pestaña Resumen" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   Ampliar la captura de pantalla desde la pestaña **Resumen**  
:::image-end:::  

### Ver información de capas   

Para ver la información sobre las capas avanzadas de un marco:  

1.  [Habilitar la instrumentación avanzada de pintura](#enable-advanced-paint-instrumentation).  
1.  Seleccione un marco de la sección **Marcos** .  DevTools muestra información sobre las capas en la ficha nuevas **capas** , junto a la ficha **registro de eventos** .  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="El panel capas" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       El panel **capas**  
    :::image-end:::  
    
Desplace el puntero sobre una capa para resaltarla en el diagrama.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Resaltar una capa" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   Resaltar una capa  
:::image-end:::  

Para mover el diagrama:  

*   Haga clic en **modo panorámico** \ ( ![ modo panorámico ][ImagePanModeIcon] \) para desplazarse por los ejes X e y.  
*   Haga clic en **modo de giro** \ ( ![ modo ][ImageRotateModeIcon] de giro \) para girar a lo largo del eje Z.  
*   Haga clic en **restablecer transformación** \ ( ![ restablecer transformación ][ImageResetTransformIcon] \) para restablecer el diagrama a la posición original.  
    
### Ver generador de perfiles de pintura   

Para ver información avanzada sobre un evento de pintura:  

1.  [Habilitar la instrumentación avanzada de pintura](#enable-advanced-paint-instrumentation).  
1.  Seleccione un evento de **pintura** en la sección **principal** .  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Pestaña generador de perfiles de pintura" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       Pestaña **generador de perfiles de pintura**  
    :::image-end:::  
    
## Analizar el rendimiento de la representación con la pestaña representación   

Use las características de la pestaña **representación** para poder visualizar el rendimiento de la representación de la página.  

Para abrir la pestaña **representación** :  

1.  [Abrir el menú de comandos][DevToolsCommandMenu].  
1.  Empiece `Rendering` a escribir y seleccione `Show Rendering` .  DevTools muestra la ficha **representación** en la parte inferior de la ventana de DevTools.  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="La pestaña representación" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       La pestaña **representación**  
    :::image-end:::  
    
### Ver fotogramas por segundo en tiempo real con el medidor de FPS   

El **medidor de fps** es una superposición que aparece en la esquina superior derecha de su ventanilla.  Proporciona una estimación en tiempo real de FPS a medida que se ejecuta la página.  Para abrir el **medidor de fps**:  

1.  Abra la pestaña **representación** .  Consulte [analizar el rendimiento de la representación con la pestaña representación](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Active la casilla de verificación de **medidor de fps** .  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="El medidor de FPS" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       El **medidor de fps**  
    :::image-end:::  
    
### Ver los eventos de pintura en tiempo real con parpadeo de pintura   

Use las intermitencias de pintura para obtener una vista en tiempo real de todos los eventos de pintura en la página.  Cada vez que se vuelve a pintar una parte de la página, DevTools esquematiza esa sección en verde.  

Para habilitar los parpadeos de pintura:  

1.  Abra la pestaña **representación** .  Consulte [analizar el rendimiento de la representación con la pestaña representación](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Active la casilla de **pintura parpadeante** .  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Pintura parpadeante" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **Pintura parpadeante**  
    :::image-end:::  
    
### Ver una superposición de capas con bordes de capas   

Use **bordes de capas** para ver una superposición de los bordes de la capa y los mosaicos en la parte superior de la página.  

Para habilitar los bordes de capas:  

1.  Abra la pestaña **representación** .  Consulte [analizar el rendimiento de la representación con la pestaña representación](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Active la casilla **bordes de capas** .  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Bordes de capas" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **Bordes de capas**  
    :::image-end:::  
    
Vea los comentarios en [`debug_colors.cc`][ChromiumDebugColors] para obtener una explicación de los códigos de color.  

### Buscar problemas de rendimiento de desplazamiento en tiempo real   

Use los problemas de rendimiento de desplazamiento para identificar los elementos de la página que tienen detectores de eventos relacionados con el desplazamiento que pueden dañar el rendimiento de la página.  
DevTools subraya los elementos potencialmente problemáticos de verde azulado.  

Para ver los problemas de rendimiento del desplazamiento:  

1.  Abra la pestaña **representación** .  Consulte [analizar el rendimiento de la representación con la pestaña representación](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Active la casilla de verificación de **problemas de rendimiento de desplazamiento** .  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Los problemas de rendimiento de desplazamiento indican que los objetos restringidos de ventanilla sin capas pueden dañar el rendimiento del desplazamiento" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       Los **problemas de rendimiento de desplazamiento** indican que los objetos restringidos de ventanilla sin capas pueden dañar el rendimiento del desplazamiento  
    :::image-end:::  
    
<!--  
<!--    


-->  

<!-- image links -->  

[ImageCaptureSettingsIcon]: ../media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: ../media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: ../media/collect-garbage-icon.msft.png  
[ImageNextIcon]: ../media/next-icon.msft.png  
[ImagePanModeIcon]: ../media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: ../media/previous-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png
[ImageRefreshPageIcon]: ../media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: ../media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: ../media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: ../media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: ../media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: ../media/show-heaviest-stack-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Abrir el menú de comandos: ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Introducción al análisis de rendimiento en tiempo de ejecución | Microsoft docs"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Demostración de las pestañas actividad | intento"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors. cc: búsqueda de código"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

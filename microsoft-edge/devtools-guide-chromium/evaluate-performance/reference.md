---
description: Una referencia sobre todas las formas de registrar y analizar el rendimiento en Microsoft Edge DevTools.
title: Referencia de análisis de rendimiento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e7774dc0aab647b8cf2bf47699368fafe6c21d70
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439692"
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

# <a name="performance-analysis-reference"></a>Referencia de análisis de rendimiento  

Esta página es una referencia completa de las características de Microsoft Edge DevTools relacionadas con el análisis del rendimiento.  

Vaya a [Introducción al análisis del rendimiento][DevtoolsEvaluatePerformanceGettingStarted] en tiempo de ejecución para obtener un tutorial guiado sobre cómo analizar el rendimiento de una página mediante Microsoft Edge [DevTools][MicrosoftEdgeDevTools].  

## <a name="record-performance"></a>Rendimiento del registro  

### <a name="record-runtime-performance"></a>Rendimiento del tiempo de ejecución de registro  

Registre el rendimiento en tiempo de ejecución cuando desee analizar el rendimiento de una página mientras se está ejecutando, en lugar de cargarla.  

1.  Vaya a la página que desea analizar.  
1.  Abra la **herramienta Rendimiento** en DevTools.  
1.  Elija **Grabar** \( ![ Icono de registro ](../media/record-icon.msft.png) \).  
    
    :::image type="complex" source="../media/evaluate-performance-performance-record-highlight.msft.png" alt-text="Grabar" lightbox="../media/evaluate-performance-performance-record-highlight.msft.png":::
       **Grabar**  
    :::image-end:::  
    
1.  Interactuar con la página.  DevTools registra toda la actividad de página que se produce como resultado de las interacciones.  
1.  Elija **Grabar de** nuevo o Detener **para** detener la grabación.  
    
### <a name="record-load-performance"></a>Rendimiento de carga de registro  

Registre el rendimiento de carga cuando desee analizar el rendimiento de una página mientras se carga, en lugar de ejecutarse.  

1.  Vaya a la página que desea analizar.  
1.  Abra **el** panel Rendimiento de DevTools.  
1.  Elija **Actualizar página** \( Actualizar página ![ ](../media/refresh-page-icon.msft.png) \).  DevTools registra las métricas de rendimiento mientras la página se actualiza y, a continuación, detiene automáticamente la grabación un par de segundos después de que finalice la carga.  
    
    :::image type="complex" source="../media/evaluate-performance-performance-refresh-button.msft.png" alt-text="Página Actualizar" lightbox="../media/evaluate-performance-performance-refresh-button.msft.png":::
       **Página Actualizar**  
    :::image-end:::  
    
DevTools acerca automáticamente la parte de la grabación donde se produjo la mayor parte de la actividad.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed.msft.png" alt-text="Una grabación de carga de página" lightbox="../media/evaluate-performance-performance-refreshed.msft.png":::
   Una grabación de carga de página  
:::image-end:::  

### <a name="capture-screenshots-while-recording"></a>Capturar capturas de pantalla durante la grabación  

Activa la casilla **Capturas de pantalla** para capturar una captura de pantalla de cada fotograma durante la grabación.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png" alt-text="La casilla Capturas de pantalla" lightbox="../media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png":::
   La **casilla Capturas de** pantalla  
:::image-end:::  

Vaya a [Ver una captura de pantalla](#view-a-screenshot) para obtener información sobre cómo interactuar con las capturas de pantalla.  

### <a name="force-garbage-collection-while-recording"></a>Forzar la recolección de elementos no utilizados durante la grabación  

Mientras graba una página, elija **Recopilar elementos no** utilizados \( Recopilar icono de elementos no utilizados ![ ](../media/collect-garbage-icon.msft.png) \) para forzar la recolección de elementos no utilizados.  

:::image type="complex" source="../media/evaluate-performance-performance-collect-garbage-button.msft.png" alt-text="Recopilar elementos no utilizados" lightbox="../media/evaluate-performance-performance-collect-garbage-button.msft.png":::
   Recopilar elementos no utilizados  
:::image-end:::  

### <a name="show-recording-settings"></a>Mostrar configuración de grabación  

Elija **Configuración de captura** \( Configuración de captura \) para exponer más opciones relacionadas con la forma en que ![ ](../media/capture-settings-icon.msft.png) DevTools captura las grabaciones de rendimiento.  

:::image type="complex" source="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png" alt-text="Sección Configuración de captura" lightbox="../media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png":::
   Sección **Configuración de** captura  
:::image-end:::  

### <a name="disable-javascript-samples"></a>Deshabilitar ejemplos de JavaScript  

De forma predeterminada, la **sección Main** de una grabación muestra las pilas de llamadas detalladas de las funciones de JavaScript a las que se llamó durante la grabación.  Para deshabilitar estas pilas de llamadas:  

1.  Abra el **menú Configuración de** captura.  Vaya a [Mostrar configuración de grabación](#show-recording-settings).  
1.  Active la casilla **Deshabilitar ejemplos de JavaScript.**  
1.  Haga una grabación de la página.  
    
Las dos cifras siguientes muestran la diferencia entre deshabilitar y habilitar ejemplos de JavaScript.  La **sección Principal** de la grabación es mucho más corta cuando se deshabilita el muestreo, ya que omite todas las pilas de llamadas de JavaScript.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png" alt-text="Un ejemplo de una grabación cuando se deshabilitan los ejemplos de JS" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png":::
         Un ejemplo de una grabación cuando se deshabilitan los ejemplos de JS  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png" alt-text="Un ejemplo de una grabación cuando se han activado las muestras de JS" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png":::
         Un ejemplo de una grabación cuando se han activado las muestras de JS  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <a name="throttle-the-network-while-recording"></a>Limitar la red durante la grabación  

Para limitar la red durante la grabación:  

1.  Abra el **menú Configuración de** captura.  Vaya a [Mostrar configuración de grabación](#show-recording-settings).  
1.  Establezca **Red** en el nivel deseado de limitación.  
    
### <a name="throttle-the-cpu-while-recording"></a>Limitar la CPU durante la grabación  

Para limitar la CPU durante la grabación:  

1.  Abra el **menú Configuración de** captura.  Vaya a [Mostrar configuración de grabación](#show-recording-settings).  
1.  Establece **la CPU** en el nivel deseado de limitación.  
    
La limitación es relativa a las capacidades del equipo.  Por ejemplo, la **opción de ralentización 2x** hace que la CPU funcione 2 veces más lento de lo normal.  DevTools no simula realmente las CPU de los dispositivos móviles, ya que la arquitectura de los dispositivos móviles es muy diferente de la de los equipos de escritorio y portátiles.  

### <a name="turn-on-advanced-paint-instrumentation"></a>Activar instrumentación de pintura avanzada  

Para ver instrumentación de pintura detallada:  

1.  Abra el **menú Configuración de** captura.  Vaya a [Mostrar configuración de grabación](#show-recording-settings).  
1.  Active la casilla **Habilitar instrumentación avanzada de pintura (lento).**  

Para obtener información sobre cómo interactuar con la información de pintura, vaya [a Ver capas](#view-layers-information) y Ver [perfiles de pintura.](#view-paint-profiler)  

## <a name="save-a-recording"></a>Guardar una grabación  

Para guardar una grabación, abra el menú contextual \(hacer clic con el botón secundario\) y elija **Guardar perfil**.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png" alt-text="Guardar perfil" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png":::
   **Guardar perfil**  
:::image-end:::  

## <a name="load-a-recording"></a>Cargar una grabación  

Para cargar una grabación, abra el menú contextual \(hacer clic con el botón secundario\) y elija **Cargar perfil**.  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png" alt-text="Perfil de carga" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png":::
   **Perfil de carga**  
:::image-end:::  

## <a name="clear-the-previous-recording"></a>Borrar la grabación anterior  

Después de realizar una grabación, elija **Borrar grabación** \( Borrar icono de grabación \) para borrar esa grabación desde el ![ panel ](../media/clear-recording-icon.msft.png) Rendimiento. ****  

:::image type="complex" source="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png" alt-text="Borrar grabación" lightbox="../media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png":::
   **Borrar grabación**  
:::image-end:::  

## <a name="analyze-a-performance-recording"></a>Analizar una grabación de rendimiento  

Después de [registrar el rendimiento en tiempo](#record-runtime-performance) de ejecución o el rendimiento de carga de registros, el panel Rendimiento proporciona una gran cantidad de datos para analizar el rendimiento de lo que acaba de suceder. [](#record-load-performance) ****  

### <a name="select-a-portion-of-a-recording"></a>Seleccionar una parte de una grabación  

Arrastre el mouse a la izquierda o a la derecha a través de **información** general para seleccionar una parte de una grabación.  Overview **es** la sección que contiene los gráficos **FPS,** **CPU**y **NET.**  

:::image type="complex" source="../media/evaluate-performance-performance-zoom-highlighted.msft.png" alt-text="Arrastre el mouse a través de información general para acercar" lightbox="../media/evaluate-performance-performance-zoom-highlighted.msft.png":::
   Arrastre el mouse a través de **información general** para acercar  
:::image-end:::  

Para seleccionar una parte con el teclado:  

1.  Elija el fondo de la **sección Principal** o cualquiera de las secciones que hay junto a ella, como **Interacciones,** **Red**o **GPU.**  Este flujo de trabajo de teclado solo funciona cuando una de estas secciones está en el foco.  
1.  Usa las teclas , , , para acercar, mover a la izquierda, alejar y mover a la `W` `A` `S` `D` derecha, respectivamente.  

Para seleccionar una parte con un trackpad, realice las siguientes acciones.  

1.  Mantenga el mouse sobre la **sección Información** general o la **sección** Detalles.  La **sección Información** general es el área que contiene los gráficos **FPS,** **CPU**y **NET.**  La **sección** Detalles es el área que contiene la **sección Principal,** la **sección Interacciones,** y así sucesivamente.  
1.  Con dos dedos, desliza el dedo hacia arriba para alejarse, desliza el dedo hacia la izquierda para moverte a la izquierda, desliza el dedo hacia abajo para acercar y desliza el dedo hacia la derecha para moverte a la derecha.  

Para desplazarse por un gráfico de llama largo en la **sección Principal** o cualquiera de los vecinos, elija y mantenga presionado mientras arrastra hacia arriba y hacia abajo.  Arrastre a la izquierda y a la derecha para mover la parte de la grabación elegida.  

### <a name="search-activities"></a>Actividades de búsqueda  

Seleccione `Control` + `F` \(Windows, Linux\) o `Command` + `F` \(macOS\) **** para abrir el cuadro de búsqueda en la parte inferior del panel Rendimiento.  

:::image type="complex" source="../media/evaluate-performance-performance-search-regex.msft.png" alt-text="El cuadro de búsqueda" lightbox="../media/evaluate-performance-performance-search-regex.msft.png":::
   El cuadro de búsqueda  
:::image-end:::  

Para navegar por actividades que coincidan con la consulta:  

*   Use los **botones** Previous \( ![ Previous ](../media/previous-icon.msft.png) \) y **Next** \( ![ Next ](../media/next-icon.msft.png) \).  
*   Seleccione `Shift` + `Enter` para seleccionar la anterior `Enter` o para seleccionar la siguiente.  

Para modificar la configuración de consulta:  

*   Elija **Distingue mayúsculas de** minúsculas ![ \( Distingue mayúsculas de ](../media/search-case-icon.msft.png) minúsculas \) para que la consulta sea confidencial.  
*   Elija **Regex** \( ![ Regex ](../media/search-regex-icon.msft.png) \) para usar una expresión regular en la consulta.  

Para ocultar el cuadro de búsqueda, elija **Cancelar**.  

### <a name="view-main-thread-activity"></a>Ver actividad de subprocesos principales  

Use la **sección Main** para ver la actividad que se produjo en el subproceso principal de la página.  

:::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Sección Principal" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
   Sección **** Principal  
:::image-end:::  

Elija un evento para ver más información sobre él en el panel **Resumen.**  DevTools describe el evento seleccionado.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-me.msft.png" alt-text="Más información sobre la función anónima en el panel Resumen" lightbox="../media/evaluate-performance-performance-summary-me.msft.png":::
   Más información sobre la `anonymous` función en el panel **Resumen**  
:::image-end:::  

DevTools representa la actividad del subproceso principal con un gráfico de llamas.  El eje X representa la grabación con el tiempo.  El eje Y representa la pila de llamadas.  Los eventos en la parte superior provocan los eventos debajo de él.  

:::image type="complex" source="../media/evaluate-performance-performance-main-flame-chart.msft.png" alt-text="Un gráfico de llamas" lightbox="../media/evaluate-performance-performance-main-flame-chart.msft.png":::
   Un gráfico de llamas  
:::image-end:::  

En la figura anterior, `click` un evento provocó una `Function Call` entrada en la línea `activitytabs.js` 53.  A `Function Call` continuación, revise que se ha ejecutado una función anónima.  La función anónima solicitada `a` , que `wait` solicitó , que solicitó `Minor GC` .  

DevTools asigna scripts de colores aleatorios.  En la figura anterior, las solicitudes de función de un script son de color verde claro.  Las solicitudes de otro script son de color beis.  El amarillo más oscuro representa la actividad de scripting y el evento púrpura representa la actividad de representación.  Estos eventos amarillos y púrpuras más oscuros son coherentes en todas las grabaciones.  

Vaya a [Deshabilitar ejemplos de JavaScript](#disable-javascript-samples) si desea ocultar el gráfico detallado de llamas de las solicitudes de JavaScript.  Cuando se deshabilitan los ejemplos de JS, solo se muestran eventos de alto nivel, como y `Event: choose` `Function Call` de la figura `str` anterior.  

### <a name="view-activities-in-a-table"></a>Ver actividades en una tabla  

Después de grabar una página, no es necesario depender únicamente de la **sección Principal** para analizar las actividades.  DevTools también proporciona tres vistas tabulares para analizar actividades.  Cada vista le ofrece una perspectiva diferente sobre las actividades:  

*   Cuando desee ver las actividades raíz que más funcionan, use el panel [Árbol de](#the-call-tree-panel) llamadas.  
*   Cuando desee ver las actividades en las que se ha dedicado más tiempo directamente, use el panel [Inferior](#the-bottom-up-panel) hacia arriba.  
*   Cuando desee ver las actividades en el orden en que se produjeron durante la grabación, use el panel [Registro de](#the-event-log-panel) eventos.  
    
> [!NOTE]
> Las tres secciones siguientes hacen referencia a la misma demostración.  Ejecute la demostración usted mismo [en La demostración de pestañas de actividad][ActivityTabsDemo].  

#### <a name="root-activities"></a>Actividades raíz  

Esta es una explicación del concepto **de actividades** raíz que se menciona en el **panel** Árbol de **llamadas,** el panel inferior arriba y el panel **Registro de** eventos.  

Las actividades raíz son las que hacen que el explorador realice algún trabajo.  Por ejemplo, al elegir una página web, el explorador ejecuta una `Event` actividad como actividad raíz.  Esto `Event` puede hacer que se ejecute un controlador, y así sucesivamente.  

En el gráfico de llama de la **sección Principal,** las actividades raíz se encuentran en la parte superior del gráfico.  En los **paneles Árbol de llamadas** y Registro **de** eventos, las actividades raíz son los elementos de nivel superior.  

Vaya al panel [Árbol de llamadas](#the-call-tree-panel) para ver un ejemplo de actividades raíz.  

#### <a name="the-call-tree-panel"></a>Panel Árbol de llamadas  

Use el **panel Árbol de llamadas** para ver qué actividades [raíz](#root-activities) causan más trabajo.  

El **panel Árbol de** llamadas solo muestra actividades durante la parte seleccionada de la grabación.  Vaya [a Seleccionar una parte de una grabación](#select-a-portion-of-a-recording) para obtener información sobre cómo seleccionar partes.  

:::image type="complex" source="../media/evaluate-performance-performance-call-tree.msft.png" alt-text="Panel Árbol de llamadas" lightbox="../media/evaluate-performance-performance-call-tree.msft.png":::
   Panel **Árbol de llamadas**  
:::image-end:::  

En la figura anterior, el nivel superior de los elementos de la columna **Actividad,** como `Evaluate Script` y son actividades `Parse HTML` raíz.  El anidamiento representa la pila de llamadas.  Por ejemplo, en la figura anterior, `Parse HTML` que `Evaluate Script` causó la `Compile Script` causa y `(anonymous)` .  

**Self Time** representa el tiempo invertido directamente en esa actividad.  **El tiempo total** representa el tiempo invertido en esa actividad o en cualquiera de los secundarios.  

Elija **Self Time**, Total **Time**o **Activity** para ordenar la tabla por esa columna.  

Use el **cuadro de** texto Filtrar para filtrar eventos por nombre de actividad.  

De forma **predeterminada, el menú** Agrupación se establece en Sin **agrupación**.  Use el **menú Agrupación** para ordenar la tabla de actividad según varios criterios.  

Elija **Mostrar pila más pesada** \( Mostrar pila más pesada \) para mostrar otra tabla a la derecha de la tabla ![ ](../media/show-heaviest-stack-icon.msft.png) **Actividad.**  Elija una actividad para rellenar la **tabla De pila más** pesada.  La **tabla Pila más pesada** muestra los elementos secundarios de la actividad seleccionada que tardaron más tiempo en ejecutarse.  

#### <a name="the-bottom-up-panel"></a>El panel Bottom-Up panel  

Use el **panel Inferior arriba** para ver qué actividades tomaron directamente la mayor parte del tiempo agregado.  

El **panel inferior arriba** solo muestra actividades durante la parte seleccionada de la grabación.  Vaya [a Seleccionar una parte de una grabación](#select-a-portion-of-a-recording) para obtener información sobre cómo seleccionar partes.  

:::image type="complex" source="../media/evaluate-performance-performance-bottoms-up.msft.png" alt-text="El panel Bottom-Up panel" lightbox="../media/evaluate-performance-performance-bottoms-up.msft.png":::
   Panel **inferior arriba**  
:::image-end:::  

En el **gráfico de** llama de sección principal de la figura anterior, vaya a ese prácticamente todo el tiempo que se ha dedicado a ejecutar `Parse HTML` .  La actividad superior del panel **inferior arriba** de la figura anterior es `Parse HTML` .  <!--In the flame chart of the previous figure, the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  Navegue hasta el panel **Inferior arriba,** la siguiente actividad más costosa es `Layout` .  

La **columna Self Time** representa el tiempo agregado invertido directamente en esa actividad, en todas las repeticiones.  

La **columna Tiempo total** representa el tiempo agregado invertido en esa actividad o en cualquiera de los secundarios.  

#### <a name="the-event-log-panel"></a>Panel Registro de eventos  

Use el **panel Registro de** eventos para ver las actividades en el orden en que se produjeron durante la grabación.  

El **panel Registro de** eventos solo muestra actividades durante la parte seleccionada de la grabación.  Vaya [a Seleccionar una parte de una grabación](#select-a-portion-of-a-recording) para obtener información sobre cómo seleccionar partes.  

:::image type="complex" source="../media/evaluate-performance-performance-event-log.msft.png" alt-text="Panel Registro de eventos" lightbox="../media/evaluate-performance-performance-event-log.msft.png":::
   Panel **Registro de eventos**  
:::image-end:::  

La **columna Hora de** inicio representa el punto en el que se inició esa actividad, en relación con el inicio de la grabación.  Por ejemplo, la hora de inicio del elemento seleccionado en la figura anterior significa que la actividad se inició `175.7 ms` 175,7 ms después de que se iniciara la grabación.  

La **columna Tiempo de** autoservicio representa el tiempo invertido directamente en esa actividad.  

Las **columnas Tiempo total** representan el tiempo invertido directamente en esa actividad o en cualquiera de los secundarios.  

Elija **Hora de inicio,** **Hora de**autoservicio o Tiempo **total** para ordenar la tabla por esa columna.

Use el **cuadro de** texto Filtrar para filtrar las actividades por su nombre.  

Use el **menú** Duración para filtrar las actividades que tardaron menos de 1 ms o 15 ms.  De forma predeterminada, **el menú** Duración se establece en **Todo**, lo que significa que se muestran todas las actividades.  

Deshabilita las **casillas Carga,** **Scripting,** **Representación**o **Pintura** para filtrar todas las actividades de dichas categorías.  

### <a name="view-gpu-activity"></a>Ver actividad de GPU  

Ver actividad de GPU en la **sección GPU.**  

:::image type="complex" source="../media/evaluate-performance-performance-gpu-zoomed.msft.png" alt-text="Sección GPU" lightbox="../media/evaluate-performance-performance-gpu-zoomed.msft.png":::
   Sección **GPU**  
:::image-end:::  

### <a name="view-raster-activity"></a>Ver actividad de trama  

Ver actividad de trama en la **sección Raster.**  

:::image type="complex" source="../media/evaluate-performance-performance-raster.msft.png" alt-text="Sección Raster" lightbox="../media/evaluate-performance-performance-raster.msft.png":::
   Sección **Raster**  
:::image-end:::  

### <a name="view-interactions"></a>Ver interacciones  

Use la **sección Interacciones** para buscar y analizar las interacciones del usuario que se han producido durante la grabación.  

:::image type="complex" source="../media/evaluate-performance-performance-interactions-animation.msft.png" alt-text="Sección Interacciones" lightbox="../media/evaluate-performance-performance-interactions-animation.msft.png":::
   Sección **Interacciones**  
:::image-end:::  

Una línea roja en la parte inferior de una interacción representa el tiempo invertido en esperar el subproceso principal.  

Elija una interacción para ver más información al respecto en el panel **Resumen.**  

### <a name="analyze-frames-per-second-fps"></a>Analizar fotogramas por segundo (FPS)  

DevTools proporciona numerosas formas de analizar fotogramas por segundo:  

*   Usa [el gráfico FPS para](#the-fps-chart) obtener información general sobre FPS durante la grabación.  
*   Use [la sección Marcos para](#the-frames-section) ver cuánto tiempo tardó un fotograma determinado.  
*   Usa el **medidor fps para** una estimación en tiempo real de FPS a medida que se ejecuta la página.  Vaya a [Ver fotogramas por segundo en tiempo real con el medidor FPS](#view-frames-per-second-in-realtime-with-the-fps-meter).  
    
#### <a name="the-fps-chart"></a>Gráfico de FPS  

El **gráfico FPS** proporciona información general sobre la velocidad de fotogramas durante toda la duración de una grabación.  En general, cuanto mayor sea la barra verde, mejor será la velocidad de fotogramas.  

Una barra roja encima del **gráfico FPS** es una advertencia de que la velocidad de fotogramas se ha reducido tan bajo que probablemente dañe la experiencia del usuario.  

:::image type="complex" source="../media/evaluate-performance-performance-fps-highlight.msft.png" alt-text="Gráfico de FPS" lightbox="../media/evaluate-performance-performance-fps-highlight.msft.png":::
   Gráfico **de FPS**  
:::image-end:::  

#### <a name="the-frames-section"></a>Sección Marcos  

La **sección** Marcos le indica exactamente cuánto tiempo tardó un fotograma en particular.  

Mantenga el mouse sobre un marco para ver una información sobre herramientas con más información sobre él.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-hover.msft.png" alt-text="Mantener el mouse en un marco" lightbox="../media/evaluate-performance-performance-frames-hover.msft.png":::
   Mantener el mouse en un marco  
:::image-end:::  

Elija un marco para ver más información sobre el marco en el panel **Resumen.**  DevTools describe el marco seleccionado en azul.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-summary.msft.png" alt-text="Ver un marco en el panel Resumen" lightbox="../media/evaluate-performance-performance-frames-summary.msft.png":::
   Ver un marco en el panel **Resumen**  
:::image-end:::  

### <a name="view-network-requests"></a>Ver solicitudes de red  

Expanda la **sección Red** para ver una cascada de solicitudes de red que se produjeron durante la grabación.  

:::image type="complex" source="../media/evaluate-performance-performance-network.msft.png" alt-text="Sección Red" lightbox="../media/evaluate-performance-performance-network.msft.png":::
   Sección **Red**  
:::image-end:::  

Las solicitudes tienen un código de color como se muestra a continuación:  

*   HTML: azul  
*   CSS: púrpura  
*   JS: amarillo  
*   Imágenes: Verde  
    
Elija una solicitud para ver más información al respecto en el panel **Resumen.**  Por ejemplo, en la figura anterior, el **panel** Resumen muestra más información sobre la solicitud azul seleccionada en la **sección** Red.  

Un cuadrado azul oscuro en la parte superior izquierda de una solicitud significa que es una solicitud de mayor prioridad.  Un cuadrado azul claro significa prioridad inferior.  Por ejemplo, en la figura anterior, la solicitud azul seleccionada es de mayor prioridad y la verde debajo de ella es de menor prioridad.  

En la 1ª de las siguientes figuras, la solicitud de se representa mediante una línea a la izquierda, una barra en el centro con una parte oscura y una parte ligera, y una línea a la `www.bing.com` derecha.  En la 2ª de las siguientes figuras se muestra la representación correspondiente de la misma solicitud en el **panel** Temporización de la **herramienta Red.**  Esta es la forma en que estas dos representaciones se asignan entre sí:

*   La línea izquierda es todo hasta el `Connection Start` grupo de eventos, inclusive.  En otras palabras, es todo lo anterior `Request Sent` a , exclusive.  
*   La parte ligera de la barra es `Request Sent` y `Waiting (TTFB)` .  
*   La parte oscura de la barra es `Content Download` .  
*   La línea correcta es básicamente el tiempo que se pasa esperando el subproceso principal.  Esto no se representa en el panel **Temporización.**  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-performance-network.msft.png" alt-text="Representación de barra de línea de la www.bing.com solicitud" lightbox="../media/evaluate-performance-bing-performance-network.msft.png":::
         Representación de barra de línea de la `www.bing.com` solicitud  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/evaluate-performance-bing-network-timing.msft.png" alt-text="La herramienta Red" lightbox="../media/evaluate-performance-bing-network-timing.msft.png":::
         La **herramienta Red**  
: ::image-end:::  
   :::column-end:::
:::row-end:::

### <a name="view-memory-metrics"></a>Ver métricas de memoria  

Activa la casilla **Memoria** para ver las métricas de memoria de la última grabación.  

:::image type="complex" source="../media/evaluate-performance-performance-memory-highlight.msft.png" alt-text="La casilla Memoria" lightbox="../media/evaluate-performance-performance-memory-highlight.msft.png":::
   La **casilla Memoria**  
:::image-end:::  

DevTools muestra un nuevo gráfico **de** memoria, encima **del** panel Resumen.  También hay un nuevo gráfico debajo del **gráfico NET,** denominado **HEAP**.  El **gráfico HEAP** proporciona la misma información que la línea **de montón JS** en el gráfico **memoria.**  

:::image type="complex" source="../media/evaluate-performance-performance-memory-chart.msft.png" alt-text="Métricas de memoria" lightbox="../media/evaluate-performance-performance-memory-chart.msft.png":::
   Métricas de memoria  
:::image-end:::  

Las líneas coloreadas del gráfico se asignan a las casillas de color situadas encima del gráfico.  
Deshabilite una casilla para ocultar esa categoría del gráfico.  

El gráfico solo muestra la región de la grabación que está seleccionada actualmente.  Por ejemplo, en la **** figura anterior, el gráfico de memoria solo muestra el uso de memoria de alrededor de la marca de 400 ms a la marca de 1750 ms.  

### <a name="view-the-duration-of-a-portion-of-a-recording"></a>Ver la duración de una parte de una grabación  

Al analizar una sección como **Red** o **Principal**, a veces se necesita una estimación más precisa del tiempo que tardaron determinados eventos.  Mantenga presionado , elija y mantenga presionado y arrastre hacia la izquierda o la `Shift` derecha para seleccionar una parte de la grabación.  En la parte inferior de la selección, DevTools muestra cuánto tiempo tardó esa parte.  

:::image type="complex" source="../media/evaluate-performance-performance-main-duration.msft.png" alt-text="Ver la duración de una parte de una grabación" lightbox="../media/evaluate-performance-performance-main-duration.msft.png":::
   Ver la duración de una parte de una grabación  
:::image-end:::  

### <a name="view-a-screenshot"></a>Ver una captura de pantalla  

Ve a [Capturar capturas de pantalla mientras grabas](#capture-screenshots-while-recording) para obtener información sobre cómo activar capturas de pantalla.  

Mantenga el mouse sobre **la información** general para ver una captura de pantalla de cómo se ve la página durante ese momento de la grabación.  Overview **es** la sección que contiene los gráficos **CPU,** **FPS**y **NET.**  

:::image type="complex" source="../media/evaluate-performance-performance-screenshots-hover.msft.png" alt-text="Ver una captura de pantalla" lightbox="../media/evaluate-performance-performance-screenshots-hover.msft.png":::
   Ver una captura de pantalla  
:::image-end:::  

También puede ver capturas de pantalla eligiendo un marco en la **sección** Marcos.  DevTools muestra una versión pequeña de la captura de pantalla en el panel **Resumen.**  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview.msft.png" alt-text="Ver una captura de pantalla en el panel Resumen" lightbox="../media/evaluate-performance-performance-summary-preview.msft.png":::
   Ver una captura de pantalla en el panel **Resumen**  
:::image-end:::  

Elija la miniatura del panel **Resumen** para acercar la captura de pantalla.  

:::image type="complex" source="../media/evaluate-performance-performance-summary-preview-select.msft.png" alt-text="Acercar una captura de pantalla desde el panel Resumen" lightbox="../media/evaluate-performance-performance-summary-preview-select.msft.png":::
   Acercar una captura de pantalla desde el panel **Resumen**  
:::image-end:::  

### <a name="view-layers-information"></a>Ver información de capas  

Para ver información de capas avanzadas sobre un marco:  

1.  [Activar instrumentación de pintura avanzada](#turn-on-advanced-paint-instrumentation).  
1.  Elija un marco en la **sección Marcos.**  DevTools muestra información sobre las capas del nuevo panel **Capas,** junto al panel **Registro de** eventos.  
    
    :::image type="complex" source="../media/evaluate-performance-layers-all.msft.png" alt-text="Panel Capas" lightbox="../media/evaluate-performance-layers-all.msft.png":::
       Panel **Capas**  
    :::image-end:::  
    
Mantenga el mouse sobre una capa para resaltarla en el diagrama.  

:::image type="complex" source="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png" alt-text="Resaltar una capa" lightbox="../media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png":::
   Resaltar una capa  
:::image-end:::  

Para mover el diagrama:  

*   Elija **Modo panorámica** \( Modo panorámica ![ \) para desplazarse por los ](../media/pan-mode-icon.msft.png) ejes X e Y.  
*   Elija **Girar modo** \( Girar modo \) para girar a lo largo del eje ![ ](../media/rotate-mode-icon.msft.png) Z.  
*   Elija **Restablecer transformación** \( Restablecer transformación ![ ](../media/reset-transform-icon.msft.png) \) para restablecer el diagrama a la posición original.  
    
### <a name="view-paint-profiler"></a>Ver el perfilador de pintura  

Para ver información avanzada sobre un evento de pintura:  

1.  [Activar](#turn-on-advanced-paint-instrumentation).  
1.  Elija un **evento Paint** en la **sección** Main.  
    
    :::image type="complex" source="../media/evaluate-performance-paint-profiler.msft.png" alt-text="Panel De perfiles de pintura" lightbox="../media/evaluate-performance-paint-profiler.msft.png":::
       Panel **De perfiles de pintura**  
    :::image-end:::  
    
## <a name="analyze-rendering-performance-with-the-rendering-tool"></a>Analizar el rendimiento de representación con la herramienta de representación  

Use las características del panel **Representación** para ayudar a visualizar el rendimiento de representación de la página.  

Para abrir la **herramienta de** representación:  

1.  [Abra el menú de comandos][DevToolsCommandMenu].  
1.  Comience a escribir `Rendering` y seleccione `Show Rendering` .  DevTools muestra la **herramienta de** representación en la parte inferior de la ventana DevTools.  
    
    :::image type="complex" source="../media/evaluate-performance-console-drawer-rendering.msft.png" alt-text="La herramienta de representación" lightbox="../media/evaluate-performance-console-drawer-rendering.msft.png":::
       La **herramienta de representación**  
    :::image-end:::  
    
### <a name="view-frames-per-second-in-realtime-with-the-fps-meter"></a>Ver fotogramas por segundo en tiempo real con el medidor FPS  

El **medidor FPS** es una superposición que aparece en la esquina superior derecha de la ventanilla.  Proporciona una estimación en tiempo real de FPS a medida que se ejecuta la página.  Para abrir el **medidor FPS:**  

1.  Abra la **herramienta De representación.**  [Analizar el rendimiento de representación con la herramienta de representación](#analyze-rendering-performance-with-the-rendering-tool).  
1.  Activa la casilla **Fps Meter.**  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png" alt-text="El medidor fps" lightbox="../media/evaluate-performance-jank-console-rendering-frame-rate.msft.png":::
       El **medidor fps**  
    :::image-end:::  
    
### <a name="view-painting-events-in-realtime-with-paint-flashing"></a>Ver eventos de pintura en tiempo real con Paint Flashing  

Use Paint Flashing para obtener una vista en tiempo real de todos los eventos de pintura de la página.  Cada vez que se vuelve a pintar una parte de la página, DevTools describe esa sección en verde.  

Para activar Paint Flashing, complete las siguientes acciones.  

1.  Abra la **herramienta De representación.**  Vaya a [Analizar el rendimiento de representación con la herramienta de representación](#analyze-rendering-performance-with-the-rendering-tool).  
1.  Activa la casilla **Destello de pintura.**  
    
    :::image type="complex" source="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png" alt-text="Paint Flashing" lightbox="../media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png":::
       **Paint Flashing**  
    :::image-end:::  
    
### <a name="view-an-overlay-of-layers-with-layer-borders"></a>Ver una superposición de capas con bordes de capa  

Usa **Bordes de capa** para ver una superposición de bordes de capa y mosaicos en la parte superior de la página.  

Para activar bordes de capa, realice las siguientes acciones,  

1.  Abra la **herramienta De representación.**  Vaya a [Analizar el rendimiento de representación con la herramienta de representación](#analyze-rendering-performance-with-the-rendering-tool).  
1.  Activa la casilla **Bordes de** capa.  
    
    :::image type="complex" source="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png" alt-text="Bordes de capa" lightbox="../media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png":::
       **Bordes de capa**  
    :::image-end:::  
    
Vaya a los comentarios de [debug_colors.cc para][ChromiumDebugColors] obtener una explicación de las codificaciones de color.  

### <a name="find-scroll-performance-issues-in-realtime"></a>Buscar problemas de rendimiento de desplazamiento en tiempo real  

Use Problemas de rendimiento de desplazamiento para identificar los elementos de la página que tienen escuchas de eventos relacionadas con el desplazamiento que pueden dañar el rendimiento de la página.  
DevTools describe los elementos potencialmente problemáticos en la teal.  

Para ver problemas de rendimiento de desplazamiento, complete las siguientes acciones. 

1.  Abra la **herramienta De representación.**  Vaya a [Analizar el rendimiento de representación con la herramienta de representación](#analyze-rendering-performance-with-the-rendering-tool).  
1.  Active la casilla **Problemas de rendimiento de desplazamiento.**  
    
    :::image type="complex" source="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png" alt-text="Problemas de rendimiento de desplazamiento indica que los objetos restringidos por ventanilla sin capa pueden dañar el rendimiento del desplazamiento" lightbox="../media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png":::
       **Problemas de rendimiento de desplazamiento** indica que los objetos restringidos por ventanilla sin capa pueden dañar el rendimiento del desplazamiento  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Herramientas para desarrolladores de Microsoft Edge (Chromium) | Microsoft Docs"  
[DevToolsCommandMenu]: ../command-menu/index.md#open-the-command-menu "Abra el menú Comando: ejecute comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsEvaluatePerformanceGettingStarted]: ./index.md "Introducción al análisis del rendimiento en tiempo de ejecución | Microsoft Docs"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Demostración de pestañas de actividad | glitch"  

[ChromiumDebugColors]: https://cs.chromium.org/chromium/src/cc/debug/debug_colors.cc "debug_colors.cc: búsqueda de código"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

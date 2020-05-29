---
title: Referencia de análisis de rendimiento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: acd6e3e68f89096cf80c08f0d0c3430ab31eaec1
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611751"
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
1.  Haga **clic en grabar** ![ Registro ][ImageRecordIcon] .  
    
    > ##### Figura 1  
    > **Grabar**  
    > ![Grabar][ImageRecord]  

1.  Interactúe con la página.  DevTools registra toda la actividad de la página que se produce como resultado de las interacciones.  
1.  Vuelva a hacer clic en **grabar** o haga clic en **detener** para detener la grabación.  

### Registrar el rendimiento de la carga   

Registre el rendimiento de la carga cuando desee analizar el rendimiento de una página mientras se está cargando, en lugar de ejecutarse.  

1.  Vaya a la página que desea analizar.  
1.  Abra el panel **rendimiento** de DevTools.  
1.  Haga clic en actualizar página de actualización de **Página** ![ ][ImageRefreshPageIcon] .  DevTools registra las métricas de rendimiento mientras se actualiza la página y, a continuación, detiene automáticamente la grabación un par de segundos después de que finalice la carga.  
    
    > ##### Figura 2  
    > **Actualizar página**  
    > ![Actualizar página][ImageRefreshPage]  

DevTools automáticamente acerca de la parte de la grabación donde se produjo la mayor parte de la actividad.  

> ##### Imagen 3  
> Una grabación de página  
> ![Una grabación de página][ImageLoadRecording]  

### Capturar capturas de pantallas durante la grabación   

Active la casilla **capturas** de pantalla para capturar una captura de pantalla de cada fotograma mientras graba.  

> ##### Imagen 4  
> La casilla de verificación **capturas de pantallas**  
> ![La casilla de verificación capturas de pantallas][ImageScreenshots]  

Consulte [ver una captura de pantalla](#view-a-screenshot) para obtener información sobre cómo interactuar con capturas de pantalla.  

### Forzar recolección de elementos no utilizados al grabar   

Mientras graba una página, haga clic en **recopilar** elementos no usados recolectar basura ![ ][ImageCollectGarbageIcon] para forzar la recolección de elementos no utilizados.  

> ##### Imagen 5  
> Recopilar basura  
> ![Recopilar basura][ImageCollectGarbage]  

### Mostrar configuración de grabación   

Haga clic en **capturar** ![ configuración ][ImageCaptureSettingsIcon] de captura de configuración para exponer más opciones de configuración relacionadas con el modo en que DevTools captura las grabaciones de rendimiento.  

> ##### Imagen 6  
> La sección **configuración de captura**  
> ![La sección configuración de captura][ImageCaptureSettings]  

### Deshabilitar ejemplos de JavaScript   

De forma predeterminada, la sección **principal** de una grabación muestra las pilas de llamadas detalladas de las funciones de JavaScript a las que se llamó durante la grabación.  Para deshabilitar estas pilas de llamadas:  

1.  Abra el menú de **configuración de captura** .  Consulte [Mostrar configuración de grabación](#show-recording-settings).  
1.  Active la casilla **deshabilitar ejemplos de JavaScript** .  
1.  Realizar una grabación de la página.  

En las [figuras 7](#figure-7) y [8](#figure-8) se muestra la diferencia entre deshabilitar y habilitar ejemplos de JavaScript.  La sección **principal** de la grabación es mucho más corta cuando el muestreo está deshabilitado, porque omite todas las pilas de llamadas de JavaScript.  

> ##### Imagen 7  
> Ejemplo de una grabación cuando se deshabilitan los ejemplos de JS  
> ![Ejemplo de una grabación cuando se deshabilitan los ejemplos de JS][ImageJSSamplesDisabled]  

> ##### Imagen 8  
> Ejemplo de una grabación cuando se habilitan ejemplos de JS  
> ![Ejemplo de una grabación cuando se habilitan ejemplos de JS][ImageJSSamplesEnabled]  

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

> ##### Imagen 9  
> **Guardar perfil**  
> ![Guardar perfil][ImageSaveProfile]  

## Cargar una grabación   

Para cargar una grabación, haga clic con el botón derecho y seleccione **cargar perfil**.  

> ##### Imagen 10  
> **Cargar perfil**  
> ![Cargar perfil][ImageLoadProfile]  

## Borrar la grabación anterior   

Después de realizar una grabación, presione **Borrar** grabación ![ Borrar grabación ][ImageClearRecordingIcon] para borrar esa grabación en el panel **rendimiento** .  

> ##### Imagen 11  
> Borrar grabación  
> ![Borrar grabación][ImageClearRecording]  

## Analizar una grabación de rendimiento   

Después de [grabar el rendimiento en tiempo de ejecución](#record-runtime-performance) o el rendimiento de la [carga de registros](#record-load-performance), el panel **rendimiento** proporciona una gran cantidad de datos para analizar el rendimiento de lo que sucedió.  

### Seleccionar una parte de una grabación   

Arrastre el ratón hacia la izquierda o hacia la derecha en la **información general** para seleccionar una parte de una grabación.  La **información general** es la sección que contiene los gráficos de **fps**, **CPU**y **net** .  

> ##### Imagen 12  
> Arrastrar el mouse por la información general para zoom  
> ![Arrastrar el mouse por la información general para zoom][ImageZoom]  

Para seleccionar una parte con el teclado:  

1.  Haga clic en el fondo de la sección **principal** o en cualquiera de las secciones que hay junto a ella, como **interacciones**, **red**o **GPU**.  Este flujo de trabajo de teclado solo funciona cuando una de estas secciones está en el foco.  
1.  Use las `W` teclas,, `A` `S` , `D` para acercar, mover a la izquierda, alejar y desplazar a la derecha, respectivamente.  

Para seleccionar una parte con un panel táctil:  

1.  Mantenga el mouse sobre la sección **Descripción general** o en la sección de **detalles** .  La sección de **información general** es el área que contiene los gráficos de **fps**, **CPU**y **net** .  La sección de **detalles** es el área que contiene la sección **principal** , la sección **interacciones** , etc.  
1.  Con dos dedos, deslice el dedo hacia arriba para alejar, deslice el dedo hacia la izquierda, deslice el dedo hacia abajo y deslice el dedo hacia la derecha para desplazarse hacia la derecha.  

Para desplazarse por un gráfico de llamas largo en la sección **principal** o en cualquiera de los vecinos, haga clic y mantenga presionado mientras arrastra hacia arriba o hacia abajo.  Arrastre hacia la izquierda y hacia la derecha para mover qué parte de la grabación está seleccionada.  

### Buscar actividades   

Pulse `Control` + `F` \ (Windows \) o `Command` + `F` \ (MacOS \) para abrir el cuadro de búsqueda en la parte inferior del panel **rendimiento** .  

> ##### Imagen 13  
> Uso de Regex en el cuadro de búsqueda de la parte inferior de la ventana para encontrar cualquier actividad que comience con `E`  
> ![El cuadro de búsqueda][ImageSearch]  

Para navegar por las actividades que coinciden con la consulta:  

*   Use los **Previous** ![ botones anterior ][ImagePreviousIcon] y **siguiente** ![ siguiente ][ImageNextIcon] .  
*   Pulse `Shift` + `Enter` para seleccionar la anterior o `Enter` para seleccionar la siguiente.  

Para modificar la configuración de la consulta:  

*   Pulse mayúsculas de minúsculas **distingue mayúsculas** ![ de minúsculas ][ImageSearchCaseIcon] para hacer distinción entre mayúsculas y minúsculas.  
*   Presione **Regex** ![ regex ][ImageSearchRegexIcon] para usar una expresión regular en la consulta.  

Para ocultar el cuadro de búsqueda, presione **Cancelar**.  

### Ver actividad de subproceso principal   

Use la sección **principal** para ver la actividad que se produjo en el subproceso principal de la página.  

> ##### Imagen 14  
> La sección **principal**  
> ![La sección principal][ImageMain]  

Haga clic en un evento para ver más información sobre él en la pestaña **Resumen** .  DevTools describe el evento seleccionado.  

> ##### Imagen 15  
> Más información sobre la `anonymous` función en la pestaña **Resumen**  
> ![Más información sobre la función anónima en la pestaña Resumen][ImageMainEventSummary]  

DevTools representa la actividad principal del subproceso con un gráfico de llama.  El eje x representa la grabación a lo largo del tiempo.  El eje y representa la pila de llamadas.  Los eventos en la parte superior provocan los eventos que se encuentran por debajo.  

> ##### Imagen 16  
> Un gráfico de llama en la sección **principal**  
> ![Un gráfico de llamas][ImageFlameChart]  

En la [figura 16](#figure-16), un `click` evento ha provocado un `Function Call` en en la `activitytabs.js` línea 53.  A continuación `Function Call` , verá que se llamó a una función anónima.  La función anónima a la que se llamó, a la que llamó `a` `wait` `Minor GC` .  

DevTools asigna scripts a colores aleatorios.  En la [figura 16](#figure-16), las llamadas de función de un script se muestran coloreadas en verde.  Las llamadas desde otra secuencia de comandos tienen color beige.  El amarillo más oscuro representa la actividad de scripting y el evento morado representa la actividad de representación.  Estos eventos amarillos y amarillos más oscuros son coherentes en todas las grabaciones.  

Consulte [deshabilitar muestras de JavaScript](#disable-javascript-samples) si desea ocultar el gráfico detallado de llamadas de JavaScript.  Cuando se deshabilitan los ejemplos de JS, solo verá eventos de alto nivel, como `Event: click` y `Function Call` de la [figura 16](#figure-16).  

### Ver actividades en una tabla   

Después de grabar una página, no es necesario basarse únicamente en la sección **principal** para analizar las actividades.  DevTools también proporciona tres vistas tabulares para analizar actividades.  Cada vista le ofrece una perspectiva diferente en las actividades:  

*   Cuando desee ver las actividades raíz que producen el mayor trabajo, use [la pestaña **árbol de llamadas** ](#the-call-tree-tab).  
*   Cuando desee ver las actividades en las que el más tiempo se dedicó directamente, use [la pestaña **de la parte inferior** ](#the-bottom-up-tab).  
*   Cuando desee ver las actividades en el orden en el que se produjeron durante la grabación, use [la pestaña **registro de eventos** ](#the-event-log-tab).  

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

> ##### Imagen 17  
> La ficha **árbol de llamadas**  
> ![La ficha árbol de llamadas][ImageCallTree]  

En la [ilustración 17](#figure-17), el nivel superior de los elementos de la columna **actividad** , como `Evaluate Script` y `Parse HTML` son las actividades raíz.  El anidamiento representa la pila de llamadas.  Por ejemplo, en la [figura 17](#figure-17), `Parse HTML` que causó `Evaluate Script` el `Compile Script` `(anonymous)` .  

El **tiempo propio** representa el tiempo que pasa directamente en esa actividad.  **Tiempo total** representa el tiempo invertido en esa actividad o en cualquiera de los elementos secundarios.  

Haga clic en **tiempo propio**, en **tiempo total**o en **actividad** para ordenar la tabla por esa columna.  

Use el cuadro de texto **filtrar** para filtrar eventos por nombre de actividad.  

De forma predeterminada, el menú **agrupar** se establece en **sin agrupar**.  Use el menú **agrupar** para ordenar la tabla actividad según varios criterios.  

Haga clic en **Mostrar pila más pesado** ![ Mostrar pila más pesada ][ImageShowHeaviestStackIcon] para revelar otra tabla a la derecha de la tabla **actividad** .  Haga clic en una actividad para rellenar la tabla de **pila más intensa** .  La tabla **pila más pesada** muestra qué elementos secundarios de la actividad seleccionada tardaron más tiempo en ejecutarse.  

#### La pestaña abajo   

Use la pestaña **de abajo** para ver las actividades que se ocuparon directamente la mayor parte del tiempo en el agregado.  

La pestaña de la **parte inferior** solo muestra actividades durante la parte seleccionada de la grabación.  Para obtener más información sobre cómo seleccionar partes, vea [seleccionar una parte de una grabación](#select-a-portion-of-a-recording) .  

> ##### Ilustración 18  
> La pestaña **abajo**  
> ![La pestaña abajo][ImageBottomUp]  

En el gráfico de llama de la sección **principal** de la [figura 18](#figure-18), vea que casi prácticamente todo el tiempo se dedicó a ejecutarse `Parse HTML` .  La actividad principal en la pestaña de la **parte inferior** de la [figura 18](#figure-18) es `Parse HTML` .  <!--In the flame chart of [Figure 18](#figure-18), the yellow below the calls to `wait` are actually thousands of `Minor GC` calls.  -->  Consulte en la pestaña de la **parte inferior** , la actividad más costosa es `Layout` .  

La columna **Self Time** representa el tiempo agregado directamente en esa actividad, en todas las apariciones.  

La columna **tiempo total** representa el tiempo agregado invertido en esa actividad o en cualquiera de los elementos secundarios.  

#### La ficha registro de eventos   

Use la pestaña **registro de eventos** para ver las actividades en el orden en el que se produjeron durante la grabación.  

La pestaña **registro de eventos** solo muestra actividades durante la parte seleccionada de la grabación.  Para obtener más información sobre cómo seleccionar partes, vea [seleccionar una parte de una grabación](#select-a-portion-of-a-recording) .  

> ##### Ilustración 19  
> La ficha **registro de eventos**  
> ![La ficha registro de eventos][ImageEventLog]  

La columna **hora de inicio** representa el punto en el que se inició la actividad, en relación con el inicio de la grabación.  Por ejemplo, la hora de inicio del `175.7 ms` elemento seleccionado en la [figura 19](#figure-19) significa que la actividad comenzó el 175,7 ms después de que se iniciara la grabación.  

La columna **Self Time** representa el tiempo invertido directamente en esa actividad.  

La columna **tiempo total** representa el tiempo invertido directamente en esa actividad o en cualquiera de los elementos secundarios.  

Haga clic en **hora de inicio**, tiempo **propio**o **tiempo total** para ordenar la tabla por esa columna.

Use el cuadro de texto **filtrar** para filtrar las actividades por nombre.  

Use el menú **duración** para filtrar todas las actividades que hayan tardado menos de 1 ms o de 15 ms.  De forma predeterminada, el menú **duración** se establece en **todos**, lo que significa que se muestran todas las actividades.  

Deshabilite las casillas de verificación **cargar**, **scripting**, **procesamiento**o **pintura** para filtrar todas las actividades de esas categorías.  

### Ver actividad de la GPU   

Ver la actividad de la GPU en la sección **GPU** .  

> ##### Ilustración 20  
> La sección **GPU**  
> ![La sección GPU][ImageGpu]  

### Ver actividad rasterizada   

Ver la actividad rasterizada en la sección de **trama** .  

> ##### Ilustración 21  
> La sección **trama**  
> ![La sección trama][ImageRaster]  

### Ver interacciones   

Use la sección **interacciones** para buscar y analizar las interacciones del usuario que se produjeron durante la grabación.  

> ##### Ilustración 22  
> La sección **interacciones**  
> ![La sección interacciones][ImageInteractions]  

Una línea roja en la parte inferior de una interacción representa el tiempo dedicado a esperar el subproceso principal.  

Haga clic en una interacción para ver más información sobre ella en la pestaña **Resumen** .  

### Analizar fotogramas por segundo (FPS)   

DevTools proporciona numerosas formas de analizar fotogramas por segundo:  

*   Use [el gráfico de **fps** ](#the-fps-chart) para obtener una visión general de los FPS durante la grabación.  
*   Use [la sección **Marcos** ](#the-frames-section) para ver cuánto tarda un marco en particular.  
*   Use el **medidor de fps** para una estimación en tiempo real de fps a medida que se ejecuta la página.  Consulte [Ver fotogramas por segundo en tiempo real con el medidor de fps](#view-frames-per-second-in-realtime-with-the-fps-meter).  

#### El gráfico de FPS   

El gráfico **fps** proporciona una descripción general de la velocidad de fotogramas en toda la duración de una grabación.  En general, cuanto más alto sea la barra verde, mejor será la velocidad de fotogramas.  

Una barra roja encima del gráfico de **fps** es una advertencia de que la velocidad de fotogramas ha disminuido tan poco que probablemente se ha dañado la experiencia del usuario.  

> ##### Ilustración 23  
> El gráfico de FPS  
> ![El gráfico de FPS][ImageFpsChart]  

#### La sección marcos   

La sección **Marcos** le indica exactamente cuánto tarda un marco en particular.  

Mantenga el mouse sobre un marco para ver una información sobre herramientas con más información sobre ella.  

> ##### Ilustración 24  
> Mantener el puntero sobre un marco  
> ![Mantener el puntero sobre un marco][ImageFramesSection]  

Haga clic en un marco para ver más información sobre el marco en la pestaña **Resumen** .  DevTools esquematiza el fotograma seleccionado en azul.  

> ##### Ilustración 25  
> Visualización de un marco en la pestaña **Resumen**  
> ![Visualización de un marco en la pestaña Resumen][ImageFrameSummary]  

### Ver solicitudes de red   

Expanda la sección **red** para ver una cascada de solicitudes de red que se produjeron durante la grabación.  

> ##### Ilustración 26  
> La sección **red**  
> ![La sección red][ImageNetworkRequest]  

Las solicitudes se codifican en colores de la siguiente manera:  

*   HTML: azul  
*   CSS: morado  
*   JS: amarillo  
*   Imágenes: verde  

Haga clic en una solicitud para ver más información sobre ella en la pestaña **Resumen** .  Por ejemplo, en la [figura 26](#figure-26) , la pestaña **Resumen** muestra más información sobre la solicitud azul seleccionada en la sección **red** .  

Un cuadrado de color azul más oscuro en la parte superior izquierda de una solicitud significa que es una solicitud de mayor prioridad.  Un cuadrado más claro significa menor prioridad.  Por ejemplo, en la [figura 26](#figure-26) , el azul, la solicitud seleccionada es de mayor prioridad y el verde que está debajo es de menor prioridad.  

En la [ilustración 27](#figure-27), la solicitud de `www.bing.com` se representa mediante una línea en la parte izquierda, una barra en el centro con una parte oscura y una parte clara, y una línea a la derecha.  En la [Ilustración 28](#figure-28) se muestra la representación correspondiente de la misma solicitud en la pestaña **intervalos** del panel **red** .  A continuación se muestra cómo se asignan entre sí estas dos representaciones:

*   La línea izquierda es todo hasta el `Connection Start` grupo de eventos, ambos incluidos.  En otras palabras, es todo lo antes `Request Sent` y exclusivo.  
*   La parte clara de la barra es `Request Sent` y `Waiting (TTFB)` .  
*   La parte oscura de la barra es `Content Download` .  
*   Esencialmente, la línea adecuada es el tiempo dedicado a esperar el hilo principal.  Esto no se representa en la pestaña **intervalos** .  

> ##### Ilustración 27  
> Representación de barra de línea de la `www.bing.com` solicitud  
> ![La representación de barra de línea de la solicitud www.bing.com][ImageLineBar]  

> ##### Ilustración 28  
> Representación de la ficha **intervalos** de la `www.bing.com` solicitud  
> ![La sección red][ImageTiming]  

### Ver métricas de memoria   

Active la casilla **memoria** para ver las métricas de memoria de la última grabación.  

> ##### Ilustración 29  
> La casilla **memoria**  
> ![La casilla memoria][ImageMemory]  

DevTools muestra un nuevo gráfico de **memoria** , encima de la pestaña **Resumen** .  También hay un nuevo gráfico debajo del gráfico **net** , denominado **montón**.  El gráfico de **montones** proporciona la misma información que la línea de **montón JS** en el gráfico de **memoria** .  

> ##### Ilustración 30  
> Métrica de memoria, encima de la pestaña **Resumen**  
> ![Métricas de memoria][ImageMemoryMetrics]  

Las líneas de color del gráfico se asignan a las casillas coloreadas encima del gráfico.  
Desactive una casilla para ocultar la categoría en el gráfico.  

El gráfico solo muestra la región de la grabación que está seleccionada actualmente.  Por ejemplo, en la [figura 30](#figure-30), el gráfico de **memoria** solo muestra el uso de memoria de aproximadamente la marca de MS 400 a la marca de 1750 ms.  

### Ver la duración de una parte de una grabación   

Al analizar una sección como la **red** o **Main**, a veces necesitarás una estimación más precisa de cuánto tiempo han tardado determinados eventos.  Espera `Shift` , haga clic y mantenga presionado y arrastre hacia la izquierda o la derecha para seleccionar una parte de la grabación.  En la parte inferior de la selección, DevTools muestra cuánto tiempo duró esa parte.  

> ##### Ilustración 31  
> La `9.47ms` marca de tiempo de la parte inferior de la parte seleccionada indica cuánto tiempo duró esa parte  
> ![Visualización de la duración de una parte de una grabación][ImageDuration]  

### Ver una captura de pantalla   

Consulte [capturar capturas de pantallas mientras graba](#capture-screenshots-while-recording) para obtener información sobre cómo habilitar capturas de pantallas.  

Pase el puntero por la **información general** para ver una captura de pantalla de cómo se vio la página durante ese momento de la grabación.  La **información general** es la sección que contiene los gráficos de **CPU**, **fps**y **net** .  

> ##### Ilustración 32  
> Ver una captura de pantalla  
> ![Ver una captura de pantalla][ImageViewScreenshot]  

También puede ver capturas de pantallas haciendo clic en un marco de la sección **Marcos** .  DevTools muestra una versión reducida de la captura de pantalla en la pestaña **Resumen** .  

> ##### Ilustración 33  
> Después de hacer clic `233.9ms` en el marco de la sección de **Marcos** , se muestra la captura de pantalla de ese marco en la pestaña **Resumen** .  
> ![Ver una captura de pantalla en la pestaña Resumen][ImageFrameScreenshotSummary]  

Para acercar la captura de pantalla, haga clic en la miniatura de la pestaña **Resumen** .  

> ##### Ilustración 34  
> Después de hacer clic en la miniatura en la pestaña **Resumen** , DevTools acerca la captura de pantalla.  
> ![Acercar una captura de pantalla de la pestaña Resumen][ImageFrameScreenshotZoom]  

### Ver información de capas   

Para ver la información sobre las capas avanzadas de un marco:  

1.  [Habilitar la instrumentación avanzada de pintura](#enable-advanced-paint-instrumentation).  
1.  Seleccione un marco de la sección **Marcos** .  DevTools muestra información sobre las capas en la ficha nuevas **capas** , junto a la ficha **registro de eventos** .  
    
    > ##### Ilustración 35  
    > El panel **capas**  
    > ![El panel capas][ImageLayers]  
    
Desplace el puntero sobre una capa para resaltarla en el diagrama.  

> ##### Ilustración 36  
> Resaltar **#39** de capa  
> ![Resaltar una capa][ImageLayerHover]  

Para mover el diagrama:  

*   Haga clic en modo **panorámico** ![ panorámico ][ImagePanModeIcon] para desplazarse por los ejes X e y.  
*   Haga clic en modo **rotar** ![ modo ][ImageRotateModeIcon] de giro para rotar a lo largo del eje Z.  
*   Haga clic en **restablecer** transformación de restablecimiento de transformaciones ![ ][ImageResetTransformIcon] para restablecer el diagrama a la posición original.  

### Ver generador de perfiles de pintura   

Para ver información avanzada sobre un evento de pintura:  

1.  [Habilitar la instrumentación avanzada de pintura](#enable-advanced-paint-instrumentation).  
1.  Seleccione un evento de **pintura** en la sección **principal** .  
    
    > ##### Ilustración 37  
    > Pestaña **generador de perfiles de pintura**  
    > ![Pestaña generador de perfiles de pintura][ImagePaintProfiler]  
    
## Analizar el rendimiento de la representación con la pestaña representación   

Use las características de la pestaña **representación** para poder visualizar el rendimiento de la representación de la página.  

Para abrir la pestaña **representación** :  

1.  [Abrir el menú de comandos][DevToolsCommandMenu].  
1.  Empiece `Rendering` a escribir y seleccione `Show Rendering` .  DevTools muestra la ficha **representación** en la parte inferior de la ventana de DevTools.  
    
    > ##### Ilustración 38  
    > La pestaña **representación**  
    > ![La pestaña representación][ImageRenderingTab]  
    
### Ver fotogramas por segundo en tiempo real con el medidor de FPS   

El **medidor de fps** es una superposición que aparece en la esquina superior derecha de su ventanilla.  Proporciona una estimación en tiempo real de FPS a medida que se ejecuta la página.  Para abrir el **medidor de fps**:  

1.  Abra la pestaña **representación** .  Consulte [analizar el rendimiento de la representación con la pestaña representación](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Active la casilla de verificación de **medidor de fps** .  
    
    > ##### Ilustración 39  
    > El medidor de FPS  
    > ![El medidor de FPS][ImageFpsMeter]  
    
### Ver los eventos de pintura en tiempo real con parpadeo de pintura   

Use las intermitencias de pintura para obtener una vista en tiempo real de todos los eventos de pintura en la página.  Cada vez que se vuelve a pintar una parte de la página, DevTools esquematiza esa sección en verde.  

Para habilitar los parpadeos de pintura:  

1.  Abra la pestaña **representación** .  Consulte [analizar el rendimiento de la representación con la pestaña representación](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Active la casilla de **pintura parpadeante** .  
    
    > ##### Ilustración 40  
    > **Pintura parpadeante**  
    > ![Pintura parpadeante][ImagePaintFlashing]  
    
### Ver una superposición de capas con bordes de capas   

Use **bordes de capas** para ver una superposición de los bordes de la capa y los mosaicos en la parte superior de la página.  

Para habilitar los bordes de capas:  

1.  Abra la pestaña **representación** .  Consulte [analizar el rendimiento de la representación con la pestaña representación](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Active la casilla **bordes de capas** .  
    
    > ##### Ilustración 41  
    > **Bordes de capas**  
    > ![Bordes de capas][ImageLayerBorders]  
    
Vea los comentarios en [`debug_colors.cc`][ChromiumDebugColors] para obtener una explicación de los códigos de color.  

### Buscar problemas de rendimiento de desplazamiento en tiempo real   

Use los problemas de rendimiento de desplazamiento para identificar los elementos de la página que tienen detectores de eventos relacionados con el desplazamiento que pueden dañar el rendimiento de la página.  
DevTools subraya los elementos potencialmente problemáticos de verde azulado.  

Para ver los problemas de rendimiento del desplazamiento:  

1.  Abra la pestaña **representación** .  Consulte [analizar el rendimiento de la representación con la pestaña representación](#analyze-rendering-performance-with-the-rendering-tab).  
1.  Active la casilla de verificación de **problemas de rendimiento de desplazamiento** .  
 
    > ##### Ilustración 42  
    > Los **problemas de rendimiento de desplazamiento** indican que los objetos restringidos de ventanilla sin capas pueden dañar el rendimiento del desplazamiento  
    > ![Los problemas de rendimiento de desplazamiento indican que los objetos restringidos de ventanilla sin capas pueden dañar el rendimiento del desplazamiento][ImageScrollingPerformanceIssues]  
    

<!--    -->  



<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageClearRecordingIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-recording-icon.msft.png  
[ImageCollectGarbageIcon]: /microsoft-edge/devtools-guide-chromium/media/collect-garbage-icon.msft.png  
[ImageNextIcon]: /microsoft-edge/devtools-guide-chromium/media/next-icon.msft.png  
[ImagePanModeIcon]: /microsoft-edge/devtools-guide-chromium/media/pan-mode-icon.msft.png  
[ImagePreviousIcon]: /microsoft-edge/devtools-guide-chromium/media/previous-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-page-icon.msft.png  
[ImageResetTransformIcon]: /microsoft-edge/devtools-guide-chromium/media/reset-transform-icon.msft.png  
[ImageRotateModeIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-mode-icon.msft.png  
[ImageSearchCaseIcon]: /microsoft-edge/devtools-guide-chromium/media/search-case-icon.msft.png  
[ImageSearchRegexIcon]: /microsoft-edge/devtools-guide-chromium/media/search-regex-icon.msft.png  
[ImageShowHeaviestStackIcon]: /microsoft-edge/devtools-guide-chromium/media/show-heaviest-stack-icon.msft.png  

[ImageRecord]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-record-highlight.msft.png "Ilustración 1: registro"  
[ImageRefreshPage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refresh-button.msft.png "Ilustración 2: actualizar página"  
[ImageLoadRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed.msft.png "Ilustración 3: una grabación de carga de página"  
[ImageScreenshots]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-screenshots-checkbox.msft.png "Figura 4: la casilla de verificación capturas de pantallas"  
[ImageCollectGarbage]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-collect-garbage-button.msft.png "Ilustración 5: recopilar los elementos no usados"  
[ImageCaptureSettings]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings-button-open-drawer.msft.png "Ilustración 6: la sección de configuración de captura"  
[ImageJSSamplesDisabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-on.msft.png "Ilustración 7: un ejemplo de una grabación cuando se deshabilitan los ejemplos de JS"  
[ImageJSSamplesEnabled]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off.msft.png "Ilustración 8: un ejemplo de una grabación cuando se habilitan los ejemplos de JS"  
[ImageSaveProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-save-profile.msft.png "Ilustración 9: guardar perfil"  
[ImageLoadProfile]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-load-profile.msft.png "Ilustración 10: cargar perfil"  
[ImageClearRecording]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-refreshed-disable-javascript-samples-checkbox-off-clear-button.msft.png "Ilustración 11: borrar grabación"  
[ImageZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-zoom-highlighted.msft.png "Ilustración 12: arrastrar el mouse por la información general para zoom"  
[ImageSearch]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-search-regex.msft.png "Ilustración 13: el cuadro de búsqueda"  
[ImageMain]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Ilustración 14: la sección principal"  
[ImageMainEventSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-me.msft.png "Ilustración 15: más información sobre la función anónima en la pestaña Resumen"  
[ImageFlameChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-flame-chart.msft.png "Ilustración 16: un gráfico de llama"  
[ImageCallTree]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-call-tree.msft.png "Ilustración 17: la ficha árbol de llamadas"  
[ImageBottomUp]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-bottoms-up.msft.png "Ilustración 18: la pestaña de abajo arriba"  
[ImageEventLog]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-event-log.msft.png "Ilustración 19: ficha registro de eventos"  
[ImageGpu]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-gpu-zoomed.msft.png "Ilustración 20: la sección GPU"  
[ImageRaster]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-raster.msft.png "Ilustración 21: la sección de trama"  
[ImageInteractions]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-interactions-animation.msft.png "Ilustración 22: la sección Interactions"  
[ImageFpsChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-highlight.msft.png "Ilustración 23: el gráfico de FPS"  
[ImageFramesSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-hover.msft.png "Ilustración 24: mantener el puntero sobre un marco"  
[ImageFrameSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-summary.msft.png "Ilustración 25: visualización de un marco en la pestaña Resumen"  
[ImageNetworkRequest]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-network.msft.png "Ilustración 26: la sección red"  
[ImageLineBar]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-performance-network.msft.png "Ilustración 27: representación de barra de línea de la solicitud www.bing.com"  
[ImageTiming]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-network-timing.msft.png "Ilustración 28: la sección red"  
[ImageMemory]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-highlight.msft.png "Ilustración 29: la casilla memoria"  
[ImageMemoryMetrics]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-memory-chart.msft.png "Ilustración 30: métrica de memoria"  
[ImageDuration]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-duration.msft.png "Ilustración 31: visualización de la duración de una parte de una grabación"  
[ImageViewScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshots-hover.msft.png "Ilustración 32: ver una captura de pantalla"  
[ImageFrameScreenshotSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview.msft.png "Ilustración 33: ver una captura de pantalla en la pestaña Resumen"  
[ImageFrameScreenshotZoom]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-preview-select.msft.png "Ilustración 34: zoom en una captura de pantalla de la pestaña Resumen"  
[ImageLayers]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-layers-all.msft.png "Ilustración 35: el panel capas"  
[ImageLayerHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frames-document-nav-bar-highlighted.msft.png "Ilustración 36: resaltado de una capa"  
[ImagePaintProfiler]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-paint-profiler.msft.png "Ilustración 37: la pestaña generador de perfiles de Paint"  
[ImageRenderingTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-console-drawer-rendering.msft.png "Ilustración 38: la pestaña representación"  
[ImageFpsMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-frame-rate.msft.png "Ilustración 39: el medidor de FPS"  
[ImagePaintFlashing]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-jank-console-rendering-paint-flashing.msft.png "Ilustración 40: parpadeo de la pintura"  
[ImageLayerBorders]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-devtools-console-rendering-layer-borders.msft.png "Ilustración 41: bordes de capas"  
[ImageScrollingPerformanceIssues]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-bing-console-drawer-rendering-scrolling-performance-issues.msft.png "Ilustración 42: los problemas de rendimiento de desplazamiento indican que los objetos restringidos de ventanilla sin capas pueden dañar el rendimiento del desplazamiento"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index#open-the-command-menu "Abrir el menú de comandos: ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  
[DevtoolsEvaluatePerformanceGettingStarted]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/index "Empezar a analizar el rendimiento en tiempo de ejecución"  

[ActivityTabsDemo]: https://microsoft-edge-chromium-devtools.glitch.me/perf/activitytabs.html "Demostración de pestañas de actividades"  

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

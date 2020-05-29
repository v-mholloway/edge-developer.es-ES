---
description: Use el panel rendimiento para analizar la responsivenes de la página durante la interacción del usuario.
title: 'DevTools: rendimiento'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, rendimiento, perfil, velocidad de fotogramas, fps, uso de CPU, ejecución de JavaScript
ms.custom: seodec18
ms.openlocfilehash: aecf3cf49592dbf1f24231e76f14ddc2ca1228c3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573810"
---
# Rendimiento

El panel **rendimiento** ofrece herramientas para la generación de perfiles y el análisis de la capacidad de respuesta de la interfaz de usuario durante el curso de interacción del usuario. Con ella, puedes hacer lo siguiente:

 - [Medir los tiempos de ejecución](#recording-a-profile) de los distintos componentes de la página 
 - [Profundice hasta dónde gasta la mayoría de los ciclos de CPU](#timeline-ruler) para ejecutar la página y el efecto visual resultante para sus usuarios
 - [Obtener un desglose paso a paso de los procesos que](#timeline-details) consumen el tiempo de ejecución de la página 
 - [Recorra las pilas de llamadas de JavaScript](#javascript-call-stacks) para identificar operaciones costosas, como las que requieren recálculos de diseño 

![Panel de rendimiento de DevTools](./media/performance.png)

## Grabación de un perfil

El primer paso para analizar el rendimiento de la página es capturar un perfil a medida que realiza un escenario de usuario determinado, como los pasos de reproducción de un error de rendimiento que está tratando de corregir o un caso de uso típico que desea optimizar para una mejor experiencia de usuario. 

### Barra de herramientas

Use los **Start**  /  **Stop** botones de inicio de la barra de herramientas (o `Ctrl+E` ) para iniciar y concluir el seguimiento de rendimiento. En la pestaña **rendimiento** , se aparecerá un indicador verde para indicar que hay una grabación en curso. 

![Barra de herramientas del panel rendimiento](./media/performance_toolbar.png)

Se generará un informe de rendimiento al detener el perfil. Puede guardarla en Disk ( `Ctrl+S` ) y volver a cargarla ( `Ctrl+O` ) en DevTools en otro momento.  Las sesiones de diagnóstico de DevTools se guardan con la extensión *. diagsession* .

Estas son algunas de las cosas que debe tener en cuenta al grabar un perfil:

- Realice el menor número de acciones que necesita para capturar el escenario que está tratando de analizar. Las acciones extrañas con la página generarán datos adicionales y abarrotarán los resultados.

- El generador de perfiles marca automáticamente los principales eventos de ciclo de vida de la aplicación en el informe, como navegación de páginas, [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded)y [carga](https://developer.mozilla.org/docs/Web/Events/load)de páginas. Puedes agregar marcadores personalizados llamando al método [performance. Mark ()](https://developer.mozilla.org/docs/Web/API/Performance/mark) desde el código o la consola. 

- Si los tiempos iniciales de carga de la página son importantes para el análisis, asegúrese de borrar la memoria caché del explorador (del panel [red](./network.md) ) para asegurarse de que todos los recursos de página se cargan desde la red.

- A veces, ayuda a grabar varias sesiones o a probar el mismo escenario en diferentes equipos para comprender mejor el problema de rendimiento en la naturaleza.

## Regla de escala de tiempo

La escala de tiempo funciona como regla de deslizamiento. Utilícelo para limitar el ámbito del informe al período de tiempo (o intervalo de eventos) en particular. Arrastre los **controles** de la diapositiva negra para limitar el intervalo de tiempo que desea investigar y filtrar datos de generación de perfiles extraños de los informes de [escala](#timeline-details) de tiempo y pilas de [llamadas de JavaScript](#javascript-call-stacks) en el panel de *detalles*inferior. 

Verá dos tipos de marcadores en la regla:

 - Las **marcas del ciclo de vida** de la aplicación en la escala de tiempo (como la navegación de páginas, [DOMContentLoaded](https://developer.mozilla.org/docs/Web/Events/DOMContentLoaded)y la [carga](https://developer.mozilla.org/docs/Web/Events/load)de páginas) se registran automáticamente al grabar un perfil.

 - Las **marcas de usuario** son marcadores personalizados que puede elegir para agregar con las llamadas al método [performance. Mark ()](https://developer.mozilla.org/docs/Web/API/Performance/mark) desde el código o la [**consola**](./console.md)de DevTools. Puede agrupar las marcas de *Inicio* y *finalización* juntas como una medida única con nombre con el método [performance. Measure ()](https://developer.mozilla.org/docs/Web/API/Performance/measure) . 

Una vez que haya seleccionado un intervalo de tiempo, puede **ampliar su zoom** desde la barra de herramientas o restablecer la selección de **zoom** y **borrar la selección** para volver a la vista completa de la traza de rendimiento (sin intervalo de tiempo seleccionado). Estos controles también están disponibles en el menú contextual.

![Escala de tiempo del panel rendimiento](./media/performance_timeline.png)

### Uso de la CPU

El gráfico de escala de tiempo **% de uso de CPU** describe los recursos de procesamiento consumidos por los diversos subsistemas del explorador necesarios para ejecutar la página, desglosados por Categoría:

#### Cargando
Indica el tiempo invertido en la recuperación de recursos de aplicaciones y el análisis de HTML y CSS. Esto puede incluir solicitudes de red. Los siguientes eventos asociados se registran en la [línea de tiempo](#timeline-details):

Evento | Descripción
:------------ | :-------------
CssParsing  | Se ha encontrado nuevo contenido CSS que necesitaba ser analizado.
HtmlParsing | Se encontró nuevo contenido HTML que necesitaba redistribuirse en los nodos e insertarse en el DOM.
HttpRequest | Se ha encontrado un recurso remoto en el DOM o se ha creado una XMLHttpRequest que requirió que se realizara una solicitud HTTP.
HtmlSpeculativeDownloading | Se estaban buscando los recursos necesarios en el contenido HTML de la página para que las solicitudes HTTP para ellos pudieran programarse lo antes posible.


#### Scripting
Indica que el tiempo invertido en el análisis y la ejecución de JavaScript. Esto incluye eventos DOM, temporizadores, evaluación de scripts y devoluciones de llamada de marcos de animación. Los siguientes eventos asociados se registran en la [línea de tiempo](#timeline-details):

Evento | Descripción
:------------ | :-------------
DomEvent | Se activó un evento en un objeto DOM.
EvaluatingScript | Se ha `<script>` encontrado un nuevo elemento en el Dom y es necesario analizarlo y ejecutarlo.
EventHandler | Se activó una escucha de eventos registrada en respuesta a un evento DOM desencadenado.
Marco | Mientras se preparó un nuevo marco, se activó una devolución de llamada registrada para que pudiera aportar cambios visuales.
Medida | Se midió un escenario específico de la aplicación con el `performance.measure()` método.
MediaQueryListener | Se invalidó una consulta de medios registradas que resultó en la ejecución de sus escuchas asociadas.
MutationObserver | Se modificó uno o más elementos DOM observados que dieron como resultado la ejecución de una devolución de llamada asociada de MutationObserver.
TimerFired | Un temporizador programado transcurrió el resultado de la ejecución de su devolución de llamada asociada.
WindowsRuntimeAsyncCallback | Un objeto de Windows en tiempo de ejecución que desencadenó una devolución de llamada completó una operación asincrónica `Promise` .
WindowsRuntimeEvent | Se activó un evento en un objeto de Windows en tiempo de ejecución que desencadenó una escucha registrada.

#### GEN
Indica el tiempo dedicado a la recopilación de memoria para objetos que ya no se usan. Los siguientes eventos asociados se registran en la [línea de tiempo](#timeline-details):

Evento | Descripción
:------------ | :-------------
GarbageCollection | El tiempo de ejecución de JavaScript ha auditado el uso de memoria actual de la aplicación para determinar los objetos a los que ya no se hace referencia y que, por lo tanto, se pueden recopilar.

#### Toque
Indica el tiempo dedicado a calcular la presentación y el diseño de elementos. Los siguientes eventos asociados se registran en la [línea de tiempo](#timeline-details):

Evento | Descripción
:------------ | :-------------
AlignedBeat | Los cambios visuales pendientes que se realizaron en el DOM se procesaron para que se pudiera actualizar la pantalla de la aplicación.
CssCalculation | Se realizaron cambios en el DOM o se agregó nuevo contenido CSS, lo que requiere que se vuelvan a calcular las propiedades de estilo de todos los elementos afectados.
Diseño | Se realizaron cambios en el DOM que requirieron calcular el tamaño o la posición de todos los elementos afectados.

#### Representación
Indica el tiempo invertido en pintar la pantalla. Los siguientes eventos asociados se registran en la [línea de tiempo](#timeline-details):

Evento | Descripción
:------------ | :-------------
Paint | Se hicieron cambios visuales en el DOM que requirieron redibujar todas las partes afectadas de la página.
RenderLayer | Se hicieron cambios visuales a un fragmento representado de forma independiente del DOM (denominado una capa) que requirieron que se redibuje su parte respectiva de la página.

#### Descodificación de imágenes
Indica el tiempo invertido en la descompresión y la descodificación de imágenes. Los siguientes eventos asociados se registran en la [línea de tiempo](#timeline-details):

Evento | Descripción
:------------ | :-------------
ImageDecoded | Se incluyó una imagen en el DOM y era necesario descomprimirla a partir de su formato original en un mapa de bits.

### Rendimiento visual

El gráfico **rendimiento visual (FPS)** muestra los *fotogramas estimados por segundo* (FPS) durante el escenario de generación de perfiles, donde 60 fps es la velocidad de visualización ideal. Los DIP en la velocidad de fotogramas indican cuellos de botella y una velocidad de fotogramas de cero significa que los fotogramas se eliminan por completo.

## Detalles de la escala de tiempo

Use el panel de detalles de último para obtener el desglose completo de lo que sucedió en la página. La pestaña detalles de la **escala de tiempo** proporciona un desglose de los eventos que se produjeron en los diversos subsistemas del explorador.

![Panel de detalles de escala de tiempo](./media/performance_details_timeline.png)

1. **Control de ordenación de lista de eventos**

    Use el control de cuadro desplegable **ordenar por** para alternar el orden de la [lista de eventos](#event-list) entre la *hora de inicio* o la *duración (inclusive*). Esto también cambia la vista de los [detalles de la escala de tiempo seleccionada](#selected-timeline-details).

2. **Agrupar eventos por marco**

    Use los **eventos de nivel superior de grupo por fotogramas** para alternar entre los eventos de nivel superior (*análisis de HTML, diseño, evento DOM,* etc.) en la unidad de trabajo correspondiente (o "fotogramas") durante los períodos de tiempo en que se producían las animaciones/actualizaciones visuales. Los marcos se tratan como otros eventos, por lo que se pueden ordenar o filtrar y proporcionar un resumen de *tiempo inclusivo* al hacer clic en la [lista de eventos](#event-list).

3. **Controles de filtro de lista de eventos**

    Use el menú **filtrar eventos** para configurar los tipos de eventos que se muestran en detalles de la [escala de tiempo](#timeline-details). 

    ![Control para filtrar eventos de rendimiento](./media/performance_filter_events.png) 

    Están disponibles los siguientes filtros:

   - **Descodificación de imágenes**: muestra los eventos que se produjeron en un subproceso en segundo plano (por ejemplo, descodificación de imagen, GC). 
   - **Tráfico de red**: mostrar las solicitudes HTTP que estaban enlazadas a la red.
   - **Actividad**de la interfaz de usuario: Mostrar eventos que se produjeron en el subproceso de interfaz de usuario o subproceso de representación (por ejemplo, controladores de eventos DOM, diseño).
   - **Medidas de usuario**: Mostrar eventos personalizados que indican llamadas al método performance. Measure ().

     Puede filtrar los eventos de nivel superior por su duración inclusiva.

### Lista de eventos

La *lista de eventos* le ofrece una lista cronológica de [los sucesos del subsistema del explorador](#cpu-utilization) que se produjeron durante el período de tiempo seleccionado. 

Haga clic en cualquier entrada para rellenar el gráfico de **detalles de eventos seleccionado** para ese elemento. Las entradas con funciones o eventos anidados mostrarán el tiempo **incluido** (tiempo dedicado a ejecutar la función *y* cualquier otra función a la que se llamó) y **exclusivas** (el tiempo invertido solo dentro del cuerpo de la misma función de llamada) en el gráfico.

Haga clic con el botón derecho en cualquier entrada para abrir el menú contextual para filtrar solo la escala de tiempo y ver el código fuente responsable del evento en el [**depurador**](./debugger.md) (o en el panel [**elementos**](./elements.md) , si procede).

### Detalles de la escala de tiempo seleccionada

Los *detalles de la escala de tiempo seleccionada* proporcionan un gráfico de barras detallado de los tiempos de eventos inclusivos o inclusivos durante el intervalo de tiempo seleccionado. Cuando se ordena por *duración (inclusive)* con el **control de ordenación**de la lista de eventos, los eventos que se ejecutan más de forma visual destacan visualmente en este gráfico. 

### Detalles del evento seleccionado

Este informe proporciona más información sobre el evento seleccionado, incluyendo la *hora de inicio*, el tipo de subproceso en ejecución (por ejemplo, *descarga*, *interfaz de usuario*, *representación*) y otros detalles contextuales específicos del tipo de evento específico. Por ejemplo, los tipos de *detectores de eventos* proporcionan vínculos de depurador a la *función de devolución* de llamada y la pila de *llamadas de programación*.

## Pilas de llamadas de JavaScript

![Intervalos de rendimiento para las pilas de llamadas de JavaScript](./media/performance_details_javascript.png)

La pestaña **pilas de llamadas de JavaScript** proporciona información sobre el uso de la CPU y los intervalos de las funciones de script que se ejecutaron durante el intervalo de tiempo seleccionado:

 Columna | Descripción
:------------ | :-------------
Nombre de la función | Nombre del explorador o de la función definida por el usuario.
CPU inclusiva (%) | Porcentaje de actividad de CPU seleccionada en esta función y en funciones llamadas por esta función.
CPU exclusiva (%) | Porcentaje de actividad de CPU seleccionada en esta función, excepto la actividad en las funciones llamadas por esta función.
CPU inclusiva (MS) | Tiempo de CPU dedicado a ejecutar código en esta función y en funciones llamadas por esta función.
CPU exclusiva (MS) | Tiempo de CPU dedicado a ejecutar código de esta función, excluido el tiempo de las funciones llamadas por esta función.
Dirección URL | Direcciones URL donde se produjo el marco de pila. Las llamadas de función que se originan desde el explorador (API Web basadas en estándares) se etiquetan como *[Dom]*.

## Abreviados

| Acción                         | Método abreviado     |
|:-------------------------------|:-------------|
| Iniciar o detener sesión de generación de perfiles | `Ctrl` + `E` |
| Importar sesión de generación de perfiles       | `Ctrl` + `O` |
| Exportar sesión de generación de perfiles       | `Ctrl` + `S` |

## Problemas conocidos

### Se produjo un error al iniciar la sesión de generación de perfiles

Si ve este mensaje de error: **se ha producido un error al iniciar la sesión de generación de perfiles** en la herramienta rendimiento, siga estos pasos para obtener una solución alternativa.

1. Presione `Windows Key`  +  `R` .

2. En el cuadro de diálogo Ejecutar, escriba **Services. msc**.
![problemas conocidos-1](./media/known_issues_1.PNG)

3. Busque el **servicio Recopilador estándar de Microsoft (R) Diagnostics Hub** y haga clic en él con el botón secundario del ratón.
![problemas conocidos-2](./media/known_issues_2.PNG)

4. Reinicie el **servicio Recopilador estándar del concentrador de diagnósticos de Microsoft (R)**.
![problemas conocidos-3](./media/known_issues_3.PNG)

5. Cierre las herramientas para desarrolladores de Microsoft Edge y la pestaña. Abra una nueva pestaña, vaya a la página y presione `F12` .

6. Ahora debería poder comenzar a crear perfiles.
![problemas conocidos-4](./media/known_issues_4-performance.PNG)

¿Aún tiene problemas? Envíenos sus comentarios con el icono para **Enviar comentarios** . 

![problemas conocidos-5](./media/known_issues_5.PNG)

### Se produjo un error al detener la sesión de generación de perfiles.

Si ve este mensaje de error: **se ha producido un error al detener la sesión de generación de perfiles** en la herramienta rendimiento, siga estos pasos para obtener una solución alternativa.

1. Presione `Windows Key`  +  `R` .

2. En el cuadro de diálogo Ejecutar, escriba **Services. msc**.
![problemas conocidos-1](./media/known_issues_1.PNG)

3. Busque el **servicio Recopilador estándar de Microsoft (R) Diagnostics Hub** y haga clic en él con el botón secundario del ratón.
![problemas conocidos-2](./media/known_issues_2.PNG)

4. Reinicie el **servicio Recopilador estándar del concentrador de diagnósticos de Microsoft (R)**.
![problemas conocidos-3](./media/known_issues_3.PNG)

5. Cierre las herramientas para desarrolladores de Microsoft Edge y la pestaña. Abra una nueva pestaña, vaya a la página y presione `F12` .

6. Ahora debería poder comenzar a crear perfiles.
![problemas conocidos-4](./media/known_issues_4-performance.PNG)

¿Aún tiene problemas? Envíenos sus comentarios con el icono para **Enviar comentarios** . 

![problemas conocidos-5](./media/known_issues_5.PNG)

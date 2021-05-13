---
description: Obtenga información sobre cómo usar Microsoft Edge y DevTools para encontrar problemas de memoria que afecten al rendimiento de la página, como pérdidas de memoria, distensión de memoria y recolecciones de elementos no utilizados frecuentes.
title: Solucionar problemas de memoria
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 3b2405d23dd6ee349484c9ba66d195e3ed12144b
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565032"
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
# <a name="fix-memory-problems"></a>Solucionar problemas de memoria  

Obtenga información sobre cómo usar Microsoft Edge y DevTools para encontrar problemas de memoria que afecten al rendimiento de la página, como pérdidas de memoria, distensión de memoria y recolecciones de elementos no utilizados frecuentes.  

### <a name="summary"></a>Resumen  

*   Descubra la cantidad de memoria que la página está usando actualmente con el administrador de tareas Microsoft Edge explorador.  
*   Visualice el uso de memoria con el tiempo con el panel **Memoria.**  
*   Identifique los árboles DOM desasociados \(una causa común de pérdidas de memoria\) con **instantánea de montón**.  
*   Descubra cuándo se asigna nueva memoria en el montón de JavaScript \(JS heap\) con instrumentación de asignación **en la escala de tiempo**.  

## <a name="overview"></a>Información general  

En el sentido del modelo de rendimiento **RAIL,** el foco de sus esfuerzos de rendimiento deben ser los usuarios.  

<!--todo: add RAIL section when available  -->  

Los problemas de memoria son importantes porque los usuarios suelen percibirlo.  Los usuarios pueden percibir problemas de memoria de las siguientes maneras:  

*   **El rendimiento de una página empeora progresivamente con el tiempo**.  Esto es posiblemente un síntoma de una pérdida de memoria.  Una pérdida de memoria es cuando un error en la página hace que la página use cada vez más memoria con el tiempo.  
*   **El rendimiento de una página es coherentemente malo.**  Este es posiblemente un síntoma del exceso de memoria.  El exceso de memoria es cuando una página usa más memoria de la necesaria para una velocidad de página óptima.  
*   **El rendimiento de una página se retrasa o parece pausar con frecuencia**.  Este es posiblemente un síntoma de las recolecciones de elementos no utilizados frecuentes.  La recolección de elementos no utilizados es cuando el explorador recupera memoria.  El explorador decide cuándo sucede esto.  Durante las colecciones, se pausa todo el script que se ejecuta.  Por lo tanto, si el explorador está recopilando muchos elementos no utilizados, el tiempo de ejecución del script se va a pausar mucho.  

### <a name="memory-bloat-how-much-is-too-much"></a>Bloat de memoria: ¿cuánto es "demasiado"?  

Una pérdida de memoria es fácil de definir.  Si un sitio usa cada vez más memoria de forma progresiva, tendrá una pérdida.  Pero la bloat de memoria es un poco más difícil de anclar.  ¿Qué califica como "usar demasiada memoria"?  

Aquí no hay números duros, ya que los distintos dispositivos y exploradores tienen capacidades diferentes.  La misma página que se ejecuta sin problemas en un smartphone de gama alta puede bloquearse en un smartphone de gama baja.  

La clave aquí es usar el modelo RAIL y centrarse en los usuarios.  Descubra qué dispositivos son populares entre los usuarios y, a continuación, pruebe la página en esos dispositivos.  Si la experiencia es coherentemente mala, es posible que la página supere las capacidades de memoria de esos dispositivos.  

## <a name="monitor-memory-use-in-realtime-with-the-microsoft-edge-browser-task-manager"></a>Supervisar el uso de memoria en tiempo real con el Administrador de tareas Microsoft Edge explorador  

Use el administrador Microsoft Edge de tareas del explorador como punto de partida para la investigación de problemas de memoria.  El Microsoft Edge de tareas del explorador es un monitor en tiempo real que le indica la cantidad de memoria que está usando actualmente una página.  

1.  Seleccione o navegue hasta el menú Microsoft Edge principal y elija Más herramientas Administrador de tareas del explorador para abrir Microsoft Edge administrador de `Shift` + `Esc` tareas ****  >  **** del explorador.  
    
    :::image type="complex" source="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png" alt-text="Abrir el administrador Microsoft Edge de tareas del explorador" lightbox="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png":::
       Figura 1: Abrir el administrador de tareas Microsoft Edge explorador  
    :::image-end:::  
    
1.  Mantenga el mouse en el encabezado de la tabla del Administrador de tareas del explorador Microsoft Edge, abra el menú contextual \(hacer clic con el botón secundario\) y habilite **la memoria de JavaScript**.  
    
    :::image type="complex" source="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png" alt-text="Habilitar memoria de JavaScript" lightbox="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png":::
       Figura 2: Habilitar memoria de JavaScript  
    :::image-end:::  
    
Estas dos columnas le dicen cosas diferentes acerca de cómo usa la memoria la página.  

*   La **columna Memoria** representa la memoria nativa.  Los nodos DOM se almacenan en la memoria nativa.  Si este valor aumenta, se crean nodos DOM.  
*   La **columna Memoria de JavaScript** representa el montón js.  Esta columna contiene dos valores.  El valor que le interesa es el número vivo \(el número entre paréntesis\).  El número directo representa la cantidad de memoria que usan los objetos accesibles en la página.  Si este número aumenta, se crean objetos nuevos o los objetos existentes están creciendo.  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <a name="visualize-memory-leaks-with-performance-panel"></a>Visualizar pérdidas de memoria con el panel Rendimiento  

También puede usar el panel Rendimiento como otro punto de partida de la investigación.  El panel Rendimiento le ayuda a visualizar el uso de memoria de una página a lo largo del tiempo.  

1.  Abra el panel **Rendimiento** en DevTools.  
1.  Active la casilla **Memoria.**  
1.  [Realizar una grabación][DevtoolsEvaluatePerformanceReferenceRecord].  

> [!TIP]
> Es una buena práctica iniciar y finalizar la grabación con una recolección de elementos no utilizados forzada.  Para forzar la recolección de elementos no utilizados, elija el botón **de** recolección de elementos no utilizados de la fuerza ![ de ][ImageForceGarbageCollectionIcon] recolección de elementos no utilizados durante la grabación.  

Para demostrar las grabaciones de memoria, tenga en cuenta el código siguiente:  

```javascript
var x = [];
function grow() {
    for (var i = 0; i < 10000; i++) {
        document.body.appendChild(document.createElement('div'));
    }
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

Cada vez que se elige el botón al que se hace referencia en el código, se anexan diez mil nodos al cuerpo del documento y se inserta una cadena de un millón de caracteres en `div` `x` la `x` matriz.  Al ejecutar el ejemplo de código anterior, se produce una grabación en **el** panel Rendimiento como la siguiente figura.  

:::image type="complex" source="../media/memory-problems-glitch-example-1-performance-memory.msft.png" alt-text="Crecimiento sencillo" lightbox="../media/memory-problems-glitch-example-1-performance-memory.msft.png":::
   Figura 3: Crecimiento simple  
:::image-end:::  

En primer lugar, una explicación de la interfaz de usuario.  El **gráfico HEAP** del panel **Información general** \(debajo de **NET**\) representa el montón de JS.  Debajo del **panel** Información general se encuentra **el panel** Contador.  El uso de memoria se desglosa mediante el montón de JS \(igual que el gráfico **HEAP** en el **panel** Información general\), documentos, nodos DOM, escuchas y memoria GPU.  Desactiva una casilla para ocultarla del gráfico.  

Ahora, un análisis del código en comparación con la figura anterior.  Si revisa el contador de nodos \(el gráfico verde\), coincide limpiamente con el código.  El número de nodos aumenta en pasos discretos.  Puede suponer que cada aumento en el número de nodos es una llamada a `grow()` .  El gráfico de montón JS \(el gráfico azul\) no es tan sencillo.  De acuerdo con los procedimientos recomendados, la primera **** inmersión es en realidad una recolección forzada de elementos no utilizados \(elija el botón de recolección de elementos no utilizados fuerza ![ de ][ImageForceGarbageCollectionIcon] recolección\).  A medida que avanza la grabación, se muestran los picos de tamaño del montón de JS.  Esto es natural y esperado: el código JavaScript está creando los nodos DOM en cada botón que elija y haciendo mucho trabajo cuando crea la cadena de un millón de caracteres.  La clave aquí es el hecho de que el montón JS termina más alto de lo que empezó \(el "principio" aquí es el punto después de la recolección forzada de elementos no utilizados\).  En el mundo real, si ves este patrón de aumento del tamaño del montón de JS o el tamaño de nodo, puede definir potencialmente una pérdida de memoria.  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <a name="discover-detached-dom-tree-memory-leaks-with-heap-snapshots"></a>Detectar pérdidas de memoria de árbol DOM desasociadas con instantáneas de montón  

Un nodo DOM solo se recopila cuando no hay referencias al nodo desde el árbol DOM o el código JavaScript que se ejecuta en la página.  Se dice que un nodo se "desasocia" cuando se quita del árbol DOM, pero algún JavaScript todavía hace referencia a él.  Los nodos DOM separados son una causa común de pérdidas de memoria.  Esta sección le enseña a usar los perfiles de montón en DevTools para identificar nodos separados.  

Este es un ejemplo sencillo de nodos DOM separados.  

```javascript
var detachedTree;

function create() {
    var ul = document.createElement('ul');
    for (var i = 0; i < 10; i++) {
        var li = document.createElement('li');
        ul.appendChild(li);
    }
    detachedTree = ul;
}
document.getElementById('create').addEventListener('click', create);
```  

Al elegir el botón al que se hace referencia en el código, se crea un `ul` nodo con diez `li` secundarios.  El código hace referencia a los nodos, pero no existen en el árbol DOM, por lo que cada uno se desasocia.  

Las instantáneas de montón son una forma de identificar nodos separados.  Como su nombre indica, las instantáneas de montón muestran cómo se distribuye la memoria entre los objetos JS y los nodos DOM de la página en el momento de la instantánea.  

Para crear una instantánea, abra DevTools y vaya al **panel** Memoria, elija el botón de **radio** Instantánea de montón > botón **Tomar instantánea.**  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png" alt-text="Tomar instantánea de montón" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png":::
   Figura 4: Tomar instantánea de montón  
:::image-end:::  

La instantánea puede tardar algún tiempo en procesarse y cargarse.  Una vez finalizada, selecciónelo en el panel izquierdo \(denominado **INSTANTÁNEAS DE HEAP**\).  

Escriba `Detached` en el cuadro de texto **Filtro** de clase para buscar árboles DOM desasociados.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png" alt-text="Filtrado de nodos separados" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png":::
   Figura 5: Filtrado de nodos separados  
:::image-end:::  

Expanda los quilates para investigar un árbol separado.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png" alt-text="Investigar árbol desasociado" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png":::
   Figura 6: Investigar árbol desasociado  
:::image-end:::  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

Elija un nodo para investigarlo más a fondo.  En el **panel Objetos,** puede revisar más información sobre el código que hace referencia a él.  Por ejemplo, en la figura siguiente, la `detachedNodes` variable hace referencia al nodo.  Para corregir la pérdida de memoria en particular, debe estudiar el código que usa la variable y asegurarse de que la referencia al nodo se quita cuando ya no es `detachedUNode` necesaria.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png" alt-text="Investigar un nodo" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png":::
   Figura 7: Investigación de un nodo  
:::image-end:::  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <a name="identify-js-heap-memory-leaks-with-allocation-instrumentation-on-timeline"></a>Identificar pérdidas de memoria de montón de JS con instrumentación de asignación en la escala de tiempo  

**La instrumentación de** asignación en la escala de tiempo es otra herramienta que puede ayudarle a realizar un seguimiento de las pérdidas de memoria en el montón de JS.  

Demostrar **instrumentación de asignación en la escala de**  tiempo con el código siguiente.  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

Cada vez que se inserta el botón al que se hace referencia en el código, se agrega una cadena de un millón de caracteres a la `x` matriz.  

Para grabar un instrumental de asignación en la escala de **** tiempo, abra DevTools, **** vaya al **panel** Memoria, elija el botón de radio **** Instrumentación de asignación en la escala de tiempo, elija el botón Inicio, realice la acción que sospeche que está causando la pérdida de memoria y, a continuación, elija el botón Detener la grabación del perfil de montón de almacenamiento dinámico cuando haya ![ ][ImageStopRecordingIcon] terminado.  

Mientras graba, observe si las barras azules se muestran en la instrumentación de asignación en la escala de tiempo, como en la siguiente figura.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png" alt-text="Nuevas asignaciones" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png":::
   Figura 8: Nuevas asignaciones  
:::image-end:::  

Esas barras azules representan nuevas asignaciones de memoria.  Esas nuevas asignaciones de memoria son sus candidatos para pérdidas de memoria.  Puede acercar una barra para filtrar el **panel Constructor** para mostrar solo los objetos que se asignaron durante el período de tiempo especificado.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png" alt-text="Escala de tiempo de asignación ampliada" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png":::
   Figura 9: Escala de tiempo de asignación ampliada  
:::image-end:::  

Expanda el objeto y seleccione el valor para ver más detalles en el **panel** Objeto.  Por ejemplo, en la siguiente figura, en los detalles del objeto recién asignado indica que se asignó a la `x` variable en el `Window` ámbito.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png" alt-text="Detalles del objeto" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png":::
   Figura 10: Detalles del objeto  
:::image-end:::  

## <a name="investigate-memory-allocation-by-function"></a>Investigar la asignación de memoria por función  

Use el **tipo de generación** de perfiles de muestreo de asignación para ver la asignación de memoria mediante la función JavaScript.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png" alt-text="Muestreo de asignación de registros" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png":::
   Figura 11: Muestreo de asignación de registros  
:::image-end:::  

1.  Elija el **botón de radio Asignación de** muestreo.  Si hay un trabajador en la página, puede seleccionarlo como el destino de generación de perfiles mediante el menú desplegable situado junto al **botón** Inicio.  
1.  Elija el **botón** Inicio.  
1.  Complete las acciones de la página web que desea investigar.  
1.  Elija el **botón** Detener cuando haya terminado todas las acciones.  

DevTools muestra un desglose de la asignación de memoria por función.  La vista predeterminada es **Heavy (Bottom Up),** que muestra las funciones que asignaron la mayor cantidad de memoria en la parte superior.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png" alt-text="Muestreo de asignación" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png":::
   Figura 12: Muestreo de asignación  
:::image-end:::  

## <a name="spot-frequent-garbage-collections"></a>Detectar colecciones de elementos no utilizados frecuentes  

Si la página parece pausar con frecuencia, es posible que tenga problemas de recolección de elementos no utilizados.  

Puede usar el Administrador de tareas Microsoft Edge explorador o grabaciones de memoria de rendimiento para detectar la recolección de elementos no utilizados frecuente.  En el Administrador Microsoft Edge de tareas del **** explorador, los valores de memoria o memoria **de JavaScript** que aumentan y bajan con frecuencia representan la recolección de elementos no utilizados frecuente.  En las grabaciones de rendimiento, los cambios frecuentes \(ascendentes y caídos\) en los gráficos de recuento de nodos o montón de JS indican una recolección de elementos no utilizados frecuente.  

Después de identificar el problema, puede **** usar un instrumental de asignación en la grabación de escala de tiempo para averiguar dónde se asigna la memoria y qué funciones están causando las asignaciones.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageForceGarbageCollectionIcon]: ../media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: ../media/stop-recording-icon.msft.png  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Rendimiento de registros: referencia de análisis de rendimiento"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

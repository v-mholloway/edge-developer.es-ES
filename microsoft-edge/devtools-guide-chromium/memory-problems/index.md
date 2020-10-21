---
description: Obtenga información sobre cómo usar Microsoft Edge y DevTools para buscar problemas de memoria que afecten al rendimiento de la página, como pérdidas de memoria, recarga de memoria y recolecciones de elementos no utilizados frecuentes.
title: Solucionar problemas de memoria
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 1d8a24fc360dc307471be33544c9c707736be06d
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125457"
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

# Solucionar problemas de memoria  

Obtenga información sobre cómo usar Microsoft Edge y DevTools para buscar problemas de memoria que afecten al rendimiento de la página, como pérdidas de memoria, recarga de memoria y recolecciones de elementos no utilizados frecuentes.  

### Resumen  

*   Averigüe cuánta memoria está usando actualmente la página con el administrador de tareas del explorador Microsoft Edge.  
*   Visualice el uso de memoria a lo largo del tiempo con el panel **memoria** .  
*   Identifique los árboles DOM desvinculados \ (una causa común de fugas de memoria \) con la **instantánea de montón**.  
*   Averigüe cuándo se va a asignar una nueva memoria en el montón \ (JS heap \) con **instrumentación de asignación en la escala de tiempo**.  

## Introducción  

En el espíritu del modelo de rendimiento **ferroviario** , el enfoque de los esfuerzos de rendimiento debe ser los usuarios.  

<!--todo: add RAIL section when available  -->  

Los problemas de memoria son importantes porque a menudo son perceptibles para los usuarios.  Los usuarios pueden percibir problemas de memoria de las siguientes maneras:  

*   **El rendimiento de una página se vuelve gradualmente con el tiempo**.  Esto es posiblemente un síntoma de pérdida de memoria.  Una pérdida de memoria se produce cuando un error en la página hace que la página use progresivamente más y más memoria a lo largo del tiempo.  
*   **El rendimiento de una página es constantemente incorrecto**.  Esto es posiblemente un síntoma de recarga de memoria.  El recargado de memoria es cuando una página utiliza más memoria de la necesaria para una velocidad de página óptima.  
*   **El rendimiento de una página se retrasa o parece que se pausa con frecuencia**.  Esto es posiblemente un síntoma de recolecciones de elementos no utilizados frecuentes.  La recolección de elementos no utilizados se recolecta cuando el explorador reclama memoria.  El explorador decide cuando esto sucede.  Durante las colecciones, todo el script en ejecución está en pausa.  Por lo tanto, si el explorador está recolectando un lote, el tiempo de ejecución de script se detendrá mucho.  

### Saturación de memoria: ¿Cuánto es "demasiado"?  

Una pérdida de memoria es fácil de definir.  Si un sitio está usando progresivamente más y más memoria, tendrá una fuga.  Pero la saturación de la memoria es un poco más difícil de anclar.  ¿Qué califica como "usando demasiada memoria"?  

No hay números fuertes aquí, ya que los distintos dispositivos y exploradores tienen funciones diferentes.  La misma página que se ejecuta sin problemas en smartphones de gama alta puede bloquearse en un smartphone de low-end.  

La clave aquí es usar el modelo de raíl y centrarse en los usuarios.  Averigüe qué dispositivos son populares con los usuarios y, a continuación, pruebe la página en esos dispositivos.  Si la experiencia es constantemente incorrecta, es posible que la página exceda las capacidades de memoria de esos dispositivos.  

## Supervisar el uso de memoria en tiempo real con el administrador de tareas del explorador Microsoft Edge  

Use el administrador de tareas del explorador Microsoft Edge como punto de partida para la investigación de problemas de memoria.  El administrador de tareas del explorador Microsoft Edge es un monitor en tiempo real que indica la cantidad de memoria que está usando una página en ese momento.  

1.  Seleccione `Shift` + `Esc` o vaya al menú principal de Microsoft Edge y elija **más herramientas**  >  **Administrador de tareas del explorador** para abrir el administrador de tareas del explorador Microsoft Edge.  
    
    :::image type="complex" source="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png":::
       Ilustración 1: abrir el administrador de tareas del explorador Microsoft Edge  
    :::image-end:::  
    
1.  Mantenga el mouse en el encabezado de tabla del administrador de tareas del explorador Microsoft Edge, abra el menú contextual \ (haga clic con el botón derecho \) y habilite la **memoria JavaScript**.  
    
    :::image type="complex" source="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png":::
       Ilustración 2: habilitar la memoria de JavaScript  
    :::image-end:::  
    
Estas dos columnas le indican diferentes cosas sobre el uso de la memoria por la página.  

*   La columna **memoria** representa la memoria nativa.  Los nodos DOM se almacenan en la memoria nativa.  Si este valor aumenta, se crean los nodos DOM.  
*   La columna **memoria de JavaScript** representa el montón de JS.  Esta columna contiene dos valores.  El valor que te interesa es el número en vivo \ (el número entre paréntesis \).  El número en vivo representa la cantidad de memoria que usan los objetos que se pueden encontrar en la página.  Si este número está aumentando, se crean objetos nuevos o los objetos existentes crecen.  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## Visualizar pérdidas de memoria con el panel rendimiento  

También puede usar el panel rendimiento como otro punto de partida en su investigación.  El panel rendimiento le ayuda a visualizar el uso de memoria de una página a lo largo del tiempo.  

1.  Abra el panel de **rendimiento** en DevTools.  
1.  Active la casilla **memoria** .  
1.  [Hacer una grabación][DevtoolsEvaluatePerformanceReferenceRecord].  

> [!TIP]
> Es recomendable iniciar y finalizar la grabación con una recolección de elementos no utilizados forzada.  Seleccione el botón **recopilar** eliminación de elementos no usados ![ en la ][ImageForceGarbageCollectionIcon] grabación para forzar la recolección de elementos no utilizados.  

Para hacer una demostración de las grabaciones de la memoria, considere el siguiente código:  

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

Cada vez que se presiona el botón al que se hace referencia en el código, `div` los nodos de 10000 se anexan al cuerpo del documento y se inserta una cadena de 1 millón `x` caracteres en la `x` matriz.  La ejecución del ejemplo de código anterior produce una grabación en el panel de **rendimiento** como la siguiente ilustración.  

:::image type="complex" source="../media/memory-problems-glitch-example-1-performance-memory.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-1-performance-memory.msft.png":::
   Ilustración 3: crecimiento simple  
:::image-end:::  

En primer lugar, una explicación de la interfaz de usuario.  El gráfico de **montones** en el panel de **información general** \ (debajo de **net**\) representa el montón de JS.  Debajo del panel de **información general** se encuentra el panel de **contador** .  Aquí puede ver el uso de memoria desglosado por montones de JS \ (igual al gráfico de **montón** en el panel de **información general** \), documentos, nodos DOM, oyentes y memoria de GPU.  Al deshabilitar una casilla, la oculta del gráfico.  

Ahora, un análisis del código comparado con la ilustración anterior.  Si miras el contador de nodos \ (el gráfico verde \), podrás ver que coincide perfectamente con el código.  El número de nodos aumenta en pasos discretos.  Puede dar por supuesto que cada aumento en el recuento de nodos es una llamada a `grow()` .  El gráfico de montón JS \ (gráfico azul \) no es tan sencillo.  Siguiendo los procedimientos recomendados, la primera DIP es, en realidad, una recolección forzada de elementos no utilizados \ (que se consigue al  **presionar el** botón de recolección de elementos no ![ utilizados ][ImageForceGarbageCollectionIcon] \).  A medida que la grabación se progrese, podrá ver que el tamaño del montón de JS es demasiado bajo.  Esto es natural y se espera: el código JavaScript crea los nodos DOM en cada pulsador de botón y realiza una gran cantidad de trabajo cuando crea la cadena de 1 millón caracteres.  Lo fundamental aquí es el hecho de que el montón JS finaliza más de lo que comenzó \ (el "comienzo" aquí es el punto después de la recolección de elementos no utilizados forzada \).  En el mundo real, si viera este patrón de aumento del tamaño de la pila de JS o del tamaño del nodo, puede definir potencialmente una pérdida de memoria.  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## Descubrir pérdidas de memoria en el árbol de DOM desvinculadas con instantáneas de montones  

Un nodo DOM solo se recolecta como no utilizado cuando no hay ninguna referencia al nodo desde el árbol DOM o el código JavaScript que se ejecuta en la página.  Se dice que un nodo está "separado" cuando se quita del árbol DOM, pero algunos JavaScript siguen haciendo referencia a él.  Los nodos DOM separados son una causa común de las pérdidas de memoria.  En esta sección aprenderá a usar los perfilers de montones en DevTools para identificar los nodos desvinculados.  

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

Al seleccionar el botón al que se hace referencia en el código, se crea un `ul` nodo con diez `li` elementos secundarios.  El código hace referencia a los nodos, pero no existen en el árbol DOM, por lo que se desasocian.  

Las instantáneas de montones son una manera de identificar los nodos desvinculados.  Como su nombre indica, las instantáneas de montones muestran cómo se distribuye la memoria entre los objetos JS y los nodos DOM de la página en el punto de tiempo de la instantánea.  

Para crear una instantánea, abra DevTools y vaya al panel **memoria** , seleccione el botón de radio de la **instantánea de montones** y, después, presione el botón **tomar instantánea** .  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png":::
   Ilustración 4: tomar instantánea de montón  
:::image-end:::  

La instantánea puede tardar algún tiempo en procesarse y cargarse.  Una vez que haya terminado, selecciónelo en el panel de la izquierda \ ( **instantáneas de montones**con nombre \).  

Escriba `Detached` el cuadro de texto **filtro de clase** para buscar árboles Dom desvinculados.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png":::
   Ilustración 5: filtrar por nodos desvinculados  
:::image-end:::  

Expanda el carats para investigar un árbol desvinculado.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png":::
   Ilustración 6: investigación de árboles desconectados  
:::image-end:::  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

Seleccione un nodo para investigarlo más a la vez.  En el panel **objetos** puede ver más información sobre el código que hace referencia.  Por ejemplo, en la siguiente ilustración se puede ver que la `detachedNodes` variable hace referencia al nodo.  Para corregir esta pérdida de memoria determinada, debe estudiar el código que usa la `detachedUNode` variable y asegurarse de que la referencia al nodo se quita cuando ya no es necesaria.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png":::
   Ilustración 7: investigar un nodo  
:::image-end:::  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## Identificar pérdidas de memoria de montón JS con instrumentación de asignación en la escala de tiempo  

La **instrumentación de asignación de la escala de tiempo** es otra herramienta que puede ayudarle a realizar un seguimiento de las pérdidas de memoria en el montón de JS.  

Muestre la **instrumentación de asignación en la escala de tiempo**  con el código siguiente.  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

Cada vez que se inserta el botón al que se hace referencia en el código, se agrega una cadena de 1 millón caracteres a la `x` matriz.  

Para grabar un instrumental de asignación en la escala de tiempo, abra DevTools, vaya al panel **memoria** , seleccione el botón **de opción instrumentación de asignación en la escala de tiempo** , presione el botón **Inicio** , realice la acción que sospecha que está causando la pérdida de memoria y, después, presione el botón Detener grabación del **montón de grabación** ![ cuando haya ][ImageStopRecordingIcon] terminado.  

Mientras graba, observe si en la línea de tiempo se muestran barras azules en la instrumentación de asignación, como en la siguiente ilustración.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png":::
   Ilustración 8: nuevas asignaciones  
:::image-end:::  

Estas barras azules representan nuevas asignaciones de memoria.  Estas nuevas asignaciones de memoria son sus candidatos para pérdidas de memoria.  Puede hacer zoom en una barra para filtrar el panel **constructor** y mostrar únicamente los objetos que se asignaron durante el período de tiempo especificado.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png":::
   Ilustración 9: escala de tiempo de asignación ampliada  
:::image-end:::  

Expanda el objeto y seleccione el valor para ver más detalles en el panel de **objetos** .  Por ejemplo, en la siguiente ilustración, al ver los detalles del objeto que se acaba de asignar, debería poder ver que se asignó a la `x` variable en el `Window` ámbito.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png":::
   Ilustración 10: detalles del objeto  
:::image-end:::  

## Investigar la asignación de memoria por función  

Use el tipo de generación de perfiles de **muestreo de asignación** para ver la asignación de memoria por función de JavaScript.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png":::
   Ilustración 11: muestreo de asignación de registros  
:::image-end:::  

1.  Seleccione el botón de opción **muestreo de asignación** .  Si hay un trabajo en la página, puede seleccionarlo como destino de la generación de perfiles con el menú desplegable situado junto al botón **Inicio** .  
1.  Pulse el botón **Inicio** .  
1.  Realice las acciones en la página que desea investigar.  
1.  Pulse el botón **detener** cuando haya finalizado todas las acciones.  

En DevTools se muestra un desglose de la asignación de memoria por función.  La vista predeterminada es **gruesa (inferior hacia arriba)**, que muestra las funciones que asignaron la mayor cantidad de memoria en la parte superior.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png":::
   Ilustración 12: muestreo de asignaciones  
:::image-end:::  

## Detectar recolecciones de basura frecuentes  

Si parece que la página se pone en pausa con frecuencia, es posible que tenga problemas de recolección de elementos no utilizados.  

Puede usar el administrador de tareas del explorador Microsoft Edge o grabaciones de la memoria de rendimiento para detectar una recolección de elementos no utilizados frecuente.  En el administrador de tareas del explorador Microsoft Edge, el aumento o la caída frecuente de **memoria** o valores de **memoria de JavaScript** representan la recolección de elementos no utilizados.  En las grabaciones de rendimiento, los cambios frecuentes \ (aumento y disminución \) en el montón de JS o los gráficos de recuento de nodos indican una recolección de elementos no utilizados frecuente.  

Después de identificar el problema, puede usar un **instrumental de asignación en** la grabación de la escala de tiempo para averiguar dónde se asigna la memoria y qué funciones están causando las asignaciones.  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageForceGarbageCollectionIcon]: ../media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: ../media/stop-recording-icon.msft.png  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Rendimiento del registro: referencia de análisis de rendimiento"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

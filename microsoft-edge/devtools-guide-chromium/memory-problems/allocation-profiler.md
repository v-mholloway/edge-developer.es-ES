---
title: Cómo usar el instrumental de asignación en la escala de tiempo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: d0a7a66a9f061d1a5d98e57269ffbcc0a0afefa4
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10985763"
---
<!-- Copyright Meggin Kearney 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->





# Cómo usar el instrumental de asignación en la escala de tiempo  



Use **instrumentación de asignación en la escala de tiempo** para buscar objetos que no se hayan recolectado correctamente y continúe manteniendo la memoria.  

## Cómo funciona el instrumental de asignación en la escala de tiempo  

La **instrumentación de asignación** de la escala de tiempo combina la información detallada de instantáneas del generador de perfiles del **montón** con la actualización incremental y el seguimiento del panel **rendimiento** .  Del mismo modo, el seguimiento de la asignación de montones para objetos implica el inicio de una grabación, la realización de una secuencia de acciones y la detención de la grabación para su análisis.  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

La **instrumentación de asignación de la escala de tiempo** toma instantáneas de montones de forma periódica en la grabación \ (con la frecuencia que cada 50 ms! \) y una instantánea final al final de la grabación.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Instrumentación de asignación en la escala de tiempo" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **Instrumentación de asignación en la escala de tiempo**  
:::image-end:::  

> [!NOTE]
> El número después del `@` es un identificador de objeto que se conserva en varias instantáneas tomadas durante la sesión de grabación.  El identificador de objeto persistente permite una comparación precisa entre los Estados de la pila.  Los objetos se mueven durante la recolección de elementos no utilizados, por lo que no tiene sentido Mostrar la dirección de un objeto.  

## Habilitar instrumentación de asignación en la escala de tiempo  

Siga estos pasos para empezar a usar el **instrumental de asignación en la escala de tiempo**.  

1.  [Abra el DevTools][DevtoolsOpenIndex].  
1.  Abra el panel **memoria** y seleccione el botón **de opción instrumentación de asignación en la escala de tiempo** .  
1.  Iniciar grabación.  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Generador de perfiles de asignaciones del montón de grabación" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       Generador de perfiles de asignaciones del montón de grabación  
    :::image-end:::  
    
## Leer una escala de tiempo de asignación del montón  

La escala de tiempo de asignación del montón muestra dónde se crean los objetos e identifica la ruta de acceso de retención.  En la siguiente ilustración, las barras de la parte superior indican cuándo se encuentran nuevos objetos en el montón.  

El alto de cada barra corresponde al tamaño de los objetos asignados recientemente, y el color de las barras indica si esos objetos siguen estando activos en la instantánea de la pila final.  Las barras azules indican que los objetos que aún están activos al final de la escala de tiempo, las barras grises indican los objetos que se asignaron durante la escala de tiempo, pero que se han recolectado como basura.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Instrumentación de asignación en instantánea de escala de tiempo" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   **Instrumentación de asignación en instantánea de escala de tiempo**  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple click actions  -->  

Puede usar los controles deslizantes de la línea de tiempo anterior para acercar ese Snapshot en particular y ver los objetos que se asignaron recientemente en ese punto:  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Acercar instantánea" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   Acercar instantánea  
:::image-end:::  

Al hacer clic en un objeto específico en el montón, se muestra el árbol de retención en la parte inferior de la instantánea del montón.  El examen de la retención de la ruta de acceso al objeto debe proporcionarle suficiente información para comprender por qué no se recopiló el objeto y debe realizar los cambios de código necesarios para quitar la referencia innecesaria.  

## Ver asignación de memoria por función   

Puede ver la asignación de memoria por función de JavaScript.  Para obtener más información [, consulte investigar la asignación de memoria por función][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction] .  

<!--
## Feedback   


-->  

<!-- links -->  

[DevToolsOpenIndex]: ../open.md "Abrir Microsoft Edge (cromo) DevTools | Microsoft docs"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Investigar la asignación de memoria por función: corrección de problemas de memoria | Microsoft docs"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Descargar un canal de Microsoft Edge"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) y está creada por [Meggin Kearney][MegginKearney] \ (editor técnico \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

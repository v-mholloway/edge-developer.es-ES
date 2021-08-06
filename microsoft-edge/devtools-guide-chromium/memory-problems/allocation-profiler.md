---
description: Use instrumentación de asignación en la escala de tiempo para buscar objetos que no se están recopilando correctamente y seguir conservando la memoria.
title: Cómo usar instrumentación de asignación en escala de tiempo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 4e029b769728446b294b4cf196be7a58b64b72c7a5e05906299b7bfe961fdb71
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11808511"
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
# <a name="how-to-use-allocation-instrumentation-on-timeline"></a>Cómo usar instrumentación de asignación en escala de tiempo  

Use **instrumentación de asignación en** la escala de tiempo para buscar objetos que no se están recopilando correctamente y seguir conservando la memoria.  

## <a name="how-allocation-instrumentation-on-timeline-works"></a>Cómo funciona la instrumentación de asignación en la escala de tiempo  

**La instrumentación de** asignación en la **** escala de tiempo combina la información detallada de instantáneas del perfilador de montón con la actualización incremental y el seguimiento del panel **Rendimiento.**  Del mismo modo, el seguimiento de la asignación de montón de objetos implica iniciar una grabación, realizar una secuencia de acciones y detener la grabación para su análisis.  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

**La instrumentación** de asignación en la escala de tiempo toma instantáneas de montón periódicamente a lo largo de la grabación \(con la frecuencia que cada 50 ms\) y una instantánea final al final de la grabación.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Instrumentación de asignación en escala de tiempo" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **Instrumentación de asignación en escala de tiempo**  
:::image-end:::  

> [!NOTE]
> El número después del es un identificador de objeto que persiste en las `@` varias instantáneas tomadas durante la sesión de grabación.  El identificador de objeto persistente permite una comparación precisa entre los estados de montón.  Los objetos se mueven durante las colecciones de elementos no utilizados, por lo que mostrar la dirección de un objeto no tiene sentido.  

## <a name="enable-allocation-instrumentation-on-timeline"></a>Habilitar instrumentación de asignación en escala de tiempo  

Complete las siguientes acciones para empezar a usar **instrumentación de asignación en la escala de tiempo**.  

1.  [Abra DevTools][DevtoolsOpenIndex].  
1.  Abra el panel **Memoria,** seleccione el botón de radio **Instrumentación de asignación en la** escala de tiempo.  
1.  Iniciar grabación.  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Registrador de asignaciones de montón" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       Registrador de asignaciones de montón  
    :::image-end:::  
    
## <a name="read-a-heap-allocation-timeline"></a>Leer una escala de tiempo de asignación de montón  

La escala de tiempo de asignación de montón muestra dónde se crean los objetos e identifica la ruta de retención.  En la siguiente figura, las barras de la parte superior indican cuándo se encuentran objetos nuevos en el montón.  

El alto de cada barra corresponde al tamaño de los objetos asignados recientemente y el color de las barras indica si esos objetos aún están en la instantánea de montón final.  Las barras azules indican objetos que aún están en vida al final de la escala de tiempo, las barras grises indican objetos que se asignaron durante la escala de tiempo, pero que desde entonces se han recopilado como elementos no utilizados.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Instrumentación de asignación en instantánea de escala de tiempo" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   **Instrumentación de asignación en instantánea de escala de** tiempo  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple choose actions  -->  

Puedes usar los controles deslizantes de la escala de tiempo anterior para acercar esa instantánea en particular y revisar los objetos que se asignaron recientemente en ese momento:  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Acercar instantáneas" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   Acercar instantáneas  
:::image-end:::  

Al elegir en un objeto específico del montón se muestra el árbol de retención en la parte inferior de la instantánea de montón.  Examinar la ruta de retención del objeto debe proporcionar suficiente información para comprender por qué no se recopiló el objeto y debe realizar los cambios de código necesarios para quitar la referencia innecesaria.  

## <a name="view-memory-allocation-by-function"></a>Ver asignación de memoria por función  

Puede ver la asignación de memoria mediante la función JavaScript.  Para obtener más información, vaya [a Investigar asignación de memoria por función][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open/index.md "Abra Microsoft Edge (Chromium) DevTools | Microsoft Docs"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Investigar asignación de memoria por función: solucionar problemas de memoria | Microsoft Docs"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Descargar un canal Microsoft Edge web"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) y es creado por [Meggin Kearney][MegginKearney] \(Technical Writer\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  

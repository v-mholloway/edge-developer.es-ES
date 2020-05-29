---
title: Cómo usar el instrumental de asignación en la escala de tiempo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: ab7a270e1d599e254aaaf4515b6898cb1d9782fc
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611737"
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





# <span data-ttu-id="e3240-103">Cómo usar el instrumental de asignación en la escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="e3240-103">How to Use Allocation Instrumentation on Timeline</span></span>  



<span data-ttu-id="e3240-104">Use **instrumentación de asignación en la escala de tiempo** para buscar objetos que no se hayan recolectado correctamente y continúe manteniendo la memoria.</span><span class="sxs-lookup"><span data-stu-id="e3240-104">Use **Allocation instrumentation on timeline** to find objects that are not being properly garbage collected, and continue to retain memory.</span></span>  

## <span data-ttu-id="e3240-105">Cómo funciona el instrumental de asignación en la escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="e3240-105">How Allocation instrumentation on timeline works</span></span>  

<span data-ttu-id="e3240-106">La **instrumentación de asignación** de la escala de tiempo combina la información detallada de instantáneas del generador de perfiles del **montón** con la actualización incremental y el seguimiento del panel **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="e3240-106">**Allocation instrumentation on timeline** combines the detailed snapshot information of the **heap profiler** with the incremental updating and tracking of the **Performance** panel.</span></span>  <span data-ttu-id="e3240-107">Del mismo modo, el seguimiento de la asignación de montones para objetos implica el inicio de una grabación, la realización de una secuencia de acciones y la detención de la grabación para su análisis.</span><span class="sxs-lookup"><span data-stu-id="e3240-107">Similarly, tracking heap allocation for objects involves starting a recording, performing a sequence of actions, and stopping the recording for analysis.</span></span>  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

<span data-ttu-id="e3240-108">La **instrumentación de asignación de la escala de tiempo** toma instantáneas de montones de forma periódica en la grabación \ (con la frecuencia que cada 50 ms! \) y una instantánea final al final de la grabación.</span><span class="sxs-lookup"><span data-stu-id="e3240-108">**Allocation instrumentation on timeline** takes heap snapshots periodically throughout the recording \(as frequently as every 50 ms!\) and one final snapshot at the end of the recording.</span></span>  

> ##### <span data-ttu-id="e3240-109">Figura 1</span><span class="sxs-lookup"><span data-stu-id="e3240-109">Figure 1</span></span>  
> **<span data-ttu-id="e3240-110">Instrumentación de asignación en la escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="e3240-110">Allocation instrumentation on timeline</span></span>**  
> ![Instrumentación de asignación en la escala de tiempo][ImageObjectTracker]  

> [!NOTE]
> <span data-ttu-id="e3240-112">El número después del `@` es un identificador de objeto que se conserva en varias instantáneas tomadas durante la sesión de grabación.</span><span class="sxs-lookup"><span data-stu-id="e3240-112">The number after the `@` is an object ID that persists across the multiple snapshots taken during the recording session.</span></span>  <span data-ttu-id="e3240-113">El identificador de objeto persistente permite una comparación precisa entre los Estados de la pila.</span><span class="sxs-lookup"><span data-stu-id="e3240-113">The persistent object ID enables precise comparison between heap states.</span></span>  <span data-ttu-id="e3240-114">Los objetos se mueven durante la recolección de elementos no utilizados, por lo que no tiene sentido Mostrar la dirección de un objeto.</span><span class="sxs-lookup"><span data-stu-id="e3240-114">Objects are moved during garbage collections, so displaying the address of an object makes no sense.</span></span>  

## <span data-ttu-id="e3240-115">Habilitar instrumentación de asignación en la escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="e3240-115">Enable Allocation Instrumentation on Timeline</span></span>  

<span data-ttu-id="e3240-116">Siga estos pasos para empezar a usar el **instrumental de asignación en la escala de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="e3240-116">Follow these steps to begin using **Allocation instrumentation on timeline**.</span></span>  

1.  <span data-ttu-id="e3240-117">[Abra el DevTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="e3240-117">[Open the DevTools][DevtoolsOpenIndex].</span></span>  
1.  <span data-ttu-id="e3240-118">Abra el panel **memoria** y seleccione el botón **de opción instrumentación de asignación en la escala de tiempo** .</span><span class="sxs-lookup"><span data-stu-id="e3240-118">Open the **Memory** panel, select the **Allocation instrumentation on timeline** radio button.</span></span>  
1.  <span data-ttu-id="e3240-119">Iniciar grabación.</span><span class="sxs-lookup"><span data-stu-id="e3240-119">Start recording.</span></span>  

> ##### <span data-ttu-id="e3240-120">Figura 2</span><span class="sxs-lookup"><span data-stu-id="e3240-120">Figure 2</span></span>  
> <span data-ttu-id="e3240-121">Generador de perfiles de asignaciones del montón de grabación</span><span class="sxs-lookup"><span data-stu-id="e3240-121">Record heap allocations profiler</span></span>  
> ![Generador de perfiles de asignaciones del montón de grabación][ImageRecordHeap]  

## <span data-ttu-id="e3240-123">Leer una escala de tiempo de asignación del montón</span><span class="sxs-lookup"><span data-stu-id="e3240-123">Read a heap allocation timeline</span></span>  

<span data-ttu-id="e3240-124">La escala de tiempo de asignación del montón muestra dónde se crean los objetos e identifica la ruta de acceso de retención.</span><span class="sxs-lookup"><span data-stu-id="e3240-124">The heap allocation timeline shows where objects are being created and identifies the retaining path.</span></span>  <span data-ttu-id="e3240-125">En la [figura 3](#figure-3), las barras de la parte superior indican cuándo se encuentran nuevos objetos en el montón.</span><span class="sxs-lookup"><span data-stu-id="e3240-125">In [Figure 3](#figure-3), the bars at the top indicate when new objects are found in the heap.</span></span>  

<span data-ttu-id="e3240-126">El alto de cada barra corresponde al tamaño de los objetos asignados recientemente, y el color de las barras indica si esos objetos siguen estando activos en la instantánea de la pila final.</span><span class="sxs-lookup"><span data-stu-id="e3240-126">The height of each bar corresponds to the size of the recently allocated objects, and the color of the bars indicate whether or not those objects are still live in the final heap snapshot.</span></span>  <span data-ttu-id="e3240-127">Las barras azules indican que los objetos que aún están activos al final de la escala de tiempo, las barras grises indican los objetos que se asignaron durante la escala de tiempo, pero que se han recolectado como basura.</span><span class="sxs-lookup"><span data-stu-id="e3240-127">Blue bars indicate objects that are still live at the end of the timeline, Gray bars indicate objects that were allocated during the timeline, but have since been garbage collected.</span></span>  

> ##### <span data-ttu-id="e3240-128">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="e3240-128">Figure 3</span></span>  
> <span data-ttu-id="e3240-129">**Instrumentación de asignación en instantánea de escala de tiempo**</span><span class="sxs-lookup"><span data-stu-id="e3240-129">**Allocation instrumentation on timeline** snapshot</span></span>  
> ![Instrumentación de asignación en instantánea de escala de tiempo][ImageCollected]  

<!--In [Figure 4](#figure-4), an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple click actions  -->  

<span data-ttu-id="e3240-131">Puede usar los controles deslizantes de la línea de tiempo anterior para acercar ese Snapshot en particular y ver los objetos que se asignaron recientemente en ese punto:</span><span class="sxs-lookup"><span data-stu-id="e3240-131">You are able to use the sliders in the timeline above to zoom into that particular snapshot and see the objects that were recently allocated at that point:</span></span>  

> ##### <span data-ttu-id="e3240-132">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="e3240-132">Figure 4</span></span>  
> <span data-ttu-id="e3240-133">Acercar instantánea</span><span class="sxs-lookup"><span data-stu-id="e3240-133">Zoom into snapshot</span></span>  
> ![Acercar instantánea][ImageSliders]  

<span data-ttu-id="e3240-135">Al hacer clic en un objeto específico en el montón, se muestra el árbol de retención en la parte inferior de la instantánea del montón.</span><span class="sxs-lookup"><span data-stu-id="e3240-135">Clicking on a specific object in the heap shows the retaining tree in the bottom portion of the heap snapshot.</span></span>  <span data-ttu-id="e3240-136">El examen de la retención de la ruta de acceso al objeto debe proporcionarle suficiente información para comprender por qué no se recopiló el objeto y debe realizar los cambios de código necesarios para quitar la referencia innecesaria.</span><span class="sxs-lookup"><span data-stu-id="e3240-136">Examining the retaining path to the object should give you enough information to understand why the object was not collected, and you should make the necessary code changes to remove the unnecessary reference.</span></span>  

## <span data-ttu-id="e3240-137">Ver asignación de memoria por función</span><span class="sxs-lookup"><span data-stu-id="e3240-137">View memory allocation by function</span></span>   

<span data-ttu-id="e3240-138">Puede ver la asignación de memoria por función de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e3240-138">You are able to view memory allocation by JavaScript function.</span></span>  <span data-ttu-id="e3240-139">Para obtener más información [, consulte investigar la asignación de memoria por función][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction] .</span><span class="sxs-lookup"><span data-stu-id="e3240-139">See [Investigate memory allocation by function][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction] for more information.</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageObjectTracker]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png "Ilustración 1: instrumentación de asignación en la escala de tiempo"  
[ImageRecordHeap]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png "Ilustración 2: generador de perfiles de asignaciones del montón de grabación"  
[ImageCollected]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-timelines-snapshot.msft.png "Ilustración 3: instrumentación de asignación en la instantánea de la escala de tiempo"  
[ImageSliders]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png "Ilustración 4: acercar la instantánea"  

<!-- links -->  

[DevToolsOpenIndex]: /microsoft-edge/devtools-guide-chromium/open "Abrir DevTools de Microsoft Edge (cromo)"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: /microsoft-edge/devtools-guide-chromium/memory-problems/index#investigate-memory-allocation-by-function "Investigar la asignación de memoria por función: corrección de problemas de memoria"  

<!--[HeapProfiler]: ../profile/memory-problems/heap-snapshots ""  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Descargar un canal de Microsoft Edge"  

> [!NOTE]
> <span data-ttu-id="e3240-147">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e3240-147">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e3240-148">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) y está creada por [Meggin Kearney][MegginKearney] \ (editor técnico \).</span><span class="sxs-lookup"><span data-stu-id="e3240-148">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e3240-150">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e3240-150">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

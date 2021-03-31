---
description: Use instrumentación de asignación en la escala de tiempo para buscar objetos que no se están recopilando correctamente y seguir conservando la memoria.
title: Cómo usar instrumentación de asignación en escala de tiempo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 374b7f0ad80b8975319b2b0ec5cecf42ce4bde82
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397821"
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

# <a name="how-to-use-allocation-instrumentation-on-timeline"></a><span data-ttu-id="4568e-104">Cómo usar instrumentación de asignación en escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="4568e-104">How to use Allocation instrumentation on Timeline</span></span>  

<span data-ttu-id="4568e-105">Use **instrumentación de asignación en** la escala de tiempo para buscar objetos que no se están recopilando correctamente y seguir conservando la memoria.</span><span class="sxs-lookup"><span data-stu-id="4568e-105">Use **Allocation instrumentation on timeline** to find objects that are not being properly garbage collected, and continue to retain memory.</span></span>  

## <a name="how-allocation-instrumentation-on-timeline-works"></a><span data-ttu-id="4568e-106">Cómo funciona la instrumentación de asignación en la escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="4568e-106">How Allocation instrumentation on timeline works</span></span>  

<span data-ttu-id="4568e-107">**La instrumentación de** asignación en la  escala de tiempo combina la información detallada de instantáneas del perfilador de montón con la actualización incremental y el seguimiento del panel **Rendimiento.**</span><span class="sxs-lookup"><span data-stu-id="4568e-107">**Allocation instrumentation on timeline** combines the detailed snapshot information of the **heap profiler** with the incremental updating and tracking of the **Performance** panel.</span></span>  <span data-ttu-id="4568e-108">Del mismo modo, el seguimiento de la asignación de montón de objetos implica iniciar una grabación, realizar una secuencia de acciones y detener la grabación para su análisis.</span><span class="sxs-lookup"><span data-stu-id="4568e-108">Similarly, tracking heap allocation for objects involves starting a recording, performing a sequence of actions, and stopping the recording for analysis.</span></span>  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

<span data-ttu-id="4568e-109">**La instrumentación** de asignación en la escala de tiempo toma instantáneas de montón periódicamente a lo largo de la grabación \(con la frecuencia que cada 50 ms\) y una instantánea final al final de la grabación.</span><span class="sxs-lookup"><span data-stu-id="4568e-109">**Allocation instrumentation on timeline** takes heap snapshots periodically throughout the recording \(as frequently as every 50 ms\) and one final snapshot at the end of the recording.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Instrumentación de asignación en escala de tiempo" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **<span data-ttu-id="4568e-111">Instrumentación de asignación en escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="4568e-111">Allocation instrumentation on timeline</span></span>**  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="4568e-112">El número después del es un identificador de objeto que persiste en las `@` varias instantáneas tomadas durante la sesión de grabación.</span><span class="sxs-lookup"><span data-stu-id="4568e-112">The number after the `@` is an object ID that persists across the multiple snapshots taken during the recording session.</span></span>  <span data-ttu-id="4568e-113">El identificador de objeto persistente permite una comparación precisa entre los estados de montón.</span><span class="sxs-lookup"><span data-stu-id="4568e-113">The persistent object ID enables precise comparison between heap states.</span></span>  <span data-ttu-id="4568e-114">Los objetos se mueven durante las colecciones de elementos no utilizados, por lo que mostrar la dirección de un objeto no tiene sentido.</span><span class="sxs-lookup"><span data-stu-id="4568e-114">Objects are moved during garbage collections, so displaying the address of an object makes no sense.</span></span>  

## <a name="enable-allocation-instrumentation-on-timeline"></a><span data-ttu-id="4568e-115">Habilitar instrumentación de asignación en escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="4568e-115">Enable Allocation Instrumentation on Timeline</span></span>  

<span data-ttu-id="4568e-116">Complete las siguientes acciones para empezar a usar **instrumentación de asignación en la escala de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="4568e-116">Complete the following actions to begin using **Allocation instrumentation on timeline**.</span></span>  

1.  <span data-ttu-id="4568e-117">[Abra DevTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="4568e-117">[Open the DevTools][DevtoolsOpenIndex].</span></span>  
1.  <span data-ttu-id="4568e-118">Abra el panel **Memoria,** seleccione el botón de radio **Instrumentación de asignación en la** escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4568e-118">Open the **Memory** panel, select the **Allocation instrumentation on timeline** radio button.</span></span>  
1.  <span data-ttu-id="4568e-119">Iniciar grabación.</span><span class="sxs-lookup"><span data-stu-id="4568e-119">Start recording.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Registrador de asignaciones de montón" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       <span data-ttu-id="4568e-121">Registrador de asignaciones de montón</span><span class="sxs-lookup"><span data-stu-id="4568e-121">Record heap allocations profiler</span></span>  
    :::image-end:::  
    
## <a name="read-a-heap-allocation-timeline"></a><span data-ttu-id="4568e-122">Leer una escala de tiempo de asignación de montón</span><span class="sxs-lookup"><span data-stu-id="4568e-122">Read a heap allocation timeline</span></span>  

<span data-ttu-id="4568e-123">La escala de tiempo de asignación de montón muestra dónde se crean los objetos e identifica la ruta de retención.</span><span class="sxs-lookup"><span data-stu-id="4568e-123">The heap allocation timeline shows where objects are being created and identifies the retaining path.</span></span>  <span data-ttu-id="4568e-124">En la siguiente figura, las barras de la parte superior indican cuándo se encuentran objetos nuevos en el montón.</span><span class="sxs-lookup"><span data-stu-id="4568e-124">In the following figure, the bars at the top indicate when new objects are found in the heap.</span></span>  

<span data-ttu-id="4568e-125">El alto de cada barra corresponde al tamaño de los objetos asignados recientemente y el color de las barras indica si esos objetos aún están en la instantánea de montón final.</span><span class="sxs-lookup"><span data-stu-id="4568e-125">The height of each bar corresponds to the size of the recently allocated objects, and the color of the bars indicate whether or not those objects are still live in the final heap snapshot.</span></span>  <span data-ttu-id="4568e-126">Las barras azules indican objetos que aún están en vida al final de la escala de tiempo, las barras grises indican objetos que se asignaron durante la escala de tiempo, pero que desde entonces se han recopilado como elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="4568e-126">Blue bars indicate objects that are still live at the end of the timeline, Gray bars indicate objects that were allocated during the timeline, but have since been garbage collected.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Instrumentación de asignación en instantánea de escala de tiempo" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   <span data-ttu-id="4568e-128">**Instrumentación de asignación en instantánea de escala de** tiempo</span><span class="sxs-lookup"><span data-stu-id="4568e-128">**Allocation instrumentation on timeline** snapshot</span></span>  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple choose actions  -->  

<span data-ttu-id="4568e-129">Puedes usar los controles deslizantes de la escala de tiempo anterior para acercar esa instantánea en particular y revisar los objetos que se asignaron recientemente en ese momento:</span><span class="sxs-lookup"><span data-stu-id="4568e-129">You are able to use the sliders in the timeline above to zoom into that particular snapshot and review the objects that were recently allocated at that point:</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Acercar instantáneas" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   <span data-ttu-id="4568e-131">Acercar instantáneas</span><span class="sxs-lookup"><span data-stu-id="4568e-131">Zoom into snapshot</span></span>  
:::image-end:::  

<span data-ttu-id="4568e-132">Al elegir en un objeto específico del montón se muestra el árbol de retención en la parte inferior de la instantánea de montón.</span><span class="sxs-lookup"><span data-stu-id="4568e-132">Choosing on a specific object in the heap shows the retaining tree in the bottom portion of the heap snapshot.</span></span>  <span data-ttu-id="4568e-133">Examinar la ruta de retención del objeto debe proporcionar suficiente información para comprender por qué no se recopiló el objeto y debe realizar los cambios de código necesarios para quitar la referencia innecesaria.</span><span class="sxs-lookup"><span data-stu-id="4568e-133">Examining the retaining path to the object should give you enough information to understand why the object was not collected, and you should make the necessary code changes to remove the unnecessary reference.</span></span>  

## <a name="view-memory-allocation-by-function"></a><span data-ttu-id="4568e-134">Ver asignación de memoria por función</span><span class="sxs-lookup"><span data-stu-id="4568e-134">View memory allocation by function</span></span>  

<span data-ttu-id="4568e-135">Puede ver la asignación de memoria mediante la función JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4568e-135">You are able to view memory allocation by JavaScript function.</span></span>  <span data-ttu-id="4568e-136">Para obtener más información, vaya [a Investigar asignación de memoria por función][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].</span><span class="sxs-lookup"><span data-stu-id="4568e-136">For more information, navigate to [Investigate memory allocation by function][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="4568e-137">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4568e-137">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open/index.md "Abra Microsoft Edge (Chromium) DevTools | Microsoft Docs"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Investigar asignación de memoria por función: solucionar problemas de memoria | Microsoft Docs"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Descargar un canal de Microsoft Edge"  

> [!NOTE]
> <span data-ttu-id="4568e-141">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4568e-141">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4568e-142">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) y es creado por [Meggin Kearney][MegginKearney] \(Technical Writer\).</span><span class="sxs-lookup"><span data-stu-id="4568e-142">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4568e-144">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4568e-144">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

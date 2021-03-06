---
description: Obtenga información sobre cómo grabar instantáneas de montón con el perfilador de montón DevTools de Microsoft Edge y buscar pérdidas de memoria.
title: Cómo grabar instantáneas de montón
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: ce7a6f972bed386f96312808428bd74f1241668f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397807"
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
   limitations under the License.  -->

# <a name="how-to-record-heap-snapshots"></a><span data-ttu-id="2bec5-104">Cómo grabar instantáneas de montón</span><span class="sxs-lookup"><span data-stu-id="2bec5-104">How to record heap snapshots</span></span>  

<span data-ttu-id="2bec5-105">Obtenga información sobre cómo grabar instantáneas de montón con el perfilador de montón DevTools de Microsoft Edge y buscar pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="2bec5-105">Learn how to record heap snapshots with the Microsoft Edge DevTools heap profiler and find memory leaks.</span></span>  

<span data-ttu-id="2bec5-106">El profiler de montón DevTools de Microsoft Edge muestra la distribución de memoria por los objetos JavaScript y los nodos DOM relacionados de la página.</span><span class="sxs-lookup"><span data-stu-id="2bec5-106">The Microsoft Edge DevTools heap profiler shows memory distribution by the JavaScript objects and related DOM nodes of your page.</span></span>  <span data-ttu-id="2bec5-107">Úselo para tomar instantáneas de montón de JavaScript \(JS heap\), analizar gráficos de memoria, comparar instantáneas y encontrar pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="2bec5-107">Use it to take JavaScript heap \(JS heap\) snapshots, analyze memory graphs, compare snapshots, and find memory leaks.</span></span>  <span data-ttu-id="2bec5-108">Vaya a [Árbol de retención de objetos][DevtoolsMemoryProblems101ObjectsRetainingTree].</span><span class="sxs-lookup"><span data-stu-id="2bec5-108">Navigate to [Objects retaining tree][DevtoolsMemoryProblems101ObjectsRetainingTree].</span></span>  

## <a name="take-a-snapshot"></a><span data-ttu-id="2bec5-109">Tomar una instantánea</span><span class="sxs-lookup"><span data-stu-id="2bec5-109">Take a snapshot</span></span>  

<span data-ttu-id="2bec5-110">En el panel **Memoria,** elija **Tomar instantánea**y, a continuación, **elija Inicio**.</span><span class="sxs-lookup"><span data-stu-id="2bec5-110">On the **Memory** panel, choose **Take snapshot**, then choose **Start**.</span></span>  <span data-ttu-id="2bec5-111">También puede seleccionar `Ctrl` + `E` \(Windows, Linux\) o `Cmd` + `E` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="2bec5-111">You may also select `Ctrl`+`E` \(Windows, Linux\) or `Cmd`+`E` \(macOS\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Elegir tipo de generación de perfiles" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   <span data-ttu-id="2bec5-113">Elegir tipo de generación de perfiles</span><span class="sxs-lookup"><span data-stu-id="2bec5-113">Choose profiling type</span></span>  
:::image-end:::  

<span data-ttu-id="2bec5-114">**Las instantáneas** se almacenan inicialmente en la memoria del proceso del representador.</span><span class="sxs-lookup"><span data-stu-id="2bec5-114">**Snapshots** are initially stored in the renderer process memory.</span></span>  <span data-ttu-id="2bec5-115">Las instantáneas se transfieren a DevTools a petición, cuando se elige en el icono de instantánea para verlo.</span><span class="sxs-lookup"><span data-stu-id="2bec5-115">Snapshots are transferred to the DevTools on demand, when you choose on the snapshot icon to view it.</span></span>  

<span data-ttu-id="2bec5-116">Después de cargar la instantánea en DevTools y analizarla, aparece el número debajo del título de la instantánea y muestra el tamaño total de los objetos [de JavaScript accesibles.][DevtoolsMemoryProblems101ObjectSizes]</span><span class="sxs-lookup"><span data-stu-id="2bec5-116">After the snapshot has been loaded into DevTools and has been parsed, the number below the snapshot title appears and shows the [total size of the reachable JavaScript objects][DevtoolsMemoryProblems101ObjectSizes].</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Tamaño total de los objetos accesibles" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   <span data-ttu-id="2bec5-118">Tamaño total de los objetos accesibles</span><span class="sxs-lookup"><span data-stu-id="2bec5-118">Total size of reachable objects</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="2bec5-119">Solo los objetos accesibles se incluyen en las instantáneas.</span><span class="sxs-lookup"><span data-stu-id="2bec5-119">Only reachable objects are included in snapshots.</span></span>  <span data-ttu-id="2bec5-120">Además, tomar una instantánea siempre comienza con una recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="2bec5-120">Also, taking a snapshot always starts with a garbage collection.</span></span>  

## <a name="clear-snapshots"></a><span data-ttu-id="2bec5-121">Borrar instantáneas</span><span class="sxs-lookup"><span data-stu-id="2bec5-121">Clear snapshots</span></span>  

<span data-ttu-id="2bec5-122">Elija **Borrar todos los perfiles** icono para quitar instantáneas \(tanto de DevTools como de cualquier memoria asociada con el proceso del representador\).</span><span class="sxs-lookup"><span data-stu-id="2bec5-122">Choose **Clear all profiles** icon to remove snapshots \(both from DevTools and any memory associated with the renderer process\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Quitar instantáneas" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   <span data-ttu-id="2bec5-124">Quitar instantáneas</span><span class="sxs-lookup"><span data-stu-id="2bec5-124">Remove snapshots</span></span>  
:::image-end:::  

<span data-ttu-id="2bec5-125">Cerrar la ventana DevTools no elimina los perfiles de la memoria asociada con el proceso del representador.</span><span class="sxs-lookup"><span data-stu-id="2bec5-125">Closing the DevTools window does not delete profiles from the memory associated with the renderer process.</span></span>  <span data-ttu-id="2bec5-126">Al volver a abrir DevTools, todas las instantáneas tomadas anteriormente vuelven a aparecer en la lista de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="2bec5-126">When reopening DevTools, all previously taken snapshots reappear in the list of snapshots.</span></span>  

> [!NOTE]
> <span data-ttu-id="2bec5-127">Pruebe este ejemplo de [objetos dispersos][GlitchDevtoolsMemoryExample03] y de perfiles con el Profiler de montón.</span><span class="sxs-lookup"><span data-stu-id="2bec5-127">Try out this example of [scattered objects][GlitchDevtoolsMemoryExample03] and profile it using the Heap Profiler.</span></span>  <span data-ttu-id="2bec5-128">Se muestra un número de asignaciones de elementos \(object\).</span><span class="sxs-lookup"><span data-stu-id="2bec5-128">A number of \(object\) item allocations are displayed.</span></span>  

## <a name="view-snapshots"></a><span data-ttu-id="2bec5-129">Ver instantáneas</span><span class="sxs-lookup"><span data-stu-id="2bec5-129">View snapshots</span></span>  

<span data-ttu-id="2bec5-130">Ver instantáneas desde diferentes perspectivas para distintas tareas.</span><span class="sxs-lookup"><span data-stu-id="2bec5-130">View snapshots from different perspectives for different tasks.</span></span>  

<span data-ttu-id="2bec5-131">**La vista resumen** muestra objetos agrupados por el nombre del constructor.</span><span class="sxs-lookup"><span data-stu-id="2bec5-131">**Summary view** shows objects grouped by the constructor name.</span></span>  <span data-ttu-id="2bec5-132">Úselo para buscar objetos \(y el uso de memoria\) en función del tipo agrupado por el nombre del constructor.</span><span class="sxs-lookup"><span data-stu-id="2bec5-132">Use it to hunt down objects \(and the memory use\) based on type grouped by constructor name.</span></span>  <span data-ttu-id="2bec5-133">Es especialmente útil para realizar un **seguimiento de las pérdidas de DOM.**</span><span class="sxs-lookup"><span data-stu-id="2bec5-133">It is particularly helpful for **tracking down DOM leaks**.</span></span>

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

<span data-ttu-id="2bec5-134">**Vista de comparación**.</span><span class="sxs-lookup"><span data-stu-id="2bec5-134">**Comparison view**.</span></span>  <span data-ttu-id="2bec5-135">Muestra la diferencia entre dos instantáneas.</span><span class="sxs-lookup"><span data-stu-id="2bec5-135">Displays the difference between two snapshots.</span></span>  <span data-ttu-id="2bec5-136">Úselo para comparar dos instantáneas de memoria \(o más\) de antes y después de una operación.</span><span class="sxs-lookup"><span data-stu-id="2bec5-136">Use it to compare two \(or more\) memory snapshots from before and after an operation.</span></span>  <span data-ttu-id="2bec5-137">Inspeccionar el delta en la memoria liberada y el recuento de referencias le permite confirmar la presencia y la causa de una pérdida de memoria.</span><span class="sxs-lookup"><span data-stu-id="2bec5-137">Inspecting the delta in freed memory and reference count lets you confirm the presence and cause of a memory leak.</span></span>  

<span data-ttu-id="2bec5-138">**Vista de contención**.</span><span class="sxs-lookup"><span data-stu-id="2bec5-138">**Containment view**.</span></span>  <span data-ttu-id="2bec5-139">Permite explorar el contenido del montón.</span><span class="sxs-lookup"><span data-stu-id="2bec5-139">Allows exploration of heap contents.</span></span>  <span data-ttu-id="2bec5-140">**La vista de** contención proporciona una mejor vista de la estructura de objetos, lo que ayuda a analizar los objetos a los que se hace referencia en el espacio de nombres global \(window\) para averiguar qué está manteniendo los objetos alrededor.</span><span class="sxs-lookup"><span data-stu-id="2bec5-140">**Containment view** provides a better view of object structure, helping analyze objects referenced in the global namespace \(window\) to find out what is keeping objects around.</span></span>  <span data-ttu-id="2bec5-141">Úselo para analizar los cierres y profundizar en los objetos en un nivel bajo.</span><span class="sxs-lookup"><span data-stu-id="2bec5-141">Use it to analyze closures and dive into your objects at a low level.</span></span>  

<span data-ttu-id="2bec5-142">Para cambiar entre vistas, use el selector en la parte superior de la vista.</span><span class="sxs-lookup"><span data-stu-id="2bec5-142">To switch between views, use the selector at the top of the view.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Selector de vistas de conmutador" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   <span data-ttu-id="2bec5-144">Selector de vistas de conmutador</span><span class="sxs-lookup"><span data-stu-id="2bec5-144">Switch views selector</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="2bec5-145">No todas las propiedades se almacenan en el montón de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2bec5-145">Not all properties are stored on the JavaScript heap.</span></span>  <span data-ttu-id="2bec5-146">Las propiedades implementadas mediante getters que ejecutan código nativo no se capturan.</span><span class="sxs-lookup"><span data-stu-id="2bec5-146">Properties implemented using getters that run native code are not captured.</span></span>  <span data-ttu-id="2bec5-147">Además, no se capturan valores que no sean de cadena, como números.</span><span class="sxs-lookup"><span data-stu-id="2bec5-147">Also, non-string values such as numbers are not captured.</span></span>  

### <a name="summary-view"></a><span data-ttu-id="2bec5-148">Vista de resumen</span><span class="sxs-lookup"><span data-stu-id="2bec5-148">Summary view</span></span>  

<span data-ttu-id="2bec5-149">Inicialmente, se abre una instantánea en la vista Resumen, que muestra totales de objeto, que se pueden expandir para mostrar instancias:</span><span class="sxs-lookup"><span data-stu-id="2bec5-149">Initially, a snapshot opens in the Summary view, displaying object totals, which may be expanded to show instances:</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Vista de resumen" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   <span data-ttu-id="2bec5-151">**Vista de resumen**</span><span class="sxs-lookup"><span data-stu-id="2bec5-151">**Summary** view</span></span>  
:::image-end:::  

<span data-ttu-id="2bec5-152">Las entradas de nivel superior son líneas "totales".</span><span class="sxs-lookup"><span data-stu-id="2bec5-152">Top-level entries are "total" lines.</span></span>  

| <span data-ttu-id="2bec5-153">Entradas de nivel superior</span><span class="sxs-lookup"><span data-stu-id="2bec5-153">Top-level entries</span></span> | <span data-ttu-id="2bec5-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bec5-154">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="2bec5-155">Constructor</span><span class="sxs-lookup"><span data-stu-id="2bec5-155">Constructor</span></span>** | <span data-ttu-id="2bec5-156">Representa todos los objetos creados con este constructor.</span><span class="sxs-lookup"><span data-stu-id="2bec5-156">Represents all objects created using this constructor.</span></span>  |  
| **<span data-ttu-id="2bec5-157">Distancia</span><span class="sxs-lookup"><span data-stu-id="2bec5-157">Distance</span></span>** | <span data-ttu-id="2bec5-158">muestra la distancia a la raíz mediante la ruta de acceso sencilla más corta de los nodos.</span><span class="sxs-lookup"><span data-stu-id="2bec5-158">displays the distance to the root using the shortest simple path of nodes.</span></span>  |  
| **<span data-ttu-id="2bec5-159">Tamaño superficial</span><span class="sxs-lookup"><span data-stu-id="2bec5-159">Shallow size</span></span>** | <span data-ttu-id="2bec5-160">Muestra la suma de tamaños superficiales de todos los objetos creados por una función de constructor determinada.</span><span class="sxs-lookup"><span data-stu-id="2bec5-160">Displays the sum of shallow sizes of all objects created by a certain constructor function.</span></span>  <span data-ttu-id="2bec5-161">El tamaño superficial es el tamaño de la memoria que contiene un objeto \(por lo general, las matrices y las cadenas tienen tamaños superficiales más grandes\).</span><span class="sxs-lookup"><span data-stu-id="2bec5-161">The shallow size is the size of memory held by an object \(generally, arrays and strings have larger shallow sizes\).</span></span>  <span data-ttu-id="2bec5-162">Vaya a [Tamaños de objeto][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="2bec5-162">Navigate to [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  
| **<span data-ttu-id="2bec5-163">Tamaño retenido</span><span class="sxs-lookup"><span data-stu-id="2bec5-163">Retained size</span></span>** | <span data-ttu-id="2bec5-164">Muestra el tamaño máximo retenido entre el mismo conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="2bec5-164">Displays the maximum retained size among the same set of objects.</span></span>  <span data-ttu-id="2bec5-165">El tamaño de memoria que puede liberar después de eliminar un objeto \(y los dependientes ya no son accesibles\) se denomina tamaño retenido.</span><span class="sxs-lookup"><span data-stu-id="2bec5-165">The size of memory that you are able to free after an object is deleted \(and the dependents are made no longer reachable\) is called the retained size.</span></span>  <span data-ttu-id="2bec5-166">Vaya a [Tamaños de objeto][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="2bec5-166">Navigate to [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

<span data-ttu-id="2bec5-167">Después de expandir una línea total en la vista superior, se muestran todas las instancias.</span><span class="sxs-lookup"><span data-stu-id="2bec5-167">After expanding a total line in the upper view, all of the instances are displayed.</span></span>  <span data-ttu-id="2bec5-168">Para cada instancia, los tamaños superficiales y retenido se muestran en las columnas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="2bec5-168">For each instance, the shallow and retained sizes are displayed in the corresponding columns.</span></span>  <span data-ttu-id="2bec5-169">El número después del carácter es el identificador único del objeto, lo que permite comparar instantáneas de montón `@` por objeto.</span><span class="sxs-lookup"><span data-stu-id="2bec5-169">The number after the `@` character is the unique ID of the object, allowing you to compare heap snapshots on per-object basis.</span></span>  

<span data-ttu-id="2bec5-170">Recuerde que los objetos amarillos tienen referencias de JavaScript y los objetos rojos son nodos separados a los que se hace referencia desde uno con un fondo amarillo.</span><span class="sxs-lookup"><span data-stu-id="2bec5-170">Remember that yellow objects have JavaScript references and red objects are detached nodes which are referenced from one with a yellow background.</span></span>  

**<span data-ttu-id="2bec5-171">¿A qué corresponden las distintas entradas del constructor \(group\) en el perfilador de montón?</span><span class="sxs-lookup"><span data-stu-id="2bec5-171">What do the various constructor \(group\) entries in the Heap profiler correspond to?</span></span>**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Grupos de constructores" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   <span data-ttu-id="2bec5-173">**Grupos de constructores**</span><span class="sxs-lookup"><span data-stu-id="2bec5-173">**Constructor** groups</span></span>  
:::image-end:::  

| <span data-ttu-id="2bec5-174">Entrada constructor \(group\)</span><span class="sxs-lookup"><span data-stu-id="2bec5-174">Constructor \(group\) entry</span></span> | <span data-ttu-id="2bec5-175">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bec5-175">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="2bec5-176">\(global property\)</span><span class="sxs-lookup"><span data-stu-id="2bec5-176">\(global property\)</span></span>** | <span data-ttu-id="2bec5-177">Los objetos intermedios entre un objeto global \(like \) y un objeto al que `window` hace referencia.</span><span class="sxs-lookup"><span data-stu-id="2bec5-177">The intermediate objects between a global object \(like `window`\) and an object referenced by it.</span></span>  <span data-ttu-id="2bec5-178">Si un objeto se crea con un constructor y lo mantiene un objeto global, la ruta de retención `Person` puede representarse como `[global] > \(global property\) > Person` .</span><span class="sxs-lookup"><span data-stu-id="2bec5-178">If an object is created using a constructor `Person` and is held by a global object, the retaining path may be represented as `[global] > \(global property\) > Person`.</span></span>  <span data-ttu-id="2bec5-179">Esto contrasta con la norma, donde los objetos se hacen referencia directamente entre sí.</span><span class="sxs-lookup"><span data-stu-id="2bec5-179">This contrasts with the norm, where objects directly reference each other.</span></span>  <span data-ttu-id="2bec5-180">Existen objetos intermedios por motivos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="2bec5-180">Intermediate objects exist for performance reasons.</span></span>  <span data-ttu-id="2bec5-181">Los globales se modifican regularmente y las optimizaciones de acceso a propiedades hacen un buen trabajo para los objetos no globales no son aplicables a los globales.</span><span class="sxs-lookup"><span data-stu-id="2bec5-181">Globals are modified regularly and property access optimizations do a good job for non-global objects are not applicable for globals.</span></span>  |  
| **<span data-ttu-id="2bec5-182">\(roots\)</span><span class="sxs-lookup"><span data-stu-id="2bec5-182">\(roots\)</span></span>** | <span data-ttu-id="2bec5-183">Las entradas raíz de la vista de árbol de retención son las entidades que tienen referencias al objeto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="2bec5-183">The root entries in the retaining tree view are the entities that have references to the selected object.</span></span>  <span data-ttu-id="2bec5-184">Las entradas también pueden ser referencias creadas por el motor para fines específicos del motor.</span><span class="sxs-lookup"><span data-stu-id="2bec5-184">The entries may also be references created by the engine for engine-specific purposes.</span></span>  <span data-ttu-id="2bec5-185">El motor tiene cachés que hacen referencia a objetos, pero todas estas referencias son débiles y no impiden que se repile un objeto dado que no hay referencias realmente seguras.</span><span class="sxs-lookup"><span data-stu-id="2bec5-185">The engine has caches which reference objects, but all such references are weak and do not prevent an object from being collected given that there are no truly strong references.</span></span>  |  
| **<span data-ttu-id="2bec5-186">\(closure\)</span><span class="sxs-lookup"><span data-stu-id="2bec5-186">\(closure\)</span></span>** | <span data-ttu-id="2bec5-187">Recuento de referencias a un grupo de objetos mediante cierres de función.</span><span class="sxs-lookup"><span data-stu-id="2bec5-187">A count of references to a group of objects through function closures.</span></span>  |  
| **<span data-ttu-id="2bec5-188">\(array, string, number, regexp\)</span><span class="sxs-lookup"><span data-stu-id="2bec5-188">\(array, string, number, regexp\)</span></span>** | <span data-ttu-id="2bec5-189">Una lista de tipos de objeto con propiedades que hacen referencia a una matriz, cadena, número o expresión regular.</span><span class="sxs-lookup"><span data-stu-id="2bec5-189">A list of object types with properties which reference an Array, String, Number, or regular expression.</span></span>  |  
| **<span data-ttu-id="2bec5-190">\(código compilado\)</span><span class="sxs-lookup"><span data-stu-id="2bec5-190">\(compiled code\)</span></span>** | <span data-ttu-id="2bec5-191">Todo lo relacionado con el código compilado.</span><span class="sxs-lookup"><span data-stu-id="2bec5-191">Everything related to compiled code.</span></span>  <span data-ttu-id="2bec5-192">El script es similar a una función, pero corresponde a un `<script>` cuerpo.</span><span class="sxs-lookup"><span data-stu-id="2bec5-192">Script is similar to a function, but corresponds to a `<script>` body.</span></span>  <span data-ttu-id="2bec5-193">SharedFunctionInfos \(SFI\) son objetos que se encuentran entre funciones y código compilado.</span><span class="sxs-lookup"><span data-stu-id="2bec5-193">SharedFunctionInfos \(SFI\) are objects standing between functions and compiled code.</span></span>  <span data-ttu-id="2bec5-194">Las funciones suelen tener un contexto, mientras que las SFI no.</span><span class="sxs-lookup"><span data-stu-id="2bec5-194">Functions usually have a context, while SFIs do not.</span></span>  |  
| <span data-ttu-id="2bec5-195">**HTMLDivElement**, **HTMLAnchorElement,** **DocumentFragment,** y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="2bec5-195">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, and so on.</span></span>  | <span data-ttu-id="2bec5-196">Referencias a elementos u objetos de documento de un tipo concreto al que hace referencia el código.</span><span class="sxs-lookup"><span data-stu-id="2bec5-196">References to elements or document objects of a particular type referenced by your code.</span></span>  |  

<!--todo: add heap profiling summary section when available -->  

### <a name="comparison-view"></a><span data-ttu-id="2bec5-197">Vista de comparación</span><span class="sxs-lookup"><span data-stu-id="2bec5-197">Comparison view</span></span>  

<span data-ttu-id="2bec5-198">Busque objetos filtrados comparando varias instantáneas entre sí.</span><span class="sxs-lookup"><span data-stu-id="2bec5-198">Find leaked objects by comparing multiple snapshots to each other.</span></span>  <span data-ttu-id="2bec5-199">Para comprobar que una determinada operación de aplicación no crea pérdidas \(por ejemplo, normalmente un par de operaciones directas e inversas, como abrir un documento y, a continuación, cerrarlo, no debe dejar elementos no utilizados\), puede seguir el escenario siguiente:</span><span class="sxs-lookup"><span data-stu-id="2bec5-199">To verify that a certain application operation does not create leaks \(for example, usually a pair of direct and reverse operations, like opening a document, and then closing it, should not leave any garbage\), you may follow the scenario below:</span></span>  

1.  <span data-ttu-id="2bec5-200">Realice una instantánea de montón antes de realizar una operación.</span><span class="sxs-lookup"><span data-stu-id="2bec5-200">Take a heap snapshot before performing an operation.</span></span>  
1.  <span data-ttu-id="2bec5-201">Realice una operación \(interactuar con una página de alguna manera que crea que está causando una pérdida\).</span><span class="sxs-lookup"><span data-stu-id="2bec5-201">Perform an operation \(interact with a page in some way that you believe to be causing a leak\).</span></span>  
1.  <span data-ttu-id="2bec5-202">Realizar una operación inversa \(hacer la interacción opuesta y repetirla unas cuantas veces\).</span><span class="sxs-lookup"><span data-stu-id="2bec5-202">Perform a reverse operation \(do the opposite interaction and repeat it a few times\).</span></span>  
1.  <span data-ttu-id="2bec5-203">Tome una segunda instantánea de montón y cambie la vista de esta a **Comparación**, comparándolo con **la instantánea 1**.</span><span class="sxs-lookup"><span data-stu-id="2bec5-203">Take a second heap snapshot and change the view of this one to **Comparison**, comparing it to **Snapshot 1**.</span></span>  
    
<span data-ttu-id="2bec5-204">En la **vista** Comparación, se muestra la diferencia entre dos instantáneas.</span><span class="sxs-lookup"><span data-stu-id="2bec5-204">In the **Comparison** view, the difference between two snapshots is displayed.</span></span>  <span data-ttu-id="2bec5-205">Al expandir una entrada total, se muestran las instancias de objeto agregadas y eliminadas.</span><span class="sxs-lookup"><span data-stu-id="2bec5-205">When expanding a total entry, added and deleted object instances are shown.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Vista de comparación" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   <span data-ttu-id="2bec5-207">**Vista de** comparación</span><span class="sxs-lookup"><span data-stu-id="2bec5-207">**Comparison** view</span></span>  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### <a name="containment-view"></a><span data-ttu-id="2bec5-208">Vista Contención</span><span class="sxs-lookup"><span data-stu-id="2bec5-208">Containment view</span></span>  

<span data-ttu-id="2bec5-209">La **vista Contención** es esencialmente una "vista visual de aves" de la estructura de objetos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2bec5-209">The **Containment** view is essentially a "bird's eye view" of the objects structure of your application.</span></span>  <span data-ttu-id="2bec5-210">Le permite echar un vistazo dentro de los cierres de funciones, observar objetos internos de máquina virtual \(VM\) que juntos son los objetos de JavaScript y comprender la cantidad de memoria que la aplicación usa en un nivel muy bajo.</span><span class="sxs-lookup"><span data-stu-id="2bec5-210">It allows you to peek inside function closures, to observe virtual machine \(VM\) internal objects that together make up your JavaScript objects, and to understand how much memory your application uses at a very low level.</span></span>  

| <span data-ttu-id="2bec5-211">Puntos de entrada de vista de contención</span><span class="sxs-lookup"><span data-stu-id="2bec5-211">Containment view entry points</span></span> | <span data-ttu-id="2bec5-212">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bec5-212">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="2bec5-213">Objetos DOMWindow</span><span class="sxs-lookup"><span data-stu-id="2bec5-213">DOMWindow objects</span></span>** | <span data-ttu-id="2bec5-214">Objetos globales para código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2bec5-214">Global objects for JavaScript code.</span></span>  |  
| **<span data-ttu-id="2bec5-215">Raíces de GC</span><span class="sxs-lookup"><span data-stu-id="2bec5-215">GC roots</span></span>** | <span data-ttu-id="2bec5-216">Las raíces de GC reales usadas por la recolección de elementos no utilizados de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2bec5-216">The actual GC roots used by the garbage of the VM.</span></span>  <span data-ttu-id="2bec5-217">Las raíces de GC se componen de mapas de objetos integrados, tablas de símbolos, pilas de subprocesos de VM, cachés de compilación, ámbitos de identificador y controladores globales.</span><span class="sxs-lookup"><span data-stu-id="2bec5-217">GC roots are comprised of built-in object maps, symbol tables, VM thread stacks, compilation caches, handle scopes, and global handles.</span></span>  |  
| **<span data-ttu-id="2bec5-218">Objetos nativos</span><span class="sxs-lookup"><span data-stu-id="2bec5-218">Native objects</span></span>** | <span data-ttu-id="2bec5-219">Los objetos del explorador se "insertan" dentro de la máquina virtual de JavaScript \(JavaScript VM\) para permitir la automatización, por ejemplo, nodos DOM, reglas CSS.</span><span class="sxs-lookup"><span data-stu-id="2bec5-219">Browser objects "pushed" inside the JavaScript virtual machine \(JavaScript VM\) to allow automation, for example, DOM nodes, CSS rules.</span></span>  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Vista Contención" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   <span data-ttu-id="2bec5-221">**Vista Contención**</span><span class="sxs-lookup"><span data-stu-id="2bec5-221">**Containment** view</span></span>  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> <span data-ttu-id="2bec5-222">Sugerencia sobre los cierres.</span><span class="sxs-lookup"><span data-stu-id="2bec5-222">A tip about closures.</span></span>  <span data-ttu-id="2bec5-223">Asigne un nombre a las funciones para que pueda distinguir fácilmente entre los cierres de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="2bec5-223">Name the functions so you are able to easily distinguish between closures in the snapshot.</span></span>  <span data-ttu-id="2bec5-224">Por ejemplo, en este ejemplo no se usan funciones con nombre.</span><span class="sxs-lookup"><span data-stu-id="2bec5-224">For example, this example does not use named functions.</span></span>  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function() { // this is NOT a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> <span data-ttu-id="2bec5-225">El fragmento de código siguiente usa funciones con nombre.</span><span class="sxs-lookup"><span data-stu-id="2bec5-225">The followingcode snippet uses named functions.</span></span>  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function lC() { // this IS a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> <!--  
> :::image type="complex" source="../media/memory-problems-domleaks.msft.png" alt-text="Name functions to distinguish between closures" lightbox="../media/memory-problems-domleaks.msft.png":::
>    Name functions to distinguish between closures  
> :::image-end:::  
> -->  
> 
> > [!NOTE]
> > <span data-ttu-id="2bec5-226">Pruebe este ejemplo de por qué [ `eval` es malo][GlitchDevtoolsMemoryExample07] analizar el impacto de los cierres en la memoria.</span><span class="sxs-lookup"><span data-stu-id="2bec5-226">Try out this example of [why `eval` is evil][GlitchDevtoolsMemoryExample07] to analyze the impact of closures on memory.</span></span>  <span data-ttu-id="2bec5-227">También puede interesarle seguirlo con este ejemplo que le lleva a través de la grabación de asignaciones [de montón][GlitchDevtoolsMemoryExample08].</span><span class="sxs-lookup"><span data-stu-id="2bec5-227">You may also be interested in following it up with this example that takes you through recording [heap allocations][GlitchDevtoolsMemoryExample08].</span></span>  
> 

## <a name="look-up-color-coding"></a><span data-ttu-id="2bec5-228">Buscar codificación de color</span><span class="sxs-lookup"><span data-stu-id="2bec5-228">Look up color coding</span></span>  

<span data-ttu-id="2bec5-229">Las propiedades y los valores de propiedad de los objetos tienen diferentes tipos y se colore en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="2bec5-229">Properties and property values of objects have different types and are colored accordingly.</span></span>  <span data-ttu-id="2bec5-230">Cada propiedad tiene uno de cuatro tipos.</span><span class="sxs-lookup"><span data-stu-id="2bec5-230">Each property has one of four types.</span></span>  

| <span data-ttu-id="2bec5-231">Tipo de propiedad</span><span class="sxs-lookup"><span data-stu-id="2bec5-231">Property Type</span></span> | <span data-ttu-id="2bec5-232">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bec5-232">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="2bec5-233">a: (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2bec5-233">a: property</span></span>** | <span data-ttu-id="2bec5-234">Una propiedad regular con un nombre, a la que se tiene acceso a través del operador \(dot\) o mediante la notación `.` `[` `]` \(brackets\), por ejemplo `["foo bar"]` .</span><span class="sxs-lookup"><span data-stu-id="2bec5-234">A regular property with a name, accessed via the `.` \(dot\) operator, or via `[` `]` \(brackets\) notation, for example `["foo bar"]`.</span></span>  |  
| **<span data-ttu-id="2bec5-235">0: elemento</span><span class="sxs-lookup"><span data-stu-id="2bec5-235">0: element</span></span>** | <span data-ttu-id="2bec5-236">Una propiedad regular con un índice numérico al que se accede a través `[` `]` de la notación \(brackets\).</span><span class="sxs-lookup"><span data-stu-id="2bec5-236">A regular property with a numeric index, accessed via `[` `]` \(brackets\) notation.</span></span>  |  
| **<span data-ttu-id="2bec5-237">a: var de contexto</span><span class="sxs-lookup"><span data-stu-id="2bec5-237">a: context var</span></span>** |  <span data-ttu-id="2bec5-238">Variable en un contexto de función, accesible por el nombre de la variable desde dentro de un cierre de función.</span><span class="sxs-lookup"><span data-stu-id="2bec5-238">A variable in a function context, accessible by the variable name from inside a function closure.</span></span>  |  
| **<span data-ttu-id="2bec5-239">a: prop del sistema</span><span class="sxs-lookup"><span data-stu-id="2bec5-239">a: system prop</span></span>** | <span data-ttu-id="2bec5-240">Una propiedad agregada por la máquina virtual de JavaScript, a la que no se puede acceder desde el código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2bec5-240">A property added by the JavaScript VM, not accessible from JavaScript code.</span></span>  |  

<span data-ttu-id="2bec5-241">Objetos designados `System` como no tienen un tipo de JavaScript correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2bec5-241">Objects designated as `System` do not have a corresponding JavaScript type.</span></span>  <span data-ttu-id="2bec5-242">Cada uno forma parte de la implementación del sistema de objetos de la vm de Javascript.</span><span class="sxs-lookup"><span data-stu-id="2bec5-242">Each is part of the object system implementation of the Javascript VM.</span></span>  <span data-ttu-id="2bec5-243">V8 asigna la mayoría de los objetos internos en el mismo montón que los objetos JS del usuario.</span><span class="sxs-lookup"><span data-stu-id="2bec5-243">V8 allocates most of the internal objects in the same heap as the user's JS objects.</span></span>  <span data-ttu-id="2bec5-244">Por lo tanto, estos son solo internos de V8.</span><span class="sxs-lookup"><span data-stu-id="2bec5-244">So these are just V8 internals.</span></span>  

## <a name="find-a-specific-object"></a><span data-ttu-id="2bec5-245">Buscar un objeto específico</span><span class="sxs-lookup"><span data-stu-id="2bec5-245">Find a specific object</span></span>  

<span data-ttu-id="2bec5-246">Para buscar un objeto en el montón recopilado, puede buscar con `Ctrl` + `F` y proporcionar el identificador del objeto.</span><span class="sxs-lookup"><span data-stu-id="2bec5-246">To find an object in the collected heap you may search using `Ctrl`+`F` and give the object ID.</span></span>  

## <a name="uncover-dom-leaks"></a><span data-ttu-id="2bec5-247">Descubrir fugas de DOM</span><span class="sxs-lookup"><span data-stu-id="2bec5-247">Uncover DOM leaks</span></span>  

<span data-ttu-id="2bec5-248">El profiler de montón tiene la capacidad de reflejar dependencias bidireccionales entre objetos nativos del explorador \(nodos DOM, reglas CSS\) y objetos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2bec5-248">The heap profiler has the ability to reflect bidirectional dependencies between browser native objects \(DOM nodes, CSS rules\) and JavaScript objects.</span></span>
<span data-ttu-id="2bec5-249">Esto ayuda a descubrir las pérdidas invisibles que se están produciendo debido a los subárboles DOM desasociados olvidados que flotan alrededor.</span><span class="sxs-lookup"><span data-stu-id="2bec5-249">This helps to discover otherwise invisible leaks happening due to forgotten detached DOM subtrees floating around.</span></span>  

<span data-ttu-id="2bec5-250">Las pérdidas de DOM pueden ser más grandes de lo que crees.</span><span class="sxs-lookup"><span data-stu-id="2bec5-250">DOM leaks may be bigger than you think.</span></span>  <span data-ttu-id="2bec5-251">Tenga en cuenta el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="2bec5-251">Consider the following sample.</span></span>  <span data-ttu-id="2bec5-252">¿Cuándo es #tree GC?</span><span class="sxs-lookup"><span data-stu-id="2bec5-252">When is the #tree GC?</span></span>  

```javascript
var select = document.querySelector;
var treeRef = select("#tree");
var leafRef = select("#leaf");
var body = select("body");
body.removeChild(treeRef);
//#tree in not GC yet due to treeRef
treeRef = null;
//#tree is not GC yet due to indirect
//reference from leafRef
leafRef = null;
//#NOW able to be #tree GC
```  

<span data-ttu-id="2bec5-253">El mantiene una referencia al elemento primario `#leaf` relevante \(parentNode\) y recursivamente hasta , por lo que solo cuando leafRef se anula es el árbol WHOLE debajo de un candidato para `#tree` `#tree` GC.</span><span class="sxs-lookup"><span data-stu-id="2bec5-253">The `#leaf` maintains a reference to the relevant parent \(parentNode\) and recursively up to `#tree`, so only when leafRef is nullified is the WHOLE tree under `#tree` a candidate for GC.</span></span>  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="Subárboles DOM" lightbox="../media/memory-problems-tree-gc.msft.png":::
   <span data-ttu-id="2bec5-255">Subárboles DOM</span><span class="sxs-lookup"><span data-stu-id="2bec5-255">DOM subtrees</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="2bec5-256">Ejemplos: pruebe este ejemplo de un nodo [DOM][GlitchDevtoolsMemoryExample06] de pérdida para comprender dónde se puede producir una pérdida y cómo detectarlo.</span><span class="sxs-lookup"><span data-stu-id="2bec5-256">Examples:  Try this example of a [leaking DOM node][GlitchDevtoolsMemoryExample06] to understand where it may leak and how to detect it.</span></span>  <span data-ttu-id="2bec5-257">También puede ver este ejemplo de [pérdidas dom siendo más grandes][GlitchDevtoolsMemoryExample09]de lo esperado.</span><span class="sxs-lookup"><span data-stu-id="2bec5-257">You may also look at this example of [DOM leaks being bigger than expected][GlitchDevtoolsMemoryExample09].</span></span>  

<span data-ttu-id="2bec5-258">Para obtener más información sobre las pérdidas de DOM y los fundamentos del análisis de memoria, consulte Búsqueda y depuración de pérdidas de memoria con [Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] de Gonzalo Ruiz de Villa.</span><span class="sxs-lookup"><span data-stu-id="2bec5-258">To read more about DOM leaks and memory analysis fundamentals checkout [Finding and debugging memory leaks with the Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] by Gonzalo Ruiz de Villa.</span></span>  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="2bec5-259">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2bec5-259">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: ./memory-101.md#object-sizes "Tamaños de objeto: terminología de memoria | Microsoft Docs"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: ./memory-101.md#objects-retaining-tree "Árbol de retención de objetos: terminología de memoria | Microsoft Docs"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "example-03.html- Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "example-06.html- Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "example-07.html- Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "example-08.html- Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "example-09.html- Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "example-10.html- Microsoft Edge (Chromium) DevTools | Glitch"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "memoria | Diapositivas"  

> [!NOTE]
> <span data-ttu-id="2bec5-269">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2bec5-269">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2bec5-270">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) y es creado por [Meggin Kearney][MegginKearney] \(Technical Writer\).</span><span class="sxs-lookup"><span data-stu-id="2bec5-270">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2bec5-272">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2bec5-272">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

---
title: Cómo grabar instantáneas de montones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e6f64b219bc2b28d01780c28cc605d56a07cb491
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611681"
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





# <span data-ttu-id="4e1af-103">Cómo grabar instantáneas de montones</span><span class="sxs-lookup"><span data-stu-id="4e1af-103">How to Record Heap Snapshots</span></span>   



<span data-ttu-id="4e1af-104">Obtenga información sobre cómo grabar instantáneas de montones con el analizador de montones de Microsoft Edge DevTools y buscar pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="4e1af-104">Learn how to record heap snapshots with the Microsoft Edge DevTools heap profiler and find memory leaks.</span></span>  

<span data-ttu-id="4e1af-105">El analizador de montones de DevTools de Microsoft Edge muestra la distribución de memoria mediante los objetos de JavaScript y los nodos DOM relacionados de la página.</span><span class="sxs-lookup"><span data-stu-id="4e1af-105">The Microsoft Edge DevTools heap profiler shows memory distribution by the JavaScript objects and related DOM nodes of your page.</span></span>  <span data-ttu-id="4e1af-106">Utilícelo para tomar instantáneas del montón \ (JS heap \) de montón de JavaScript, analizar gráficos de memoria, Comparar instantáneas y buscar pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="4e1af-106">Use it to take JavaScript heap \(JS heap\) snapshots, analyze memory graphs, compare snapshots, and find memory leaks.</span></span>  <span data-ttu-id="4e1af-107">Vea también [objetos reteniendo árbol][DevtoolsMemoryProblems101ObjectsRetainingTree].</span><span class="sxs-lookup"><span data-stu-id="4e1af-107">See also [Objects retaining tree][DevtoolsMemoryProblems101ObjectsRetainingTree].</span></span>  

## <span data-ttu-id="4e1af-108">Tomar una instantánea</span><span class="sxs-lookup"><span data-stu-id="4e1af-108">Take a snapshot</span></span>  

<span data-ttu-id="4e1af-109">En el panel **memoria** , elija **tomar instantánea**y, a continuación, haga clic en **iniciar**.</span><span class="sxs-lookup"><span data-stu-id="4e1af-109">On the **Memory** panel, choose **Take snapshot**, then click **Start**.</span></span>  <span data-ttu-id="4e1af-110">También puede pulsar `Ctrl` + `E` \ (Windows \) o `Cmd` + `E` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="4e1af-110">You may also press `Ctrl`+`E` \(Windows\) or `Cmd`+`E` \(macOS\).</span></span>  

> ##### <span data-ttu-id="4e1af-111">Figura 1</span><span class="sxs-lookup"><span data-stu-id="4e1af-111">Figure 1</span></span>  
> <span data-ttu-id="4e1af-112">Seleccionar tipo de generación de perfiles</span><span class="sxs-lookup"><span data-stu-id="4e1af-112">Select profiling type</span></span>  
> ![Seleccionar tipo de generación de perfiles][ImageProfilingType]  

<span data-ttu-id="4e1af-114">Las **instantáneas** se almacenan inicialmente en la memoria del proceso del representador.</span><span class="sxs-lookup"><span data-stu-id="4e1af-114">**Snapshots** are initially stored in the renderer process memory.</span></span>  <span data-ttu-id="4e1af-115">Las instantáneas se transfieren a la DevTools a petición, al hacer clic en el icono de instantánea para verlo.</span><span class="sxs-lookup"><span data-stu-id="4e1af-115">Snapshots are transferred to the DevTools on demand, when you click on the snapshot icon to view it.</span></span>  

<span data-ttu-id="4e1af-116">Una vez que la instantánea se ha cargado en DevTools y se ha analizado, aparece el número debajo del título de la instantánea, que muestra el [Tamaño total de los objetos de JavaScript accesibles][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="4e1af-116">After the snapshot has been loaded into DevTools and has been parsed, the number below the snapshot title appears and shows the [total size of the reachable JavaScript objects][DevtoolsMemoryProblems101ObjectSizes].</span></span>  

> ##### <span data-ttu-id="4e1af-117">Figura 2</span><span class="sxs-lookup"><span data-stu-id="4e1af-117">Figure 2</span></span>  
> <span data-ttu-id="4e1af-118">Tamaño total de objetos accesibles</span><span class="sxs-lookup"><span data-stu-id="4e1af-118">Total size of reachable objects</span></span>  
> ![Tamaño total de objetos accesibles][ImageTotalSize]  

> [!NOTE]
> <span data-ttu-id="4e1af-120">Solo los objetos accesibles se incluyen en las instantáneas.</span><span class="sxs-lookup"><span data-stu-id="4e1af-120">Only reachable objects are included in snapshots.</span></span>  <span data-ttu-id="4e1af-121">Además, tomar una instantánea siempre comienza con una recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="4e1af-121">Also, taking a snapshot always starts with a garbage collection.</span></span>  

## <span data-ttu-id="4e1af-122">Borrar instantáneas</span><span class="sxs-lookup"><span data-stu-id="4e1af-122">Clear snapshots</span></span>  

<span data-ttu-id="4e1af-123">Haga clic en el icono **borrar todos los perfiles** para quitar las instantáneas \ (tanto de DevTools como de cualquier memoria asociada al proceso de representación \).</span><span class="sxs-lookup"><span data-stu-id="4e1af-123">Click **Clear all profiles** icon to remove snapshots \(both from DevTools and any memory associated with the renderer process\).</span></span>  

> ##### <span data-ttu-id="4e1af-124">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="4e1af-124">Figure 3</span></span>  
> <span data-ttu-id="4e1af-125">Quitar instantáneas</span><span class="sxs-lookup"><span data-stu-id="4e1af-125">Remove snapshots</span></span>  
> ![Quitar instantáneas][ImageRemoveSnapshots]  

<span data-ttu-id="4e1af-127">Al cerrar la ventana DevTools, no se eliminan los perfiles de la memoria asociada con el proceso de representación.</span><span class="sxs-lookup"><span data-stu-id="4e1af-127">Closing the DevTools window does not delete profiles from the memory associated with the renderer process.</span></span>  <span data-ttu-id="4e1af-128">Al volver a abrir DevTools, todas las instantáneas tomadas anteriormente volverán a aparecer en la lista de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="4e1af-128">When reopening DevTools, all previously taken snapshots reappear in the list of snapshots.</span></span>  

> [!NOTE]
> <span data-ttu-id="4e1af-129">Pruebe este ejemplo de [objetos dispersos][GlitchDevtoolsMemoryExample03] y envíelo con el generador de perfiles de montones.</span><span class="sxs-lookup"><span data-stu-id="4e1af-129">Try out this example of [scattered objects][GlitchDevtoolsMemoryExample03] and profile it using the Heap Profiler.</span></span>  <span data-ttu-id="4e1af-130">Debería ver varias asignaciones de elementos \ (objeto \).</span><span class="sxs-lookup"><span data-stu-id="4e1af-130">You should see a number of \(object\) item allocations.</span></span>  

## <span data-ttu-id="4e1af-131">Ver instantáneas</span><span class="sxs-lookup"><span data-stu-id="4e1af-131">View snapshots</span></span>  

<span data-ttu-id="4e1af-132">Ver instantáneas de diferentes perspectivas para tareas diferentes.</span><span class="sxs-lookup"><span data-stu-id="4e1af-132">View snapshots from different perspectives for different tasks.</span></span>  

<span data-ttu-id="4e1af-133">La **vista de Resumen** muestra los objetos agrupados por el nombre del constructor.</span><span class="sxs-lookup"><span data-stu-id="4e1af-133">**Summary view** shows objects grouped by the constructor name.</span></span>  <span data-ttu-id="4e1af-134">Se usa para buscar objetos \ (y el uso de memoria \) según el tipo agrupado por nombre de constructor.</span><span class="sxs-lookup"><span data-stu-id="4e1af-134">Use it to hunt down objects \(and the memory use\) based on type grouped by constructor name.</span></span>  <span data-ttu-id="4e1af-135">Es especialmente útil para **rastrear las pérdidas de Dom**.</span><span class="sxs-lookup"><span data-stu-id="4e1af-135">It is particularly helpful for **tracking down DOM leaks**.</span></span>

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

<span data-ttu-id="4e1af-136">**Vista de comparación**.</span><span class="sxs-lookup"><span data-stu-id="4e1af-136">**Comparison view**.</span></span>  <span data-ttu-id="4e1af-137">Muestra la diferencia entre dos instantáneas.</span><span class="sxs-lookup"><span data-stu-id="4e1af-137">Displays the difference between two snapshots.</span></span>  <span data-ttu-id="4e1af-138">Utilícelo para comparar dos (o más \) instantáneas de memoria de antes y después de una operación.</span><span class="sxs-lookup"><span data-stu-id="4e1af-138">Use it to compare two \(or more\) memory snapshots from before and after an operation.</span></span>  <span data-ttu-id="4e1af-139">Inspeccionar el delta en la memoria liberada y el recuento de referencias le permite confirmar la presencia y la causa de una pérdida de memoria.</span><span class="sxs-lookup"><span data-stu-id="4e1af-139">Inspecting the delta in freed memory and reference count lets you confirm the presence and cause of a memory leak.</span></span>  

<span data-ttu-id="4e1af-140">**Vista de inclusión**.</span><span class="sxs-lookup"><span data-stu-id="4e1af-140">**Containment view**.</span></span>  <span data-ttu-id="4e1af-141">Permite la exploración del contenido del montón.</span><span class="sxs-lookup"><span data-stu-id="4e1af-141">Allows exploration of heap contents.</span></span>  <span data-ttu-id="4e1af-142">La **vista contención** ofrece una mejor vista de la estructura del objeto, lo que ayuda a analizar los objetos a los que se hace referencia en el espacio de nombres global \ (ventana \) para descubrir de qué está manteniendo los objetos.</span><span class="sxs-lookup"><span data-stu-id="4e1af-142">**Containment view** provides a better view of object structure, helping analyze objects referenced in the global namespace \(window\) to find out what is keeping objects around.</span></span>  <span data-ttu-id="4e1af-143">Úsela para analizar los cierres y profundizar en los objetos a un bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="4e1af-143">Use it to analyze closures and dive into your objects at a low level.</span></span>  

<span data-ttu-id="4e1af-144">Para cambiar entre las vistas, use el selector de la parte superior de la vista.</span><span class="sxs-lookup"><span data-stu-id="4e1af-144">To switch between views, use the selector at the top of the view.</span></span>  

> ##### <span data-ttu-id="4e1af-145">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="4e1af-145">Figure 4</span></span>  
> <span data-ttu-id="4e1af-146">Cambiar el selector de vistas</span><span class="sxs-lookup"><span data-stu-id="4e1af-146">Switch views selector</span></span>  
> ![Cambiar el selector de vistas][ImageSwitchViews]  

> [!NOTE]
> <span data-ttu-id="4e1af-148">No todas las propiedades se almacenan en el montón de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4e1af-148">Not all properties are stored on the JavaScript heap.</span></span>  <span data-ttu-id="4e1af-149">Las propiedades implementadas mediante captadores que ejecutan código nativo no se capturan.</span><span class="sxs-lookup"><span data-stu-id="4e1af-149">Properties implemented using getters that run native code are not captured.</span></span>  <span data-ttu-id="4e1af-150">Además, no se capturan valores que no sean de cadena, como los números.</span><span class="sxs-lookup"><span data-stu-id="4e1af-150">Also, non-string values such as numbers are not captured.</span></span>  

### <span data-ttu-id="4e1af-151">Vista de Resumen</span><span class="sxs-lookup"><span data-stu-id="4e1af-151">Summary view</span></span>  

<span data-ttu-id="4e1af-152">Inicialmente, se abre una instantánea en la vista de Resumen, que muestra los totales de los objetos, que se pueden expandir para mostrar las instancias:</span><span class="sxs-lookup"><span data-stu-id="4e1af-152">Initially, a snapshot opens in the Summary view, displaying object totals, which may be expanded to show instances:</span></span>  

> ##### <span data-ttu-id="4e1af-153">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="4e1af-153">Figure 5</span></span>  
> <span data-ttu-id="4e1af-154">Vista de Resumen</span><span class="sxs-lookup"><span data-stu-id="4e1af-154">Summary view</span></span>  
> ![Vista de Resumen][ImageSummaryView]  

<span data-ttu-id="4e1af-156">Las entradas de nivel superior son líneas de "total".</span><span class="sxs-lookup"><span data-stu-id="4e1af-156">Top-level entries are "total" lines.</span></span>  

| <span data-ttu-id="4e1af-157">Entradas de nivel superior</span><span class="sxs-lookup"><span data-stu-id="4e1af-157">Top-level entries</span></span> | <span data-ttu-id="4e1af-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e1af-158">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="4e1af-159">Constructor</span><span class="sxs-lookup"><span data-stu-id="4e1af-159">Constructor</span></span>** | <span data-ttu-id="4e1af-160">Representa todos los objetos creados con este constructor.</span><span class="sxs-lookup"><span data-stu-id="4e1af-160">Represents all objects created using this constructor.</span></span>  |  
| **<span data-ttu-id="4e1af-161">Distancia</span><span class="sxs-lookup"><span data-stu-id="4e1af-161">Distance</span></span>** | <span data-ttu-id="4e1af-162">muestra la distancia a la raíz mediante la ruta de acceso más corta de los nodos.</span><span class="sxs-lookup"><span data-stu-id="4e1af-162">displays the distance to the root using the shortest simple path of nodes.</span></span>  |  
| **<span data-ttu-id="4e1af-163">Tamaño superficial</span><span class="sxs-lookup"><span data-stu-id="4e1af-163">Shallow size</span></span>** | <span data-ttu-id="4e1af-164">Muestra la suma de los tamaños superficiales de todos los objetos creados por una determinada función constructora.</span><span class="sxs-lookup"><span data-stu-id="4e1af-164">Displays the sum of shallow sizes of all objects created by a certain constructor function.</span></span>  <span data-ttu-id="4e1af-165">El tamaño superficial es el tamaño de la memoria que mantiene un objeto \ (generalmente, las matrices y cadenas tienen tamaños superficiales mayores \).</span><span class="sxs-lookup"><span data-stu-id="4e1af-165">The shallow size is the size of memory held by an object \(generally, arrays and strings have larger shallow sizes\).</span></span>  <span data-ttu-id="4e1af-166">Vea también [tamaños de objeto][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="4e1af-166">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  
| **<span data-ttu-id="4e1af-167">Tamaño retenido</span><span class="sxs-lookup"><span data-stu-id="4e1af-167">Retained size</span></span>** | <span data-ttu-id="4e1af-168">Muestra el tamaño máximo retenido entre el mismo conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="4e1af-168">Displays the maximum retained size among the same set of objects.</span></span>  <span data-ttu-id="4e1af-169">El tamaño de la memoria que puede liberar después de que se elimine un objeto \ (y los dependientes ya no se pueden alcanzar \) se denomina tamaño conservado.</span><span class="sxs-lookup"><span data-stu-id="4e1af-169">The size of memory that you are able to free after an object is deleted \(and the dependents are made no longer reachable\) is called the retained size.</span></span>  <span data-ttu-id="4e1af-170">Vea también [tamaños de objeto][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="4e1af-170">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

<span data-ttu-id="4e1af-171">Después de expandir una línea total en la vista superior, se muestran todas las instancias.</span><span class="sxs-lookup"><span data-stu-id="4e1af-171">After expanding a total line in the upper view, all of the instances are displayed.</span></span>  <span data-ttu-id="4e1af-172">Para cada instancia, los tamaños superficiales y retenidos se muestran en las columnas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="4e1af-172">For each instance, the shallow and retained sizes are displayed in the corresponding columns.</span></span>  <span data-ttu-id="4e1af-173">El número después del `@` carácter es el identificador único del objeto, lo que le permite comparar instantáneas de montones en función de cada objeto.</span><span class="sxs-lookup"><span data-stu-id="4e1af-173">The number after the `@` character is the unique ID of the object, allowing you to compare heap snapshots on per-object basis.</span></span>  

<span data-ttu-id="4e1af-174">Recuerde que los objetos amarillos tienen referencias de JavaScript y los objetos rojos son nodos desvinculados a los que se hace referencia desde uno con un fondo amarillo.</span><span class="sxs-lookup"><span data-stu-id="4e1af-174">Remember that yellow objects have JavaScript references and red objects are detached nodes which are referenced from one with a yellow background.</span></span>  

**<span data-ttu-id="4e1af-175">¿Para qué se corresponden las diversas entradas de constructor \ (grupo \) en el generador de perfiles del montón?</span><span class="sxs-lookup"><span data-stu-id="4e1af-175">What do the various constructor \(group\) entries in the Heap profiler correspond to?</span></span>**  

> ##### <span data-ttu-id="4e1af-176">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="4e1af-176">Figure 6</span></span>  
> <span data-ttu-id="4e1af-177">Grupos de constructores</span><span class="sxs-lookup"><span data-stu-id="4e1af-177">Constructor groups</span></span>  
> ![Grupos de constructores][ImageConstructorGroups]  

| <span data-ttu-id="4e1af-179">Entrada de constructor \ (grupo \)</span><span class="sxs-lookup"><span data-stu-id="4e1af-179">Constructor \(group\) entry</span></span> | <span data-ttu-id="4e1af-180">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e1af-180">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="4e1af-181">\ (propiedad global \)</span><span class="sxs-lookup"><span data-stu-id="4e1af-181">\(global property\)</span></span>** | <span data-ttu-id="4e1af-182">Los objetos intermedios entre un objeto global \ (como `window` \) y un objeto al que hace referencia.</span><span class="sxs-lookup"><span data-stu-id="4e1af-182">The intermediate objects between a global object \(like `window`\) and an object referenced by it.</span></span>  <span data-ttu-id="4e1af-183">Si se crea un objeto con un constructor `Person` y es retenido por un objeto global, la ruta de retención tendrá el aspecto siguiente `[global] > \(global property\) > Person` .</span><span class="sxs-lookup"><span data-stu-id="4e1af-183">If an object is created using a constructor `Person` and is held by a global object, the retaining path would look like `[global] > \(global property\) > Person`.</span></span>  <span data-ttu-id="4e1af-184">Esto contrasta con la norma, donde los objetos se hacen referencia directamente entre sí.</span><span class="sxs-lookup"><span data-stu-id="4e1af-184">This contrasts with the norm, where objects directly reference each other.</span></span>  <span data-ttu-id="4e1af-185">Los objetos intermedios existen por razones de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4e1af-185">Intermediate objects exist for performance reasons.</span></span>  <span data-ttu-id="4e1af-186">Las globales se modifican periódicamente y las optimizaciones de acceso a la propiedad hacen un buen trabajo para los objetos no globales que no son aplicables a los usuarios globales.</span><span class="sxs-lookup"><span data-stu-id="4e1af-186">Globals are modified regularly and property access optimizations do a good job for non-global objects are not applicable for globals.</span></span>  |  
| **<span data-ttu-id="4e1af-187">\ (raíces \)</span><span class="sxs-lookup"><span data-stu-id="4e1af-187">\(roots\)</span></span>** | <span data-ttu-id="4e1af-188">Las entradas raíz de la vista de árbol de retención son las entidades que tienen referencias al objeto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4e1af-188">The root entries in the retaining tree view are the entities that have references to the selected object.</span></span>  <span data-ttu-id="4e1af-189">Las entradas también pueden ser referencias creadas por el motor para fines específicos del motor.</span><span class="sxs-lookup"><span data-stu-id="4e1af-189">The entries may also be references created by the engine for engine-specific purposes.</span></span>  <span data-ttu-id="4e1af-190">El motor tiene cachés que hacen referencia a objetos, pero todas estas referencias son débiles y no impiden que se recopile un objeto dado que no hay referencias realmente fuertes.</span><span class="sxs-lookup"><span data-stu-id="4e1af-190">The engine has caches which reference objects, but all such references are weak and do not prevent an object from being collected given that there are no truly strong references.</span></span>  |  
| **<span data-ttu-id="4e1af-191">\ (cierre \)</span><span class="sxs-lookup"><span data-stu-id="4e1af-191">\(closure\)</span></span>** | <span data-ttu-id="4e1af-192">Un recuento de referencias a un grupo de objetos a través de cierres de función.</span><span class="sxs-lookup"><span data-stu-id="4e1af-192">A count of references to a group of objects through function closures.</span></span>  |  
| **<span data-ttu-id="4e1af-193">\ (matriz, cadena, número, RegExp \)</span><span class="sxs-lookup"><span data-stu-id="4e1af-193">\(array, string, number, regexp\)</span></span>** | <span data-ttu-id="4e1af-194">Una lista de tipos de objeto con propiedades que hacen referencia a una matriz, una cadena, un número o una expresión regular.</span><span class="sxs-lookup"><span data-stu-id="4e1af-194">A list of object types with properties which reference an Array, String, Number, or regular expression.</span></span>  |  
| **<span data-ttu-id="4e1af-195">\ (código compilado \)</span><span class="sxs-lookup"><span data-stu-id="4e1af-195">\(compiled code\)</span></span>** | <span data-ttu-id="4e1af-196">Todo lo relacionado con el código compilado.</span><span class="sxs-lookup"><span data-stu-id="4e1af-196">Everything related to compiled code.</span></span>  <span data-ttu-id="4e1af-197">El script es similar a una función, pero se corresponde con un `<script>` cuerpo.</span><span class="sxs-lookup"><span data-stu-id="4e1af-197">Script is similar to a function, but corresponds to a `<script>` body.</span></span>  <span data-ttu-id="4e1af-198">SharedFunctionInfos \ (SFI \) están en los objetos entre las funciones y el código compilado.</span><span class="sxs-lookup"><span data-stu-id="4e1af-198">SharedFunctionInfos \(SFI\) are objects standing between functions and compiled code.</span></span>  <span data-ttu-id="4e1af-199">Las funciones suelen tener un contexto, mientras que SFIs no.</span><span class="sxs-lookup"><span data-stu-id="4e1af-199">Functions usually have a context, while SFIs do not.</span></span>  |  
| <span data-ttu-id="4e1af-200">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, etc.</span><span class="sxs-lookup"><span data-stu-id="4e1af-200">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, and so on.</span></span>  | <span data-ttu-id="4e1af-201">Referencias a elementos o objetos de documento de un tipo específico al que hace referencia el código.</span><span class="sxs-lookup"><span data-stu-id="4e1af-201">References to elements or document objects of a particular type referenced by your code.</span></span>  |  

<!--todo: add heap profiling summary section when available -->  

### <span data-ttu-id="4e1af-202">Vista comparación</span><span class="sxs-lookup"><span data-stu-id="4e1af-202">Comparison view</span></span>  

<span data-ttu-id="4e1af-203">Busque objetos perdidos comparando varias instantáneas entre sí.</span><span class="sxs-lookup"><span data-stu-id="4e1af-203">Find leaked objects by comparing multiple snapshots to each other.</span></span>  <span data-ttu-id="4e1af-204">Para comprobar que una determinada operación de la aplicación no crea fugas \ (por ejemplo, normalmente un par de operaciones directas e inversas, como abrir un documento y, a continuación, cerrarla, no debe salir de los residuos \), puede seguir el siguiente escenario:</span><span class="sxs-lookup"><span data-stu-id="4e1af-204">To verify that a certain application operation does not create leaks \(for example, usually a pair of direct and reverse operations, like opening a document, and then closing it, should not leave any garbage\), you may follow the scenario below:</span></span>  

1.  <span data-ttu-id="4e1af-205">Tomar una instantánea del montón antes de realizar una operación.</span><span class="sxs-lookup"><span data-stu-id="4e1af-205">Take a heap snapshot before performing an operation.</span></span>  
1.  <span data-ttu-id="4e1af-206">Realice una operación \ (interactúe con una página de alguna manera que considere que está causando una fuga \).</span><span class="sxs-lookup"><span data-stu-id="4e1af-206">Perform an operation \(interact with a page in some way that you believe to be causing a leak\).</span></span>  
1.  <span data-ttu-id="4e1af-207">Realizar una operación inversa \ (hacer la interacción opuesta y repetir varias veces \).</span><span class="sxs-lookup"><span data-stu-id="4e1af-207">Perform a reverse operation \(do the opposite interaction and repeat it a few times\).</span></span>  
1.  <span data-ttu-id="4e1af-208">Tomar una segunda instantánea del montón y cambiar la vista de esta para **compararla, comparándola**con la **instantánea 1**.</span><span class="sxs-lookup"><span data-stu-id="4e1af-208">Take a second heap snapshot and change the view of this one to **Comparison**, comparing it to **Snapshot 1**.</span></span>  

<span data-ttu-id="4e1af-209">En la vista **comparación** , se muestra la diferencia entre dos instantáneas.</span><span class="sxs-lookup"><span data-stu-id="4e1af-209">In the **Comparison** view, the difference between two snapshots is displayed.</span></span>  <span data-ttu-id="4e1af-210">Al expandir una entrada total, se muestran instancias de objeto eliminadas y agregadas.</span><span class="sxs-lookup"><span data-stu-id="4e1af-210">When expanding a total entry, added and deleted object instances are shown.</span></span>  

> ##### <span data-ttu-id="4e1af-211">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="4e1af-211">Figure 7</span></span>  
> <span data-ttu-id="4e1af-212">Vista comparación</span><span class="sxs-lookup"><span data-stu-id="4e1af-212">Comparison view</span></span>  
> ![Vista comparación][ImageComparisonView]  

<!--todo: add HeapProfilingComparison section when available  -->  

### <span data-ttu-id="4e1af-214">Vista de contención</span><span class="sxs-lookup"><span data-stu-id="4e1af-214">Containment view</span></span>  

<span data-ttu-id="4e1af-215">La vista **contención** es esencialmente una "vista de pájaro" de la estructura de objetos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e1af-215">The **Containment** view is essentially a "bird's eye view" of the objects structure of your application.</span></span>  <span data-ttu-id="4e1af-216">Le permite realizar un vistazo a los cierres de función para observar los objetos internos de la máquina virtual \ (VM \) que juntos componen los objetos de JavaScript y comprender cuánta memoria usa la aplicación en un nivel muy bajo.</span><span class="sxs-lookup"><span data-stu-id="4e1af-216">It allows you to peek inside function closures, to observe virtual machine \(VM\) internal objects that together make up your JavaScript objects, and to understand how much memory your application uses at a very low level.</span></span>  

| <span data-ttu-id="4e1af-217">Puntos de entrada de la vista de contención</span><span class="sxs-lookup"><span data-stu-id="4e1af-217">Containment view entry points</span></span> | <span data-ttu-id="4e1af-218">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e1af-218">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="4e1af-219">Objetos DOMWindow</span><span class="sxs-lookup"><span data-stu-id="4e1af-219">DOMWindow objects</span></span>** | <span data-ttu-id="4e1af-220">Objetos globales para el código de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4e1af-220">Global objects for JavaScript code.</span></span>  |  
| **<span data-ttu-id="4e1af-221">Raíces de GC</span><span class="sxs-lookup"><span data-stu-id="4e1af-221">GC roots</span></span>** | <span data-ttu-id="4e1af-222">Las raíces de GC reales usadas por el uso de los elementos no usados de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4e1af-222">The actual GC roots used by the garbage of the VM.</span></span>  <span data-ttu-id="4e1af-223">Las raíces de GC se componen de mapas de objetos integrados, tablas de símbolos, pilas de subprocesos de VM, memorias caché de compilación, ámbitos de administración y identificadores globales.</span><span class="sxs-lookup"><span data-stu-id="4e1af-223">GC roots are comprised of built-in object maps, symbol tables, VM thread stacks, compilation caches, handle scopes, and global handles.</span></span>  |  
| **<span data-ttu-id="4e1af-224">Objetos nativos</span><span class="sxs-lookup"><span data-stu-id="4e1af-224">Native objects</span></span>** | <span data-ttu-id="4e1af-225">Los objetos del explorador "se insertan" dentro de la máquina virtual de JavaScript \ (Java VM \) para permitir la automatización, por ejemplo, los nodos DOM, las reglas CSS.</span><span class="sxs-lookup"><span data-stu-id="4e1af-225">Browser objects "pushed" inside the JavaScript virtual machine \(JavaScript VM\) to allow automation, for example, DOM nodes, CSS rules.</span></span>  |  

> ##### <span data-ttu-id="4e1af-226">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="4e1af-226">Figure 8</span></span>  
> <span data-ttu-id="4e1af-227">Vista de contención</span><span class="sxs-lookup"><span data-stu-id="4e1af-227">Containment view</span></span>  
> ![Vista de contención][ImageContainmentView]  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> <span data-ttu-id="4e1af-229">Información sobre cierres.</span><span class="sxs-lookup"><span data-stu-id="4e1af-229">A tip about closures.</span></span>  <span data-ttu-id="4e1af-230">Asigne un nombre a las funciones de modo que pueda distinguir fácilmente entre cierres de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="4e1af-230">Name the functions so you are able to easily distinguish between closures in the snapshot.</span></span>  <span data-ttu-id="4e1af-231">Por ejemplo, en este ejemplo no se usan funciones con nombre.</span><span class="sxs-lookup"><span data-stu-id="4e1af-231">For example, this example does not use named functions.</span></span>  
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
> <span data-ttu-id="4e1af-232">Este ejemplo usa funciones con nombre:</span><span class="sxs-lookup"><span data-stu-id="4e1af-232">This example uses named functions:</span></span>  
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
> > ##### old Figure 9  
> > Name functions to distinguish between closures  
> > ![Name functions to distinguish between closures][ImageDomLeaks]  
> -->  
> 
> > [!NOTE]
> > <span data-ttu-id="4e1af-233">Pruebe este ejemplo para saber [por qué `eval` es malo][GlitchDevtoolsMemoryExample07] analizar el impacto de los cierres en la memoria.</span><span class="sxs-lookup"><span data-stu-id="4e1af-233">Try out this example of [why `eval` is evil][GlitchDevtoolsMemoryExample07] to analyze the impact of closures on memory.</span></span>  <span data-ttu-id="4e1af-234">También puede estar interesado en seguirlo con este ejemplo que le guiará a través de la grabación de [asignaciones del montón][GlitchDevtoolsMemoryExample08].</span><span class="sxs-lookup"><span data-stu-id="4e1af-234">You may also be interested in following it up with this example that takes you through recording [heap allocations][GlitchDevtoolsMemoryExample08].</span></span>  
> 

## <span data-ttu-id="4e1af-235">Buscar códigos de colores</span><span class="sxs-lookup"><span data-stu-id="4e1af-235">Look up color coding</span></span>  

<span data-ttu-id="4e1af-236">Las propiedades y los valores de propiedad de los objetos tienen tipos diferentes y se colorean según corresponda.</span><span class="sxs-lookup"><span data-stu-id="4e1af-236">Properties and property values of objects have different types and are colored accordingly.</span></span>  <span data-ttu-id="4e1af-237">Cada propiedad tiene uno de cuatro tipos.</span><span class="sxs-lookup"><span data-stu-id="4e1af-237">Each property has one of four types.</span></span>  

| <span data-ttu-id="4e1af-238">Tipo de propiedad</span><span class="sxs-lookup"><span data-stu-id="4e1af-238">Property Type</span></span> | <span data-ttu-id="4e1af-239">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e1af-239">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="4e1af-240">a: (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4e1af-240">a: property</span></span>** | <span data-ttu-id="4e1af-241">Una propiedad normal con un nombre, al que se accede mediante el `.` operador \ (punto \) o mediante la `[` `]` notación \ (corchetes \), por ejemplo `["foo bar"]` .</span><span class="sxs-lookup"><span data-stu-id="4e1af-241">A regular property with a name, accessed via the `.` \(dot\) operator, or via `[` `]` \(brackets\) notation, for example `["foo bar"]`.</span></span>  |  
| **<span data-ttu-id="4e1af-242">elemento 0:</span><span class="sxs-lookup"><span data-stu-id="4e1af-242">0: element</span></span>** | <span data-ttu-id="4e1af-243">Una propiedad normal con un índice numérico, al que se accede mediante la `[` `]` notación \ (corchetes \).</span><span class="sxs-lookup"><span data-stu-id="4e1af-243">A regular property with a numeric index, accessed via `[` `]` \(brackets\) notation.</span></span>  |  
| **<span data-ttu-id="4e1af-244">a: var de contexto</span><span class="sxs-lookup"><span data-stu-id="4e1af-244">a: context var</span></span>** |  <span data-ttu-id="4e1af-245">Variable en un contexto de función, accesible por el nombre de la variable desde un cierre de función.</span><span class="sxs-lookup"><span data-stu-id="4e1af-245">A variable in a function context, accessible by the variable name from inside a function closure.</span></span>  |  
| **<span data-ttu-id="4e1af-246">a: Prop del sistema</span><span class="sxs-lookup"><span data-stu-id="4e1af-246">a: system prop</span></span>** | <span data-ttu-id="4e1af-247">Una propiedad agregada por la VM de JavaScript, no accesible desde el código de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4e1af-247">A property added by the JavaScript VM, not accessible from JavaScript code.</span></span>  |  

<span data-ttu-id="4e1af-248">Los objetos designados como `System` no tienen un tipo de JavaScript correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4e1af-248">Objects designated as `System` do not have a corresponding JavaScript type.</span></span>  <span data-ttu-id="4e1af-249">Cada uno es parte de la implementación del sistema de objetos de la VM de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4e1af-249">Each is part of the object system implementation of the Javascript VM.</span></span>  <span data-ttu-id="4e1af-250">V8 asigna la mayoría de los objetos internos en el mismo montón que los objetos JS del usuario.</span><span class="sxs-lookup"><span data-stu-id="4e1af-250">V8 allocates most of the internal objects in the same heap as the user's JS objects.</span></span>  <span data-ttu-id="4e1af-251">Por eso, son solo 8.</span><span class="sxs-lookup"><span data-stu-id="4e1af-251">So these are just V8 internals.</span></span>  

## <span data-ttu-id="4e1af-252">Buscar un objeto específico</span><span class="sxs-lookup"><span data-stu-id="4e1af-252">Find a specific object</span></span>  

<span data-ttu-id="4e1af-253">Para encontrar un objeto en el montón recopilado, puede realizar la búsqueda con `Ctrl` + `F` el identificador de objeto y darle el nombre.</span><span class="sxs-lookup"><span data-stu-id="4e1af-253">To find an object in the collected heap you may search using `Ctrl`+`F` and give the object ID.</span></span>  

## <span data-ttu-id="4e1af-254">Descubrir fugas de DOM</span><span class="sxs-lookup"><span data-stu-id="4e1af-254">Uncover DOM leaks</span></span>  

<span data-ttu-id="4e1af-255">El generador de perfiles de pila tiene la capacidad de reflejar las dependencias bidireccionales entre objetos nativos del explorador \ (nodos DOM, reglas CSS \) y objetos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4e1af-255">The heap profiler has the ability to reflect bidirectional dependencies between browser native objects \(DOM nodes, CSS rules\) and JavaScript objects.</span></span>
<span data-ttu-id="4e1af-256">Esto ayuda a descubrir de otra manera las pérdidas invisibles debido a la olvido de subárboles de DOM desvinculados.</span><span class="sxs-lookup"><span data-stu-id="4e1af-256">This helps to discover otherwise invisible leaks happening due to forgotten detached DOM subtrees floating around.</span></span>  

<span data-ttu-id="4e1af-257">Las fugas de DOM pueden ser más grandes de lo que crees.</span><span class="sxs-lookup"><span data-stu-id="4e1af-257">DOM leaks may be bigger than you think.</span></span>  <span data-ttu-id="4e1af-258">Considere el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4e1af-258">Consider the following sample.</span></span>  <span data-ttu-id="4e1af-259">¿Cuándo está el #tree GC?</span><span class="sxs-lookup"><span data-stu-id="4e1af-259">When is the #tree GC?</span></span>  

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

<span data-ttu-id="4e1af-260">El `#leaf` mantiene una referencia a los elementos primarios \ (parentNode \) y, de forma recursiva, hasta el momento en que `#tree` el leafRef se ha anulado es todo el árbol bajo `#tree` un candidato para GC.</span><span class="sxs-lookup"><span data-stu-id="4e1af-260">The `#leaf` maintains a reference to the relevant parent \(parentNode\) and recursively up to `#tree`, so only when leafRef is nullified is the WHOLE tree under `#tree` a candidate for GC.</span></span>  

> ##### <span data-ttu-id="4e1af-261">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="4e1af-261">Figure 9</span></span>  
> <span data-ttu-id="4e1af-262">Subárboles DOM</span><span class="sxs-lookup"><span data-stu-id="4e1af-262">DOM subtrees</span></span>  
> <span data-ttu-id="4e1af-263">! [Subárboles DOM] [ImageTreeGc]</span><span class="sxs-lookup"><span data-stu-id="4e1af-263">![DOM subtrees][ImageTreeGc]</span></span>  

> [!NOTE]
> <span data-ttu-id="4e1af-264">Ejemplos: Pruebe este ejemplo de un [nodo DOM de pérdida][GlitchDevtoolsMemoryExample06] de información para comprender dónde se puede filtrar y cómo detectarlo.</span><span class="sxs-lookup"><span data-stu-id="4e1af-264">Examples:  Try this example of a [leaking DOM node][GlitchDevtoolsMemoryExample06] to understand where it may leak and how to detect it.</span></span>  <span data-ttu-id="4e1af-265">También puede ver este ejemplo de [fugas de Dom de mayor tamaño de lo esperado][GlitchDevtoolsMemoryExample09].</span><span class="sxs-lookup"><span data-stu-id="4e1af-265">You may also look at this example of [DOM leaks being bigger than expected][GlitchDevtoolsMemoryExample09].</span></span>  

<span data-ttu-id="4e1af-266">Para obtener más información sobre las pérdidas de DOM y el análisis de memoria fundamentos de desprotección [Buscar y depurar pérdidas de memoria con Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] por Gonzalo Ruiz de Villa.</span><span class="sxs-lookup"><span data-stu-id="4e1af-266">To read more about DOM leaks and memory analysis fundamentals checkout [Finding and debugging memory leaks with the Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] by Gonzalo Ruiz de Villa.</span></span>  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

<!--## Feedback   -->  



<!-- image links -->  

[ImageProfilingType]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png "Ilustración 1: seleccionar el tipo de generación de perfiles"  
[ImageTotalSize]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png "Ilustración 2: tamaño total de los objetos que se puede alcanzar"  
[ImageRemoveSnapshots]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png "Ilustración 3: quitar instantáneas"  
[ImageSwitchViews]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png "Ilustración 4: selector cambiar vistas"  
[ImageSummaryView]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png "Ilustración 5: vista de Resumen"  
[ImageConstructorGroups]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png "Ilustración 6: grupos de constructores"  
[ImageComparisonView]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png "Ilustración 7: vista comparación"  
[ImageContainmentView]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png "Ilustración 8: vista de contención"  
<!--[ImageDomLeaks]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-domleaks.msft.png "old Figure 9: Name functions to distinguish between closures"  -->  
[ImageTreeGc]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Memory-problems-Tree-GC.msft.png "Ilustración 9: subárboles DOM"  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: /microsoft-edge/devtools-guide-chromium/memory-problems/memory-101#object-sizes "Tamaños de objetos: terminología de memoria"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: /microsoft-edge/devtools-guide-chromium/memory-problems/memory-101#objects-retaining-tree "Objetos que conservan la terminología de la memoria de árbol"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "Example-03. html-Microsoft Edge (cromo) DevTools | Intento"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "Example-06. html-Microsoft Edge (cromo) DevTools | Intento"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "Example-07. html-Microsoft Edge (cromo) DevTools | Intento"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "Example-08. html-Microsoft Edge (cromo) DevTools | Intento"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "Example-09. html-Microsoft Edge (cromo) DevTools | Intento"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "Example-10. html-Microsoft Edge (cromo) DevTools | Intento"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "memoria | Las"  

> [!NOTE]
> <span data-ttu-id="4e1af-285">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4e1af-285">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4e1af-286">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) y está creada por [Meggin Kearney][MegginKearney] \ (editor técnico \).</span><span class="sxs-lookup"><span data-stu-id="4e1af-286">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4e1af-288">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4e1af-288">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  

---
description: Use el panel memoria para
title: 'DevTools: memoria'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, memoria, montón, GC, recolección de elementos no utilizados, retenciones de tamaño, Dominators
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5ad284f8072cc296743299ec9c4fb2037f8fd883
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236004"
---
# <span data-ttu-id="55b56-104">Memoria</span><span class="sxs-lookup"><span data-stu-id="55b56-104">Memory</span></span>

<span data-ttu-id="55b56-105">Use el panel **memoria** para medir el uso de los recursos del sistema y Comparar instantáneas de montones en diferentes Estados de ejecución de código.</span><span class="sxs-lookup"><span data-stu-id="55b56-105">Use the **Memory** panel to measure your use of system resources and compare heap snapshots at different states of code execution.</span></span> <span data-ttu-id="55b56-106">Con ella, puedes hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="55b56-106">With it, you can:</span></span>

- <span data-ttu-id="55b56-107">[Representar el consumo de memoria de la página en tiempo real](#memory-usage-timeline) y tomar instantáneas del montón</span><span class="sxs-lookup"><span data-stu-id="55b56-107">[Graph the memory consumption of your page in real time](#memory-usage-timeline) and take snapshots of the heap</span></span>
- <span data-ttu-id="55b56-108">[Identificar problemas potenciales de memoria](#snapshot-summary) en el código, como objetos retenidos no adjuntos al Dom</span><span class="sxs-lookup"><span data-stu-id="55b56-108">[Identify potential memory issues](#snapshot-summary) in your code, such as retained objects not attached to the DOM</span></span>
- <span data-ttu-id="55b56-109">[Revisar los datos de uso de memoria](#snapshot-details) por tipo de objeto, recuento de instancias, tamaño y referencias para ayudar a aislar problemas</span><span class="sxs-lookup"><span data-stu-id="55b56-109">[Review memory usage data](#snapshot-details) by object type, instance count, size, and references to help isolate issues</span></span>
- <span data-ttu-id="55b56-110">[Aplicar filtros de datos de instantáneas](#filters) para reducir el ruido de información no accionable</span><span class="sxs-lookup"><span data-stu-id="55b56-110">[Apply snapshot data filters](#filters) to reduce the noise of non-actionable information</span></span>
- <span data-ttu-id="55b56-111">[Identificar el costo de memoria de un objeto específico](#object-references) y las referencias que lo mantienen activo</span><span class="sxs-lookup"><span data-stu-id="55b56-111">[Identify the memory cost of a specific object](#object-references) and the references keeping it alive</span></span>
- <span data-ttu-id="55b56-112">[Comparar el montón en diferentes fases de su investigación](#snapshot-comparison) para localizar el origen de las pérdidas de memoria y otros problemas</span><span class="sxs-lookup"><span data-stu-id="55b56-112">[Diff the heap at different phases of your investigation](#snapshot-comparison) to track down the source of memory leaks and other problems</span></span>

![Panel de memoria de Microsoft Edge DevTools](./media/memory.png)


## <span data-ttu-id="55b56-114">Barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="55b56-114">Toolbar</span></span>

1. <span data-ttu-id="55b56-115">**Iniciar o detener la sesión de generación de perfiles (Ctrl + E)**: activar el generador de perfiles le permite realizar un seguimiento del uso de memoria y tomar instantáneas del montón.</span><span class="sxs-lookup"><span data-stu-id="55b56-115">**Start/Stop profiling session (Ctrl+E)**: Turning on the profiler enables you to track memory usage and take snapshots of the heap.</span></span>
2. <span data-ttu-id="55b56-116">**Importar sesión de generación de perfiles (Ctrl + O)**: cargue una sesión de diagnóstico de memoria de DevTools guardada.</span><span class="sxs-lookup"><span data-stu-id="55b56-116">**Import profiling session (Ctrl+O)**: Load a saved  DevTools memory diagnostic session.</span></span>
3. <span data-ttu-id="55b56-117">**Exportar sesión de generación de perfiles (Ctrl + S)**: guardar la sesión de diagnóstico actual en el disco.</span><span class="sxs-lookup"><span data-stu-id="55b56-117">**Export profiling session (Ctrl+S)**: Save the current diagnostic session to disk.</span></span>
4. <span data-ttu-id="55b56-118">**Tomar instantánea de montón (Ctrl + Mayús + T)**: registrar asignaciones de memoria actuales para un punto de tiempo determinado.</span><span class="sxs-lookup"><span data-stu-id="55b56-118">**Take heap snapshot (Ctrl+Shift+T)**: Record current memory allocations for a given point of time.</span></span>


## <span data-ttu-id="55b56-119">Escala de tiempo de uso de memoria</span><span class="sxs-lookup"><span data-stu-id="55b56-119">Memory usage timeline</span></span>

<span data-ttu-id="55b56-120">Los problemas de memoria pueden ser una causa importante de problemas de rendimiento, lo que hace que la página deje de responder y sea más atrasada a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="55b56-120">Memory problems can be a major culprit of performance issues, causing your page to become increasingly unresponsive and laggy over time.</span></span>

<span data-ttu-id="55b56-121">El primer paso para analizar el uso de memoria de la página es [iniciar una sesión de generación de perfiles](#toolbar) con el fin de llevar instantáneas antes o después de que se reproduzcan los pasos que producen saturación de memoria o una pérdida de memoria sospechosa.</span><span class="sxs-lookup"><span data-stu-id="55b56-121">The first step to analyzing the memory usage of your page is to [start a profiling session](#toolbar) in order to take before/after snapshots of the heap as you repro the steps causing memory bloat or a suspected memory leak.</span></span>

<span data-ttu-id="55b56-122">Al iniciar el generador de perfiles de memoria, verá un gráfico de memoria de proceso que le permite observar el conjunto de trabajo privado global (la cantidad de memoria consumida por la página) a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="55b56-122">When you start the memory profiler, you will see a process memory graph that allows you to observe the overall private working set (the amount of memory consumed by the page) over time.</span></span> <span data-ttu-id="55b56-123">El gráfico de memoria muestra una vista en vivo de la memoria de proceso de la pestaña, que incluye bytes privados, memoria nativa y el montón de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="55b56-123">The memory graph shows you a live view of the tab's process memory, which includes private bytes, native memory, and the JavaScript heap.</span></span> 

![Escala de tiempo de uso de memoria](./media/memory_timeline.png)

 <span data-ttu-id="55b56-125">El gráfico le da una indicación de la tendencia de la memoria de la página que le permite juzgar Cuándo es adecuado [tomar una instantánea de montón](#toolbar) para compararla posteriormente, como cuando ve períodos de retención de memoria inesperada.</span><span class="sxs-lookup"><span data-stu-id="55b56-125">The graph gives you an indication of the memory trend for the page which enables you to judge when it is appropriate to [take a heap snapshot](#toolbar) for later comparison, such as when you see periods of unexpected memory retention.</span></span>

### <span data-ttu-id="55b56-126">Performance. Mark ()</span><span class="sxs-lookup"><span data-stu-id="55b56-126">Performance.mark()</span></span>

<span data-ttu-id="55b56-127">Puede agregar marcas de **usuario** personalizadas a la escala de tiempo para ayudar a identificar eventos clave durante el curso de su sesión de análisis mediante una llamada al [`Performance.mark()`](https://developer.mozilla.org/docs/Web/API/Performance/mark) método desde el código o la [**consola**](./console.md)de DevTools.</span><span class="sxs-lookup"><span data-stu-id="55b56-127">You can add custom **User marks** to the timeline to help identify  key events during the course of your analysis session by calling the [`Performance.mark()`](https://developer.mozilla.org/docs/Web/API/Performance/mark) method from within your code or the  DevTools [**Console**](./console.md).</span></span>

### <span data-ttu-id="55b56-128">Console. takeheapSnapshot ()</span><span class="sxs-lookup"><span data-stu-id="55b56-128">Console.takeheapSnapshot()</span></span>

<span data-ttu-id="55b56-129">En ocasiones, es necesario tomar instantáneas en momentos específicos, como inmediatamente antes de una gran mutación del DOM.</span><span class="sxs-lookup"><span data-stu-id="55b56-129">Sometimes you need to take snapshots at very specific points in time, such as immediately before a large mutation of the DOM.</span></span> <span data-ttu-id="55b56-130">En estos casos, puede tomar instantáneas mediante programación con [`Console.takeHeapSnapshot()`](./console/console-api.md#taking-heap-snapshots) .</span><span class="sxs-lookup"><span data-stu-id="55b56-130">In these cases,you can take snapshots programmatically with [`Console.takeHeapSnapshot()`](./console/console-api.md#taking-heap-snapshots).</span></span>

## <span data-ttu-id="55b56-131">Resumen de instantáneas</span><span class="sxs-lookup"><span data-stu-id="55b56-131">Snapshot summary</span></span>

<span data-ttu-id="55b56-132">[Tomar una instantánea](#toolbar) generará un icono de resumen que indica el tamaño del montón de JavaScript en el momento en que se realizó la instantánea, junto con el número de objetos asignados y una captura de pantalla de la página.</span><span class="sxs-lookup"><span data-stu-id="55b56-132">[Taking a snapshot](#toolbar) will generate a summary tile that indicates the size of the JavaScript heap at the time the snapshot was taken, along with the number of objects allocated and a screenshot of the page.</span></span> <span data-ttu-id="55b56-133">Puede seguir tomando instantáneas en cualquier momento mientras se ejecuta a través del escenario de usuario que requiere análisis.</span><span class="sxs-lookup"><span data-stu-id="55b56-133">You can continue to take snapshots at any time as you run through the user scenario requiring analysis.</span></span> <span data-ttu-id="55b56-134">Las instantáneas generan mosaicos adicionales, cada uno de los cuales indica la diferencia en la memoria JavaScript de la instantánea anterior.</span><span class="sxs-lookup"><span data-stu-id="55b56-134">The snapshots generate additional tiles, each of which indicates the difference in JavaScript memory from the previous snapshot.</span></span>

![Instantánea de montón](./media/memory_snapshot.png)

<span data-ttu-id="55b56-136">Al hacer clic en los valores del icono Resumen, se cambiará al panel con los [detalles de los datos de la instantánea](#snapshot-details).</span><span class="sxs-lookup"><span data-stu-id="55b56-136">Clicking on the values in the summary tile will switch to the pane showing [details of the snapshot data](#snapshot-details).</span></span> <span data-ttu-id="55b56-137">Los posibles [problemas de memoria se indican](#snapshot-details) con un icono de información azul ("i").</span><span class="sxs-lookup"><span data-stu-id="55b56-137">Potential [memory issues are indicated](#snapshot-details) with a blue informational ("i") icon.</span></span>

## <span data-ttu-id="55b56-138">Detalles de instantáneas</span><span class="sxs-lookup"><span data-stu-id="55b56-138">Snapshot details</span></span>

<span data-ttu-id="55b56-139">Los datos del panel *instantáneas* muestran los objetos creados por la página, junto con cualquier memoria asignada por Marcos de JavaScript que pueda estar consumiendo.</span><span class="sxs-lookup"><span data-stu-id="55b56-139">The data in the *Snapshot* pane shows the objects created by your page along with any memory allocated by JavaScript frameworks you may be consuming.</span></span>

![Tabla detalles de instantáneas](./media/memory_details.png)

<span data-ttu-id="55b56-141">Las tres pestañas representan distintas vistas de los datos:</span><span class="sxs-lookup"><span data-stu-id="55b56-141">The three tabs represent different views of the data:</span></span>

#### <span data-ttu-id="55b56-142">Tipos</span><span class="sxs-lookup"><span data-stu-id="55b56-142">Types</span></span>

<span data-ttu-id="55b56-143">Muestra el recuento de instancias y el tamaño total de los objetos del montón, agrupados por tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="55b56-143">Shows the instance count and total size of objects on the heap, grouped by object type.</span></span> <span data-ttu-id="55b56-144">De forma predeterminada, se ordenan por recuento de instancias.</span><span class="sxs-lookup"><span data-stu-id="55b56-144">By default, these are sorted by instance count.</span></span>

<span data-ttu-id="55b56-145">Al seleccionar un objeto en el panel *tipos* superiores, en la tabla [referencias de objetos](#object-references) del panel inferior se enumeran todos los objetos que apuntan a ese objeto.</span><span class="sxs-lookup"><span data-stu-id="55b56-145">When you select an object in the upper *Types* pane, the [Object references](#object-references) table in the lower pane will list all the objects that point to that object.</span></span>

#### <span data-ttu-id="55b56-146">Raíz</span><span class="sxs-lookup"><span data-stu-id="55b56-146">Roots</span></span>

<span data-ttu-id="55b56-147">Muestra una vista jerárquica de las referencias secundarias para describir cómo los objetos se arraigan en el objeto global, lo que impide su recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="55b56-147">Shows a hierarchical view of child references to describe how objects are rooted to the global object, thus preventing them from being garbage-collected.</span></span>

<span data-ttu-id="55b56-148">De forma predeterminada, los nodos secundarios se ordenan por la columna tamaño retenido, con el tamaño más alto en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="55b56-148">By default, the child nodes are sorted by the retained size column, with the largest at the top.</span></span>

#### <span data-ttu-id="55b56-149">Dominators</span><span class="sxs-lookup"><span data-stu-id="55b56-149">Dominators</span></span>

<span data-ttu-id="55b56-150">Muestra una lista de objetos en el montón que tienen referencias exclusivas a otros objetos.</span><span class="sxs-lookup"><span data-stu-id="55b56-150">Shows a list of objects on the heap that have exclusive references to other objects.</span></span> <span data-ttu-id="55b56-151">Dominators se ordenan por tamaño retenido para indicar que los objetos que consumen la mayor cantidad de memoria son potencialmente más fáciles de liberar.</span><span class="sxs-lookup"><span data-stu-id="55b56-151">Dominators are sorted by retained size to indicate the objects consuming the most memory that are potentially easiest to free.</span></span>

<span data-ttu-id="55b56-152">A continuación se explica cómo interpretar las columnas de los *tipos, las raíces* y las vistas de *Dominators* :</span><span class="sxs-lookup"><span data-stu-id="55b56-152">Here's how to interpret the columns in the *Types, Roots* and *Dominators* views:</span></span>

<span data-ttu-id="55b56-153">Columna</span><span class="sxs-lookup"><span data-stu-id="55b56-153">Column</span></span> | <span data-ttu-id="55b56-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="55b56-154">Description</span></span>
:------------ | :-------------
<span data-ttu-id="55b56-155">Identificador (s)</span><span class="sxs-lookup"><span data-stu-id="55b56-155">Identifier(s)</span></span> | <span data-ttu-id="55b56-156">Nombre que mejor identifica el objeto.</span><span class="sxs-lookup"><span data-stu-id="55b56-156">Name that best identifies the object.</span></span> <span data-ttu-id="55b56-157">Por ejemplo, para los elementos HTML, los detalles de la instantánea muestran el valor del atributo ID, si se usa alguno.</span><span class="sxs-lookup"><span data-stu-id="55b56-157">For example, for HTML elements the snapshot details show the ID attribute value, if one is used.</span></span>
<span data-ttu-id="55b56-158">Tipo</span><span class="sxs-lookup"><span data-stu-id="55b56-158">Type</span></span> | <span data-ttu-id="55b56-159">Tipo de objeto (por ejemplo, *HTMLDivElement*).</span><span class="sxs-lookup"><span data-stu-id="55b56-159">Object type (for example, *HTMLDivElement*).</span></span>
<span data-ttu-id="55b56-160">Tamaño</span><span class="sxs-lookup"><span data-stu-id="55b56-160">Size</span></span> | <span data-ttu-id="55b56-161">Tamaño del objeto, sin incluir el tamaño de los objetos a los que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="55b56-161">Object size, not including the size of any referenced objects.</span></span>
<span data-ttu-id="55b56-162">Tamaño retenido</span><span class="sxs-lookup"><span data-stu-id="55b56-162">Retained size</span></span> | <span data-ttu-id="55b56-163">Tamaño de objeto más el tamaño de todos los objetos secundarios que no tienen otros elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="55b56-163">Object size plus the size of all child objects that have no other parents.</span></span> <span data-ttu-id="55b56-164">Por motivos prácticos, esta es la cantidad de memoria que retiene el objeto, por lo que si elimina el objeto, se reclama la cantidad de memoria especificada.</span><span class="sxs-lookup"><span data-stu-id="55b56-164">For practical purposes, this is the amount of memory retained by the object, so if you delete the object you reclaim the specified amount of memory.</span></span>
<span data-ttu-id="55b56-165">Número</span><span class="sxs-lookup"><span data-stu-id="55b56-165">Count</span></span> | <span data-ttu-id="55b56-166">Número de instancias de objetos.</span><span class="sxs-lookup"><span data-stu-id="55b56-166">Number of object instances.</span></span> <span data-ttu-id="55b56-167">Este valor solo aparece en la vista tipos.</span><span class="sxs-lookup"><span data-stu-id="55b56-167">This value appears only in the Types view.</span></span>

<span data-ttu-id="55b56-168">Al seleccionar un objeto en el panel superior de *Dominators* , en la tabla [referencias de objetos](#object-references) del panel inferior se enumeran todos los objetos que apuntan a ese objeto.</span><span class="sxs-lookup"><span data-stu-id="55b56-168">When you select an object in the upper *Dominators* pane, the [Object references](#object-references) table in the lower pane will list all the objects that point to that object.</span></span>

### <span data-ttu-id="55b56-169">Filtros</span><span class="sxs-lookup"><span data-stu-id="55b56-169">Filters</span></span>

<span data-ttu-id="55b56-170">Puede ajustar aún más los datos de la tabla con lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="55b56-170">You can further adjust data in the table with the following:</span></span>

![Filtrar por integradas e identificadores de objetos](./media/memory_filter.png)

1. <span data-ttu-id="55b56-172">**Filtro de identificador**: filtrar datos buscando un identificador de objeto concreto</span><span class="sxs-lookup"><span data-stu-id="55b56-172">**Identifier filter**: Filter out data by searching for a particular object identifier</span></span>
2. <span data-ttu-id="55b56-173">**Agrupar por Dominator**: solo se muestran los objetos con referencias *exclusivas* a otros objetos en la vista de nivel superior de los objetos (esta es la vista predeterminada de la pestaña *Dominators* ).</span><span class="sxs-lookup"><span data-stu-id="55b56-173">**Group by dominator**: Only objects with *exclusive* references to other objects are shown in the top-level view of objects (this is the default view in the *Dominators* tab).</span></span>
3. <span data-ttu-id="55b56-174">**Filtro de incorporaciones/IDS**: de forma predeterminada, los [objetos integrados de JavaScript](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects) se incluyen en la lista.</span><span class="sxs-lookup"><span data-stu-id="55b56-174">**Built-ins / IDs filter**: By default, [JavaScript built-in objects](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects) are included in the list.</span></span> <span data-ttu-id="55b56-175">La lista de identificadores de objetos puede ser útil si hay varios objetos anónimos que deben diferenciarse.</span><span class="sxs-lookup"><span data-stu-id="55b56-175">Listing object IDs can be useful if there are multiple anonymous objects which need to be differentiated.</span></span>

<span data-ttu-id="55b56-176">Los *tipos, las raíces* y las vistas de *Dominators* tienen su propio filtro, por lo que el filtro no se conserva al cambiar a otra vista.</span><span class="sxs-lookup"><span data-stu-id="55b56-176">The *Types, Roots* and *Dominators* views each has its own filter, so the filter isn't preserved when you switch to another view.</span></span>

### <span data-ttu-id="55b56-177">Referencias a objetos</span><span class="sxs-lookup"><span data-stu-id="55b56-177">Object references</span></span>

<span data-ttu-id="55b56-178">En las vistas [**tipos**](#types) y [**Dominators**](#dominators) , el panel inferior contiene una lista de **referencias de objeto** que muestra las referencias compartidas.</span><span class="sxs-lookup"><span data-stu-id="55b56-178">In the [**Types**](#types) and [**Dominators**](#dominators) views, the lower pane contains an **Object references** list that displays shared references.</span></span> <span data-ttu-id="55b56-179">Al elegir un objeto en el panel superior, esta lista muestra todos los objetos que apuntan a ese objeto, en otras palabras, los objetos que mantienen activos el objeto seleccionado.</span><span class="sxs-lookup"><span data-stu-id="55b56-179">When you choose an object in the upper pane, this list displays all objects that point to that object--in other words, the objects that are keeping the selected object alive.</span></span>

<span data-ttu-id="55b56-180">Las referencias circulares se muestran con un asterisco (\*) y la información sobre herramientas informativa, y no se pueden expandir.</span><span class="sxs-lookup"><span data-stu-id="55b56-180">Circular references are shown with an asterisk (\*) and informational tooltip, and cannot be expanded.</span></span> <span data-ttu-id="55b56-181">De lo contrario, impediría subir el árbol de referencia e identificar los objetos que están conservando la memoria.</span><span class="sxs-lookup"><span data-stu-id="55b56-181">Otherwise, they would prevent you from walking up the reference tree and identifying objects that are retaining memory.</span></span>

<span data-ttu-id="55b56-182">Para identificar rápidamente los objetos equivalentes, marque la opción de filtro [*Mostrar identificadores de objeto*](#filters) para mostrar los identificadores de objeto junto a los nombres de objeto en la columna *identificador (s)* .</span><span class="sxs-lookup"><span data-stu-id="55b56-182">To quickly identify equivalent objects, tick the [*Display object IDs*](#filters) filter option to display object IDs next to object names in the *Identifier(s)* column.</span></span> <span data-ttu-id="55b56-183">Los objetos que tienen el mismo identificador son referencias compartidas.</span><span class="sxs-lookup"><span data-stu-id="55b56-183">Objects that have the same ID are shared references.</span></span>

### <span data-ttu-id="55b56-184">Comparación de instantáneas</span><span class="sxs-lookup"><span data-stu-id="55b56-184">Snapshot comparison</span></span>

<span data-ttu-id="55b56-185">Al hacer clic en una [ficha comparación de instantáneas](#snapshot-details) o en un vínculo de comparación en el [mosaico Resumen de instantánea](#snapshot-summary)  , aparecerá una diferencia de información entre las dos instantáneas.</span><span class="sxs-lookup"><span data-stu-id="55b56-185">Clicking on a [snapshot comparison tab](#snapshot-details) or comparison link on the [snapshot summary tile](#snapshot-summary)  will show a diff of information between the two snapshots.</span></span> <span data-ttu-id="55b56-186">En el panel comparación, las vistas *Dominators, tipos* y *raíces* proporcionan los mismos [*detalles de instantánea*](#snapshot-details) que se verían para una única instantánea, con estos valores adicionales:</span><span class="sxs-lookup"><span data-stu-id="55b56-186">In the comparison pane, the *Dominators, Types* and *Roots* views provide the same [*snapshot details*](#snapshot-details) you would see for a single snapshots, with these additional values:</span></span>

<span data-ttu-id="55b56-187">Columna</span><span class="sxs-lookup"><span data-stu-id="55b56-187">Column</span></span> | <span data-ttu-id="55b56-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="55b56-188">Description</span></span>
:------------ | :-------------
<span data-ttu-id="55b56-189">Diferencia de tamaño.</span><span class="sxs-lookup"><span data-stu-id="55b56-189">Size diff.</span></span> | <span data-ttu-id="55b56-190">Diferencia entre el tamaño del objeto en la instantánea actual y su tamaño en la instantánea anterior, sin incluir el tamaño de los objetos a los que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="55b56-190">Difference between the size of the object in the current snapshot and its size in the previous snapshot, not including the size of any referenced objects.</span></span>
<span data-ttu-id="55b56-191">Diferencias de tamaño retenida.</span><span class="sxs-lookup"><span data-stu-id="55b56-191">Retained size diff.</span></span> | <span data-ttu-id="55b56-192">Diferencia entre el tamaño conservado del objeto en la instantánea actual y su tamaño retenido en la instantánea anterior.</span><span class="sxs-lookup"><span data-stu-id="55b56-192">Difference between the retained size of the object in the current snapshot and its retained size in the previous snapshot.</span></span> <span data-ttu-id="55b56-193">El tamaño retenido incluye el tamaño del objeto, además del tamaño de todos sus objetos secundarios, que no tienen otros elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="55b56-193">The retained size includes the object size plus the size of all its child objects that have no other parents.</span></span> <span data-ttu-id="55b56-194">Por motivos prácticos, el tamaño retenido es la cantidad de memoria retenida por el objeto, por lo que si elimina el objeto, se reclama la cantidad de memoria especificada.</span><span class="sxs-lookup"><span data-stu-id="55b56-194">For practical purposes, the retained size is the amount of memory retained by the object, so if you delete the object you reclaim the specified amount of memory.</span></span>

<span data-ttu-id="55b56-195">Puede usar la lista desplegable **ámbito** para filtrar la información diferencial entre instantáneas:</span><span class="sxs-lookup"><span data-stu-id="55b56-195">You can use the **Scope** dropdown to filter differential info between snapshots:</span></span>

![Filtro de ámbito de las comparaciones de instantáneas](./media/memory_comparison_scope_filter.png)

- <strong><span data-ttu-id="55b56-197">Objetos que quedan de la instantánea # <number></strong> : muestra las diferencias entre los objetos agregados al montón y que se han quitado del montón de la instantánea de línea base a la instantánea anterior.</span><span class="sxs-lookup"><span data-stu-id="55b56-197">Objects left over from Snapshot #<number></strong>: Shows the diff between the objects added to the heap and removed from the heap from the baseline snapshot to the previous snapshot.</span></span> <span data-ttu-id="55b56-198">Por ejemplo, si el Resumen de instantánea muestra <em> + 205/-195 </em> en el recuento de objetos, este filtro mostrará los diez objetos que se han agregado pero no se han quitado.</span><span class="sxs-lookup"><span data-stu-id="55b56-198">For example, if the snapshot summary shows <em>+205 / -195</em> in the object count, this filter will show you the ten objects that were added but not removed.</span></span>

- <strong><span data-ttu-id="55b56-199">Los objetos agregados entre la instantánea # <number> y # <number></strong> : muestran todos los objetos agregados al montón desde la instantánea anterior.</span><span class="sxs-lookup"><span data-stu-id="55b56-199">Objects added between Snapshot #<number> and #<number></strong>: Shows all objects added to the heap from the previous snapshot.</span></span>

- <strong><span data-ttu-id="55b56-200">Todos los objetos de la instantánea # <number></strong> : muestra todos los objetos del montón (en otras palabras, una <em> vista sin filtrar </em> ).</span><span class="sxs-lookup"><span data-stu-id="55b56-200">All objects in Snapshot #<number></strong>: Shows all objects on the heap (in other words, an <em>unfiltered</em> view).</span></span>

<span data-ttu-id="55b56-201">De forma predeterminada, el filtro *Mostrar referencias no coincidentes* se aplica a la vista comparación para indicar referencias de objeto que no coinciden con el filtro de ámbito actual.</span><span class="sxs-lookup"><span data-stu-id="55b56-201">By default, the *Show non-matching references* filter is applied to the comparison view to indicate object references that don't match the current Scope filter.</span></span> <span data-ttu-id="55b56-202">Puede desactivarla en el menú desplegable:</span><span class="sxs-lookup"><span data-stu-id="55b56-202">You can turn it off from the dropdown menu:</span></span>

![Filtro de referencias no coincidentes para comparaciones de instantáneas](./media/memory_comparison_matching_filter.png)


## <span data-ttu-id="55b56-204">Accesos directos</span><span class="sxs-lookup"><span data-stu-id="55b56-204">Shortcuts</span></span>

 <span data-ttu-id="55b56-205">Acción</span><span class="sxs-lookup"><span data-stu-id="55b56-205">Action</span></span> | <span data-ttu-id="55b56-206">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="55b56-206">Shortcut</span></span>
:------------ | :-------------
<span data-ttu-id="55b56-207">Iniciar o detener sesión de generación de perfiles</span><span class="sxs-lookup"><span data-stu-id="55b56-207">Start / Stop profiling session</span></span>  | `Ctrl` + `E`
<span data-ttu-id="55b56-208">Importar sesión de generación de perfiles</span><span class="sxs-lookup"><span data-stu-id="55b56-208">Import profiling session</span></span> | `Ctrl` + `O`
<span data-ttu-id="55b56-209">Exportar sesión de generación de perfiles</span><span class="sxs-lookup"><span data-stu-id="55b56-209">Export profiling session</span></span> | `Ctrl` + `S`
<span data-ttu-id="55b56-210">Tomar instantánea de montón</span><span class="sxs-lookup"><span data-stu-id="55b56-210">Take heap snapshot</span></span> | `Ctrl` + `Shift` + `T`

## <span data-ttu-id="55b56-211">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="55b56-211">Known Issues</span></span>

### <span data-ttu-id="55b56-212">Se produjo un error al iniciar la sesión de generación de perfiles</span><span class="sxs-lookup"><span data-stu-id="55b56-212">An error occurred while starting the profiling session</span></span>

<span data-ttu-id="55b56-213">Si ve este mensaje de error: **se ha producido un error al iniciar la sesión de generación de perfiles** en la herramienta memoria, siga estos pasos para obtener una solución alternativa.</span><span class="sxs-lookup"><span data-stu-id="55b56-213">If you see this error message: **An error occurred while starting the profiling session** in the Memory tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="55b56-214">Presione `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="55b56-214">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="55b56-215">En el cuadro de diálogo Ejecutar, escriba **Services. msc**.</span><span class="sxs-lookup"><span data-stu-id="55b56-215">In the Run dialog, enter **services.msc**.</span></span>
![problemas conocidos-1](./media/known_issues_1.PNG)

3. <span data-ttu-id="55b56-217">Busque el **servicio Recopilador estándar de Microsoft (R) Diagnostics Hub** y haga clic en él con el botón secundario del ratón.</span><span class="sxs-lookup"><span data-stu-id="55b56-217">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![problemas conocidos-2](./media/known_issues_2.PNG)

4. <span data-ttu-id="55b56-219">Reinicie el **servicio Recopilador estándar del concentrador de diagnósticos de Microsoft (R)**.</span><span class="sxs-lookup"><span data-stu-id="55b56-219">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![problemas conocidos-3](./media/known_issues_3.PNG)

5. <span data-ttu-id="55b56-221">Cierre las herramientas para desarrolladores de Microsoft Edge y la pestaña. Abra una nueva pestaña, vaya a la página y presione `F12` .</span><span class="sxs-lookup"><span data-stu-id="55b56-221">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="55b56-222">Ahora debería poder comenzar a crear perfiles.</span><span class="sxs-lookup"><span data-stu-id="55b56-222">You should now be able to begin profiling.</span></span> 
![problemas conocidos-4](./media/known_issues_4-memory.PNG)

<span data-ttu-id="55b56-224">¿Aún tiene problemas?</span><span class="sxs-lookup"><span data-stu-id="55b56-224">Still running into problems?</span></span> <span data-ttu-id="55b56-225">Envíenos sus comentarios con el icono para **Enviar comentarios** .</span><span class="sxs-lookup"><span data-stu-id="55b56-225">Please send us your feedback using the **Send feedback** icon!</span></span> 

![problemas conocidos-5](./media/known_issues_5.PNG)

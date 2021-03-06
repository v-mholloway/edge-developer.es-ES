---
description: En esta sección se describen los términos comunes usados en el análisis de memoria y se aplica a una variedad de herramientas de generación de perfiles de memoria para diferentes idiomas.
title: Terminología de memoria
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 1579374be29f0f419ded3bf88f5dea284f0bbb1a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397793"
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

# <a name="memory-terminology"></a><span data-ttu-id="18d08-104">Terminología de memoria</span><span class="sxs-lookup"><span data-stu-id="18d08-104">Memory terminology</span></span>  

<span data-ttu-id="18d08-105">En este artículo se describen los términos comunes usados en el análisis de memoria y se aplica a varias herramientas de generación de perfiles de memoria para diferentes idiomas.</span><span class="sxs-lookup"><span data-stu-id="18d08-105">This article describes common terms used in memory analysis, and is applicable to various memory profiling tools for different languages.</span></span>  

<span data-ttu-id="18d08-106">Los términos y nociones que se describen aquí hacen referencia al [panel Memoria][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="18d08-106">The terms and notions described here refer to the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="18d08-107">Si alguna vez ha trabajado con el Java, .NET o algún otro perfilador de memoria, este artículo puede ser un actualizador.</span><span class="sxs-lookup"><span data-stu-id="18d08-107">If you have ever worked with either the Java, .NET, or some other memory profiler, then this article may be a refresher.</span></span>  

## <a name="object-sizes"></a><span data-ttu-id="18d08-108">Tamaños de objeto</span><span class="sxs-lookup"><span data-stu-id="18d08-108">Object sizes</span></span>  

<span data-ttu-id="18d08-109">Piense en la memoria como un gráfico con tipos primitivos \(como números y cadenas\) y objetos \(matrices asociativas\).</span><span class="sxs-lookup"><span data-stu-id="18d08-109">Think of memory as a graph with primitive types \(like numbers and strings\) and objects \(associative arrays\).</span></span>  <span data-ttu-id="18d08-110">Puede mostrarse como un gráfico con muchos puntos interconectados, como la siguiente figura.</span><span class="sxs-lookup"><span data-stu-id="18d08-110">It may display as a graph with many interconnected points such as following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Representación visual de la memoria" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   <span data-ttu-id="18d08-112">Representación visual de la memoria</span><span class="sxs-lookup"><span data-stu-id="18d08-112">Visual representation of memory</span></span>  
:::image-end:::  

<span data-ttu-id="18d08-113">Un objeto puede contener memoria de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="18d08-113">An object may hold memory in two ways:</span></span>  

*   <span data-ttu-id="18d08-114">Directamente por el objeto.</span><span class="sxs-lookup"><span data-stu-id="18d08-114">Directly by the object.</span></span>  
*   <span data-ttu-id="18d08-115">Implícitamente manteniendo referencias a otros objetos y, por lo tanto, evitando que un recolector de elementos no utilizados desechar automáticamente esos objetos.</span><span class="sxs-lookup"><span data-stu-id="18d08-115">Implicitly by holding references to other objects, and therefore preventing those objects from being automatically disposed by a garbage collector.</span></span>  

<span data-ttu-id="18d08-116">Al trabajar con el [panel][DevtoolsMemoryProblemsHeapSnapshots] Memoria en DevTools \(una herramienta para investigar problemas de memoria encontrados en **Memoria**\), puede encontrarse mirando algunas columnas diferentes de información.</span><span class="sxs-lookup"><span data-stu-id="18d08-116">When working with the [Memory][DevtoolsMemoryProblemsHeapSnapshots] panel in DevTools \(a tool for investigating memory issues found under **Memory**\), you may find yourself looking at a few different columns of information.</span></span>  <span data-ttu-id="18d08-117">Dos que destacan son **Shallow Size y** **Retained Size,** pero ¿qué representan estos?</span><span class="sxs-lookup"><span data-stu-id="18d08-117">Two that stand out are **Shallow Size** and **Retained Size**, but what do these represent?</span></span>  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Tamaño superficial y retenido" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   <span data-ttu-id="18d08-119">Tamaño superficial y retenido</span><span class="sxs-lookup"><span data-stu-id="18d08-119">Shallow and Retained Size</span></span>  
:::image-end:::  

### <a name="shallow-size"></a><span data-ttu-id="18d08-120">Tamaño superficial</span><span class="sxs-lookup"><span data-stu-id="18d08-120">Shallow size</span></span>  

<span data-ttu-id="18d08-121">Este es el tamaño de la memoria que contiene el objeto.</span><span class="sxs-lookup"><span data-stu-id="18d08-121">This is the size of memory that is held by the object.</span></span>  

<span data-ttu-id="18d08-122">Los objetos JavaScript típicos tienen algo de memoria reservada para su descripción y para almacenar valores inmediatos.</span><span class="sxs-lookup"><span data-stu-id="18d08-122">Typical JavaScript objects have some memory reserved for their description and for storing immediate values.</span></span>  <span data-ttu-id="18d08-123">Normalmente, solo las matrices y las cadenas pueden tener un tamaño superficial significativo.</span><span class="sxs-lookup"><span data-stu-id="18d08-123">Usually, only arrays and strings are able to have a significant shallow size.</span></span>  <span data-ttu-id="18d08-124">Sin embargo, las cadenas y matrices externas a menudo tienen su almacenamiento principal en la memoria del representador, lo que expone solo un pequeño objeto contenedor en el montón de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="18d08-124">However, strings and external arrays often have their main storage in renderer memory, exposing only a small wrapper object on the JavaScript heap.</span></span>  

<span data-ttu-id="18d08-125">La memoria del representador es toda la memoria del proceso en el que se representa una página inspeccionada: memoria nativa + memoria de montón JS de la página + memoria de montón JS de todos los trabajadores dedicados iniciados por la página.</span><span class="sxs-lookup"><span data-stu-id="18d08-125">Renderer memory is all memory of the process where an inspected page is rendered: native memory + JS heap memory of the page + JS heap memory of all dedicated workers started by the page.</span></span>  <span data-ttu-id="18d08-126">Sin embargo, incluso un objeto pequeño puede contener una gran cantidad de memoria indirectamente, al impedir que el proceso de recolección automática de elementos no utilizados desechar otros objetos.</span><span class="sxs-lookup"><span data-stu-id="18d08-126">Nevertheless, even a small object is able to hold a large amount of memory indirectly, by preventing other objects from being disposed of by the automatic garbage collection process.</span></span>  

### <a name="retained-size"></a><span data-ttu-id="18d08-127">Tamaño retenido</span><span class="sxs-lookup"><span data-stu-id="18d08-127">Retained size</span></span>  

<span data-ttu-id="18d08-128">Este es el tamaño de la memoria que se libera una vez que el objeto se elimina junto con los objetos dependientes que se han hecho inaccesibles desde las raíces del recolector **de elementos no utilizados.**</span><span class="sxs-lookup"><span data-stu-id="18d08-128">This is the size of memory that is freed once the object is deleted along with the dependent objects that were made unreachable from **Garbage Collector roots**.</span></span>  

<span data-ttu-id="18d08-129">**Las** raíces del recolector de elementos no utilizados están hechas de controladores que se crean \(local o global\) al hacer una referencia desde código nativo a un objeto JavaScript fuera de V8. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="18d08-129">**Garbage Collector roots** are made up of **handles** that are created \(either local or global\) when making a reference from native code to a JavaScript object outside of V8.</span></span>  <span data-ttu-id="18d08-130">Todos estos controladores pueden encontrarse en una instantánea de montón en el ámbito de control de raíces **de GC**y en las raíces  >  \*\*\*\* de **GC**  >  **Controladores globales.**</span><span class="sxs-lookup"><span data-stu-id="18d08-130">All such handles may be found within a heap snapshot under **GC roots** > **Handle scope** and **GC roots** > **Global handles**.</span></span>  <span data-ttu-id="18d08-131">Describir los controladores de esta documentación sin entrar en detalles de la implementación del explorador puede resultar confuso.</span><span class="sxs-lookup"><span data-stu-id="18d08-131">Describing the handles in this documentation without diving into details of the browser implementation may be confusing.</span></span>  <span data-ttu-id="18d08-132">Tanto las raíces del recolector de elementos no utilizados como los controladores no son algo de lo que tenga que preocuparse.</span><span class="sxs-lookup"><span data-stu-id="18d08-132">Both Garbage Collector roots and the handles are not something you need to worry about.</span></span>  

<span data-ttu-id="18d08-133">Hay muchas raíces internas del recolector de elementos no utilizados, la mayoría de las cuales no son interesantes para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="18d08-133">There are lots of internal Garbage Collector roots, most of which are not interesting for the users.</span></span>  <span data-ttu-id="18d08-134">Desde el punto de vista de las aplicaciones, hay siguientes tipos de raíces.</span><span class="sxs-lookup"><span data-stu-id="18d08-134">From the applications standpoint there are following kinds of roots.</span></span>  

*   <span data-ttu-id="18d08-135">Objeto global window \(en cada iframe\).</span><span class="sxs-lookup"><span data-stu-id="18d08-135">Window global object \(in each iframe\).</span></span>  <span data-ttu-id="18d08-136">Hay un campo de distancia en las instantáneas de montón, que es el número de referencias a propiedades en la ruta de retención más corta de la ventana.</span><span class="sxs-lookup"><span data-stu-id="18d08-136">There is a distance field in the heap snapshots which is the number of property references on the shortest retaining path from the window.</span></span>  
*   <span data-ttu-id="18d08-137">Árbol DOM de documento que consta de todos los nodos DOM nativos a los que se puede acceder recorriendo el documento.</span><span class="sxs-lookup"><span data-stu-id="18d08-137">Document DOM tree consisting of all native DOM nodes reachable by traversing the document.</span></span>  <span data-ttu-id="18d08-138">No todos los nodos pueden tener contenedores JS, pero si un nodo tiene un contenedor, está activo mientras el documento está activo.</span><span class="sxs-lookup"><span data-stu-id="18d08-138">Not all of the nodes may have JS wrappers but if a node has a wrapper, it is alive while the document is alive.</span></span>  
*   <span data-ttu-id="18d08-139">A veces, el contexto del depurador puede retener objetos en el panel **Orígenes** y la consola **\(por** ejemplo, después de la evaluación de la consola\).</span><span class="sxs-lookup"><span data-stu-id="18d08-139">Sometimes objects may be retained by the debugger context in the **Sources** panel and the **Console** \(for example after Console evaluation\).</span></span>  <span data-ttu-id="18d08-140">Cree instantáneas de montón con un panel **de** consola desactivado y sin puntos de interrupción activos en el depurador en **el** panel Orígenes.</span><span class="sxs-lookup"><span data-stu-id="18d08-140">Create heap snapshots with a cleared **Console** panel and no active breakpoints in the debugger in the **Sources** panel.</span></span>

>[!TIP]
> <span data-ttu-id="18d08-141">Desactive el panel **Consola** ejecutando y desactivando puntos de interrupción en el panel Orígenes antes de tomar una instantánea `clear()` de montón en el panel [Memoria][DevtoolsMemoryProblemsHeapSnapshots]. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="18d08-141">Clear the **Console** panel by running `clear()` and deactivate breakpoints in the **Sources** panel before taking a heap snapshot in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>

<span data-ttu-id="18d08-142">El gráfico de memoria comienza con una raíz, que puede ser el objeto del explorador o el `window` objeto de un Node.js `Global` módulo.</span><span class="sxs-lookup"><span data-stu-id="18d08-142">The memory graph starts with a root, which may be the `window` object of the browser or the `Global` object of a Node.js module.</span></span>  <span data-ttu-id="18d08-143">No se controla cómo se recopila este objeto raíz.</span><span class="sxs-lookup"><span data-stu-id="18d08-143">You do not control how this root object is garbage collected.</span></span>  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="No puede controlar cómo se recopila el objeto raíz." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   <span data-ttu-id="18d08-145">No puede controlar cómo se recopila el objeto raíz.</span><span class="sxs-lookup"><span data-stu-id="18d08-145">You are not able to control how the root object is garbage collected.</span></span>  
:::image-end:::  

<span data-ttu-id="18d08-146">Todo lo que no se puede obtener desde la raíz obtiene la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="18d08-146">Whatever is not reachable from the root gets garbage collected.</span></span>  

> [!NOTE]
> <span data-ttu-id="18d08-147">Las columnas [Tamaño superficial y](#shallow-size) Tamaño [retenido](#retained-size) representan datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="18d08-147">Both the [Shallow size](#shallow-size) and [Retained size](#retained-size) columns represent data in bytes.</span></span>  

## <a name="objects-retaining-tree"></a><span data-ttu-id="18d08-148">Árbol de retención de objetos</span><span class="sxs-lookup"><span data-stu-id="18d08-148">Objects retaining tree</span></span>  

<span data-ttu-id="18d08-149">El montón es una red de objetos interconectados.</span><span class="sxs-lookup"><span data-stu-id="18d08-149">The heap is a network of interconnected objects.</span></span>  <span data-ttu-id="18d08-150">En el mundo matemático, esta estructura se denomina gráfico **o** gráfico de memoria.</span><span class="sxs-lookup"><span data-stu-id="18d08-150">In the mathematical world, this structure is called a **graph** or memory graph.</span></span>  <span data-ttu-id="18d08-151">Un gráfico se construye a partir de **nodos conectados** mediante **bordes,** a los que se les dan etiquetas.</span><span class="sxs-lookup"><span data-stu-id="18d08-151">A graph is constructed from **nodes** connected by means of **edges**, both of which are given labels.</span></span>  

*   <span data-ttu-id="18d08-152">**Los** nodos \(u **objetos**\) se etiquetan con el nombre de la **función de constructor** que se usó para crearlos.</span><span class="sxs-lookup"><span data-stu-id="18d08-152">**Nodes** \(or **objects**\) are labelled using the name of the **constructor** function that was used to build them.</span></span>  
*   <span data-ttu-id="18d08-153">**Los** bordes se etiquetan con los nombres de **las propiedades**.</span><span class="sxs-lookup"><span data-stu-id="18d08-153">**Edges** are labelled using the names of **properties**.</span></span>  

<span data-ttu-id="18d08-154">Obtenga [información sobre cómo grabar un perfil mediante el Profiler de montón][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="18d08-154">Learn [how to record a profile using the Heap Profiler][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="18d08-155">En la siguiente figura, algunos de los aspectos [][DevtoolsMemoryProblemsHeapSnapshots] notables de la grabación de instantáneas de montón en la herramienta Memoria incluyen distancia: la distancia desde la raíz del recolector de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="18d08-155">In the following figure, some of the notable things in the Heap Snapshot recording in the [Memory][DevtoolsMemoryProblemsHeapSnapshots] tool include distance:  the distance from the Garbage Collector root.</span></span>  <span data-ttu-id="18d08-156">Si casi todos los objetos del mismo tipo están a la misma distancia y algunos están a una distancia mayor, eso es algo que vale la pena investigar.</span><span class="sxs-lookup"><span data-stu-id="18d08-156">If almost all the objects of the same type are at the same distance, and a few are at a bigger distance, that is something worth investigating.</span></span>  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Distancia desde la raíz" lightbox="../media/memory-problems-root.msft.png":::
   <span data-ttu-id="18d08-158">Distancia desde la raíz</span><span class="sxs-lookup"><span data-stu-id="18d08-158">Distance from root</span></span>  
:::image-end:::  

## <a name="dominators"></a><span data-ttu-id="18d08-159">Dominadores</span><span class="sxs-lookup"><span data-stu-id="18d08-159">Dominators</span></span>  

<span data-ttu-id="18d08-160">Los objetos dominantes se componen de una estructura de árbol porque cada objeto tiene exactamente un dominante.</span><span class="sxs-lookup"><span data-stu-id="18d08-160">Dominator objects are comprised of a tree structure because each object has exactly one dominator.</span></span>  <span data-ttu-id="18d08-161">Un dominante de un objeto puede carecer de referencias directas a un objeto que domina; es decir, el árbol del dominante no es un árbol de expansión del gráfico.</span><span class="sxs-lookup"><span data-stu-id="18d08-161">A dominator of an object may lack direct references to an object it dominates; that is, the tree of the dominator is not a spanning tree of the graph.</span></span>  

<span data-ttu-id="18d08-162">En la siguiente figura, se cumple la siguiente instrucción.</span><span class="sxs-lookup"><span data-stu-id="18d08-162">In the following figure, the following statement are true.</span></span>  

*   <span data-ttu-id="18d08-163">El nodo 1 domina el nodo 2</span><span class="sxs-lookup"><span data-stu-id="18d08-163">Node 1 dominates node 2</span></span>  
*   <span data-ttu-id="18d08-164">El nodo 2 domina los nodos 3, 4 y 6</span><span class="sxs-lookup"><span data-stu-id="18d08-164">Node 2 dominates nodes 3, 4 and 6</span></span>  
*   <span data-ttu-id="18d08-165">El nodo 3 domina el nodo 5</span><span class="sxs-lookup"><span data-stu-id="18d08-165">Node 3 dominates node 5</span></span>  
*   <span data-ttu-id="18d08-166">El nodo 5 domina el nodo 8</span><span class="sxs-lookup"><span data-stu-id="18d08-166">Node 5 dominates node 8</span></span>  
*   <span data-ttu-id="18d08-167">El nodo 6 domina el nodo 7</span><span class="sxs-lookup"><span data-stu-id="18d08-167">Node 6 dominates node 7</span></span>  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Estructura de árbol de dominio" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   <span data-ttu-id="18d08-169">Estructura de árbol de dominio</span><span class="sxs-lookup"><span data-stu-id="18d08-169">Dominator tree structure</span></span>  
:::image-end:::  

<span data-ttu-id="18d08-170">En la siguiente figura, node es el dominante de , pero también existe en todas las rutas `#3` `#10` `#7` sencillas de recolector de elementos no utilizados a `#10` .</span><span class="sxs-lookup"><span data-stu-id="18d08-170">In the following figure, node `#3` is the dominator of `#10`, but `#7` also exists in every simple path from Garbage Collector to `#10`.</span></span>  <span data-ttu-id="18d08-171">Por lo tanto, un objeto B es un dominante de un objeto A si B existe en todas las rutas de acceso sencillas desde la raíz al objeto A.</span><span class="sxs-lookup"><span data-stu-id="18d08-171">Therefore, an object B is a dominator of an object A if B exists in every simple path from the root to the object A.</span></span>  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Ilustración de un domador animado" lightbox="../media/memory-problems-dominators.msft.gif":::
   <span data-ttu-id="18d08-173">Ilustración de un domador animado</span><span class="sxs-lookup"><span data-stu-id="18d08-173">Animated dominator illustration</span></span>  
:::image-end:::  

## <a name="v8-specifics"></a><span data-ttu-id="18d08-174">Detalles de V8</span><span class="sxs-lookup"><span data-stu-id="18d08-174">V8 specifics</span></span>  

<span data-ttu-id="18d08-175">Al generar perfiles de memoria, resulta útil comprender por qué las instantáneas de montón tienen un aspecto determinado.</span><span class="sxs-lookup"><span data-stu-id="18d08-175">When profiling memory, it is helpful to understand why heap snapshots look a certain way.</span></span>  <span data-ttu-id="18d08-176">En esta sección se describen algunos temas relacionados con la memoria que corresponden específicamente a la máquina **virtual V8 JavaScript** \(V8 VM o VM\).</span><span class="sxs-lookup"><span data-stu-id="18d08-176">This section describes some memory-related topics specifically corresponding to the **V8 JavaScript virtual machine** \(V8 VM or VM\).</span></span>  

### <a name="javascript-object-representation"></a><span data-ttu-id="18d08-177">Representación de objetos de JavaScript</span><span class="sxs-lookup"><span data-stu-id="18d08-177">JavaScript object representation</span></span>  

<span data-ttu-id="18d08-178">Hay tres tipos primitivos:</span><span class="sxs-lookup"><span data-stu-id="18d08-178">There are three primitive types:</span></span>  

*   <span data-ttu-id="18d08-179">Números \(por ejemplo `3.14159...` \)</span><span class="sxs-lookup"><span data-stu-id="18d08-179">Numbers \(for example `3.14159...`\)</span></span>  
*   <span data-ttu-id="18d08-180">Booleans \( `true` o `false` \)</span><span class="sxs-lookup"><span data-stu-id="18d08-180">Booleans \(`true` or `false`\)</span></span>  
*   <span data-ttu-id="18d08-181">Cadenas \(por ejemplo `"Werner Heisenberg"` \)</span><span class="sxs-lookup"><span data-stu-id="18d08-181">Strings \(for example `"Werner Heisenberg"`\)</span></span>  

<span data-ttu-id="18d08-182">Los primitivos no pueden hacer referencia a otros valores y siempre son hojas o nodos de finalización.</span><span class="sxs-lookup"><span data-stu-id="18d08-182">Primitives are not able to reference other values and are always leafs or terminating nodes.</span></span>  

<span data-ttu-id="18d08-183">**Los** números se pueden almacenar como:</span><span class="sxs-lookup"><span data-stu-id="18d08-183">**Numbers** are able to be stored as either:</span></span>  

*   <span data-ttu-id="18d08-184">valores enteros inmediatos de 31 bits **denominados enteros pequeños** \(**SMI**s\) o</span><span class="sxs-lookup"><span data-stu-id="18d08-184">an immediate 31-bit integer values called **small integers** \(**SMI**s\), or</span></span>  
*   <span data-ttu-id="18d08-185">objetos de montón, denominados números **de montón**.</span><span class="sxs-lookup"><span data-stu-id="18d08-185">heap objects, referred to as **heap numbers**.</span></span> <span data-ttu-id="18d08-186">Los números de montón se usan para almacenar valores que no caben en el formulario SMI, como **dobles,** o cuando es necesario boxe un **valor,** como establecer propiedades en él.</span><span class="sxs-lookup"><span data-stu-id="18d08-186">Heap numbers are used for storing values that do not fit into the SMI form, such as **doubles**, or when a value needs to be **boxed**, such as setting properties on it.</span></span>  

<span data-ttu-id="18d08-187">**Las cadenas** pueden almacenarse en:</span><span class="sxs-lookup"><span data-stu-id="18d08-187">**Strings** are able to be stored in either:</span></span>  

*   <span data-ttu-id="18d08-188">el **montón de vm**o</span><span class="sxs-lookup"><span data-stu-id="18d08-188">the **VM heap**, or</span></span>
*   <span data-ttu-id="18d08-189">externamente en la **memoria del representador**.</span><span class="sxs-lookup"><span data-stu-id="18d08-189">externally in the **memory of the renderer**.</span></span>  <span data-ttu-id="18d08-190">Se **crea un** objeto contenedor y se usa para obtener acceso al almacenamiento externo donde, por ejemplo, se almacenan orígenes de scripts y otro contenido que se recibe de la Web, en lugar de copiarse en el montón de vm.</span><span class="sxs-lookup"><span data-stu-id="18d08-190">A **wrapper object** is created and used for accessing external storage where, for example, script sources and other content that is received from the Web is stored, rather than copied onto the VM heap.</span></span>

<span data-ttu-id="18d08-191">La memoria de los nuevos objetos JavaScript se asigna desde un montón de JavaScript dedicado \(o **montón de vm**\).</span><span class="sxs-lookup"><span data-stu-id="18d08-191">Memory for new JavaScript objects is allocated from a dedicated JavaScript heap \(or **VM heap**\).</span></span>  <span data-ttu-id="18d08-192">El recolector de elementos no utilizados administra estos objetos en V8 y, por lo tanto, permanecen vivos siempre que haya al menos una referencia segura a ellos.</span><span class="sxs-lookup"><span data-stu-id="18d08-192">These objects are managed by the garbage collector in V8 and therefore, stay alive as long as there is at least one strong reference to them.</span></span>  

<span data-ttu-id="18d08-193">Cualquier cosa que no esté en el montón de JavaScript se denomina **objeto nativo**.</span><span class="sxs-lookup"><span data-stu-id="18d08-193">Anything not in the JavaScript heap is called a **native object**.</span></span>  <span data-ttu-id="18d08-194">El recolector de elementos no utilizados V8 no administra los objetos nativos, a diferencia de los objetos montón, y solo se puede obtener acceso a ellos desde JavaScript mediante el objeto contenedor de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="18d08-194">Native objects, in contrast to heap objects, are not managed by the V8 garbage collector throughout their lifetime, and may only be accessed from JavaScript using the JavaScript wrapper object.</span></span>  

<span data-ttu-id="18d08-195">**La cadena Cons** es un objeto que consta de pares de cadenas almacenadas y luego unidas, y es el resultado de la concatenación.</span><span class="sxs-lookup"><span data-stu-id="18d08-195">**Cons string** is an object that consists of pairs of strings stored and then joined, and is a result of concatenation.</span></span>  <span data-ttu-id="18d08-196">La unión del contenido **de la cadena cons** se produce solo según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="18d08-196">The joining of the **cons string** contents occurs only as needed.</span></span>  <span data-ttu-id="18d08-197">Por ejemplo, cuando es necesario construir una subcadena de una cadena unida.</span><span class="sxs-lookup"><span data-stu-id="18d08-197">For example, when a substring of a joined string needs to be constructed.</span></span>

<span data-ttu-id="18d08-198">Por ejemplo, si concatena y `a` , obtiene una cadena que representa el resultado de la `b` `(a, b)` concatenación.</span><span class="sxs-lookup"><span data-stu-id="18d08-198">For example, if you concatenate `a` and `b`, you get a string `(a, b)` which represents the result of concatenation.</span></span>  <span data-ttu-id="18d08-199">Si más tarde concatena con `d` ese resultado, obtiene otra **cadena de cons**: `((a, b, d)` .</span><span class="sxs-lookup"><span data-stu-id="18d08-199">If you later concatenated `d` with that result, you get another **cons string**: `((a, b, d)`.</span></span>  

<span data-ttu-id="18d08-200">**Array** es un objeto con claves numéricas.</span><span class="sxs-lookup"><span data-stu-id="18d08-200">**Array** is an object with numeric keys.</span></span> <span data-ttu-id="18d08-201">**Las matrices** se usan ampliamente en la vm V8 para almacenar grandes cantidades de datos.</span><span class="sxs-lookup"><span data-stu-id="18d08-201">**Arrays** are used extensively in the V8 VM for storing large amounts of data.</span></span> <span data-ttu-id="18d08-202">Las matrices copian una copia de seguridad de los conjuntos de pares clave-valor, como **diccionarios.**</span><span class="sxs-lookup"><span data-stu-id="18d08-202">Sets of key-value pairs, like dictionaries, are backed up by **arrays**.</span></span>  

<span data-ttu-id="18d08-203">Un objeto JavaScript típico se almacena como solo uno de los dos tipos **de matriz:**</span><span class="sxs-lookup"><span data-stu-id="18d08-203">A typical JavaScript object is stored as only one of two **array** types:</span></span>  

*   <span data-ttu-id="18d08-204">propiedades con nombre y</span><span class="sxs-lookup"><span data-stu-id="18d08-204">named properties, and</span></span>  
*   <span data-ttu-id="18d08-205">elementos numéricos</span><span class="sxs-lookup"><span data-stu-id="18d08-205">numeric elements</span></span>  

<span data-ttu-id="18d08-206">Cuando hay un número reducido de propiedades, las propiedades se almacenan internamente en el objeto JavaScript.</span><span class="sxs-lookup"><span data-stu-id="18d08-206">When there are a small number of properties, the properties are stored internally in the JavaScript object.</span></span>  

<span data-ttu-id="18d08-207">**Map** es un objeto que describe tanto el tipo de objeto que es como el diseño.</span><span class="sxs-lookup"><span data-stu-id="18d08-207">**Map** is an object that describes both the kind of object it is and the layout.</span></span> <span data-ttu-id="18d08-208">Por ejemplo, los mapas se usan para describir jerarquías de objetos implícitos para [el acceso rápido a propiedades][V8FastProperties].</span><span class="sxs-lookup"><span data-stu-id="18d08-208">For example, maps are used to describe implicit object hierarchies for [fast property access][V8FastProperties].</span></span>  

### <a name="object-groups"></a><span data-ttu-id="18d08-209">Grupos de objetos</span><span class="sxs-lookup"><span data-stu-id="18d08-209">Object groups</span></span>  

<span data-ttu-id="18d08-210">Cada **grupo de objetos** nativos está hecho de objetos que tienen referencias mutuas entre sí.</span><span class="sxs-lookup"><span data-stu-id="18d08-210">Each **native objects** group is made up of objects that hold mutual references to each other.</span></span>  <span data-ttu-id="18d08-211">Tenga en cuenta, por ejemplo, un subárbol DOM donde cada nodo tiene un vínculo al elemento primario relativo y vínculos al siguiente elemento secundario y al siguiente elemento del mismo nivel, formando así un gráfico conectado.</span><span class="sxs-lookup"><span data-stu-id="18d08-211">Consider, for example, a DOM subtree where every node has a link to the relative parent and links to the next child and next sibling, therefore forming a connected graph.</span></span>  

> [!NOTE]
> <span data-ttu-id="18d08-212">Los objetos nativos no se representan en el montón de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="18d08-212">Native objects are not represented in the JavaScript heap.</span></span>  <span data-ttu-id="18d08-213">La falta de representación es la razón por la que los objetos nativos tienen un tamaño cero.</span><span class="sxs-lookup"><span data-stu-id="18d08-213">The lack of representation is why native objects have zero size.</span></span> <span data-ttu-id="18d08-214">En su lugar, se crean objetos contenedor.</span><span class="sxs-lookup"><span data-stu-id="18d08-214">Instead, wrapper objects are created.</span></span>  

<span data-ttu-id="18d08-215">Cada objeto contenedor contiene una referencia al objeto nativo correspondiente, para redirigir comandos a él.</span><span class="sxs-lookup"><span data-stu-id="18d08-215">Each wrapper object holds a reference to the corresponding native object, for redirecting commands to it.</span></span>  <span data-ttu-id="18d08-216">A su vez, un grupo de objetos contiene objetos contenedor.</span><span class="sxs-lookup"><span data-stu-id="18d08-216">In turn, an object group holds wrapper objects.</span></span>  <span data-ttu-id="18d08-217">Sin embargo, esto no crea un ciclo irreconectable, ya que recolector de elementos no utilizados es lo suficientemente inteligente como para liberar grupos de objetos cuyos contenedores ya no se hacen referencia.</span><span class="sxs-lookup"><span data-stu-id="18d08-217">However, this does not create an uncollectable cycle, as Garbage Collector is smart enough to release object groups whose wrappers are no longer referenced.</span></span>  <span data-ttu-id="18d08-218">Pero el olvido de liberar un solo contenedor contiene todo el grupo y los contenedores asociados.</span><span class="sxs-lookup"><span data-stu-id="18d08-218">But forgetting to release a single wrapper holds the whole group and associated wrappers.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="18d08-219">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="18d08-219">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Cómo grabar instantáneas de montón | Microsoft Docs"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Propiedades rápidas en V8 | V8"  

> [!NOTE]
> <span data-ttu-id="18d08-222">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="18d08-222">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="18d08-223">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) y es creado por [Meggin Kearney][MegginKearney] \(Technical Writer\).</span><span class="sxs-lookup"><span data-stu-id="18d08-223">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="18d08-225">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="18d08-225">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney

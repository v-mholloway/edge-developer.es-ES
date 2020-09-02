---
title: Terminología de la memoria
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: cb258135b7b3c931116d84b1e9b7a548a2b58a6d
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986272"
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

# <span data-ttu-id="5b560-103">Terminología de la memoria</span><span class="sxs-lookup"><span data-stu-id="5b560-103">Memory Terminology</span></span>  

<span data-ttu-id="5b560-104">En esta sección se describen los términos comunes que se usan en el análisis de memoria y se aplica a una variedad de herramientas de generación de perfiles de memoria para diferentes idiomas.</span><span class="sxs-lookup"><span data-stu-id="5b560-104">This section describes common terms used in memory analysis, and is applicable to a variety of memory profiling tools for different languages.</span></span>  

<span data-ttu-id="5b560-105">Las cláusulas y nociones que se describen aquí hacen referencia al [Panel memoria][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="5b560-105">The terms and notions described here refer to the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="5b560-106">Si alguna vez ha trabajado con Java, .NET o algún otro analizador de memoria, es posible que se trata de un repaso.</span><span class="sxs-lookup"><span data-stu-id="5b560-106">If you have ever worked with either the Java, .NET, or some other memory profiler, then this may be a refresher.</span></span>  

## <span data-ttu-id="5b560-107">Tamaños de objeto</span><span class="sxs-lookup"><span data-stu-id="5b560-107">Object sizes</span></span>  

<span data-ttu-id="5b560-108">Piense en la memoria como en un gráfico con tipos primitivos \ (como números y cadenas \) y objetos \ (asociantes de matrices \).</span><span class="sxs-lookup"><span data-stu-id="5b560-108">Think of memory as a graph with primitive types \(like numbers and strings\) and objects \(associative arrays\).</span></span>  <span data-ttu-id="5b560-109">Puede representarse visualmente como un gráfico con un número de puntos interconectados, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="5b560-109">It might visually be represented as a graph with a number of interconnected points as follows:</span></span>  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Representación visual de la memoria" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   <span data-ttu-id="5b560-111">Representación visual de la memoria</span><span class="sxs-lookup"><span data-stu-id="5b560-111">Visual representation of memory</span></span>  
:::image-end:::  

<span data-ttu-id="5b560-112">Un objeto puede contener memoria de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="5b560-112">An object may hold memory in two ways:</span></span>  

*   <span data-ttu-id="5b560-113">Directamente por el objeto.</span><span class="sxs-lookup"><span data-stu-id="5b560-113">Directly by the object.</span></span>  
*   <span data-ttu-id="5b560-114">De forma implícita, reteniendo referencias a otros objetos y, por lo tanto, impidiendo que un recolector de elementos no utilizados \ (**GC** por abreviado \) lo elimine automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5b560-114">Implicitly by holding references to other objects, and therefore preventing those objects from being automatically disposed by a garbage collector \(**GC** for short\).</span></span>  

<span data-ttu-id="5b560-115">Al trabajar con el panel [memoria][DevtoolsMemoryProblemsHeapSnapshots] en DevTools \ (una herramienta para investigar los problemas de memoria que se encuentran en **memoria**\), es posible que vea algunas columnas de información diferentes.</span><span class="sxs-lookup"><span data-stu-id="5b560-115">When working with the [Memory][DevtoolsMemoryProblemsHeapSnapshots] panel in DevTools \(a tool for investigating memory issues found under **Memory**\), you may find yourself looking at a few different columns of information.</span></span>  <span data-ttu-id="5b560-116">Dos que destaquen son **el tamaño superficial** y **el tamaño guardado**, pero ¿qué representa?</span><span class="sxs-lookup"><span data-stu-id="5b560-116">Two that stand out are **Shallow Size** and **Retained Size**, but what do these represent?</span></span>  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Tamaño Shallow y retenido" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   <span data-ttu-id="5b560-118">Tamaño Shallow y retenido</span><span class="sxs-lookup"><span data-stu-id="5b560-118">Shallow and Retained Size</span></span>  
:::image-end:::  

### <span data-ttu-id="5b560-119">Tamaño superficial</span><span class="sxs-lookup"><span data-stu-id="5b560-119">Shallow size</span></span>  

<span data-ttu-id="5b560-120">Este es el tamaño de la memoria que posee el objeto.</span><span class="sxs-lookup"><span data-stu-id="5b560-120">This is the size of memory that is held by the object.</span></span>  

<span data-ttu-id="5b560-121">Los objetos típicos de JavaScript tienen memoria reservada para su descripción y para almacenar valores inmediatos.</span><span class="sxs-lookup"><span data-stu-id="5b560-121">Typical JavaScript objects have some memory reserved for their description and for storing immediate values.</span></span>  <span data-ttu-id="5b560-122">Normalmente, solo las matrices y cadenas pueden tener un tamaño superficial significativo.</span><span class="sxs-lookup"><span data-stu-id="5b560-122">Usually, only arrays and strings are able to have a significant shallow size.</span></span>  <span data-ttu-id="5b560-123">Sin embargo, las cadenas y las matrices externas suelen tener su almacenamiento principal en la memoria del representador y solo exponen un pequeño objeto contenedor en el montón de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5b560-123">However, strings and external arrays often have their main storage in renderer memory, exposing only a small wrapper object on the JavaScript heap.</span></span>  

<span data-ttu-id="5b560-124">La memoria del representador es toda la memoria del proceso donde se representa una página inspeccionada: memoria nativa + JS memoria del montón de la memoria del montón Page + JS de todos los trabajadores dedicados iniciados por la página.</span><span class="sxs-lookup"><span data-stu-id="5b560-124">Renderer memory is all memory of the process where an inspected page is rendered: native memory + JS heap memory of the page + JS heap memory of all dedicated workers started by the page.</span></span>  <span data-ttu-id="5b560-125">Sin embargo, incluso un objeto pequeño puede contener una gran cantidad de memoria indirectamente, impidiendo que otros objetos sean eliminados por el proceso de recolección automática de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="5b560-125">Nevertheless, even a small object is able to hold a large amount of memory indirectly, by preventing other objects from being disposed of by the automatic garbage collection process.</span></span>  

### <span data-ttu-id="5b560-126">Tamaño retenido</span><span class="sxs-lookup"><span data-stu-id="5b560-126">Retained size</span></span>  

<span data-ttu-id="5b560-127">Este es el tamaño de memoria que se libera una vez que se elimina el objeto junto con los objetos dependientes que se han inaccesible desde las **raíces del recolector de elementos no utilizados** \ (raíces de GC \).</span><span class="sxs-lookup"><span data-stu-id="5b560-127">This is the size of memory that is freed once the object is deleted along with the dependent objects that were made unreachable from **Garbage Collector roots** \(GC roots\) .</span></span>  

<span data-ttu-id="5b560-128">Las **raíces del recolector de elementos no utilizados** \ (raíces de GC \) se componen de **identificadores** que se crean \ (local o global \) cuando se hace referencia desde código nativo a un objeto de JavaScript fuera de V8.</span><span class="sxs-lookup"><span data-stu-id="5b560-128">**Garbage Collector roots** \(GC roots\) are made up of **handles** that are created \(either local or global\) when making a reference from native code to a JavaScript object outside of V8.</span></span>  <span data-ttu-id="5b560-129">Puede encontrar todos los identificadores de ese tipo dentro de una instantánea de montones, en **raíces de GC**  >  **Handle scope** , **GC roots**  >  **identificadores globales**de ámbito y raíz del GC.</span><span class="sxs-lookup"><span data-stu-id="5b560-129">All such handles may be found within a heap snapshot under **GC roots** > **Handle scope** and **GC roots** > **Global handles**.</span></span>  <span data-ttu-id="5b560-130">La descripción de los identificadores de esta documentación sin profundizar en los detalles de la implementación del explorador puede resultar confusa.</span><span class="sxs-lookup"><span data-stu-id="5b560-130">Describing the handles in this documentation without diving into details of the browser implementation may be confusing.</span></span>  <span data-ttu-id="5b560-131">Tanto las raíces del recopilador de elementos no usados (GC) como los identificadores no son algo de lo que necesita preocuparse.</span><span class="sxs-lookup"><span data-stu-id="5b560-131">Both Garbage Collector (GC) roots and the handles are not something you need to worry about.</span></span>  

<span data-ttu-id="5b560-132">Hay una gran cantidad de raíces de GC internas, la mayoría de las cuales no son interesantes para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="5b560-132">There are lots of internal GC roots, most of which are not interesting for the users.</span></span>  <span data-ttu-id="5b560-133">Desde el punto de vista de las aplicaciones existen siguientes tipos de raíces.</span><span class="sxs-lookup"><span data-stu-id="5b560-133">From the applications standpoint there are following kinds of roots.</span></span>  

*   <span data-ttu-id="5b560-134">Objeto global Window \ (en cada iframe \).</span><span class="sxs-lookup"><span data-stu-id="5b560-134">Window global object \(in each iframe\).</span></span>  <span data-ttu-id="5b560-135">Hay un campo Distance en las instantáneas de montones, que es el número de referencias de propiedad en la ruta de retención más corta de la ventana.</span><span class="sxs-lookup"><span data-stu-id="5b560-135">There is a distance field in the heap snapshots which is the number of property references on the shortest retaining path from the window.</span></span>  
*   <span data-ttu-id="5b560-136">Árbol DOM de documento compuesto de todos los nodos DOM nativos a los que se puede atravesar el documento.</span><span class="sxs-lookup"><span data-stu-id="5b560-136">Document DOM tree consisting of all native DOM nodes reachable by traversing the document.</span></span>  <span data-ttu-id="5b560-137">Es posible que no todos los nodos tengan contenedores JS, pero si un nodo tiene un contenedor, estará activo mientras el documento está activo.</span><span class="sxs-lookup"><span data-stu-id="5b560-137">Not all of the nodes may have JS wrappers but if a node has a wrapper, it is alive while the document is alive.</span></span>  
*   <span data-ttu-id="5b560-138">A veces, el contexto del depurador puede conservar los objetos en el panel **orígenes** y la **consola** \ (por ejemplo, después de la evaluación de consola \).</span><span class="sxs-lookup"><span data-stu-id="5b560-138">Sometimes objects may be retained by the debugger context in the **Sources** panel and the **Console** \(for example after Console evaluation\).</span></span>  <span data-ttu-id="5b560-139">Crear instantáneas de montones con un panel de **consola** desactivado y sin puntos de interrupción activos en el depurador del panel **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="5b560-139">Create heap snapshots with a cleared **Console** panel and no active breakpoints in the debugger in the **Sources** panel.</span></span>

>[!TIP]
> <span data-ttu-id="5b560-140">Para borrar el panel de la **consola** , ejecute `clear()` y desactive los puntos de interrupción en el panel **fuentes** antes de tomar una instantánea del montón en el [Panel memoria][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="5b560-140">Clear the **Console** panel by running `clear()` and deactivate breakpoints in the **Sources** panel before taking a heap snapshot in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>

<span data-ttu-id="5b560-141">El gráfico de memoria se inicia con una raíz, que puede ser el `window` objeto del explorador o el `Global` objeto de un módulo Node.js.</span><span class="sxs-lookup"><span data-stu-id="5b560-141">The memory graph starts with a root, which may be the `window` object of the browser or the `Global` object of a Node.js module.</span></span>  <span data-ttu-id="5b560-142">No controla cómo se recolecta este objeto raíz (M.c. d).</span><span class="sxs-lookup"><span data-stu-id="5b560-142">You do not control how this root object is garbage collected (GCd).</span></span>  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="No puede controlar cómo se recolectan los elementos no utilizados en el objeto raíz." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   <span data-ttu-id="5b560-144">No puede controlar cómo se recolectan los elementos no utilizados en el objeto raíz.</span><span class="sxs-lookup"><span data-stu-id="5b560-144">You are not able to control how the root object is garbage collected.</span></span>  
:::image-end:::  

<span data-ttu-id="5b560-145">Lo que no sea accesible desde la raíz obtiene el recolector de elementos no usados \ (M.c. d \).</span><span class="sxs-lookup"><span data-stu-id="5b560-145">Whatever is not reachable from the root gets garbage collected \(GCd\).</span></span>  

> [!NOTE]
> <span data-ttu-id="5b560-146">Las columnas [tamaño superficial](#shallow-size) y [tamaño retenido](#retained-size) representan datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="5b560-146">Both the [Shallow size](#shallow-size) and [Retained size](#retained-size) columns represent data in bytes.</span></span>  

## <span data-ttu-id="5b560-147">Árbol de objetos reteniendo</span><span class="sxs-lookup"><span data-stu-id="5b560-147">Objects retaining tree</span></span>  

<span data-ttu-id="5b560-148">El montón es una red de objetos interconectados.</span><span class="sxs-lookup"><span data-stu-id="5b560-148">The heap is a network of interconnected objects.</span></span>  <span data-ttu-id="5b560-149">En el mundo matemático, esta estructura se denomina gráfico **o gráfico de memoria** .</span><span class="sxs-lookup"><span data-stu-id="5b560-149">In the mathematical world, this structure is called a **graph** or memory graph.</span></span>  <span data-ttu-id="5b560-150">Un gráfico se crea a partir de los **nodos** conectados por medio de **bordes**, de los cuales se proporcionan etiquetas.</span><span class="sxs-lookup"><span data-stu-id="5b560-150">A graph is constructed from **nodes** connected by means of **edges**, both of which are given labels.</span></span>  

*   <span data-ttu-id="5b560-151">Los **nodos** \ (u **objetos**\) se etiquetan con el nombre de la función **constructora** que se usó para crearlos.</span><span class="sxs-lookup"><span data-stu-id="5b560-151">**Nodes** \(or **objects**\) are labelled using the name of the **constructor** function that was used to build them.</span></span>  
*   <span data-ttu-id="5b560-152">Los **bordes** se etiquetan con los nombres de **las propiedades**.</span><span class="sxs-lookup"><span data-stu-id="5b560-152">**Edges** are labelled using the names of **properties**.</span></span>  

<span data-ttu-id="5b560-153">Obtenga información sobre [Cómo grabar un perfil con el generador de perfiles del montón][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="5b560-153">Learn [how to record a profile using the Heap Profiler][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="5b560-154">En la siguiente ilustración, algunas de las cosas llamativas que puede ver en el registro de instantáneas de montones en el [Panel memoria][DevtoolsMemoryProblemsHeapSnapshots] incluyen distancia: la distancia desde la raíz del recolector de elementos no utilizados \ (GC \).</span><span class="sxs-lookup"><span data-stu-id="5b560-154">In the following figure, some of the eye-catching things that you may see in the Heap Snapshot recording in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots] include distance:  the distance from the Garbage Collector \(GC\) root.</span></span>  <span data-ttu-id="5b560-155">Si casi todos los objetos del mismo tipo se encuentran a la misma distancia y algunos están a una mayor distancia, es algo que vale la pena investigar.</span><span class="sxs-lookup"><span data-stu-id="5b560-155">If almost all the objects of the same type are at the same distance, and a few are at a bigger distance, that is something worth investigating.</span></span>  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Distancia desde la raíz" lightbox="../media/memory-problems-root.msft.png":::
   <span data-ttu-id="5b560-157">Distancia desde la raíz</span><span class="sxs-lookup"><span data-stu-id="5b560-157">Distance from root</span></span>  
:::image-end:::  

## <span data-ttu-id="5b560-158">Dominators</span><span class="sxs-lookup"><span data-stu-id="5b560-158">Dominators</span></span>  

<span data-ttu-id="5b560-159">Los objetos Dominator se componen de una estructura de árbol, ya que cada objeto tiene exactamente un Dominator.</span><span class="sxs-lookup"><span data-stu-id="5b560-159">Dominator objects are comprised of a tree structure because each object has exactly one dominator.</span></span>  <span data-ttu-id="5b560-160">Un Dominator de un objeto puede carecer de referencias directas a un objeto que domina; es decir, el árbol de Dominator no es un árbol de expansión del gráfico.</span><span class="sxs-lookup"><span data-stu-id="5b560-160">A dominator of an object may lack direct references to an object it dominates; that is, the tree of the dominator is not a spanning tree of the graph.</span></span>  

<span data-ttu-id="5b560-161">En la siguiente ilustración, la siguiente instrucción es verdadera.</span><span class="sxs-lookup"><span data-stu-id="5b560-161">In the following figure, the following statement are true.</span></span>  

*   <span data-ttu-id="5b560-162">El nodo 1 domina el nodo 2</span><span class="sxs-lookup"><span data-stu-id="5b560-162">Node 1 dominates node 2</span></span>  
*   <span data-ttu-id="5b560-163">El nodo 2 predomina los nodos 3, 4 y 6</span><span class="sxs-lookup"><span data-stu-id="5b560-163">Node 2 dominates nodes 3, 4 and 6</span></span>  
*   <span data-ttu-id="5b560-164">Nodo 3 domina el nodo 5</span><span class="sxs-lookup"><span data-stu-id="5b560-164">Node 3 dominates node 5</span></span>  
*   <span data-ttu-id="5b560-165">El nodo 5 domina el nodo 8</span><span class="sxs-lookup"><span data-stu-id="5b560-165">Node 5 dominates node 8</span></span>  
*   <span data-ttu-id="5b560-166">El nodo 6 domina el nodo 7</span><span class="sxs-lookup"><span data-stu-id="5b560-166">Node 6 dominates node 7</span></span>  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Estructura de árbol de Dominator" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   <span data-ttu-id="5b560-168">Estructura de árbol de Dominator</span><span class="sxs-lookup"><span data-stu-id="5b560-168">Dominator tree structure</span></span>  
:::image-end:::  

<span data-ttu-id="5b560-169">En la siguiente ilustración, node `#3` es el Dominator de `#10` , pero `#7` también existe en cada path simple desde el recolector de elementos no utilizados \ (GC \) a `#10` .</span><span class="sxs-lookup"><span data-stu-id="5b560-169">In the following figure, node `#3` is the dominator of `#10`, but `#7` also exists in every simple path from Garbage Collector \(GC\) to `#10`.</span></span>  <span data-ttu-id="5b560-170">Por lo tanto, un objeto B es un Dominator de un objeto A si B existe en cada ruta simple de la raíz al objeto a.</span><span class="sxs-lookup"><span data-stu-id="5b560-170">Therefore, an object B is a dominator of an object A if B exists in every simple path from the root to the object A.</span></span>  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Ilustración Dominator animada" lightbox="../media/memory-problems-dominators.msft.gif":::
   <span data-ttu-id="5b560-172">Ilustración Dominator animada</span><span class="sxs-lookup"><span data-stu-id="5b560-172">Animated dominator illustration</span></span>  
:::image-end:::  

## <span data-ttu-id="5b560-173">Características específicas de V8</span><span class="sxs-lookup"><span data-stu-id="5b560-173">V8 specifics</span></span>  

<span data-ttu-id="5b560-174">Al generar perfiles de memoria, resulta útil comprender por qué las instantáneas de montones se ven de una determinada manera.</span><span class="sxs-lookup"><span data-stu-id="5b560-174">When profiling memory, it is helpful to understand why heap snapshots look a certain way.</span></span>  <span data-ttu-id="5b560-175">En esta sección se describen algunos temas relacionados con la memoria que corresponden específicamente a la **máquina virtual de JavaScript V8** \ (V8 VM o VM \).</span><span class="sxs-lookup"><span data-stu-id="5b560-175">This section describes some memory-related topics specifically corresponding to the **V8 JavaScript virtual machine** \(V8 VM or VM\).</span></span>  

### <span data-ttu-id="5b560-176">Representación de objeto de JavaScript</span><span class="sxs-lookup"><span data-stu-id="5b560-176">JavaScript object representation</span></span>  

<span data-ttu-id="5b560-177">Hay tres tipos primitivos:</span><span class="sxs-lookup"><span data-stu-id="5b560-177">There are three primitive types:</span></span>  

*   <span data-ttu-id="5b560-178">Números \ (por ejemplo `3.14159...` \)</span><span class="sxs-lookup"><span data-stu-id="5b560-178">Numbers \(for example `3.14159...`\)</span></span>  
*   <span data-ttu-id="5b560-179">Booleanos \ ( `true` o `false` \)</span><span class="sxs-lookup"><span data-stu-id="5b560-179">Booleans \(`true` or `false`\)</span></span>  
*   <span data-ttu-id="5b560-180">Cadenas \ (por ejemplo `"Werner Heisenberg"` \)</span><span class="sxs-lookup"><span data-stu-id="5b560-180">Strings \(for example `"Werner Heisenberg"`\)</span></span>  

<span data-ttu-id="5b560-181">Los tipos primitivos no pueden hacer referencia a otros valores y siempre son hojas o nodos de terminación.</span><span class="sxs-lookup"><span data-stu-id="5b560-181">Primitives are not able to reference other values and are always leafs or terminating nodes.</span></span>  

<span data-ttu-id="5b560-182">**Los números** se pueden almacenar como:</span><span class="sxs-lookup"><span data-stu-id="5b560-182">**Numbers** are able to be stored as either:</span></span>  

*   <span data-ttu-id="5b560-183">valores enteros de 31 bits inmediatos denominados **pequeños enteros** \ (**SMI**s \) o</span><span class="sxs-lookup"><span data-stu-id="5b560-183">an immediate 31-bit integer values called **small integers** \(**SMI**s\), or</span></span>  
*   <span data-ttu-id="5b560-184">objetos Heap, denominados **números de montones**.</span><span class="sxs-lookup"><span data-stu-id="5b560-184">heap objects, referred to as **heap numbers**.</span></span> <span data-ttu-id="5b560-185">Los números de montones se usan para almacenar valores que no se ajustan al formulario de SMI, como valores **Double**o cuando es necesario aplicar la **conversión boxing**a un valor, como establecer propiedades en él.</span><span class="sxs-lookup"><span data-stu-id="5b560-185">Heap numbers are used for storing values that do not fit into the SMI form, such as **doubles**, or when a value needs to be **boxed**, such as setting properties on it.</span></span>  

<span data-ttu-id="5b560-186">Las **cadenas** pueden almacenarse en:</span><span class="sxs-lookup"><span data-stu-id="5b560-186">**Strings** are able to be stored in either:</span></span>  

*   <span data-ttu-id="5b560-187">el **montón de VM**o</span><span class="sxs-lookup"><span data-stu-id="5b560-187">the **VM heap**, or</span></span>
*   <span data-ttu-id="5b560-188">externamente en la **memoria del representador**.</span><span class="sxs-lookup"><span data-stu-id="5b560-188">externally in the **memory of the renderer**.</span></span>  <span data-ttu-id="5b560-189">Se crea un **objeto contenedor** y se usa para acceder a un almacenamiento externo donde, por ejemplo, se almacenan los orígenes de script y otro contenido que se recibe de la web, en lugar de copiarse en el montón de la VM.</span><span class="sxs-lookup"><span data-stu-id="5b560-189">A **wrapper object** is created and used for accessing external storage where, for example, script sources and other content that is received from the Web is stored, rather than copied onto the VM heap.</span></span>

<span data-ttu-id="5b560-190">La memoria de los nuevos objetos de JavaScript se asigna desde un montón de JavaScript dedicado \ (o **montón VM**\).</span><span class="sxs-lookup"><span data-stu-id="5b560-190">Memory for new JavaScript objects is allocated from a dedicated JavaScript heap \(or **VM heap**\).</span></span>  <span data-ttu-id="5b560-191">Estos objetos se administran mediante el recolector de elementos no utilizados en V8 y, por lo tanto, permanecen activos siempre que haya al menos una referencia fuerte.</span><span class="sxs-lookup"><span data-stu-id="5b560-191">These objects are managed by the garbage collector in V8 and therefore, stay alive as long as there is at least one strong reference to them.</span></span>  

<span data-ttu-id="5b560-192">Todo lo que no esté en el montón de JavaScript se denomina **objeto nativo**.</span><span class="sxs-lookup"><span data-stu-id="5b560-192">Anything not in the JavaScript heap is called a **native object**.</span></span>  <span data-ttu-id="5b560-193">Los objetos nativos, a diferencia de los objetos Heap, no se administran en el recolector de elementos no utilizados de la V8 durante su período de duración, y solo se puede acceder a ellos desde JavaScript mediante el objeto wrapper de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5b560-193">Native objects, in contrast to heap objects, are not managed by the V8 garbage collector throughout their lifetime, and may only be accessed from JavaScript using the JavaScript wrapper object.</span></span>  

<span data-ttu-id="5b560-194">La **cadena cons** es un objeto que consta de pares de cadenas almacenadas y, a continuación, se unen, y es un resultado de una concatenación.</span><span class="sxs-lookup"><span data-stu-id="5b560-194">**Cons string** is an object that consists of pairs of strings stored and then joined, and is a result of concatenation.</span></span>  <span data-ttu-id="5b560-195">La Unión del contenido de la **cadena cons** solo se produce cuando es necesario.</span><span class="sxs-lookup"><span data-stu-id="5b560-195">The joining of the **cons string** contents occurs only as needed.</span></span> <span data-ttu-id="5b560-196">Un ejemplo sería cuando es necesario construir una subcadena de una cadena combinada.</span><span class="sxs-lookup"><span data-stu-id="5b560-196">An example would be when a substring of a joined string needs to be constructed.</span></span>

<span data-ttu-id="5b560-197">Por ejemplo, si concatena `a` y `b` , obtiene una cadena `(a, b)` que representa el resultado de la concatenación.</span><span class="sxs-lookup"><span data-stu-id="5b560-197">For example, if you concatenate `a` and `b`, you get a string `(a, b)` which represents the result of concatenation.</span></span>  <span data-ttu-id="5b560-198">Si más adelante se ha concatenado `d` con ese resultado, obtendrá otra **cadena de cons**: `((a, b, d)` .</span><span class="sxs-lookup"><span data-stu-id="5b560-198">If you later concatenated `d` with that result, you get another **cons string**: `((a, b, d)`.</span></span>  

<span data-ttu-id="5b560-199">**Matriz** es un objeto con teclas numéricas.</span><span class="sxs-lookup"><span data-stu-id="5b560-199">**Array** is an object with numeric keys.</span></span> <span data-ttu-id="5b560-200">Las **matrices** se usan ampliamente en la máquina virtual V8 para almacenar grandes cantidades de datos.</span><span class="sxs-lookup"><span data-stu-id="5b560-200">**Arrays** are used extensively in the V8 VM for storing large amounts of data.</span></span> <span data-ttu-id="5b560-201">Se realiza una copia de seguridad de los conjuntos de pares clave-valor, como diccionarios, por **matriz**.</span><span class="sxs-lookup"><span data-stu-id="5b560-201">Sets of key-value pairs, like dictionaries, are backed up by **arrays**.</span></span>  

<span data-ttu-id="5b560-202">Un objeto de JavaScript típico se almacena como uno de los dos tipos de **matriz** :</span><span class="sxs-lookup"><span data-stu-id="5b560-202">A typical JavaScript object is stored as only one of two **array** types:</span></span>  

*   <span data-ttu-id="5b560-203">propiedades con nombre y</span><span class="sxs-lookup"><span data-stu-id="5b560-203">named properties, and</span></span>  
*   <span data-ttu-id="5b560-204">elementos numéricos</span><span class="sxs-lookup"><span data-stu-id="5b560-204">numeric elements</span></span>  

<span data-ttu-id="5b560-205">Cuando hay un pequeño número de propiedades, las propiedades se almacenan internamente en el objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5b560-205">When there are a small number of properties, the properties are stored internally in the JavaScript object.</span></span>  

<span data-ttu-id="5b560-206">**Map** es un objeto que describe el tipo de objeto que es y el diseño.</span><span class="sxs-lookup"><span data-stu-id="5b560-206">**Map** is an object that describes both the kind of object it is and the layout.</span></span> <span data-ttu-id="5b560-207">Por ejemplo, los mapas se usan para describir jerarquías de objetos implícitas para un [acceso rápido a la propiedad][V8FastProperties].</span><span class="sxs-lookup"><span data-stu-id="5b560-207">For example, maps are used to describe implicit object hierarchies for [fast property access][V8FastProperties].</span></span>  

### <span data-ttu-id="5b560-208">Grupos de objetos</span><span class="sxs-lookup"><span data-stu-id="5b560-208">Object groups</span></span>  

<span data-ttu-id="5b560-209">Cada grupo de **objetos nativos** está compuesto de objetos que contienen referencias mutuas entre sí.</span><span class="sxs-lookup"><span data-stu-id="5b560-209">Each **native objects** group is made up of objects that hold mutual references to each other.</span></span>  <span data-ttu-id="5b560-210">Considere, por ejemplo, un subárbol DOM en el que cada nodo tiene un vínculo al elemento primario relativo y vincula al siguiente elemento secundario y al elemento relacionado siguiente, por lo tanto, formando un gráfico conectado.</span><span class="sxs-lookup"><span data-stu-id="5b560-210">Consider, for example, a DOM subtree where every node has a link to the relative parent and links to the next child and next sibling, therefore forming a connected graph.</span></span>  

> [!NOTE]
> <span data-ttu-id="5b560-211">Los objetos nativos no se representan en el montón de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5b560-211">Native objects are not represented in the JavaScript heap.</span></span>  <span data-ttu-id="5b560-212">La falta de representación es el motivo por el que los objetos nativos tienen el tamaño cero.</span><span class="sxs-lookup"><span data-stu-id="5b560-212">The lack of representation is why native objects have zero size.</span></span> <span data-ttu-id="5b560-213">En su lugar, se crean objetos contenedores.</span><span class="sxs-lookup"><span data-stu-id="5b560-213">Instead, wrapper objects are created.</span></span>  

<span data-ttu-id="5b560-214">Cada objeto contenedor mantiene una referencia al objeto nativo correspondiente, para redirigir comandos a él.</span><span class="sxs-lookup"><span data-stu-id="5b560-214">Each wrapper object holds a reference to the corresponding native object, for redirecting commands to it.</span></span>  <span data-ttu-id="5b560-215">A su vez, un grupo de objetos contiene objetos contenedores.</span><span class="sxs-lookup"><span data-stu-id="5b560-215">In turn, an object group holds wrapper objects.</span></span>  <span data-ttu-id="5b560-216">Sin embargo, esto no crea un ciclo que no se puede cobrar porque el recolector de elementos no usados \ (GC \) es lo suficientemente inteligente para liberar los grupos de objetos cuyos contenedores ya no se hacen referencia.</span><span class="sxs-lookup"><span data-stu-id="5b560-216">However, this does not create an uncollectable cycle, as Garbage Collector \(GC\) is smart enough to release object groups whose wrappers are no longer referenced.</span></span> <span data-ttu-id="5b560-217">Pero olvidar liberar un único contenedor alberga todo el grupo y los contenedores asociados.</span><span class="sxs-lookup"><span data-stu-id="5b560-217">But forgetting to release a single wrapper holds the whole group and associated wrappers.</span></span>  

## <span data-ttu-id="5b560-218">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5b560-218">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Cómo grabar instantáneas de montones | Microsoft docs"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Propiedades rápidas de V8 | V8"  

> [!NOTE]
> <span data-ttu-id="5b560-221">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5b560-221">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5b560-222">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) y está creada por [Meggin Kearney][MegginKearney] \ (editor técnico \).</span><span class="sxs-lookup"><span data-stu-id="5b560-222">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5b560-224">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5b560-224">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney

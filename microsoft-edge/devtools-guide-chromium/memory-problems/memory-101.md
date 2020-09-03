---
description: En esta sección se describen los términos comunes que se usan en el análisis de memoria y se aplica a una variedad de herramientas de generación de perfiles de memoria para diferentes idiomas.
title: Terminología de la memoria
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 3455b05cf19f3aa5a69de5571ab3a24d5654dfe4
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992753"
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

# <span data-ttu-id="9c121-104">Terminología de la memoria</span><span class="sxs-lookup"><span data-stu-id="9c121-104">Memory Terminology</span></span>  

<span data-ttu-id="9c121-105">En esta sección se describen los términos comunes que se usan en el análisis de memoria y se aplica a una variedad de herramientas de generación de perfiles de memoria para diferentes idiomas.</span><span class="sxs-lookup"><span data-stu-id="9c121-105">This section describes common terms used in memory analysis, and is applicable to a variety of memory profiling tools for different languages.</span></span>  

<span data-ttu-id="9c121-106">Las cláusulas y nociones que se describen aquí hacen referencia al [Panel memoria][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="9c121-106">The terms and notions described here refer to the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="9c121-107">Si alguna vez ha trabajado con Java, .NET o algún otro analizador de memoria, es posible que se trata de un repaso.</span><span class="sxs-lookup"><span data-stu-id="9c121-107">If you have ever worked with either the Java, .NET, or some other memory profiler, then this may be a refresher.</span></span>  

## <span data-ttu-id="9c121-108">Tamaños de objeto</span><span class="sxs-lookup"><span data-stu-id="9c121-108">Object sizes</span></span>  

<span data-ttu-id="9c121-109">Piense en la memoria como en un gráfico con tipos primitivos \ (como números y cadenas \) y objetos \ (asociantes de matrices \).</span><span class="sxs-lookup"><span data-stu-id="9c121-109">Think of memory as a graph with primitive types \(like numbers and strings\) and objects \(associative arrays\).</span></span>  <span data-ttu-id="9c121-110">Puede representarse visualmente como un gráfico con un número de puntos interconectados, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="9c121-110">It might visually be represented as a graph with a number of interconnected points as follows:</span></span>  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Representación visual de la memoria" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   <span data-ttu-id="9c121-112">Representación visual de la memoria</span><span class="sxs-lookup"><span data-stu-id="9c121-112">Visual representation of memory</span></span>  
:::image-end:::  

<span data-ttu-id="9c121-113">Un objeto puede contener memoria de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="9c121-113">An object may hold memory in two ways:</span></span>  

*   <span data-ttu-id="9c121-114">Directamente por el objeto.</span><span class="sxs-lookup"><span data-stu-id="9c121-114">Directly by the object.</span></span>  
*   <span data-ttu-id="9c121-115">De forma implícita, reteniendo referencias a otros objetos y, por lo tanto, impidiendo que un recolector de elementos no utilizados \ (**GC** por abreviado \) lo elimine automáticamente.</span><span class="sxs-lookup"><span data-stu-id="9c121-115">Implicitly by holding references to other objects, and therefore preventing those objects from being automatically disposed by a garbage collector \(**GC** for short\).</span></span>  

<span data-ttu-id="9c121-116">Al trabajar con el panel [memoria][DevtoolsMemoryProblemsHeapSnapshots] en DevTools \ (una herramienta para investigar los problemas de memoria que se encuentran en **memoria**\), es posible que vea algunas columnas de información diferentes.</span><span class="sxs-lookup"><span data-stu-id="9c121-116">When working with the [Memory][DevtoolsMemoryProblemsHeapSnapshots] panel in DevTools \(a tool for investigating memory issues found under **Memory**\), you may find yourself looking at a few different columns of information.</span></span>  <span data-ttu-id="9c121-117">Dos que destaquen son **el tamaño superficial** y **el tamaño guardado**, pero ¿qué representa?</span><span class="sxs-lookup"><span data-stu-id="9c121-117">Two that stand out are **Shallow Size** and **Retained Size**, but what do these represent?</span></span>  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Tamaño Shallow y retenido" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   <span data-ttu-id="9c121-119">Tamaño Shallow y retenido</span><span class="sxs-lookup"><span data-stu-id="9c121-119">Shallow and Retained Size</span></span>  
:::image-end:::  

### <span data-ttu-id="9c121-120">Tamaño superficial</span><span class="sxs-lookup"><span data-stu-id="9c121-120">Shallow size</span></span>  

<span data-ttu-id="9c121-121">Este es el tamaño de la memoria que posee el objeto.</span><span class="sxs-lookup"><span data-stu-id="9c121-121">This is the size of memory that is held by the object.</span></span>  

<span data-ttu-id="9c121-122">Los objetos típicos de JavaScript tienen memoria reservada para su descripción y para almacenar valores inmediatos.</span><span class="sxs-lookup"><span data-stu-id="9c121-122">Typical JavaScript objects have some memory reserved for their description and for storing immediate values.</span></span>  <span data-ttu-id="9c121-123">Normalmente, solo las matrices y cadenas pueden tener un tamaño superficial significativo.</span><span class="sxs-lookup"><span data-stu-id="9c121-123">Usually, only arrays and strings are able to have a significant shallow size.</span></span>  <span data-ttu-id="9c121-124">Sin embargo, las cadenas y las matrices externas suelen tener su almacenamiento principal en la memoria del representador y solo exponen un pequeño objeto contenedor en el montón de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9c121-124">However, strings and external arrays often have their main storage in renderer memory, exposing only a small wrapper object on the JavaScript heap.</span></span>  

<span data-ttu-id="9c121-125">La memoria del representador es toda la memoria del proceso donde se representa una página inspeccionada: memoria nativa + JS memoria del montón de la memoria del montón Page + JS de todos los trabajadores dedicados iniciados por la página.</span><span class="sxs-lookup"><span data-stu-id="9c121-125">Renderer memory is all memory of the process where an inspected page is rendered: native memory + JS heap memory of the page + JS heap memory of all dedicated workers started by the page.</span></span>  <span data-ttu-id="9c121-126">Sin embargo, incluso un objeto pequeño puede contener una gran cantidad de memoria indirectamente, impidiendo que otros objetos sean eliminados por el proceso de recolección automática de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="9c121-126">Nevertheless, even a small object is able to hold a large amount of memory indirectly, by preventing other objects from being disposed of by the automatic garbage collection process.</span></span>  

### <span data-ttu-id="9c121-127">Tamaño retenido</span><span class="sxs-lookup"><span data-stu-id="9c121-127">Retained size</span></span>  

<span data-ttu-id="9c121-128">Este es el tamaño de memoria que se libera una vez que se elimina el objeto junto con los objetos dependientes que se han inaccesible desde las **raíces del recolector de elementos no utilizados** \ (raíces de GC \).</span><span class="sxs-lookup"><span data-stu-id="9c121-128">This is the size of memory that is freed once the object is deleted along with the dependent objects that were made unreachable from **Garbage Collector roots** \(GC roots\) .</span></span>  

<span data-ttu-id="9c121-129">Las **raíces del recolector de elementos no utilizados** \ (raíces de GC \) se componen de **identificadores** que se crean \ (local o global \) cuando se hace referencia desde código nativo a un objeto de JavaScript fuera de V8.</span><span class="sxs-lookup"><span data-stu-id="9c121-129">**Garbage Collector roots** \(GC roots\) are made up of **handles** that are created \(either local or global\) when making a reference from native code to a JavaScript object outside of V8.</span></span>  <span data-ttu-id="9c121-130">Puede encontrar todos los identificadores de ese tipo dentro de una instantánea de montones, en **raíces de GC**  >  **Handle scope** , **GC roots**  >  **identificadores globales**de ámbito y raíz del GC.</span><span class="sxs-lookup"><span data-stu-id="9c121-130">All such handles may be found within a heap snapshot under **GC roots** > **Handle scope** and **GC roots** > **Global handles**.</span></span>  <span data-ttu-id="9c121-131">La descripción de los identificadores de esta documentación sin profundizar en los detalles de la implementación del explorador puede resultar confusa.</span><span class="sxs-lookup"><span data-stu-id="9c121-131">Describing the handles in this documentation without diving into details of the browser implementation may be confusing.</span></span>  <span data-ttu-id="9c121-132">Tanto las raíces del recopilador de elementos no usados (GC) como los identificadores no son algo de lo que necesita preocuparse.</span><span class="sxs-lookup"><span data-stu-id="9c121-132">Both Garbage Collector (GC) roots and the handles are not something you need to worry about.</span></span>  

<span data-ttu-id="9c121-133">Hay una gran cantidad de raíces de GC internas, la mayoría de las cuales no son interesantes para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="9c121-133">There are lots of internal GC roots, most of which are not interesting for the users.</span></span>  <span data-ttu-id="9c121-134">Desde el punto de vista de las aplicaciones existen siguientes tipos de raíces.</span><span class="sxs-lookup"><span data-stu-id="9c121-134">From the applications standpoint there are following kinds of roots.</span></span>  

*   <span data-ttu-id="9c121-135">Objeto global Window \ (en cada iframe \).</span><span class="sxs-lookup"><span data-stu-id="9c121-135">Window global object \(in each iframe\).</span></span>  <span data-ttu-id="9c121-136">Hay un campo Distance en las instantáneas de montones, que es el número de referencias de propiedad en la ruta de retención más corta de la ventana.</span><span class="sxs-lookup"><span data-stu-id="9c121-136">There is a distance field in the heap snapshots which is the number of property references on the shortest retaining path from the window.</span></span>  
*   <span data-ttu-id="9c121-137">Árbol DOM de documento compuesto de todos los nodos DOM nativos a los que se puede atravesar el documento.</span><span class="sxs-lookup"><span data-stu-id="9c121-137">Document DOM tree consisting of all native DOM nodes reachable by traversing the document.</span></span>  <span data-ttu-id="9c121-138">Es posible que no todos los nodos tengan contenedores JS, pero si un nodo tiene un contenedor, estará activo mientras el documento está activo.</span><span class="sxs-lookup"><span data-stu-id="9c121-138">Not all of the nodes may have JS wrappers but if a node has a wrapper, it is alive while the document is alive.</span></span>  
*   <span data-ttu-id="9c121-139">A veces, el contexto del depurador puede conservar los objetos en el panel **orígenes** y la **consola** \ (por ejemplo, después de la evaluación de consola \).</span><span class="sxs-lookup"><span data-stu-id="9c121-139">Sometimes objects may be retained by the debugger context in the **Sources** panel and the **Console** \(for example after Console evaluation\).</span></span>  <span data-ttu-id="9c121-140">Crear instantáneas de montones con un panel de **consola** desactivado y sin puntos de interrupción activos en el depurador del panel **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="9c121-140">Create heap snapshots with a cleared **Console** panel and no active breakpoints in the debugger in the **Sources** panel.</span></span>

>[!TIP]
> <span data-ttu-id="9c121-141">Para borrar el panel de la **consola** , ejecute `clear()` y desactive los puntos de interrupción en el panel **fuentes** antes de tomar una instantánea del montón en el [Panel memoria][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="9c121-141">Clear the **Console** panel by running `clear()` and deactivate breakpoints in the **Sources** panel before taking a heap snapshot in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>

<span data-ttu-id="9c121-142">El gráfico de memoria se inicia con una raíz, que puede ser el `window` objeto del explorador o el `Global` objeto de un módulo Node.js.</span><span class="sxs-lookup"><span data-stu-id="9c121-142">The memory graph starts with a root, which may be the `window` object of the browser or the `Global` object of a Node.js module.</span></span>  <span data-ttu-id="9c121-143">No controla cómo se recolecta este objeto raíz (M.c. d).</span><span class="sxs-lookup"><span data-stu-id="9c121-143">You do not control how this root object is garbage collected (GCd).</span></span>  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="No puede controlar cómo se recolectan los elementos no utilizados en el objeto raíz." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   <span data-ttu-id="9c121-145">No puede controlar cómo se recolectan los elementos no utilizados en el objeto raíz.</span><span class="sxs-lookup"><span data-stu-id="9c121-145">You are not able to control how the root object is garbage collected.</span></span>  
:::image-end:::  

<span data-ttu-id="9c121-146">Lo que no sea accesible desde la raíz obtiene el recolector de elementos no usados \ (M.c. d \).</span><span class="sxs-lookup"><span data-stu-id="9c121-146">Whatever is not reachable from the root gets garbage collected \(GCd\).</span></span>  

> [!NOTE]
> <span data-ttu-id="9c121-147">Las columnas [tamaño superficial](#shallow-size) y [tamaño retenido](#retained-size) representan datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="9c121-147">Both the [Shallow size](#shallow-size) and [Retained size](#retained-size) columns represent data in bytes.</span></span>  

## <span data-ttu-id="9c121-148">Árbol de objetos reteniendo</span><span class="sxs-lookup"><span data-stu-id="9c121-148">Objects retaining tree</span></span>  

<span data-ttu-id="9c121-149">El montón es una red de objetos interconectados.</span><span class="sxs-lookup"><span data-stu-id="9c121-149">The heap is a network of interconnected objects.</span></span>  <span data-ttu-id="9c121-150">En el mundo matemático, esta estructura se denomina gráfico **o gráfico de memoria** .</span><span class="sxs-lookup"><span data-stu-id="9c121-150">In the mathematical world, this structure is called a **graph** or memory graph.</span></span>  <span data-ttu-id="9c121-151">Un gráfico se crea a partir de los **nodos** conectados por medio de **bordes**, de los cuales se proporcionan etiquetas.</span><span class="sxs-lookup"><span data-stu-id="9c121-151">A graph is constructed from **nodes** connected by means of **edges**, both of which are given labels.</span></span>  

*   <span data-ttu-id="9c121-152">Los **nodos** \ (u **objetos**\) se etiquetan con el nombre de la función **constructora** que se usó para crearlos.</span><span class="sxs-lookup"><span data-stu-id="9c121-152">**Nodes** \(or **objects**\) are labelled using the name of the **constructor** function that was used to build them.</span></span>  
*   <span data-ttu-id="9c121-153">Los **bordes** se etiquetan con los nombres de **las propiedades**.</span><span class="sxs-lookup"><span data-stu-id="9c121-153">**Edges** are labelled using the names of **properties**.</span></span>  

<span data-ttu-id="9c121-154">Obtenga información sobre [Cómo grabar un perfil con el generador de perfiles del montón][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="9c121-154">Learn [how to record a profile using the Heap Profiler][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="9c121-155">En la siguiente ilustración, algunas de las cosas llamativas que puede ver en el registro de instantáneas de montones en el [Panel memoria][DevtoolsMemoryProblemsHeapSnapshots] incluyen distancia: la distancia desde la raíz del recolector de elementos no utilizados \ (GC \).</span><span class="sxs-lookup"><span data-stu-id="9c121-155">In the following figure, some of the eye-catching things that you may see in the Heap Snapshot recording in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots] include distance:  the distance from the Garbage Collector \(GC\) root.</span></span>  <span data-ttu-id="9c121-156">Si casi todos los objetos del mismo tipo se encuentran a la misma distancia y algunos están a una mayor distancia, es algo que vale la pena investigar.</span><span class="sxs-lookup"><span data-stu-id="9c121-156">If almost all the objects of the same type are at the same distance, and a few are at a bigger distance, that is something worth investigating.</span></span>  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Distancia desde la raíz" lightbox="../media/memory-problems-root.msft.png":::
   <span data-ttu-id="9c121-158">Distancia desde la raíz</span><span class="sxs-lookup"><span data-stu-id="9c121-158">Distance from root</span></span>  
:::image-end:::  

## <span data-ttu-id="9c121-159">Dominators</span><span class="sxs-lookup"><span data-stu-id="9c121-159">Dominators</span></span>  

<span data-ttu-id="9c121-160">Los objetos Dominator se componen de una estructura de árbol, ya que cada objeto tiene exactamente un Dominator.</span><span class="sxs-lookup"><span data-stu-id="9c121-160">Dominator objects are comprised of a tree structure because each object has exactly one dominator.</span></span>  <span data-ttu-id="9c121-161">Un Dominator de un objeto puede carecer de referencias directas a un objeto que domina; es decir, el árbol de Dominator no es un árbol de expansión del gráfico.</span><span class="sxs-lookup"><span data-stu-id="9c121-161">A dominator of an object may lack direct references to an object it dominates; that is, the tree of the dominator is not a spanning tree of the graph.</span></span>  

<span data-ttu-id="9c121-162">En la siguiente ilustración, la siguiente instrucción es verdadera.</span><span class="sxs-lookup"><span data-stu-id="9c121-162">In the following figure, the following statement are true.</span></span>  

*   <span data-ttu-id="9c121-163">El nodo 1 domina el nodo 2</span><span class="sxs-lookup"><span data-stu-id="9c121-163">Node 1 dominates node 2</span></span>  
*   <span data-ttu-id="9c121-164">El nodo 2 predomina los nodos 3, 4 y 6</span><span class="sxs-lookup"><span data-stu-id="9c121-164">Node 2 dominates nodes 3, 4 and 6</span></span>  
*   <span data-ttu-id="9c121-165">Nodo 3 domina el nodo 5</span><span class="sxs-lookup"><span data-stu-id="9c121-165">Node 3 dominates node 5</span></span>  
*   <span data-ttu-id="9c121-166">El nodo 5 domina el nodo 8</span><span class="sxs-lookup"><span data-stu-id="9c121-166">Node 5 dominates node 8</span></span>  
*   <span data-ttu-id="9c121-167">El nodo 6 domina el nodo 7</span><span class="sxs-lookup"><span data-stu-id="9c121-167">Node 6 dominates node 7</span></span>  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Estructura de árbol de Dominator" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   <span data-ttu-id="9c121-169">Estructura de árbol de Dominator</span><span class="sxs-lookup"><span data-stu-id="9c121-169">Dominator tree structure</span></span>  
:::image-end:::  

<span data-ttu-id="9c121-170">En la siguiente ilustración, node `#3` es el Dominator de `#10` , pero `#7` también existe en cada path simple desde el recolector de elementos no utilizados \ (GC \) a `#10` .</span><span class="sxs-lookup"><span data-stu-id="9c121-170">In the following figure, node `#3` is the dominator of `#10`, but `#7` also exists in every simple path from Garbage Collector \(GC\) to `#10`.</span></span>  <span data-ttu-id="9c121-171">Por lo tanto, un objeto B es un Dominator de un objeto A si B existe en cada ruta simple de la raíz al objeto a.</span><span class="sxs-lookup"><span data-stu-id="9c121-171">Therefore, an object B is a dominator of an object A if B exists in every simple path from the root to the object A.</span></span>  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Ilustración Dominator animada" lightbox="../media/memory-problems-dominators.msft.gif":::
   <span data-ttu-id="9c121-173">Ilustración Dominator animada</span><span class="sxs-lookup"><span data-stu-id="9c121-173">Animated dominator illustration</span></span>  
:::image-end:::  

## <span data-ttu-id="9c121-174">Características específicas de V8</span><span class="sxs-lookup"><span data-stu-id="9c121-174">V8 specifics</span></span>  

<span data-ttu-id="9c121-175">Al generar perfiles de memoria, resulta útil comprender por qué las instantáneas de montones se ven de una determinada manera.</span><span class="sxs-lookup"><span data-stu-id="9c121-175">When profiling memory, it is helpful to understand why heap snapshots look a certain way.</span></span>  <span data-ttu-id="9c121-176">En esta sección se describen algunos temas relacionados con la memoria que corresponden específicamente a la **máquina virtual de JavaScript V8** \ (V8 VM o VM \).</span><span class="sxs-lookup"><span data-stu-id="9c121-176">This section describes some memory-related topics specifically corresponding to the **V8 JavaScript virtual machine** \(V8 VM or VM\).</span></span>  

### <span data-ttu-id="9c121-177">Representación de objeto de JavaScript</span><span class="sxs-lookup"><span data-stu-id="9c121-177">JavaScript object representation</span></span>  

<span data-ttu-id="9c121-178">Hay tres tipos primitivos:</span><span class="sxs-lookup"><span data-stu-id="9c121-178">There are three primitive types:</span></span>  

*   <span data-ttu-id="9c121-179">Números \ (por ejemplo `3.14159...` \)</span><span class="sxs-lookup"><span data-stu-id="9c121-179">Numbers \(for example `3.14159...`\)</span></span>  
*   <span data-ttu-id="9c121-180">Booleanos \ ( `true` o `false` \)</span><span class="sxs-lookup"><span data-stu-id="9c121-180">Booleans \(`true` or `false`\)</span></span>  
*   <span data-ttu-id="9c121-181">Cadenas \ (por ejemplo `"Werner Heisenberg"` \)</span><span class="sxs-lookup"><span data-stu-id="9c121-181">Strings \(for example `"Werner Heisenberg"`\)</span></span>  

<span data-ttu-id="9c121-182">Los tipos primitivos no pueden hacer referencia a otros valores y siempre son hojas o nodos de terminación.</span><span class="sxs-lookup"><span data-stu-id="9c121-182">Primitives are not able to reference other values and are always leafs or terminating nodes.</span></span>  

<span data-ttu-id="9c121-183">**Los números** se pueden almacenar como:</span><span class="sxs-lookup"><span data-stu-id="9c121-183">**Numbers** are able to be stored as either:</span></span>  

*   <span data-ttu-id="9c121-184">valores enteros de 31 bits inmediatos denominados **pequeños enteros** \ (**SMI**s \) o</span><span class="sxs-lookup"><span data-stu-id="9c121-184">an immediate 31-bit integer values called **small integers** \(**SMI**s\), or</span></span>  
*   <span data-ttu-id="9c121-185">objetos Heap, denominados **números de montones**.</span><span class="sxs-lookup"><span data-stu-id="9c121-185">heap objects, referred to as **heap numbers**.</span></span> <span data-ttu-id="9c121-186">Los números de montones se usan para almacenar valores que no se ajustan al formulario de SMI, como valores **Double**o cuando es necesario aplicar la **conversión boxing**a un valor, como establecer propiedades en él.</span><span class="sxs-lookup"><span data-stu-id="9c121-186">Heap numbers are used for storing values that do not fit into the SMI form, such as **doubles**, or when a value needs to be **boxed**, such as setting properties on it.</span></span>  

<span data-ttu-id="9c121-187">Las **cadenas** pueden almacenarse en:</span><span class="sxs-lookup"><span data-stu-id="9c121-187">**Strings** are able to be stored in either:</span></span>  

*   <span data-ttu-id="9c121-188">el **montón de VM**o</span><span class="sxs-lookup"><span data-stu-id="9c121-188">the **VM heap**, or</span></span>
*   <span data-ttu-id="9c121-189">externamente en la **memoria del representador**.</span><span class="sxs-lookup"><span data-stu-id="9c121-189">externally in the **memory of the renderer**.</span></span>  <span data-ttu-id="9c121-190">Se crea un **objeto contenedor** y se usa para acceder a un almacenamiento externo donde, por ejemplo, se almacenan los orígenes de script y otro contenido que se recibe de la web, en lugar de copiarse en el montón de la VM.</span><span class="sxs-lookup"><span data-stu-id="9c121-190">A **wrapper object** is created and used for accessing external storage where, for example, script sources and other content that is received from the Web is stored, rather than copied onto the VM heap.</span></span>

<span data-ttu-id="9c121-191">La memoria de los nuevos objetos de JavaScript se asigna desde un montón de JavaScript dedicado \ (o **montón VM**\).</span><span class="sxs-lookup"><span data-stu-id="9c121-191">Memory for new JavaScript objects is allocated from a dedicated JavaScript heap \(or **VM heap**\).</span></span>  <span data-ttu-id="9c121-192">Estos objetos se administran mediante el recolector de elementos no utilizados en V8 y, por lo tanto, permanecen activos siempre que haya al menos una referencia fuerte.</span><span class="sxs-lookup"><span data-stu-id="9c121-192">These objects are managed by the garbage collector in V8 and therefore, stay alive as long as there is at least one strong reference to them.</span></span>  

<span data-ttu-id="9c121-193">Todo lo que no esté en el montón de JavaScript se denomina **objeto nativo**.</span><span class="sxs-lookup"><span data-stu-id="9c121-193">Anything not in the JavaScript heap is called a **native object**.</span></span>  <span data-ttu-id="9c121-194">Los objetos nativos, a diferencia de los objetos Heap, no se administran en el recolector de elementos no utilizados de la V8 durante su período de duración, y solo se puede acceder a ellos desde JavaScript mediante el objeto wrapper de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9c121-194">Native objects, in contrast to heap objects, are not managed by the V8 garbage collector throughout their lifetime, and may only be accessed from JavaScript using the JavaScript wrapper object.</span></span>  

<span data-ttu-id="9c121-195">La **cadena cons** es un objeto que consta de pares de cadenas almacenadas y, a continuación, se unen, y es un resultado de una concatenación.</span><span class="sxs-lookup"><span data-stu-id="9c121-195">**Cons string** is an object that consists of pairs of strings stored and then joined, and is a result of concatenation.</span></span>  <span data-ttu-id="9c121-196">La Unión del contenido de la **cadena cons** solo se produce cuando es necesario.</span><span class="sxs-lookup"><span data-stu-id="9c121-196">The joining of the **cons string** contents occurs only as needed.</span></span> <span data-ttu-id="9c121-197">Un ejemplo sería cuando es necesario construir una subcadena de una cadena combinada.</span><span class="sxs-lookup"><span data-stu-id="9c121-197">An example would be when a substring of a joined string needs to be constructed.</span></span>

<span data-ttu-id="9c121-198">Por ejemplo, si concatena `a` y `b` , obtiene una cadena `(a, b)` que representa el resultado de la concatenación.</span><span class="sxs-lookup"><span data-stu-id="9c121-198">For example, if you concatenate `a` and `b`, you get a string `(a, b)` which represents the result of concatenation.</span></span>  <span data-ttu-id="9c121-199">Si más adelante se ha concatenado `d` con ese resultado, obtendrá otra **cadena de cons**: `((a, b, d)` .</span><span class="sxs-lookup"><span data-stu-id="9c121-199">If you later concatenated `d` with that result, you get another **cons string**: `((a, b, d)`.</span></span>  

<span data-ttu-id="9c121-200">**Matriz** es un objeto con teclas numéricas.</span><span class="sxs-lookup"><span data-stu-id="9c121-200">**Array** is an object with numeric keys.</span></span> <span data-ttu-id="9c121-201">Las **matrices** se usan ampliamente en la máquina virtual V8 para almacenar grandes cantidades de datos.</span><span class="sxs-lookup"><span data-stu-id="9c121-201">**Arrays** are used extensively in the V8 VM for storing large amounts of data.</span></span> <span data-ttu-id="9c121-202">Se realiza una copia de seguridad de los conjuntos de pares clave-valor, como diccionarios, por **matriz**.</span><span class="sxs-lookup"><span data-stu-id="9c121-202">Sets of key-value pairs, like dictionaries, are backed up by **arrays**.</span></span>  

<span data-ttu-id="9c121-203">Un objeto de JavaScript típico se almacena como uno de los dos tipos de **matriz** :</span><span class="sxs-lookup"><span data-stu-id="9c121-203">A typical JavaScript object is stored as only one of two **array** types:</span></span>  

*   <span data-ttu-id="9c121-204">propiedades con nombre y</span><span class="sxs-lookup"><span data-stu-id="9c121-204">named properties, and</span></span>  
*   <span data-ttu-id="9c121-205">elementos numéricos</span><span class="sxs-lookup"><span data-stu-id="9c121-205">numeric elements</span></span>  

<span data-ttu-id="9c121-206">Cuando hay un pequeño número de propiedades, las propiedades se almacenan internamente en el objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9c121-206">When there are a small number of properties, the properties are stored internally in the JavaScript object.</span></span>  

<span data-ttu-id="9c121-207">**Map** es un objeto que describe el tipo de objeto que es y el diseño.</span><span class="sxs-lookup"><span data-stu-id="9c121-207">**Map** is an object that describes both the kind of object it is and the layout.</span></span> <span data-ttu-id="9c121-208">Por ejemplo, los mapas se usan para describir jerarquías de objetos implícitas para un [acceso rápido a la propiedad][V8FastProperties].</span><span class="sxs-lookup"><span data-stu-id="9c121-208">For example, maps are used to describe implicit object hierarchies for [fast property access][V8FastProperties].</span></span>  

### <span data-ttu-id="9c121-209">Grupos de objetos</span><span class="sxs-lookup"><span data-stu-id="9c121-209">Object groups</span></span>  

<span data-ttu-id="9c121-210">Cada grupo de **objetos nativos** está compuesto de objetos que contienen referencias mutuas entre sí.</span><span class="sxs-lookup"><span data-stu-id="9c121-210">Each **native objects** group is made up of objects that hold mutual references to each other.</span></span>  <span data-ttu-id="9c121-211">Considere, por ejemplo, un subárbol DOM en el que cada nodo tiene un vínculo al elemento primario relativo y vincula al siguiente elemento secundario y al elemento relacionado siguiente, por lo tanto, formando un gráfico conectado.</span><span class="sxs-lookup"><span data-stu-id="9c121-211">Consider, for example, a DOM subtree where every node has a link to the relative parent and links to the next child and next sibling, therefore forming a connected graph.</span></span>  

> [!NOTE]
> <span data-ttu-id="9c121-212">Los objetos nativos no se representan en el montón de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9c121-212">Native objects are not represented in the JavaScript heap.</span></span>  <span data-ttu-id="9c121-213">La falta de representación es el motivo por el que los objetos nativos tienen el tamaño cero.</span><span class="sxs-lookup"><span data-stu-id="9c121-213">The lack of representation is why native objects have zero size.</span></span> <span data-ttu-id="9c121-214">En su lugar, se crean objetos contenedores.</span><span class="sxs-lookup"><span data-stu-id="9c121-214">Instead, wrapper objects are created.</span></span>  

<span data-ttu-id="9c121-215">Cada objeto contenedor mantiene una referencia al objeto nativo correspondiente, para redirigir comandos a él.</span><span class="sxs-lookup"><span data-stu-id="9c121-215">Each wrapper object holds a reference to the corresponding native object, for redirecting commands to it.</span></span>  <span data-ttu-id="9c121-216">A su vez, un grupo de objetos contiene objetos contenedores.</span><span class="sxs-lookup"><span data-stu-id="9c121-216">In turn, an object group holds wrapper objects.</span></span>  <span data-ttu-id="9c121-217">Sin embargo, esto no crea un ciclo que no se puede cobrar porque el recolector de elementos no usados \ (GC \) es lo suficientemente inteligente para liberar los grupos de objetos cuyos contenedores ya no se hacen referencia.</span><span class="sxs-lookup"><span data-stu-id="9c121-217">However, this does not create an uncollectable cycle, as Garbage Collector \(GC\) is smart enough to release object groups whose wrappers are no longer referenced.</span></span> <span data-ttu-id="9c121-218">Pero olvidar liberar un único contenedor alberga todo el grupo y los contenedores asociados.</span><span class="sxs-lookup"><span data-stu-id="9c121-218">But forgetting to release a single wrapper holds the whole group and associated wrappers.</span></span>  

## <span data-ttu-id="9c121-219">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9c121-219">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Cómo grabar instantáneas de montones | Microsoft docs"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Propiedades rápidas de V8 | V8"  

> [!NOTE]
> <span data-ttu-id="9c121-222">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9c121-222">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9c121-223">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) y está creada por [Meggin Kearney][MegginKearney] \ (editor técnico \).</span><span class="sxs-lookup"><span data-stu-id="9c121-223">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9c121-225">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9c121-225">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney

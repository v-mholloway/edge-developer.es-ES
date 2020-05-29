---
title: Terminología de la memoria
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e3373cf1475ec0eeaabcebf1a7f49505c7a3c1bb
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611730"
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





# <span data-ttu-id="2da55-103">Terminología de la memoria</span><span class="sxs-lookup"><span data-stu-id="2da55-103">Memory Terminology</span></span>   



<span data-ttu-id="2da55-104">En esta sección se describen los términos comunes que se usan en el análisis de memoria y se aplica a una variedad de herramientas de generación de perfiles de memoria para diferentes idiomas.</span><span class="sxs-lookup"><span data-stu-id="2da55-104">This section describes common terms used in memory analysis, and is applicable to a variety of memory profiling tools for different languages.</span></span>  

<span data-ttu-id="2da55-105">Las cláusulas y nociones que se describen aquí hacen referencia al [Panel memoria][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="2da55-105">The terms and notions described here refer to the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="2da55-106">Si alguna vez ha trabajado con Java, .NET o algún otro analizador de memoria, es posible que se trata de un repaso.</span><span class="sxs-lookup"><span data-stu-id="2da55-106">If you have ever worked with either the Java, .NET, or some other memory profiler, then this may be a refresher.</span></span>  

## <span data-ttu-id="2da55-107">Tamaños de objeto</span><span class="sxs-lookup"><span data-stu-id="2da55-107">Object sizes</span></span>  

<span data-ttu-id="2da55-108">Piense en la memoria como en un gráfico con tipos primitivos \ (como números y cadenas \) y objetos \ (asociantes de matrices \).</span><span class="sxs-lookup"><span data-stu-id="2da55-108">Think of memory as a graph with primitive types \(like numbers and strings\) and objects \(associative arrays\).</span></span>  <span data-ttu-id="2da55-109">Puede representarse visualmente como un gráfico con un número de puntos interconectados, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="2da55-109">It might visually be represented as a graph with a number of interconnected points as follows:</span></span>  

> ##### <span data-ttu-id="2da55-110">Figura 1</span><span class="sxs-lookup"><span data-stu-id="2da55-110">Figure 1</span></span>  
> <span data-ttu-id="2da55-111">Representación visual de la memoria</span><span class="sxs-lookup"><span data-stu-id="2da55-111">Visual representation of memory</span></span>  
>![Representación visual de la memoria][ImageThinkGraph]  

<span data-ttu-id="2da55-113">Un objeto puede contener memoria de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="2da55-113">An object may hold memory in two ways:</span></span>  

*   <span data-ttu-id="2da55-114">Directamente por el objeto.</span><span class="sxs-lookup"><span data-stu-id="2da55-114">Directly by the object.</span></span>  
*   <span data-ttu-id="2da55-115">De forma implícita, reteniendo referencias a otros objetos y, por lo tanto, impidiendo que un recolector de elementos no utilizados \ (**GC** por abreviado \) lo elimine automáticamente.</span><span class="sxs-lookup"><span data-stu-id="2da55-115">Implicitly by holding references to other objects, and therefore preventing those objects from being automatically disposed by a garbage collector \(**GC** for short\).</span></span>  

<span data-ttu-id="2da55-116">Al trabajar con el [Panel memoria][DevtoolsMemoryProblemsHeapSnapshots] en DevTools \ (una herramienta para investigar los problemas de memoria que se encuentran en "memoria" \), puede que tenga que mirar algunas columnas de información diferentes.</span><span class="sxs-lookup"><span data-stu-id="2da55-116">When working with the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots] in DevTools \(a tool for investigating memory issues found under "Memory"\), you may find yourself looking at a few different columns of information.</span></span>  <span data-ttu-id="2da55-117">Dos que destaquen son **el tamaño superficial** y **el tamaño guardado**, pero ¿qué representa?</span><span class="sxs-lookup"><span data-stu-id="2da55-117">Two that stand out are **Shallow Size** and **Retained Size**, but what do these represent?</span></span>  

> ##### <span data-ttu-id="2da55-118">Figura 2</span><span class="sxs-lookup"><span data-stu-id="2da55-118">Figure 2</span></span>  
> <span data-ttu-id="2da55-119">Tamaño Shallow y retenido</span><span class="sxs-lookup"><span data-stu-id="2da55-119">Shallow and Retained Size</span></span>  
>![Tamaño Shallow y retenido][ImageShallowRetained]  

### <span data-ttu-id="2da55-121">Tamaño superficial</span><span class="sxs-lookup"><span data-stu-id="2da55-121">Shallow size</span></span>  

<span data-ttu-id="2da55-122">Este es el tamaño de la memoria que posee el objeto.</span><span class="sxs-lookup"><span data-stu-id="2da55-122">This is the size of memory that is held by the object.</span></span>  

<span data-ttu-id="2da55-123">Los objetos típicos de JavaScript tienen memoria reservada para su descripción y para almacenar valores inmediatos.</span><span class="sxs-lookup"><span data-stu-id="2da55-123">Typical JavaScript objects have some memory reserved for their description and for storing immediate values.</span></span>  <span data-ttu-id="2da55-124">Normalmente, solo las matrices y cadenas pueden tener un tamaño superficial significativo.</span><span class="sxs-lookup"><span data-stu-id="2da55-124">Usually, only arrays and strings are able to have a significant shallow size.</span></span>  <span data-ttu-id="2da55-125">Sin embargo, las cadenas y las matrices externas suelen tener su almacenamiento principal en la memoria del representador y solo exponen un pequeño objeto contenedor en el montón de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2da55-125">However, strings and external arrays often have their main storage in renderer memory, exposing only a small wrapper object on the JavaScript heap.</span></span>  

<span data-ttu-id="2da55-126">La memoria del representador es toda la memoria del proceso donde se representa una página inspeccionada: memoria nativa + JS memoria del montón de la memoria del montón Page + JS de todos los trabajadores dedicados iniciados por la página.</span><span class="sxs-lookup"><span data-stu-id="2da55-126">Renderer memory is all memory of the process where an inspected page is rendered: native memory + JS heap memory of the page + JS heap memory of all dedicated workers started by the page.</span></span>  <span data-ttu-id="2da55-127">Sin embargo, incluso un objeto pequeño puede contener una gran cantidad de memoria indirectamente, impidiendo que otros objetos sean eliminados por el proceso de recolección automática de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="2da55-127">Nevertheless, even a small object is able to hold a large amount of memory indirectly, by preventing other objects from being disposed of by the automatic garbage collection process.</span></span>  

### <span data-ttu-id="2da55-128">Tamaño retenido</span><span class="sxs-lookup"><span data-stu-id="2da55-128">Retained size</span></span>  

<span data-ttu-id="2da55-129">Este es el tamaño de memoria que se libera una vez que se elimina el objeto junto con los objetos dependientes que se han inaccesible desde las **raíces del recolector de elementos no utilizados** \ (raíces de GC \).</span><span class="sxs-lookup"><span data-stu-id="2da55-129">This is the size of memory that is freed once the object is deleted along with the dependent objects that were made unreachable from **Garbage Collector roots** \(GC roots\) .</span></span>  

<span data-ttu-id="2da55-130">Las **raíces del recolector de elementos no utilizados** \ (raíces de GC \) se componen de **identificadores** que se crean \ (local o global \) cuando se hace referencia desde código nativo a un objeto de JavaScript fuera de V8.</span><span class="sxs-lookup"><span data-stu-id="2da55-130">**Garbage Collector roots** \(GC roots\) are made up of **handles** that are created \(either local or global\) when making a reference from native code to a JavaScript object outside of V8.</span></span>  <span data-ttu-id="2da55-131">Puede encontrar todos los identificadores de ese tipo dentro de una instantánea de montones, en **raíces de GC**  >  **Handle scope** , **GC roots**  >  **identificadores globales**de ámbito y raíz del GC.</span><span class="sxs-lookup"><span data-stu-id="2da55-131">All such handles may be found within a heap snapshot under **GC roots** > **Handle scope** and **GC roots** > **Global handles**.</span></span>  <span data-ttu-id="2da55-132">La descripción de los identificadores de esta documentación sin profundizar en los detalles de la implementación del explorador puede resultar confusa.</span><span class="sxs-lookup"><span data-stu-id="2da55-132">Describing the handles in this documentation without diving into details of the browser implementation may be confusing.</span></span>  <span data-ttu-id="2da55-133">Tanto las raíces del recopilador de elementos no usados (GC) como los identificadores no son algo de lo que necesita preocuparse.</span><span class="sxs-lookup"><span data-stu-id="2da55-133">Both Garbage Collector (GC) roots and the handles are not something you need to worry about.</span></span>  

<span data-ttu-id="2da55-134">Hay una gran cantidad de raíces de GC internas, la mayoría de las cuales no son interesantes para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="2da55-134">There are lots of internal GC roots, most of which are not interesting for the users.</span></span>  <span data-ttu-id="2da55-135">Desde el punto de vista de las aplicaciones existen siguientes tipos de raíces.</span><span class="sxs-lookup"><span data-stu-id="2da55-135">From the applications standpoint there are following kinds of roots.</span></span>  

*   <span data-ttu-id="2da55-136">Objeto global Window \ (en cada iframe \).</span><span class="sxs-lookup"><span data-stu-id="2da55-136">Window global object \(in each iframe\).</span></span>  <span data-ttu-id="2da55-137">Hay un campo Distance en las instantáneas de montones, que es el número de referencias de propiedad en la ruta de retención más corta de la ventana.</span><span class="sxs-lookup"><span data-stu-id="2da55-137">There is a distance field in the heap snapshots which is the number of property references on the shortest retaining path from the window.</span></span>  
*   <span data-ttu-id="2da55-138">Árbol DOM de documento compuesto de todos los nodos DOM nativos a los que se puede atravesar el documento.</span><span class="sxs-lookup"><span data-stu-id="2da55-138">Document DOM tree consisting of all native DOM nodes reachable by traversing the document.</span></span>  <span data-ttu-id="2da55-139">Es posible que no todos los nodos tengan contenedores JS, pero si un nodo tiene un contenedor, estará activo mientras el documento está activo.</span><span class="sxs-lookup"><span data-stu-id="2da55-139">Not all of the nodes may have JS wrappers but if a node has a wrapper, it is alive while the document is alive.</span></span>  
*   <span data-ttu-id="2da55-140">A veces, el contexto del depurador puede conservar los objetos en el panel **orígenes** y la **consola** \ (por ejemplo, después de la evaluación de consola \).</span><span class="sxs-lookup"><span data-stu-id="2da55-140">Sometimes objects may be retained by the debugger context in the **Sources** panel and the **Console** \(for example after Console evaluation\).</span></span>  <span data-ttu-id="2da55-141">Crear instantáneas de montones con un panel de **consola** desactivado y sin puntos de interrupción activos en el depurador del panel **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="2da55-141">Create heap snapshots with a cleared **Console** panel and no active breakpoints in the debugger in the **Sources** panel.</span></span>

>[!TIP]
> <span data-ttu-id="2da55-142">Para borrar el panel de la **consola** , ejecute `clear()` y desactive los puntos de interrupción en el panel **fuentes** antes de tomar una instantánea del montón en el [Panel memoria][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="2da55-142">Clear the **Console** panel by running `clear()` and deactivate breakpoints in the **Sources** panel before taking a heap snapshot in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>

<span data-ttu-id="2da55-143">El gráfico de memoria se inicia con una raíz, que puede ser el `window` objeto del explorador o el `Global` objeto de un módulo node. js.</span><span class="sxs-lookup"><span data-stu-id="2da55-143">The memory graph starts with a root, which may be the `window` object of the browser or the `Global` object of a Node.js module.</span></span>  <span data-ttu-id="2da55-144">No controla cómo se recolecta este objeto raíz (M.c. d).</span><span class="sxs-lookup"><span data-stu-id="2da55-144">You do not control how this root object is garbage collected (GCd).</span></span>  

> ##### <span data-ttu-id="2da55-145">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="2da55-145">Figure 3</span></span>  
> <span data-ttu-id="2da55-146">No se puede controlar cómo se ha recolectado el objeto raíz \ (M.c. d \).</span><span class="sxs-lookup"><span data-stu-id="2da55-146">You are not able to control how the root object is garbage collected \(GCd\).</span></span>  
>![No puede controlar cómo se ha recolectado el objeto raíz (M.c. d).][ImageDontControl]  

<span data-ttu-id="2da55-148">Lo que no sea accesible desde la raíz obtiene el recolector de elementos no usados \ (M.c. d \).</span><span class="sxs-lookup"><span data-stu-id="2da55-148">Whatever is not reachable from the root gets garbage collected \(GCd\).</span></span>  

> [!NOTE]
> <span data-ttu-id="2da55-149">Las columnas [tamaño superficial](#shallow-size) y [tamaño retenido](#retained-size) representan datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="2da55-149">Both the [Shallow size](#shallow-size) and [Retained size](#retained-size) columns represent data in bytes.</span></span>  

## <span data-ttu-id="2da55-150">Árbol de objetos reteniendo</span><span class="sxs-lookup"><span data-stu-id="2da55-150">Objects retaining tree</span></span>  

<span data-ttu-id="2da55-151">El montón es una red de objetos interconectados.</span><span class="sxs-lookup"><span data-stu-id="2da55-151">The heap is a network of interconnected objects.</span></span>  <span data-ttu-id="2da55-152">En el mundo matemático, esta estructura se denomina gráfico **o gráfico de memoria** .</span><span class="sxs-lookup"><span data-stu-id="2da55-152">In the mathematical world, this structure is called a **graph** or memory graph.</span></span>  <span data-ttu-id="2da55-153">Un gráfico se crea a partir de los **nodos** conectados por medio de **bordes**, de los cuales se proporcionan etiquetas.</span><span class="sxs-lookup"><span data-stu-id="2da55-153">A graph is constructed from **nodes** connected by means of **edges**, both of which are given labels.</span></span>  

*   <span data-ttu-id="2da55-154">Los **nodos** \ (u **objetos**\) se etiquetan con el nombre de la función **constructora** que se usó para crearlos.</span><span class="sxs-lookup"><span data-stu-id="2da55-154">**Nodes**  \(or **objects**\) are labelled using the name of the **constructor** function that was used to build them.</span></span>  
*   <span data-ttu-id="2da55-155">Los **bordes** se etiquetan con los nombres de **las propiedades**.</span><span class="sxs-lookup"><span data-stu-id="2da55-155">**Edges**  are labelled using the names of **properties**.</span></span>  

<span data-ttu-id="2da55-156">Obtenga información sobre [Cómo grabar un perfil con el generador de perfiles del montón][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="2da55-156">Learn [how to record a profile using the Heap Profiler][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="2da55-157">Algunas de las cosas atractivas que puede ver en el registro de instantáneas de montones en el [Panel memoria][DevtoolsMemoryProblemsHeapSnapshots] de la [figura 4](#figure-4) son la distancia: la distancia desde la raíz del recolector de elementos no utilizados \ (GC \).</span><span class="sxs-lookup"><span data-stu-id="2da55-157">Some of the eye-catching things that you may see in the Heap Snapshot recording in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots] in [Figure 4](#figure-4) include distance: the distance from the Garbage Collector \(GC\) root.</span></span>  <span data-ttu-id="2da55-158">Si casi todos los objetos del mismo tipo se encuentran a la misma distancia y algunos están a una mayor distancia, es algo que vale la pena investigar.</span><span class="sxs-lookup"><span data-stu-id="2da55-158">If almost all the objects of the same type are at the same distance, and a few are at a bigger distance, that is something worth investigating.</span></span>  

> ##### <span data-ttu-id="2da55-159">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="2da55-159">Figure 4</span></span>  
> <span data-ttu-id="2da55-160">Distancia desde la raíz</span><span class="sxs-lookup"><span data-stu-id="2da55-160">Distance from root</span></span>  
>![Distancia desde la raíz][ImageRoot]  

## <span data-ttu-id="2da55-162">Dominators</span><span class="sxs-lookup"><span data-stu-id="2da55-162">Dominators</span></span>  

<span data-ttu-id="2da55-163">Los objetos Dominator se componen de una estructura de árbol, ya que cada objeto tiene exactamente un Dominator.</span><span class="sxs-lookup"><span data-stu-id="2da55-163">Dominator objects are comprised of a tree structure because each object has exactly one dominator.</span></span>  <span data-ttu-id="2da55-164">Un Dominator de un objeto puede carecer de referencias directas a un objeto que domina; es decir, el árbol de Dominator no es un árbol de expansión del gráfico.</span><span class="sxs-lookup"><span data-stu-id="2da55-164">A dominator of an object may lack direct references to an object it dominates; that is, the tree of the dominator is not a spanning tree of the graph.</span></span>  

<span data-ttu-id="2da55-165">En la [figura 5](#figure-5):</span><span class="sxs-lookup"><span data-stu-id="2da55-165">In [Figure 5](#figure-5):</span></span>  

*   <span data-ttu-id="2da55-166">El nodo 1 domina el nodo 2</span><span class="sxs-lookup"><span data-stu-id="2da55-166">Node 1 dominates node 2</span></span>  
*   <span data-ttu-id="2da55-167">El nodo 2 predomina los nodos 3, 4 y 6</span><span class="sxs-lookup"><span data-stu-id="2da55-167">Node 2 dominates nodes 3, 4 and 6</span></span>  
*   <span data-ttu-id="2da55-168">Nodo 3 domina el nodo 5</span><span class="sxs-lookup"><span data-stu-id="2da55-168">Node 3 dominates node 5</span></span>  
*   <span data-ttu-id="2da55-169">El nodo 5 domina el nodo 8</span><span class="sxs-lookup"><span data-stu-id="2da55-169">Node 5 dominates node 8</span></span>  
*   <span data-ttu-id="2da55-170">El nodo 6 domina el nodo 7</span><span class="sxs-lookup"><span data-stu-id="2da55-170">Node 6 dominates node 7</span></span>  

> ##### <span data-ttu-id="2da55-171">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="2da55-171">Figure 5</span></span>  
> <span data-ttu-id="2da55-172">Estructura de árbol de Dominator</span><span class="sxs-lookup"><span data-stu-id="2da55-172">Dominator tree structure</span></span>  
>![Estructura de árbol de Dominator][ImageDominatorsSpanning]  

<span data-ttu-id="2da55-174">En la [figura 6](#figure-6), nodo `#3` es el Dominator de `#10` , pero `#7` también existe en cada ruta simple desde el recolector de elementos no utilizados \ (GC \) a `#10` .</span><span class="sxs-lookup"><span data-stu-id="2da55-174">In [Figure 6](#figure-6), node `#3` is the dominator of `#10`, but `#7` also exists in every simple path from Garbage Collector \(GC\) to `#10`.</span></span>  <span data-ttu-id="2da55-175">Por lo tanto, un objeto B es un Dominator de un objeto A si B existe en cada ruta simple de la raíz al objeto a.</span><span class="sxs-lookup"><span data-stu-id="2da55-175">Therefore, an object B is a dominator of an object A if B exists in every simple path from the root to the object A.</span></span>  

> ##### <span data-ttu-id="2da55-176">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="2da55-176">Figure 6</span></span>  
> <span data-ttu-id="2da55-177">Ilustración Dominator animada</span><span class="sxs-lookup"><span data-stu-id="2da55-177">Animated dominator illustration</span></span>  
>![Ilustración Dominator animada][ImageDominators]  

## <span data-ttu-id="2da55-179">Características específicas de V8</span><span class="sxs-lookup"><span data-stu-id="2da55-179">V8 specifics</span></span>  

<span data-ttu-id="2da55-180">Al generar perfiles de memoria, resulta útil comprender por qué las instantáneas de montones se ven de una determinada manera.</span><span class="sxs-lookup"><span data-stu-id="2da55-180">When profiling memory, it is helpful to understand why heap snapshots look a certain way.</span></span>  <span data-ttu-id="2da55-181">En esta sección se describen algunos temas relacionados con la memoria que corresponden específicamente a la **máquina virtual de JavaScript V8** \ (V8 VM o VM \).</span><span class="sxs-lookup"><span data-stu-id="2da55-181">This section describes some memory-related topics specifically corresponding to the **V8 JavaScript virtual machine** \(V8 VM or VM\).</span></span>  

### <span data-ttu-id="2da55-182">Representación de objeto de JavaScript</span><span class="sxs-lookup"><span data-stu-id="2da55-182">JavaScript object representation</span></span>  

<span data-ttu-id="2da55-183">Hay tres tipos primitivos:</span><span class="sxs-lookup"><span data-stu-id="2da55-183">There are three primitive types:</span></span>  

*   <span data-ttu-id="2da55-184">Números \ (por ejemplo `3.14159...` \)</span><span class="sxs-lookup"><span data-stu-id="2da55-184">Numbers \(for example `3.14159...`\)</span></span>  
*   <span data-ttu-id="2da55-185">Booleanos \ ( `true` o `false` \)</span><span class="sxs-lookup"><span data-stu-id="2da55-185">Booleans \(`true` or `false`\)</span></span>  
*   <span data-ttu-id="2da55-186">Cadenas \ (por ejemplo `"Werner Heisenberg"` \)</span><span class="sxs-lookup"><span data-stu-id="2da55-186">Strings \(for example `"Werner Heisenberg"`\)</span></span>  

<span data-ttu-id="2da55-187">Los tipos primitivos no pueden hacer referencia a otros valores y siempre son hojas o nodos de terminación.</span><span class="sxs-lookup"><span data-stu-id="2da55-187">Primitives are not able to reference other values and are always leafs or terminating nodes.</span></span>  

<span data-ttu-id="2da55-188">**Los números** se pueden almacenar como:</span><span class="sxs-lookup"><span data-stu-id="2da55-188">**Numbers** are able to be stored as either:</span></span>  

*   <span data-ttu-id="2da55-189">valores enteros de 31 bits inmediatos denominados **pequeños enteros** \ (**SMI**s \) o</span><span class="sxs-lookup"><span data-stu-id="2da55-189">an immediate 31-bit integer values called **small integers** \(**SMI**s\), or</span></span>  
*   <span data-ttu-id="2da55-190">objetos Heap, denominados **números de montones**.</span><span class="sxs-lookup"><span data-stu-id="2da55-190">heap objects, referred to as **heap numbers**.</span></span> <span data-ttu-id="2da55-191">Los números de montones se usan para almacenar valores que no se ajustan al formulario de SMI, como valores **Double**o cuando es necesario aplicar la **conversión boxing**a un valor, como establecer propiedades en él.</span><span class="sxs-lookup"><span data-stu-id="2da55-191">Heap numbers are used for storing values that do not fit into the SMI form, such as **doubles**, or when a value needs to be **boxed**, such as setting properties on it.</span></span>  

<span data-ttu-id="2da55-192">Las **cadenas** pueden almacenarse en:</span><span class="sxs-lookup"><span data-stu-id="2da55-192">**Strings** are able to be stored in either:</span></span>  

*   <span data-ttu-id="2da55-193">el **montón de VM**o</span><span class="sxs-lookup"><span data-stu-id="2da55-193">the **VM heap**, or</span></span>
*   <span data-ttu-id="2da55-194">externamente en la **memoria del representador**.</span><span class="sxs-lookup"><span data-stu-id="2da55-194">externally in the **memory of the renderer**.</span></span>  <span data-ttu-id="2da55-195">Se crea un **objeto contenedor** y se usa para acceder a un almacenamiento externo donde, por ejemplo, se almacenan los orígenes de script y otro contenido que se recibe de la web, en lugar de copiarse en el montón de la VM.</span><span class="sxs-lookup"><span data-stu-id="2da55-195">A **wrapper object** is created and used for accessing external storage where, for example, script sources and other content that is received from the Web is stored, rather than copied onto the VM heap.</span></span>

<span data-ttu-id="2da55-196">La memoria de los nuevos objetos de JavaScript se asigna desde un montón de JavaScript dedicado \ (o **montón VM**\).</span><span class="sxs-lookup"><span data-stu-id="2da55-196">Memory for new JavaScript objects is allocated from a dedicated JavaScript heap \(or **VM heap**\).</span></span>  <span data-ttu-id="2da55-197">Estos objetos se administran mediante el recolector de elementos no utilizados en V8 y, por lo tanto, permanecen activos siempre que haya al menos una referencia fuerte.</span><span class="sxs-lookup"><span data-stu-id="2da55-197">These objects are managed by the garbage collector in V8 and therefore, stay alive as long as there is at least one strong reference to them.</span></span>  

<span data-ttu-id="2da55-198">Todo lo que no esté en el montón de JavaScript se denomina **objeto nativo**.</span><span class="sxs-lookup"><span data-stu-id="2da55-198">Anything not in the JavaScript heap is called a **native object**.</span></span>  <span data-ttu-id="2da55-199">Los objetos nativos, a diferencia de los objetos Heap, no se administran en el recolector de elementos no utilizados de la V8 durante su período de duración, y solo se puede acceder a ellos desde JavaScript mediante el objeto wrapper de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2da55-199">Native objects, in contrast to heap objects, are not managed by the V8 garbage collector throughout their lifetime, and may only be accessed from JavaScript using the JavaScript wrapper object.</span></span>  

<span data-ttu-id="2da55-200">La **cadena cons** es un objeto que consta de pares de cadenas almacenadas y, a continuación, se unen, y es un resultado de una concatenación.</span><span class="sxs-lookup"><span data-stu-id="2da55-200">**Cons string** is an object that consists of pairs of strings stored and then joined, and is a result of concatenation.</span></span>  <span data-ttu-id="2da55-201">La Unión del contenido de la **cadena cons** solo se produce cuando es necesario.</span><span class="sxs-lookup"><span data-stu-id="2da55-201">The joining of the **cons string** contents occurs only as needed.</span></span> <span data-ttu-id="2da55-202">Un ejemplo sería cuando es necesario construir una subcadena de una cadena combinada.</span><span class="sxs-lookup"><span data-stu-id="2da55-202">An example would be when a substring of a joined string needs to be constructed.</span></span>

<span data-ttu-id="2da55-203">Por ejemplo, si concatena `a` y `b` , obtiene una cadena `(a, b)` que representa el resultado de la concatenación.</span><span class="sxs-lookup"><span data-stu-id="2da55-203">For example, if you concatenate `a` and `b`, you get a string `(a, b)` which represents the result of concatenation.</span></span>  <span data-ttu-id="2da55-204">Si más adelante se ha concatenado `d` con ese resultado, obtendrá otra **cadena de cons**: `((a, b, d)` .</span><span class="sxs-lookup"><span data-stu-id="2da55-204">If you later concatenated `d` with that result, you get another **cons string**: `((a, b, d)`.</span></span>  

<span data-ttu-id="2da55-205">**Matriz** es un objeto con teclas numéricas.</span><span class="sxs-lookup"><span data-stu-id="2da55-205">**Array** is an object with numeric keys.</span></span> <span data-ttu-id="2da55-206">Las **matrices** se usan ampliamente en la máquina virtual V8 para almacenar grandes cantidades de datos.</span><span class="sxs-lookup"><span data-stu-id="2da55-206">**Arrays** are used extensively in the V8 VM for storing large amounts of data.</span></span> <span data-ttu-id="2da55-207">Se realiza una copia de seguridad de los conjuntos de pares clave-valor, como diccionarios, por **matriz**.</span><span class="sxs-lookup"><span data-stu-id="2da55-207">Sets of key-value pairs, like dictionaries, are backed up by **arrays**.</span></span>  

<span data-ttu-id="2da55-208">Un objeto de JavaScript típico se almacena como uno de los dos tipos de **matriz** :</span><span class="sxs-lookup"><span data-stu-id="2da55-208">A typical JavaScript object is stored as only one of two **array** types:</span></span>  

*   <span data-ttu-id="2da55-209">propiedades con nombre y</span><span class="sxs-lookup"><span data-stu-id="2da55-209">named properties, and</span></span>  
*   <span data-ttu-id="2da55-210">elementos numéricos</span><span class="sxs-lookup"><span data-stu-id="2da55-210">numeric elements</span></span>  

<span data-ttu-id="2da55-211">Cuando hay un pequeño número de propiedades, las propiedades se almacenan internamente en el objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2da55-211">When there are a small number of properties, the properties are stored internally in the JavaScript object.</span></span>  

<span data-ttu-id="2da55-212">**Map** es un objeto que describe el tipo de objeto que es y el diseño.</span><span class="sxs-lookup"><span data-stu-id="2da55-212">**Map** is an object that describes both the kind of object it is and the layout.</span></span> <span data-ttu-id="2da55-213">Por ejemplo, los mapas se usan para describir jerarquías de objetos implícitas para un [acceso rápido a la propiedad][V8FastProperties].</span><span class="sxs-lookup"><span data-stu-id="2da55-213">For example, maps are used to describe implicit object hierarchies for [fast property access][V8FastProperties].</span></span>  


### <span data-ttu-id="2da55-214">Grupos de objetos</span><span class="sxs-lookup"><span data-stu-id="2da55-214">Object groups</span></span>  

<span data-ttu-id="2da55-215">Cada grupo de **objetos nativos** está compuesto de objetos que contienen referencias mutuas entre sí.</span><span class="sxs-lookup"><span data-stu-id="2da55-215">Each **native objects** group is made up of objects that hold mutual references to each other.</span></span>  <span data-ttu-id="2da55-216">Considere, por ejemplo, un subárbol DOM en el que cada nodo tiene un vínculo al elemento primario relativo y vincula al siguiente elemento secundario y siguiente, de modo que se forme un gráfico conectado.</span><span class="sxs-lookup"><span data-stu-id="2da55-216">Consider, for example, a DOM subtree where every node has a link to the relative parent and links to the next child and next sibling, thus forming a connected graph.</span></span>  <span data-ttu-id="2da55-217">Tenga en cuenta que los objetos nativos no se representan en el montón de JavaScript, es decir, los objetos nativos tienen el tamaño cero.</span><span class="sxs-lookup"><span data-stu-id="2da55-217">Note that native objects are not represented in the JavaScript heap  —  that is why native objects have zero size.</span></span> <span data-ttu-id="2da55-218">En su lugar, se crean objetos contenedores.</span><span class="sxs-lookup"><span data-stu-id="2da55-218">Instead, wrapper objects are created.</span></span>  

<span data-ttu-id="2da55-219">Cada objeto contenedor mantiene una referencia al objeto nativo correspondiente, para redirigir comandos a él.</span><span class="sxs-lookup"><span data-stu-id="2da55-219">Each wrapper object holds a reference to the corresponding native object, for redirecting commands to it.</span></span>  <span data-ttu-id="2da55-220">A su vez, un grupo de objetos contiene objetos contenedores.</span><span class="sxs-lookup"><span data-stu-id="2da55-220">In turn, an object group holds wrapper objects.</span></span>  <span data-ttu-id="2da55-221">Sin embargo, esto no crea un ciclo que no se puede cobrar porque el recolector de elementos no usados \ (GC \) es lo suficientemente inteligente para liberar los grupos de objetos cuyos contenedores ya no se hacen referencia.</span><span class="sxs-lookup"><span data-stu-id="2da55-221">However, this does not create an uncollectable cycle, as Garbage Collector \(GC\) is smart enough to release object groups whose wrappers are no longer referenced.</span></span> <span data-ttu-id="2da55-222">Pero olvidar liberar un único contenedor alberga todo el grupo y los contenedores asociados.</span><span class="sxs-lookup"><span data-stu-id="2da55-222">But forgetting to release a single wrapper holds the whole group and associated wrappers.</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageThinkGraph]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-thinkgraph.msft.png "Ilustración 1: representación visual de la memoria"  
[ImageShallowRetained]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-shallow-retained.msft.png "Ilustración 2: tamaño Shallow y retenido"  
[ImageDontControl]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-dontcontrol.msft.png "Ilustración 3: no puede controlar cómo se recolecta el objeto raíz (M.c. d)."  
[ImageRoot]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-root.msft.png "Ilustración 4: distancia desde la raíz"  
[ImageDominatorsSpanning]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-dominatorsspanning.msft.png "Ilustración 5: estructura de árbol de Dominator"  
[ImageDominators]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-dominators.msft.gif "Ilustración 6: ilustración de Dominator animada"  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: /microsoft-edge/devtools-guide-chromium/media/memory-problems/heap-snapshots "/microsoft-edge/devtools-guide-chromium/media/memory-problems"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Propiedades rápidas de V8 | V8"  

> [!NOTE]
> <span data-ttu-id="2da55-231">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2da55-231">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2da55-232">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) y está creada por [Meggin Kearney][MegginKearney] \ (editor técnico \).</span><span class="sxs-lookup"><span data-stu-id="2da55-232">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2da55-234">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2da55-234">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney

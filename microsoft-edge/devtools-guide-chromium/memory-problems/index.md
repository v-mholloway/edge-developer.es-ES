---
description: Obtenga información sobre cómo usar Microsoft Edge y DevTools para encontrar problemas de memoria que afecten al rendimiento de la página, como pérdidas de memoria, distensión de memoria y recolecciones de elementos no utilizados frecuentes.
title: Solucionar problemas de memoria
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 3b2405d23dd6ee349484c9ba66d195e3ed12144b
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565032"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->
# <a name="fix-memory-problems"></a><span data-ttu-id="dd799-104">Solucionar problemas de memoria</span><span class="sxs-lookup"><span data-stu-id="dd799-104">Fix memory problems</span></span>  

<span data-ttu-id="dd799-105">Obtenga información sobre cómo usar Microsoft Edge y DevTools para encontrar problemas de memoria que afecten al rendimiento de la página, como pérdidas de memoria, distensión de memoria y recolecciones de elementos no utilizados frecuentes.</span><span class="sxs-lookup"><span data-stu-id="dd799-105">Learn how to use Microsoft Edge and DevTools to find memory issues that affect page performance, including memory leaks, memory bloat, and frequent garbage collections.</span></span>  

### <a name="summary"></a><span data-ttu-id="dd799-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="dd799-106">Summary</span></span>  

*   <span data-ttu-id="dd799-107">Descubra la cantidad de memoria que la página está usando actualmente con el administrador de tareas Microsoft Edge explorador.</span><span class="sxs-lookup"><span data-stu-id="dd799-107">Find out how much memory your page is currently using with the Microsoft Edge Browser Task Manager.</span></span>  
*   <span data-ttu-id="dd799-108">Visualice el uso de memoria con el tiempo con el panel **Memoria.**</span><span class="sxs-lookup"><span data-stu-id="dd799-108">Visualize memory usage over time with the **Memory** panel.</span></span>  
*   <span data-ttu-id="dd799-109">Identifique los árboles DOM desasociados \(una causa común de pérdidas de memoria\) con **instantánea de montón**.</span><span class="sxs-lookup"><span data-stu-id="dd799-109">Identify detached DOM trees \(a common cause of memory leaks\) with **Heap snapshot**.</span></span>  
*   <span data-ttu-id="dd799-110">Descubra cuándo se asigna nueva memoria en el montón de JavaScript \(JS heap\) con instrumentación de asignación **en la escala de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="dd799-110">Find out when new memory is being allocated in your JavaScript heap \(JS heap\) with **Allocation instrumentation on timeline**.</span></span>  

## <a name="overview"></a><span data-ttu-id="dd799-111">Introducción</span><span class="sxs-lookup"><span data-stu-id="dd799-111">Overview</span></span>  

<span data-ttu-id="dd799-112">En el sentido del modelo de rendimiento **RAIL,** el foco de sus esfuerzos de rendimiento deben ser los usuarios.</span><span class="sxs-lookup"><span data-stu-id="dd799-112">In the spirit of the **RAIL** performance model, the focus of your performance efforts should be your users.</span></span>  

<!--todo: add RAIL section when available  -->  

<span data-ttu-id="dd799-113">Los problemas de memoria son importantes porque los usuarios suelen percibirlo.</span><span class="sxs-lookup"><span data-stu-id="dd799-113">Memory issues are important because they are often perceivable by users.</span></span>  <span data-ttu-id="dd799-114">Los usuarios pueden percibir problemas de memoria de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="dd799-114">Users may perceive memory issues in the following ways:</span></span>  

*   <span data-ttu-id="dd799-115">**El rendimiento de una página empeora progresivamente con el tiempo**.</span><span class="sxs-lookup"><span data-stu-id="dd799-115">**The performance of a page gets progressively worse over time**.</span></span>  <span data-ttu-id="dd799-116">Esto es posiblemente un síntoma de una pérdida de memoria.</span><span class="sxs-lookup"><span data-stu-id="dd799-116">This is possibly a symptom of a memory leak.</span></span>  <span data-ttu-id="dd799-117">Una pérdida de memoria es cuando un error en la página hace que la página use cada vez más memoria con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="dd799-117">A memory leak is when a bug in the page causes the page to progressively use more and more memory over time.</span></span>  
*   <span data-ttu-id="dd799-118">**El rendimiento de una página es coherentemente malo.**</span><span class="sxs-lookup"><span data-stu-id="dd799-118">**The performance of a page is consistently bad**.</span></span>  <span data-ttu-id="dd799-119">Este es posiblemente un síntoma del exceso de memoria.</span><span class="sxs-lookup"><span data-stu-id="dd799-119">This is possibly a symptom of memory bloat.</span></span>  <span data-ttu-id="dd799-120">El exceso de memoria es cuando una página usa más memoria de la necesaria para una velocidad de página óptima.</span><span class="sxs-lookup"><span data-stu-id="dd799-120">Memory bloat is when a page uses more memory than is necessary for optimal page speed.</span></span>  
*   <span data-ttu-id="dd799-121">**El rendimiento de una página se retrasa o parece pausar con frecuencia**.</span><span class="sxs-lookup"><span data-stu-id="dd799-121">**The performance of a page is delayed or appears to pause frequently**.</span></span>  <span data-ttu-id="dd799-122">Este es posiblemente un síntoma de las recolecciones de elementos no utilizados frecuentes.</span><span class="sxs-lookup"><span data-stu-id="dd799-122">This is possibly a symptom of frequent garbage collections.</span></span>  <span data-ttu-id="dd799-123">La recolección de elementos no utilizados es cuando el explorador recupera memoria.</span><span class="sxs-lookup"><span data-stu-id="dd799-123">Garbage collection is when the browser reclaims memory.</span></span>  <span data-ttu-id="dd799-124">El explorador decide cuándo sucede esto.</span><span class="sxs-lookup"><span data-stu-id="dd799-124">The browser decides when this happens.</span></span>  <span data-ttu-id="dd799-125">Durante las colecciones, se pausa todo el script que se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="dd799-125">During collections, all script running is paused.</span></span>  <span data-ttu-id="dd799-126">Por lo tanto, si el explorador está recopilando muchos elementos no utilizados, el tiempo de ejecución del script se va a pausar mucho.</span><span class="sxs-lookup"><span data-stu-id="dd799-126">So if the browser is garbage collecting a lot, script runtime is going to get paused a lot.</span></span>  

### <a name="memory-bloat-how-much-is-too-much"></a><span data-ttu-id="dd799-127">Bloat de memoria: ¿cuánto es "demasiado"?</span><span class="sxs-lookup"><span data-stu-id="dd799-127">Memory bloat: how much is "too much"?</span></span>  

<span data-ttu-id="dd799-128">Una pérdida de memoria es fácil de definir.</span><span class="sxs-lookup"><span data-stu-id="dd799-128">A memory leak is easy to define.</span></span>  <span data-ttu-id="dd799-129">Si un sitio usa cada vez más memoria de forma progresiva, tendrá una pérdida.</span><span class="sxs-lookup"><span data-stu-id="dd799-129">If a site is progressively using more and more memory, then you have a leak.</span></span>  <span data-ttu-id="dd799-130">Pero la bloat de memoria es un poco más difícil de anclar.</span><span class="sxs-lookup"><span data-stu-id="dd799-130">But memory bloat is a bit harder to pin down.</span></span>  <span data-ttu-id="dd799-131">¿Qué califica como "usar demasiada memoria"?</span><span class="sxs-lookup"><span data-stu-id="dd799-131">What qualifies as "using too much memory"?</span></span>  

<span data-ttu-id="dd799-132">Aquí no hay números duros, ya que los distintos dispositivos y exploradores tienen capacidades diferentes.</span><span class="sxs-lookup"><span data-stu-id="dd799-132">There are no hard numbers here, because different devices and browsers have different capabilities.</span></span>  <span data-ttu-id="dd799-133">La misma página que se ejecuta sin problemas en un smartphone de gama alta puede bloquearse en un smartphone de gama baja.</span><span class="sxs-lookup"><span data-stu-id="dd799-133">The same page that runs smoothly on a high-end smartphone may crash on a low-end smartphone.</span></span>  

<span data-ttu-id="dd799-134">La clave aquí es usar el modelo RAIL y centrarse en los usuarios.</span><span class="sxs-lookup"><span data-stu-id="dd799-134">The key here is to use the RAIL model and focus on your users.</span></span>  <span data-ttu-id="dd799-135">Descubra qué dispositivos son populares entre los usuarios y, a continuación, pruebe la página en esos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="dd799-135">Find out what devices are popular with your users, and then test out your page on those devices.</span></span>  <span data-ttu-id="dd799-136">Si la experiencia es coherentemente mala, es posible que la página supere las capacidades de memoria de esos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="dd799-136">If the experience is consistently bad, the page may be exceeding the memory capabilities of those devices.</span></span>  

## <a name="monitor-memory-use-in-realtime-with-the-microsoft-edge-browser-task-manager"></a><span data-ttu-id="dd799-137">Supervisar el uso de memoria en tiempo real con el Administrador de tareas Microsoft Edge explorador</span><span class="sxs-lookup"><span data-stu-id="dd799-137">Monitor memory use in realtime with the Microsoft Edge Browser Task Manager</span></span>  

<span data-ttu-id="dd799-138">Use el administrador Microsoft Edge de tareas del explorador como punto de partida para la investigación de problemas de memoria.</span><span class="sxs-lookup"><span data-stu-id="dd799-138">Use the Microsoft Edge Browser Task Manager as a starting point to your memory issue investigation.</span></span>  <span data-ttu-id="dd799-139">El Microsoft Edge de tareas del explorador es un monitor en tiempo real que le indica la cantidad de memoria que está usando actualmente una página.</span><span class="sxs-lookup"><span data-stu-id="dd799-139">The Microsoft Edge Browser Task Manager is a realtime monitor that tells you how much memory a page is currently using.</span></span>  

1.  <span data-ttu-id="dd799-140">Seleccione o navegue hasta el menú Microsoft Edge principal y elija Más herramientas Administrador de tareas del explorador para abrir Microsoft Edge administrador de `Shift` + `Esc` tareas \*\*\*\*  >  \*\*\*\* del explorador.</span><span class="sxs-lookup"><span data-stu-id="dd799-140">Select `Shift`+`Esc` or navigate to the Microsoft Edge main menu and choose **More tools** > **Browser Task Manager** to open the Microsoft Edge Browser Task Manager.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png" alt-text="Abrir el administrador Microsoft Edge de tareas del explorador" lightbox="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png":::
       <span data-ttu-id="dd799-142">Figura 1: Abrir el administrador de tareas Microsoft Edge explorador</span><span class="sxs-lookup"><span data-stu-id="dd799-142">Figure 1:  Opening the Microsoft Edge Browser Task Manager</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="dd799-143">Mantenga el mouse en el encabezado de la tabla del Administrador de tareas del explorador Microsoft Edge, abra el menú contextual \(hacer clic con el botón secundario\) y habilite **la memoria de JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="dd799-143">Hover on the table header of the Microsoft Edge Browser Task Manager, open the contextual menu \(right-click\), and enable **JavaScript memory**.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png" alt-text="Habilitar memoria de JavaScript" lightbox="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png":::
       <span data-ttu-id="dd799-145">Figura 2: Habilitar memoria de JavaScript</span><span class="sxs-lookup"><span data-stu-id="dd799-145">Figure 2:  Enable JavaScript memory</span></span>  
    :::image-end:::  
    
<span data-ttu-id="dd799-146">Estas dos columnas le dicen cosas diferentes acerca de cómo usa la memoria la página.</span><span class="sxs-lookup"><span data-stu-id="dd799-146">These two columns tell you different things about how your page is using memory.</span></span>  

*   <span data-ttu-id="dd799-147">La **columna Memoria** representa la memoria nativa.</span><span class="sxs-lookup"><span data-stu-id="dd799-147">The **Memory** column represents native memory.</span></span>  <span data-ttu-id="dd799-148">Los nodos DOM se almacenan en la memoria nativa.</span><span class="sxs-lookup"><span data-stu-id="dd799-148">DOM nodes are stored in native memory.</span></span>  <span data-ttu-id="dd799-149">Si este valor aumenta, se crean nodos DOM.</span><span class="sxs-lookup"><span data-stu-id="dd799-149">If this value is increasing, DOM nodes are getting created.</span></span>  
*   <span data-ttu-id="dd799-150">La **columna Memoria de JavaScript** representa el montón js.</span><span class="sxs-lookup"><span data-stu-id="dd799-150">The **JavaScript Memory** column represents the JS heap.</span></span>  <span data-ttu-id="dd799-151">Esta columna contiene dos valores.</span><span class="sxs-lookup"><span data-stu-id="dd799-151">This column contains two values.</span></span>  <span data-ttu-id="dd799-152">El valor que le interesa es el número vivo \(el número entre paréntesis\).</span><span class="sxs-lookup"><span data-stu-id="dd799-152">The value you are interested in is the live number \(the number in parentheses\).</span></span>  <span data-ttu-id="dd799-153">El número directo representa la cantidad de memoria que usan los objetos accesibles en la página.</span><span class="sxs-lookup"><span data-stu-id="dd799-153">The live number represents how much memory the reachable objects on your page are using.</span></span>  <span data-ttu-id="dd799-154">Si este número aumenta, se crean objetos nuevos o los objetos existentes están creciendo.</span><span class="sxs-lookup"><span data-stu-id="dd799-154">If this number is increasing, either new objects are being created, or the existing objects are growing.</span></span>  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <a name="visualize-memory-leaks-with-performance-panel"></a><span data-ttu-id="dd799-155">Visualizar pérdidas de memoria con el panel Rendimiento</span><span class="sxs-lookup"><span data-stu-id="dd799-155">Visualize memory leaks with Performance panel</span></span>  

<span data-ttu-id="dd799-156">También puede usar el panel Rendimiento como otro punto de partida de la investigación.</span><span class="sxs-lookup"><span data-stu-id="dd799-156">You may also use the Performance panel as another starting point in your investigation.</span></span>  <span data-ttu-id="dd799-157">El panel Rendimiento le ayuda a visualizar el uso de memoria de una página a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="dd799-157">The Performance panel helps you visualize the memory use of a page over time.</span></span>  

1.  <span data-ttu-id="dd799-158">Abra el panel **Rendimiento** en DevTools.</span><span class="sxs-lookup"><span data-stu-id="dd799-158">Open the **Performance** panel on DevTools.</span></span>  
1.  <span data-ttu-id="dd799-159">Active la casilla **Memoria.**</span><span class="sxs-lookup"><span data-stu-id="dd799-159">Enable the **Memory** checkbox.</span></span>  
1.  <span data-ttu-id="dd799-160">[Realizar una grabación][DevtoolsEvaluatePerformanceReferenceRecord].</span><span class="sxs-lookup"><span data-stu-id="dd799-160">[Make a recording][DevtoolsEvaluatePerformanceReferenceRecord].</span></span>  

> [!TIP]
> <span data-ttu-id="dd799-161">Es una buena práctica iniciar y finalizar la grabación con una recolección de elementos no utilizados forzada.</span><span class="sxs-lookup"><span data-stu-id="dd799-161">It is a good practice to start and end your recording with a forced garbage collection.</span></span>  <span data-ttu-id="dd799-162">Para forzar la recolección de elementos no utilizados, elija el botón **de** recolección de elementos no utilizados de la fuerza ![ de ][ImageForceGarbageCollectionIcon] recolección de elementos no utilizados durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="dd799-162">To force garbage collection, choose the **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button while recording.</span></span>  

<span data-ttu-id="dd799-163">Para demostrar las grabaciones de memoria, tenga en cuenta el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="dd799-163">To demonstrate memory recordings, consider the code below:</span></span>  

```javascript
var x = [];
function grow() {
    for (var i = 0; i < 10000; i++) {
        document.body.appendChild(document.createElement('div'));
    }
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="dd799-164">Cada vez que se elige el botón al que se hace referencia en el código, se anexan diez mil nodos al cuerpo del documento y se inserta una cadena de un millón de caracteres en `div` `x` la `x` matriz.</span><span class="sxs-lookup"><span data-stu-id="dd799-164">Every time that the button referenced in the code is chosen, ten thousand `div` nodes are appended to the document body, and a string of one million `x` characters is pushed onto the `x` array.</span></span>  <span data-ttu-id="dd799-165">Al ejecutar el ejemplo de código anterior, se produce una grabación en **el** panel Rendimiento como la siguiente figura.</span><span class="sxs-lookup"><span data-stu-id="dd799-165">Running the previous code sample produces a recording in the **Performance** panel like the following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-1-performance-memory.msft.png" alt-text="Crecimiento sencillo" lightbox="../media/memory-problems-glitch-example-1-performance-memory.msft.png":::
   <span data-ttu-id="dd799-167">Figura 3: Crecimiento simple</span><span class="sxs-lookup"><span data-stu-id="dd799-167">Figure 3:  Simple growth</span></span>  
:::image-end:::  

<span data-ttu-id="dd799-168">En primer lugar, una explicación de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="dd799-168">First, an explanation of the user interface.</span></span>  <span data-ttu-id="dd799-169">El **gráfico HEAP** del panel **Información general** \(debajo de **NET**\) representa el montón de JS.</span><span class="sxs-lookup"><span data-stu-id="dd799-169">The **HEAP** graph in the **Overview** pane \(below **NET**\) represents the JS heap.</span></span>  <span data-ttu-id="dd799-170">Debajo del **panel** Información general se encuentra **el panel** Contador.</span><span class="sxs-lookup"><span data-stu-id="dd799-170">Below the **Overview** pane is the **Counter** pane.</span></span>  <span data-ttu-id="dd799-171">El uso de memoria se desglosa mediante el montón de JS \(igual que el gráfico **HEAP** en el **panel** Información general\), documentos, nodos DOM, escuchas y memoria GPU.</span><span class="sxs-lookup"><span data-stu-id="dd799-171">The memory usage is broken down by JS heap \(same as **HEAP** graph in the **Overview** pane\), documents, DOM nodes, listeners, and GPU memory.</span></span>  <span data-ttu-id="dd799-172">Desactiva una casilla para ocultarla del gráfico.</span><span class="sxs-lookup"><span data-stu-id="dd799-172">Turn off a checkbox to hide it from the graph.</span></span>  

<span data-ttu-id="dd799-173">Ahora, un análisis del código en comparación con la figura anterior.</span><span class="sxs-lookup"><span data-stu-id="dd799-173">Now, an analysis of the code compared with the previous figure.</span></span>  <span data-ttu-id="dd799-174">Si revisa el contador de nodos \(el gráfico verde\), coincide limpiamente con el código.</span><span class="sxs-lookup"><span data-stu-id="dd799-174">If you review the node counter \(the green graph\), it matches up cleanly with the code.</span></span>  <span data-ttu-id="dd799-175">El número de nodos aumenta en pasos discretos.</span><span class="sxs-lookup"><span data-stu-id="dd799-175">The node count increases in discrete steps.</span></span>  <span data-ttu-id="dd799-176">Puede suponer que cada aumento en el número de nodos es una llamada a `grow()` .</span><span class="sxs-lookup"><span data-stu-id="dd799-176">You may presume that each increase in the node count is a call to `grow()`.</span></span>  <span data-ttu-id="dd799-177">El gráfico de montón JS \(el gráfico azul\) no es tan sencillo.</span><span class="sxs-lookup"><span data-stu-id="dd799-177">The JS heap graph \(the blue graph\) is not as straightforward.</span></span>  <span data-ttu-id="dd799-178">De acuerdo con los procedimientos recomendados, la primera \*\*\*\* inmersión es en realidad una recolección forzada de elementos no utilizados \(elija el botón de recolección de elementos no utilizados fuerza ![ de ][ImageForceGarbageCollectionIcon] recolección\).</span><span class="sxs-lookup"><span data-stu-id="dd799-178">In keeping with best practices, the first dip is actually a forced garbage collection \(choose the  **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button\).</span></span>  <span data-ttu-id="dd799-179">A medida que avanza la grabación, se muestran los picos de tamaño del montón de JS.</span><span class="sxs-lookup"><span data-stu-id="dd799-179">As the recording progresses, the JS heap size spikes are displayed.</span></span>  <span data-ttu-id="dd799-180">Esto es natural y esperado: el código JavaScript está creando los nodos DOM en cada botón que elija y haciendo mucho trabajo cuando crea la cadena de un millón de caracteres.</span><span class="sxs-lookup"><span data-stu-id="dd799-180">This is natural and expected:  the JavaScript code is creating the DOM nodes on every button you choose and doing a lot of work when it creates the string of one million characters.</span></span>  <span data-ttu-id="dd799-181">La clave aquí es el hecho de que el montón JS termina más alto de lo que empezó \(el "principio" aquí es el punto después de la recolección forzada de elementos no utilizados\).</span><span class="sxs-lookup"><span data-stu-id="dd799-181">The key thing here is the fact that the JS heap ends higher than it began \(the "beginning" here being the point after the forced garbage collection\).</span></span>  <span data-ttu-id="dd799-182">En el mundo real, si ves este patrón de aumento del tamaño del montón de JS o el tamaño de nodo, puede definir potencialmente una pérdida de memoria.</span><span class="sxs-lookup"><span data-stu-id="dd799-182">In the real world, if you saw this pattern of increasing JS heap size or node size, it may potentially define a memory leak.</span></span>  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <a name="discover-detached-dom-tree-memory-leaks-with-heap-snapshots"></a><span data-ttu-id="dd799-183">Detectar pérdidas de memoria de árbol DOM desasociadas con instantáneas de montón</span><span class="sxs-lookup"><span data-stu-id="dd799-183">Discover detached DOM tree memory leaks with Heap Snapshots</span></span>  

<span data-ttu-id="dd799-184">Un nodo DOM solo se recopila cuando no hay referencias al nodo desde el árbol DOM o el código JavaScript que se ejecuta en la página.</span><span class="sxs-lookup"><span data-stu-id="dd799-184">A DOM node is only garbage collected when there are no references to the node from either the DOM tree or JavaScript code running on the page.</span></span>  <span data-ttu-id="dd799-185">Se dice que un nodo se "desasocia" cuando se quita del árbol DOM, pero algún JavaScript todavía hace referencia a él.</span><span class="sxs-lookup"><span data-stu-id="dd799-185">A node is said to be "detached" when it is removed from the DOM tree but some JavaScript still references it.</span></span>  <span data-ttu-id="dd799-186">Los nodos DOM separados son una causa común de pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="dd799-186">Detached DOM nodes are a common cause of memory leaks.</span></span>  <span data-ttu-id="dd799-187">Esta sección le enseña a usar los perfiles de montón en DevTools para identificar nodos separados.</span><span class="sxs-lookup"><span data-stu-id="dd799-187">This section teaches you how to use the heap profilers in DevTools to identify detached nodes.</span></span>  

<span data-ttu-id="dd799-188">Este es un ejemplo sencillo de nodos DOM separados.</span><span class="sxs-lookup"><span data-stu-id="dd799-188">Here is a simple example of detached DOM nodes.</span></span>  

```javascript
var detachedTree;

function create() {
    var ul = document.createElement('ul');
    for (var i = 0; i < 10; i++) {
        var li = document.createElement('li');
        ul.appendChild(li);
    }
    detachedTree = ul;
}
document.getElementById('create').addEventListener('click', create);
```  

<span data-ttu-id="dd799-189">Al elegir el botón al que se hace referencia en el código, se crea un `ul` nodo con diez `li` secundarios.</span><span class="sxs-lookup"><span data-stu-id="dd799-189">Choosing the button referenced in the code creates a `ul` node with ten `li` children.</span></span>  <span data-ttu-id="dd799-190">El código hace referencia a los nodos, pero no existen en el árbol DOM, por lo que cada uno se desasocia.</span><span class="sxs-lookup"><span data-stu-id="dd799-190">The nodes are referenced by the code but do not exist in the DOM tree, so each is detached.</span></span>  

<span data-ttu-id="dd799-191">Las instantáneas de montón son una forma de identificar nodos separados.</span><span class="sxs-lookup"><span data-stu-id="dd799-191">Heap snapshots are one way to identify detached nodes.</span></span>  <span data-ttu-id="dd799-192">Como su nombre indica, las instantáneas de montón muestran cómo se distribuye la memoria entre los objetos JS y los nodos DOM de la página en el momento de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="dd799-192">As the name implies, heap snapshots show you how memory is distributed among the JS objects and DOM nodes for your page at the point of time of the snapshot.</span></span>  

<span data-ttu-id="dd799-193">Para crear una instantánea, abra DevTools y vaya al **panel** Memoria, elija el botón de **radio** Instantánea de montón > botón **Tomar instantánea.**</span><span class="sxs-lookup"><span data-stu-id="dd799-193">To create a snapshot, open DevTools and navigate to the **Memory** panel, choose the **Heap snapshot** radio button > **Take snapshot** button.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png" alt-text="Tomar instantánea de montón" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png":::
   <span data-ttu-id="dd799-195">Figura 4: Tomar instantánea de montón</span><span class="sxs-lookup"><span data-stu-id="dd799-195">Figure 4:  Take heap snapshot</span></span>  
:::image-end:::  

<span data-ttu-id="dd799-196">La instantánea puede tardar algún tiempo en procesarse y cargarse.</span><span class="sxs-lookup"><span data-stu-id="dd799-196">The snapshot may take some time to process and load.</span></span>  <span data-ttu-id="dd799-197">Una vez finalizada, selecciónelo en el panel izquierdo \(denominado **INSTANTÁNEAS DE HEAP**\).</span><span class="sxs-lookup"><span data-stu-id="dd799-197">After it is finished, select it from the left-hand panel \(named **HEAP SNAPSHOTS**\).</span></span>  

<span data-ttu-id="dd799-198">Escriba `Detached` en el cuadro de texto **Filtro** de clase para buscar árboles DOM desasociados.</span><span class="sxs-lookup"><span data-stu-id="dd799-198">Type `Detached` in the **Class filter** textbox to search for detached DOM trees.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png" alt-text="Filtrado de nodos separados" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png":::
   <span data-ttu-id="dd799-200">Figura 5: Filtrado de nodos separados</span><span class="sxs-lookup"><span data-stu-id="dd799-200">Figure 5:  Filtering for detached nodes</span></span>  
:::image-end:::  

<span data-ttu-id="dd799-201">Expanda los quilates para investigar un árbol separado.</span><span class="sxs-lookup"><span data-stu-id="dd799-201">Expand the carats to investigate a detached tree.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png" alt-text="Investigar árbol desasociado" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png":::
   <span data-ttu-id="dd799-203">Figura 6: Investigar árbol desasociado</span><span class="sxs-lookup"><span data-stu-id="dd799-203">Figure 6:  Investigating detached tree</span></span>  
:::image-end:::  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

<span data-ttu-id="dd799-204">Elija un nodo para investigarlo más a fondo.</span><span class="sxs-lookup"><span data-stu-id="dd799-204">Choose a node to investigate it further.</span></span>  <span data-ttu-id="dd799-205">En el **panel Objetos,** puede revisar más información sobre el código que hace referencia a él.</span><span class="sxs-lookup"><span data-stu-id="dd799-205">In the **Objects** pane, you may review more information about the code that is referencing it.</span></span>  <span data-ttu-id="dd799-206">Por ejemplo, en la figura siguiente, la `detachedNodes` variable hace referencia al nodo.</span><span class="sxs-lookup"><span data-stu-id="dd799-206">For example, in the following figure, the `detachedNodes` variable is referencing the node.</span></span>  <span data-ttu-id="dd799-207">Para corregir la pérdida de memoria en particular, debe estudiar el código que usa la variable y asegurarse de que la referencia al nodo se quita cuando ya no es `detachedUNode` necesaria.</span><span class="sxs-lookup"><span data-stu-id="dd799-207">To fix the particular memory leak, you should study the code that uses the `detachedUNode` variable and ensure that the reference to the node is removed when it is no longer needed.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png" alt-text="Investigar un nodo" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png":::
   <span data-ttu-id="dd799-209">Figura 7: Investigación de un nodo</span><span class="sxs-lookup"><span data-stu-id="dd799-209">Figure 7:  Investigating a node</span></span>  
:::image-end:::  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <a name="identify-js-heap-memory-leaks-with-allocation-instrumentation-on-timeline"></a><span data-ttu-id="dd799-210">Identificar pérdidas de memoria de montón de JS con instrumentación de asignación en la escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="dd799-210">Identify JS heap memory leaks with Allocation instrumentation on timeline</span></span>  

<span data-ttu-id="dd799-211">**La instrumentación de** asignación en la escala de tiempo es otra herramienta que puede ayudarle a realizar un seguimiento de las pérdidas de memoria en el montón de JS.</span><span class="sxs-lookup"><span data-stu-id="dd799-211">**Allocation instrumentation on timeline** is another tool that may help you track down memory leaks in your JS heap.</span></span>  

<span data-ttu-id="dd799-212">Demostrar **instrumentación de asignación en la escala de**  tiempo con el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="dd799-212">Demonstrate **Allocation instrumentation on timeline**  using the following code.</span></span>  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="dd799-213">Cada vez que se inserta el botón al que se hace referencia en el código, se agrega una cadena de un millón de caracteres a la `x` matriz.</span><span class="sxs-lookup"><span data-stu-id="dd799-213">Every time that the button referenced in the code is pushed, a string of one million characters is added to the `x` array.</span></span>  

<span data-ttu-id="dd799-214">Para grabar un instrumental de asignación en la escala de \*\*\*\* tiempo, abra DevTools, \*\*\*\* vaya al **panel** Memoria, elija el botón de radio \*\*\*\* Instrumentación de asignación en la escala de tiempo, elija el botón Inicio, realice la acción que sospeche que está causando la pérdida de memoria y, a continuación, elija el botón Detener la grabación del perfil de montón de almacenamiento dinámico cuando haya ![ ][ImageStopRecordingIcon] terminado.</span><span class="sxs-lookup"><span data-stu-id="dd799-214">To record an Allocation instrumentation on timeline, open DevTools, navigate to the **Memory** panel, choose the **Allocation instrumentation on timeline** radio button, choose the **Start** button, perform the action that you suspect is causing the memory leak, and then choose the **Stop recording heap profile** ![stop recording][ImageStopRecordingIcon] button when you are done.</span></span>  

<span data-ttu-id="dd799-215">Mientras graba, observe si las barras azules se muestran en la instrumentación de asignación en la escala de tiempo, como en la siguiente figura.</span><span class="sxs-lookup"><span data-stu-id="dd799-215">As you are recording, notice if any blue bars show up on the Allocation instrumentation on timeline, like in the following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png" alt-text="Nuevas asignaciones" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png":::
   <span data-ttu-id="dd799-217">Figura 8: Nuevas asignaciones</span><span class="sxs-lookup"><span data-stu-id="dd799-217">Figure 8:  New allocations</span></span>  
:::image-end:::  

<span data-ttu-id="dd799-218">Esas barras azules representan nuevas asignaciones de memoria.</span><span class="sxs-lookup"><span data-stu-id="dd799-218">Those blue bars represent new memory allocations.</span></span>  <span data-ttu-id="dd799-219">Esas nuevas asignaciones de memoria son sus candidatos para pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="dd799-219">Those new memory allocations are your candidates for memory leaks.</span></span>  <span data-ttu-id="dd799-220">Puede acercar una barra para filtrar el **panel Constructor** para mostrar solo los objetos que se asignaron durante el período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="dd799-220">You are able to zoom on a bar to filter the **Constructor** pane to only show objects that were allocated during the specified timeframe.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png" alt-text="Escala de tiempo de asignación ampliada" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png":::
   <span data-ttu-id="dd799-222">Figura 9: Escala de tiempo de asignación ampliada</span><span class="sxs-lookup"><span data-stu-id="dd799-222">Figure 9:  Zoomed allocation timeline</span></span>  
:::image-end:::  

<span data-ttu-id="dd799-223">Expanda el objeto y seleccione el valor para ver más detalles en el **panel** Objeto.</span><span class="sxs-lookup"><span data-stu-id="dd799-223">Expand the object and select the value to view more details in the **Object** pane.</span></span>  <span data-ttu-id="dd799-224">Por ejemplo, en la siguiente figura, en los detalles del objeto recién asignado indica que se asignó a la `x` variable en el `Window` ámbito.</span><span class="sxs-lookup"><span data-stu-id="dd799-224">For example, in the following figure, in the details of the newly allocated object indicates that it was allocated to the `x` variable in the `Window` scope.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png" alt-text="Detalles del objeto" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png":::
   <span data-ttu-id="dd799-226">Figura 10: Detalles del objeto</span><span class="sxs-lookup"><span data-stu-id="dd799-226">Figure 10:  Object details</span></span>  
:::image-end:::  

## <a name="investigate-memory-allocation-by-function"></a><span data-ttu-id="dd799-227">Investigar la asignación de memoria por función</span><span class="sxs-lookup"><span data-stu-id="dd799-227">Investigate memory allocation by function</span></span>  

<span data-ttu-id="dd799-228">Use el **tipo de generación** de perfiles de muestreo de asignación para ver la asignación de memoria mediante la función JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dd799-228">Use the **Allocation sampling** profiling type to view memory allocation by JavaScript function.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png" alt-text="Muestreo de asignación de registros" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png":::
   <span data-ttu-id="dd799-230">Figura 11: Muestreo de asignación de registros</span><span class="sxs-lookup"><span data-stu-id="dd799-230">Figure 11:  Record Allocation sampling</span></span>  
:::image-end:::  

1.  <span data-ttu-id="dd799-231">Elija el **botón de radio Asignación de** muestreo.</span><span class="sxs-lookup"><span data-stu-id="dd799-231">Choose the **Allocation sampling** radio button.</span></span>  <span data-ttu-id="dd799-232">Si hay un trabajador en la página, puede seleccionarlo como el destino de generación de perfiles mediante el menú desplegable situado junto al **botón** Inicio.</span><span class="sxs-lookup"><span data-stu-id="dd799-232">If there is a worker on the page, you are able to select that as the profiling target using the dropdown menu next to the **Start** button.</span></span>  
1.  <span data-ttu-id="dd799-233">Elija el **botón** Inicio.</span><span class="sxs-lookup"><span data-stu-id="dd799-233">Choose the **Start** button.</span></span>  
1.  <span data-ttu-id="dd799-234">Complete las acciones de la página web que desea investigar.</span><span class="sxs-lookup"><span data-stu-id="dd799-234">Complete the actions on the webpage which you want to investigate.</span></span>  
1.  <span data-ttu-id="dd799-235">Elija el **botón** Detener cuando haya terminado todas las acciones.</span><span class="sxs-lookup"><span data-stu-id="dd799-235">Choose the **Stop** button when you have finished all of your actions.</span></span>  

<span data-ttu-id="dd799-236">DevTools muestra un desglose de la asignación de memoria por función.</span><span class="sxs-lookup"><span data-stu-id="dd799-236">DevTools shows you a breakdown of memory allocation by function.</span></span>  <span data-ttu-id="dd799-237">La vista predeterminada es **Heavy (Bottom Up),** que muestra las funciones que asignaron la mayor cantidad de memoria en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="dd799-237">The default view is **Heavy (Bottom Up)**, which displays the functions that allocated the most memory at the top.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png" alt-text="Muestreo de asignación" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png":::
   <span data-ttu-id="dd799-239">Figura 12: Muestreo de asignación</span><span class="sxs-lookup"><span data-stu-id="dd799-239">Figure 12:  Allocation sampling</span></span>  
:::image-end:::  

## <a name="spot-frequent-garbage-collections"></a><span data-ttu-id="dd799-240">Detectar colecciones de elementos no utilizados frecuentes</span><span class="sxs-lookup"><span data-stu-id="dd799-240">Spot frequent garbage collections</span></span>  

<span data-ttu-id="dd799-241">Si la página parece pausar con frecuencia, es posible que tenga problemas de recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="dd799-241">If your page appears to pause frequently, then you may have garbage collection issues.</span></span>  

<span data-ttu-id="dd799-242">Puede usar el Administrador de tareas Microsoft Edge explorador o grabaciones de memoria de rendimiento para detectar la recolección de elementos no utilizados frecuente.</span><span class="sxs-lookup"><span data-stu-id="dd799-242">You are able to use either the Microsoft Edge Browser Task Manager or Performance memory recordings to spot frequent garbage collection.</span></span>  <span data-ttu-id="dd799-243">En el Administrador Microsoft Edge de tareas del \*\*\*\* explorador, los valores de memoria o memoria **de JavaScript** que aumentan y bajan con frecuencia representan la recolección de elementos no utilizados frecuente.</span><span class="sxs-lookup"><span data-stu-id="dd799-243">In the Microsoft Edge Browser Task Manager, frequently rising and falling **Memory** or **JavaScript Memory** values represent frequent garbage collection.</span></span>  <span data-ttu-id="dd799-244">En las grabaciones de rendimiento, los cambios frecuentes \(ascendentes y caídos\) en los gráficos de recuento de nodos o montón de JS indican una recolección de elementos no utilizados frecuente.</span><span class="sxs-lookup"><span data-stu-id="dd799-244">In Performance recordings, frequent changes \(rising and falling\) to the JS heap or node count graphs indicate frequent garbage collection.</span></span>  

<span data-ttu-id="dd799-245">Después de identificar el problema, puede \*\*\*\* usar un instrumental de asignación en la grabación de escala de tiempo para averiguar dónde se asigna la memoria y qué funciones están causando las asignaciones.</span><span class="sxs-lookup"><span data-stu-id="dd799-245">After you have identified the problem, you are able to use an **Allocation instrumentation on timeline** recording to find out where memory is being allocated and which functions are causing the allocations.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="dd799-246">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="dd799-246">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageForceGarbageCollectionIcon]: ../media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: ../media/stop-recording-icon.msft.png  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Rendimiento de registros: referencia de análisis de rendimiento"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> <span data-ttu-id="dd799-248">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dd799-248">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="dd799-249">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="dd799-249">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="dd799-251">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dd799-251">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

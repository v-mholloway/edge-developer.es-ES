---
description: Obtenga información sobre cómo usar Microsoft Edge y DevTools para buscar problemas de memoria que afecten al rendimiento de la página, como pérdidas de memoria, recarga de memoria y recolecciones de elementos no utilizados frecuentes.
title: Solucionar problemas de memoria
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 1d8a24fc360dc307471be33544c9c707736be06d
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125457"
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

# <span data-ttu-id="74ea9-104">Solucionar problemas de memoria</span><span class="sxs-lookup"><span data-stu-id="74ea9-104">Fix Memory Problems</span></span>  

<span data-ttu-id="74ea9-105">Obtenga información sobre cómo usar Microsoft Edge y DevTools para buscar problemas de memoria que afecten al rendimiento de la página, como pérdidas de memoria, recarga de memoria y recolecciones de elementos no utilizados frecuentes.</span><span class="sxs-lookup"><span data-stu-id="74ea9-105">Learn how to use Microsoft Edge and DevTools to find memory issues that affect page performance, including memory leaks, memory bloat, and frequent garbage collections.</span></span>  

### <span data-ttu-id="74ea9-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="74ea9-106">Summary</span></span>  

*   <span data-ttu-id="74ea9-107">Averigüe cuánta memoria está usando actualmente la página con el administrador de tareas del explorador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="74ea9-107">Find out how much memory your page is currently using with the Microsoft Edge Browser Task Manager.</span></span>  
*   <span data-ttu-id="74ea9-108">Visualice el uso de memoria a lo largo del tiempo con el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="74ea9-108">Visualize memory usage over time with the **Memory** panel.</span></span>  
*   <span data-ttu-id="74ea9-109">Identifique los árboles DOM desvinculados \ (una causa común de fugas de memoria \) con la **instantánea de montón**.</span><span class="sxs-lookup"><span data-stu-id="74ea9-109">Identify detached DOM trees \(a common cause of memory leaks\) with **Heap snapshot**.</span></span>  
*   <span data-ttu-id="74ea9-110">Averigüe cuándo se va a asignar una nueva memoria en el montón \ (JS heap \) con **instrumentación de asignación en la escala de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="74ea9-110">Find out when new memory is being allocated in your JavaScript heap \(JS heap\) with **Allocation instrumentation on timeline**.</span></span>  

## <span data-ttu-id="74ea9-111">Introducción</span><span class="sxs-lookup"><span data-stu-id="74ea9-111">Overview</span></span>  

<span data-ttu-id="74ea9-112">En el espíritu del modelo de rendimiento **ferroviario** , el enfoque de los esfuerzos de rendimiento debe ser los usuarios.</span><span class="sxs-lookup"><span data-stu-id="74ea9-112">In the spirit of the **RAIL** performance model, the focus of your performance efforts should be your users.</span></span>  

<!--todo: add RAIL section when available  -->  

<span data-ttu-id="74ea9-113">Los problemas de memoria son importantes porque a menudo son perceptibles para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="74ea9-113">Memory issues are important because they are often perceivable by users.</span></span>  <span data-ttu-id="74ea9-114">Los usuarios pueden percibir problemas de memoria de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="74ea9-114">Users may perceive memory issues in the following ways:</span></span>  

*   <span data-ttu-id="74ea9-115">**El rendimiento de una página se vuelve gradualmente con el tiempo**.</span><span class="sxs-lookup"><span data-stu-id="74ea9-115">**The performance of a page gets progressively worse over time**.</span></span>  <span data-ttu-id="74ea9-116">Esto es posiblemente un síntoma de pérdida de memoria.</span><span class="sxs-lookup"><span data-stu-id="74ea9-116">This is possibly a symptom of a memory leak.</span></span>  <span data-ttu-id="74ea9-117">Una pérdida de memoria se produce cuando un error en la página hace que la página use progresivamente más y más memoria a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="74ea9-117">A memory leak is when a bug in the page causes the page to progressively use more and more memory over time.</span></span>  
*   <span data-ttu-id="74ea9-118">**El rendimiento de una página es constantemente incorrecto**.</span><span class="sxs-lookup"><span data-stu-id="74ea9-118">**The performance of a page is consistently bad**.</span></span>  <span data-ttu-id="74ea9-119">Esto es posiblemente un síntoma de recarga de memoria.</span><span class="sxs-lookup"><span data-stu-id="74ea9-119">This is possibly a symptom of memory bloat.</span></span>  <span data-ttu-id="74ea9-120">El recargado de memoria es cuando una página utiliza más memoria de la necesaria para una velocidad de página óptima.</span><span class="sxs-lookup"><span data-stu-id="74ea9-120">Memory bloat is when a page uses more memory than is necessary for optimal page speed.</span></span>  
*   <span data-ttu-id="74ea9-121">**El rendimiento de una página se retrasa o parece que se pausa con frecuencia**.</span><span class="sxs-lookup"><span data-stu-id="74ea9-121">**The performance of a page is delayed or appears to pause frequently**.</span></span>  <span data-ttu-id="74ea9-122">Esto es posiblemente un síntoma de recolecciones de elementos no utilizados frecuentes.</span><span class="sxs-lookup"><span data-stu-id="74ea9-122">This is possibly a symptom of frequent garbage collections.</span></span>  <span data-ttu-id="74ea9-123">La recolección de elementos no utilizados se recolecta cuando el explorador reclama memoria.</span><span class="sxs-lookup"><span data-stu-id="74ea9-123">Garbage collection is when the browser reclaims memory.</span></span>  <span data-ttu-id="74ea9-124">El explorador decide cuando esto sucede.</span><span class="sxs-lookup"><span data-stu-id="74ea9-124">The browser decides when this happens.</span></span>  <span data-ttu-id="74ea9-125">Durante las colecciones, todo el script en ejecución está en pausa.</span><span class="sxs-lookup"><span data-stu-id="74ea9-125">During collections, all script running is paused.</span></span>  <span data-ttu-id="74ea9-126">Por lo tanto, si el explorador está recolectando un lote, el tiempo de ejecución de script se detendrá mucho.</span><span class="sxs-lookup"><span data-stu-id="74ea9-126">So if the browser is garbage collecting a lot, script runtime is going to get paused a lot.</span></span>  

### <span data-ttu-id="74ea9-127">Saturación de memoria: ¿Cuánto es "demasiado"?</span><span class="sxs-lookup"><span data-stu-id="74ea9-127">Memory bloat: how much is "too much"?</span></span>  

<span data-ttu-id="74ea9-128">Una pérdida de memoria es fácil de definir.</span><span class="sxs-lookup"><span data-stu-id="74ea9-128">A memory leak is easy to define.</span></span>  <span data-ttu-id="74ea9-129">Si un sitio está usando progresivamente más y más memoria, tendrá una fuga.</span><span class="sxs-lookup"><span data-stu-id="74ea9-129">If a site is progressively using more and more memory, then you have a leak.</span></span>  <span data-ttu-id="74ea9-130">Pero la saturación de la memoria es un poco más difícil de anclar.</span><span class="sxs-lookup"><span data-stu-id="74ea9-130">But memory bloat is a bit harder to pin down.</span></span>  <span data-ttu-id="74ea9-131">¿Qué califica como "usando demasiada memoria"?</span><span class="sxs-lookup"><span data-stu-id="74ea9-131">What qualifies as "using too much memory"?</span></span>  

<span data-ttu-id="74ea9-132">No hay números fuertes aquí, ya que los distintos dispositivos y exploradores tienen funciones diferentes.</span><span class="sxs-lookup"><span data-stu-id="74ea9-132">There are no hard numbers here, because different devices and browsers have different capabilities.</span></span>  <span data-ttu-id="74ea9-133">La misma página que se ejecuta sin problemas en smartphones de gama alta puede bloquearse en un smartphone de low-end.</span><span class="sxs-lookup"><span data-stu-id="74ea9-133">The same page that runs smoothly on a high-end smartphone may crash on a low-end smartphone.</span></span>  

<span data-ttu-id="74ea9-134">La clave aquí es usar el modelo de raíl y centrarse en los usuarios.</span><span class="sxs-lookup"><span data-stu-id="74ea9-134">The key here is to use the RAIL model and focus on your users.</span></span>  <span data-ttu-id="74ea9-135">Averigüe qué dispositivos son populares con los usuarios y, a continuación, pruebe la página en esos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="74ea9-135">Find out what devices are popular with your users, and then test out your page on those devices.</span></span>  <span data-ttu-id="74ea9-136">Si la experiencia es constantemente incorrecta, es posible que la página exceda las capacidades de memoria de esos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="74ea9-136">If the experience is consistently bad, the page may be exceeding the memory capabilities of those devices.</span></span>  

## <span data-ttu-id="74ea9-137">Supervisar el uso de memoria en tiempo real con el administrador de tareas del explorador Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="74ea9-137">Monitor memory use in realtime with the Microsoft Edge Browser Task Manager</span></span>  

<span data-ttu-id="74ea9-138">Use el administrador de tareas del explorador Microsoft Edge como punto de partida para la investigación de problemas de memoria.</span><span class="sxs-lookup"><span data-stu-id="74ea9-138">Use the Microsoft Edge Browser Task Manager as a starting point to your memory issue investigation.</span></span>  <span data-ttu-id="74ea9-139">El administrador de tareas del explorador Microsoft Edge es un monitor en tiempo real que indica la cantidad de memoria que está usando una página en ese momento.</span><span class="sxs-lookup"><span data-stu-id="74ea9-139">The Microsoft Edge Browser Task Manager is a realtime monitor that tells you how much memory a page is currently using.</span></span>  

1.  <span data-ttu-id="74ea9-140">Seleccione `Shift` + `Esc` o vaya al menú principal de Microsoft Edge y elija **más herramientas**  >  **Administrador de tareas del explorador** para abrir el administrador de tareas del explorador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="74ea9-140">Select `Shift`+`Esc` or go to the Microsoft Edge main menu and choose **More tools** > **Browser Task Manager** to open the Microsoft Edge Browser Task Manager.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png":::
       <span data-ttu-id="74ea9-142">Ilustración 1: abrir el administrador de tareas del explorador Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="74ea9-142">Figure 1:  Opening the Microsoft Edge Browser Task Manager</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="74ea9-143">Mantenga el mouse en el encabezado de tabla del administrador de tareas del explorador Microsoft Edge, abra el menú contextual \ (haga clic con el botón derecho \) y habilite la **memoria JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="74ea9-143">Hover on the table header of the Microsoft Edge Browser Task Manager, open the contextual menu \(right-click\), and enable **JavaScript memory**.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png":::
       <span data-ttu-id="74ea9-145">Ilustración 2: habilitar la memoria de JavaScript</span><span class="sxs-lookup"><span data-stu-id="74ea9-145">Figure 2:  Enable JavaScript memory</span></span>  
    :::image-end:::  
    
<span data-ttu-id="74ea9-146">Estas dos columnas le indican diferentes cosas sobre el uso de la memoria por la página.</span><span class="sxs-lookup"><span data-stu-id="74ea9-146">These two columns tell you different things about how your page is using memory.</span></span>  

*   <span data-ttu-id="74ea9-147">La columna **memoria** representa la memoria nativa.</span><span class="sxs-lookup"><span data-stu-id="74ea9-147">The **Memory** column represents native memory.</span></span>  <span data-ttu-id="74ea9-148">Los nodos DOM se almacenan en la memoria nativa.</span><span class="sxs-lookup"><span data-stu-id="74ea9-148">DOM nodes are stored in native memory.</span></span>  <span data-ttu-id="74ea9-149">Si este valor aumenta, se crean los nodos DOM.</span><span class="sxs-lookup"><span data-stu-id="74ea9-149">If this value is increasing, DOM nodes are getting created.</span></span>  
*   <span data-ttu-id="74ea9-150">La columna **memoria de JavaScript** representa el montón de JS.</span><span class="sxs-lookup"><span data-stu-id="74ea9-150">The **JavaScript Memory** column represents the JS heap.</span></span>  <span data-ttu-id="74ea9-151">Esta columna contiene dos valores.</span><span class="sxs-lookup"><span data-stu-id="74ea9-151">This column contains two values.</span></span>  <span data-ttu-id="74ea9-152">El valor que te interesa es el número en vivo \ (el número entre paréntesis \).</span><span class="sxs-lookup"><span data-stu-id="74ea9-152">The value you are interested in is the live number \(the number in parentheses\).</span></span>  <span data-ttu-id="74ea9-153">El número en vivo representa la cantidad de memoria que usan los objetos que se pueden encontrar en la página.</span><span class="sxs-lookup"><span data-stu-id="74ea9-153">The live number represents how much memory the reachable objects on your page are using.</span></span>  <span data-ttu-id="74ea9-154">Si este número está aumentando, se crean objetos nuevos o los objetos existentes crecen.</span><span class="sxs-lookup"><span data-stu-id="74ea9-154">If this number is increasing, either new objects are being created, or the existing objects are growing.</span></span>  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <span data-ttu-id="74ea9-155">Visualizar pérdidas de memoria con el panel rendimiento</span><span class="sxs-lookup"><span data-stu-id="74ea9-155">Visualize memory leaks with Performance panel</span></span>  

<span data-ttu-id="74ea9-156">También puede usar el panel rendimiento como otro punto de partida en su investigación.</span><span class="sxs-lookup"><span data-stu-id="74ea9-156">You may also use the Performance panel as another starting point in your investigation.</span></span>  <span data-ttu-id="74ea9-157">El panel rendimiento le ayuda a visualizar el uso de memoria de una página a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="74ea9-157">The Performance panel helps you visualize the memory use of a page over time.</span></span>  

1.  <span data-ttu-id="74ea9-158">Abra el panel de **rendimiento** en DevTools.</span><span class="sxs-lookup"><span data-stu-id="74ea9-158">Open the **Performance** panel on DevTools.</span></span>  
1.  <span data-ttu-id="74ea9-159">Active la casilla **memoria** .</span><span class="sxs-lookup"><span data-stu-id="74ea9-159">Enable the **Memory** checkbox.</span></span>  
1.  <span data-ttu-id="74ea9-160">[Hacer una grabación][DevtoolsEvaluatePerformanceReferenceRecord].</span><span class="sxs-lookup"><span data-stu-id="74ea9-160">[Make a recording][DevtoolsEvaluatePerformanceReferenceRecord].</span></span>  

> [!TIP]
> <span data-ttu-id="74ea9-161">Es recomendable iniciar y finalizar la grabación con una recolección de elementos no utilizados forzada.</span><span class="sxs-lookup"><span data-stu-id="74ea9-161">It is a good practice to start and end your recording with a forced garbage collection.</span></span>  <span data-ttu-id="74ea9-162">Seleccione el botón **recopilar** eliminación de elementos no usados ![ en la ][ImageForceGarbageCollectionIcon] grabación para forzar la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="74ea9-162">Select the **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button while recording to force garbage collection.</span></span>  

<span data-ttu-id="74ea9-163">Para hacer una demostración de las grabaciones de la memoria, considere el siguiente código:</span><span class="sxs-lookup"><span data-stu-id="74ea9-163">To demonstrate memory recordings, consider the code below:</span></span>  

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

<span data-ttu-id="74ea9-164">Cada vez que se presiona el botón al que se hace referencia en el código, `div` los nodos de 10000 se anexan al cuerpo del documento y se inserta una cadena de 1 millón `x` caracteres en la `x` matriz.</span><span class="sxs-lookup"><span data-stu-id="74ea9-164">Every time that the button referenced in the code is pressed, ten thousand `div` nodes are appended to the document body, and a string of one million `x` characters is pushed onto the `x` array.</span></span>  <span data-ttu-id="74ea9-165">La ejecución del ejemplo de código anterior produce una grabación en el panel de **rendimiento** como la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="74ea9-165">Running the previous code sample produces a recording in the **Performance** panel like the following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-1-performance-memory.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-1-performance-memory.msft.png":::
   <span data-ttu-id="74ea9-167">Ilustración 3: crecimiento simple</span><span class="sxs-lookup"><span data-stu-id="74ea9-167">Figure 3:  Simple growth</span></span>  
:::image-end:::  

<span data-ttu-id="74ea9-168">En primer lugar, una explicación de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="74ea9-168">First, an explanation of the user interface.</span></span>  <span data-ttu-id="74ea9-169">El gráfico de **montones** en el panel de **información general** \ (debajo de **net**\) representa el montón de JS.</span><span class="sxs-lookup"><span data-stu-id="74ea9-169">The **HEAP** graph in the **Overview** pane \(below **NET**\) represents the JS heap.</span></span>  <span data-ttu-id="74ea9-170">Debajo del panel de **información general** se encuentra el panel de **contador** .</span><span class="sxs-lookup"><span data-stu-id="74ea9-170">Below the **Overview** pane is the **Counter** pane.</span></span>  <span data-ttu-id="74ea9-171">Aquí puede ver el uso de memoria desglosado por montones de JS \ (igual al gráfico de **montón** en el panel de **información general** \), documentos, nodos DOM, oyentes y memoria de GPU.</span><span class="sxs-lookup"><span data-stu-id="74ea9-171">Here you are able to see memory usage broken down by JS heap \(same as **HEAP** graph in the **Overview** pane\), documents, DOM nodes, listeners, and GPU memory.</span></span>  <span data-ttu-id="74ea9-172">Al deshabilitar una casilla, la oculta del gráfico.</span><span class="sxs-lookup"><span data-stu-id="74ea9-172">Disabling a checkbox hides it from the graph.</span></span>  

<span data-ttu-id="74ea9-173">Ahora, un análisis del código comparado con la ilustración anterior.</span><span class="sxs-lookup"><span data-stu-id="74ea9-173">Now, an analysis of the code compared with the previous figure.</span></span>  <span data-ttu-id="74ea9-174">Si miras el contador de nodos \ (el gráfico verde \), podrás ver que coincide perfectamente con el código.</span><span class="sxs-lookup"><span data-stu-id="74ea9-174">If you look at the node counter \(the green graph\) you are able to see that it matches up cleanly with the code.</span></span>  <span data-ttu-id="74ea9-175">El número de nodos aumenta en pasos discretos.</span><span class="sxs-lookup"><span data-stu-id="74ea9-175">The node count increases in discrete steps.</span></span>  <span data-ttu-id="74ea9-176">Puede dar por supuesto que cada aumento en el recuento de nodos es una llamada a `grow()` .</span><span class="sxs-lookup"><span data-stu-id="74ea9-176">You may presume that each increase in the node count is a call to `grow()`.</span></span>  <span data-ttu-id="74ea9-177">El gráfico de montón JS \ (gráfico azul \) no es tan sencillo.</span><span class="sxs-lookup"><span data-stu-id="74ea9-177">The JS heap graph \(the blue graph\) is not as straightforward.</span></span>  <span data-ttu-id="74ea9-178">Siguiendo los procedimientos recomendados, la primera DIP es, en realidad, una recolección forzada de elementos no utilizados \ (que se consigue al  **presionar el** botón de recolección de elementos no ![ utilizados ][ImageForceGarbageCollectionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="74ea9-178">In keeping with best practices, the first dip is actually a forced garbage collection \(achieved by pressing the  **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button\).</span></span>  <span data-ttu-id="74ea9-179">A medida que la grabación se progrese, podrá ver que el tamaño del montón de JS es demasiado bajo.</span><span class="sxs-lookup"><span data-stu-id="74ea9-179">As the recording progresses you are able to see that the JS heap size spikes.</span></span>  <span data-ttu-id="74ea9-180">Esto es natural y se espera: el código JavaScript crea los nodos DOM en cada pulsador de botón y realiza una gran cantidad de trabajo cuando crea la cadena de 1 millón caracteres.</span><span class="sxs-lookup"><span data-stu-id="74ea9-180">This is natural and expected:  the JavaScript code is creating the DOM nodes on every button press and doing a lot of work when it creates the string of one million characters.</span></span>  <span data-ttu-id="74ea9-181">Lo fundamental aquí es el hecho de que el montón JS finaliza más de lo que comenzó \ (el "comienzo" aquí es el punto después de la recolección de elementos no utilizados forzada \).</span><span class="sxs-lookup"><span data-stu-id="74ea9-181">The key thing here is the fact that the JS heap ends higher than it began \(the "beginning" here being the point after the forced garbage collection\).</span></span>  <span data-ttu-id="74ea9-182">En el mundo real, si viera este patrón de aumento del tamaño de la pila de JS o del tamaño del nodo, puede definir potencialmente una pérdida de memoria.</span><span class="sxs-lookup"><span data-stu-id="74ea9-182">In the real world, if you saw this pattern of increasing JS heap size or node size, it may potentially define a memory leak.</span></span>  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <span data-ttu-id="74ea9-183">Descubrir pérdidas de memoria en el árbol de DOM desvinculadas con instantáneas de montones</span><span class="sxs-lookup"><span data-stu-id="74ea9-183">Discover detached DOM tree memory leaks with Heap Snapshots</span></span>  

<span data-ttu-id="74ea9-184">Un nodo DOM solo se recolecta como no utilizado cuando no hay ninguna referencia al nodo desde el árbol DOM o el código JavaScript que se ejecuta en la página.</span><span class="sxs-lookup"><span data-stu-id="74ea9-184">A DOM node is only garbage collected when there are no references to the node from either the DOM tree or JavaScript code running on the page.</span></span>  <span data-ttu-id="74ea9-185">Se dice que un nodo está "separado" cuando se quita del árbol DOM, pero algunos JavaScript siguen haciendo referencia a él.</span><span class="sxs-lookup"><span data-stu-id="74ea9-185">A node is said to be "detached" when it is removed from the DOM tree but some JavaScript still references it.</span></span>  <span data-ttu-id="74ea9-186">Los nodos DOM separados son una causa común de las pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="74ea9-186">Detached DOM nodes are a common cause of memory leaks.</span></span>  <span data-ttu-id="74ea9-187">En esta sección aprenderá a usar los perfilers de montones en DevTools para identificar los nodos desvinculados.</span><span class="sxs-lookup"><span data-stu-id="74ea9-187">This section teaches you how to use the heap profilers in DevTools to identify detached nodes.</span></span>  

<span data-ttu-id="74ea9-188">Este es un ejemplo sencillo de nodos DOM separados.</span><span class="sxs-lookup"><span data-stu-id="74ea9-188">Here is a simple example of detached DOM nodes.</span></span>  

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

<span data-ttu-id="74ea9-189">Al seleccionar el botón al que se hace referencia en el código, se crea un `ul` nodo con diez `li` elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="74ea9-189">Selecting the button referenced in the code creates a `ul` node with ten `li` children.</span></span>  <span data-ttu-id="74ea9-190">El código hace referencia a los nodos, pero no existen en el árbol DOM, por lo que se desasocian.</span><span class="sxs-lookup"><span data-stu-id="74ea9-190">The nodes are referenced by the code but do not exist in the DOM tree, so each is detached.</span></span>  

<span data-ttu-id="74ea9-191">Las instantáneas de montones son una manera de identificar los nodos desvinculados.</span><span class="sxs-lookup"><span data-stu-id="74ea9-191">Heap snapshots are one way to identify detached nodes.</span></span>  <span data-ttu-id="74ea9-192">Como su nombre indica, las instantáneas de montones muestran cómo se distribuye la memoria entre los objetos JS y los nodos DOM de la página en el punto de tiempo de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="74ea9-192">As the name implies, heap snapshots show you how memory is distributed among the JS objects and DOM nodes for your page at the point of time of the snapshot.</span></span>  

<span data-ttu-id="74ea9-193">Para crear una instantánea, abra DevTools y vaya al panel **memoria** , seleccione el botón de radio de la **instantánea de montones** y, después, presione el botón **tomar instantánea** .</span><span class="sxs-lookup"><span data-stu-id="74ea9-193">To create a snapshot, open DevTools and go to the **Memory** panel, select the **Heap snapshot** radio button, and then press the **Take snapshot** button.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png":::
   <span data-ttu-id="74ea9-195">Ilustración 4: tomar instantánea de montón</span><span class="sxs-lookup"><span data-stu-id="74ea9-195">Figure 4:  Take heap snapshot</span></span>  
:::image-end:::  

<span data-ttu-id="74ea9-196">La instantánea puede tardar algún tiempo en procesarse y cargarse.</span><span class="sxs-lookup"><span data-stu-id="74ea9-196">The snapshot may take some time to process and load.</span></span>  <span data-ttu-id="74ea9-197">Una vez que haya terminado, selecciónelo en el panel de la izquierda \ ( **instantáneas de montones**con nombre \).</span><span class="sxs-lookup"><span data-stu-id="74ea9-197">After it is finished, select it from the left-hand panel \(named **HEAP SNAPSHOTS**\).</span></span>  

<span data-ttu-id="74ea9-198">Escriba `Detached` el cuadro de texto **filtro de clase** para buscar árboles Dom desvinculados.</span><span class="sxs-lookup"><span data-stu-id="74ea9-198">Type `Detached` in the **Class filter** textbox to search for detached DOM trees.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png":::
   <span data-ttu-id="74ea9-200">Ilustración 5: filtrar por nodos desvinculados</span><span class="sxs-lookup"><span data-stu-id="74ea9-200">Figure 5:  Filtering for detached nodes</span></span>  
:::image-end:::  

<span data-ttu-id="74ea9-201">Expanda el carats para investigar un árbol desvinculado.</span><span class="sxs-lookup"><span data-stu-id="74ea9-201">Expand the carats to investigate a detached tree.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png":::
   <span data-ttu-id="74ea9-203">Ilustración 6: investigación de árboles desconectados</span><span class="sxs-lookup"><span data-stu-id="74ea9-203">Figure 6:  Investigating detached tree</span></span>  
:::image-end:::  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

<span data-ttu-id="74ea9-204">Seleccione un nodo para investigarlo más a la vez.</span><span class="sxs-lookup"><span data-stu-id="74ea9-204">Select a node to investigate it further.</span></span>  <span data-ttu-id="74ea9-205">En el panel **objetos** puede ver más información sobre el código que hace referencia.</span><span class="sxs-lookup"><span data-stu-id="74ea9-205">In the **Objects** pane you are able to see more information about the code that is referencing it.</span></span>  <span data-ttu-id="74ea9-206">Por ejemplo, en la siguiente ilustración se puede ver que la `detachedNodes` variable hace referencia al nodo.</span><span class="sxs-lookup"><span data-stu-id="74ea9-206">For example, in the following figure you are able to see that the `detachedNodes` variable is referencing the node.</span></span>  <span data-ttu-id="74ea9-207">Para corregir esta pérdida de memoria determinada, debe estudiar el código que usa la `detachedUNode` variable y asegurarse de que la referencia al nodo se quita cuando ya no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="74ea9-207">To fix this particular memory leak, you should study the code that uses the `detachedUNode` variable and ensure that the reference to the node is removed when it is no longer needed.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png":::
   <span data-ttu-id="74ea9-209">Ilustración 7: investigar un nodo</span><span class="sxs-lookup"><span data-stu-id="74ea9-209">Figure 7:  Investigating a node</span></span>  
:::image-end:::  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <span data-ttu-id="74ea9-210">Identificar pérdidas de memoria de montón JS con instrumentación de asignación en la escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="74ea9-210">Identify JS heap memory leaks with Allocation instrumentation on timeline</span></span>  

<span data-ttu-id="74ea9-211">La **instrumentación de asignación de la escala de tiempo** es otra herramienta que puede ayudarle a realizar un seguimiento de las pérdidas de memoria en el montón de JS.</span><span class="sxs-lookup"><span data-stu-id="74ea9-211">**Allocation instrumentation on timeline** is another tool that may help you track down memory leaks in your JS heap.</span></span>  

<span data-ttu-id="74ea9-212">Muestre la **instrumentación de asignación en la escala de tiempo**  con el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="74ea9-212">Demonstrate **Allocation instrumentation on timeline**  using the following code.</span></span>  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="74ea9-213">Cada vez que se inserta el botón al que se hace referencia en el código, se agrega una cadena de 1 millón caracteres a la `x` matriz.</span><span class="sxs-lookup"><span data-stu-id="74ea9-213">Every time that the button referenced in the code is pushed, a string of one million characters is added to the `x` array.</span></span>  

<span data-ttu-id="74ea9-214">Para grabar un instrumental de asignación en la escala de tiempo, abra DevTools, vaya al panel **memoria** , seleccione el botón **de opción instrumentación de asignación en la escala de tiempo** , presione el botón **Inicio** , realice la acción que sospecha que está causando la pérdida de memoria y, después, presione el botón Detener grabación del **montón de grabación** ![ cuando haya ][ImageStopRecordingIcon] terminado.</span><span class="sxs-lookup"><span data-stu-id="74ea9-214">To record an Allocation instrumentation on timeline, open DevTools, go to the **Memory** panel, select the **Allocation instrumentation on timeline** radio button, press the **Start** button, perform the action that you suspect is causing the memory leak, and then press the **Stop recording heap profile** ![stop recording][ImageStopRecordingIcon] button when you are done.</span></span>  

<span data-ttu-id="74ea9-215">Mientras graba, observe si en la línea de tiempo se muestran barras azules en la instrumentación de asignación, como en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="74ea9-215">As you are recording, notice if any blue bars show up on the Allocation instrumentation on timeline, like in the following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png":::
   <span data-ttu-id="74ea9-217">Ilustración 8: nuevas asignaciones</span><span class="sxs-lookup"><span data-stu-id="74ea9-217">Figure 8:  New allocations</span></span>  
:::image-end:::  

<span data-ttu-id="74ea9-218">Estas barras azules representan nuevas asignaciones de memoria.</span><span class="sxs-lookup"><span data-stu-id="74ea9-218">Those blue bars represent new memory allocations.</span></span>  <span data-ttu-id="74ea9-219">Estas nuevas asignaciones de memoria son sus candidatos para pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="74ea9-219">Those new memory allocations are your candidates for memory leaks.</span></span>  <span data-ttu-id="74ea9-220">Puede hacer zoom en una barra para filtrar el panel **constructor** y mostrar únicamente los objetos que se asignaron durante el período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="74ea9-220">You are able to zoom on a bar to filter the **Constructor** pane to only show objects that were allocated during the specified timeframe.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png":::
   <span data-ttu-id="74ea9-222">Ilustración 9: escala de tiempo de asignación ampliada</span><span class="sxs-lookup"><span data-stu-id="74ea9-222">Figure 9:  Zoomed allocation timeline</span></span>  
:::image-end:::  

<span data-ttu-id="74ea9-223">Expanda el objeto y seleccione el valor para ver más detalles en el panel de **objetos** .</span><span class="sxs-lookup"><span data-stu-id="74ea9-223">Expand the object and select the value to view more details in the **Object** pane.</span></span>  <span data-ttu-id="74ea9-224">Por ejemplo, en la siguiente ilustración, al ver los detalles del objeto que se acaba de asignar, debería poder ver que se asignó a la `x` variable en el `Window` ámbito.</span><span class="sxs-lookup"><span data-stu-id="74ea9-224">For example, in the following figure, by viewing the details of the object that was newly allocated, you should be able to see that it was allocated to the `x` variable in the `Window` scope.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png":::
   <span data-ttu-id="74ea9-226">Ilustración 10: detalles del objeto</span><span class="sxs-lookup"><span data-stu-id="74ea9-226">Figure 10:  Object details</span></span>  
:::image-end:::  

## <span data-ttu-id="74ea9-227">Investigar la asignación de memoria por función</span><span class="sxs-lookup"><span data-stu-id="74ea9-227">Investigate memory allocation by function</span></span>  

<span data-ttu-id="74ea9-228">Use el tipo de generación de perfiles de **muestreo de asignación** para ver la asignación de memoria por función de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="74ea9-228">Use the **Allocation sampling** profiling type to view memory allocation by JavaScript function.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png":::
   <span data-ttu-id="74ea9-230">Ilustración 11: muestreo de asignación de registros</span><span class="sxs-lookup"><span data-stu-id="74ea9-230">Figure 11:  Record Allocation sampling</span></span>  
:::image-end:::  

1.  <span data-ttu-id="74ea9-231">Seleccione el botón de opción **muestreo de asignación** .</span><span class="sxs-lookup"><span data-stu-id="74ea9-231">Select the **Allocation sampling** radio button.</span></span>  <span data-ttu-id="74ea9-232">Si hay un trabajo en la página, puede seleccionarlo como destino de la generación de perfiles con el menú desplegable situado junto al botón **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="74ea9-232">If there is a worker on the page, you are able to select that as the profiling target using the dropdown menu next to the **Start** button.</span></span>  
1.  <span data-ttu-id="74ea9-233">Pulse el botón **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="74ea9-233">Press the **Start** button.</span></span>  
1.  <span data-ttu-id="74ea9-234">Realice las acciones en la página que desea investigar.</span><span class="sxs-lookup"><span data-stu-id="74ea9-234">Perform the actions on the page which you want to investigate.</span></span>  
1.  <span data-ttu-id="74ea9-235">Pulse el botón **detener** cuando haya finalizado todas las acciones.</span><span class="sxs-lookup"><span data-stu-id="74ea9-235">Press the **Stop** button when you have finished all of your actions.</span></span>  

<span data-ttu-id="74ea9-236">En DevTools se muestra un desglose de la asignación de memoria por función.</span><span class="sxs-lookup"><span data-stu-id="74ea9-236">DevTools shows you a breakdown of memory allocation by function.</span></span>  <span data-ttu-id="74ea9-237">La vista predeterminada es **gruesa (inferior hacia arriba)**, que muestra las funciones que asignaron la mayor cantidad de memoria en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="74ea9-237">The default view is **Heavy (Bottom Up)**, which displays the functions that allocated the most memory at the top.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png" alt-text="Abrir el administrador de tareas del explorador Microsoft Edge" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png":::
   <span data-ttu-id="74ea9-239">Ilustración 12: muestreo de asignaciones</span><span class="sxs-lookup"><span data-stu-id="74ea9-239">Figure 12:  Allocation sampling</span></span>  
:::image-end:::  

## <span data-ttu-id="74ea9-240">Detectar recolecciones de basura frecuentes</span><span class="sxs-lookup"><span data-stu-id="74ea9-240">Spot frequent garbage collections</span></span>  

<span data-ttu-id="74ea9-241">Si parece que la página se pone en pausa con frecuencia, es posible que tenga problemas de recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="74ea9-241">If your page appears to pause frequently, then you may have garbage collection issues.</span></span>  

<span data-ttu-id="74ea9-242">Puede usar el administrador de tareas del explorador Microsoft Edge o grabaciones de la memoria de rendimiento para detectar una recolección de elementos no utilizados frecuente.</span><span class="sxs-lookup"><span data-stu-id="74ea9-242">You are able to use either the Microsoft Edge Browser Task Manager or Performance memory recordings to spot frequent garbage collection.</span></span>  <span data-ttu-id="74ea9-243">En el administrador de tareas del explorador Microsoft Edge, el aumento o la caída frecuente de **memoria** o valores de **memoria de JavaScript** representan la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="74ea9-243">In the Microsoft Edge Browser Task Manager, frequently rising and falling **Memory** or **JavaScript Memory** values represent frequent garbage collection.</span></span>  <span data-ttu-id="74ea9-244">En las grabaciones de rendimiento, los cambios frecuentes \ (aumento y disminución \) en el montón de JS o los gráficos de recuento de nodos indican una recolección de elementos no utilizados frecuente.</span><span class="sxs-lookup"><span data-stu-id="74ea9-244">In Performance recordings, frequent changes \(rising and falling\) to the JS heap or node count graphs indicate frequent garbage collection.</span></span>  

<span data-ttu-id="74ea9-245">Después de identificar el problema, puede usar un **instrumental de asignación en** la grabación de la escala de tiempo para averiguar dónde se asigna la memoria y qué funciones están causando las asignaciones.</span><span class="sxs-lookup"><span data-stu-id="74ea9-245">After you have identified the problem, you are able to use an **Allocation instrumentation on timeline** recording to find out where memory is being allocated and which functions are causing the allocations.</span></span>  

## <span data-ttu-id="74ea9-246">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="74ea9-246">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageForceGarbageCollectionIcon]: ../media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: ../media/stop-recording-icon.msft.png  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Rendimiento del registro: referencia de análisis de rendimiento"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> <span data-ttu-id="74ea9-248">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="74ea9-248">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="74ea9-249">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="74ea9-249">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="74ea9-251">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="74ea9-251">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

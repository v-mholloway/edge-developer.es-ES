---
title: Solucionar problemas de memoria
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 738ef5fe682633f3100345c922ff12c3c27a7166
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611765"
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





# <span data-ttu-id="12be2-103">Solucionar problemas de memoria</span><span class="sxs-lookup"><span data-stu-id="12be2-103">Fix Memory Problems</span></span>   



<span data-ttu-id="12be2-104">Obtenga información sobre cómo usar Microsoft Edge y DevTools para buscar problemas de memoria que afecten al rendimiento de la página, como pérdidas de memoria, recarga de memoria y recolecciones de elementos no utilizados frecuentes.</span><span class="sxs-lookup"><span data-stu-id="12be2-104">Learn how to use Microsoft Edge and DevTools to find memory issues that affect page performance, including memory leaks, memory bloat, and frequent garbage collections.</span></span>  

### <span data-ttu-id="12be2-105">Resumen</span><span class="sxs-lookup"><span data-stu-id="12be2-105">Summary</span></span>  

*   <span data-ttu-id="12be2-106">Averigüe cuánta memoria está usando actualmente la página con el administrador de tareas del explorador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="12be2-106">Find out how much memory your page is currently using with the Microsoft Edge Browser Task Manager.</span></span>  
*   <span data-ttu-id="12be2-107">Visualice el uso de memoria a lo largo del tiempo con el panel **memoria** .</span><span class="sxs-lookup"><span data-stu-id="12be2-107">Visualize memory usage over time with the **Memory** panel.</span></span>  
*   <span data-ttu-id="12be2-108">Identifique los árboles DOM desvinculados \ (una causa común de fugas de memoria \) con la **instantánea de montón**.</span><span class="sxs-lookup"><span data-stu-id="12be2-108">Identify detached DOM trees \(a common cause of memory leaks\) with **Heap snapshot**.</span></span>  
*   <span data-ttu-id="12be2-109">Averigüe cuándo se va a asignar una nueva memoria en el montón \ (JS heap \) con **instrumentación de asignación en la escala de tiempo**.</span><span class="sxs-lookup"><span data-stu-id="12be2-109">Find out when new memory is being allocated in your JavaScript heap \(JS heap\) with **Allocation instrumentation on timeline**.</span></span>  

## <span data-ttu-id="12be2-110">Introducción</span><span class="sxs-lookup"><span data-stu-id="12be2-110">Overview</span></span>  

<span data-ttu-id="12be2-111">En el espíritu del modelo de rendimiento **ferroviario** , el enfoque de los esfuerzos de rendimiento debe ser los usuarios.</span><span class="sxs-lookup"><span data-stu-id="12be2-111">In the spirit of the **RAIL** performance model, the focus of your performance efforts should be your users.</span></span>  

<!--todo: add RAIL section when available  -->  

<span data-ttu-id="12be2-112">Los problemas de memoria son importantes porque a menudo son perceptibles para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="12be2-112">Memory issues are important because they are often perceivable by users.</span></span>  <span data-ttu-id="12be2-113">Los usuarios pueden percibir problemas de memoria de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="12be2-113">Users may perceive memory issues in the following ways:</span></span>  

*   <span data-ttu-id="12be2-114">**El rendimiento de una página se vuelve gradualmente con el tiempo**.</span><span class="sxs-lookup"><span data-stu-id="12be2-114">**The performance of a page gets progressively worse over time**.</span></span>  <span data-ttu-id="12be2-115">Esto es posiblemente un síntoma de pérdida de memoria.</span><span class="sxs-lookup"><span data-stu-id="12be2-115">This is possibly a symptom of a memory leak.</span></span>  <span data-ttu-id="12be2-116">Una pérdida de memoria se produce cuando un error en la página hace que la página use progresivamente más y más memoria a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="12be2-116">A memory leak is when a bug in the page causes the page to progressively use more and more memory over time.</span></span>  
*   <span data-ttu-id="12be2-117">**El rendimiento de una página es constantemente incorrecto**.</span><span class="sxs-lookup"><span data-stu-id="12be2-117">**The performance of a page is consistently bad**.</span></span>  <span data-ttu-id="12be2-118">Esto es posiblemente un síntoma de recarga de memoria.</span><span class="sxs-lookup"><span data-stu-id="12be2-118">This is possibly a symptom of memory bloat.</span></span>  <span data-ttu-id="12be2-119">El recargado de memoria es cuando una página utiliza más memoria de la necesaria para una velocidad de página óptima.</span><span class="sxs-lookup"><span data-stu-id="12be2-119">Memory bloat is when a page uses more memory than is necessary for optimal page speed.</span></span>  
*   <span data-ttu-id="12be2-120">**El rendimiento de una página se retrasa o parece que se pausa con frecuencia**.</span><span class="sxs-lookup"><span data-stu-id="12be2-120">**The performance of a page is delayed or appears to pause frequently**.</span></span>  <span data-ttu-id="12be2-121">Esto es posiblemente un síntoma de recolecciones de elementos no utilizados frecuentes.</span><span class="sxs-lookup"><span data-stu-id="12be2-121">This is possibly a symptom of frequent garbage collections.</span></span>  <span data-ttu-id="12be2-122">La recolección de elementos no utilizados se recolecta cuando el explorador reclama memoria.</span><span class="sxs-lookup"><span data-stu-id="12be2-122">Garbage collection is when the browser reclaims memory.</span></span>  <span data-ttu-id="12be2-123">El explorador decide cuando esto sucede.</span><span class="sxs-lookup"><span data-stu-id="12be2-123">The browser decides when this happens.</span></span>  <span data-ttu-id="12be2-124">Durante las colecciones, todo el script en ejecución está en pausa.</span><span class="sxs-lookup"><span data-stu-id="12be2-124">During collections, all script running is paused.</span></span>  <span data-ttu-id="12be2-125">Por lo tanto, si el explorador está recolectando un lote, el tiempo de ejecución de script se detendrá mucho.</span><span class="sxs-lookup"><span data-stu-id="12be2-125">So if the browser is garbage collecting a lot, script runtime is going to get paused a lot.</span></span>  

### <span data-ttu-id="12be2-126">Saturación de memoria: ¿Cuánto es "demasiado"?</span><span class="sxs-lookup"><span data-stu-id="12be2-126">Memory bloat: how much is "too much"?</span></span>  

<span data-ttu-id="12be2-127">Una pérdida de memoria es fácil de definir.</span><span class="sxs-lookup"><span data-stu-id="12be2-127">A memory leak is easy to define.</span></span>  <span data-ttu-id="12be2-128">Si un sitio está usando progresivamente más y más memoria, tendrá una fuga.</span><span class="sxs-lookup"><span data-stu-id="12be2-128">If a site is progressively using more and more memory, then you have a leak.</span></span>  <span data-ttu-id="12be2-129">Pero la saturación de la memoria es un poco más difícil de anclar.</span><span class="sxs-lookup"><span data-stu-id="12be2-129">But memory bloat is a bit harder to pin down.</span></span>  <span data-ttu-id="12be2-130">¿Qué califica como "usando demasiada memoria"?</span><span class="sxs-lookup"><span data-stu-id="12be2-130">What qualifies as "using too much memory"?</span></span>  

<span data-ttu-id="12be2-131">No hay números fuertes aquí, ya que los distintos dispositivos y exploradores tienen funciones diferentes.</span><span class="sxs-lookup"><span data-stu-id="12be2-131">There are no hard numbers here, because different devices and browsers have different capabilities.</span></span>  <span data-ttu-id="12be2-132">La misma página que se ejecuta sin problemas en smartphones de gama alta puede bloquearse en un smartphone de low-end.</span><span class="sxs-lookup"><span data-stu-id="12be2-132">The same page that runs smoothly on a high-end smartphone may crash on a low-end smartphone.</span></span>  

<span data-ttu-id="12be2-133">La clave aquí es usar el modelo de raíl y centrarse en los usuarios.</span><span class="sxs-lookup"><span data-stu-id="12be2-133">The key here is to use the RAIL model and focus on your users.</span></span>  <span data-ttu-id="12be2-134">Averigüe qué dispositivos son populares con los usuarios y, a continuación, pruebe la página en esos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="12be2-134">Find out what devices are popular with your users, and then test out your page on those devices.</span></span>  <span data-ttu-id="12be2-135">Si la experiencia es constantemente incorrecta, es posible que la página exceda las capacidades de memoria de esos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="12be2-135">If the experience is consistently bad, the page may be exceeding the memory capabilities of those devices.</span></span>  

## <span data-ttu-id="12be2-136">Supervisar el uso de memoria en tiempo real con el administrador de tareas del explorador Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="12be2-136">Monitor memory use in realtime with the Microsoft Edge Browser Task Manager</span></span>  

<span data-ttu-id="12be2-137">Use el administrador de tareas del explorador Microsoft Edge como punto de partida para la investigación de problemas de memoria.</span><span class="sxs-lookup"><span data-stu-id="12be2-137">Use the Microsoft Edge Browser Task Manager as a starting point to your memory issue investigation.</span></span>  <span data-ttu-id="12be2-138">El administrador de tareas del explorador Microsoft Edge es un monitor en tiempo real que indica la cantidad de memoria que está usando una página en ese momento.</span><span class="sxs-lookup"><span data-stu-id="12be2-138">The Microsoft Edge Browser Task Manager is a realtime monitor that tells you how much memory a page is currently using.</span></span>  

1.  <span data-ttu-id="12be2-139">Presione `Shift` + `Esc` o vaya al menú principal de Microsoft Edge y seleccione **más herramientas**  >  **Administrador de tareas del explorador** para abrir el administrador de tareas del explorador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="12be2-139">Press `Shift`+`Esc` or go to the Microsoft Edge main menu and select **More tools** > **Browser Task Manager** to open the Microsoft Edge Browser Task Manager.</span></span>  
    
    > ##### <span data-ttu-id="12be2-140">Figura 1</span><span class="sxs-lookup"><span data-stu-id="12be2-140">Figure 1</span></span>  
    > <span data-ttu-id="12be2-141">Abrir el administrador de tareas del explorador Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="12be2-141">Opening the Microsoft Edge Browser Task Manager</span></span>  
    > ![Abrir el administrador de tareas del explorador Microsoft Edge][ImageTaskManager]  
    
1.  <span data-ttu-id="12be2-143">Haga clic con el botón derecho en el encabezado de tabla del administrador de tareas del explorador Microsoft Edge y habilite la **memoria JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="12be2-143">Right-click on the table header of the Microsoft Edge Browser Task Manager and enable **JavaScript memory**.</span></span>  
    
    > ##### <span data-ttu-id="12be2-144">Figura 2</span><span class="sxs-lookup"><span data-stu-id="12be2-144">Figure 2</span></span>  
    > <span data-ttu-id="12be2-145">Habilitar la memoria de JavaScript</span><span class="sxs-lookup"><span data-stu-id="12be2-145">Enable JavaScript memory</span></span>  
    > ![Habilitar la memoria de JavaScript][ImageJavascriptMemory]  
    
<span data-ttu-id="12be2-147">Estas dos columnas le indican diferentes cosas sobre cómo está usando la página la memoria:</span><span class="sxs-lookup"><span data-stu-id="12be2-147">These two columns tell you different things about how your page is using memory:</span></span>  

*   <span data-ttu-id="12be2-148">La columna **memoria** representa la memoria nativa.</span><span class="sxs-lookup"><span data-stu-id="12be2-148">The **Memory** column represents native memory.</span></span>  <span data-ttu-id="12be2-149">Los nodos DOM se almacenan en la memoria nativa.</span><span class="sxs-lookup"><span data-stu-id="12be2-149">DOM nodes are stored in native memory.</span></span>  <span data-ttu-id="12be2-150">Si este valor aumenta, se crean los nodos DOM.</span><span class="sxs-lookup"><span data-stu-id="12be2-150">If this value is increasing, DOM nodes are getting created.</span></span>  
*   <span data-ttu-id="12be2-151">La columna **memoria de JavaScript** representa el montón de JS.</span><span class="sxs-lookup"><span data-stu-id="12be2-151">The **JavaScript Memory** column represents the JS heap.</span></span>  <span data-ttu-id="12be2-152">Esta columna contiene dos valores.</span><span class="sxs-lookup"><span data-stu-id="12be2-152">This column contains two values.</span></span>  <span data-ttu-id="12be2-153">El valor que te interesa es el número en vivo \ (el número entre paréntesis \).</span><span class="sxs-lookup"><span data-stu-id="12be2-153">The value you are interested in is the live number \(the number in parentheses\).</span></span>  <span data-ttu-id="12be2-154">El número en vivo representa la cantidad de memoria que usan los objetos que se pueden encontrar en la página.</span><span class="sxs-lookup"><span data-stu-id="12be2-154">The live number represents how much memory the reachable objects on your page are using.</span></span>  <span data-ttu-id="12be2-155">Si este número está aumentando, se crean objetos nuevos o los objetos existentes crecen.</span><span class="sxs-lookup"><span data-stu-id="12be2-155">If this number is increasing, either new objects are being created, or the existing objects are growing.</span></span>  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <span data-ttu-id="12be2-156">Visualizar pérdidas de memoria con el panel rendimiento</span><span class="sxs-lookup"><span data-stu-id="12be2-156">Visualize memory leaks with Performance panel</span></span>  

<span data-ttu-id="12be2-157">También puede usar el panel rendimiento como otro punto de partida en su investigación.</span><span class="sxs-lookup"><span data-stu-id="12be2-157">You may also use the Performance panel as another starting point in your investigation.</span></span>  <span data-ttu-id="12be2-158">El panel rendimiento le ayuda a visualizar el uso de memoria de una página a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="12be2-158">The Performance panel helps you visualize the memory use of a page over time.</span></span>  

1.  <span data-ttu-id="12be2-159">Abra el panel de **rendimiento** en DevTools.</span><span class="sxs-lookup"><span data-stu-id="12be2-159">Open the **Performance** panel on DevTools.</span></span>  
1.  <span data-ttu-id="12be2-160">Active la casilla **memoria** .</span><span class="sxs-lookup"><span data-stu-id="12be2-160">Enable the **Memory** checkbox.</span></span>  
1.  <span data-ttu-id="12be2-161">[Hacer una grabación][DevtoolsEvaluatePerformanceReferenceRecord].</span><span class="sxs-lookup"><span data-stu-id="12be2-161">[Make a recording][DevtoolsEvaluatePerformanceReferenceRecord].</span></span>  

> [!TIP]
> <span data-ttu-id="12be2-162">Es recomendable iniciar y finalizar la grabación con una recolección de elementos no utilizados forzada.</span><span class="sxs-lookup"><span data-stu-id="12be2-162">It is a good practice to start and end your recording with a forced garbage collection.</span></span>  <span data-ttu-id="12be2-163">Haga clic en el botón **recopilar** eliminación de elementos no usados al ![ ][ImageForceGarbageCollectionIcon] grabar para forzar la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="12be2-163">Click the **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button while recording to force garbage collection.</span></span>  

<span data-ttu-id="12be2-164">Para hacer una demostración de las grabaciones de la memoria, considere el siguiente código:</span><span class="sxs-lookup"><span data-stu-id="12be2-164">To demonstrate memory recordings, consider the code below:</span></span>  

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

<span data-ttu-id="12be2-165">Cada vez que se presiona el botón al que se hace referencia en el código, `div` los nodos de 10000 se anexan al cuerpo del documento y se inserta una cadena de 1 millón `x` caracteres en la `x` matriz.</span><span class="sxs-lookup"><span data-stu-id="12be2-165">Every time that the button referenced in the code is pressed, ten thousand `div` nodes are appended to the document body, and a string of one million `x` characters is pushed onto the `x` array.</span></span>  <span data-ttu-id="12be2-166">La ejecución de este código genera una grabación en el panel de **rendimiento** , como la [ilustración 3](#figure-3).</span><span class="sxs-lookup"><span data-stu-id="12be2-166">Running this code produces a recording in the **Performance** panel like [Figure 3](#figure-3).</span></span>  

> ##### <span data-ttu-id="12be2-167">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="12be2-167">Figure 3</span></span>  
> <span data-ttu-id="12be2-168">Crecimiento simple</span><span class="sxs-lookup"><span data-stu-id="12be2-168">Simple growth</span></span>  
> ![Crecimiento simple][ImageSimpleGrowth]  

<span data-ttu-id="12be2-170">En primer lugar, una explicación de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="12be2-170">First, an explanation of the user interface.</span></span>  <span data-ttu-id="12be2-171">El gráfico de **montones** en el panel de **información general** \ (debajo de **net**\) representa el montón de JS.</span><span class="sxs-lookup"><span data-stu-id="12be2-171">The **HEAP** graph in the **Overview** pane \(below **NET**\) represents the JS heap.</span></span>  <span data-ttu-id="12be2-172">Debajo del panel de **información general** se encuentra el panel de **contador** .</span><span class="sxs-lookup"><span data-stu-id="12be2-172">Below the **Overview** pane is the **Counter** pane.</span></span>  <span data-ttu-id="12be2-173">Aquí puede ver el uso de memoria desglosado por montones de JS \ (igual al gráfico de **montón** en el panel de **información general** \), documentos, nodos DOM, oyentes y memoria de GPU.</span><span class="sxs-lookup"><span data-stu-id="12be2-173">Here you are able to see memory usage broken down by JS heap \(same as **HEAP** graph in the **Overview** pane\), documents, DOM nodes, listeners, and GPU memory.</span></span>  <span data-ttu-id="12be2-174">Al deshabilitar una casilla, la oculta del gráfico.</span><span class="sxs-lookup"><span data-stu-id="12be2-174">Disabling a checkbox hides it from the graph.</span></span>  

<span data-ttu-id="12be2-175">Ahora, un análisis del código comparado con la [ilustración 3](#figure-3).</span><span class="sxs-lookup"><span data-stu-id="12be2-175">Now, an analysis of the code compared with [Figure 3](#figure-3).</span></span>  <span data-ttu-id="12be2-176">Si miras el contador de nodos \ (el gráfico verde \), podrás ver que coincide perfectamente con el código.</span><span class="sxs-lookup"><span data-stu-id="12be2-176">If you look at the node counter \(the green graph\) you are able to see that it matches up cleanly with the code.</span></span>  <span data-ttu-id="12be2-177">El número de nodos aumenta en pasos discretos.</span><span class="sxs-lookup"><span data-stu-id="12be2-177">The node count increases in discrete steps.</span></span>  <span data-ttu-id="12be2-178">Puede dar por supuesto que cada aumento en el recuento de nodos es una llamada a `grow()` .</span><span class="sxs-lookup"><span data-stu-id="12be2-178">You may presume that each increase in the node count is a call to `grow()`.</span></span>  <span data-ttu-id="12be2-179">El gráfico de montón JS \ (gráfico azul \) no es tan sencillo.</span><span class="sxs-lookup"><span data-stu-id="12be2-179">The JS heap graph \(the blue graph\) is not as straightforward.</span></span>  <span data-ttu-id="12be2-180">Siguiendo los procedimientos recomendados, la primera DIP es, en realidad, una recolección forzada de elementos no utilizados \ (que se consigue al **presionar el** botón de recolección de elementos no ![ utilizados ][ImageForceGarbageCollectionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="12be2-180">In keeping with best practices, the first dip is actually a forced garbage collection \(achieved by pressing the  **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button\).</span></span>  <span data-ttu-id="12be2-181">A medida que la grabación se progrese, podrá ver que el tamaño del montón de JS es demasiado bajo.</span><span class="sxs-lookup"><span data-stu-id="12be2-181">As the recording progresses you are able to see that the JS heap size spikes.</span></span>  <span data-ttu-id="12be2-182">Esto es natural y se espera: el código JavaScript crea los nodos DOM en cada botón haga clic y realice una gran cantidad de trabajo cuando crea la cadena de 1 millón caracteres.</span><span class="sxs-lookup"><span data-stu-id="12be2-182">This is natural and expected:  the JavaScript code is creating the DOM nodes on every button click and doing a lot of work when it creates the string of one million characters.</span></span>  <span data-ttu-id="12be2-183">Lo fundamental aquí es el hecho de que el montón JS finaliza más de lo que comenzó \ (el "comienzo" aquí es el punto después de la recolección de elementos no utilizados forzada \).</span><span class="sxs-lookup"><span data-stu-id="12be2-183">The key thing here is the fact that the JS heap ends higher than it began \(the "beginning" here being the point after the forced garbage collection\).</span></span>  <span data-ttu-id="12be2-184">En el mundo real, si viera este patrón de aumento del tamaño de la pila de JS o del tamaño del nodo, puede definir potencialmente una pérdida de memoria.</span><span class="sxs-lookup"><span data-stu-id="12be2-184">In the real world, if you saw this pattern of increasing JS heap size or node size, it may potentially define a memory leak.</span></span>  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <span data-ttu-id="12be2-185">Descubrir pérdidas de memoria en el árbol de DOM desvinculadas con instantáneas de montones</span><span class="sxs-lookup"><span data-stu-id="12be2-185">Discover detached DOM tree memory leaks with Heap Snapshots</span></span>  

<span data-ttu-id="12be2-186">Un nodo DOM solo se recolecta como no utilizado cuando no hay ninguna referencia al nodo desde el árbol DOM o el código JavaScript que se ejecuta en la página.</span><span class="sxs-lookup"><span data-stu-id="12be2-186">A DOM node is only garbage collected when there are no references to the node from either the DOM tree or JavaScript code running on the page.</span></span>  <span data-ttu-id="12be2-187">Se dice que un nodo está "separado" cuando se quita del árbol DOM, pero algunos JavaScript siguen haciendo referencia a él.</span><span class="sxs-lookup"><span data-stu-id="12be2-187">A node is said to be "detached" when it is removed from the DOM tree but some JavaScript still references it.</span></span>  <span data-ttu-id="12be2-188">Los nodos DOM separados son una causa común de las pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="12be2-188">Detached DOM nodes are a common cause of memory leaks.</span></span>  <span data-ttu-id="12be2-189">En esta sección aprenderá a usar los perfilers de montones en DevTools para identificar los nodos desvinculados.</span><span class="sxs-lookup"><span data-stu-id="12be2-189">This section teaches you how to use the heap profilers in DevTools to identify detached nodes.</span></span>  

<span data-ttu-id="12be2-190">Este es un ejemplo sencillo de nodos DOM separados.</span><span class="sxs-lookup"><span data-stu-id="12be2-190">Here is a simple example of detached DOM nodes.</span></span>  

```javascript
var detachedNodes;
function create() {
    var ul = document.createElement('ul');
    for (var i = 0; i < 10; i++) {
        var li = document.createElement('li');
        ul.appendChild(li);
    }
    detachedNodes = ul;
}
document.getElementById('create').addEventListener('click', create);
```  

<span data-ttu-id="12be2-191">Al hacer clic en el botón al que se hace referencia en el código, se crea un `ul` nodo con diez `li` elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="12be2-191">Clicking the button referenced in the code creates a `ul` node with ten `li` children.</span></span>  <span data-ttu-id="12be2-192">El código hace referencia a estos nodos, pero no existen en el árbol DOM, por lo que se desasocian.</span><span class="sxs-lookup"><span data-stu-id="12be2-192">These nodes are referenced by the code but do not exist in the DOM tree, so each is detached.</span></span>  

<span data-ttu-id="12be2-193">Las instantáneas de montones son una manera de identificar los nodos desvinculados.</span><span class="sxs-lookup"><span data-stu-id="12be2-193">Heap snapshots are one way to identify detached nodes.</span></span>  <span data-ttu-id="12be2-194">Como su nombre indica, las instantáneas de montones muestran cómo se distribuye la memoria entre los objetos JS y los nodos DOM de la página en el punto de tiempo de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="12be2-194">As the name implies, heap snapshots show you how memory is distributed among the JS objects and DOM nodes for your page at the point of time of the snapshot.</span></span>  

<span data-ttu-id="12be2-195">Para crear una instantánea, abra DevTools y vaya al panel **memoria** , seleccione el botón de radio de la **instantánea de montones** y, después, presione el botón **tomar instantánea** .</span><span class="sxs-lookup"><span data-stu-id="12be2-195">To create a snapshot, open DevTools and go to the **Memory** panel, select the **Heap snapshot** radio button, and then press the **Take snapshot** button.</span></span>  

> ##### <span data-ttu-id="12be2-196">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="12be2-196">Figure 4</span></span>  
> <span data-ttu-id="12be2-197">Tomar instantánea de montón</span><span class="sxs-lookup"><span data-stu-id="12be2-197">Take heap snapshot</span></span>  
> ![Tomar instantánea de montón][ImageTakeHeapSnapshot]  

<span data-ttu-id="12be2-199">La instantánea puede tardar algún tiempo en procesarse y cargarse.</span><span class="sxs-lookup"><span data-stu-id="12be2-199">The snapshot may take some time to process and load.</span></span>  <span data-ttu-id="12be2-200">Una vez que haya terminado, selecciónelo en el panel de la izquierda \ ( **instantáneas de montones**con nombre \).</span><span class="sxs-lookup"><span data-stu-id="12be2-200">After it is finished, select it from the left-hand panel \(named **HEAP SNAPSHOTS**\).</span></span>  

<span data-ttu-id="12be2-201">Escriba `Detached` el cuadro de texto **filtro de clase** para buscar árboles Dom desvinculados.</span><span class="sxs-lookup"><span data-stu-id="12be2-201">Type `Detached` in the **Class filter** textbox to search for detached DOM trees.</span></span>  

> ##### <span data-ttu-id="12be2-202">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="12be2-202">Figure 5</span></span>  
> <span data-ttu-id="12be2-203">Filtrar por nodos desvinculados</span><span class="sxs-lookup"><span data-stu-id="12be2-203">Filtering for detached nodes</span></span>  
> ![Filtrar por nodos desvinculados][ImageFilteringForDetachedNodes]  

<span data-ttu-id="12be2-205">Expanda el carats para investigar un árbol desvinculado.</span><span class="sxs-lookup"><span data-stu-id="12be2-205">Expand the carats to investigate a detached tree.</span></span>  

> ##### <span data-ttu-id="12be2-206">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="12be2-206">Figure 6</span></span>  
> <span data-ttu-id="12be2-207">Investigando el árbol separado</span><span class="sxs-lookup"><span data-stu-id="12be2-207">Investigating detached tree</span></span>  
> ![Investigando el árbol separado][ImageInvestigatingDetachedTree]  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

<span data-ttu-id="12be2-209">Haga clic en un nodo para investigarlo más lejos.</span><span class="sxs-lookup"><span data-stu-id="12be2-209">Click on a node to investigate it further.</span></span>  <span data-ttu-id="12be2-210">En el panel **objetos** puede ver más información sobre el código que hace referencia.</span><span class="sxs-lookup"><span data-stu-id="12be2-210">In the **Objects** pane you are able to see more information about the code that is referencing it.</span></span>  <span data-ttu-id="12be2-211">Por ejemplo, en la [figura 7](#figure-7) puede ver que la `detachedNodes` variable hace referencia al nodo.</span><span class="sxs-lookup"><span data-stu-id="12be2-211">For example, in [Figure 7](#figure-7) you are able to see that the `detachedNodes` variable is referencing the node.</span></span>  <span data-ttu-id="12be2-212">Para corregir esta pérdida de memoria determinada, debe estudiar el código que usa la `detachedUNode` variable y asegurarse de que la referencia al nodo se quita cuando ya no es necesaria.</span><span class="sxs-lookup"><span data-stu-id="12be2-212">To fix this particular memory leak, you should study the code that uses the `detachedUNode` variable and ensure that the reference to the node is removed when it is no longer needed.</span></span>

> ##### <span data-ttu-id="12be2-213">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="12be2-213">Figure 7</span></span>  
> <span data-ttu-id="12be2-214">Investigar un nodo</span><span class="sxs-lookup"><span data-stu-id="12be2-214">Investigating a node</span></span>  
> ![Investigar un nodo][ImageInvestigatingNode]  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <span data-ttu-id="12be2-216">Identificar pérdidas de memoria de montón JS con instrumentación de asignación en la escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="12be2-216">Identify JS heap memory leaks with Allocation instrumentation on timeline</span></span>  

<span data-ttu-id="12be2-217">La **instrumentación de asignación de la escala de tiempo** es otra herramienta que puede ayudarle a realizar un seguimiento de las pérdidas de memoria en el montón de JS.</span><span class="sxs-lookup"><span data-stu-id="12be2-217">**Allocation instrumentation on timeline** is another tool that may help you track down memory leaks in your JS heap.</span></span>  

<span data-ttu-id="12be2-218">Muestre la **instrumentación de asignación en la escala de tiempo** con el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="12be2-218">Demonstrate **Allocation instrumentation on timeline**  using the following code.</span></span>  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="12be2-219">Cada vez que se inserta el botón al que se hace referencia en el código, se agrega una cadena de 1 millón caracteres a la `x` matriz.</span><span class="sxs-lookup"><span data-stu-id="12be2-219">Every time that the button referenced in the code is pushed, a string of one million characters is added to the `x` array.</span></span>  

<span data-ttu-id="12be2-220">Para grabar un instrumental de asignación en la escala de tiempo, abra DevTools, vaya al panel **memoria** , seleccione el botón **de opción instrumentación de asignación en la escala de tiempo** , presione el botón **Inicio** , realice la acción que sospecha que está causando la pérdida de memoria y, después, presione el botón Detener grabación del **montón de grabación** ![ cuando haya ][ImageStopRecordingIcon] terminado.</span><span class="sxs-lookup"><span data-stu-id="12be2-220">To record an Allocation instrumentation on timeline, open DevTools, go to the **Memory** panel, select the **Allocation instrumentation on timeline** radio button, press the **Start** button, perform the action that you suspect is causing the memory leak, and then press the **Stop recording heap profile** ![stop recording][ImageStopRecordingIcon] button when you are done.</span></span>  

<span data-ttu-id="12be2-221">Mientras graba, observe si en la línea de tiempo se muestran barras azules en la instrumentación de asignación, como en la [figura 8](#figure-8).</span><span class="sxs-lookup"><span data-stu-id="12be2-221">As you are recording, notice if any blue bars show up on the Allocation instrumentation on timeline, like in [Figure 8](#figure-8).</span></span>  

> ##### <span data-ttu-id="12be2-222">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="12be2-222">Figure 8</span></span>  
> <span data-ttu-id="12be2-223">Nuevas asignaciones</span><span class="sxs-lookup"><span data-stu-id="12be2-223">New allocations</span></span>  
> ![Nuevas asignaciones][ImageNewAllocations]  

<span data-ttu-id="12be2-225">Estas barras azules representan nuevas asignaciones de memoria.</span><span class="sxs-lookup"><span data-stu-id="12be2-225">Those blue bars represent new memory allocations.</span></span>  <span data-ttu-id="12be2-226">Estas nuevas asignaciones de memoria son sus candidatos para pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="12be2-226">Those new memory allocations are your candidates for memory leaks.</span></span>  <span data-ttu-id="12be2-227">Puede hacer zoom en una barra para filtrar el panel **constructor** y mostrar únicamente los objetos que se asignaron durante el período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="12be2-227">You are able to zoom on a bar to filter the **Constructor** pane to only show objects that were allocated during the specified timeframe.</span></span>  

> ##### <span data-ttu-id="12be2-228">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="12be2-228">Figure 9</span></span>  
> <span data-ttu-id="12be2-229">Escala de tiempo de asignación ampliada</span><span class="sxs-lookup"><span data-stu-id="12be2-229">Zoomed allocation timeline</span></span>  
> ![Escala de tiempo de asignación ampliada][ImageZoomedAllocationTimeline]  

<span data-ttu-id="12be2-231">Expanda el objeto y haga clic en el valor para ver más detalles en el panel de **objetos** .</span><span class="sxs-lookup"><span data-stu-id="12be2-231">Expand the object and click on the value to view more details in the **Object** pane.</span></span>  <span data-ttu-id="12be2-232">Por ejemplo, en la [figura 10](#figure-10), al ver los detalles del objeto que se ha asignado recientemente, debería poder ver que se ha asignado a la `x` variable en el `Window` ámbito.</span><span class="sxs-lookup"><span data-stu-id="12be2-232">For example, in [Figure 10](#figure-10), by viewing the details of the object that was newly allocated, you should be able to see that it was allocated to the `x` variable in the `Window` scope.</span></span>  

> ##### <span data-ttu-id="12be2-233">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="12be2-233">Figure 10</span></span> 
> <span data-ttu-id="12be2-234">Detalles del objeto</span><span class="sxs-lookup"><span data-stu-id="12be2-234">Object details</span></span>  
> ![Detalles del objeto][ImageObjectDetail]  

## <span data-ttu-id="12be2-236">Investigar la asignación de memoria por función</span><span class="sxs-lookup"><span data-stu-id="12be2-236">Investigate memory allocation by function</span></span>   

<span data-ttu-id="12be2-237">Use el tipo de generación de perfiles de **muestreo de asignación** para ver la asignación de memoria por función de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="12be2-237">Use the **Allocation sampling** profiling type to view memory allocation by JavaScript function.</span></span>  

> ##### <span data-ttu-id="12be2-238">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="12be2-238">Figure 11</span></span>  
> <span data-ttu-id="12be2-239">Muestreo de asignación de registros</span><span class="sxs-lookup"><span data-stu-id="12be2-239">Record Allocation sampling</span></span>  
> ![Muestreo de asignación de registros][ImageRecordAllocationSampling]  

1.  <span data-ttu-id="12be2-241">Seleccione el botón de opción **muestreo de asignación** .</span><span class="sxs-lookup"><span data-stu-id="12be2-241">Select the **Allocation sampling** radio button.</span></span>  <span data-ttu-id="12be2-242">Si hay un trabajo en la página, puede seleccionarlo como destino de la generación de perfiles con el menú desplegable situado junto al botón **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="12be2-242">If there is a worker on the page, you are able to select that as the profiling target using the dropdown menu next to the **Start** button.</span></span>  
1.  <span data-ttu-id="12be2-243">Pulse el botón **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="12be2-243">Press the **Start** button.</span></span>  
1.  <span data-ttu-id="12be2-244">Realice las acciones en la página que desea investigar.</span><span class="sxs-lookup"><span data-stu-id="12be2-244">Perform the actions on the page which you want to investigate.</span></span>  
1.  <span data-ttu-id="12be2-245">Pulse el botón **detener** cuando haya finalizado todas las acciones.</span><span class="sxs-lookup"><span data-stu-id="12be2-245">Press the **Stop** button when you have finished all of your actions.</span></span>  

<span data-ttu-id="12be2-246">En DevTools se muestra un desglose de la asignación de memoria por función.</span><span class="sxs-lookup"><span data-stu-id="12be2-246">DevTools shows you a breakdown of memory allocation by function.</span></span>  <span data-ttu-id="12be2-247">La vista predeterminada es **gruesa (inferior hacia arriba)**, que muestra las funciones que asignaron la mayor cantidad de memoria en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="12be2-247">The default view is **Heavy (Bottom Up)**, which displays the functions that allocated the most memory at the top.</span></span>  

> ##### <span data-ttu-id="12be2-248">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="12be2-248">Figure 12</span></span>  
> <span data-ttu-id="12be2-249">Muestreo de asignación</span><span class="sxs-lookup"><span data-stu-id="12be2-249">Allocation sampling</span></span>  
>![Muestreo de asignación][ImageAllocationSampling]  

## <span data-ttu-id="12be2-251">Detectar recolecciones de basura frecuentes</span><span class="sxs-lookup"><span data-stu-id="12be2-251">Spot frequent garbage collections</span></span>  

<span data-ttu-id="12be2-252">Si parece que la página se pone en pausa con frecuencia, es posible que tenga problemas de recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="12be2-252">If your page appears to pause frequently, then you may have garbage collection issues.</span></span>  

<span data-ttu-id="12be2-253">Puede usar el administrador de tareas del explorador Microsoft Edge o grabaciones de la memoria de rendimiento para detectar una recolección de elementos no utilizados frecuente.</span><span class="sxs-lookup"><span data-stu-id="12be2-253">You are able to use either the Microsoft Edge Browser Task Manager or Performance memory recordings to spot frequent garbage collection.</span></span>  <span data-ttu-id="12be2-254">En el administrador de tareas del explorador Microsoft Edge, el aumento o la caída frecuente de **memoria** o valores de **memoria de JavaScript** representan la recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="12be2-254">In the Microsoft Edge Browser Task Manager, frequently rising and falling **Memory** or **JavaScript Memory** values represent frequent garbage collection.</span></span>  <span data-ttu-id="12be2-255">En las grabaciones de rendimiento, los cambios frecuentes (aumento o caída) en el montón de JS o en los gráficos de recuento de nodos indican una recolección de elementos no utilizados frecuente.</span><span class="sxs-lookup"><span data-stu-id="12be2-255">In Performance recordings, frequent changes (rising and falling) to the JS heap or node count graphs indicate frequent garbage collection.</span></span>  

<span data-ttu-id="12be2-256">Después de identificar el problema, puede usar un **instrumental de asignación en** la grabación de la escala de tiempo para averiguar dónde se asigna la memoria y qué funciones están causando las asignaciones.</span><span class="sxs-lookup"><span data-stu-id="12be2-256">After you have identified the problem, you are able to use an **Allocation instrumentation on timeline** recording to find out where memory is being allocated and which functions are causing the allocations.</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageForceGarbageCollectionIcon]: /microsoft-edge/devtools-guide-chromium/media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: /microsoft-edge/devtools-guide-chromium/media/stop-recording-icon.msft.png  

[ImageTaskManager]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png "Ilustración 1: abrir el administrador de tareas del explorador Microsoft Edge"  
[ImageJavascriptMemory]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png "Ilustración 2: habilitar la memoria de JavaScript"  
[ImageSimpleGrowth]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-1-performance-memory.msft.png "Ilustración 3: crecimiento simple"  
[ImageTakeHeapSnapshot]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png "Ilustración 4: tomar instantánea de montón"  
[ImageFilteringForDetachedNodes]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png "Ilustración 5: filtrar por nodos desvinculados"  
[ImageInvestigatingDetachedTree]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png "Ilustración 6: investigación de árboles desconectados"  
[ImageInvestigatingNode]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png "Ilustración 7: investigar un nodo"  
[ImageNewAllocations]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png "Ilustración 8: nuevas asignaciones"  
[ImageZoomedAllocationTimeline]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png "Ilustración 9: escala de tiempo de asignación ampliada"  
[ImageObjectDetail]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png "Ilustración 10: detalles del objeto"  
[ImageRecordAllocationSampling]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png "Ilustración 11: muestreo de asignación de registros"  
[ImageAllocationSampling]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png "Ilustración 12: muestreo de asignaciones"  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Rendimiento del registro: referencia de análisis de rendimiento"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> <span data-ttu-id="12be2-270">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="12be2-270">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="12be2-271">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="12be2-271">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="12be2-273">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="12be2-273">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

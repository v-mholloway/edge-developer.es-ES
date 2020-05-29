---
title: Referencia de depuración de JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 1d361bb39523e9b039500f46da54e60b82adbda6
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581743"
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







# <span data-ttu-id="3a827-103">Referencia de depuración de JavaScript</span><span class="sxs-lookup"><span data-stu-id="3a827-103">JavaScript Debugging Reference</span></span>   



<span data-ttu-id="3a827-104">Descubra nuevos flujos de trabajo de depuración con esta referencia completa de las características de depuración de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="3a827-104">Discover new debugging workflows with this comprehensive reference of Microsoft Edge DevTools debugging features.</span></span>  

<span data-ttu-id="3a827-105">Consulta Introducción a la [depuración de JavaScript en Microsoft Edge DevTools][DevToolsJavascriptGetStarted] para conocer los conceptos básicos de la depuración.</span><span class="sxs-lookup"><span data-stu-id="3a827-105">See [Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted] to learn the basics of debugging.</span></span>  

## <span data-ttu-id="3a827-106">Pausar código con puntos de interrupción</span><span class="sxs-lookup"><span data-stu-id="3a827-106">Pause code with breakpoints</span></span>   

<span data-ttu-id="3a827-107">Establezca un punto de interrupción para que pueda pausar el código en el medio del Runtime.</span><span class="sxs-lookup"><span data-stu-id="3a827-107">Set a breakpoint so that you are able to pause your code in the middle of the runtime.</span></span>  

<span data-ttu-id="3a827-108">Vea [pausar el código con puntos de interrupción][DevToolsJavascriptBreakpoints] para obtener información sobre cómo establecer puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="3a827-108">See [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints] to learn how to set breakpoints.</span></span>  

[DevToolsJavascriptBreakpoints]: breakpoints.md "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools"  

## <span data-ttu-id="3a827-110">Recorrer el código</span><span class="sxs-lookup"><span data-stu-id="3a827-110">Step through code</span></span>   

<span data-ttu-id="3a827-111">Una vez que el código esté pausado, recorralo, de una línea a la vez, investigando el flujo de control y los valores de propiedad durante el proceso.</span><span class="sxs-lookup"><span data-stu-id="3a827-111">Once your code is paused, step through it, one line at a time, investigating control flow and property values along the way.</span></span>  

### <span data-ttu-id="3a827-112">Paso a paso por la línea de código</span><span class="sxs-lookup"><span data-stu-id="3a827-112">Step over line of code</span></span>   

<span data-ttu-id="3a827-113">Cuando esté pausado en una línea de código que contenga una función que no sea relevante para el problema que está depurando, haga clic **en el icono de paso a** paso por encima ![ ][ImageStepOverIcon] para ejecutar la función sin ir a la misma.</span><span class="sxs-lookup"><span data-stu-id="3a827-113">When paused on a line of code containing a function that is not relevant to the problem you are debugging, click on the **Step over** ![Step over][ImageStepOverIcon] icon to run the function without stepping into it.</span></span>  

> ##### <span data-ttu-id="3a827-114">Figura 1</span><span class="sxs-lookup"><span data-stu-id="3a827-114">Figure 1</span></span>  
> <span data-ttu-id="3a827-115">Seleccionar **paso a paso por procedimientos**</span><span class="sxs-lookup"><span data-stu-id="3a827-115">Selecting **Step over**</span></span>  
> ![Seleccionar paso a paso por procedimientos][ImageSelectingStepOver]  

<span data-ttu-id="3a827-117">Por ejemplo, supongamos que está depurando el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="3a827-117">For example, suppose you are debugging the following code:</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name); // D
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name; // C
}
```  

<span data-ttu-id="3a827-118">Estás pausado el `A` .</span><span class="sxs-lookup"><span data-stu-id="3a827-118">You are paused on `A`.</span></span>  <span data-ttu-id="3a827-119">Si pulsas **paso a paso**, DevTools ejecuta todo el código de la función que estás recorriendo, que `B` es `C` y.</span><span class="sxs-lookup"><span data-stu-id="3a827-119">By pressing **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="3a827-120">DevTools, luego, se detiene en `D` .</span><span class="sxs-lookup"><span data-stu-id="3a827-120">DevTools then pauses on `D`.</span></span>  

### <span data-ttu-id="3a827-121">Ir a la línea de código</span><span class="sxs-lookup"><span data-stu-id="3a827-121">Step into line of code</span></span>   

<span data-ttu-id="3a827-122">Cuando esté pausado en una línea de código que contenga una llamada de función que esté relacionada con el problema que está depurando, haga clic en el icono paso **a paso** ![ por instrucciones ][ImageStepIntoIcon] para investigar la función más.</span><span class="sxs-lookup"><span data-stu-id="3a827-122">When paused on a line of code containing a function call that is related to the problem you are debugging, click on the **Step into** ![Step into][ImageStepIntoIcon] icon to investigate that function further.</span></span>  

> ##### <span data-ttu-id="3a827-123">Figura 2</span><span class="sxs-lookup"><span data-stu-id="3a827-123">Figure 2</span></span>  
> <span data-ttu-id="3a827-124">Seleccionar **paso a paso por instrucciones**</span><span class="sxs-lookup"><span data-stu-id="3a827-124">Selecting **Step into**</span></span>  
> ![Seleccionar paso a paso por instrucciones][ImageSelectingStepInto]  

<span data-ttu-id="3a827-126">Por ejemplo, supongamos que está depurando el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="3a827-126">For example, suppose you are debugging the following code:</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name);
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name;
}
```  

<span data-ttu-id="3a827-127">Estás pausado el `A` .</span><span class="sxs-lookup"><span data-stu-id="3a827-127">You are paused on `A`.</span></span>  <span data-ttu-id="3a827-128">Al presionar **paso a paso por instrucciones**, DevTools ejecuta esta línea de código y luego detiene el `B` .</span><span class="sxs-lookup"><span data-stu-id="3a827-128">By pressing **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <span data-ttu-id="3a827-129">Paso fuera de la línea de código</span><span class="sxs-lookup"><span data-stu-id="3a827-129">Step out of line of code</span></span>   

<span data-ttu-id="3a827-130">Cuando esté pausado dentro de una función que no esté relacionada con el problema que está depurando, haga clic **en el** ![ icono paso a paso ][ImageStepOutIcon] para salir para ejecutar el resto del código de la función.</span><span class="sxs-lookup"><span data-stu-id="3a827-130">When paused inside of a function that is not related to the problem you are debugging, click on the **Step out** ![Step out][ImageStepOutIcon] icon to run the rest of the code of the function.</span></span>  

> ##### <span data-ttu-id="3a827-131">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="3a827-131">Figure 3</span></span>  
> <span data-ttu-id="3a827-132">Selección del **paso salir**</span><span class="sxs-lookup"><span data-stu-id="3a827-132">Selecting **Step out**</span></span>  
> ![Selección del paso salir][ImageSelectingStepOut]  

<span data-ttu-id="3a827-134">Por ejemplo, supongamos que está depurando el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="3a827-134">For example, suppose you are debugging the following code:</span></span>  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName();
    updateName(name); // C
}
function getName() {
    var name = app.first + ' ' + app.last; // A
    return name; // B
}
```  

<span data-ttu-id="3a827-135">Estás pausado el `A` .</span><span class="sxs-lookup"><span data-stu-id="3a827-135">You are paused on `A`.</span></span>  <span data-ttu-id="3a827-136">Si pulsas **paso a paso**, DevTools ejecuta el resto del código de `getName()` , que se encuentra `B` en este ejemplo, y luego realiza una pausa en `C` .</span><span class="sxs-lookup"><span data-stu-id="3a827-136">By pressing **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <span data-ttu-id="3a827-137">Ejecutar todo el código hasta una línea específica</span><span class="sxs-lookup"><span data-stu-id="3a827-137">Run all code up to a specific line</span></span>   

<span data-ttu-id="3a827-138">Cuando se depura una función Long, puede haber una gran cantidad de código que no está relacionado con el problema que se está depurando.</span><span class="sxs-lookup"><span data-stu-id="3a827-138">When debugging a long function, there may be a lot of code that is not related to the problem you are debugging.</span></span>  

<span data-ttu-id="3a827-139">Puede elegir recorrer todas las líneas, pero eso es tedioso.</span><span class="sxs-lookup"><span data-stu-id="3a827-139">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="3a827-140">Puede optar por establecer un punto de interrupción de línea de código en la línea en la que está interesado y, después, hacer clic en el icono de ejecución reanudar la ejecución de la **secuencia de comandos** ![ ][ImageResumeScriptExecutionIcon] , pero hay una forma más rápida.</span><span class="sxs-lookup"><span data-stu-id="3a827-140">You may choose to set a line-of-code breakpoint on the line in which you are interested and then click on the **Resume Script Execution** ![Resume Script Execution][ImageResumeScriptExecutionIcon] icon, but there is a faster way.</span></span>  

<span data-ttu-id="3a827-141">Haga clic con el botón derecho en la línea de código en la que está interesado y seleccione **continuar aquí**.</span><span class="sxs-lookup"><span data-stu-id="3a827-141">Right-click the line of code in which you are interested, and select **Continue to here**.</span></span>  <span data-ttu-id="3a827-142">DevTools ejecuta todo el código hasta ese punto y, después, se detiene en esa línea.</span><span class="sxs-lookup"><span data-stu-id="3a827-142">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

> ##### <span data-ttu-id="3a827-143">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="3a827-143">Figure 4</span></span>  
> <span data-ttu-id="3a827-144">Selecciona **continuar aquí**</span><span class="sxs-lookup"><span data-stu-id="3a827-144">Selecting **Continue to here**</span></span>  
> ![Selecciona continuar aquí][ImageSelectingContinueToHere]  

### <span data-ttu-id="3a827-146">Reiniciar la función superior de la pila de llamadas</span><span class="sxs-lookup"><span data-stu-id="3a827-146">Restart the top function of the call stack</span></span>   

<span data-ttu-id="3a827-147">Mientras esté pausado en una línea de código, haga clic con el botón secundario en cualquier lugar del panel **pila de llamadas** y seleccione **reiniciar marco** para hacer una pausa en la primera línea de la función superior de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="3a827-147">While paused on a line of code, right-click anywhere in the **Call Stack** pane and select **Restart Frame** to pause on the first line of the top function in your call stack.</span></span>  <span data-ttu-id="3a827-148">La función Top es la última función que se llamó.</span><span class="sxs-lookup"><span data-stu-id="3a827-148">The top function is the last function that was called.</span></span>  

<span data-ttu-id="3a827-149">Por ejemplo, supongamos que está recorriendo el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="3a827-149">For example, suppose you are stepping through the following code:</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="3a827-150">Estás pausado el `A` .</span><span class="sxs-lookup"><span data-stu-id="3a827-150">You are paused on `A`.</span></span>  <span data-ttu-id="3a827-151">Después de hacer clic en **Restarted Frame**, debe estar pausado `B` , sin tener que establecer un punto de interrupción ni Pulsar **resume script Execution**.</span><span class="sxs-lookup"><span data-stu-id="3a827-151">After clicking **Restart Frame**, you should be paused on `B`, without ever setting a breakpoint or pressing **Resume script execution**.</span></span>  

> ##### <span data-ttu-id="3a827-152">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="3a827-152">Figure 5</span></span>  
> <span data-ttu-id="3a827-153">Selección del **marco de reinicio**</span><span class="sxs-lookup"><span data-stu-id="3a827-153">Selecting **Restart Frame**</span></span>  
> ![Selección del marco de reinicio][ImageSelectingRestartFrame]  

### <span data-ttu-id="3a827-155">Reanudar script Runtime</span><span class="sxs-lookup"><span data-stu-id="3a827-155">Resume script runtime</span></span>   

<span data-ttu-id="3a827-156">Para continuar el tiempo de ejecución después de una pausa de la secuencia de comandos, haga clic en el icono de ejecución de reanudar **ejecución de script** de reanudación ![ ][ImageResumeScriptExecutionIcon] .</span><span class="sxs-lookup"><span data-stu-id="3a827-156">To continue the runtime after a pause of your script, click on the **Resume Script Execution** ![Resume Script Execution][ImageResumeScriptExecutionIcon] icon.</span></span>  <span data-ttu-id="3a827-157">DevTools ejecuta la secuencia de comandos hasta el siguiente punto de interrupción, si existe.</span><span class="sxs-lookup"><span data-stu-id="3a827-157">DevTools runs the script up until the next breakpoint, if any.</span></span>  

> ##### <span data-ttu-id="3a827-158">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="3a827-158">Figure 6</span></span>  
> <span data-ttu-id="3a827-159">Selección de la **ejecución de reanudar script**</span><span class="sxs-lookup"><span data-stu-id="3a827-159">Selecting **Resume script execution**</span></span>  
> ![Selección de la ejecución de reanudar script][ImageSelectingResumeScriptExecution]  

#### <span data-ttu-id="3a827-161">Tiempo de ejecución de script forzado</span><span class="sxs-lookup"><span data-stu-id="3a827-161">Force script runtime</span></span>   

<span data-ttu-id="3a827-162">Para ignorar todos los puntos de interrupción y forzar la reanudación del script, haga clic y mantenga presionado el icono de ejecución reanudar **ejecución** de script de reanudación de ejecución ![ ][ImageResumeScriptExecutionIcon] y seleccione **forzar ejecución** de script ![ forzar ejecución de script ][ImageForceScriptExecutionIcon] .</span><span class="sxs-lookup"><span data-stu-id="3a827-162">To ignore all breakpoints and force your script to resume running, click and hold the **Resume Script Execution** ![Resume Script Execution][ImageResumeScriptExecutionIcon] icon and then select **Force script execution** ![Force script execution][ImageForceScriptExecutionIcon].</span></span>  

> ##### <span data-ttu-id="3a827-163">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="3a827-163">Figure 7</span></span>  
> <span data-ttu-id="3a827-164">Selección de **forzar ejecución de script**</span><span class="sxs-lookup"><span data-stu-id="3a827-164">Selecting **Force script execution**</span></span>  
> ![Selección de forzar ejecución de script][ImageSelectingForceScriptExecution]  

### <span data-ttu-id="3a827-166">Cambiar el contexto del hilo</span><span class="sxs-lookup"><span data-stu-id="3a827-166">Change thread context</span></span>   

<span data-ttu-id="3a827-167">Cuando trabaje con trabajadores web o trabajos de servicio, haga clic en el contexto que aparece en el panel de **subprocesos** para cambiar a ese contexto.</span><span class="sxs-lookup"><span data-stu-id="3a827-167">When working with web workers or service workers, click on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="3a827-168">El icono de flecha azul representa el contexto que está seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="3a827-168">The blue arrow icon represents which context is currently selected.</span></span>  

> ##### <span data-ttu-id="3a827-169">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="3a827-169">Figure 8</span></span>  
> <span data-ttu-id="3a827-170">El panel de **subprocesos**</span><span class="sxs-lookup"><span data-stu-id="3a827-170">The **Threads** pane</span></span>  
> ![El panel de subprocesos][ImageThreadsPane]  

<span data-ttu-id="3a827-172">Por ejemplo, supongamos que está pausado en un punto de interrupción tanto en el script principal como en el script de trabajo de servicio.</span><span class="sxs-lookup"><span data-stu-id="3a827-172">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="3a827-173">Desea ver las propiedades locales y globales del contexto de trabajo de servicio, pero el panel **orígenes** muestra el contexto de script principal.</span><span class="sxs-lookup"><span data-stu-id="3a827-173">You want to view the local and global properties for the service worker context, but the **Sources** panel is showing the main script context.</span></span>  <span data-ttu-id="3a827-174">Al hacer clic en la entrada de trabajador de servicio en el panel de **subprocesos** , debería poder cambiar a ese contexto.</span><span class="sxs-lookup"><span data-stu-id="3a827-174">By clicking on the service worker entry in the **Threads** pane, you should be able to switch to that context.</span></span>  

## <span data-ttu-id="3a827-175">Ver y editar propiedades locales, de cierre y globales</span><span class="sxs-lookup"><span data-stu-id="3a827-175">View and edit local, closure, and global properties</span></span>   

<span data-ttu-id="3a827-176">Mientras esté pausado en una línea de código, use el panel **ámbito** para ver y editar los valores de las propiedades y variables de los ámbitos local, de cierre y global.</span><span class="sxs-lookup"><span data-stu-id="3a827-176">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="3a827-177">Haga doble clic en un valor de propiedad para cambiarlo.</span><span class="sxs-lookup"><span data-stu-id="3a827-177">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="3a827-178">Las propiedades no enumerables están atenuadas.</span><span class="sxs-lookup"><span data-stu-id="3a827-178">Non-enumerable properties are greyed out.</span></span>  

> ##### <span data-ttu-id="3a827-179">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="3a827-179">Figure 9</span></span>  
> <span data-ttu-id="3a827-180">El panel **ámbito**</span><span class="sxs-lookup"><span data-stu-id="3a827-180">The **Scope** pane</span></span>  
> ![El panel ámbito][ImageScopePane]  

## <span data-ttu-id="3a827-182">Ver la pila de llamadas actual</span><span class="sxs-lookup"><span data-stu-id="3a827-182">View the current call stack</span></span>   

<span data-ttu-id="3a827-183">Mientras esté pausado en una línea de código, use el panel **pila de llamadas** para ver la pila de llamadas que le han llegado a este punto.</span><span class="sxs-lookup"><span data-stu-id="3a827-183">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="3a827-184">Haga clic en una entrada para ir a la línea de código donde se llamó a esa función.</span><span class="sxs-lookup"><span data-stu-id="3a827-184">Click on an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="3a827-185">El icono de flecha azul representa qué función DevTools está resaltando actualmente.</span><span class="sxs-lookup"><span data-stu-id="3a827-185">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

> ##### <span data-ttu-id="3a827-186">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="3a827-186">Figure 10</span></span>  
> <span data-ttu-id="3a827-187">Panel **pila de llamadas**</span><span class="sxs-lookup"><span data-stu-id="3a827-187">The **Call Stack** pane</span></span>  
> ![Panel pila de llamadas][ImageCallStackPane]  

> [!NOTE]
> <span data-ttu-id="3a827-189">Cuando no está pausado en una línea de código, el panel **pila de llamadas** está vacío.</span><span class="sxs-lookup"><span data-stu-id="3a827-189">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <span data-ttu-id="3a827-190">Copiar seguimiento de pila</span><span class="sxs-lookup"><span data-stu-id="3a827-190">Copy stack trace</span></span>   

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="3a827-191">Haga clic con el botón secundario en cualquier lugar del panel de la **pila de llamadas** y seleccione **copiar seguimiento de pila** para copiar la pila de llamadas actual en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="3a827-191">Right-click anywhere in the **Call Stack** pane and select **Copy stack trace** to copy the current call stack to the clipboard.</span></span>  

> ##### <span data-ttu-id="3a827-192">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="3a827-192">Figure 11</span></span>  
> <span data-ttu-id="3a827-193">Selección de **copiar seguimiento** de la pila</span><span class="sxs-lookup"><span data-stu-id="3a827-193">Selecting **Copy Stack Trace**</span></span>  
> ![Selección de copiar seguimiento de la pila][ImageSelectingCopyStackTrace]  

<span data-ttu-id="3a827-195">A continuación se muestra un ejemplo del resultado:</span><span class="sxs-lookup"><span data-stu-id="3a827-195">Below is an example of the output:</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## <span data-ttu-id="3a827-196">Ignorar un script o una trama de scripts</span><span class="sxs-lookup"><span data-stu-id="3a827-196">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="3a827-197">Marque un script como código de biblioteca cuando desee omitir ese script durante la depuración.</span><span class="sxs-lookup"><span data-stu-id="3a827-197">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="3a827-198">Cuando se marca como código de biblioteca, un script se oculta en el panel **pila de llamadas** y nunca se le detallan las funciones de la secuencia de comandos cuando pasa por el código.</span><span class="sxs-lookup"><span data-stu-id="3a827-198">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="3a827-199">Por ejemplo, supongamos que está recorriendo este código:</span><span class="sxs-lookup"><span data-stu-id="3a827-199">For example, suppose you are stepping through this code:</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` <span data-ttu-id="3a827-200">es una biblioteca de terceros en la que confía.</span><span class="sxs-lookup"><span data-stu-id="3a827-200">is a third-party library that you trust.</span></span>  <span data-ttu-id="3a827-201">Si está seguro de que el problema que está depurando no está relacionado con la biblioteca de terceros, tiene sentido marcar el script como **código de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="3a827-201">If you are confident that the problem you are debugging is not related to the third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

### <span data-ttu-id="3a827-202">Marcar un script como código de biblioteca desde el panel Editor</span><span class="sxs-lookup"><span data-stu-id="3a827-202">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="3a827-203">Para marcar un script como **código de biblioteca** desde el panel **Editor** :</span><span class="sxs-lookup"><span data-stu-id="3a827-203">To mark a script as **Library code** from the **Editor** pane:</span></span>  

1.  <span data-ttu-id="3a827-204">Abra el archivo.</span><span class="sxs-lookup"><span data-stu-id="3a827-204">Open the file.</span></span>  
1.  <span data-ttu-id="3a827-205">Haga clic con el botón derecho en cualquier parte.</span><span class="sxs-lookup"><span data-stu-id="3a827-205">Right-click anywhere.</span></span>  
1.  <span data-ttu-id="3a827-206">Seleccione **marcar como código de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="3a827-206">Select **Mark as Library code**.</span></span>  

> ##### <span data-ttu-id="3a827-207">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="3a827-207">Figure 12</span></span>  
> <span data-ttu-id="3a827-208">Marcar un script como **código de biblioteca** desde el panel **Editor**</span><span class="sxs-lookup"><span data-stu-id="3a827-208">Marking a script as **Library code** from the **Editor** pane</span></span>  
> ![Marcar un script como código de biblioteca desde el panel Editor][ImageMarkEditorPane]  

### <span data-ttu-id="3a827-210">Marcar un script como código de biblioteca desde el panel de pila de llamadas</span><span class="sxs-lookup"><span data-stu-id="3a827-210">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="3a827-211">Para marcar un script como **código de biblioteca** desde el panel **pila de llamadas** :</span><span class="sxs-lookup"><span data-stu-id="3a827-211">To mark a script as **Library code** from the **Call Stack** pane:</span></span>  

1.  <span data-ttu-id="3a827-212">Haga clic con el botón derecho en una función de la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="3a827-212">Right-click on a function from the script.</span></span>  
1.  <span data-ttu-id="3a827-213">Seleccione **marcar como código de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="3a827-213">Select **Mark as Library code**.</span></span>  

> ##### <span data-ttu-id="3a827-214">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="3a827-214">Figure 13</span></span>  
> <span data-ttu-id="3a827-215">Marcar un script como **código de biblioteca** desde el panel **pila de llamadas**</span><span class="sxs-lookup"><span data-stu-id="3a827-215">Marking a script as **Library code** from the **Call Stack** pane</span></span>  
> ![Marcar un script como código de biblioteca desde el panel pila de llamadas][ImageMarkCallStackPane]  

### <span data-ttu-id="3a827-217">Marcar un script como código de biblioteca desde la configuración</span><span class="sxs-lookup"><span data-stu-id="3a827-217">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="3a827-218">Para marcar un único script o patrón de scripts de la configuración:</span><span class="sxs-lookup"><span data-stu-id="3a827-218">To mark a single script or pattern of scripts from Settings:</span></span>  

1.  <span data-ttu-id="3a827-219">Abra [configuración][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="3a827-219">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="3a827-220">Vaya a la pestaña **código de biblioteca** .</span><span class="sxs-lookup"><span data-stu-id="3a827-220">Go to the **Library code** tab.</span></span>  
1.  <span data-ttu-id="3a827-221">Haga clic en **Agregar patrón**.</span><span class="sxs-lookup"><span data-stu-id="3a827-221">Click **Add pattern**.</span></span>  
1.  <span data-ttu-id="3a827-222">Escriba el nombre del script o un patrón de Regex de nombres de script para marcarlo como **código de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="3a827-222">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="3a827-223">Haz clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="3a827-223">Click **Add**.</span></span>  

> ##### <span data-ttu-id="3a827-224">Imagen 14</span><span class="sxs-lookup"><span data-stu-id="3a827-224">Figure 14</span></span>  
> <span data-ttu-id="3a827-225">Marcar un script como **código de biblioteca** desde la configuración</span><span class="sxs-lookup"><span data-stu-id="3a827-225">Marking a script as **Library code** from Settings</span></span>  
> ![Marcar un script como código de biblioteca desde la configuración][ImageMarkScriptSettings]  

## <span data-ttu-id="3a827-227">Ejecutar fragmentos de código de depuración desde cualquier página</span><span class="sxs-lookup"><span data-stu-id="3a827-227">Run snippets of debug code from any page</span></span>   

<span data-ttu-id="3a827-228">Si se encuentra ejecutando el mismo código de depuración en la consola una y otra vez, considere la posibilidad de recortes.</span><span class="sxs-lookup"><span data-stu-id="3a827-228">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="3a827-229">Los fragmentos de código son scripts de tiempo de ejecución que usted crea, almacena y ejecuta dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="3a827-229">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="3a827-230">Vea [Ejecutar fragmentos de código desde cualquier página][DevToolsJavascriptSnippets] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="3a827-230">See [Run Snippets of Code From Any Page][DevToolsJavascriptSnippets] to learn more.</span></span>  

## <span data-ttu-id="3a827-231">Ver los valores de las expresiones de JavaScript personalizadas</span><span class="sxs-lookup"><span data-stu-id="3a827-231">Watch the values of custom JavaScript expressions</span></span>   

<span data-ttu-id="3a827-232">Use el panel **inspección** para ver los valores de expresiones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="3a827-232">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="3a827-233">Puede ver cualquier expresión válida de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3a827-233">You may watch any valid JavaScript expression.</span></span>  

> ##### <span data-ttu-id="3a827-234">Imagen 15</span><span class="sxs-lookup"><span data-stu-id="3a827-234">Figure 15</span></span>  
> <span data-ttu-id="3a827-235">Panel de **inspección**</span><span class="sxs-lookup"><span data-stu-id="3a827-235">The **Watch** pane</span></span>  
> ![Panel de inspección][ImageWatchPane]  

*   <span data-ttu-id="3a827-237">Haga clic en el icono **Agregar** expresión de ![ adición de expresión ][ImageAddExpressionIcon] para crear una nueva expresión de inspección.</span><span class="sxs-lookup"><span data-stu-id="3a827-237">Click on the **Add Expression** ![Add Expression][ImageAddExpressionIcon] icon to create a new watch expression.</span></span>  
*   <span data-ttu-id="3a827-238">Haga clic en el icono **Actualizar** ![ actualización ][ImageRefreshIcon] para actualizar los valores de todas las expresiones existentes.</span><span class="sxs-lookup"><span data-stu-id="3a827-238">Click on the **Refresh** ![Refresh][ImageRefreshIcon] icon to refresh the values of all existing expressions.</span></span>  <span data-ttu-id="3a827-239">Los valores se actualizan automáticamente al recorrer el código.</span><span class="sxs-lookup"><span data-stu-id="3a827-239">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="3a827-240">Desplace el puntero sobre una expresión y haga clic en el icono Eliminar expresión para eliminar **una expresión** ![ ][ImageDeleteExpressionIcon] para eliminarla.</span><span class="sxs-lookup"><span data-stu-id="3a827-240">Hover over an expression and click on the **Delete Expression** ![Delete Expression][ImageDeleteExpressionIcon] icon to delete it.</span></span>  

## <span data-ttu-id="3a827-241">Hacer que un archivo minified sea legible</span><span class="sxs-lookup"><span data-stu-id="3a827-241">Make a minified file readable</span></span>   

<span data-ttu-id="3a827-242">Haga clic en el icono formato **de formato** ![ para que ][ImageFormatIcon] un archivo minified sea legible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="3a827-242">Click on the **Format** ![Format][ImageFormatIcon] icon to make a minified file human-readable.</span></span>  

> ##### <span data-ttu-id="3a827-243">Imagen 16</span><span class="sxs-lookup"><span data-stu-id="3a827-243">Figure 16</span></span>  
> <span data-ttu-id="3a827-244">El botón **formato**</span><span class="sxs-lookup"><span data-stu-id="3a827-244">The **Format** button</span></span>  
> ![El botón formato][ImageFormat]  

## <span data-ttu-id="3a827-246">Editar un script</span><span class="sxs-lookup"><span data-stu-id="3a827-246">Edit a script</span></span>   

<span data-ttu-id="3a827-247">Al corregir un error, a menudo desearás probar algunos cambios en el código de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3a827-247">When fixing a bug, you often want to test out some changes to your JavaScript code.</span></span>  <span data-ttu-id="3a827-248">No es necesario realizar los cambios en un editor externo o IDE y, a continuación, volver a cargar la página.</span><span class="sxs-lookup"><span data-stu-id="3a827-248">You do not need to make the changes in an external editor or IDE and then reload the page.</span></span>  <span data-ttu-id="3a827-249">Puede editar su script en DevTools.</span><span class="sxs-lookup"><span data-stu-id="3a827-249">You may edit your script in DevTools.</span></span>  

<span data-ttu-id="3a827-250">Para editar un script:</span><span class="sxs-lookup"><span data-stu-id="3a827-250">To edit a script:</span></span>  

1.  <span data-ttu-id="3a827-251">Abra el archivo en el panel **Editor** del panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="3a827-251">Open the file in the **Editor** pane of the **Sources** panel.</span></span>  
1.  <span data-ttu-id="3a827-252">Realice los cambios en el panel **Editor** .</span><span class="sxs-lookup"><span data-stu-id="3a827-252">Make your changes in the **Editor** pane.</span></span>  
1.  <span data-ttu-id="3a827-253">Pulse `Ctrl` + `S` \ (Windows \) o `Command` + `S` \ (MacOS \) para guardar.</span><span class="sxs-lookup"><span data-stu-id="3a827-253">Press `Ctrl`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="3a827-254">DevTools revisa todo el archivo JS en el motor de JavaScript de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3a827-254">DevTools patches the entire JS file into the JavaScript engine of Microsoft Edge.</span></span>  

> ##### <span data-ttu-id="3a827-255">Imagen 17</span><span class="sxs-lookup"><span data-stu-id="3a827-255">Figure 17</span></span>  
> <span data-ttu-id="3a827-256">El panel **Editor**</span><span class="sxs-lookup"><span data-stu-id="3a827-256">The **Editor** pane</span></span>  
> ![El panel Editor][ImageEditorPane]  

## <span data-ttu-id="3a827-258">Deshabilitar JavaScript</span><span class="sxs-lookup"><span data-stu-id="3a827-258">Disable JavaScript</span></span>   

<span data-ttu-id="3a827-259">Consulte [deshabilitar JavaScript con Microsoft Edge DevTools][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="3a827-259">See [Disable JavaScript With Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageStepOverIcon]: /microsoft-edge/devtools-guide-chromium/media/step-over-icon.msft.png  
[ImageStepIntoIcon]: /microsoft-edge/devtools-guide-chromium/media/step-into-icon.msft.png  
[ImageStepOutIcon]: /microsoft-edge/devtools-guide-chromium/media/step-out-icon.msft.png  
[ImageResumeScriptExecutionIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-run-icon.msft.png  
[ImageForceScriptExecutionIcon]: /microsoft-edge/devtools-guide-chromium/media/force-script-run-icon.msft.png  
[ImageAddExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/add-expression-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageDeleteExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-expression-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  

[ImageSelectingStepOver]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-over-next-function-call.msft.png "Ilustración 1: selección de paso a paso por procedimientos"  
[ImageSelectingStepInto]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-into-next-function-call.msft.png "Ilustración 2: selección de paso a paso por instrucciones"  
[ImageSelectingStepOut]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-out-of-current-function.msft.png "Ilustración 3: selección del paso"  
[ImageSelectingContinueToHere]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-continue-to-here.msft.png "Ilustración 4: seleccionar la opción continuar aquí"  
[ImageSelectingRestartFrame]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-restart-frame.msft.png "Ilustración 5: seleccionar el marco de reinicio"  
[ImageSelectingResumeScriptExecution]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-resume-script-runtime.msft.png "Ilustración 6: selección de la ejecución de la secuencia de reanudación"  
[ImageSelectingForceScriptExecution]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-force-script-runtime.msft.png "Ilustración 7: selección de la ejecución de la secuencia de comandos forzar"  
[ImageThreadsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-main-min-js-threads.msft.png "Ilustración 8: el panel de subprocesos"  
[ImageScopePane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-scope.msft.png "Ilustración 9: el panel ámbito"  
[ImageCallStackPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png "Ilustración 10: el panel de pila de llamadas"  
[ImageSelectingCopyStackTrace]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png "Ilustración 11: selección de seguimiento de la pila de copia"  
[ImageMarkEditorPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png "Ilustración 12: marcar un script como código de biblioteca desde el panel Editor"  
[ImageMarkCallStackPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png "Ilustración 13: marcar un script como código de biblioteca desde el panel pila de llamadas"  
[ImageMarkScriptSettings]: /microsoft-edge/devtools-guide-chromium/media/javascript-framework-library-code.msft.png "Ilustración 14: marcar una secuencia de comandos como código de biblioteca desde la configuración"  
[ImageWatchPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-watch.msft.png "Ilustración 15: el panel de inspección"  
[ImageFormat]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-html-non-minified.msft.png "Ilustración 16: el botón formato"  
[ImageEditorPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-html-minified.msft.png "Ilustración 17: el panel Editor"  

<!-- links -->  

[DevToolsJavascriptDisable]: disable.md "Deshabilitar JavaScript con Microsoft Edge DevTools"  
[DevToolsJavascriptGetStarted]: index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools"  
[DevToolsJavascriptSnippets]: snippets.md "Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools"  

[DevToolsCustomize]: ../customize/index.md "Personalizar Microsoft Edge DevTools"  

> [!NOTE]
> <span data-ttu-id="3a827-281">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3a827-281">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3a827-282">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="3a827-282">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3a827-284">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3a827-284">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

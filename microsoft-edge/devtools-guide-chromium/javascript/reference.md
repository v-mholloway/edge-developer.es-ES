---
title: Referencia de depuración de JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: a6ec2438457c81ed527154af30c9642d5c287d3c
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991213"
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

# <span data-ttu-id="8a26a-103">Referencia de febugging de JavaScript</span><span class="sxs-lookup"><span data-stu-id="8a26a-103">JavaScript febugging reference</span></span>  

<span data-ttu-id="8a26a-104">Descubra nuevos flujos de trabajo de depuración con la siguiente referencia completa de las características de depuración de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="8a26a-104">Discover new debugging workflows with the following comprehensive reference of Microsoft Edge DevTools debugging features.</span></span>  

<span data-ttu-id="8a26a-105">Consulta Introducción a la [depuración de JavaScript en Microsoft Edge DevTools][DevToolsJavascriptGetStarted] para conocer los conceptos básicos de la depuración.</span><span class="sxs-lookup"><span data-stu-id="8a26a-105">See [Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted] to learn the basics of debugging.</span></span>  

## <span data-ttu-id="8a26a-106">Pausar código con puntos de interrupción</span><span class="sxs-lookup"><span data-stu-id="8a26a-106">Pause code with breakpoints</span></span>  

<span data-ttu-id="8a26a-107">Establezca un punto de interrupción para que pueda pausar el código en el medio del Runtime.</span><span class="sxs-lookup"><span data-stu-id="8a26a-107">Set a breakpoint so that you are able to pause your code in the middle of the runtime.</span></span>  

<span data-ttu-id="8a26a-108">Vea [pausar el código con puntos de interrupción][DevToolsJavascriptBreakpoints] para obtener información sobre cómo establecer puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="8a26a-108">See [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints] to learn how to set breakpoints.</span></span>  

## <span data-ttu-id="8a26a-109">Recorrer el código</span><span class="sxs-lookup"><span data-stu-id="8a26a-109">Step through code</span></span>  

<span data-ttu-id="8a26a-110">Una vez que el código esté pausado, recorralo, de una línea a la vez, investigando el flujo de control y los valores de propiedad durante el proceso.</span><span class="sxs-lookup"><span data-stu-id="8a26a-110">Once your code is paused, step through it, one line at a time, investigating control flow and property values along the way.</span></span>  

### <span data-ttu-id="8a26a-111">Paso a paso por la línea de código</span><span class="sxs-lookup"><span data-stu-id="8a26a-111">Step over line of code</span></span>  

<span data-ttu-id="8a26a-112">Cuando esté pausado en una línea de código que contenga una función que no sea relevante para el problema que está depurando, haga clic en el botón **paso a paso por procedimientos** \ ( ![ paso a paso por procedimientos ][ImageStepOverIcon] ) para ejecutar la función sin entrar en ella.</span><span class="sxs-lookup"><span data-stu-id="8a26a-112">When paused on a line of code containing a function that is not relevant to the problem you are debugging, click the **Step over** \(![Step over][ImageStepOverIcon]\) button to run the function without stepping into it.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Seleccione recorrer" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   <span data-ttu-id="8a26a-114">Seleccione **recorrer**</span><span class="sxs-lookup"><span data-stu-id="8a26a-114">Select **Step over**</span></span>  
:::image-end:::  

<span data-ttu-id="8a26a-115">Por ejemplo, supongamos que está depurando el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="8a26a-115">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="8a26a-116">Estás pausado el `A` .</span><span class="sxs-lookup"><span data-stu-id="8a26a-116">You are paused on `A`.</span></span>  <span data-ttu-id="8a26a-117">Si pulsas **paso a paso**, DevTools ejecuta todo el código de la función que estás recorriendo, que `B` es `C` y.</span><span class="sxs-lookup"><span data-stu-id="8a26a-117">By pressing **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="8a26a-118">DevTools, luego, se detiene en `D` .</span><span class="sxs-lookup"><span data-stu-id="8a26a-118">DevTools then pauses on `D`.</span></span>  

### <span data-ttu-id="8a26a-119">Ir a la línea de código</span><span class="sxs-lookup"><span data-stu-id="8a26a-119">Step into line of code</span></span>  

<span data-ttu-id="8a26a-120">Cuando esté pausado en una línea de código que contenga una llamada de función relacionada con el problema que está depurando, haga clic en el botón **ir al paso** \ ( ![ paso a paso ][ImageStepIntoIcon] \) para investigar la función más.</span><span class="sxs-lookup"><span data-stu-id="8a26a-120">When paused on a line of code containing a function call that is related to the problem you are debugging, click the **Step into** \(![Step into][ImageStepIntoIcon]\) button to investigate that function further.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Seleccione ir a" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   <span data-ttu-id="8a26a-122">Seleccione **ir a**</span><span class="sxs-lookup"><span data-stu-id="8a26a-122">Select **Step into**</span></span>  
:::image-end:::  

<span data-ttu-id="8a26a-123">Por ejemplo, supongamos que está depurando el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="8a26a-123">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="8a26a-124">Estás pausado el `A` .</span><span class="sxs-lookup"><span data-stu-id="8a26a-124">You are paused on `A`.</span></span>  <span data-ttu-id="8a26a-125">Al presionar **paso a paso por instrucciones**, DevTools ejecuta esta línea de código y luego detiene el `B` .</span><span class="sxs-lookup"><span data-stu-id="8a26a-125">By pressing **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <span data-ttu-id="8a26a-126">Paso fuera de la línea de código</span><span class="sxs-lookup"><span data-stu-id="8a26a-126">Step out of line of code</span></span>  

<span data-ttu-id="8a26a-127">Cuando esté pausado dentro de una función que no esté relacionada con el problema que está depurando, haga clic en el botón **\ (** ![ paso salir ][ImageStepOutIcon] \) para ejecutar el resto del código de la función.</span><span class="sxs-lookup"><span data-stu-id="8a26a-127">When paused inside of a function that is not related to the problem you are debugging, click the **Step out** \(![Step out][ImageStepOutIcon]\) button to run the rest of the code of the function.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Seleccione salir" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   <span data-ttu-id="8a26a-129">Seleccione **salir**</span><span class="sxs-lookup"><span data-stu-id="8a26a-129">Select **Step out**</span></span>  
:::image-end:::  

<span data-ttu-id="8a26a-130">Por ejemplo, supongamos que está depurando el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="8a26a-130">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="8a26a-131">Estás pausado el `A` .</span><span class="sxs-lookup"><span data-stu-id="8a26a-131">You are paused on `A`.</span></span>  <span data-ttu-id="8a26a-132">Si pulsas **paso a paso**, DevTools ejecuta el resto del código de `getName()` , que se encuentra `B` en este ejemplo, y luego realiza una pausa en `C` .</span><span class="sxs-lookup"><span data-stu-id="8a26a-132">By pressing **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <span data-ttu-id="8a26a-133">Ejecutar todo el código hasta una línea específica</span><span class="sxs-lookup"><span data-stu-id="8a26a-133">Run all code up to a specific line</span></span>  

<span data-ttu-id="8a26a-134">Cuando se depura una función Long, puede haber una gran cantidad de código que no está relacionado con el problema que se está depurando.</span><span class="sxs-lookup"><span data-stu-id="8a26a-134">When debugging a long function, there may be a lot of code that is not related to the problem you are debugging.</span></span>  

<span data-ttu-id="8a26a-135">Puede elegir recorrer todas las líneas, pero eso es tedioso.</span><span class="sxs-lookup"><span data-stu-id="8a26a-135">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="8a26a-136">Puede optar por establecer un punto de interrupción de línea de código en la línea en la que está interesado y, a continuación, hacer clic en el botón **reanudar ejecución de script** \ ( ![ resume script Execution ][ImageResumeScriptExecutionIcon] \), pero hay una forma más rápida.</span><span class="sxs-lookup"><span data-stu-id="8a26a-136">You may choose to set a line-of-code breakpoint on the line in which you are interested and then click the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button, but there is a faster way.</span></span>  

<span data-ttu-id="8a26a-137">Haga clic con el botón derecho en la línea de código en la que está interesado y seleccione **continuar aquí**.</span><span class="sxs-lookup"><span data-stu-id="8a26a-137">Right-click the line of code in which you are interested, and select **Continue to here**.</span></span>  <span data-ttu-id="8a26a-138">DevTools ejecuta todo el código hasta ese punto y, después, se detiene en esa línea.</span><span class="sxs-lookup"><span data-stu-id="8a26a-138">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Seleccione continuar aquí" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   <span data-ttu-id="8a26a-140">Seleccione **continuar aquí**</span><span class="sxs-lookup"><span data-stu-id="8a26a-140">Select **Continue to here**</span></span>  
:::image-end:::  

### <span data-ttu-id="8a26a-141">Reiniciar la función superior de la pila de llamadas</span><span class="sxs-lookup"><span data-stu-id="8a26a-141">Restart the top function of the call stack</span></span>  

<span data-ttu-id="8a26a-142">Mientras esté pausado en una línea de código, haga clic con el botón secundario en cualquier lugar del panel **pila de llamadas** y seleccione **reiniciar marco** para hacer una pausa en la primera línea de la función superior de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="8a26a-142">While paused on a line of code, right-click anywhere in the **Call Stack** pane and select **Restart Frame** to pause on the first line of the top function in your call stack.</span></span>  <span data-ttu-id="8a26a-143">La función Top es la última función que se ejecutó.</span><span class="sxs-lookup"><span data-stu-id="8a26a-143">The top function is the last function that was run.</span></span>  

<span data-ttu-id="8a26a-144">El siguiente fragmento de código es un ejemplo de paso a paso.</span><span class="sxs-lookup"><span data-stu-id="8a26a-144">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="8a26a-145">Estás pausado el `A` .</span><span class="sxs-lookup"><span data-stu-id="8a26a-145">You are paused on `A`.</span></span>  <span data-ttu-id="8a26a-146">Después de hacer clic en **Restarted Frame**, debe estar pausado `B` , sin tener que establecer un punto de interrupción ni Pulsar **resume script Execution**.</span><span class="sxs-lookup"><span data-stu-id="8a26a-146">After clicking **Restart Frame**, you should be paused on `B`, without ever setting a breakpoint or pressing **Resume script execution**.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Seleccionar el marco de reinicio" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   <span data-ttu-id="8a26a-148">Seleccionar el **marco de reinicio**</span><span class="sxs-lookup"><span data-stu-id="8a26a-148">Select **Restart Frame**</span></span>  
:::image-end:::  

### <span data-ttu-id="8a26a-149">Reanudar script Runtime</span><span class="sxs-lookup"><span data-stu-id="8a26a-149">Resume script runtime</span></span>  

<span data-ttu-id="8a26a-150">Para continuar el tiempo de ejecución después de una pausa de la secuencia de comandos, haga clic en el botón **reanudar ejecución** de script \ ( ![ resume script Execution ][ImageResumeScriptExecutionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="8a26a-150">To continue the runtime after a pause of your script, click the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button.</span></span>  <span data-ttu-id="8a26a-151">DevTools ejecuta la secuencia de comandos hasta el siguiente punto de interrupción, si existe.</span><span class="sxs-lookup"><span data-stu-id="8a26a-151">DevTools runs the script up until the next breakpoint, if any.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Seleccione reanudar script Execution" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   <span data-ttu-id="8a26a-153">Seleccione **reanudar script Execution**</span><span class="sxs-lookup"><span data-stu-id="8a26a-153">Select **Resume script execution**</span></span>  
:::image-end:::  

#### <span data-ttu-id="8a26a-154">Tiempo de ejecución de script forzado</span><span class="sxs-lookup"><span data-stu-id="8a26a-154">Force script runtime</span></span>  

<span data-ttu-id="8a26a-155">Para ignorar todos los puntos de interrupción y forzar la reanudación de su script, haga clic y mantenga presionado el botón **reanudar** ejecución de script \ ( ![ reanudar ejecución de script \ ][ImageResumeScriptExecutionIcon] ) y, a continuación, seleccione el botón **forzar** ejecución de script \ ( ![ forzar ejecución de scripts ][ImageForceScriptExecutionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="8a26a-155">To ignore all breakpoints and force your script to resume running, click and hold the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button and then select the **Force script execution** \(![Force script execution][ImageForceScriptExecutionIcon]\) button.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Seleccione forzar ejecución de script" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   <span data-ttu-id="8a26a-157">Seleccione **forzar ejecución de script**</span><span class="sxs-lookup"><span data-stu-id="8a26a-157">Select **Force script execution**</span></span>  
:::image-end:::  

### <span data-ttu-id="8a26a-158">Cambiar el contexto del hilo</span><span class="sxs-lookup"><span data-stu-id="8a26a-158">Change thread context</span></span>  

<span data-ttu-id="8a26a-159">Cuando trabaje con trabajadores web o trabajos de servicio, haga clic en el contexto que aparece en el panel de **subprocesos** para cambiar a ese contexto.</span><span class="sxs-lookup"><span data-stu-id="8a26a-159">When working with web workers or service workers, click on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="8a26a-160">El icono de flecha azul representa el contexto que está seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="8a26a-160">The blue arrow icon represents which context is currently selected.</span></span>  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="El panel de subprocesos" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   <span data-ttu-id="8a26a-162">El panel de **subprocesos**</span><span class="sxs-lookup"><span data-stu-id="8a26a-162">The **Threads** pane</span></span>  
:::image-end:::  

<span data-ttu-id="8a26a-163">Por ejemplo, supongamos que está pausado en un punto de interrupción tanto en el script principal como en el script de trabajo de servicio.</span><span class="sxs-lookup"><span data-stu-id="8a26a-163">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="8a26a-164">Desea ver las propiedades locales y globales del contexto de trabajo de servicio, pero el panel **orígenes** muestra el contexto de script principal.</span><span class="sxs-lookup"><span data-stu-id="8a26a-164">You want to view the local and global properties for the service worker context, but the **Sources** panel is showing the main script context.</span></span>  <span data-ttu-id="8a26a-165">Al hacer clic en la entrada de trabajador de servicio en el panel de **subprocesos** , debería poder cambiar a ese contexto.</span><span class="sxs-lookup"><span data-stu-id="8a26a-165">By clicking on the service worker entry in the **Threads** pane, you should be able to switch to that context.</span></span>  

## <span data-ttu-id="8a26a-166">Ver y editar propiedades locales, de cierre y globales</span><span class="sxs-lookup"><span data-stu-id="8a26a-166">View and edit local, closure, and global properties</span></span>  

<span data-ttu-id="8a26a-167">Mientras esté pausado en una línea de código, use el panel **ámbito** para ver y editar los valores de las propiedades y variables de los ámbitos local, de cierre y global.</span><span class="sxs-lookup"><span data-stu-id="8a26a-167">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="8a26a-168">Haga doble clic en un valor de propiedad para cambiarlo.</span><span class="sxs-lookup"><span data-stu-id="8a26a-168">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="8a26a-169">Las propiedades no enumerables están atenuadas.</span><span class="sxs-lookup"><span data-stu-id="8a26a-169">Non-enumerable properties are greyed out.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="El panel ámbito" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   <span data-ttu-id="8a26a-171">El panel **ámbito**</span><span class="sxs-lookup"><span data-stu-id="8a26a-171">The **Scope** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="8a26a-172">Ver la pila de llamadas actual</span><span class="sxs-lookup"><span data-stu-id="8a26a-172">View the current call stack</span></span>  

<span data-ttu-id="8a26a-173">Mientras esté pausado en una línea de código, use el panel **pila de llamadas** para ver la pila de llamadas que le han llegado a este punto.</span><span class="sxs-lookup"><span data-stu-id="8a26a-173">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="8a26a-174">Haga clic en una entrada para ir a la línea de código donde se llamó a esa función.</span><span class="sxs-lookup"><span data-stu-id="8a26a-174">Click on an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="8a26a-175">El icono de flecha azul representa qué función DevTools está resaltando actualmente.</span><span class="sxs-lookup"><span data-stu-id="8a26a-175">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Panel pila de llamadas" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   <span data-ttu-id="8a26a-177">Panel **pila de llamadas**</span><span class="sxs-lookup"><span data-stu-id="8a26a-177">The **Call Stack** pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="8a26a-178">Cuando no está pausado en una línea de código, el panel **pila de llamadas** está vacío.</span><span class="sxs-lookup"><span data-stu-id="8a26a-178">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <span data-ttu-id="8a26a-179">Copiar seguimiento de pila</span><span class="sxs-lookup"><span data-stu-id="8a26a-179">Copy stack trace</span></span>  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="8a26a-180">Haga clic con el botón secundario en cualquier lugar del panel de la **pila de llamadas** y seleccione **copiar seguimiento de pila** para copiar la pila de llamadas actual en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="8a26a-180">Right-click anywhere in the **Call Stack** pane and select **Copy stack trace** to copy the current call stack to the clipboard.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Seleccione copiar seguimiento de pila" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   <span data-ttu-id="8a26a-182">Seleccione **copiar seguimiento de pila**</span><span class="sxs-lookup"><span data-stu-id="8a26a-182">Select **Copy Stack Trace**</span></span>  
:::image-end:::  

<span data-ttu-id="8a26a-183">El siguiente fragmento de código es un ejemplo de la salida.</span><span class="sxs-lookup"><span data-stu-id="8a26a-183">The following code snippet is an example of the output.</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## <span data-ttu-id="8a26a-184">Ignorar un script o una trama de scripts</span><span class="sxs-lookup"><span data-stu-id="8a26a-184">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="8a26a-185">Marque un script como código de biblioteca cuando desee omitir ese script durante la depuración.</span><span class="sxs-lookup"><span data-stu-id="8a26a-185">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="8a26a-186">Cuando se marca como código de biblioteca, un script se oculta en el panel **pila de llamadas** y nunca se le detallan las funciones de la secuencia de comandos cuando pasa por el código.</span><span class="sxs-lookup"><span data-stu-id="8a26a-186">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="8a26a-187">El siguiente fragmento de código es un ejemplo de paso a paso.</span><span class="sxs-lookup"><span data-stu-id="8a26a-187">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` <span data-ttu-id="8a26a-188">es una biblioteca de terceros en la que confía.</span><span class="sxs-lookup"><span data-stu-id="8a26a-188">is a third-party library that you trust.</span></span>  <span data-ttu-id="8a26a-189">Si está seguro de que el problema que está depurando no está relacionado con la biblioteca de terceros, tiene sentido marcar el script como **código de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="8a26a-189">If you are confident that the problem you are debugging is not related to the third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

### <span data-ttu-id="8a26a-190">Marcar un script como código de biblioteca desde el panel Editor</span><span class="sxs-lookup"><span data-stu-id="8a26a-190">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="8a26a-191">Complete las acciones siguientes para marcar un script como **código de biblioteca** desde el panel **Editor** .</span><span class="sxs-lookup"><span data-stu-id="8a26a-191">Complete the following actions to mark a script as **Library code** from the **Editor** pane.</span></span>  

1.  <span data-ttu-id="8a26a-192">Abra el archivo.</span><span class="sxs-lookup"><span data-stu-id="8a26a-192">Open the file.</span></span>  
1.  <span data-ttu-id="8a26a-193">Haga clic con el botón derecho en cualquier parte.</span><span class="sxs-lookup"><span data-stu-id="8a26a-193">Right-click anywhere.</span></span>  
1.  <span data-ttu-id="8a26a-194">Seleccione **marcar como código de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="8a26a-194">Select **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde el panel Editor" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       <span data-ttu-id="8a26a-196">Marcar un script como **código de biblioteca** desde el panel **Editor**</span><span class="sxs-lookup"><span data-stu-id="8a26a-196">Mark a script as **Library code** from the **Editor** pane</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="8a26a-197">Marcar un script como código de biblioteca desde el panel de pila de llamadas</span><span class="sxs-lookup"><span data-stu-id="8a26a-197">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="8a26a-198">Compelte las acciones de folliwng para marcar un script como **código de biblioteca** desde el panel pila de **llamadas** .</span><span class="sxs-lookup"><span data-stu-id="8a26a-198">Compelte the folliwng actions to mark a script as **Library code** from the **Call Stack** pane.</span></span>  

1.  <span data-ttu-id="8a26a-199">Haga clic con el botón derecho en una función de la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="8a26a-199">Right-click on a function from the script.</span></span>  
1.  <span data-ttu-id="8a26a-200">Seleccione **marcar como código de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="8a26a-200">Select **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde el panel de pila de llamadas" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       <span data-ttu-id="8a26a-202">Marcar un script como **código de biblioteca** desde el panel de **pila de llamadas**</span><span class="sxs-lookup"><span data-stu-id="8a26a-202">Mark a script as **Library code** from the **Call Stack** pane</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="8a26a-203">Marcar un script como código de biblioteca desde la configuración</span><span class="sxs-lookup"><span data-stu-id="8a26a-203">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="8a26a-204">Complete las siguientes acciones para marcar un único script o patrón de scripts de la **configuración**.</span><span class="sxs-lookup"><span data-stu-id="8a26a-204">Complete the following actions to mark a single script or pattern of scripts from **Settings**.</span></span>  

1.  <span data-ttu-id="8a26a-205">Abra [configuración][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="8a26a-205">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="8a26a-206">Vaya a la pestaña **código de biblioteca** .</span><span class="sxs-lookup"><span data-stu-id="8a26a-206">Go to the **Library code** tab.</span></span>  
1.  <span data-ttu-id="8a26a-207">Haga clic en **Agregar patrón**.</span><span class="sxs-lookup"><span data-stu-id="8a26a-207">Click **Add pattern**.</span></span>  
1.  <span data-ttu-id="8a26a-208">Escriba el nombre del script o un patrón de Regex de nombres de script para marcarlo como **código de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="8a26a-208">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="8a26a-209">Haz clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="8a26a-209">Click **Add**.</span></span>  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde la configuración" lightbox="../media/javascript-framework-library-code.msft.png":::
       <span data-ttu-id="8a26a-211">Marcar un script como **código de biblioteca** desde la **configuración**</span><span class="sxs-lookup"><span data-stu-id="8a26a-211">Mark a script as **Library code** from **Settings**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="8a26a-212">Ejecutar fragmentos de código de depuración desde cualquier página</span><span class="sxs-lookup"><span data-stu-id="8a26a-212">Run snippets of debug code from any page</span></span>   

<span data-ttu-id="8a26a-213">Si se encuentra ejecutando el mismo código de depuración en la consola una y otra vez, considere la posibilidad de recortes.</span><span class="sxs-lookup"><span data-stu-id="8a26a-213">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="8a26a-214">Los fragmentos de código son scripts de tiempo de ejecución que usted crea, almacena y ejecuta dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="8a26a-214">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="8a26a-215">Vea [Ejecutar fragmentos de código desde cualquier página][DevToolsJavascriptSnippets] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8a26a-215">See [Run Snippets of Code From Any Page][DevToolsJavascriptSnippets] to learn more.</span></span>  

## <span data-ttu-id="8a26a-216">Ver los valores de las expresiones de JavaScript personalizadas</span><span class="sxs-lookup"><span data-stu-id="8a26a-216">Watch the values of custom JavaScript expressions</span></span>  

<span data-ttu-id="8a26a-217">Use el panel **inspección** para ver los valores de expresiones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="8a26a-217">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="8a26a-218">Puede ver cualquier expresión válida de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8a26a-218">You may watch any valid JavaScript expression.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="Panel de inspección" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   <span data-ttu-id="8a26a-220">Panel de **inspección**</span><span class="sxs-lookup"><span data-stu-id="8a26a-220">The **Watch** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="8a26a-221">Haga clic en el botón **Agregar expresión** \ ( ![ Agregar expresión ][ImageAddExpressionIcon] \) para crear una nueva expresión de inspección.</span><span class="sxs-lookup"><span data-stu-id="8a26a-221">Click the **Add Expression** \(![Add Expression][ImageAddExpressionIcon]\) button to create a new watch expression.</span></span>  
*   <span data-ttu-id="8a26a-222">Haga clic en el botón **Actualizar** \ ( ![ actualizar ][ImageRefreshIcon] \) para actualizar los valores de todas las expresiones existentes.</span><span class="sxs-lookup"><span data-stu-id="8a26a-222">Click the **Refresh** \(![Refresh][ImageRefreshIcon]\) button to refresh the values of all existing expressions.</span></span>  <span data-ttu-id="8a26a-223">Los valores se actualizan automáticamente al recorrer el código.</span><span class="sxs-lookup"><span data-stu-id="8a26a-223">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="8a26a-224">Mueva el puntero sobre una expresión y haga clic en el botón **eliminar expresión** \ ( ![ eliminar expresión ][ImageDeleteExpressionIcon] \) para eliminarla.</span><span class="sxs-lookup"><span data-stu-id="8a26a-224">Hover over an expression and click the **Delete Expression** \(![Delete Expression][ImageDeleteExpressionIcon]\) button to delete it.</span></span>  

## <span data-ttu-id="8a26a-225">Hacer que un archivo minified sea legible</span><span class="sxs-lookup"><span data-stu-id="8a26a-225">Make a minified file readable</span></span>  

<span data-ttu-id="8a26a-226">Haga clic **en el** botón \ ( ![ formato ][ImageFormatIcon] \) para hacer que un archivo minified sea legible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="8a26a-226">Click the **Format** \(![Format][ImageFormatIcon]\) button to make a minified file human-readable.</span></span>  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="El botón formato" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   <span data-ttu-id="8a26a-228">El botón **formato**</span><span class="sxs-lookup"><span data-stu-id="8a26a-228">The **Format** button</span></span>  
:::image-end:::  

## <span data-ttu-id="8a26a-229">Editar un script</span><span class="sxs-lookup"><span data-stu-id="8a26a-229">Edit a script</span></span>   

<span data-ttu-id="8a26a-230">Al corregir un error, a menudo desearás probar algunos cambios en el código de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8a26a-230">When fixing a bug, you often want to test out some changes to your JavaScript code.</span></span>  <span data-ttu-id="8a26a-231">No es necesario realizar los cambios en un editor externo o IDE y, a continuación, volver a cargar la página.</span><span class="sxs-lookup"><span data-stu-id="8a26a-231">You do not need to make the changes in an external editor or IDE and then reload the page.</span></span>  <span data-ttu-id="8a26a-232">Puede editar su script en DevTools.</span><span class="sxs-lookup"><span data-stu-id="8a26a-232">You may edit your script in DevTools.</span></span>  

<span data-ttu-id="8a26a-233">Complete las acciones siguientes para editar un script.</span><span class="sxs-lookup"><span data-stu-id="8a26a-233">Complete the following actions to edit a script.</span></span>  

1.  <span data-ttu-id="8a26a-234">Abra el archivo en el panel **Editor** del panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="8a26a-234">Open the file in the **Editor** pane of the **Sources** panel.</span></span>  
1.  <span data-ttu-id="8a26a-235">Realice los cambios en el panel **Editor** .</span><span class="sxs-lookup"><span data-stu-id="8a26a-235">Make your changes in the **Editor** pane.</span></span>  
1.  <span data-ttu-id="8a26a-236">Pulse `Ctrl` + `S` \ (Windows \) o `Command` + `S` \ (MacOS \) para guardar.</span><span class="sxs-lookup"><span data-stu-id="8a26a-236">Press `Ctrl`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="8a26a-237">DevTools revisa todo el archivo JS en el motor de JavaScript de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8a26a-237">DevTools patches the entire JS file into the JavaScript engine of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="El panel Editor" lightbox="../media/javascript-sources-html-minified.msft.png":::
       <span data-ttu-id="8a26a-239">El panel **Editor**</span><span class="sxs-lookup"><span data-stu-id="8a26a-239">The **Editor** pane</span></span>  
    :::image-end:::  
     
## <span data-ttu-id="8a26a-240">Deshabilitar JavaScript</span><span class="sxs-lookup"><span data-stu-id="8a26a-240">Disable JavaScript</span></span>   

<span data-ttu-id="8a26a-241">Consulte [deshabilitar JavaScript con Microsoft Edge DevTools][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="8a26a-241">See [Disable JavaScript with Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>  

## <span data-ttu-id="8a26a-242">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8a26a-242">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageStepOverIcon]: ../media/step-over-icon.msft.png  
[ImageStepIntoIcon]: ../media/step-into-icon.msft.png  
[ImageStepOutIcon]: ../media/step-out-icon.msft.png  
[ImageResumeScriptExecutionIcon]: ../media/resume-script-run-icon.msft.png  
[ImageForceScriptExecutionIcon]: ../media/force-script-run-icon.msft.png  
[ImageAddExpressionIcon]: ../media/add-expression-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageDeleteExpressionIcon]: ../media/delete-expression-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  

<!-- links -->  

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft docs"  
[DevToolsJavascriptDisable]: ./disable.md "Deshabilitar JavaScript con Microsoft Edge DevTools | Microsoft docs"  
[DevToolsJavascriptGetStarted]: ./index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft docs"  
[DevToolsJavascriptSnippets]: ./snippets.md "Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools | Microsoft docs"  
[DevToolsCustomize]: ../customize/index.md "Personalizar Microsoft Edge DevTools | Microsoft docs"  

> [!NOTE]
> <span data-ttu-id="8a26a-248">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8a26a-248">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8a26a-249">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="8a26a-249">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8a26a-251">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8a26a-251">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

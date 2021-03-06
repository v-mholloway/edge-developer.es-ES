---
description: Descubra nuevos flujos de trabajo de depuración en esta referencia completa de las características de depuración de Microsoft Edge DevTools.
title: Referencia de depuración de JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 09a2d61269b2fe3a23a57ce58eb1c89b12a7639c
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398479"
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

# <a name="javascript-debugging-reference"></a><span data-ttu-id="96dba-104">Referencia de depuración de JavaScript</span><span class="sxs-lookup"><span data-stu-id="96dba-104">JavaScript debugging reference</span></span>  

<span data-ttu-id="96dba-105">Descubra nuevos flujos de trabajo de depuración con la siguiente referencia completa de las características de depuración de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="96dba-105">Discover new debugging workflows with the following comprehensive reference of Microsoft Edge DevTools debugging features.</span></span>  

<span data-ttu-id="96dba-106">Para obtener información sobre los conceptos básicos de la depuración, vaya a Introducción a [La depuración de JavaScript en Microsoft Edge DevTools][DevToolsJavascriptGetStarted].</span><span class="sxs-lookup"><span data-stu-id="96dba-106">To learn the basics of debugging, navigate to [Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted].</span></span>  

## <a name="pause-code-with-breakpoints"></a><span data-ttu-id="96dba-107">Pausar código con puntos de interrupción</span><span class="sxs-lookup"><span data-stu-id="96dba-107">Pause code with breakpoints</span></span>  

<span data-ttu-id="96dba-108">Establece un punto de interrupción para que puedas pausar el código en medio del tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="96dba-108">Set a breakpoint so that you are able to pause your code in the middle of the runtime.</span></span>  

<span data-ttu-id="96dba-109">Para obtener información sobre cómo establecer puntos de interrupción, vaya [a Pausar el código con puntos de interrupción][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="96dba-109">To learn how to set breakpoints, navigate to [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <a name="step-through-code"></a><span data-ttu-id="96dba-110">Paso a través del código</span><span class="sxs-lookup"><span data-stu-id="96dba-110">Step through code</span></span>  

<span data-ttu-id="96dba-111">Una vez que el código está en pausa, pase por él, una línea a la vez, investigando el flujo de control y los valores de propiedad en el camino.</span><span class="sxs-lookup"><span data-stu-id="96dba-111">Once your code is paused, step through it, one line at a time, investigating control flow and property values along the way.</span></span>  

### <a name="step-over-line-of-code"></a><span data-ttu-id="96dba-112">Paso a paso por la línea de código</span><span class="sxs-lookup"><span data-stu-id="96dba-112">Step over line of code</span></span>  

<span data-ttu-id="96dba-113">Cuando se pausa en una línea de código que contiene una función que no es relevante para el problema que está depurando, elija el botón **Paso** a paso \( Paso sobre \) para ejecutar la función sin entrar en ![ ][ImageStepOverIcon] ella.</span><span class="sxs-lookup"><span data-stu-id="96dba-113">When paused on a line of code containing a function that is not relevant to the problem you are debugging, choose the **Step over** \(![Step over][ImageStepOverIcon]\) button to run the function without stepping into it.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Elija Paso a paso" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   <span data-ttu-id="96dba-115">Elija **Paso a paso**</span><span class="sxs-lookup"><span data-stu-id="96dba-115">Choose **Step over**</span></span>  
:::image-end:::  

<span data-ttu-id="96dba-116">Por ejemplo, supongamos que está depurando el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="96dba-116">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="96dba-117">Está en pausa en `A` .</span><span class="sxs-lookup"><span data-stu-id="96dba-117">You are paused on `A`.</span></span>  <span data-ttu-id="96dba-118">Después de elegir **Paso a paso**, DevTools ejecuta todo el código de la función que va a pasar, que es y `B` `C` .</span><span class="sxs-lookup"><span data-stu-id="96dba-118">After you choose **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="96dba-119">A continuación, DevTools hace una pausa en `D` .</span><span class="sxs-lookup"><span data-stu-id="96dba-119">DevTools then pauses on `D`.</span></span>  

### <a name="step-into-line-of-code"></a><span data-ttu-id="96dba-120">Paso a paso en la línea de código</span><span class="sxs-lookup"><span data-stu-id="96dba-120">Step into line of code</span></span>  

<span data-ttu-id="96dba-121">Cuando se pausa en una línea de código que contiene una llamada de función relacionada con el problema que está depurando, elija el botón Paso a **paso** en \( Paso a \) para investigar esa función más ![ ][ImageStepIntoIcon] adelante.</span><span class="sxs-lookup"><span data-stu-id="96dba-121">When paused on a line of code containing a function call that is related to the problem you are debugging, choose the **Step into** \(![Step into][ImageStepIntoIcon]\) button to investigate that function further.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Elija Paso a paso" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   <span data-ttu-id="96dba-123">Elija **Paso a paso**</span><span class="sxs-lookup"><span data-stu-id="96dba-123">Choose **Step into**</span></span>  
:::image-end:::  

<span data-ttu-id="96dba-124">Por ejemplo, supongamos que está depurando el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="96dba-124">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="96dba-125">Está en pausa en `A` .</span><span class="sxs-lookup"><span data-stu-id="96dba-125">You are paused on `A`.</span></span>  <span data-ttu-id="96dba-126">Después de elegir **Paso en**, DevTools ejecuta esta línea de código y, a continuación, se pausa en `B` .</span><span class="sxs-lookup"><span data-stu-id="96dba-126">After you choose **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <a name="step-out-of-line-of-code"></a><span data-ttu-id="96dba-127">Salir de la línea de código</span><span class="sxs-lookup"><span data-stu-id="96dba-127">Step out of line of code</span></span>  

<span data-ttu-id="96dba-128">Cuando se pausa dentro de una función que no está relacionada con el problema que está depurando, elija el botón Salir **\(** Salir \) para ejecutar el resto del código de ![ la ][ImageStepOutIcon] función.</span><span class="sxs-lookup"><span data-stu-id="96dba-128">When paused inside of a function that is not related to the problem you are debugging, choose the **Step out** \(![Step out][ImageStepOutIcon]\) button to run the rest of the code of the function.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Elija Salir" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   <span data-ttu-id="96dba-130">Elija **Salir**</span><span class="sxs-lookup"><span data-stu-id="96dba-130">Choose **Step out**</span></span>  
:::image-end:::  

<span data-ttu-id="96dba-131">Por ejemplo, supongamos que está depurando el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="96dba-131">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="96dba-132">Está en pausa en `A` .</span><span class="sxs-lookup"><span data-stu-id="96dba-132">You are paused on `A`.</span></span>  <span data-ttu-id="96dba-133">Después de elegir **Step out**, DevTools ejecuta el resto del código en , que está en este ejemplo y, a `getName()` continuación, se pausa en `B` `C` .</span><span class="sxs-lookup"><span data-stu-id="96dba-133">After you choose **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <a name="run-all-code-up-to-a-specific-line"></a><span data-ttu-id="96dba-134">Ejecutar todo el código hasta una línea específica</span><span class="sxs-lookup"><span data-stu-id="96dba-134">Run all code up to a specific line</span></span>  

<span data-ttu-id="96dba-135">Al depurar una función larga, puede haber una gran cantidad de código que no está relacionado con el problema que está depurando.</span><span class="sxs-lookup"><span data-stu-id="96dba-135">When debugging a long function, there may be a lot of code that is not related to the problem you are debugging.</span></span>  

<span data-ttu-id="96dba-136">Puede optar por pasar por todas las líneas, pero eso es tedioso.</span><span class="sxs-lookup"><span data-stu-id="96dba-136">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="96dba-137">Puede elegir establecer un punto de interrupción de línea de código en la línea en la que está interesado y, a continuación, elegir el botón Reanudar ejecución de **script** \( Reanudar ejecución de script \), pero hay una forma más ![ ][ImageResumeScriptExecutionIcon] rápida.</span><span class="sxs-lookup"><span data-stu-id="96dba-137">You may choose to set a line-of-code breakpoint on the line in which you are interested and then choose the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button, but there is a faster way.</span></span>  

<span data-ttu-id="96dba-138">Mantenga el mouse sobre la línea de código en la que le interesa, abra el menú contextual \(hacer clic con el botón secundario\) y **elija Continuar hasta aquí**.</span><span class="sxs-lookup"><span data-stu-id="96dba-138">Hover on the line of code in which you are interested, open the contextual menu \(right-click\), and choose **Continue to here**.</span></span>  <span data-ttu-id="96dba-139">DevTools ejecuta todo el código hasta ese punto y, a continuación, se pausa en esa línea.</span><span class="sxs-lookup"><span data-stu-id="96dba-139">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Elija Continuar hasta aquí" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   <span data-ttu-id="96dba-141">Elija **Continuar hasta aquí**</span><span class="sxs-lookup"><span data-stu-id="96dba-141">Choose **Continue to here**</span></span>  
:::image-end:::  

### <a name="restart-the-top-function-of-the-call-stack"></a><span data-ttu-id="96dba-142">Reiniciar la función superior de la pila de llamadas</span><span class="sxs-lookup"><span data-stu-id="96dba-142">Restart the top function of the call stack</span></span>  

<span data-ttu-id="96dba-143">Para pausar en la primera línea de la función superior de la pila de \*\*\*\* llamadas, mientras se pausa en una línea de código, mantenga el mouse en cualquier lugar del panel Pila de llamadas, abra el menú contextual \(haga clic con el botón secundario\) y elija **Reiniciar**marco .</span><span class="sxs-lookup"><span data-stu-id="96dba-143">To pause on the first line of the top function in your call stack, while paused on a line of code, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Restart Frame**.</span></span>  <span data-ttu-id="96dba-144">La función superior es la última función que se ha ejecutado.</span><span class="sxs-lookup"><span data-stu-id="96dba-144">The top function is the last function that was run.</span></span>  

<span data-ttu-id="96dba-145">El siguiente fragmento de código es un ejemplo de paso a paso.</span><span class="sxs-lookup"><span data-stu-id="96dba-145">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="96dba-146">Está en pausa en `A` .</span><span class="sxs-lookup"><span data-stu-id="96dba-146">You are paused on `A`.</span></span>  <span data-ttu-id="96dba-147">Después de elegir **Reiniciar fotograma**, debe pausarse en , sin establecer nunca un punto de interrupción ni elegir Reanudar ejecución `B` de **script**.</span><span class="sxs-lookup"><span data-stu-id="96dba-147">After choosing **Restart Frame**, you should be paused on `B`, without ever setting a breakpoint or choosing **Resume script execution**.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Elegir fotograma de reinicio" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   <span data-ttu-id="96dba-149">Elegir **fotograma de reinicio**</span><span class="sxs-lookup"><span data-stu-id="96dba-149">Choose **Restart Frame**</span></span>  
:::image-end:::  

### <a name="resume-script-runtime"></a><span data-ttu-id="96dba-150">Resume script runtime</span><span class="sxs-lookup"><span data-stu-id="96dba-150">Resume script runtime</span></span>  

<span data-ttu-id="96dba-151">Para continuar con el tiempo de ejecución después de una pausa del script, elija el botón Reanudar ejecución de **script** \( ![ Reanudar ejecución de script ][ImageResumeScriptExecutionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="96dba-151">To continue the runtime after a pause of your script, choose the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button.</span></span>  <span data-ttu-id="96dba-152">DevTools ejecuta el script hasta el siguiente punto de interrupción, si lo hay.</span><span class="sxs-lookup"><span data-stu-id="96dba-152">DevTools runs the script up until the next breakpoint, if any.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Elegir Reanudar ejecución de script" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   <span data-ttu-id="96dba-154">Elegir **Reanudar ejecución de script**</span><span class="sxs-lookup"><span data-stu-id="96dba-154">Choose **Resume script execution**</span></span>  
:::image-end:::  

#### <a name="force-script-runtime"></a><span data-ttu-id="96dba-155">Forzar tiempo de ejecución de script</span><span class="sxs-lookup"><span data-stu-id="96dba-155">Force script runtime</span></span>  

<span data-ttu-id="96dba-156">Para omitir todos los puntos de interrupción y forzar la reanudación de la ejecución del script, elija y mantenga presionado el botón Reanudar ejecución de script **\(** Reanudar ejecución de script \) y, a continuación, elija el botón Forzar ejecución de script \( Forzar la ejecución del ![ ][ImageResumeScriptExecutionIcon] script \*\*\*\* ![ ][ImageForceScriptExecutionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="96dba-156">To ignore all breakpoints and force your script to resume running, choose and hold the **Resume Script Execution** \(![Resume Script Execution][ImageResumeScriptExecutionIcon]\) button and then choose the **Force script execution** \(![Force script execution][ImageForceScriptExecutionIcon]\) button.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Elegir Forzar ejecución de script" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   <span data-ttu-id="96dba-158">Elegir **Forzar ejecución de script**</span><span class="sxs-lookup"><span data-stu-id="96dba-158">Choose **Force script execution**</span></span>  
:::image-end:::  

### <a name="change-thread-context"></a><span data-ttu-id="96dba-159">Cambiar contexto de subproceso</span><span class="sxs-lookup"><span data-stu-id="96dba-159">Change thread context</span></span>  

<span data-ttu-id="96dba-160">Al trabajar con trabajadores web o trabajadores \*\*\*\* de servicio, elija en un contexto que aparece en el panel Subprocesos para cambiar a ese contexto.</span><span class="sxs-lookup"><span data-stu-id="96dba-160">When working with web workers or service workers, choose on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="96dba-161">El icono de flecha azul representa qué contexto está seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="96dba-161">The blue arrow icon represents which context is currently selected.</span></span>  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Panel Subprocesos" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   <span data-ttu-id="96dba-163">Panel **Subprocesos**</span><span class="sxs-lookup"><span data-stu-id="96dba-163">The **Threads** pane</span></span>  
:::image-end:::  

<span data-ttu-id="96dba-164">Por ejemplo, suponga que está pausado en un punto de interrupción tanto en el script principal como en el script de trabajo de servicio.</span><span class="sxs-lookup"><span data-stu-id="96dba-164">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="96dba-165">Desea ver las propiedades locales y globales del contexto de trabajo de servicio, pero el **panel** Orígenes muestra el contexto de script principal.</span><span class="sxs-lookup"><span data-stu-id="96dba-165">You want to view the local and global properties for the service worker context, but the **Sources** panel is showing the main script context.</span></span>  <span data-ttu-id="96dba-166">Al elegir en la entrada de trabajo de servicio en **el** panel Subprocesos, debería poder cambiar a ese contexto.</span><span class="sxs-lookup"><span data-stu-id="96dba-166">By choosing on the service worker entry in the **Threads** pane, you should be able to switch to that context.</span></span>  

## <a name="view-and-edit-local-closure-and-global-properties"></a><span data-ttu-id="96dba-167">Ver y editar propiedades locales, de cierre y globales</span><span class="sxs-lookup"><span data-stu-id="96dba-167">View and edit local, closure, and global properties</span></span>  

<span data-ttu-id="96dba-168">Mientras está pausado en una \*\*\*\* línea de código, use el panel Ámbito para ver y editar los valores de propiedades y variables en los ámbitos local, de cierre y global.</span><span class="sxs-lookup"><span data-stu-id="96dba-168">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="96dba-169">Haga doble clic en un valor de propiedad para cambiarlo.</span><span class="sxs-lookup"><span data-stu-id="96dba-169">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="96dba-170">Las propiedades no enumerables están grises.</span><span class="sxs-lookup"><span data-stu-id="96dba-170">Non-enumerable properties are greyed out.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Panel Ámbito" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   <span data-ttu-id="96dba-172">Panel **Ámbito**</span><span class="sxs-lookup"><span data-stu-id="96dba-172">The **Scope** pane</span></span>  
:::image-end:::  

## <a name="view-the-current-call-stack"></a><span data-ttu-id="96dba-173">Ver la pila de llamadas actual</span><span class="sxs-lookup"><span data-stu-id="96dba-173">View the current call stack</span></span>  

<span data-ttu-id="96dba-174">Mientras está pausado en una línea de código, use el panel **Pila** de llamadas para ver la pila de llamadas que le ha hecho llegar hasta este punto.</span><span class="sxs-lookup"><span data-stu-id="96dba-174">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="96dba-175">Elija una entrada para saltar a la línea de código donde se llamó a esa función.</span><span class="sxs-lookup"><span data-stu-id="96dba-175">Choose an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="96dba-176">El icono de flecha azul representa la función DevTools que está resaltando actualmente.</span><span class="sxs-lookup"><span data-stu-id="96dba-176">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Panel Pila de llamadas" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   <span data-ttu-id="96dba-178">Panel **Pila de** llamadas</span><span class="sxs-lookup"><span data-stu-id="96dba-178">The **Call Stack** pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="96dba-179">Cuando no se pausa en una línea de código, el panel **Pila** de llamadas está vacío.</span><span class="sxs-lookup"><span data-stu-id="96dba-179">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <a name="copy-stack-trace"></a><span data-ttu-id="96dba-180">Copiar seguimiento de pila</span><span class="sxs-lookup"><span data-stu-id="96dba-180">Copy stack trace</span></span>  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="96dba-181">para copiar la pila de llamadas actual \*\*\*\* en el Portapapeles, mantenga el mouse en cualquier lugar del panel Pila de llamadas, abra el menú contextual \(clic con el botón secundario\) y elija Copiar seguimiento **de pila**.</span><span class="sxs-lookup"><span data-stu-id="96dba-181">to copy the current call stack to the clipboard, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Copy stack trace**.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Elija Copiar seguimiento de pila" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   <span data-ttu-id="96dba-183">Elija **Copiar seguimiento de pila**</span><span class="sxs-lookup"><span data-stu-id="96dba-183">Choose **Copy Stack Trace**</span></span>  
:::image-end:::  

<span data-ttu-id="96dba-184">El siguiente fragmento de código es un ejemplo de la salida.</span><span class="sxs-lookup"><span data-stu-id="96dba-184">The following code snippet is an example of the output.</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onChoose (get-started.js:15)
```  

## <a name="ignore-a-script-or-pattern-of-scripts"></a><span data-ttu-id="96dba-185">Omitir un script o patrón de scripts</span><span class="sxs-lookup"><span data-stu-id="96dba-185">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="96dba-186">Marca un script como código de biblioteca cuando quieras omitir ese script durante la depuración.</span><span class="sxs-lookup"><span data-stu-id="96dba-186">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="96dba-187">Cuando se marca como código de biblioteca, un script se oculta en el panel Pila de llamadas y nunca se pasa a las funciones del script cuando se pasa por el código. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="96dba-187">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="96dba-188">El siguiente fragmento de código es un ejemplo de paso a paso.</span><span class="sxs-lookup"><span data-stu-id="96dba-188">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` <span data-ttu-id="96dba-189">es una biblioteca de terceros en la que confía.</span><span class="sxs-lookup"><span data-stu-id="96dba-189">is a third-party library that you trust.</span></span>  <span data-ttu-id="96dba-190">Si está seguro de que el problema que está depurando no está relacionado con la biblioteca de terceros, tiene sentido marcar el script como **código de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="96dba-190">If you are confident that the problem you are debugging is not related to the third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

### <a name="mark-a-script-as-library-code-from-the-editor-pane"></a><span data-ttu-id="96dba-191">Marcar un script como código de biblioteca desde el panel Editor</span><span class="sxs-lookup"><span data-stu-id="96dba-191">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="96dba-192">Complete las siguientes acciones para marcar un script como **código de biblioteca** desde el panel **Editor.**</span><span class="sxs-lookup"><span data-stu-id="96dba-192">Complete the following actions to mark a script as **Library code** from the **Editor** pane.</span></span>  

1.  <span data-ttu-id="96dba-193">Abra el archivo.</span><span class="sxs-lookup"><span data-stu-id="96dba-193">Open the file.</span></span>  
1.  <span data-ttu-id="96dba-194">Mantenga el mouse en cualquier lugar y abra el menú contextual \(hacer clic con el botón secundario\).</span><span class="sxs-lookup"><span data-stu-id="96dba-194">Hover anywhere and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="96dba-195">Elija **Marcar como código de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="96dba-195">Choose **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde el panel Editor" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       <span data-ttu-id="96dba-197">Marcar un script como **código de biblioteca** desde el panel **Editor**</span><span class="sxs-lookup"><span data-stu-id="96dba-197">Mark a script as **Library code** from the **Editor** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-the-call-stack-pane"></a><span data-ttu-id="96dba-198">Marcar un script como código de biblioteca desde el panel Pila de llamadas</span><span class="sxs-lookup"><span data-stu-id="96dba-198">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="96dba-199">Complete las siguientes acciones para marcar un script como **código de biblioteca** desde el panel Pila **de** llamadas.</span><span class="sxs-lookup"><span data-stu-id="96dba-199">Complete the following actions to mark a script as **Library code** from the **Call Stack** pane.</span></span>  

1.  <span data-ttu-id="96dba-200">Mantenga el mouse sobre una función del script y abra el menú contextual \(hacer clic con el botón secundario\).</span><span class="sxs-lookup"><span data-stu-id="96dba-200">Hover on a function from the script and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="96dba-201">Elija **Marcar como código de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="96dba-201">Choose **Mark as Library code**.</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde el panel Pila de llamadas" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       <span data-ttu-id="96dba-203">Marcar un script como **código de biblioteca** desde el panel Pila **de** llamadas</span><span class="sxs-lookup"><span data-stu-id="96dba-203">Mark a script as **Library code** from the **Call Stack** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-settings"></a><span data-ttu-id="96dba-204">Marcar un script como código de biblioteca desde Configuración</span><span class="sxs-lookup"><span data-stu-id="96dba-204">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="96dba-205">Complete las siguientes acciones para marcar un único script o patrón de scripts desde **Configuración**.</span><span class="sxs-lookup"><span data-stu-id="96dba-205">Complete the following actions to mark a single script or pattern of scripts from **Settings**.</span></span>  

1.  <span data-ttu-id="96dba-206">Abra [Configuración][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="96dba-206">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="96dba-207">Vaya a la **configuración de código de biblioteca.**</span><span class="sxs-lookup"><span data-stu-id="96dba-207">Navigate to the **Library code** setting.</span></span>  
1.  <span data-ttu-id="96dba-208">Elija **Agregar patrón**.</span><span class="sxs-lookup"><span data-stu-id="96dba-208">Choose **Add pattern**.</span></span>  
1.  <span data-ttu-id="96dba-209">Escriba el nombre del script o un patrón regex de nombres de script para marcar como **código de biblioteca.**</span><span class="sxs-lookup"><span data-stu-id="96dba-209">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="96dba-210">Elija **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="96dba-210">Choose **Add**.</span></span>  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde Configuración" lightbox="../media/javascript-framework-library-code.msft.png":::
       <span data-ttu-id="96dba-212">Marcar un script como código **de biblioteca desde** **Configuración**</span><span class="sxs-lookup"><span data-stu-id="96dba-212">Mark a script as **Library code** from **Settings**</span></span>  
    :::image-end:::  
    
## <a name="run-snippets-of-debug-code-from-any-page"></a><span data-ttu-id="96dba-213">Ejecutar fragmentos de código de depuración desde cualquier página</span><span class="sxs-lookup"><span data-stu-id="96dba-213">Run snippets of debug code from any page</span></span>  

<span data-ttu-id="96dba-214">Si se encuentra ejecutando el mismo código de depuración en la consola una y otra vez, considere Fragmentos de código.</span><span class="sxs-lookup"><span data-stu-id="96dba-214">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="96dba-215">Los fragmentos de código son scripts en tiempo de ejecución que se pueden crear, almacenar y ejecutar en DevTools.</span><span class="sxs-lookup"><span data-stu-id="96dba-215">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="96dba-216">Para obtener más información, vaya [a Ejecutar fragmentos de código desde cualquier página][DevToolsJavascriptSnippets].</span><span class="sxs-lookup"><span data-stu-id="96dba-216">To learn more, navigate to [Run Snippets of Code From Any Page][DevToolsJavascriptSnippets].</span></span>  

## <a name="watch-the-values-of-custom-javascript-expressions"></a><span data-ttu-id="96dba-217">Ver los valores de las expresiones de JavaScript personalizadas</span><span class="sxs-lookup"><span data-stu-id="96dba-217">Watch the values of custom JavaScript expressions</span></span>  

<span data-ttu-id="96dba-218">Use el **panel** Ver para ver los valores de las expresiones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="96dba-218">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="96dba-219">Puede ver cualquier expresión de JavaScript válida.</span><span class="sxs-lookup"><span data-stu-id="96dba-219">You may watch any valid JavaScript expression.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="El panel Ver" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   <span data-ttu-id="96dba-221">El **panel Ver**</span><span class="sxs-lookup"><span data-stu-id="96dba-221">The **Watch** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="96dba-222">Elija el botón Agregar **expresión** \( ![ Agregar expresión ][ImageAddExpressionIcon] \) para crear una nueva expresión de reloj.</span><span class="sxs-lookup"><span data-stu-id="96dba-222">Choose the **Add Expression** \(![Add Expression][ImageAddExpressionIcon]\) button to create a new watch expression.</span></span>  
*   <span data-ttu-id="96dba-223">Elija el **botón Actualizar** \( ![ Actualizar ][ImageRefreshIcon] \) para actualizar los valores de todas las expresiones existentes.</span><span class="sxs-lookup"><span data-stu-id="96dba-223">Choose the **Refresh** \(![Refresh][ImageRefreshIcon]\) button to refresh the values of all existing expressions.</span></span>  <span data-ttu-id="96dba-224">Los valores se actualizan automáticamente al pasar por el código.</span><span class="sxs-lookup"><span data-stu-id="96dba-224">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="96dba-225">Mantenga el mouse sobre una expresión y elija el **botón Eliminar expresión** \( Eliminar expresión ![ ][ImageDeleteExpressionIcon] \) para eliminarla.</span><span class="sxs-lookup"><span data-stu-id="96dba-225">Hover on an expression and choose the **Delete Expression** \(![Delete Expression][ImageDeleteExpressionIcon]\) button to delete it.</span></span>  

## <a name="make-a-minified-file-readable"></a><span data-ttu-id="96dba-226">Hacer que un archivo minified sea legible</span><span class="sxs-lookup"><span data-stu-id="96dba-226">Make a minified file readable</span></span>  

<span data-ttu-id="96dba-227">Elija el **botón Formato** \( ![ Formato ][ImageFormatIcon] \) para que un archivo minificado sea legible.</span><span class="sxs-lookup"><span data-stu-id="96dba-227">Choose the **Format** \(![Format][ImageFormatIcon]\) button to make a minified file human-readable.</span></span>  

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="El botón Formato" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   <span data-ttu-id="96dba-229">El **botón** Formato</span><span class="sxs-lookup"><span data-stu-id="96dba-229">The **Format** button</span></span>  
:::image-end:::  

## <a name="edit-a-script"></a><span data-ttu-id="96dba-230">Editar un script</span><span class="sxs-lookup"><span data-stu-id="96dba-230">Edit a script</span></span>  

<span data-ttu-id="96dba-231">Al corregir un error, a menudo quieres probar algunos cambios en el código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="96dba-231">When fixing a bug, you often want to test out some changes to your JavaScript code.</span></span>  <span data-ttu-id="96dba-232">No es necesario realizar los cambios en un editor externo o IDE y, a continuación, actualizar la página.</span><span class="sxs-lookup"><span data-stu-id="96dba-232">You do not need to make the changes in an external editor or IDE and then refresh the page.</span></span>  <span data-ttu-id="96dba-233">Puede editar el script en DevTools.</span><span class="sxs-lookup"><span data-stu-id="96dba-233">You may edit your script in DevTools.</span></span>  

<span data-ttu-id="96dba-234">Complete las siguientes acciones para editar un script.</span><span class="sxs-lookup"><span data-stu-id="96dba-234">Complete the following actions to edit a script.</span></span>  

1.  <span data-ttu-id="96dba-235">Abra el archivo en el **panel Editor** del panel **Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="96dba-235">Open the file in the **Editor** pane of the **Sources** panel.</span></span>  
1.  <span data-ttu-id="96dba-236">Realice los cambios en el **panel Editor.**</span><span class="sxs-lookup"><span data-stu-id="96dba-236">Make your changes in the **Editor** pane.</span></span>  
1.  <span data-ttu-id="96dba-237">Seleccione `Ctrl` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\) para guardar.</span><span class="sxs-lookup"><span data-stu-id="96dba-237">Select `Ctrl`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="96dba-238">DevTools parchea todo el archivo JS en el motor JavaScript de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="96dba-238">DevTools patches the entire JS file into the JavaScript engine of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Panel Editor" lightbox="../media/javascript-sources-html-minified.msft.png":::
       <span data-ttu-id="96dba-240">Panel **Editor**</span><span class="sxs-lookup"><span data-stu-id="96dba-240">The **Editor** pane</span></span>  
    :::image-end:::  
     
## <a name="disable-javascript"></a><span data-ttu-id="96dba-241">Deshabilitar JavaScript</span><span class="sxs-lookup"><span data-stu-id="96dba-241">Disable JavaScript</span></span>  

<span data-ttu-id="96dba-242">Vaya a [Deshabilitar JavaScript con Microsoft Edge DevTools][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="96dba-242">Navigate to [Disable JavaScript with Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="96dba-243">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="96dba-243">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptDisable]: ./disable.md "Deshabilitar JavaScript con Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptGetStarted]: ./index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptSnippets]: ./snippets.md "Ejecutar fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomize]: ../customize/index.md "Personalizar Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="96dba-249">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="96dba-249">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="96dba-250">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="96dba-250">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="96dba-252">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="96dba-252">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

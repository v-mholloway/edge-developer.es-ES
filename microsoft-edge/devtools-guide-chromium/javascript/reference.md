---
description: Descubra nuevos flujos de trabajo de depuración en esta referencia completa de Microsoft Edge de depuración de DevTools.
title: Usar las características del depurador
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 6b15d317d4c720ab5ad76b7047532df101f69376
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564129"
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
# <a name="use-the-debugger-features"></a><span data-ttu-id="83ad2-104">Usar las características del depurador</span><span class="sxs-lookup"><span data-stu-id="83ad2-104">Use the debugger features</span></span>

<span data-ttu-id="83ad2-105">En este artículo se describe cómo usar el depurador en Microsoft Edge DevTools, incluido cómo establecer un punto de interrupción de línea de código.</span><span class="sxs-lookup"><span data-stu-id="83ad2-105">This article covers how to use the debugger in Microsoft Edge DevTools, including how to set a line-of-code breakpoint.</span></span>  <span data-ttu-id="83ad2-106">Para establecer otros tipos de puntos de interrupción, vea [Pause your code with breakpoints][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="83ad2-106">To set other types of breakpoints, see [Pause your code with breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

<span data-ttu-id="83ad2-107">Para conocer los conceptos básicos de la depuración, vaya a Introducción a la depuración de JavaScript en [Microsoft Edge DevTools][DevToolsJavascriptGetStarted], que es un tutorial que usa una página web existente basada en formularios.</span><span class="sxs-lookup"><span data-stu-id="83ad2-107">To learn the basics of debugging, navigate to [Get started with debugging JavaScript in Microsoft Edge DevTools][DevToolsJavascriptGetStarted], which is a tutorial that uses an existing, form-based webpage.</span></span>  <span data-ttu-id="83ad2-108">El tutorial tiene capturas de pantalla, por lo que puedes desaconscarla.</span><span class="sxs-lookup"><span data-stu-id="83ad2-108">The tutorial has screen captures, so you can skim it.</span></span>  <span data-ttu-id="83ad2-109">Puedes probar fácilmente las características del depurador mediante la página web de demostración.</span><span class="sxs-lookup"><span data-stu-id="83ad2-109">You can easily try out the debugger features by using the demo webpage.</span></span>

## <a name="view-and-edit-javascript-code"></a><span data-ttu-id="83ad2-110">Ver y editar código JavaScript</span><span class="sxs-lookup"><span data-stu-id="83ad2-110">View and edit JavaScript code</span></span>

<span data-ttu-id="83ad2-111">Al corregir un error, a menudo quieres probar algunos cambios en el código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="83ad2-111">When fixing a bug, you often want to try out some changes to your JavaScript code.</span></span>  <span data-ttu-id="83ad2-112">No es necesario realizar los cambios en un editor externo o IDE, volver a cargar el archivo en el servidor y, a continuación, actualizar la página; en su lugar, para probar los cambios, puede editar el código JavaScript directamente en DevTools y ver el resultado inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="83ad2-112">You don't need to make the changes in an external editor or IDE, re-upload the file to the server, and then refresh the page; instead, to test changes, you can edit your JavaScript code directly in DevTools and see the result immediately.</span></span>  

<span data-ttu-id="83ad2-113">Para ver y editar un archivo JavaScript:</span><span class="sxs-lookup"><span data-stu-id="83ad2-113">To view and edit a JavaScript file:</span></span>  

1.  <span data-ttu-id="83ad2-114">Vaya a la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="83ad2-114">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="83ad2-115">En el **panel** Navegador, seleccione el archivo para abrirlo en el **panel Editor.**</span><span class="sxs-lookup"><span data-stu-id="83ad2-115">In the **Navigator** pane, select your file, to open it in the **Editor** pane.</span></span>
1.  <span data-ttu-id="83ad2-116">En el **panel Editor,** edite el archivo.</span><span class="sxs-lookup"><span data-stu-id="83ad2-116">In the **Editor** pane, edit your file.</span></span>  
1.  <span data-ttu-id="83ad2-117">Seleccione `Ctrl` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\) para guardar.</span><span class="sxs-lookup"><span data-stu-id="83ad2-117">Select `Ctrl`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  <span data-ttu-id="83ad2-118">A continuación, DevTools carga el archivo JavaScript en el motor JavaScript de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="83ad2-118">DevTools then loads the JavaScript file into the JavaScript engine of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-html-minified.msft.png" alt-text="Panel Editor" lightbox="../media/javascript-sources-html-minified.msft.png":::
       <span data-ttu-id="83ad2-120">Panel **Editor**</span><span class="sxs-lookup"><span data-stu-id="83ad2-120">The **Editor** pane</span></span>  
    :::image-end:::  
     
## <a name="reformat-a-minified-javascript-file-with-pretty-print"></a><span data-ttu-id="83ad2-121">Volver a formatear un archivo JavaScript minificado con pretty-print</span><span class="sxs-lookup"><span data-stu-id="83ad2-121">Reformat a minified JavaScript file with pretty-print</span></span>

<span data-ttu-id="83ad2-122">Para que un archivo minificado sea legible, elija el botón **Formato** \( Formato \) situado en la parte inferior ![ del ](../media/format-icon.msft.png) **panel** Editor.</span><span class="sxs-lookup"><span data-stu-id="83ad2-122">To make a minified file human-readable, choose the **Format** \(![Format](../media/format-icon.msft.png)\) button at the bottom of the **Editor** pane.</span></span>

:::image type="complex" source="../media/javascript-sources-html-non-minified.msft.png" alt-text="El botón Formato" lightbox="../media/javascript-sources-html-non-minified.msft.png":::
   <span data-ttu-id="83ad2-124">El **botón** Formato</span><span class="sxs-lookup"><span data-stu-id="83ad2-124">The **Format** button</span></span>  
:::image-end:::  

## <a name="set-a-breakpoint-to-pause-code"></a><span data-ttu-id="83ad2-125">Establecer un punto de interrupción para pausar el código</span><span class="sxs-lookup"><span data-stu-id="83ad2-125">Set a breakpoint, to pause code</span></span>

<span data-ttu-id="83ad2-126">Para pausar el código en medio del tiempo de ejecución, establezca un punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="83ad2-126">To pause your code in the middle of the runtime, set a breakpoint.</span></span>  <span data-ttu-id="83ad2-127">El tipo de punto de interrupción más básico y conocido es un punto de interrupción de línea de código.</span><span class="sxs-lookup"><span data-stu-id="83ad2-127">The most basic and well-known type of breakpoint is a line-of-code breakpoint.</span></span>

<span data-ttu-id="83ad2-128">Use un punto de interrupción de línea de código cuando sepa la región exacta del código que necesita investigar.</span><span class="sxs-lookup"><span data-stu-id="83ad2-128">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="83ad2-129">DevTools siempre se pausa en la línea de código especificada, antes de ejecutarlo.</span><span class="sxs-lookup"><span data-stu-id="83ad2-129">DevTools always pauses at the specified line of code, before running it.</span></span>

<span data-ttu-id="83ad2-130">Para establecer un punto de interrupción de línea de código:</span><span class="sxs-lookup"><span data-stu-id="83ad2-130">To set a line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="83ad2-131">Vaya a la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="83ad2-131">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="83ad2-132">Abra el archivo que contiene la línea de código.</span><span class="sxs-lookup"><span data-stu-id="83ad2-132">Open the file that contains the line of code.</span></span>  
1.  <span data-ttu-id="83ad2-133">Seleccione el área a la izquierda del número de línea para la línea de código.</span><span class="sxs-lookup"><span data-stu-id="83ad2-133">Select the area to the left of the line number for the line of code.</span></span>  <span data-ttu-id="83ad2-134">O bien, haga clic con el botón secundario en el número de línea y, a continuación, **elija Agregar punto de interrupción**.</span><span class="sxs-lookup"><span data-stu-id="83ad2-134">Or, right-click the line number and then choose **Add breakpoint**.</span></span>  <span data-ttu-id="83ad2-135">A continuación, aparece un círculo rojo junto al número de línea, que indica un punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="83ad2-135">A red circle then appears next to the line number, indicating a breakpoint.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Punto de interrupción de línea de código" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="83ad2-137">Punto de interrupción de línea de código</span><span class="sxs-lookup"><span data-stu-id="83ad2-137">A line-of-code breakpoint</span></span>  
    :::image-end:::  

<span data-ttu-id="83ad2-138">Los puntos de interrupción de línea de código pueden ser ineficientes para establecer, especialmente si no sabe exactamente dónde buscar o si su base de código es grande.</span><span class="sxs-lookup"><span data-stu-id="83ad2-138">Line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if your codebase is large.</span></span>  <span data-ttu-id="83ad2-139">Para ahorrar tiempo al depurar, obtenga información sobre cómo y cuándo usar los otros tipos de puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="83ad2-139">To save time when debugging, learn how and when to use the other types of breakpoints.</span></span>  <span data-ttu-id="83ad2-140">Para obtener más información, vaya [a Pausar el código con puntos de interrupción.][DevToolsJavascriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="83ad2-140">For more information, navigate to [Pause your code with breakpoints][DevToolsJavascriptBreakpoints].</span></span>

## <a name="step-through-code"></a><span data-ttu-id="83ad2-141">Paso a través del código</span><span class="sxs-lookup"><span data-stu-id="83ad2-141">Step through code</span></span>  

<span data-ttu-id="83ad2-142">Después de pausar el código en un punto de interrupción, pase por el código, una línea a la vez, investigando el flujo de control y los valores de propiedad en el camino.</span><span class="sxs-lookup"><span data-stu-id="83ad2-142">After your code is paused at a breakpoint, step through the code, one line at a time, investigating control flow and property values along the way.</span></span>  

### <a name="step-over-line-of-code"></a><span data-ttu-id="83ad2-143">Paso a paso por la línea de código</span><span class="sxs-lookup"><span data-stu-id="83ad2-143">Step over line of code</span></span>  

<span data-ttu-id="83ad2-144">Cuando se pausa en una línea de código que contiene una función que no es relevante para el problema que está depurando, elija el botón **Paso** a paso \( Paso sobre \) para ejecutar la función sin entrar en ![ ](../media/step-over-icon.msft.png) ella.</span><span class="sxs-lookup"><span data-stu-id="83ad2-144">When paused on a line of code containing a function that isn't relevant to the problem you are debugging, choose the **Step over** \(![Step over](../media/step-over-icon.msft.png)\) button to run the function without stepping into it.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png" alt-text="Elija Paso a paso" lightbox="../media/javascript-source-page-debugger-step-over-next-function-call.msft.png":::
   <span data-ttu-id="83ad2-146">Elija **Paso a paso**</span><span class="sxs-lookup"><span data-stu-id="83ad2-146">Choose **Step over**</span></span>  
:::image-end:::  

<span data-ttu-id="83ad2-147">Por ejemplo, supongamos que está depurando el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="83ad2-147">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="83ad2-148">Está en pausa en `A` .</span><span class="sxs-lookup"><span data-stu-id="83ad2-148">You are paused on `A`.</span></span>  <span data-ttu-id="83ad2-149">Después de elegir **Paso a paso**, DevTools ejecuta todo el código de la función que va a pasar, que es y `B` `C` .</span><span class="sxs-lookup"><span data-stu-id="83ad2-149">After you choose **Step over**, DevTools runs all the code in the function that you are stepping over, which is `B` and `C`.</span></span>  <span data-ttu-id="83ad2-150">A continuación, DevTools hace una pausa en `D` .</span><span class="sxs-lookup"><span data-stu-id="83ad2-150">DevTools then pauses on `D`.</span></span>  

### <a name="step-into-line-of-code"></a><span data-ttu-id="83ad2-151">Paso a paso en la línea de código</span><span class="sxs-lookup"><span data-stu-id="83ad2-151">Step into line of code</span></span>  

<span data-ttu-id="83ad2-152">Cuando se pausa en una línea de código que contiene una llamada de función relacionada con el problema que está depurando, elija el botón Paso a **paso** en \( Paso a \) para investigar esa función más ![ ](../media/step-into-icon.msft.png) adelante.</span><span class="sxs-lookup"><span data-stu-id="83ad2-152">When paused on a line of code containing a function call that is related to the problem you are debugging, choose the **Step into** \(![Step into](../media/step-into-icon.msft.png)\) button to investigate that function further.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png" alt-text="Elija Paso a paso" lightbox="../media/javascript-source-page-debugger-step-into-next-function-call.msft.png":::
   <span data-ttu-id="83ad2-154">Elija **Paso a paso**</span><span class="sxs-lookup"><span data-stu-id="83ad2-154">Choose **Step into**</span></span>  
:::image-end:::  

<span data-ttu-id="83ad2-155">Por ejemplo, supongamos que está depurando el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="83ad2-155">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="83ad2-156">Está en pausa en `A` .</span><span class="sxs-lookup"><span data-stu-id="83ad2-156">You are paused on `A`.</span></span>  <span data-ttu-id="83ad2-157">Después de elegir **Paso en**, DevTools ejecuta esta línea de código y, a continuación, se pausa en `B` .</span><span class="sxs-lookup"><span data-stu-id="83ad2-157">After you choose **Step into**, DevTools runs this line of code, then pauses on `B`.</span></span>  

### <a name="step-out-of-line-of-code"></a><span data-ttu-id="83ad2-158">Salir de la línea de código</span><span class="sxs-lookup"><span data-stu-id="83ad2-158">Step out of line of code</span></span>  

<span data-ttu-id="83ad2-159">Cuando se pausa dentro de una función que no está relacionada con el problema que está depurando, elija el botón Salir **\(** Salir \) para ejecutar el resto del código de ![ la ](../media/step-out-icon.msft.png) función.</span><span class="sxs-lookup"><span data-stu-id="83ad2-159">When paused inside of a function that isn't related to the problem you are debugging, choose the **Step out** \(![Step out](../media/step-out-icon.msft.png)\) button to run the rest of the code of the function.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png" alt-text="Elija Salir" lightbox="../media/javascript-source-page-debugger-step-out-of-current-function.msft.png":::
   <span data-ttu-id="83ad2-161">Elija **Salir**</span><span class="sxs-lookup"><span data-stu-id="83ad2-161">Choose **Step out**</span></span>  
:::image-end:::  

<span data-ttu-id="83ad2-162">Por ejemplo, supongamos que está depurando el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="83ad2-162">For example, suppose you are debugging the following code snippet.</span></span>  

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

<span data-ttu-id="83ad2-163">Está en pausa en `A` .</span><span class="sxs-lookup"><span data-stu-id="83ad2-163">You are paused on `A`.</span></span>  <span data-ttu-id="83ad2-164">Después de elegir **Step out**, DevTools ejecuta el resto del código en , que está en este ejemplo y, a `getName()` continuación, se pausa en `B` `C` .</span><span class="sxs-lookup"><span data-stu-id="83ad2-164">After you choose **Step out**, DevTools runs the rest of the code in `getName()`, which is just `B` in this example, and then pauses on `C`.</span></span>  

### <a name="run-all-code-up-to-a-specific-line"></a><span data-ttu-id="83ad2-165">Ejecutar todo el código hasta una línea específica</span><span class="sxs-lookup"><span data-stu-id="83ad2-165">Run all code up to a specific line</span></span>  

<span data-ttu-id="83ad2-166">Al depurar una función larga, puede haber una gran cantidad de código que no esté relacionado con el problema que está depurando.</span><span class="sxs-lookup"><span data-stu-id="83ad2-166">When debugging a long function, there may be a lot of code that isn't related to the problem you are debugging.</span></span>  

<span data-ttu-id="83ad2-167">Puede optar por pasar por todas las líneas, pero eso es tedioso.</span><span class="sxs-lookup"><span data-stu-id="83ad2-167">You may choose to step through all the lines, but that is tedious.</span></span>  <span data-ttu-id="83ad2-168">Puede elegir establecer un punto de interrupción de línea de código en la línea en la que está interesado y, a continuación, elegir el botón Reanudar ejecución de **script** \( Reanudar ejecución de script \), pero hay una forma más ![ ](../media/resume-script-run-icon.msft.png) rápida.</span><span class="sxs-lookup"><span data-stu-id="83ad2-168">You may choose to set a line-of-code breakpoint on the line in which you are interested and then choose the **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\) button, but there is a faster way.</span></span>  

<span data-ttu-id="83ad2-169">Mantenga el mouse sobre la línea de código en la que le interesa, abra el menú contextual \(hacer clic con el botón secundario\) y **elija Continuar hasta aquí**.</span><span class="sxs-lookup"><span data-stu-id="83ad2-169">Hover on the line of code in which you are interested, open the contextual menu \(right-click\), and choose **Continue to here**.</span></span>  <span data-ttu-id="83ad2-170">DevTools ejecuta todo el código hasta ese punto y, a continuación, se pausa en esa línea.</span><span class="sxs-lookup"><span data-stu-id="83ad2-170">DevTools runs all of the code up to that point, and then pauses on that line.</span></span>  

:::image type="complex" source="../media/javascript-source-page-continue-to-here.msft.png" alt-text="Elija Continuar hasta aquí" lightbox="../media/javascript-source-page-continue-to-here.msft.png":::
   <span data-ttu-id="83ad2-172">Elija **Continuar hasta aquí**</span><span class="sxs-lookup"><span data-stu-id="83ad2-172">Choose **Continue to here**</span></span>  
:::image-end:::  

### <a name="restart-the-top-function-of-the-call-stack"></a><span data-ttu-id="83ad2-173">Reiniciar la función superior de la pila de llamadas</span><span class="sxs-lookup"><span data-stu-id="83ad2-173">Restart the top function of the call stack</span></span>  

<span data-ttu-id="83ad2-174">Para pausar en la primera línea de la función superior de la pila de \*\*\*\* llamadas, mientras está pausada en una línea de código, mantenga el mouse en cualquier lugar del panel Pila de llamadas, abra el menú contextual \(haga clic con el botón secundario\) y elija **Reiniciar**fotograma .</span><span class="sxs-lookup"><span data-stu-id="83ad2-174">To pause on the first line of the top function in your call stack, while paused on a line of code, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Restart frame**.</span></span>  <span data-ttu-id="83ad2-175">La función superior es la última función que se ha ejecutado.</span><span class="sxs-lookup"><span data-stu-id="83ad2-175">The top function is the last function that was run.</span></span>  

<span data-ttu-id="83ad2-176">El siguiente fragmento de código es un ejemplo de paso a paso.</span><span class="sxs-lookup"><span data-stu-id="83ad2-176">The following code snippet is an example for you to step-through.</span></span>  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

<span data-ttu-id="83ad2-177">Está en pausa en `A` .</span><span class="sxs-lookup"><span data-stu-id="83ad2-177">You are paused on `A`.</span></span>  <span data-ttu-id="83ad2-178">Después de elegir **Reiniciar fotograma,** debe pausarse en , sin establecer nunca un punto de interrupción ni elegir Reanudar ejecución `B` de **script**.</span><span class="sxs-lookup"><span data-stu-id="83ad2-178">After choosing **Restart frame**, you should be paused on `B`, without ever setting a breakpoint or choosing **Resume script execution**.</span></span>  

:::image type="complex" source="../media/javascript-source-page-debugger-restart-frame.msft.png" alt-text="Elegir fotograma reiniciar" lightbox="../media/javascript-source-page-debugger-restart-frame.msft.png":::
   <span data-ttu-id="83ad2-180">Elegir **fotograma reiniciar**</span><span class="sxs-lookup"><span data-stu-id="83ad2-180">Choose **Restart frame**</span></span>  
:::image-end:::  

### <a name="resume-script-runtime"></a><span data-ttu-id="83ad2-181">Resume script runtime</span><span class="sxs-lookup"><span data-stu-id="83ad2-181">Resume script runtime</span></span>  

<span data-ttu-id="83ad2-182">Para continuar con el tiempo de ejecución después de una pausa del script, elija el botón Reanudar ejecución de **script** \( ![ Reanudar ejecución de script ](../media/resume-script-run-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="83ad2-182">To continue the runtime after a pause of your script, choose the **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\) button.</span></span>  <span data-ttu-id="83ad2-183">DevTools ejecuta el script hasta el siguiente punto de interrupción, si lo hay.</span><span class="sxs-lookup"><span data-stu-id="83ad2-183">DevTools runs the script up until the next breakpoint, if any.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png" alt-text="Elegir Reanudar ejecución de script" lightbox="../media/javascript-sources-get-started-js-resume-script-runtime.msft.png":::
   <span data-ttu-id="83ad2-185">Elegir **Reanudar ejecución de script**</span><span class="sxs-lookup"><span data-stu-id="83ad2-185">Choose **Resume script execution**</span></span>  
:::image-end:::  

#### <a name="force-script-runtime"></a><span data-ttu-id="83ad2-186">Forzar tiempo de ejecución de script</span><span class="sxs-lookup"><span data-stu-id="83ad2-186">Force script runtime</span></span>  

<span data-ttu-id="83ad2-187">Para omitir todos los puntos de interrupción y forzar la ejecución del script, elija y mantenga presionado el botón Reanudar ejecución de **scripts** \( Reanudar ejecución de script \) y, a continuación, elija el botón Forzar ejecución de script \( Forzar ejecución de ![ ](../media/resume-script-run-icon.msft.png) script \*\*\*\* ![ ](../media/force-script-run-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="83ad2-187">To ignore all breakpoints and force your script to continue to run, choose and hold the **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\) button and then choose the **Force script execution** \(![Force script execution](../media/force-script-run-icon.msft.png)\) button.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-force-script-runtime.msft.png" alt-text="Elegir Forzar ejecución de script" lightbox="../media/javascript-sources-get-started-js-force-script-runtime.msft.png":::
   <span data-ttu-id="83ad2-189">Elegir **Forzar ejecución de script**</span><span class="sxs-lookup"><span data-stu-id="83ad2-189">Choose **Force script execution**</span></span>  
:::image-end:::  

### <a name="change-thread-context"></a><span data-ttu-id="83ad2-190">Cambiar contexto de subproceso</span><span class="sxs-lookup"><span data-stu-id="83ad2-190">Change thread context</span></span>  

<span data-ttu-id="83ad2-191">Al trabajar con trabajadores web o trabajadores \*\*\*\* de servicio, elija en un contexto que aparece en el panel Subprocesos para cambiar a ese contexto.</span><span class="sxs-lookup"><span data-stu-id="83ad2-191">When working with web workers or service workers, choose on a context listed in the **Threads** pane to switch to that context.</span></span>  <span data-ttu-id="83ad2-192">El icono de flecha azul representa qué contexto está seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="83ad2-192">The blue arrow icon represents which context is currently selected.</span></span>  

:::image type="complex" source="../media/javascript-sources-main-min-js-threads.msft.png" alt-text="Panel Subprocesos" lightbox="../media/javascript-sources-main-min-js-threads.msft.png":::
   <span data-ttu-id="83ad2-194">Panel **Subprocesos**</span><span class="sxs-lookup"><span data-stu-id="83ad2-194">The **Threads** pane</span></span>  
:::image-end:::  

<span data-ttu-id="83ad2-195">Por ejemplo, suponga que está pausado en un punto de interrupción tanto en el script principal como en el script de trabajo de servicio.</span><span class="sxs-lookup"><span data-stu-id="83ad2-195">For example, suppose that you are paused on a breakpoint in both your main script and your service worker script.</span></span>  <span data-ttu-id="83ad2-196">Desea ver las propiedades locales y globales del contexto de trabajo de servicio, pero la herramienta **Orígenes** muestra el contexto de script principal.</span><span class="sxs-lookup"><span data-stu-id="83ad2-196">You want to view the local and global properties for the service worker context, but the **Sources** tool is showing the main script context.</span></span>  <span data-ttu-id="83ad2-197">Para cambiar al contexto de trabajo de servicio, en el **panel Subprocesos,** elija la entrada de trabajador de servicio.</span><span class="sxs-lookup"><span data-stu-id="83ad2-197">To switch to the service worker context, in the **Threads** pane, choose the service worker entry.</span></span>  

## <a name="view-and-edit-properties-and-variables"></a><span data-ttu-id="83ad2-198">Ver y editar propiedades y variables</span><span class="sxs-lookup"><span data-stu-id="83ad2-198">View and edit properties and variables</span></span>

<span data-ttu-id="83ad2-199">Mientras está pausado en una \*\*\*\* línea de código, use el panel Ámbito para ver y editar los valores de propiedades y variables en los ámbitos local, de cierre y global.</span><span class="sxs-lookup"><span data-stu-id="83ad2-199">While paused on a line of code, use the **Scope** pane to view and edit the values of properties and variables in the local, closure, and global scopes.</span></span>  

*   <span data-ttu-id="83ad2-200">Haga doble clic en un valor de propiedad para cambiarlo.</span><span class="sxs-lookup"><span data-stu-id="83ad2-200">Double-click a property value to change it.</span></span>  
*   <span data-ttu-id="83ad2-201">Las propiedades no enumerables están grises.</span><span class="sxs-lookup"><span data-stu-id="83ad2-201">Non-enumerable properties are greyed out.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-scope.msft.png" alt-text="Panel Ámbito" lightbox="../media/javascript-sources-get-started-js-scope.msft.png":::
   <span data-ttu-id="83ad2-203">Panel **Ámbito**</span><span class="sxs-lookup"><span data-stu-id="83ad2-203">The **Scope** pane</span></span>  
:::image-end:::  

## <a name="watch-the-values-of-javascript-expressions"></a><span data-ttu-id="83ad2-204">Ver los valores de las expresiones de JavaScript</span><span class="sxs-lookup"><span data-stu-id="83ad2-204">Watch the values of JavaScript expressions</span></span>  

<span data-ttu-id="83ad2-205">Use el **panel** Ver para ver los valores de las expresiones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="83ad2-205">Use the **Watch** pane to watch the values of custom expressions.</span></span>  <span data-ttu-id="83ad2-206">Puede ver cualquier expresión de JavaScript válida.</span><span class="sxs-lookup"><span data-stu-id="83ad2-206">You can watch any valid JavaScript expression.</span></span>  

:::image type="complex" source="../media/javascript-sources-get-started-js-watch.msft.png" alt-text="El panel Ver" lightbox="../media/javascript-sources-get-started-js-watch.msft.png":::
   <span data-ttu-id="83ad2-208">El **panel Ver**</span><span class="sxs-lookup"><span data-stu-id="83ad2-208">The **Watch** pane</span></span>  
:::image-end:::  

*   <span data-ttu-id="83ad2-209">Para crear una nueva expresión de reloj, seleccione el botón Agregar expresión **de** reloj \( ![ Agregar expresión de reloj ](../media/add-expression-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="83ad2-209">To create a new watch expression, select the **Add watch expression** \(![Add watch expression](../media/add-expression-icon.msft.png)\) button.</span></span>  
*   <span data-ttu-id="83ad2-210">Para actualizar los valores de todas las expresiones existentes, seleccione el botón **Actualizar** ![ \( Actualizar ](../media/refresh-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="83ad2-210">To refresh the values of all existing expressions, select the **Refresh** \(![Refresh](../media/refresh-icon.msft.png)\) button.</span></span>  <span data-ttu-id="83ad2-211">Los valores se actualizan automáticamente al pasar por el código.</span><span class="sxs-lookup"><span data-stu-id="83ad2-211">Values automatically refresh while stepping through code.</span></span>  
*   <span data-ttu-id="83ad2-212">Para eliminar una expresión de reloj, haga clic con el botón secundario en la expresión y, a continuación, seleccione **Eliminar** expresión de reloj \( ![ Eliminar expresión de reloj ](../media/delete-expression-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="83ad2-212">To delete a watch expression, right-click the expression and then select **Delete watch expression** \(![Delete watch expression](../media/delete-expression-icon.msft.png)\).</span></span>  

## <a name="view-the-call-stack"></a><span data-ttu-id="83ad2-213">Ver la pila de llamadas</span><span class="sxs-lookup"><span data-stu-id="83ad2-213">View the call stack</span></span>  

<span data-ttu-id="83ad2-214">Mientras está pausado en una línea de código, use el panel **Pila** de llamadas para ver la pila de llamadas que le ha hecho llegar hasta este punto.</span><span class="sxs-lookup"><span data-stu-id="83ad2-214">While paused on a line of code, use the **Call Stack** pane to view the call stack that got you to this point.</span></span>  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

<span data-ttu-id="83ad2-215">Elija una entrada para saltar a la línea de código donde se llamó a esa función.</span><span class="sxs-lookup"><span data-stu-id="83ad2-215">Choose an entry to jump to the line of code where that function was called.</span></span>  <span data-ttu-id="83ad2-216">El icono de flecha azul representa la función DevTools que está resaltando actualmente.</span><span class="sxs-lookup"><span data-stu-id="83ad2-216">The blue arrow icon represents which function DevTools is currently highlighting.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png" alt-text="Panel Pila de llamadas" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png":::
   <span data-ttu-id="83ad2-218">Panel **Pila de** llamadas</span><span class="sxs-lookup"><span data-stu-id="83ad2-218">The **Call Stack** pane</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="83ad2-219">Cuando no se pausa en una línea de código, el panel **Pila** de llamadas está vacío.</span><span class="sxs-lookup"><span data-stu-id="83ad2-219">When not paused on a line of code, the **Call Stack** pane is empty.</span></span>  

### <a name="copy-stack-trace"></a><span data-ttu-id="83ad2-220">Copiar seguimiento de pila</span><span class="sxs-lookup"><span data-stu-id="83ad2-220">Copy stack trace</span></span>  

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

<span data-ttu-id="83ad2-221">Para copiar la pila de llamadas actual \*\*\*\* en el Portapapeles, mantenga el mouse en cualquier lugar del panel Pila de llamadas, abra el menú contextual \(clic con el botón secundario\) y elija Copiar seguimiento **de pila**.</span><span class="sxs-lookup"><span data-stu-id="83ad2-221">To copy the current call stack to the clipboard, hover anywhere in the **Call Stack** pane, open the contextual menu \(right-click\), and choose **Copy stack trace**.</span></span>  

:::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png" alt-text="Elija Copiar seguimiento de pila" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png":::
   <span data-ttu-id="83ad2-223">Elija **Copiar seguimiento de pila**</span><span class="sxs-lookup"><span data-stu-id="83ad2-223">Choose **Copy Stack Trace**</span></span>  
:::image-end:::  

<span data-ttu-id="83ad2-224">El siguiente fragmento de código es un ejemplo de la salida.</span><span class="sxs-lookup"><span data-stu-id="83ad2-224">The following code snippet is an example of the output.</span></span>  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onChoose (get-started.js:15)
```  

## <a name="ignore-a-script-or-pattern-of-scripts"></a><span data-ttu-id="83ad2-225">Omitir un script o patrón de scripts</span><span class="sxs-lookup"><span data-stu-id="83ad2-225">Ignore a script or pattern of scripts</span></span>  

<span data-ttu-id="83ad2-226">Marca un script como código de biblioteca cuando quieras omitir ese script durante la depuración.</span><span class="sxs-lookup"><span data-stu-id="83ad2-226">Mark a script as Library code when you want to ignore that script while debugging.</span></span>  <span data-ttu-id="83ad2-227">Cuando se marca como código de biblioteca, un script se oculta en el panel Pila de llamadas y nunca se pasa a las funciones del script cuando se pasa por el código. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="83ad2-227">When marked as Library code, a script is obscured in the **Call Stack** pane, and you never step into the functions of the script when you step through your code.</span></span>  

<span data-ttu-id="83ad2-228">Por ejemplo, en el siguiente fragmento de código, line `A` usa , que es una biblioteca de `lib` terceros.</span><span class="sxs-lookup"><span data-stu-id="83ad2-228">For example, in the following code snippet, line `A` uses `lib`, which is a third-party library.</span></span>  <span data-ttu-id="83ad2-229">Si está seguro de que el problema que está depurando no está relacionado con esa biblioteca de terceros, tiene sentido marcar el script como **código de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="83ad2-229">If you are confident that the problem you are debugging is not related to that third-party library, then it makes sense to mark the script as **Library code**.</span></span>  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

### <a name="mark-a-script-as-library-code-from-the-editor-pane"></a><span data-ttu-id="83ad2-230">Marcar un script como código de biblioteca desde el panel Editor</span><span class="sxs-lookup"><span data-stu-id="83ad2-230">Mark a script as Library code from the Editor pane</span></span>  

<span data-ttu-id="83ad2-231">Para marcar un script como **código de biblioteca** desde el panel **Editor:**</span><span class="sxs-lookup"><span data-stu-id="83ad2-231">To mark a script as **Library code** from the **Editor** pane:</span></span>  

1.  <span data-ttu-id="83ad2-232">Abra el archivo.</span><span class="sxs-lookup"><span data-stu-id="83ad2-232">Open the file.</span></span>  
1.  <span data-ttu-id="83ad2-233">Mantenga el mouse en cualquier lugar y abra el menú contextual \(hacer clic con el botón secundario\).</span><span class="sxs-lookup"><span data-stu-id="83ad2-233">Hover anywhere and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="83ad2-234">Elija **Agregar script para omitir la lista** (anteriormente se muestra como Marcar como código de **biblioteca).**</span><span class="sxs-lookup"><span data-stu-id="83ad2-234">Choose **Add script to ignore list** (previously shown as **Mark as Library code**).</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde el panel Editor" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png":::
       <span data-ttu-id="83ad2-236">Marcar un script como **código de biblioteca** desde el panel **Editor**</span><span class="sxs-lookup"><span data-stu-id="83ad2-236">Mark a script as **Library code** from the **Editor** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-the-call-stack-pane"></a><span data-ttu-id="83ad2-237">Marcar un script como código de biblioteca desde el panel Pila de llamadas</span><span class="sxs-lookup"><span data-stu-id="83ad2-237">Mark a script as Library code from the Call Stack pane</span></span>  

<span data-ttu-id="83ad2-238">Para marcar un script como **código de biblioteca** desde el panel Pila **de** llamadas:</span><span class="sxs-lookup"><span data-stu-id="83ad2-238">To mark a script as **Library code** from the **Call Stack** pane:</span></span>  

1.  <span data-ttu-id="83ad2-239">Mantenga el mouse sobre una función del script y abra el menú contextual \(hacer clic con el botón secundario\).</span><span class="sxs-lookup"><span data-stu-id="83ad2-239">Hover on a function from the script and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="83ad2-240">Elija **Agregar script para omitir la lista** (anteriormente se muestra como Marcar como código de **biblioteca).**</span><span class="sxs-lookup"><span data-stu-id="83ad2-240">Choose **Add script to ignore list** (previously shown as **Mark as Library code**).</span></span>  
    
    :::image type="complex" source="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde el panel Pila de llamadas" lightbox="../media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png":::
       <span data-ttu-id="83ad2-242">Marcar un script como **código de biblioteca** desde el panel Pila **de** llamadas</span><span class="sxs-lookup"><span data-stu-id="83ad2-242">Mark a script as **Library code** from the **Call Stack** pane</span></span>  
    :::image-end:::  
    
### <a name="mark-a-script-as-library-code-from-settings"></a><span data-ttu-id="83ad2-243">Marcar un script como código de biblioteca desde Configuración</span><span class="sxs-lookup"><span data-stu-id="83ad2-243">Mark a script as Library code from Settings</span></span>  

<span data-ttu-id="83ad2-244">Para marcar un único script o patrón de scripts desde **Configuración**:</span><span class="sxs-lookup"><span data-stu-id="83ad2-244">To mark a single script or pattern of scripts from **Settings**:</span></span>  

1.  <span data-ttu-id="83ad2-245">Abra [Configuración][DevToolsCustomize].</span><span class="sxs-lookup"><span data-stu-id="83ad2-245">Open [Settings][DevToolsCustomize].</span></span>  
1.  <span data-ttu-id="83ad2-246">Vaya a la **configuración de código de biblioteca.**</span><span class="sxs-lookup"><span data-stu-id="83ad2-246">Navigate to the **Library code** setting.</span></span>  
1.  <span data-ttu-id="83ad2-247">Elija **Agregar patrón**.</span><span class="sxs-lookup"><span data-stu-id="83ad2-247">Choose **Add pattern**.</span></span>  
1.  <span data-ttu-id="83ad2-248">Escriba el nombre del script o un patrón regex de nombres de script para marcar como **código de biblioteca.**</span><span class="sxs-lookup"><span data-stu-id="83ad2-248">Enter the script name or a regex pattern of script names to mark as **Library code**.</span></span>  
1.  <span data-ttu-id="83ad2-249">Elija **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="83ad2-249">Choose **Add**.</span></span>  
    
    :::image type="complex" source="../media/javascript-framework-library-code.msft.png" alt-text="Marcar un script como código de biblioteca desde Configuración" lightbox="../media/javascript-framework-library-code.msft.png":::
       <span data-ttu-id="83ad2-251">Marcar un script como **código de biblioteca** desde **Configuración**</span><span class="sxs-lookup"><span data-stu-id="83ad2-251">Mark a script as **Library code** from **Settings**</span></span>  
    :::image-end:::  
    
## <a name="run-snippets-of-debug-code-from-any-page"></a><span data-ttu-id="83ad2-252">Ejecutar fragmentos de código de depuración desde cualquier página</span><span class="sxs-lookup"><span data-stu-id="83ad2-252">Run snippets of debug code from any page</span></span>  

<span data-ttu-id="83ad2-253">Si se encuentra ejecutando el mismo código de depuración en la consola una y otra vez, considere Fragmentos de código.</span><span class="sxs-lookup"><span data-stu-id="83ad2-253">If you find yourself running the same debug code in the Console over and over, consider Snippets.</span></span>  <span data-ttu-id="83ad2-254">Los fragmentos de código son scripts en tiempo de ejecución que se pueden crear, almacenar y ejecutar en DevTools.</span><span class="sxs-lookup"><span data-stu-id="83ad2-254">Snippets are runtime scripts that you author, store, and run within DevTools.</span></span>  

<span data-ttu-id="83ad2-255">Consulte [Ejecutar fragmentos de código de JavaScript en cualquier página web][DevToolsJavascriptSnippets].</span><span class="sxs-lookup"><span data-stu-id="83ad2-255">See [Run snippets of JavaScript on any webpage][DevToolsJavascriptSnippets].</span></span>  

## <a name="see-also"></a><span data-ttu-id="83ad2-256">Consulte también</span><span class="sxs-lookup"><span data-stu-id="83ad2-256">See also</span></span>  

*   <span data-ttu-id="83ad2-257">[Introducción Con depuración de JavaScript en Microsoft Edge DevTools:][DevToolsJavascriptGetStarted] un tutorial sencillo y breve con código existente, con capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="83ad2-257">[Get Started With Debugging JavaScript In Microsoft Edge DevTools][DevToolsJavascriptGetStarted] - A simple, short tutorial using existing code, with screen captures.</span></span>
*   <span data-ttu-id="83ad2-258">[Introducción a la herramienta][DevToolsSourcesIndex] Orígenes: la **herramienta Orígenes** incluye el depurador y el editor de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="83ad2-258">[Sources tool overview][DevToolsSourcesIndex] - The **Sources** tool includes the JavaScript debugger and editor.</span></span>
*   <span data-ttu-id="83ad2-259">[Deshabilitar JavaScript con Microsoft Edge DevTools][DevToolsJavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="83ad2-259">[Disable JavaScript with Microsoft Edge DevTools][DevToolsJavascriptDisable].</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="83ad2-260">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="83ad2-260">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptBreakpoints]: ./breakpoints.md "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptDisable]: ./disable.md "Deshabilitar JavaScript con Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptGetStarted]: ./index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavascriptSnippets]: ./snippets.md "Ejecute fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsSourcesIndex]: ../sources/index.md "Información general sobre la herramienta sources | Microsoft Docs"  
[DevToolsCustomize]: ../customize/index.md "Personalizar Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="83ad2-267">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="83ad2-267">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="83ad2-268">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="83ad2-268">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="83ad2-270">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="83ad2-270">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

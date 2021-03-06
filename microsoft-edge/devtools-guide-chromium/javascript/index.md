---
description: Obtenga información sobre cómo usar Microsoft Edge DevTools para buscar y corregir errores de JavaScript.
title: Introducción a la depuración de JavaScript en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e146c6708f097b1ea8dc82f08be58f5aa5e52d1f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398444"
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
# <a name="get-started-with-debugging-javascript-in-microsoft-edge-devtools"></a><span data-ttu-id="c1b9e-104">Introducción a la depuración de JavaScript en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c1b9e-104">Get started with debugging JavaScript in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="c1b9e-105">Este artículo le enseña el flujo de trabajo básico para depurar cualquier problema de JavaScript en DevTools.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-105">This article teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <a name="step-1-reproduce-the-bug"></a><span data-ttu-id="c1b9e-106">Paso 1: Reproducir el error</span><span class="sxs-lookup"><span data-stu-id="c1b9e-106">Step 1: Reproduce the bug</span></span>  

<span data-ttu-id="c1b9e-107">Encontrar una serie de acciones que reproducen un error de forma coherente siempre es el primer paso para la depuración.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-107">Finding a series of actions that consistently reproduce a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="c1b9e-108">Elija **Abrir demostración**.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-108">Choose **Open Demo**.</span></span>  <span data-ttu-id="c1b9e-109">Mantenga `Control` presionado \(Windows, Linux\) o `Command` \(macOS\) y abra la demostración en una nueva pestaña del explorador.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and open the demo in a new browser tab.</span></span>  
    
    [<span data-ttu-id="c1b9e-110">Demostración abierta</span><span class="sxs-lookup"><span data-stu-id="c1b9e-110">Open Demo</span></span>][OpenDebugJSDemo]  
    
1.  <span data-ttu-id="c1b9e-111">Escriba `5` en el cuadro de texto Número **1.**</span><span class="sxs-lookup"><span data-stu-id="c1b9e-111">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="c1b9e-112">Escriba `1` en el cuadro de texto Número **2.**</span><span class="sxs-lookup"><span data-stu-id="c1b9e-112">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="c1b9e-113">Elija **Agregar número 1 y número 2**.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-113">Choose **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="c1b9e-114">La etiqueta debajo del botón indica `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="c1b9e-114">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="c1b9e-115">El resultado debe ser `6` .</span><span class="sxs-lookup"><span data-stu-id="c1b9e-115">The result should be `6`.</span></span>  <span data-ttu-id="c1b9e-116">A continuación, corrija el error de adición que es el error.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-116">Next, fix the addition error that is the bug.</span></span>  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 da como resultado 51, pero debe ser 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` <span data-ttu-id="c1b9e-118">da como `51` resultado , pero debe ser</span><span class="sxs-lookup"><span data-stu-id="c1b9e-118">results in `51`, but should be</span></span> `6`  
    :::image-end:::  
    
## <a name="step-2-get-familiar-with-the-sources-tool-ui"></a><span data-ttu-id="c1b9e-119">Paso 2: Familiarizarse con la interfaz de usuario de la herramienta Orígenes</span><span class="sxs-lookup"><span data-stu-id="c1b9e-119">Step 2: Get familiar with the Sources tool UI</span></span>  

<span data-ttu-id="c1b9e-120">DevTools proporciona muchas herramientas diferentes para distintas tareas.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-120">DevTools provides many different tools for different tasks.</span></span>  <span data-ttu-id="c1b9e-121">Entre las tareas diferentes se incluyen cambiar CSS, generar perfiles de rendimiento de carga de página y supervisar solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-121">Different tasks include changing CSS, profiling page-load performance, and monitoring network requests.</span></span>  <span data-ttu-id="c1b9e-122">La **herramienta Orígenes** es donde se depura JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-122">The **Sources** tool is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="c1b9e-123">Para abrir la **herramienta Consola** en DevTools, seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="c1b9e-123">To open the **Console** tool in DevTools, select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="La herramienta Consola" lightbox="../media/javascript-console-empty.msft.png":::
       <span data-ttu-id="c1b9e-125">La **herramienta Consola**</span><span class="sxs-lookup"><span data-stu-id="c1b9e-125">The **Console** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c1b9e-126">Elija la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="c1b9e-126">Choose the **Sources** tool.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="La herramienta Orígenes" lightbox="../media/javascript-sources-sections.msft.png":::
       <span data-ttu-id="c1b9e-128">La **herramienta Orígenes**</span><span class="sxs-lookup"><span data-stu-id="c1b9e-128">The **Sources** tool</span></span>  
    :::image-end:::  
    
<span data-ttu-id="c1b9e-129">La **interfaz de usuario de** la herramienta Orígenes tiene tres partes.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-129">The **Sources** tool UI has three parts.</span></span>  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="Las 3 partes de la interfaz de usuario de la herramienta Orígenes" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   <span data-ttu-id="c1b9e-131">Las 3 partes de la interfaz **de usuario de la herramienta Orígenes**</span><span class="sxs-lookup"><span data-stu-id="c1b9e-131">The 3 parts of the **Sources** tool UI</span></span>  
:::image-end:::  

1.  <span data-ttu-id="c1b9e-132">El **panel Explorador de** archivos \(Sección 1 de la figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="c1b9e-132">The **File Navigator** panel \(Section 1 in the previous figure\).</span></span>  <span data-ttu-id="c1b9e-133">Aquí se enumeran todos los archivos que solicita la página web.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-133">Every file that the webpage requests is listed here.</span></span>  
1.  <span data-ttu-id="c1b9e-134">El **panel Editor de** código \(Sección 2 de la figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="c1b9e-134">The **Code Editor** panel \(Section 2 in the previous figure\).</span></span>  <span data-ttu-id="c1b9e-135">Después de seleccionar un archivo en el panel **Explorador de** archivos, el contenido de ese archivo se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-135">After selecting a file in the **File Navigator** pane, the contents of that file are displayed here.</span></span>  
1.  <span data-ttu-id="c1b9e-136">El **panel Depuración de JavaScript** \(Sección 3 de la figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="c1b9e-136">The **JavaScript Debugging** panel \(Section 3 in the previous figure\).</span></span>  <span data-ttu-id="c1b9e-137">Varias herramientas para inspeccionar JavaScript para la página web.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-137">Various tools for inspecting the JavaScript for the webpage.</span></span>  <span data-ttu-id="c1b9e-138">Si la ventana DevTools es amplia, este panel se muestra a la derecha del **panel Editor de** código.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-138">If your DevTools window is wide, this pane is displayed to the right of the **Code Editor** pane.</span></span>  
    
## <a name="step-3-pause-the-code-with-a-breakpoint"></a><span data-ttu-id="c1b9e-139">Paso 3: Pausar el código con un punto de interrupción</span><span class="sxs-lookup"><span data-stu-id="c1b9e-139">Step 3: Pause the code with a breakpoint</span></span>  

<span data-ttu-id="c1b9e-140">Un método común para depurar este tipo de problema es insertar varias instrucciones en el código y, a continuación, inspeccionar los valores a medida que `console.log()` se ejecuta el script.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-140">A common method for debugging this type of problem is to insert several `console.log()` statements into the code and then to inspect values as the script runs.</span></span>  <span data-ttu-id="c1b9e-141">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c1b9e-141">For example:</span></span>  

```javascript
function updateLabel() {
    var addend1 = getNumber1();
    console.log('addend1:', addend1);
    var addend2 = getNumber2();
    console.log('addend2:', addend2);
    var sum = addend1 + addend2;
    console.log('sum:', sum);
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
}
```  

<span data-ttu-id="c1b9e-142">El `console.log()` método puede realizar el trabajo, pero los puntos de **interrupción** lo hacen más rápido.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-142">The `console.log()` method may get the job done, but **breakpoints** get it done faster.</span></span>  <span data-ttu-id="c1b9e-143">Un punto de interrupción permite pausar el código en medio del tiempo de ejecución y examinar todos los valores en ese momento.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-143">A breakpoint allows you to pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="c1b9e-144">Los puntos de interrupción tienen las siguientes ventajas sobre el `console.log()` método.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-144">Breakpoints have the following advantages over the `console.log()` method.</span></span>  

*   <span data-ttu-id="c1b9e-145">Con , debe abrir manualmente el código fuente, buscar el código relevante, insertar las instrucciones y, a continuación, actualizar la página web para mostrar los mensajes en `console.log()` `console.log()` la **consola**.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-145">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.</span></span>  <span data-ttu-id="c1b9e-146">Con los puntos de interrupción, puede pausar el código relevante sin saber siquiera cómo se estructura el código.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-146">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="c1b9e-147">En las `console.log()` instrucciones, debe especificar explícitamente cada valor que desea inspeccionar.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-147">In your `console.log()` statements, you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="c1b9e-148">Con puntos de interrupción, DevTools muestra los valores de todas las variables en ese momento.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-148">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="c1b9e-149">A veces, las variables que afectan al código están ocultas y ocultas.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-149">Sometimes variables that affect your code are hidden and obfuscated.</span></span>  
    
<span data-ttu-id="c1b9e-150">En resumen, los puntos de interrupción pueden ayudarle a encontrar y corregir errores más rápido que el `console.log()` método.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-150">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="c1b9e-151">Si retroces y piensas en cómo funciona la aplicación, puedes hacer una conjetura educada de que la suma incorrecta \( \) se calcula en el agente de escucha de eventos asociado con los botones Agregar número 1 y Número `5 + 1 = 51` `click` **2.**</span><span class="sxs-lookup"><span data-stu-id="c1b9e-151">If you step back and think about how the app works, you may make an educated guess that the incorrect sum \(`5 + 1 = 51`\) is computed in the `click` event listener associated with the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="c1b9e-152">Por lo tanto, probablemente quiera pausar el código durante el tiempo en que se ejecute `click` el agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-152">So, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="c1b9e-153">**Los puntos de interrupción de escucha de** eventos le permiten hacer exactamente lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="c1b9e-153">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="c1b9e-154">En el **panel Depuración de JavaScript,** elija Puntos de interrupción de **escucha de eventos** para expandir la sección.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-154">In the **JavaScript Debugging** pane, choose **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="c1b9e-155">DevTools muestra una lista de categorías de eventos expandibles, como **Animación y** **Portapapeles.**</span><span class="sxs-lookup"><span data-stu-id="c1b9e-155">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="c1b9e-156">Junto a la categoría de eventos **Mouse,** elija **Expandir** \( ![ Expandir icono ][ImageExpandIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c1b9e-156">Next to the **Mouse** event category, choose **Expand** \(![Expand icon][ImageExpandIcon]\).</span></span>  <span data-ttu-id="c1b9e-157">DevTools muestra una lista de eventos de mouse, como clic **y** **mousedown**.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-157">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="c1b9e-158">Cada evento tiene una casilla junto a él.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-158">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="c1b9e-159">Seleccione la casilla situada junto **a**.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-159">Choose the checkbox next to **click**.</span></span>  <span data-ttu-id="c1b9e-160">DevTools ahora está configurado para pausar automáticamente cuando se ejecuta cualquier `click` escucha de eventos.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-160">DevTools is now set up to automatically pause when any `click` event listener runs.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Seleccione la casilla situada junto a hacer clic" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       <span data-ttu-id="c1b9e-162">Seleccione la casilla situada junto a **hacer clic**</span><span class="sxs-lookup"><span data-stu-id="c1b9e-162">Choose the checkbox next to **click**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c1b9e-163">En la demostración, vuelve **a elegir Agregar número 1 y Número 2.**</span><span class="sxs-lookup"><span data-stu-id="c1b9e-163">Back on the demo, choose **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="c1b9e-164">DevTools pausa la demostración y resalta una línea de código en la **herramienta** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-164">DevTools pauses the demo and highlights a line of code in the **Sources** tool.</span></span>  <span data-ttu-id="c1b9e-165">DevTools debe pausar la línea 16 en `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="c1b9e-165">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="c1b9e-166">Si pausa en una línea de código diferente, elija Reanudar ejecución de **script** \( Reanudar ejecución de script \) hasta que se detenga ![ en la línea ][ImageResumeIcon] correcta.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-166">If you pause on a different line of code, choose **Resume Script Execution** \(![Resume Script Execution][ImageResumeIcon]\) until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c1b9e-167">Si hizo una pausa en una línea diferente, tiene una extensión de explorador que registra un agente de escucha de eventos en todas las páginas `click` web que visita.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-167">If you paused on a different line, you have a browser extension that registers a `click` event listener on every webpage that you visit.</span></span>  <span data-ttu-id="c1b9e-168">Está en pausa en el agente `click` de escucha de la extensión.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-168">You are paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="c1b9e-169">Si usa el modo InPrivate para examinar en privado **,** lo que deshabilita todas las extensiones, es posible que vea que se pausa en la línea de código deseada cada vez.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-169">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="c1b9e-170">**Los puntos de interrupción de escucha de** eventos son solo uno de los muchos tipos de puntos de interrupción disponibles en DevTools.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-170">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="c1b9e-171">Memoriza todos los tipos diferentes para ayudarte a depurar escenarios diferentes lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-171">Memorize all the different types to help you debug different scenarios as quickly as possible.</span></span>  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <a name="step-4-step-through-the-code"></a><span data-ttu-id="c1b9e-172">Paso 4: Paso a paso por el código</span><span class="sxs-lookup"><span data-stu-id="c1b9e-172">Step 4: Step through the code</span></span>  

<span data-ttu-id="c1b9e-173">Una causa común de errores es cuando un script se ejecuta en el orden incorrecto.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-173">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="c1b9e-174">El paso a través del código le permite recorrer el tiempo de ejecución del código.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-174">Stepping through your code allows you to walk through the runtime of your code.</span></span>  <span data-ttu-id="c1b9e-175">Puede recorrer una línea a la vez para ayudarle a averiguar exactamente dónde se ejecuta el código en un orden diferente del esperado.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-175">You walk through one line at a time to help you figure out exactly where your code is running in a different order than you expect.</span></span>  <span data-ttu-id="c1b9e-176">Pruébalo ahora:</span><span class="sxs-lookup"><span data-stu-id="c1b9e-176">Try it now:</span></span>  

1.  <span data-ttu-id="c1b9e-177">Elija **Paso sobre la siguiente llamada de función** \( Paso sobre la siguiente llamada de función ![ ][ImageOverIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c1b9e-177">Choose **Step over next function call** \(![Step over next function call][ImageOverIcon]\).</span></span>  <span data-ttu-id="c1b9e-178">DevTools ejecuta el siguiente código sin entrar en él.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-178">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="c1b9e-179">DevTools omite algunas líneas de código.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-179">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="c1b9e-180">Esto se debe a que se evalúa como false, por lo que no se ejecuta el bloque `inputsAreEmpty()` de código de la `if` instrucción.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-180">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  
    
1.  <span data-ttu-id="c1b9e-181">En la **herramienta Orígenes** de DevTools, elija Paso a siguiente llamada de función **\(** Paso a siguiente llamada de función \) para pasar por el tiempo de ejecución de la función, una línea ![ a ][ImageIntoIcon] `updateLabel()` la vez.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-181">On the **Sources** tool of DevTools, choose **Step into next function call** \(![Step into next function call][ImageIntoIcon]\) to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  
    
<span data-ttu-id="c1b9e-182">Revisar una línea a la vez es la idea básica de pasar por el código.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-182">Reviewing one line at a time is the basic idea of stepping through code.</span></span>  <span data-ttu-id="c1b9e-183">Si revisa el código en , el error probablemente esté en `get-started.js` algún lugar de la `updateLabel()` función.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-183">If you review the code in `get-started.js`, the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="c1b9e-184">En lugar de pasar por todas las líneas de código, puede usar otro tipo de punto de interrupción para pausar el código más cerca de la ubicación probable del error.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-184">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <a name="step-5-set-a-line-of-code-breakpoint"></a><span data-ttu-id="c1b9e-185">Paso 5: Establecer un punto de interrupción de línea de código</span><span class="sxs-lookup"><span data-stu-id="c1b9e-185">Step 5: Set a line-of-code breakpoint</span></span>  

<span data-ttu-id="c1b9e-186">Los puntos de interrupción de línea de código son el tipo más común de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-186">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="c1b9e-187">Cuando llegue a la línea de código específica que desea pausar, use un punto de interrupción de línea de código.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-187">When you get to the specific line of code you want to pause, use a line-of-code breakpoint.</span></span>  

1.  <span data-ttu-id="c1b9e-188">Vea la última línea de código en `updateLabel()` :</span><span class="sxs-lookup"><span data-stu-id="c1b9e-188">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="c1b9e-189">A la izquierda, el número de esta línea de código en particular se muestra como **34**.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-189">On the left, the number of this particular line of code is displayed as **34**.</span></span>  <span data-ttu-id="c1b9e-190">Elija la **línea 34**.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-190">Choose line **34**.</span></span>  <span data-ttu-id="c1b9e-191">DevTools muestra un icono rojo a la izquierda de **34**.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-191">DevTools displays a red icon to the left of **34**.</span></span>  <span data-ttu-id="c1b9e-192">El icono rojo indica que un punto de interrupción de línea de código está en esta línea.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-192">The red icon indicates that a line-of-code breakpoint is on this line.</span></span>  <span data-ttu-id="c1b9e-193">DevTools siempre se pausa antes de que se ejecute esta línea de código.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-193">DevTools always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="c1b9e-194">Elija **Reanudar ejecución de script** \( Reanudar ejecución de script ![ ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c1b9e-194">Choose **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  <span data-ttu-id="c1b9e-195">El script continúa en ejecución hasta que llega a la línea 33.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-195">The script continues to run until it reaches line 33.</span></span>  <span data-ttu-id="c1b9e-196">En las líneas 31, 32 y 33, DevTools imprime los valores de , y a la derecha de los dos puntos y coma `addend1` `addend2` en cada `sum` línea.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-196">On lines 31, 32, and 33, DevTools prints the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools se pausa en el punto de interrupción de línea de código en la línea 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       <span data-ttu-id="c1b9e-198">DevTools se pausa en el punto de interrupción de línea de código en la línea 34</span><span class="sxs-lookup"><span data-stu-id="c1b9e-198">DevTools pauses on the line-of-code breakpoint on line 34</span></span>  
    :::image-end:::  
    
## <a name="step-6-check-variable-values"></a><span data-ttu-id="c1b9e-199">Paso 6: Comprobar valores de variables</span><span class="sxs-lookup"><span data-stu-id="c1b9e-199">Step 6: Check variable values</span></span>  

<span data-ttu-id="c1b9e-200">Los valores de `addend1` , `addend2` y parecen `sum` sospechosos.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-200">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="c1b9e-201">Los valores están entre comillas.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-201">The values are wrapped in quotes.</span></span>  <span data-ttu-id="c1b9e-202">Las comillas significan que el valor es una cadena, que es una buena hipótesis para explicar la causa del error.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-202">The quotations mean that the value is a string, which is a good hypothesis to explain the cause of the bug.</span></span>  <span data-ttu-id="c1b9e-203">Recopila más información sobre la situación.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-203">Gather more information about the situation.</span></span>  <span data-ttu-id="c1b9e-204">DevTools proporciona muchas herramientas para examinar valores de variables.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-204">DevTools provides many tools for examining variable values.</span></span>  

### <a name="method-1-the-scope-panel"></a><span data-ttu-id="c1b9e-205">Método 1: panel Ámbito</span><span class="sxs-lookup"><span data-stu-id="c1b9e-205">Method 1: The Scope panel</span></span>  

<span data-ttu-id="c1b9e-206">Si se pausa en una línea de código, el **panel** Ámbito muestra las variables locales y globales que están definidas actualmente, junto con el valor de cada variable.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-206">If you pause on a line of code, the **Scope** panel displays the local and global variables that are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="c1b9e-207">También muestra variables de cierre, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-207">It also displays closure variables, as applicable.</span></span>  <span data-ttu-id="c1b9e-208">Haga doble clic en un valor de variable para editarlo.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-208">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="c1b9e-209">Si no se pausa en una línea de código, **el** panel Ámbito está vacío.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-209">If you don't pause on a line of code, the **Scope** panel is empty.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Panel Ámbito" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   <span data-ttu-id="c1b9e-211">Panel **Ámbito**</span><span class="sxs-lookup"><span data-stu-id="c1b9e-211">The **Scope** pane</span></span>  
:::image-end:::  

### <a name="method-2-watch-expressions"></a><span data-ttu-id="c1b9e-212">Método 2: Ver expresiones</span><span class="sxs-lookup"><span data-stu-id="c1b9e-212">Method 2: Watch Expressions</span></span>  

<span data-ttu-id="c1b9e-213">El **panel Ver expresiones** le permite supervisar los valores de las variables a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-213">The **Watch Expressions** panel lets you monitor the values of variables over time.</span></span>  <span data-ttu-id="c1b9e-214">Como su nombre indica, **las expresiones de** reloj no se limitan a variables.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-214">As the name implies, **Watch Expressions** aren't limited to variables.</span></span>  <span data-ttu-id="c1b9e-215">Puede almacenar cualquier expresión de JavaScript válida en una **expresión Watch**.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-215">You may store any valid JavaScript expression in a **Watch Expression**.</span></span>  <span data-ttu-id="c1b9e-216">Pruébalo ahora.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-216">Try it now.</span></span>  

1.  <span data-ttu-id="c1b9e-217">Elija **el** panel Ver.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-217">Choose the **Watch** panel.</span></span>  
1.  <span data-ttu-id="c1b9e-218">Elija **Agregar expresión** \( Agregar expresión ![ ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c1b9e-218">Choose **Add Expression** \(![Add Expression][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="c1b9e-219">Escribe `typeof sum`.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-219">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="c1b9e-220">Seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c1b9e-220">Select `Enter`.</span></span>  <span data-ttu-id="c1b9e-221">DevTools muestra `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="c1b9e-221">DevTools shows `typeof sum: "string"`.</span></span>  <span data-ttu-id="c1b9e-222">El valor a la derecha de los dos puntos es el resultado de la expresión Watch.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-222">The value to the right of the colon is the result of your Watch Expression.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="c1b9e-223">En el **panel Ver expresión** \(bottom-right\) de la siguiente figura, se muestra la expresión `typeof sum` watch.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-223">In the **Watch Expression** pane \(bottom-right\) in the following figure, the `typeof sum` Watch Expression is displayed.</span></span>  <span data-ttu-id="c1b9e-224">Si la ventana DevTools es grande, el panel **Ver** expresión se encuentra a la derecha encima del panel Puntos de interrupción **de escucha de eventos.**</span><span class="sxs-lookup"><span data-stu-id="c1b9e-224">If your DevTools window is large, the **Watch Expression** pane is on the right above the **Event Listener Breakpoints** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Panel Expresión de reloj" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   <span data-ttu-id="c1b9e-226">Panel **Expresión de** reloj</span><span class="sxs-lookup"><span data-stu-id="c1b9e-226">The **Watch Expression** panel</span></span>  
:::image-end:::  

<span data-ttu-id="c1b9e-227">Como se sospecha, `sum` se está evaluando como una cadena, cuando debe ser un número.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-227">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="c1b9e-228">Ahora ha confirmado que el tipo de valor es la causa del error.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-228">You now confirmed value type is the cause of the bug.</span></span>  

### <a name="method-3-the-console"></a><span data-ttu-id="c1b9e-229">Método 3: La consola</span><span class="sxs-lookup"><span data-stu-id="c1b9e-229">Method 3: The Console</span></span>  

<span data-ttu-id="c1b9e-230">La **consola** le permite ver mensajes y también puede usarlos para evaluar `console.log()` instrucciones de JavaScript arbitrarias.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-230">The **Console** allows you to view `console.log()` messages and you may also use it to evaluate arbitrary JavaScript statements.</span></span>  <span data-ttu-id="c1b9e-231">Para la depuración, puede usar la **consola** para probar posibles correcciones de errores.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-231">For debugging, you may use the **Console** to test potential fixes for bugs.</span></span>  <span data-ttu-id="c1b9e-232">Pruébalo ahora.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-232">Try it now.</span></span>  

1.  <span data-ttu-id="c1b9e-233">Si la **herramienta** Consola está cerrada, seleccione `Escape` para abrirla.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-233">If the **Console** tool is closed, select `Escape` to open it.</span></span>  <span data-ttu-id="c1b9e-234">La **herramienta** Consola se abre en el panel inferior de la ventana DevTools.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-234">The **Console** tool opens in the lower panel of the DevTools window.</span></span>  
1.  <span data-ttu-id="c1b9e-235">En la **consola**, escriba `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="c1b9e-235">In the **Console**, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="c1b9e-236">La instrucción que la herramienta se pausa en una línea de código donde `addend1` y están en el `addend2` ámbito.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-236">The statement the tool is paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="c1b9e-237">Seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c1b9e-237">Select `Enter`.</span></span>  <span data-ttu-id="c1b9e-238">DevTools evalúa la instrucción e imprime , que es el `6` resultado que espera que la demostración produzca.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-238">DevTools evaluates the statement and prints `6`, which is the result you expect the demo to produce.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="La herramienta Consola, después de evaluar parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       <span data-ttu-id="c1b9e-240">La **herramienta Consola,** después de evaluar</span><span class="sxs-lookup"><span data-stu-id="c1b9e-240">The **Console** tool, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <a name="step-7-apply-a-fix"></a><span data-ttu-id="c1b9e-241">Paso 7: Aplicar una corrección</span><span class="sxs-lookup"><span data-stu-id="c1b9e-241">Step 7: Apply a fix</span></span>  

<span data-ttu-id="c1b9e-242">Si encuentras una solución para el error, prueba la corrección editando el código y rerunning la demostración.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-242">If you find a fix for the bug, try out your fix by editing the code and rerunning the demo.</span></span>  <span data-ttu-id="c1b9e-243">Puede editar código JavaScript directamente en la interfaz de usuario de DevTools y aplicar la corrección.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-243">You may edit JavaScript code directly within the DevTools UI and apply the fix.</span></span>  <span data-ttu-id="c1b9e-244">Pruébalo ahora.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-244">Try it now.</span></span>  

1.  <span data-ttu-id="c1b9e-245">Elija **Reanudar ejecución de script** \( Reanudar ejecución de script ![ ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c1b9e-245">Choose **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  
1.  <span data-ttu-id="c1b9e-246">En el **Editor de código,** reemplace la línea 32, `var sum = addend1 + addend2` , por `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="c1b9e-246">In the **Code Editor**, replace line 32, `var sum = addend1 + addend2`, with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="c1b9e-247">Seleccione `Control` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\) para guardar el cambio.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-247">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="c1b9e-248">Elija **Desactivar puntos de interrupción** \( Desactivar puntos de ![ interrupción ][ImageDeactivateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c1b9e-248">Choose **Deactivate breakpoints** \(![Deactivate breakpoints][ImageDeactivateIcon]\).</span></span>  <span data-ttu-id="c1b9e-249">Cambia de color azul para indicar que la opción está activa.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-249">It changes blue to indicate the option is active.</span></span>  <span data-ttu-id="c1b9e-250">Mientras **se establecen los puntos** de interrupción Deactivate, DevTools omite los puntos de interrupción establecidos.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-250">While **Deactivate breakpoints** is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="c1b9e-251">Pruebe la demostración con valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-251">Try out the demo with different values.</span></span>  <span data-ttu-id="c1b9e-252">La demostración ahora calcula correctamente.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-252">The demo now calculates correctly.</span></span>  
    
> [!CAUTION]
> <span data-ttu-id="c1b9e-253">Este flujo de trabajo solo aplica una corrección al código que se ejecuta en el explorador.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-253">This workflow only applies a fix to the code that is running in your browser.</span></span>  <span data-ttu-id="c1b9e-254">No corrige el código de todos los usuarios que visitan la página web.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-254">It does not fix the code for all users that visit your webpage.</span></span>  <span data-ttu-id="c1b9e-255">Para ello, debe corregir el código que está en los servidores.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-255">To do that, you need to fix the code that is on your servers.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="c1b9e-256">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="c1b9e-256">Next steps</span></span>  

<span data-ttu-id="c1b9e-257">¡Enhorabuena!</span><span class="sxs-lookup"><span data-stu-id="c1b9e-257">Congratulations!</span></span>  <span data-ttu-id="c1b9e-258">Ahora sabe cómo obtener el máximo partido de Microsoft Edge DevTools al depurar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-258">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="c1b9e-259">Las herramientas y los métodos que aprendió en este artículo pueden ahorrarle incontables horas.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-259">The tools and methods you learned in this article may save you countless hours.</span></span>  

<span data-ttu-id="c1b9e-260">Este artículo solo le enseñó dos formas de establecer puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-260">This article only taught you two ways to set breakpoints.</span></span>  <span data-ttu-id="c1b9e-261">DevTools ofrece muchas otras formas, incluida la siguiente configuración.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-261">DevTools offers many other ways including the following settings.</span></span>  

*   <span data-ttu-id="c1b9e-262">Puntos de interrupción condicionales que solo se desencadenan cuando la condición que se proporciona es true.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-262">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="c1b9e-263">Puntos de interrupción en excepciones capturadas o no capturadas.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-263">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="c1b9e-264">Puntos de interrupción XHR que se desencadenan cuando la dirección URL solicitada coincide con una subcadena que se proporciona.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-264">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  
    
<span data-ttu-id="c1b9e-265">Para obtener más información sobre cuándo y cómo usar cada tipo, vaya [a Pausar el código con puntos de interrupción][DevtoolsJavscriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="c1b9e-265">For more information about when and how to use each type, navigate to [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].</span></span>  

<span data-ttu-id="c1b9e-266">En este artículo no se explica un par de controles de paso a paso de código.</span><span class="sxs-lookup"><span data-stu-id="c1b9e-266">A couple of code stepping controls aren't explained in this article.</span></span>  <span data-ttu-id="c1b9e-267">Para obtener más información, vaya [a Paso sobre la línea de código][DevtoolsJavascriptReferenceStepThroughCode].</span><span class="sxs-lookup"><span data-stu-id="c1b9e-267">For more information, navigate to [Step over line of code][DevtoolsJavascriptReferenceStepThroughCode].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c1b9e-268">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c1b9e-268">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Paso a paso por el código: referencia de depuración de JavaScript | Microsoft Docs"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Abra la demostración | Glitch"  

> [!NOTE]
> <span data-ttu-id="c1b9e-272">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c1b9e-272">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c1b9e-273">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="c1b9e-273">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c1b9e-275">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c1b9e-275">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

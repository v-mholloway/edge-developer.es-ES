---
description: Obtenga información sobre cómo usar Microsoft Edge DevTools para buscar y corregir errores de JavaScript.
title: Introducción a la depuración de JavaScript en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: a60bd0c734df18ba7424cde6a828abbd9e7135a9
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519376"
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
# <a name="get-started-with-debugging-javascript-in-microsoft-edge-devtools"></a><span data-ttu-id="bcef1-104">Introducción a la depuración de JavaScript en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bcef1-104">Get started with debugging JavaScript in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="bcef1-105">Este artículo le enseña el flujo de trabajo básico para depurar cualquier problema de JavaScript en DevTools.</span><span class="sxs-lookup"><span data-stu-id="bcef1-105">This article teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <a name="step-1-reproduce-the-bug"></a><span data-ttu-id="bcef1-106">Paso 1: Reproducir el error</span><span class="sxs-lookup"><span data-stu-id="bcef1-106">Step 1: Reproduce the bug</span></span>  

<span data-ttu-id="bcef1-107">Encontrar una serie de acciones que reproducen un error de forma coherente siempre es el primer paso para la depuración.</span><span class="sxs-lookup"><span data-stu-id="bcef1-107">Finding a series of actions that consistently reproduce a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="bcef1-108">Elija el siguiente **vínculo Abrir demostración** y abra la página web en una nueva pestaña.  Para abrir la demostración en una pestaña nueva, seleccione y mantenga presionada `Ctrl` \(Windows, Linux\) o `Command` \(macOS\) y, a continuación, elija **Abrir demostración**.</span><span class="sxs-lookup"><span data-stu-id="bcef1-108">Choose the following **Open Demo** link and open the webpage in a new tab.  To open the demo in a new tab, select and hold `Ctrl` \(Windows, Linux\) or `Command` \(macOS\), and then choose **Open Demo**.</span></span>  
    
    [<span data-ttu-id="bcef1-109">Demostración abierta</span><span class="sxs-lookup"><span data-stu-id="bcef1-109">Open Demo</span></span>][OpenDebugJSDemo]  
    
1.  <span data-ttu-id="bcef1-110">Escriba `5` en el cuadro de texto Número **1.**</span><span class="sxs-lookup"><span data-stu-id="bcef1-110">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="bcef1-111">Escriba `1` en el cuadro de texto Número **2.**</span><span class="sxs-lookup"><span data-stu-id="bcef1-111">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="bcef1-112">Elija **Agregar número 1 y número 2**.</span><span class="sxs-lookup"><span data-stu-id="bcef1-112">Choose **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="bcef1-113">La etiqueta debajo del botón indica `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="bcef1-113">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="bcef1-114">El resultado debe ser `6` .</span><span class="sxs-lookup"><span data-stu-id="bcef1-114">The result should be `6`.</span></span>  <span data-ttu-id="bcef1-115">A continuación, corrija el error de adición que es el error.</span><span class="sxs-lookup"><span data-stu-id="bcef1-115">Next, fix the addition error that is the bug.</span></span>  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 da como resultado 51, pero debe ser 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` <span data-ttu-id="bcef1-117">da como `51` resultado , pero debe ser</span><span class="sxs-lookup"><span data-stu-id="bcef1-117">results in `51`, but should be</span></span> `6`  
    :::image-end:::  
    
## <a name="step-2-get-familiar-with-the-sources-tool-ui"></a><span data-ttu-id="bcef1-118">Paso 2: Familiarizarse con la interfaz de usuario de la herramienta Orígenes</span><span class="sxs-lookup"><span data-stu-id="bcef1-118">Step 2: Get familiar with the Sources tool UI</span></span>  

<span data-ttu-id="bcef1-119">DevTools proporciona muchas herramientas diferentes para distintas tareas.</span><span class="sxs-lookup"><span data-stu-id="bcef1-119">DevTools provides many different tools for different tasks.</span></span>  <span data-ttu-id="bcef1-120">Entre las tareas diferentes se incluyen cambiar CSS, generar perfiles de rendimiento de carga de página y supervisar solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="bcef1-120">Different tasks include changing CSS, profiling page-load performance, and monitoring network requests.</span></span>  <span data-ttu-id="bcef1-121">La **herramienta Orígenes** es donde se depura JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bcef1-121">The **Sources** tool is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="bcef1-122">Para abrir la **herramienta Consola** en DevTools, seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="bcef1-122">To open the **Console** tool in DevTools, select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="La herramienta Consola" lightbox="../media/javascript-console-empty.msft.png":::
       <span data-ttu-id="bcef1-124">La **herramienta Consola**</span><span class="sxs-lookup"><span data-stu-id="bcef1-124">The **Console** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bcef1-125">Elija la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="bcef1-125">Choose the **Sources** tool.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="La herramienta Orígenes" lightbox="../media/javascript-sources-sections.msft.png":::
       <span data-ttu-id="bcef1-127">La **herramienta Orígenes**</span><span class="sxs-lookup"><span data-stu-id="bcef1-127">The **Sources** tool</span></span>  
    :::image-end:::  
    
<span data-ttu-id="bcef1-128">La **interfaz de usuario de** la herramienta Orígenes tiene tres partes.</span><span class="sxs-lookup"><span data-stu-id="bcef1-128">The **Sources** tool UI has three parts.</span></span>  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="Las 3 partes de la interfaz de usuario de la herramienta Orígenes" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   <span data-ttu-id="bcef1-130">Las 3 partes de la interfaz **de usuario de la herramienta Orígenes**</span><span class="sxs-lookup"><span data-stu-id="bcef1-130">The 3 parts of the **Sources** tool UI</span></span>  
:::image-end:::  

1.  <span data-ttu-id="bcef1-131">El **panel** Navegador \(Sección 1 de la figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="bcef1-131">The **Navigator** pane \(Section 1 in the previous figure\).</span></span>  <span data-ttu-id="bcef1-132">Aquí se enumeran todos los archivos que solicita la página web.</span><span class="sxs-lookup"><span data-stu-id="bcef1-132">Every file that the webpage requests is listed here.</span></span>  
1.  <span data-ttu-id="bcef1-133">El **panel Editor** \(Sección 2 de la figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="bcef1-133">The **Editor** pane \(Section 2 in the previous figure\).</span></span>  <span data-ttu-id="bcef1-134">Después de elegir un archivo en el panel **Navegador,** este panel muestra el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="bcef1-134">After you choose a file in the **Navigator** pane, this pane displays the contents of the file.</span></span>  
1.  <span data-ttu-id="bcef1-135">El **panel** Depurador \(Sección 3 de la figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="bcef1-135">The **Debugger** pane \(Section 3 in the previous figure\).</span></span>  <span data-ttu-id="bcef1-136">Este panel proporciona herramientas para inspeccionar JavaScript para la página web.</span><span class="sxs-lookup"><span data-stu-id="bcef1-136">This pane provides tools for inspecting the JavaScript for the webpage.</span></span>  <span data-ttu-id="bcef1-137">Si la ventana DevTools es amplia, este panel se muestra a la derecha del **panel Editor.**</span><span class="sxs-lookup"><span data-stu-id="bcef1-137">If your DevTools window is wide, this pane is displayed to the right of the **Editor** pane.</span></span>  
    
## <a name="step-3-pause-the-code-with-a-breakpoint"></a><span data-ttu-id="bcef1-138">Paso 3: Pausar el código con un punto de interrupción</span><span class="sxs-lookup"><span data-stu-id="bcef1-138">Step 3: Pause the code with a breakpoint</span></span>  

<span data-ttu-id="bcef1-139">Un método común para depurar este tipo de problema es insertar varias instrucciones en el código y, a continuación, inspeccionar los valores a medida que `console.log()` se ejecuta el script.</span><span class="sxs-lookup"><span data-stu-id="bcef1-139">A common method for debugging this type of problem is to insert several `console.log()` statements into the code and then to inspect values as the script runs.</span></span>  <span data-ttu-id="bcef1-140">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="bcef1-140">For example:</span></span>  

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

<span data-ttu-id="bcef1-141">El `console.log()` método puede realizar el trabajo, pero los puntos de **interrupción** lo hacen más rápido.</span><span class="sxs-lookup"><span data-stu-id="bcef1-141">The `console.log()` method may get the job done, but **breakpoints** get it done faster.</span></span>  <span data-ttu-id="bcef1-142">Un punto de interrupción permite pausar el código en medio del tiempo de ejecución y examinar todos los valores en ese momento.</span><span class="sxs-lookup"><span data-stu-id="bcef1-142">A breakpoint allows you to pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="bcef1-143">Los puntos de interrupción tienen las siguientes ventajas sobre el `console.log()` método.</span><span class="sxs-lookup"><span data-stu-id="bcef1-143">Breakpoints have the following advantages over the `console.log()` method.</span></span>  

*   <span data-ttu-id="bcef1-144">Con , debe abrir manualmente el código fuente, buscar el código relevante, insertar las instrucciones y, a continuación, actualizar la página web para mostrar los mensajes en `console.log()` `console.log()` la **consola**.</span><span class="sxs-lookup"><span data-stu-id="bcef1-144">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.</span></span>  <span data-ttu-id="bcef1-145">Con los puntos de interrupción, puede pausar el código relevante sin saber siquiera cómo se estructura el código.</span><span class="sxs-lookup"><span data-stu-id="bcef1-145">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="bcef1-146">En las `console.log()` instrucciones, debe especificar explícitamente cada valor que desea inspeccionar.</span><span class="sxs-lookup"><span data-stu-id="bcef1-146">In your `console.log()` statements, you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="bcef1-147">Con puntos de interrupción, DevTools muestra los valores de todas las variables en ese momento.</span><span class="sxs-lookup"><span data-stu-id="bcef1-147">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="bcef1-148">A veces, las variables que afectan al código están ocultas y ocultas.</span><span class="sxs-lookup"><span data-stu-id="bcef1-148">Sometimes variables that affect your code are hidden and obfuscated.</span></span>  
    
<span data-ttu-id="bcef1-149">En resumen, los puntos de interrupción pueden ayudarle a encontrar y corregir errores más rápido que el `console.log()` método.</span><span class="sxs-lookup"><span data-stu-id="bcef1-149">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="bcef1-150">Si retroces y piensas en cómo funciona la aplicación, puedes hacer una conjetura educada de que la suma incorrecta \( \) se calcula en el agente de escucha de eventos asociado con los botones Agregar número 1 y Número `5 + 1 = 51` `click` **2.**</span><span class="sxs-lookup"><span data-stu-id="bcef1-150">If you step back and think about how the app works, you may make an educated guess that the incorrect sum \(`5 + 1 = 51`\) is computed in the `click` event listener associated with the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="bcef1-151">Por lo tanto, probablemente quiera pausar el código durante el tiempo en que se ejecute `click` el agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="bcef1-151">So, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="bcef1-152">**Los puntos de interrupción de escucha de** eventos le permiten hacer exactamente lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bcef1-152">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="bcef1-153">En el **panel Depurador,** elija Puntos de interrupción **de escucha de eventos** para expandir la sección.</span><span class="sxs-lookup"><span data-stu-id="bcef1-153">In the **Debugger** pane, choose **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="bcef1-154">DevTools muestra una lista de categorías de eventos expandibles, como **Animación y** **Portapapeles.**</span><span class="sxs-lookup"><span data-stu-id="bcef1-154">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="bcef1-155">Junto a la categoría de eventos **Mouse,** elija **Expandir** \( ![ Expandir icono ](../media/expand-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="bcef1-155">Next to the **Mouse** event category, choose **Expand** \(![Expand icon](../media/expand-icon.msft.png)\).</span></span>  <span data-ttu-id="bcef1-156">DevTools muestra una lista de eventos de mouse, como clic **y** **mousedown**.</span><span class="sxs-lookup"><span data-stu-id="bcef1-156">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="bcef1-157">Cada evento tiene una casilla junto a él.</span><span class="sxs-lookup"><span data-stu-id="bcef1-157">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="bcef1-158">Seleccione la casilla situada junto **a**.</span><span class="sxs-lookup"><span data-stu-id="bcef1-158">Choose the checkbox next to **click**.</span></span>  <span data-ttu-id="bcef1-159">DevTools ahora está configurado para pausar automáticamente cuando se ejecuta cualquier `click` escucha de eventos.</span><span class="sxs-lookup"><span data-stu-id="bcef1-159">DevTools is now set up to automatically pause when any `click` event listener runs.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Seleccione la casilla situada junto a hacer clic" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       <span data-ttu-id="bcef1-161">Seleccione la casilla situada junto a **hacer clic**</span><span class="sxs-lookup"><span data-stu-id="bcef1-161">Choose the checkbox next to **click**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="bcef1-162">En la demostración, vuelve **a elegir Agregar número 1 y Número 2.**</span><span class="sxs-lookup"><span data-stu-id="bcef1-162">Back on the demo, choose **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="bcef1-163">DevTools pausa la demostración y resalta una línea de código en la **herramienta** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="bcef1-163">DevTools pauses the demo and highlights a line of code in the **Sources** tool.</span></span>  <span data-ttu-id="bcef1-164">DevTools debe pausar la línea 16 en `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="bcef1-164">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="bcef1-165">Si pausa en una línea de código diferente, elija Reanudar ejecución de **script** \( Reanudar ejecución de script \) hasta que se detenga ![ en la línea ](../media/resume-script-run-icon.msft.png) correcta.</span><span class="sxs-lookup"><span data-stu-id="bcef1-165">If you pause on a different line of code, choose **Resume Script Execution** \(![Resume Script Execution](../media/resume-script-run-icon.msft.png)\) until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="bcef1-166">Si hizo una pausa en una línea diferente, tiene una extensión de explorador que registra un agente de escucha de eventos en todas las páginas `click` web que visita.</span><span class="sxs-lookup"><span data-stu-id="bcef1-166">If you paused on a different line, you have a browser extension that registers a `click` event listener on every webpage that you visit.</span></span>  <span data-ttu-id="bcef1-167">Está en pausa en el agente `click` de escucha de la extensión.</span><span class="sxs-lookup"><span data-stu-id="bcef1-167">You are paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="bcef1-168">Si usa el modo InPrivate para examinar en privado **,** lo que deshabilita todas las extensiones, es posible que vea que se pausa en la línea de código deseada cada vez.</span><span class="sxs-lookup"><span data-stu-id="bcef1-168">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="bcef1-169">**Los puntos de interrupción de escucha de** eventos son solo uno de los muchos tipos de puntos de interrupción disponibles en DevTools.</span><span class="sxs-lookup"><span data-stu-id="bcef1-169">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="bcef1-170">Memoriza todos los tipos diferentes para ayudarte a depurar escenarios diferentes lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="bcef1-170">Memorize all the different types to help you debug different scenarios as quickly as possible.</span></span>  <!--  To learn when and how to use each type, navigate to [Pause your code with breakpoints][JSBreakpoints].  -->  

## <a name="step-4-step-through-the-code"></a><span data-ttu-id="bcef1-171">Paso 4: Paso a paso por el código</span><span class="sxs-lookup"><span data-stu-id="bcef1-171">Step 4: Step through the code</span></span>  

<span data-ttu-id="bcef1-172">Una causa común de errores es cuando un script se ejecuta en el orden incorrecto.</span><span class="sxs-lookup"><span data-stu-id="bcef1-172">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="bcef1-173">El paso a través del código le permite recorrer el tiempo de ejecución del código.</span><span class="sxs-lookup"><span data-stu-id="bcef1-173">Stepping through your code allows you to walk through the runtime of your code.</span></span>  <span data-ttu-id="bcef1-174">Puede recorrer una línea a la vez para ayudarle a averiguar exactamente dónde se ejecuta el código en un orden diferente del esperado.</span><span class="sxs-lookup"><span data-stu-id="bcef1-174">You walk through one line at a time to help you figure out exactly where your code is running in a different order than you expect.</span></span>  <span data-ttu-id="bcef1-175">Pruébalo ahora:</span><span class="sxs-lookup"><span data-stu-id="bcef1-175">Try it now:</span></span>  

1.  <span data-ttu-id="bcef1-176">Elija **Paso sobre la siguiente llamada de función** \( Paso sobre la siguiente llamada de función ![ ](../media/step-over-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="bcef1-176">Choose **Step over next function call** \(![Step over next function call](../media/step-over-icon.msft.png)\).</span></span>  <span data-ttu-id="bcef1-177">DevTools ejecuta el siguiente código sin entrar en él.</span><span class="sxs-lookup"><span data-stu-id="bcef1-177">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="bcef1-178">DevTools omite algunas líneas de código.</span><span class="sxs-lookup"><span data-stu-id="bcef1-178">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="bcef1-179">Esto se debe a que se evalúa como false, por lo que no se ejecuta el bloque `inputsAreEmpty()` de código de la `if` instrucción.</span><span class="sxs-lookup"><span data-stu-id="bcef1-179">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  
    
1.  <span data-ttu-id="bcef1-180">En la **herramienta Orígenes** de DevTools, elija Paso a siguiente llamada de función **\(** Paso a siguiente llamada de función \) para pasar por el tiempo de ejecución de la función, una línea ![ a ](../media/step-into-icon.msft.png) `updateLabel()` la vez.</span><span class="sxs-lookup"><span data-stu-id="bcef1-180">On the **Sources** tool of DevTools, choose **Step into next function call** \(![Step into next function call](../media/step-into-icon.msft.png)\) to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  
    
<span data-ttu-id="bcef1-181">Revisar una línea a la vez es la idea básica de pasar por el código.</span><span class="sxs-lookup"><span data-stu-id="bcef1-181">Reviewing one line at a time is the basic idea of stepping through code.</span></span>  <span data-ttu-id="bcef1-182">Si revisa el código en , el error probablemente esté en `get-started.js` algún lugar de la `updateLabel()` función.</span><span class="sxs-lookup"><span data-stu-id="bcef1-182">If you review the code in `get-started.js`, the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="bcef1-183">En lugar de pasar por todas las líneas de código, puede usar otro tipo de punto de interrupción para pausar el código más cerca de la ubicación probable del error.</span><span class="sxs-lookup"><span data-stu-id="bcef1-183">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <a name="step-5-set-a-line-of-code-breakpoint"></a><span data-ttu-id="bcef1-184">Paso 5: Establecer un punto de interrupción de línea de código</span><span class="sxs-lookup"><span data-stu-id="bcef1-184">Step 5: Set a line-of-code breakpoint</span></span>  

<span data-ttu-id="bcef1-185">Los puntos de interrupción de línea de código son el tipo más común de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="bcef1-185">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="bcef1-186">Cuando llegue a la línea de código específica que desea pausar, use un punto de interrupción de línea de código.</span><span class="sxs-lookup"><span data-stu-id="bcef1-186">When you get to the specific line of code you want to pause, use a line-of-code breakpoint.</span></span>  

1.  <span data-ttu-id="bcef1-187">Vea la última línea de código en `updateLabel()` :</span><span class="sxs-lookup"><span data-stu-id="bcef1-187">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="bcef1-188">A la izquierda, el número de esta línea de código en particular se muestra como **34**.</span><span class="sxs-lookup"><span data-stu-id="bcef1-188">On the left, the number of this particular line of code is displayed as **34**.</span></span>  <span data-ttu-id="bcef1-189">Elija la **línea 34**.</span><span class="sxs-lookup"><span data-stu-id="bcef1-189">Choose line **34**.</span></span>  <span data-ttu-id="bcef1-190">DevTools muestra un icono rojo a la izquierda de **34**.</span><span class="sxs-lookup"><span data-stu-id="bcef1-190">DevTools displays a red icon to the left of **34**.</span></span>  <span data-ttu-id="bcef1-191">El icono rojo indica que un punto de interrupción de línea de código está en esta línea.</span><span class="sxs-lookup"><span data-stu-id="bcef1-191">The red icon indicates that a line-of-code breakpoint is on this line.</span></span>  <span data-ttu-id="bcef1-192">DevTools siempre se pausa antes de que se ejecute esta línea de código.</span><span class="sxs-lookup"><span data-stu-id="bcef1-192">DevTools always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="bcef1-193">Elija **Reanudar ejecución de script** \( Reanudar ejecución de script ![ ](../media/resume-script-run-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="bcef1-193">Choose **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\).</span></span>  <span data-ttu-id="bcef1-194">El script continúa en ejecución hasta que llega a la línea 33.</span><span class="sxs-lookup"><span data-stu-id="bcef1-194">The script continues to run until it reaches line 33.</span></span>  <span data-ttu-id="bcef1-195">En las líneas 31, 32 y 33, DevTools imprime los valores de , y a la derecha de los dos puntos y coma `addend1` `addend2` en cada `sum` línea.</span><span class="sxs-lookup"><span data-stu-id="bcef1-195">On lines 31, 32, and 33, DevTools prints the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools se pausa en el punto de interrupción de línea de código en la línea 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       <span data-ttu-id="bcef1-197">DevTools se pausa en el punto de interrupción de línea de código en la línea 34</span><span class="sxs-lookup"><span data-stu-id="bcef1-197">DevTools pauses on the line-of-code breakpoint on line 34</span></span>  
    :::image-end:::  
    
## <a name="step-6-check-variable-values"></a><span data-ttu-id="bcef1-198">Paso 6: Comprobar valores de variables</span><span class="sxs-lookup"><span data-stu-id="bcef1-198">Step 6: Check variable values</span></span>  

<span data-ttu-id="bcef1-199">Los valores de `addend1` , `addend2` y parecen `sum` sospechosos.</span><span class="sxs-lookup"><span data-stu-id="bcef1-199">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="bcef1-200">Los valores están entre comillas.</span><span class="sxs-lookup"><span data-stu-id="bcef1-200">The values are wrapped in quotes.</span></span>  <span data-ttu-id="bcef1-201">Las comillas significan que el valor es una cadena, que es una buena hipótesis para explicar la causa del error.</span><span class="sxs-lookup"><span data-stu-id="bcef1-201">The quotations mean that the value is a string, which is a good hypothesis to explain the cause of the bug.</span></span>  <span data-ttu-id="bcef1-202">Recopila más información sobre la situación.</span><span class="sxs-lookup"><span data-stu-id="bcef1-202">Gather more information about the situation.</span></span>  <span data-ttu-id="bcef1-203">DevTools proporciona muchas herramientas para examinar valores de variables.</span><span class="sxs-lookup"><span data-stu-id="bcef1-203">DevTools provides many tools for examining variable values.</span></span>  

### <a name="method-1-the-scope-pane"></a><span data-ttu-id="bcef1-204">Método 1: panel Ámbito</span><span class="sxs-lookup"><span data-stu-id="bcef1-204">Method 1: The Scope pane</span></span>  

<span data-ttu-id="bcef1-205">Si se pausa en una \*\*\*\* línea de código, el panel Ámbito muestra las variables locales y globales que están definidas actualmente, junto con el valor de cada variable.</span><span class="sxs-lookup"><span data-stu-id="bcef1-205">If you pause on a line of code, the **Scope** pane displays the local and global variables that are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="bcef1-206">También muestra variables de cierre, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="bcef1-206">It also displays closure variables, as applicable.</span></span>  <span data-ttu-id="bcef1-207">Haga doble clic en un valor de variable para editarlo.</span><span class="sxs-lookup"><span data-stu-id="bcef1-207">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="bcef1-208">Si no se pausa en una línea de código, **el** panel Ámbito está vacío.</span><span class="sxs-lookup"><span data-stu-id="bcef1-208">If you don't pause on a line of code, the **Scope** pane is empty.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Panel Ámbito" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   <span data-ttu-id="bcef1-210">Panel **Ámbito**</span><span class="sxs-lookup"><span data-stu-id="bcef1-210">The **Scope** pane</span></span>  
:::image-end:::  

### <a name="method-2-watch-expressions"></a><span data-ttu-id="bcef1-211">Método 2: Ver expresiones</span><span class="sxs-lookup"><span data-stu-id="bcef1-211">Method 2: Watch Expressions</span></span>  

<span data-ttu-id="bcef1-212">El **panel** Ver permite supervisar los valores de variables (como ) o `sum` expresiones (como `typeof sum` ).</span><span class="sxs-lookup"><span data-stu-id="bcef1-212">The **Watch** pane allows you to monitor the values of variables (such as `sum`) or expressions (such as `typeof sum`).</span></span>  <span data-ttu-id="bcef1-213">Puede almacenar cualquier expresión de JavaScript válida en una expresión watch.</span><span class="sxs-lookup"><span data-stu-id="bcef1-213">You may store any valid JavaScript expression in a Watch Expression.</span></span>  

1.  <span data-ttu-id="bcef1-214">Elija el **panel** Ver.</span><span class="sxs-lookup"><span data-stu-id="bcef1-214">Choose the **Watch** pane.</span></span>  
1.  <span data-ttu-id="bcef1-215">Elija **Agregar expresión de reloj** \( Agregar expresión de reloj ![ ](../media/add-expression-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="bcef1-215">Choose **Add watch expression** \(![Add watch expression](../media/add-expression-icon.msft.png)\).</span></span>  
1.  <span data-ttu-id="bcef1-216">Escriba `typeof sum`.</span><span class="sxs-lookup"><span data-stu-id="bcef1-216">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="bcef1-217">Seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="bcef1-217">Select `Enter`.</span></span>  <span data-ttu-id="bcef1-218">DevTools muestra `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="bcef1-218">DevTools displays `typeof sum: "string"`.</span></span>  <span data-ttu-id="bcef1-219">El valor a la derecha de los dos puntos es el resultado de la expresión Watch.</span><span class="sxs-lookup"><span data-stu-id="bcef1-219">The value to the right of the colon is the result of your Watch Expression.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="bcef1-220">En la siguiente figura, la `typeof sum` expresión watch se muestra en el **panel** Ver.</span><span class="sxs-lookup"><span data-stu-id="bcef1-220">In the following figure, the `typeof sum` Watch Expression is displayed in the **Watch** pane.</span></span>  <span data-ttu-id="bcef1-221">Si la ventana DevTools es amplia, el **panel** Ver se muestra en el panel **Depurador,** que aparece a la derecha.</span><span class="sxs-lookup"><span data-stu-id="bcef1-221">If your DevTools window is wide, the **Watch** pane is displayed within the **Debugger** pane, which then appears on the right.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="El panel Ver" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   <span data-ttu-id="bcef1-223">El **panel Ver**</span><span class="sxs-lookup"><span data-stu-id="bcef1-223">The **Watch** pane</span></span>  
:::image-end:::  

<span data-ttu-id="bcef1-224">Como se sospecha, `sum` se está evaluando como una cadena, cuando debe ser un número.</span><span class="sxs-lookup"><span data-stu-id="bcef1-224">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="bcef1-225">Ahora ha confirmado que el tipo de valor es la causa del error.</span><span class="sxs-lookup"><span data-stu-id="bcef1-225">You now confirmed value type is the cause of the bug.</span></span>  

### <a name="method-3-the-console"></a><span data-ttu-id="bcef1-226">Método 3: La consola</span><span class="sxs-lookup"><span data-stu-id="bcef1-226">Method 3: The Console</span></span>  

<span data-ttu-id="bcef1-227">La **consola** le permite ver el `console.log()` resultado.</span><span class="sxs-lookup"><span data-stu-id="bcef1-227">The **Console** allows you to view `console.log()` output.</span></span>  <span data-ttu-id="bcef1-228">También puede usar la consola **para** evaluar instrucciones de JavaScript arbitrarias mientras el depurador se pausa en una instrucción de código.</span><span class="sxs-lookup"><span data-stu-id="bcef1-228">You can also use the **Console** to evaluate arbitrary JavaScript statements while the debugger is paused at a code statement.</span></span>  <span data-ttu-id="bcef1-229">Para la depuración, puede usar **la** consola para probar posibles correcciones de errores.</span><span class="sxs-lookup"><span data-stu-id="bcef1-229">For debugging, you can use the **Console** to test potential fixes for bugs.</span></span>

1.  <span data-ttu-id="bcef1-230">Si la **herramienta** Consola está cerrada, seleccione `Esc` para abrirla.</span><span class="sxs-lookup"><span data-stu-id="bcef1-230">If the **Console** tool is closed, select `Esc` to open it.</span></span>  <span data-ttu-id="bcef1-231">La **herramienta** Consola se abre en el panel inferior de la ventana DevTools.</span><span class="sxs-lookup"><span data-stu-id="bcef1-231">The **Console** tool opens in the lower pane of the DevTools window.</span></span>  
1.  <span data-ttu-id="bcef1-232">En la **consola**, escriba `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="bcef1-232">In the **Console**, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="bcef1-233">La instrucción que la herramienta se pausa en una línea de código donde `addend1` y están en el `addend2` ámbito.</span><span class="sxs-lookup"><span data-stu-id="bcef1-233">The statement the tool is paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="bcef1-234">Seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="bcef1-234">Select `Enter`.</span></span>  <span data-ttu-id="bcef1-235">DevTools evalúa la instrucción e imprime , que es el `6` resultado que espera que la demostración produzca.</span><span class="sxs-lookup"><span data-stu-id="bcef1-235">DevTools evaluates the statement and prints `6`, which is the result you expect the demo to produce.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="La herramienta Consola, después de evaluar parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       <span data-ttu-id="bcef1-237">La **herramienta Consola,** después de evaluar</span><span class="sxs-lookup"><span data-stu-id="bcef1-237">The **Console** tool, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <a name="step-7-apply-a-fix"></a><span data-ttu-id="bcef1-238">Paso 7: Aplicar una corrección</span><span class="sxs-lookup"><span data-stu-id="bcef1-238">Step 7: Apply a fix</span></span>  

<span data-ttu-id="bcef1-239">Hemos identificado una posible corrección para el error.</span><span class="sxs-lookup"><span data-stu-id="bcef1-239">We've identified a possible fix for the bug.</span></span>  <span data-ttu-id="bcef1-240">A continuación, edite el código JavaScript directamente en la interfaz de usuario de DevTools y vuelva a ejecutar la demostración para probar la corrección, de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="bcef1-240">Next, edit the JavaScript code directly within the DevTools UI and then rerun the demo to test the fix, as follows.</span></span>

1.  <span data-ttu-id="bcef1-241">Elija **Reanudar ejecución de script** \( Reanudar ejecución de script ![ ](../media/resume-script-run-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="bcef1-241">Choose **Resume script execution** \(![Resume script execution](../media/resume-script-run-icon.msft.png)\).</span></span>  
1.  <span data-ttu-id="bcef1-242">En el **panel Editor,** reemplace la línea `var sum = addend1 + addend2` por `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="bcef1-242">In the **Editor** pane, replace the line `var sum = addend1 + addend2` with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="bcef1-243">Seleccione `Control` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\) para guardar el cambio.</span><span class="sxs-lookup"><span data-stu-id="bcef1-243">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="bcef1-244">Elija **Desactivar puntos de interrupción** \( Desactivar puntos de ![ interrupción ](../media/deactivate-breakpoints-button-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="bcef1-244">Choose **Deactivate breakpoints** \(![Deactivate breakpoints](../media/deactivate-breakpoints-button-icon.msft.png)\).</span></span>  <span data-ttu-id="bcef1-245">Cambia de color azul para indicar que la opción está activa.</span><span class="sxs-lookup"><span data-stu-id="bcef1-245">It changes blue to indicate the option is active.</span></span>  <span data-ttu-id="bcef1-246">Mientras **se establecen los puntos** de interrupción Deactivate, DevTools omite los puntos de interrupción establecidos.</span><span class="sxs-lookup"><span data-stu-id="bcef1-246">While **Deactivate breakpoints** is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="bcef1-247">Pruebe la demostración con valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="bcef1-247">Try out the demo with different values.</span></span>  <span data-ttu-id="bcef1-248">La demostración ahora calcula correctamente.</span><span class="sxs-lookup"><span data-stu-id="bcef1-248">The demo now calculates correctly.</span></span>  
    
> [!CAUTION]
> <span data-ttu-id="bcef1-249">Este flujo de trabajo solo aplica una corrección a una copia local del código enviado desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="bcef1-249">This workflow only applies a fix to a local copy of the code sent from the server.</span></span>  <span data-ttu-id="bcef1-250">Al depurar el proyecto, después de identificar la corrección, debe aplicar esa corrección al código del servidor, por ejemplo, editando el código fuente local y, a continuación, implementando de nuevo el código fijo en el servidor.</span><span class="sxs-lookup"><span data-stu-id="bcef1-250">When debugging your project, after you identify the fix, you still need to apply that fix to the code on the server, such as by editing your local source code and then re-deploying your fixed code to the server.</span></span>

## <a name="next-steps"></a><span data-ttu-id="bcef1-251">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="bcef1-251">Next steps</span></span>  

<span data-ttu-id="bcef1-252">¡Enhorabuena!</span><span class="sxs-lookup"><span data-stu-id="bcef1-252">Congratulations!</span></span>  <span data-ttu-id="bcef1-253">Ahora sabe cómo obtener el máximo partido de Microsoft Edge DevTools al depurar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bcef1-253">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="bcef1-254">Las herramientas y los métodos que aprendió en este artículo pueden ahorrarle incontables horas.</span><span class="sxs-lookup"><span data-stu-id="bcef1-254">The tools and methods you learned in this article may save you countless hours.</span></span>  

<span data-ttu-id="bcef1-255">En este artículo se mostraron dos formas de establecer puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="bcef1-255">This article showed two ways to set breakpoints.</span></span>  <span data-ttu-id="bcef1-256">DevTools también proporciona formas de establecer puntos de interrupción para pausar el código cuando se cumplen determinadas condiciones, como:</span><span class="sxs-lookup"><span data-stu-id="bcef1-256">DevTools also provides ways to set breakpoints to pause your code when certain conditions are met, such as:</span></span>

*   <span data-ttu-id="bcef1-257">Puntos de interrupción condicionales que solo se desencadenan cuando la condición que se proporciona es true.</span><span class="sxs-lookup"><span data-stu-id="bcef1-257">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="bcef1-258">Puntos de interrupción en excepciones capturadas o no capturadas.</span><span class="sxs-lookup"><span data-stu-id="bcef1-258">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="bcef1-259">Puntos de interrupción XHR que se desencadenan cuando la dirección URL solicitada coincide con una subcadena que se proporciona.</span><span class="sxs-lookup"><span data-stu-id="bcef1-259">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  
    
<span data-ttu-id="bcef1-260">Para obtener más información sobre cuándo y cómo usar cada tipo, vaya [a Pausar el código con puntos de interrupción.][DevToolsJavscriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="bcef1-260">For more information about when and how to use each type, navigate to [Pause your code with breakpoints][DevToolsJavscriptBreakpoints].</span></span>  

<span data-ttu-id="bcef1-261">En este artículo no se explica un par de controles de paso a paso de código.</span><span class="sxs-lookup"><span data-stu-id="bcef1-261">A couple of code stepping controls aren't explained in this article.</span></span>  <span data-ttu-id="bcef1-262">Para obtener más información, vaya [a Paso sobre la línea de código][DevToolsJavascriptReferenceStepThroughCode] en el artículo "Usar las características del depurador".</span><span class="sxs-lookup"><span data-stu-id="bcef1-262">For more information, navigate to [Step over line of code][DevToolsJavascriptReferenceStepThroughCode] in the "Use the debugger features" article.</span></span>

### <a name="see-also"></a><span data-ttu-id="bcef1-263">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bcef1-263">See also</span></span>

*   <span data-ttu-id="bcef1-264">[Usar las características del depurador:][DevToolsJavascriptReference] usar la interfaz de usuario del depurador en la herramienta Orígenes.</span><span class="sxs-lookup"><span data-stu-id="bcef1-264">[Use the debugger features][DevToolsJavascriptReference] - Using the UI of the debugger in the Sources tool.</span></span>
*   <span data-ttu-id="bcef1-265">[Introducción a la herramienta Sources:][DevToolsSourcesIndex] presenta el depurador de JavaScript y el editor de código.</span><span class="sxs-lookup"><span data-stu-id="bcef1-265">[Sources tool overview][DevToolsSourcesIndex] - Introduces the JavaScript debugger and code editor.</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="bcef1-266">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bcef1-266">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptReference]: ./reference.md "Usar las características del depurador | Microsoft Docs"  
[DevToolsSourcesIndex]: ../sources/index.md "Información general sobre la herramienta sources | Microsoft Docs"  
[DevToolsJavscriptBreakpoints]: ./breakpoints.md "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft Docs"
[DevToolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Paso a través del código: use las características del depurador | Microsoft Docs"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Abra la demostración | Glitch"  

> [!NOTE]
> <span data-ttu-id="bcef1-272">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bcef1-272">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="bcef1-273">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="bcef1-273">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="bcef1-275">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bcef1-275">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

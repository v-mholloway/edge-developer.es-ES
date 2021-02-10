---
description: Aprende a usar Microsoft Edge DevTools para buscar y corregir errores de JavaScript.
title: Introducción a la depuración de JavaScript en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: b036fc87149d13446ab1bc05afc8fc8631d27c8d
ms.sourcegitcommit: e737277744dd25a7585c113eef22a2aa4d4c167f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "11325954"
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
# <span data-ttu-id="7a892-104">Introducción a la depuración de JavaScript en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7a892-104">Get started with debugging JavaScript in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="7a892-105">Este artículo le enseña el flujo de trabajo básico para depurar cualquier problema de JavaScript en DevTools.</span><span class="sxs-lookup"><span data-stu-id="7a892-105">This article teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <span data-ttu-id="7a892-106">Paso 1: Reproducir el error</span><span class="sxs-lookup"><span data-stu-id="7a892-106">Step 1: Reproduce the bug</span></span>  

<span data-ttu-id="7a892-107">Encontrar una serie de acciones que reproduzcan de forma coherente un error siempre es el primer paso para la depuración.</span><span class="sxs-lookup"><span data-stu-id="7a892-107">Finding a series of actions that consistently reproduce a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="7a892-108">Elija **Abrir demostración.**</span><span class="sxs-lookup"><span data-stu-id="7a892-108">Choose **Open Demo**.</span></span>  <span data-ttu-id="7a892-109">Espera `Control` \(Windows, Linux\) o \(macOS\) y abre la `Command` demostración en una nueva pestaña del explorador.</span><span class="sxs-lookup"><span data-stu-id="7a892-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and open the demo in a new browser tab.</span></span>  
    
    [<span data-ttu-id="7a892-110">Demostración abierta</span><span class="sxs-lookup"><span data-stu-id="7a892-110">Open Demo</span></span>][OpenDebugJSDemo]  
    
1.  <span data-ttu-id="7a892-111">Escriba `5` en el cuadro de texto Número **1.**</span><span class="sxs-lookup"><span data-stu-id="7a892-111">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="7a892-112">Escriba `1` en el cuadro de texto Número **2.**</span><span class="sxs-lookup"><span data-stu-id="7a892-112">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="7a892-113">Elija **Agregar número 1 y Número 2.**</span><span class="sxs-lookup"><span data-stu-id="7a892-113">Choose **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="7a892-114">La etiqueta debajo del botón indica `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="7a892-114">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="7a892-115">El resultado debe ser `6` .</span><span class="sxs-lookup"><span data-stu-id="7a892-115">The result should be `6`.</span></span>  <span data-ttu-id="7a892-116">A continuación, corrija el error de adición que es el error.</span><span class="sxs-lookup"><span data-stu-id="7a892-116">Next, fix the addition error that is the bug.</span></span>  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="5 + 1 da como resultado 51, pero debe ser 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       `5 + 1` <span data-ttu-id="7a892-118">da como `51` resultado , pero debe ser</span><span class="sxs-lookup"><span data-stu-id="7a892-118">results in `51`, but should be</span></span> `6`  
    :::image-end:::  
    
## <span data-ttu-id="7a892-119">Paso 2: Familiarizarse con la interfaz de usuario del panel Orígenes</span><span class="sxs-lookup"><span data-stu-id="7a892-119">Step 2: Get familiar with the Sources panel UI</span></span>  

<span data-ttu-id="7a892-120">DevTools proporciona muchas herramientas diferentes para diferentes tareas.</span><span class="sxs-lookup"><span data-stu-id="7a892-120">DevTools provides many different tools for different tasks.</span></span>  <span data-ttu-id="7a892-121">Entre las distintas tareas se incluyen el cambio de CSS, la generación de perfiles de rendimiento de la carga de páginas y la supervisión de solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="7a892-121">Different tasks include changing CSS, profiling page-load performance, and monitoring network requests.</span></span>  <span data-ttu-id="7a892-122">El \*\*\*\* panel Orígenes es donde se depura JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7a892-122">The **Sources** panel is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="7a892-123">Abre DevTools presionando `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="7a892-123">Open DevTools by pressing `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="7a892-124">Este acceso directo abre el panel **Consola.**</span><span class="sxs-lookup"><span data-stu-id="7a892-124">This shortcut opens the **Console** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Panel de consola" lightbox="../media/javascript-console-empty.msft.png":::
       <span data-ttu-id="7a892-126">La **herramienta consola**</span><span class="sxs-lookup"><span data-stu-id="7a892-126">The **Console** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a892-127">Elija la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="7a892-127">Choose the **Sources** tool.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Panel Orígenes" lightbox="../media/javascript-sources-sections.msft.png":::
       <span data-ttu-id="7a892-129">Panel **Orígenes**</span><span class="sxs-lookup"><span data-stu-id="7a892-129">The **Sources** panel</span></span>  
    :::image-end:::  
    
<span data-ttu-id="7a892-130">La **interfaz de** usuario del panel Orígenes tiene tres partes.</span><span class="sxs-lookup"><span data-stu-id="7a892-130">The **Sources** panel UI has three parts.</span></span>  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="Las 3 partes de la interfaz de usuario del panel Orígenes" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   <span data-ttu-id="7a892-132">Las 3 partes de la interfaz de usuario **del** panel Orígenes</span><span class="sxs-lookup"><span data-stu-id="7a892-132">The 3 parts of the **Sources** panel UI</span></span>  
:::image-end:::  

1.  <span data-ttu-id="7a892-133">El **panel Navegador de** archivos \(Sección 1 de la figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="7a892-133">The **File Navigator** pane \(Section 1 in the previous figure\).</span></span>  <span data-ttu-id="7a892-134">Todos los archivos que solicita la página web se enumeran aquí.</span><span class="sxs-lookup"><span data-stu-id="7a892-134">Every file that the webpage requests is listed here.</span></span>  
1.  <span data-ttu-id="7a892-135">El **panel Editor** de código \(Sección 2 de la figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="7a892-135">The **Code Editor** pane \(Section 2 in the previous figure\).</span></span>  <span data-ttu-id="7a892-136">Después de seleccionar un archivo en el panel Navegador **de** archivos, el contenido de ese archivo se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="7a892-136">After selecting a file in the **File Navigator** pane, the contents of that file are displayed here.</span></span>  
1.  <span data-ttu-id="7a892-137">El **panel depuración de JavaScript** \(Sección 3 de la figura anterior\).</span><span class="sxs-lookup"><span data-stu-id="7a892-137">The **JavaScript Debugging** pane \(Section 3 in the previous figure\).</span></span>  <span data-ttu-id="7a892-138">Varias herramientas para inspeccionar el JavaScript de la página web.</span><span class="sxs-lookup"><span data-stu-id="7a892-138">Various tools for inspecting the JavaScript for the webpage.</span></span>  <span data-ttu-id="7a892-139">Si la ventana de DevTools es ancha, este panel se muestra a la derecha del **panel Editor de** código.</span><span class="sxs-lookup"><span data-stu-id="7a892-139">If your DevTools window is wide, this pane is displayed to the right of the **Code Editor** pane.</span></span>  
    
## <span data-ttu-id="7a892-140">Paso 3: Pausar el código con un punto de interrupción</span><span class="sxs-lookup"><span data-stu-id="7a892-140">Step 3: Pause the code with a breakpoint</span></span>  

<span data-ttu-id="7a892-141">Un método común para depurar este tipo de problema es insertar varias instrucciones en el código y, a continuación, inspeccionar los valores a medida que `console.log()` se ejecuta el script.</span><span class="sxs-lookup"><span data-stu-id="7a892-141">A common method for debugging this type of problem is to insert several `console.log()` statements into the code and then to inspect values as the script runs.</span></span>  <span data-ttu-id="7a892-142">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="7a892-142">For example:</span></span>  

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

<span data-ttu-id="7a892-143">El `console.log()` método puede realizar el trabajo, pero los puntos de **interrupción** lo hacen más rápido.</span><span class="sxs-lookup"><span data-stu-id="7a892-143">The `console.log()` method may get the job done, but **breakpoints** get it done faster.</span></span>  <span data-ttu-id="7a892-144">Un punto de interrupción le permite pausar el código en medio del tiempo de ejecución y examinar todos los valores en ese momento.</span><span class="sxs-lookup"><span data-stu-id="7a892-144">A breakpoint lets you pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="7a892-145">Los puntos de interrupción tienen algunas ventajas sobre el `console.log()` método:</span><span class="sxs-lookup"><span data-stu-id="7a892-145">Breakpoints have a few advantages over the `console.log()` method:</span></span>  

*   <span data-ttu-id="7a892-146">With `console.log()` , you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.</span><span class="sxs-lookup"><span data-stu-id="7a892-146">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then refresh the webpage to display the messages in the **Console**.</span></span>  <span data-ttu-id="7a892-147">Con los puntos de interrupción, puede pausar el código relevante sin saber cómo está estructurado el código.</span><span class="sxs-lookup"><span data-stu-id="7a892-147">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="7a892-148">En las `console.log()` instrucciones, debe especificar explícitamente cada valor que desee inspeccionar.</span><span class="sxs-lookup"><span data-stu-id="7a892-148">In your `console.log()` statements, you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="7a892-149">Con los puntos de interrupción, DevTools muestra los valores de todas las variables en ese momento en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="7a892-149">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="7a892-150">A veces, las variables que afectan al código están ocultas y ocultas.</span><span class="sxs-lookup"><span data-stu-id="7a892-150">Sometimes variables that affect your code are hidden and obfuscated.</span></span>  
    
<span data-ttu-id="7a892-151">En resumen, los puntos de interrupción pueden ayudarle a encontrar y corregir errores más rápido que el `console.log()` método.</span><span class="sxs-lookup"><span data-stu-id="7a892-151">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="7a892-152">Si retroces y piensa en cómo funciona la aplicación, puedes hacer una suposición informada de que la suma incorrecta \( \) se calcula en el agente de escucha de eventos asociado con el botón Agregar número 1 y Número `5 + 1 = 51` `click` **2.**</span><span class="sxs-lookup"><span data-stu-id="7a892-152">If you step back and think about how the app works, you may make an educated guess that the incorrect sum \(`5 + 1 = 51`\) is computed in the `click` event listener associated with the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="7a892-153">Por lo tanto, probablemente quieras pausar el código en el momento en que se ejecuta `click` el agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="7a892-153">So, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="7a892-154">**Los puntos de interrupción del agente** de escucha de eventos le permiten hacer exactamente lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7a892-154">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="7a892-155">En el **panel Depuración de JavaScript,** elija Puntos de interrupción de escucha **de eventos** para expandir la sección.</span><span class="sxs-lookup"><span data-stu-id="7a892-155">In the **JavaScript Debugging** pane, choose **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="7a892-156">DevTools muestra una lista de categorías de eventos expandibles, como **animación** y **portapapeles.**</span><span class="sxs-lookup"><span data-stu-id="7a892-156">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="7a892-157">Junto a la **categoría de eventos del mouse,** elija **Expandir** \( Icono ![ Expandir ][ImageExpandIcon] \).</span><span class="sxs-lookup"><span data-stu-id="7a892-157">Next to the **Mouse** event category, choose **Expand** \(![Expand icon][ImageExpandIcon]\).</span></span>  <span data-ttu-id="7a892-158">DevTools muestra una lista de eventos de mouse, **como** hacer clic y pasar **el mouse.**</span><span class="sxs-lookup"><span data-stu-id="7a892-158">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="7a892-159">Cada evento tiene una casilla al lado.</span><span class="sxs-lookup"><span data-stu-id="7a892-159">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="7a892-160">Seleccione la casilla situada junto a **.**</span><span class="sxs-lookup"><span data-stu-id="7a892-160">Choose the checkbox next to **click**.</span></span>  <span data-ttu-id="7a892-161">DevTools ahora está configurado para pausar automáticamente cuando se ejecuta cualquier escucha `click` de eventos.</span><span class="sxs-lookup"><span data-stu-id="7a892-161">DevTools is now set up to automatically pause when any `click` event listener runs.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="Elegir la casilla junto a hacer clic" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       <span data-ttu-id="7a892-163">Seleccione la casilla al lado para **hacer clic**</span><span class="sxs-lookup"><span data-stu-id="7a892-163">Choose the checkbox next to **click**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7a892-164">De nuevo en la demostración, elija **Agregar número 1 y Número 2** de nuevo.</span><span class="sxs-lookup"><span data-stu-id="7a892-164">Back on the demo, choose **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="7a892-165">DevTools pausa la demostración y resalta una línea de código en **el** panel Orígenes.</span><span class="sxs-lookup"><span data-stu-id="7a892-165">DevTools pauses the demo and highlights a line of code in the **Sources** panel.</span></span>  <span data-ttu-id="7a892-166">DevTools debe pausar en la línea 16 in `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="7a892-166">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="7a892-167">Si hace una pausa en una línea de código diferente, presione Reanudar ejecución de **script** \( Reanudar ejecución de script \) hasta que se detenga ![ en la línea ][ImageResumeIcon] correcta.</span><span class="sxs-lookup"><span data-stu-id="7a892-167">If you pause on a different line of code, press **Resume Script Execution** \(![Resume Script Execution][ImageResumeIcon]\) until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="7a892-168">Si ha pausado en una línea diferente, tiene una extensión de explorador que registra un agente de escucha de eventos en todas las páginas `click` web que visite.</span><span class="sxs-lookup"><span data-stu-id="7a892-168">If you paused on a different line, you have a browser extension that registers a `click` event listener on every webpage that you visit.</span></span>  <span data-ttu-id="7a892-169">Se ha pausado en el `click` agente de escucha de la extensión.</span><span class="sxs-lookup"><span data-stu-id="7a892-169">You were paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="7a892-170">Si usas el modo InPrivate para navegar en **privado,** lo que deshabilita todas las extensiones, es posible que veas que pausas en la línea de código deseada cada vez.</span><span class="sxs-lookup"><span data-stu-id="7a892-170">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="7a892-171">**Los puntos de interrupción del agente de** escucha de eventos son solo uno de los muchos tipos de puntos de interrupción disponibles en DevTools.</span><span class="sxs-lookup"><span data-stu-id="7a892-171">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="7a892-172">Memoriza todos los tipos diferentes para ayudarte a depurar diferentes escenarios lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="7a892-172">Memorize all the different types to help you debug different scenarios as quickly as possible.</span></span>  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <span data-ttu-id="7a892-173">Paso 4: Paso a paso por el código</span><span class="sxs-lookup"><span data-stu-id="7a892-173">Step 4: Step through the code</span></span>  

<span data-ttu-id="7a892-174">Una causa común de errores es cuando un script se ejecuta en un orden incorrecto.</span><span class="sxs-lookup"><span data-stu-id="7a892-174">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="7a892-175">El paso a través del código te permite recorrer el tiempo de ejecución del código.</span><span class="sxs-lookup"><span data-stu-id="7a892-175">Stepping through your code allows you to walk through the runtime of your code.</span></span>  <span data-ttu-id="7a892-176">Puede recorrer una línea cada vez para averiguar exactamente dónde se ejecuta el código en un orden diferente del esperado.</span><span class="sxs-lookup"><span data-stu-id="7a892-176">You walk through one line at a time to help you figure out exactly where your code is running in a different order than you expect.</span></span>  <span data-ttu-id="7a892-177">Pruébalo ahora:</span><span class="sxs-lookup"><span data-stu-id="7a892-177">Try it now:</span></span>  

1.  <span data-ttu-id="7a892-178">Choose **Step over next function call** \( Step over next function call ![ ][ImageOverIcon] \).</span><span class="sxs-lookup"><span data-stu-id="7a892-178">Choose **Step over next function call** \(![Step over next function call][ImageOverIcon]\).</span></span>  <span data-ttu-id="7a892-179">DevTools ejecuta el siguiente código sin entrar en él.</span><span class="sxs-lookup"><span data-stu-id="7a892-179">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="7a892-180">DevTools omite algunas líneas de código.</span><span class="sxs-lookup"><span data-stu-id="7a892-180">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="7a892-181">Esto se debe a que se evalúa como false, por lo que no se ejecuta el bloque de código de `inputsAreEmpty()` `if` la instrucción.</span><span class="sxs-lookup"><span data-stu-id="7a892-181">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  
    
1.  <span data-ttu-id="7a892-182">En **el** panel Orígenes de DevTools, elija Paso a paso en la siguiente llamada de función **\(** Paso a siguiente llamada de función \) para pasar por el tiempo de ejecución de la función, una línea ![ cada ][ImageIntoIcon] `updateLabel()` vez.</span><span class="sxs-lookup"><span data-stu-id="7a892-182">On the **Sources** panel of DevTools, choose **Step into next function call** \(![Step into next function call][ImageIntoIcon]\) to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  
    
<span data-ttu-id="7a892-183">Revisar una línea a la vez es la idea básica de pasar por el código.</span><span class="sxs-lookup"><span data-stu-id="7a892-183">Reviewing one line at a time is the basic idea of stepping through code.</span></span>  <span data-ttu-id="7a892-184">Si observa el código en , verá que el error probablemente se encuentra en `get-started.js` algún lugar de la `updateLabel()` función.</span><span class="sxs-lookup"><span data-stu-id="7a892-184">If you look at the code in `get-started.js`, you see that the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="7a892-185">En lugar de pasar por cada línea de código, puede usar otro tipo de punto de interrupción para pausar el código más cerca de la ubicación probable del error.</span><span class="sxs-lookup"><span data-stu-id="7a892-185">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <span data-ttu-id="7a892-186">Paso 5: Establecer un punto de interrupción de línea de código</span><span class="sxs-lookup"><span data-stu-id="7a892-186">Step 5: Set a line-of-code breakpoint</span></span>  

<span data-ttu-id="7a892-187">Los puntos de interrupción de línea de código son el tipo más común de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="7a892-187">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="7a892-188">Cuando llegue a la línea de código específica que desea pausar, use un punto de interrupción de línea de código.</span><span class="sxs-lookup"><span data-stu-id="7a892-188">When you get to the specific line of code you want to pause, use a line-of-code breakpoint.</span></span>  

1.  <span data-ttu-id="7a892-189">Mire la última línea de código `updateLabel()` en:</span><span class="sxs-lookup"><span data-stu-id="7a892-189">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="7a892-190">A la izquierda, el número de esta línea de código en particular se muestra como **34**.</span><span class="sxs-lookup"><span data-stu-id="7a892-190">On the left, the number of this particular line of code is displayed as **34**.</span></span>  <span data-ttu-id="7a892-191">Elija la **línea 34.**</span><span class="sxs-lookup"><span data-stu-id="7a892-191">Choose line **34**.</span></span>  <span data-ttu-id="7a892-192">DevTools coloca un icono rojo a la izquierda de **34**.</span><span class="sxs-lookup"><span data-stu-id="7a892-192">DevTools puts a red icon to the left of **34**.</span></span>  <span data-ttu-id="7a892-193">El icono rojo indica que hay un punto de interrupción de línea de código en esta línea.</span><span class="sxs-lookup"><span data-stu-id="7a892-193">The red icon indicates that a line-of-code breakpoint is on this line.</span></span>  <span data-ttu-id="7a892-194">DevTools siempre hace una pausa antes de ejecutar esta línea de código.</span><span class="sxs-lookup"><span data-stu-id="7a892-194">DevTools always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="7a892-195">Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="7a892-195">Choose **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  <span data-ttu-id="7a892-196">El script continúa ejecutándose hasta que llega a la línea 33.</span><span class="sxs-lookup"><span data-stu-id="7a892-196">The script continues running until it reaches line 33.</span></span>  <span data-ttu-id="7a892-197">En las líneas 31, 32 y 33, DevTools imprime los valores de , y a la derecha del punto y coma `addend1` `addend2` en cada `sum` línea.</span><span class="sxs-lookup"><span data-stu-id="7a892-197">On lines 31, 32, and 33, DevTools prints the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools se pausa en el punto de interrupción de línea de código en la línea 34" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       <span data-ttu-id="7a892-199">DevTools se pausa en el punto de interrupción de línea de código en la línea 34</span><span class="sxs-lookup"><span data-stu-id="7a892-199">DevTools pauses on the line-of-code breakpoint on line 34</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="7a892-200">Paso 6: Comprobar los valores de las variables</span><span class="sxs-lookup"><span data-stu-id="7a892-200">Step 6: Check variable values</span></span>  

<span data-ttu-id="7a892-201">Los valores de `addend1` , `addend2` y parecen `sum` sospechosos.</span><span class="sxs-lookup"><span data-stu-id="7a892-201">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="7a892-202">Los valores se encapsulan entre comillas.</span><span class="sxs-lookup"><span data-stu-id="7a892-202">The values are wrapped in quotes.</span></span>  <span data-ttu-id="7a892-203">Las comillas significan que el valor es una cadena, que es una buena hipótesis para explicar la causa del error.</span><span class="sxs-lookup"><span data-stu-id="7a892-203">The quotations mean that the value is a string, which is a good hypothesis to explain the cause of the bug.</span></span>  <span data-ttu-id="7a892-204">Recopila más información sobre la situación.</span><span class="sxs-lookup"><span data-stu-id="7a892-204">Gather more information about the situation.</span></span>  <span data-ttu-id="7a892-205">DevTools proporciona muchas herramientas para examinar valores de variables.</span><span class="sxs-lookup"><span data-stu-id="7a892-205">DevTools provides many tools for examining variable values.</span></span>  

### <span data-ttu-id="7a892-206">Método 1: el panel Ámbito</span><span class="sxs-lookup"><span data-stu-id="7a892-206">Method 1: The Scope pane</span></span>  

<span data-ttu-id="7a892-207">Si hace una pausa en \*\*\*\* una línea de código, el panel Ámbito muestra las variables locales y globales que están definidas actualmente, junto con el valor de cada variable.</span><span class="sxs-lookup"><span data-stu-id="7a892-207">If you pause on a line of code, the **Scope** pane displays the local and global variables that are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="7a892-208">También muestra variables de cierre, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="7a892-208">It also displays closure variables, as applicable.</span></span>  <span data-ttu-id="7a892-209">Haga doble clic en un valor de variable para editarlo.</span><span class="sxs-lookup"><span data-stu-id="7a892-209">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="7a892-210">Si no pausa una línea de código, el **panel** Ámbito está vacío.</span><span class="sxs-lookup"><span data-stu-id="7a892-210">If you don't pause on a line of code, the **Scope** pane is empty.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="Panel Ámbito" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   <span data-ttu-id="7a892-212">Panel **Ámbito**</span><span class="sxs-lookup"><span data-stu-id="7a892-212">The **Scope** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="7a892-213">Método 2: Expresiones de reloj</span><span class="sxs-lookup"><span data-stu-id="7a892-213">Method 2: Watch Expressions</span></span>  

<span data-ttu-id="7a892-214">El **panel Expresiones de supervisión** permite supervisar los valores de las variables a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="7a892-214">The **Watch Expressions** pane lets you monitor the values of variables over time.</span></span>  <span data-ttu-id="7a892-215">Como su nombre indica, **las expresiones de** watch no están limitadas a variables.</span><span class="sxs-lookup"><span data-stu-id="7a892-215">As the name implies, **Watch Expressions** aren't limited to variables.</span></span>  <span data-ttu-id="7a892-216">Puede almacenar cualquier expresión de JavaScript válida en una **expresión watch**.</span><span class="sxs-lookup"><span data-stu-id="7a892-216">You may store any valid JavaScript expression in a **Watch Expression**.</span></span>  <span data-ttu-id="7a892-217">Pruébalo ahora.</span><span class="sxs-lookup"><span data-stu-id="7a892-217">Try it now.</span></span>  

1.  <span data-ttu-id="7a892-218">Elija el **panel** Ver.</span><span class="sxs-lookup"><span data-stu-id="7a892-218">Choose the **Watch** pane.</span></span>  
1.  <span data-ttu-id="7a892-219">Elija **Agregar expresión** \( Agregar expresión ![ ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="7a892-219">Choose **Add Expression** \(![Add Expression][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="7a892-220">Escribe `typeof sum`.</span><span class="sxs-lookup"><span data-stu-id="7a892-220">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="7a892-221">Seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7a892-221">Select `Enter`.</span></span>  <span data-ttu-id="7a892-222">DevTools muestra `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="7a892-222">DevTools shows `typeof sum: "string"`.</span></span>  <span data-ttu-id="7a892-223">El valor a la derecha de los dos puntos es el resultado de la expresión de reloj.</span><span class="sxs-lookup"><span data-stu-id="7a892-223">The value to the right of the colon is the result of your Watch Expression.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="7a892-224">En el **panel Expresión de** reloj \(abajo a la derecha\) de la siguiente figura, se muestra la expresión de la `typeof sum` vista.</span><span class="sxs-lookup"><span data-stu-id="7a892-224">In the **Watch Expression** pane \(bottom-right\) in the following figure, the `typeof sum` Watch Expression is displayed.</span></span>  <span data-ttu-id="7a892-225">Si la ventana DevTools \*\*\*\* es grande, el panel Expresión de reloj se encuentra a la derecha sobre el panel Puntos de interrupción de escucha **de eventos.**</span><span class="sxs-lookup"><span data-stu-id="7a892-225">If your DevTools window is large, the **Watch Expression** pane is on the right above the **Event Listener Breakpoints** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Panel De expresiones de reloj" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   <span data-ttu-id="7a892-227">Panel **De expresiones de** reloj</span><span class="sxs-lookup"><span data-stu-id="7a892-227">The **Watch Expression** pane</span></span>  
:::image-end:::  

<span data-ttu-id="7a892-228">Como se sospecha, `sum` se está evaluando como una cadena, cuando debe ser un número.</span><span class="sxs-lookup"><span data-stu-id="7a892-228">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="7a892-229">Ahora ha confirmado que el tipo de valor es la causa del error.</span><span class="sxs-lookup"><span data-stu-id="7a892-229">You now confirmed value type is the cause of the bug.</span></span>  

### <span data-ttu-id="7a892-230">Método 3: La consola</span><span class="sxs-lookup"><span data-stu-id="7a892-230">Method 3: The Console</span></span>  

<span data-ttu-id="7a892-231">La **consola** le permite ver mensajes y también puede usarlos para evaluar `console.log()` instrucciones arbitrarias de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7a892-231">The **Console** allows you to view `console.log()` messages and you may also use it to evaluate arbitrary JavaScript statements.</span></span>  <span data-ttu-id="7a892-232">Para la depuración, puede usar la **consola para** probar posibles correcciones de errores.</span><span class="sxs-lookup"><span data-stu-id="7a892-232">For debugging, you may use the **Console** to test potential fixes for bugs.</span></span>  <span data-ttu-id="7a892-233">Pruébalo ahora.</span><span class="sxs-lookup"><span data-stu-id="7a892-233">Try it now.</span></span>  

1.  <span data-ttu-id="7a892-234">Si el **cajón** de la consola está cerrado, `Escape` selecciónelo para abrirlo.</span><span class="sxs-lookup"><span data-stu-id="7a892-234">If the **Console** drawer is closed, select `Escape` to open it.</span></span>  <span data-ttu-id="7a892-235">El **cajón** de la consola se abre en el panel inferior de la ventana DevTools.</span><span class="sxs-lookup"><span data-stu-id="7a892-235">The **Console** drawer opens in the lower panel of the DevTools window.</span></span>  
1.  <span data-ttu-id="7a892-236">En la **consola,** escriba `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="7a892-236">In the **Console**, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="7a892-237">La instrucción que la herramienta se pausa en una línea de código donde `addend1` y están en el `addend2` ámbito.</span><span class="sxs-lookup"><span data-stu-id="7a892-237">The statement the tool is paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="7a892-238">Seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7a892-238">Select `Enter`.</span></span>  <span data-ttu-id="7a892-239">DevTools evalúa la instrucción e imprime, que es el `6` resultado que esperas que produzca la demostración.</span><span class="sxs-lookup"><span data-stu-id="7a892-239">DevTools evaluates the statement and prints `6`, which is the result you expect the demo to produce.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="El cajón de la consola, después de evaluar parseInt(addend1) + parseInt(addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       <span data-ttu-id="7a892-241">El **cajón de** la consola, después de evaluar</span><span class="sxs-lookup"><span data-stu-id="7a892-241">The **Console** drawer, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <span data-ttu-id="7a892-242">Paso 7: Aplicar una corrección</span><span class="sxs-lookup"><span data-stu-id="7a892-242">Step 7: Apply a fix</span></span>  

<span data-ttu-id="7a892-243">Si encuentras una corrección para el error, prueba la corrección editando el código y rerunning la demostración.</span><span class="sxs-lookup"><span data-stu-id="7a892-243">If you find a fix for the bug, try out your fix by editing the code and rerunning the demo.</span></span>  <span data-ttu-id="7a892-244">Puedes editar código JavaScript directamente en la interfaz de usuario de DevTools y aplicar la corrección.</span><span class="sxs-lookup"><span data-stu-id="7a892-244">You may edit JavaScript code directly within the DevTools UI and apply the fix.</span></span>  <span data-ttu-id="7a892-245">Pruébalo ahora.</span><span class="sxs-lookup"><span data-stu-id="7a892-245">Try it now.</span></span>  

1.  <span data-ttu-id="7a892-246">Choose **Resume script execution** \( Resume script execution ![ ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="7a892-246">Choose **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  
1.  <span data-ttu-id="7a892-247">En el **Editor de**código, reemplace la línea 32, , `var sum = addend1 + addend2` por `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="7a892-247">In the **Code Editor**, replace line 32, `var sum = addend1 + addend2`, with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="7a892-248">Seleccione `Control` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\) para guardar el cambio.</span><span class="sxs-lookup"><span data-stu-id="7a892-248">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="7a892-249">Elija **Desactivar puntos de interrupción** \( Desactivar puntos de ![ ][ImageDeactivateIcon] interrupción \).</span><span class="sxs-lookup"><span data-stu-id="7a892-249">Choose **Deactivate breakpoints** \(![Deactivate breakpoints][ImageDeactivateIcon]\).</span></span>  <span data-ttu-id="7a892-250">Cambia de color azul para indicar que la opción está activa.</span><span class="sxs-lookup"><span data-stu-id="7a892-250">It changes blue to indicate the option is active.</span></span>  <span data-ttu-id="7a892-251">Mientras **se establecen los puntos de interrupción** Deactivate, DevTools omite los puntos de interrupción que establezca.</span><span class="sxs-lookup"><span data-stu-id="7a892-251">While **Deactivate breakpoints** is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="7a892-252">Pruebe la demostración con diferentes valores.</span><span class="sxs-lookup"><span data-stu-id="7a892-252">Try out the demo with different values.</span></span>  <span data-ttu-id="7a892-253">La demostración ahora calcula correctamente.</span><span class="sxs-lookup"><span data-stu-id="7a892-253">The demo now calculates correctly.</span></span>  
    
> [!CAUTION]
> <span data-ttu-id="7a892-254">Este flujo de trabajo solo aplica una corrección al código que se ejecuta en el explorador.</span><span class="sxs-lookup"><span data-stu-id="7a892-254">This workflow only applies a fix to the code that is running in your browser.</span></span>  <span data-ttu-id="7a892-255">No corrige el código de todos los usuarios que visitan la página web.</span><span class="sxs-lookup"><span data-stu-id="7a892-255">It does not fix the code for all users that visit your webpage.</span></span>  <span data-ttu-id="7a892-256">Para ello, debe corregir el código que se encuentra en los servidores.</span><span class="sxs-lookup"><span data-stu-id="7a892-256">To do that, you need to fix the code that is on your servers.</span></span>  

## <span data-ttu-id="7a892-257">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="7a892-257">Next steps</span></span>  

<span data-ttu-id="7a892-258">¡Enhorabuena!</span><span class="sxs-lookup"><span data-stu-id="7a892-258">Congratulations!</span></span>  <span data-ttu-id="7a892-259">Ahora ya sabes cómo obtener el máximo partido de Microsoft Edge DevTools al depurar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7a892-259">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="7a892-260">Las herramientas y los métodos que aprendió en este artículo pueden ahorrarle incontables horas.</span><span class="sxs-lookup"><span data-stu-id="7a892-260">The tools and methods you learned in this article may save you countless hours.</span></span>  

<span data-ttu-id="7a892-261">En este artículo solo se le enseñaron dos formas de establecer puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="7a892-261">This article only taught you two ways to set breakpoints.</span></span>  <span data-ttu-id="7a892-262">DevTools ofrece muchas otras formas, incluida la siguiente configuración.</span><span class="sxs-lookup"><span data-stu-id="7a892-262">DevTools offers many other ways including the following settings.</span></span>  

*   <span data-ttu-id="7a892-263">Puntos de interrupción condicionales que solo se desencadenan cuando la condición que se proporciona es verdadera.</span><span class="sxs-lookup"><span data-stu-id="7a892-263">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="7a892-264">Puntos de interrupción en excepciones detectadas o no detectadas.</span><span class="sxs-lookup"><span data-stu-id="7a892-264">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="7a892-265">Puntos de interrupción XHR que se desencadenan cuando la dirección URL solicitada coincide con una subcadena que se proporciona.</span><span class="sxs-lookup"><span data-stu-id="7a892-265">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  
    
<span data-ttu-id="7a892-266">Para obtener más información sobre cuándo y cómo usar cada tipo, vaya a [Pausar el código con puntos de interrupción.][DevtoolsJavscriptBreakpoints]</span><span class="sxs-lookup"><span data-stu-id="7a892-266">For more information about when and how to use each type, navigate to [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].</span></span>  

<span data-ttu-id="7a892-267">En este artículo no se explica un par de controles paso a paso de código.</span><span class="sxs-lookup"><span data-stu-id="7a892-267">A couple of code stepping controls aren't explained in this article.</span></span>  <span data-ttu-id="7a892-268">Para obtener más información, vaya [a Paso a través de la línea de código.][DevtoolsJavascriptReferenceStepThroughCode]</span><span class="sxs-lookup"><span data-stu-id="7a892-268">For more information, navigate to [Step over line of code][DevtoolsJavascriptReferenceStepThroughCode].</span></span>  

## <span data-ttu-id="7a892-269">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7a892-269">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Código paso a paso: referencia de depuración de JavaScript | Microsoft Docs"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Abra el archivo de demostración | Problemas"  

> [!NOTE]
> <span data-ttu-id="7a892-273">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7a892-273">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7a892-274">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& DevTools\).</span><span class="sxs-lookup"><span data-stu-id="7a892-274">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7a892-276">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7a892-276">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

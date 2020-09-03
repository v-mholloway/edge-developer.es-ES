---
description: Obtenga información sobre cómo usar Microsoft Edge DevTools para buscar y corregir errores de JavaScript.
title: Introducción a la depuración de JavaScript en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f8846388f92ba330940b4b6842964d96d9bbce4d
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993397"
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







# <span data-ttu-id="84cfe-104">Introducción a la depuración de JavaScript en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="84cfe-104">Get started with debugging JavaScript in Microsoft Edge DevTools</span></span>   



<span data-ttu-id="84cfe-105">Este tutorial le enseña el flujo de trabajo básico para la depuración de cualquier problema de JavaScript en DevTools.</span><span class="sxs-lookup"><span data-stu-id="84cfe-105">This tutorial teaches you the basic workflow for debugging any JavaScript issue in DevTools.</span></span>  

## <span data-ttu-id="84cfe-106">Paso 1: reproducir el error</span><span class="sxs-lookup"><span data-stu-id="84cfe-106">Step 1: Reproduce the bug</span></span>   

<span data-ttu-id="84cfe-107">Encontrar una serie de acciones que reproduce sistemáticamente un error siempre es el primer paso para la depuración.</span><span class="sxs-lookup"><span data-stu-id="84cfe-107">Finding a series of actions that consistently reproduces a bug is always the first step to debugging.</span></span>  

1.  <span data-ttu-id="84cfe-108">Haga clic en **abrir demo**.</span><span class="sxs-lookup"><span data-stu-id="84cfe-108">Click **Open Demo**.</span></span>  <span data-ttu-id="84cfe-109">Mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y abra la demostración en una pestaña nueva.</span><span class="sxs-lookup"><span data-stu-id="84cfe-109">Hold `Control` \(Windows\) or `Command` \(macOS\) and open the demo in a new tab.</span></span>  
    
    [<span data-ttu-id="84cfe-110">Abrir demo</span><span class="sxs-lookup"><span data-stu-id="84cfe-110">Open Demo</span></span>][OpenDebugJSDemo]  
    
1.  <span data-ttu-id="84cfe-111">Escriba `5` en el cuadro de texto **número 1** .</span><span class="sxs-lookup"><span data-stu-id="84cfe-111">Enter `5` in the **Number 1** text box.</span></span>  
1.  <span data-ttu-id="84cfe-112">Escriba `1` en el cuadro de texto **número 2** .</span><span class="sxs-lookup"><span data-stu-id="84cfe-112">Enter `1` in the **Number 2** text box.</span></span>  
1.  <span data-ttu-id="84cfe-113">Haga clic en **Agregar número 1 y número 2**.</span><span class="sxs-lookup"><span data-stu-id="84cfe-113">Click **Add Number 1 and Number 2**.</span></span>  <span data-ttu-id="84cfe-114">La etiqueta que se encuentra debajo del botón dice `5 + 1 = 51` .</span><span class="sxs-lookup"><span data-stu-id="84cfe-114">The label below the button says `5 + 1 = 51`.</span></span>  <span data-ttu-id="84cfe-115">El resultado debería ser `6` .</span><span class="sxs-lookup"><span data-stu-id="84cfe-115">The result should be `6`.</span></span>  <span data-ttu-id="84cfe-116">Este es el error que va a corregir.</span><span class="sxs-lookup"><span data-stu-id="84cfe-116">This is the bug you are going to fix.</span></span>  
    
    :::image type="complex" source="../media/javascript-js-demo-bad.msft.png" alt-text="El resultado de 5 + 1 es 51, pero debe ser 6" lightbox="../media/javascript-js-demo-bad.msft.png":::
       <span data-ttu-id="84cfe-118">El resultado de `5 + 1` es `51` , pero debe ser</span><span class="sxs-lookup"><span data-stu-id="84cfe-118">The result of `5 + 1` is `51`, but should be</span></span> `6`  
    :::image-end:::  
    
## <span data-ttu-id="84cfe-119">Paso 2: Familiarícese con la interfaz de usuario del panel de orígenes</span><span class="sxs-lookup"><span data-stu-id="84cfe-119">Step 2: Get familiar with the Sources panel UI</span></span>   

<span data-ttu-id="84cfe-120">DevTools proporciona una gran variedad de herramientas para diferentes tareas, como, por ejemplo, el cambio de CSS, la generación de perfiles de rendimiento de carga de páginas y la supervisión de solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="84cfe-120">DevTools provides a lot of different tools for different tasks, such as changing CSS, profiling page load performance, and monitoring network requests.</span></span>  <span data-ttu-id="84cfe-121">El panel **orígenes** es donde se depura JavaScript.</span><span class="sxs-lookup"><span data-stu-id="84cfe-121">The **Sources** panel is where you debug JavaScript.</span></span>  

1.  <span data-ttu-id="84cfe-122">Abra DevTools presionando `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="84cfe-122">Open DevTools by pressing `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) .</span></span>  <span data-ttu-id="84cfe-123">Este método abreviado de teclado abre el panel de **consola** .</span><span class="sxs-lookup"><span data-stu-id="84cfe-123">This shortcut opens the **Console** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-empty.msft.png" alt-text="Panel de consola" lightbox="../media/javascript-console-empty.msft.png":::
       <span data-ttu-id="84cfe-125">Panel de **consola**</span><span class="sxs-lookup"><span data-stu-id="84cfe-125">The **Console** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="84cfe-126">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="84cfe-126">Click the **Sources** tab.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-sections.msft.png" alt-text="Panel orígenes" lightbox="../media/javascript-sources-sections.msft.png":::
       <span data-ttu-id="84cfe-128">Panel **orígenes**</span><span class="sxs-lookup"><span data-stu-id="84cfe-128">The **Sources** panel</span></span>  
    :::image-end:::  
    
<span data-ttu-id="84cfe-129">La interfaz de usuario del panel de **orígenes** tiene 3 partes.</span><span class="sxs-lookup"><span data-stu-id="84cfe-129">The **Sources** panel UI has 3 parts.</span></span>  

:::image type="complex" source="../media/javascript-sources-sections-annotated.msft.png" alt-text="Las 3 partes de la interfaz de usuario del panel de fuentes" lightbox="../media/javascript-sources-sections-annotated.msft.png":::
   <span data-ttu-id="84cfe-131">Las 3 partes de la interfaz de usuario del panel de **fuentes**</span><span class="sxs-lookup"><span data-stu-id="84cfe-131">The 3 parts of the **Sources** panel UI</span></span>  
:::image-end:::  

1.  <span data-ttu-id="84cfe-132">El panel **Explorador de archivos** \ (sección 1 de la figura anterior \).</span><span class="sxs-lookup"><span data-stu-id="84cfe-132">The **File Navigator** pane \(Section 1 in the previous figure\).</span></span>  <span data-ttu-id="84cfe-133">Todos los archivos que solicita la página se muestran aquí.</span><span class="sxs-lookup"><span data-stu-id="84cfe-133">Every file that the page requests is listed here.</span></span>  
1.  <span data-ttu-id="84cfe-134">El panel del **Editor de código** \ (sección 2 de la figura anterior \).</span><span class="sxs-lookup"><span data-stu-id="84cfe-134">The **Code Editor** pane \(Section 2 in the previous figure\).</span></span>  <span data-ttu-id="84cfe-135">Después de seleccionar un archivo en el panel **Explorador de archivos** , el contenido de ese archivo se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="84cfe-135">After selecting a file in the **File Navigator** pane, the contents of that file are displayed here.</span></span>  
1.  <span data-ttu-id="84cfe-136">El panel de **depuración de JavaScript** \ (sección 3 de la figura anterior \).</span><span class="sxs-lookup"><span data-stu-id="84cfe-136">The **JavaScript Debugging** pane \(Section 3 in the previous figure\).</span></span>  <span data-ttu-id="84cfe-137">Varias herramientas para inspeccionar el JavaScript de la página.</span><span class="sxs-lookup"><span data-stu-id="84cfe-137">Various tools for inspecting the JavaScript for the page.</span></span>  <span data-ttu-id="84cfe-138">Si la ventana de DevTools es ancha, este panel se muestra a la derecha del panel del **Editor de código** .</span><span class="sxs-lookup"><span data-stu-id="84cfe-138">If your DevTools window is wide, this pane is displayed to the right of the **Code Editor** pane.</span></span>  
    
## <span data-ttu-id="84cfe-139">Paso 3: pausar el código con un punto de interrupción</span><span class="sxs-lookup"><span data-stu-id="84cfe-139">Step 3: Pause the code with a breakpoint</span></span>   

<span data-ttu-id="84cfe-140">Un método común para depurar un problema como este es insertar muchas instrucciones en `console.log()` el código, para poder inspeccionar valores a medida que se ejecuta el script.</span><span class="sxs-lookup"><span data-stu-id="84cfe-140">A common method for debugging a problem like this is to insert a lot of `console.log()` statements into the code, in order to inspect values as the script runs.</span></span>  <span data-ttu-id="84cfe-141">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="84cfe-141">For example:</span></span>  

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

<span data-ttu-id="84cfe-142">El `console.log()` método puede realizar el trabajo, pero los **puntos de interrupción** pueden hacerlo más rápido.</span><span class="sxs-lookup"><span data-stu-id="84cfe-142">The `console.log()` method may get the job done, but **breakpoints** are able to get it done faster.</span></span>  <span data-ttu-id="84cfe-143">Un punto de interrupción le permite pausar el código en el medio del tiempo de ejecución y examinar todos los valores en ese momento.</span><span class="sxs-lookup"><span data-stu-id="84cfe-143">A breakpoint lets you pause your code in the middle of the runtime, and examine all values at that moment in time.</span></span>  <span data-ttu-id="84cfe-144">Los puntos de interrupción tienen algunas ventajas en comparación con el `console.log()` método:</span><span class="sxs-lookup"><span data-stu-id="84cfe-144">Breakpoints have a few advantages over the `console.log()` method:</span></span>  

*   <span data-ttu-id="84cfe-145">Con `console.log()` , debe abrir manualmente el código fuente, buscar el código correspondiente, insertar las `console.log()` instrucciones y, a continuación, volver a cargar la página para ver los mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="84cfe-145">With `console.log()`, you need to manually open the source code, find the relevant code, insert the `console.log()` statements, and then reload the page in order to see the messages in the Console.</span></span>  <span data-ttu-id="84cfe-146">Con los puntos de interrupción, puedes hacer una pausa en el código relevante sin necesidad de saber cómo se estructura el código.</span><span class="sxs-lookup"><span data-stu-id="84cfe-146">With breakpoints, you may pause on the relevant code without even knowing how the code is structured.</span></span>  
*   <span data-ttu-id="84cfe-147">En las `console.log()` instrucciones debe especificar explícitamente cada valor que desee inspeccionar.</span><span class="sxs-lookup"><span data-stu-id="84cfe-147">In your `console.log()` statements you need to explicitly specify each value that you want to inspect.</span></span>  <span data-ttu-id="84cfe-148">Con los puntos de interrupción, DevTools muestra los valores de todas las variables en ese momento.</span><span class="sxs-lookup"><span data-stu-id="84cfe-148">With breakpoints, DevTools shows you the values of all variables at that moment in time.</span></span>  <span data-ttu-id="84cfe-149">A veces, hay variables que afectan al código que aún no se tiene en cuenta.</span><span class="sxs-lookup"><span data-stu-id="84cfe-149">Sometimes there are variables affecting your code that you are not even aware of.</span></span>  

<span data-ttu-id="84cfe-150">En Resumen, los puntos de interrupción pueden ayudarle a encontrar y corregir errores más rápidamente que el `console.log()` método.</span><span class="sxs-lookup"><span data-stu-id="84cfe-150">In short, breakpoints may help you find and fix bugs faster than the `console.log()` method.</span></span>  

<span data-ttu-id="84cfe-151">Si toma un paso atrás y piensa en cómo funciona la aplicación, puede hacer una conjetura educada de que la suma incorrecta ( `5 + 1 = 51` ) se calcula en el `click` agente de escucha de eventos asociado al botón **Agregar número 1 y número 2** .</span><span class="sxs-lookup"><span data-stu-id="84cfe-151">If you take a step back and think about how the app works, you are able to make an educated guess that the incorrect sum (`5 + 1 = 51`) gets computed in the `click` event listener that is associated to the **Add Number 1 and Number 2** button.</span></span>  <span data-ttu-id="84cfe-152">Por lo tanto, es probable que desee pausar el código en el momento en que `click` se ejecuta el agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="84cfe-152">Therefore, you probably want to pause the code around the time that the `click` listener runs.</span></span>  <span data-ttu-id="84cfe-153">Los **puntos de interrupción de escucha de eventos** te permiten hacer exactamente eso:</span><span class="sxs-lookup"><span data-stu-id="84cfe-153">**Event Listener Breakpoints** let you do exactly that:</span></span>  

1.  <span data-ttu-id="84cfe-154">En el panel de **depuración de JavaScript** , haga clic en **puntos de interrupción de escucha de eventos** para expandir la sección.</span><span class="sxs-lookup"><span data-stu-id="84cfe-154">In the **JavaScript Debugging** pane, click **Event Listener Breakpoints** to expand the section.</span></span>  <span data-ttu-id="84cfe-155">DevTools revela una lista de categorías de eventos expansibles, como la **animación** y el **portapapeles**.</span><span class="sxs-lookup"><span data-stu-id="84cfe-155">DevTools reveals a list of expandable event categories, such as **Animation** and **Clipboard**.</span></span>  
1.  <span data-ttu-id="84cfe-156">Junto a la categoría de evento **del mouse** , haga clic en **expandir** \ ( ![ icono de expandir ][ImageExpandIcon] \).</span><span class="sxs-lookup"><span data-stu-id="84cfe-156">Next to the **Mouse** event category, click **Expand** \(![Expand icon][ImageExpandIcon]\).</span></span>  <span data-ttu-id="84cfe-157">DevTools revela una lista de los eventos del mouse, como **click** y **MouseDown**.</span><span class="sxs-lookup"><span data-stu-id="84cfe-157">DevTools reveals a list of mouse events, such as **click** and **mousedown**.</span></span>  <span data-ttu-id="84cfe-158">Cada evento tiene una casilla al lado.</span><span class="sxs-lookup"><span data-stu-id="84cfe-158">Each event has a checkbox next to it.</span></span>  
1.  <span data-ttu-id="84cfe-159">Active la casilla **click** .</span><span class="sxs-lookup"><span data-stu-id="84cfe-159">Check the **click** checkbox.</span></span>  <span data-ttu-id="84cfe-160">DevTools está configurado para pausarse automáticamente cuando *any* `click` se ejecuta cualquier detector de eventos.</span><span class="sxs-lookup"><span data-stu-id="84cfe-160">DevTools is now set up to automatically pause when *any* `click` event listener runs.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png" alt-text="La casilla click está habilitada" lightbox="../media/javascript-sources-event-listener-breakpoint-mouse-click.msft.png":::
       <span data-ttu-id="84cfe-162">La casilla **click** está habilitada</span><span class="sxs-lookup"><span data-stu-id="84cfe-162">The **click** checkbox is enabled</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="84cfe-163">De nuevo en la demostración, haz clic en **Añadir número 1 y número 2 de** nuevo.</span><span class="sxs-lookup"><span data-stu-id="84cfe-163">Back on the demo, click **Add Number 1 and Number 2** again.</span></span>  <span data-ttu-id="84cfe-164">DevTools en pausa la demostración y resalta una línea de código en el panel **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="84cfe-164">DevTools pauses the demo and highlights a line of code in the **Sources** panel.</span></span>  <span data-ttu-id="84cfe-165">DevTools se debe pausar en la línea 16 `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="84cfe-165">DevTools should pause on line 16 in `get-started.js`.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    <span data-ttu-id="84cfe-166">Si se detiene en una línea de código diferente, presione **reanudar script Execution** \ ( ![ resume script Execution ][ImageResumeIcon] \) hasta que se detenga en la línea correcta.</span><span class="sxs-lookup"><span data-stu-id="84cfe-166">If you pause on a different line of code, press **Resume Script Execution** \(![Resume Script Execution][ImageResumeIcon]\) until you pause on the correct line.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="84cfe-167">Si ha pausado en una línea diferente, tiene una extensión de explorador que registra un `click` detector de eventos en cada página que visite.</span><span class="sxs-lookup"><span data-stu-id="84cfe-167">If you paused on a different line, you have a browser extension that registers a `click` event listener on every page that you visit.</span></span>  <span data-ttu-id="84cfe-168">Se pausó en la `click` escucha de la extensión.</span><span class="sxs-lookup"><span data-stu-id="84cfe-168">You were paused in the `click` listener of the extension.</span></span>  <span data-ttu-id="84cfe-169">Si usa el modo de InPrivate para **explorar en privado**, lo que deshabilita todas las extensiones, es posible que vea que se detiene en la línea de código deseada cada vez.</span><span class="sxs-lookup"><span data-stu-id="84cfe-169">If you use InPrivate Mode to **browse in private**, which disables all extensions, you may see that you pause on the desired line of code every time.</span></span>  

<!--todo: add inprivate section when available -->  

<span data-ttu-id="84cfe-170">Los puntos de interrupción de **escucha de eventos** son solo uno de los muchos tipos de puntos de interrupción disponibles en DevTools.</span><span class="sxs-lookup"><span data-stu-id="84cfe-170">**Event Listener Breakpoints** are just one of many types of breakpoints available in DevTools.</span></span>  <span data-ttu-id="84cfe-171">Merece la pena memorizar todos los tipos diferentes, ya que cada tipo en último término le ayuda a depurar diferentes escenarios lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="84cfe-171">It is worth memorizing all the different types, because each type ultimately helps you debug different scenarios as quickly as possible.</span></span>  <!--See [Pause Your Code With Breakpoints][JSBreakpoints] to learn when and how to use each type.  -->  

## <span data-ttu-id="84cfe-172">Paso 4: recorrer el código</span><span class="sxs-lookup"><span data-stu-id="84cfe-172">Step 4: Step through the code</span></span>   

<span data-ttu-id="84cfe-173">Una causa común de los errores es cuando un script se ejecuta en el orden equivocado.</span><span class="sxs-lookup"><span data-stu-id="84cfe-173">One common cause of bugs is when a script runs in the wrong order.</span></span>  <span data-ttu-id="84cfe-174">Al recorrer el código, podrás recorrer el motor en tiempo de ejecución de tu código, de línea en línea, y averiguar exactamente dónde se está ejecutando en un orden diferente del esperado.</span><span class="sxs-lookup"><span data-stu-id="84cfe-174">Stepping through your code enables you to walk through the runtime of your code, one line at a time, and figure out exactly where it is running in a different order than you expected.</span></span>  <span data-ttu-id="84cfe-175">Pruébelo ahora:</span><span class="sxs-lookup"><span data-stu-id="84cfe-175">Try it now:</span></span>  

1.  <span data-ttu-id="84cfe-176">Haga clic en **paso a paso por la siguiente llamada de función** \ ( ![ paso a paso por la siguiente función llamada ][ImageOverIcon] \).</span><span class="sxs-lookup"><span data-stu-id="84cfe-176">Click **Step over next function call** \(![Step over next function call][ImageOverIcon]\).</span></span>  <span data-ttu-id="84cfe-177">DevTools ejecuta el siguiente código sin entrar en él.</span><span class="sxs-lookup"><span data-stu-id="84cfe-177">DevTools runs the following code without stepping into it.</span></span>  
    
    ```javascript
    if (inputsAreEmpty()) {
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="84cfe-178">DevTools omite unas líneas de código.</span><span class="sxs-lookup"><span data-stu-id="84cfe-178">DevTools skips a few lines of code.</span></span>  <span data-ttu-id="84cfe-179">Esto se debe `inputsAreEmpty()` a que evalúa como falso, por lo que el bloque de código para la instrucción no se `if` ejecuta.</span><span class="sxs-lookup"><span data-stu-id="84cfe-179">This is because `inputsAreEmpty()` evaluates as false, so the block of code for the `if` statement does not run.</span></span>  
    
1.  <span data-ttu-id="84cfe-180">En el panel **orígenes** de DevTools, haga clic en **paso a paso siguiente llamada de función** \ ( ![ ir a la siguiente función llamada ][ImageIntoIcon] \) para recorrer el motor en tiempo de ejecución de la `updateLabel()` función, de línea en línea.</span><span class="sxs-lookup"><span data-stu-id="84cfe-180">On the **Sources** panel of DevTools, click **Step into next function call** \(![Step into next function call][ImageIntoIcon]\) to step through the runtime of the `updateLabel()` function, one line at a time.</span></span>  
    
<span data-ttu-id="84cfe-181">Es la idea básica de recorrer el código.</span><span class="sxs-lookup"><span data-stu-id="84cfe-181">That is the basic idea of stepping through code.</span></span>  <span data-ttu-id="84cfe-182">Si miras el código de `get-started.js` , verás que el error probablemente esté en algún lugar de la `updateLabel()` función.</span><span class="sxs-lookup"><span data-stu-id="84cfe-182">If you look at the code in `get-started.js`, you see that the bug is probably somewhere in the `updateLabel()` function.</span></span>  <span data-ttu-id="84cfe-183">En lugar de ir pasando por todas las líneas de código, puede usar otro tipo de punto de interrupción para pausar el código más cerca de la ubicación probable del error.</span><span class="sxs-lookup"><span data-stu-id="84cfe-183">Rather than stepping through every line of code, you may use another type of breakpoint to pause the code closer to the probable location of the bug.</span></span>  

## <span data-ttu-id="84cfe-184">Paso 5: establecer un punto de interrupción de línea de código</span><span class="sxs-lookup"><span data-stu-id="84cfe-184">Step 5: Set a line-of-code breakpoint</span></span>   

<span data-ttu-id="84cfe-185">Los puntos de interrupción de línea de código son el tipo más común de punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="84cfe-185">Line-of-code breakpoints are the most common type of breakpoint.</span></span>  <span data-ttu-id="84cfe-186">Cuando obtenga la línea de código específica en la que desea hacer una pausa, use un punto de interrupción de línea de código:</span><span class="sxs-lookup"><span data-stu-id="84cfe-186">When you get the specific line of code that you want to pause on, use a line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="84cfe-187">Mire la última línea de código de `updateLabel()` :</span><span class="sxs-lookup"><span data-stu-id="84cfe-187">Look at the last line of code in `updateLabel()`:</span></span>  
    
    ```javascript
    label.textContent = addend1 + ' + ' + addend2 + ' = ' + sum;
    ```  
    
1.  <span data-ttu-id="84cfe-188">A la izquierda del código verás el número de línea de esta línea de código en particular, que es **33**.</span><span class="sxs-lookup"><span data-stu-id="84cfe-188">To the left of the code you see the line number of this particular line of code, which is **33**.</span></span>  <span data-ttu-id="84cfe-189">Haga clic en **33**.</span><span class="sxs-lookup"><span data-stu-id="84cfe-189">Click on **33**.</span></span>  <span data-ttu-id="84cfe-190">DevTools coloca un icono rojo a la izquierda de **33**.</span><span class="sxs-lookup"><span data-stu-id="84cfe-190">DevTools puts a red icon to the left of **33**.</span></span>  <span data-ttu-id="84cfe-191">Esto significa que hay un punto de interrupción de línea de código en esta línea.</span><span class="sxs-lookup"><span data-stu-id="84cfe-191">This means that there is a line-of-code breakpoint on this line.</span></span>  <span data-ttu-id="84cfe-192">DevTools ahora siempre pausa antes de que se ejecute esta línea de código.</span><span class="sxs-lookup"><span data-stu-id="84cfe-192">DevTools now always pauses before this line of code is run.</span></span>  
1.  <span data-ttu-id="84cfe-193">Haga clic en **reanudar script Execution** \ ( ![ resume script Execution ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="84cfe-193">Click **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  <span data-ttu-id="84cfe-194">El script continúa ejecutándose hasta que llega a la línea 33.</span><span class="sxs-lookup"><span data-stu-id="84cfe-194">The script continues running until it reaches line 33.</span></span>  <span data-ttu-id="84cfe-195">En las líneas 30, 31 y 32, DevTools imprime los valores de `addend1` , `addend2` y `sum` a la derecha del punto y coma de cada línea.</span><span class="sxs-lookup"><span data-stu-id="84cfe-195">On lines 30, 31, and 32, DevTools prints out the values of `addend1`, `addend2`, and `sum` to the right of the semi-colon on each line.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused.msft.png" alt-text="DevTools pausa en el punto de interrupción de línea de código en la línea 32" lightbox="../media/javascript-sources-breakpoint-paused.msft.png":::
       <span data-ttu-id="84cfe-197">DevTools pausa en el punto de interrupción de línea de código en la línea 32</span><span class="sxs-lookup"><span data-stu-id="84cfe-197">DevTools pauses on the line-of-code breakpoint on line 32</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="84cfe-198">Paso 6: comprobar los valores de las variables</span><span class="sxs-lookup"><span data-stu-id="84cfe-198">Step 6: Check variable values</span></span>   

<span data-ttu-id="84cfe-199">Los valores de `addend1` , `addend2` y `sum` parecen sospechosos.</span><span class="sxs-lookup"><span data-stu-id="84cfe-199">The values of `addend1`, `addend2`, and `sum` look suspicious.</span></span>  <span data-ttu-id="84cfe-200">Se escriben entre comillas, lo que significa que son cadenas.</span><span class="sxs-lookup"><span data-stu-id="84cfe-200">They are wrapped in quotes, which means that they are strings.</span></span>  <span data-ttu-id="84cfe-201">Esta es una buena hipótesis para explicar la causa del error.</span><span class="sxs-lookup"><span data-stu-id="84cfe-201">This is a good hypothesis for the explaining the cause of the bug.</span></span>  <span data-ttu-id="84cfe-202">Ahora es el momento de recopilar más información.</span><span class="sxs-lookup"><span data-stu-id="84cfe-202">Now it is time to gather more information.</span></span>  <span data-ttu-id="84cfe-203">DevTools proporciona una gran cantidad de herramientas para examinar valores de variables.</span><span class="sxs-lookup"><span data-stu-id="84cfe-203">DevTools provides a lot of tools for examining variable values.</span></span>  

### <span data-ttu-id="84cfe-204">Método 1: el panel ámbito</span><span class="sxs-lookup"><span data-stu-id="84cfe-204">Method 1: The Scope pane</span></span>   

<span data-ttu-id="84cfe-205">Al pausar una línea de código, el panel **ámbito** muestra qué variables locales y globales están definidas actualmente, junto con el valor de cada variable.</span><span class="sxs-lookup"><span data-stu-id="84cfe-205">When you pause on a line of code, the **Scope** pane shows you what local and global variables are currently defined, along with the value of each variable.</span></span>  <span data-ttu-id="84cfe-206">También muestra las variables de cierre, cuando corresponda.</span><span class="sxs-lookup"><span data-stu-id="84cfe-206">It also shows closure variables, when applicable.</span></span>  <span data-ttu-id="84cfe-207">Haga doble clic en un valor de variable para modificarlo.</span><span class="sxs-lookup"><span data-stu-id="84cfe-207">Double-click a variable value to edit it.</span></span>  <span data-ttu-id="84cfe-208">Cuando no se ha pausado en una línea de código, el panel de **ámbito** está vacío.</span><span class="sxs-lookup"><span data-stu-id="84cfe-208">When you are not paused on a line of code, the **Scope** pane is empty.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-scope.msft.png" alt-text="El panel ámbito" lightbox="../media/javascript-sources-breakpoint-paused-scope.msft.png":::
   <span data-ttu-id="84cfe-210">El panel **ámbito**</span><span class="sxs-lookup"><span data-stu-id="84cfe-210">The **Scope** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="84cfe-211">Método 2: ver expresiones</span><span class="sxs-lookup"><span data-stu-id="84cfe-211">Method 2: Watch Expressions</span></span>   

<span data-ttu-id="84cfe-212">La pestaña **inspección de expresiones** le permite supervisar los valores de variables a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="84cfe-212">The **Watch Expressions** tab lets you monitor the values of variables over time.</span></span>  <span data-ttu-id="84cfe-213">Como su nombre implica, las expresiones de inspección no se limitan solo a variables.</span><span class="sxs-lookup"><span data-stu-id="84cfe-213">As the name implies, Watch Expressions are not just limited to variables.</span></span>  <span data-ttu-id="84cfe-214">Puedes almacenar cualquier expresión de JavaScript válida en una expresión de inspección.</span><span class="sxs-lookup"><span data-stu-id="84cfe-214">You are able to store any valid JavaScript expression in a Watch Expression.</span></span>  <span data-ttu-id="84cfe-215">Pruébelo ahora:</span><span class="sxs-lookup"><span data-stu-id="84cfe-215">Try it now:</span></span>  

1.  <span data-ttu-id="84cfe-216">Haga clic en la pestaña **inspección** .</span><span class="sxs-lookup"><span data-stu-id="84cfe-216">Click the **Watch** tab.</span></span>  
1.  <span data-ttu-id="84cfe-217">Haga clic en **Agregar expresión** \ ( ![ Agregar expresión ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="84cfe-217">Click **Add Expression** \(![Add Expression][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="84cfe-218">Escribe `typeof sum`.</span><span class="sxs-lookup"><span data-stu-id="84cfe-218">Type `typeof sum`.</span></span>  
1.  <span data-ttu-id="84cfe-219">Presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="84cfe-219">Press `Enter`.</span></span>  <span data-ttu-id="84cfe-220">DevTools `typeof sum: "string"` .</span><span class="sxs-lookup"><span data-stu-id="84cfe-220">DevTools shows `typeof sum: "string"`.</span></span>  <span data-ttu-id="84cfe-221">El valor a la derecha de los dos puntos es el resultado de la expresión de inspección.</span><span class="sxs-lookup"><span data-stu-id="84cfe-221">The value to the right of the colon is the result of your Watch Expression.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="84cfe-222">En el panel de expresiones de inspección \ (inferior derecha \) en la siguiente ilustración, `typeof sum` se muestra la expresión de inspección.</span><span class="sxs-lookup"><span data-stu-id="84cfe-222">In the Watch Expression pane \(bottom-right\) in in the following figure, the `typeof sum` Watch Expression is displayed.</span></span>  <span data-ttu-id="84cfe-223">Si la ventana de DevTools es grande, el panel de expresiones de inspección se encuentra a la derecha sobre el panel de **puntos de interrupción de escucha de eventos** .</span><span class="sxs-lookup"><span data-stu-id="84cfe-223">If your DevTools window is large, the Watch Expression pane is on the right above the **Event Listener Breakpoints** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-breakpoint-paused-watch.msft.png" alt-text="Panel de expresiones de inspección" lightbox="../media/javascript-sources-breakpoint-paused-watch.msft.png":::
   <span data-ttu-id="84cfe-225">Panel de **expresiones de inspección**</span><span class="sxs-lookup"><span data-stu-id="84cfe-225">The **Watch Expression** pane</span></span>  
:::image-end:::  

<span data-ttu-id="84cfe-226">Como se sospecha, `sum` se evalúa como una cadena, cuando debería ser un número.</span><span class="sxs-lookup"><span data-stu-id="84cfe-226">As suspected, `sum` is being evaluated as a string, when it should be a number.</span></span>  <span data-ttu-id="84cfe-227">Ya ha confirmado que esta es la causa del error.</span><span class="sxs-lookup"><span data-stu-id="84cfe-227">You have now confirmed that this is the cause of the bug.</span></span>  

### <span data-ttu-id="84cfe-228">Método 3: la consola</span><span class="sxs-lookup"><span data-stu-id="84cfe-228">Method 3: The Console</span></span>   

<span data-ttu-id="84cfe-229">Además de ver `console.log()` los mensajes, también puede usar la consola para evaluar instrucciones de JavaScript arbitrarias.</span><span class="sxs-lookup"><span data-stu-id="84cfe-229">In addition to viewing `console.log()` messages, you may also use the Console to evaluate arbitrary JavaScript statements.</span></span>  <span data-ttu-id="84cfe-230">En términos de depuración, puede usar la consola para probar posibles soluciones para errores.</span><span class="sxs-lookup"><span data-stu-id="84cfe-230">In terms of debugging, you may use the Console to test out potential fixes for bugs.</span></span>  <span data-ttu-id="84cfe-231">Pruébelo ahora:</span><span class="sxs-lookup"><span data-stu-id="84cfe-231">Try it now:</span></span>  

1.  <span data-ttu-id="84cfe-232">Si no tiene abierto el cajón de la consola, pulse `Escape` para abrirlo.</span><span class="sxs-lookup"><span data-stu-id="84cfe-232">If you do not have the Console drawer open, press `Escape` to open it.</span></span>  <span data-ttu-id="84cfe-233">Se abre en la parte inferior de la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="84cfe-233">It opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="84cfe-234">En la consola, escriba `parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="84cfe-234">In the Console, type `parseInt(addend1) + parseInt(addend2)`.</span></span>  <span data-ttu-id="84cfe-235">Esta instrucción funciona porque se ha pausado en una línea de código en la que `addend1` `addend2` se encuentran en el ámbito.</span><span class="sxs-lookup"><span data-stu-id="84cfe-235">This statement works because you are paused on a line of code where `addend1` and `addend2` are in scope.</span></span>  
1.  <span data-ttu-id="84cfe-236">Presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="84cfe-236">Press `Enter`.</span></span>  <span data-ttu-id="84cfe-237">DevTools evalúa la instrucción e imprime `6` , que es el resultado que espera que la demostración produzca.</span><span class="sxs-lookup"><span data-stu-id="84cfe-237">DevTools evaluates the statement and prints out `6`, which is the result you expect the demo to produce.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-breakpoint-paused-console.msft.png" alt-text="El cajón de consola, después de evaluar parseInt (addend1) + parseInt (addend2)" lightbox="../media/javascript-sources-breakpoint-paused-console.msft.png":::
       <span data-ttu-id="84cfe-239">El cajón de **consola** , después de la evaluación</span><span class="sxs-lookup"><span data-stu-id="84cfe-239">The **Console** drawer, after evaluating</span></span> `parseInt(addend1) + parseInt(addend2)`  
    :::image-end:::  
    
## <span data-ttu-id="84cfe-240">Paso 7: aplicar una corrección</span><span class="sxs-lookup"><span data-stu-id="84cfe-240">Step 7: Apply a fix</span></span>   

<span data-ttu-id="84cfe-241">Si encuentra una corrección para el error, pruebe su corrección editando el código y volviendo a ejecutar la demostración.</span><span class="sxs-lookup"><span data-stu-id="84cfe-241">If you find a fix for the bug, try out your fix by editing the code and re-running the demo.</span></span>  <span data-ttu-id="84cfe-242">No es necesario dejar DevTools para aplicar la corrección.</span><span class="sxs-lookup"><span data-stu-id="84cfe-242">You do not need to leave DevTools to apply the fix.</span></span>  <span data-ttu-id="84cfe-243">Puedes editar código JavaScript directamente dentro de la interfaz de usuario de DevTools.</span><span class="sxs-lookup"><span data-stu-id="84cfe-243">You are able to edit JavaScript code directly within the DevTools UI.</span></span>  <span data-ttu-id="84cfe-244">Pruébelo ahora:</span><span class="sxs-lookup"><span data-stu-id="84cfe-244">Try it now:</span></span>  

1.  <span data-ttu-id="84cfe-245">Haga clic en **reanudar script Execution** \ ( ![ resume script Execution ][ImageResumeIcon] \).</span><span class="sxs-lookup"><span data-stu-id="84cfe-245">Click **Resume script execution** \(![Resume script execution][ImageResumeIcon]\).</span></span>  
1.  <span data-ttu-id="84cfe-246">En el **Editor de código**, cambie la línea 32, `var sum = addend1 + addend2` con `var sum = parseInt(addend1) + parseInt(addend2)` .</span><span class="sxs-lookup"><span data-stu-id="84cfe-246">In the **Code Editor**, replace line 32, `var sum = addend1 + addend2`, with `var sum = parseInt(addend1) + parseInt(addend2)`.</span></span>  
1.  <span data-ttu-id="84cfe-247">Pulse `Control` + `S` \ (Windows \) o `Command` + `S` \ (MacOS \) para guardar el cambio.</span><span class="sxs-lookup"><span data-stu-id="84cfe-247">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save your change.</span></span>  
1.  <span data-ttu-id="84cfe-248">Haga clic en **desactivar puntos de interrupción** \ ( ![ desactivar puntos de interrupción ][ImageDeactivateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="84cfe-248">Click **Deactivate breakpoints** \(![Deactivate breakpoints][ImageDeactivateIcon]\).</span></span>  <span data-ttu-id="84cfe-249">Cambia de color azul para indicar que está activo.</span><span class="sxs-lookup"><span data-stu-id="84cfe-249">It changes blue to indicate that it is active.</span></span>  <span data-ttu-id="84cfe-250">Aunque está establecido, DevTools omite los puntos de interrupción que haya establecido.</span><span class="sxs-lookup"><span data-stu-id="84cfe-250">While this is set, DevTools ignores any breakpoints you set.</span></span>  
1.  <span data-ttu-id="84cfe-251">Pruebe la demostración con diferentes valores.</span><span class="sxs-lookup"><span data-stu-id="84cfe-251">Try out the demo with different values.</span></span>  <span data-ttu-id="84cfe-252">La demostración ahora se calcula correctamente.</span><span class="sxs-lookup"><span data-stu-id="84cfe-252">The demo now calculates correctly.</span></span>  
    
> [!CAUTION]
> <span data-ttu-id="84cfe-253">Este flujo de trabajo solo aplica una corrección para el código que se ejecuta en el explorador.</span><span class="sxs-lookup"><span data-stu-id="84cfe-253">This workflow only applies a fix to the code that is running in your browser.</span></span>  <span data-ttu-id="84cfe-254">No se corrige el código de todos los usuarios que visitan la página.</span><span class="sxs-lookup"><span data-stu-id="84cfe-254">It does not fix the code for all users that visit your page.</span></span>  <span data-ttu-id="84cfe-255">Para ello, debe corregir el código que está en los servidores.</span><span class="sxs-lookup"><span data-stu-id="84cfe-255">To do that, you need to fix the code that is on your servers.</span></span>  

## <span data-ttu-id="84cfe-256">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="84cfe-256">Next steps</span></span>   

<span data-ttu-id="84cfe-257">¡Enhorabuena!</span><span class="sxs-lookup"><span data-stu-id="84cfe-257">Congratulations!</span></span>  <span data-ttu-id="84cfe-258">Ahora sabes cómo sacar el máximo provecho de Microsoft Edge DevTools al depurar JavaScript.</span><span class="sxs-lookup"><span data-stu-id="84cfe-258">You now know how to make the most of Microsoft Edge DevTools when debugging JavaScript.</span></span>  <span data-ttu-id="84cfe-259">Las herramientas y métodos que aprendió en este tutorial pueden ahorrar innumerables horas.</span><span class="sxs-lookup"><span data-stu-id="84cfe-259">The tools and methods you learned in this tutorial may save you countless hours.</span></span>  

<span data-ttu-id="84cfe-260">En este tutorial, solo se mostraron dos formas de establecer puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="84cfe-260">This tutorial only showed you two ways to set breakpoints.</span></span>  <span data-ttu-id="84cfe-261">DevTools ofrece muchas otras formas, entre las que se incluyen las siguientes.</span><span class="sxs-lookup"><span data-stu-id="84cfe-261">DevTools offers many other ways including the following settings.</span></span>  

*   <span data-ttu-id="84cfe-262">Puntos de interrupción condicionales que solo se desencadenan cuando la condición que proporciona es verdadera.</span><span class="sxs-lookup"><span data-stu-id="84cfe-262">Conditional breakpoints that are only triggered when the condition that you provide is true.</span></span>  
*   <span data-ttu-id="84cfe-263">Puntos de interrupción en excepciones detectadas o no capturadas.</span><span class="sxs-lookup"><span data-stu-id="84cfe-263">Breakpoints on caught or uncaught exceptions.</span></span>  
*   <span data-ttu-id="84cfe-264">XHRlos puntos de interrupción que se desencadenan cuando la dirección URL solicitada coincide con una subcadena que proporciona.</span><span class="sxs-lookup"><span data-stu-id="84cfe-264">XHR breakpoints that are triggered when the requested URL matches a substring that you provide.</span></span>  
    
<span data-ttu-id="84cfe-265">Para obtener más información sobre cuándo y cómo usar cada tipo, vaya a [pausar el código con puntos de interrupción][DevtoolsJavscriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="84cfe-265">For more information about when and how to use each type, go to [Pause Your Code With Breakpoints][DevtoolsJavscriptBreakpoints].</span></span>  

<span data-ttu-id="84cfe-266">Hay un par de controles de versión de paso que no se han explicado en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="84cfe-266">There are a couple of code stepping controls that were not explained in this tutorial.</span></span>  <span data-ttu-id="84cfe-267">Para obtener más información, vaya a [paso a paso por la línea de código][DevtoolsJavascriptReferenceStepThroughCode].</span><span class="sxs-lookup"><span data-stu-id="84cfe-267">For more information, go to [Step over line of code][DevtoolsJavascriptReferenceStepThroughCode].</span></span>  

<!--  
 


-->  

<!-- image links -->  

[ImageAddIcon]: ../media/add-expression-icon.msft.png  
[ImageDeactivateIcon]: ../media/deactivate-breakpoints-button-icon.msft.png  
[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageIntoIcon]: ../media/step-into-icon.msft.png  
[ImageOverIcon]: ../media/step-over-icon.msft.png  
[ImageResumeIcon]: ../media/resume-script-run-icon.msft.png  

<!-- links -->  

[DevtoolsJavscriptBreakpoints]: ./breakpoints.md "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft docs"
[DevtoolsJavascriptReferenceStepThroughCode]: ./reference.md#step-through-code "Paso a paso por el código: referencia de la depuración de JavaScript | Microsoft docs"

<!--[inPrivate]: https://support.alphabet.com/alphabet-browser/answer/95464  -->  

[OpenDebugJSDemo]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Abrir demo | Intento"  

> [!NOTE]
> <span data-ttu-id="84cfe-271">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="84cfe-271">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="84cfe-272">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="84cfe-272">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="84cfe-274">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="84cfe-274">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

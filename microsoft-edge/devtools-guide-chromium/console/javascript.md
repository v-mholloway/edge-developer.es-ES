---
title: Introducción a la ejecución de JavaScript en la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 7e91d9844b2926bc8302331c6b9d971922d27ea3
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982270"
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







# <span data-ttu-id="e3ceb-103">Introducción a la ejecución de JavaScript en la consola</span><span class="sxs-lookup"><span data-stu-id="e3ceb-103">Get Started With Running JavaScript In The Console</span></span>   



<span data-ttu-id="e3ceb-104">Este tutorial interactivo muestra cómo ejecutar JavaScript en la **consola**de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-104">This interactive tutorial shows you how to run JavaScript in the Microsoft Edge DevTools **Console**.</span></span>  <span data-ttu-id="e3ceb-105">Para obtener más información sobre cómo registrar mensajes en la **consola**, consulte Introducción a [los mensajes de registro][DevToolsConsoleLoggingMessages].</span><span class="sxs-lookup"><span data-stu-id="e3ceb-105">For more information about how to log messages to the **Console**, see [Get Started With Logging Messages][DevToolsConsoleLoggingMessages].</span></span>  <span data-ttu-id="e3ceb-106">Para obtener más información sobre cómo pausar código JavaScript y resaltarlo de línea en línea, consulte Introducción a la [depuración de JavaScript][DevToolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="e3ceb-106">For more information about how to pause JavaScript code and step through it one line at a time, see [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="La consola" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   <span data-ttu-id="e3ceb-108">La **consola**</span><span class="sxs-lookup"><span data-stu-id="e3ceb-108">The **Console**</span></span>  
:::image-end:::  

## <span data-ttu-id="e3ceb-109">Introducción</span><span class="sxs-lookup"><span data-stu-id="e3ceb-109">Overview</span></span>   

<span data-ttu-id="e3ceb-110">La **consola** es una [REPL][WikiReadEvalPrintLoop], lo que significa lectura, evaluación, impresión y bucle.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-110">The **Console** is a [REPL][WikiReadEvalPrintLoop], which stands for Read, Evaluate, Print, and Loop.</span></span>  <span data-ttu-id="e3ceb-111">Lee el código JavaScript que escribe en él, evalúa el código, imprime el resultado de la [expresión][2alityExpressionsVersusStatements]y, a continuación, retrocede al primer paso.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-111">It reads the JavaScript that you type into it, evaluates your code, prints out the result of your [expression][2alityExpressionsVersusStatements], and then loops back to the first step.</span></span>  

## <span data-ttu-id="e3ceb-112">Configurar DevTools</span><span class="sxs-lookup"><span data-stu-id="e3ceb-112">Set up DevTools</span></span>   

<span data-ttu-id="e3ceb-113">Este tutorial está diseñado para que abras la demostración y pruebe todos los flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-113">This tutorial is designed for you to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="e3ceb-114">Cuando sigues físicamente, es más probable que recuerdes los flujos de trabajo más adelante.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-114">When you physically follow along, you are more likely to remember the workflows later.</span></span>

1.  <span data-ttu-id="e3ceb-115">Pulse `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \) para abrir la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-115">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console**.</span></span>  
1.  <span data-ttu-id="e3ceb-116">Mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y haga clic en **ejemplo de JavaScript de consola** para abrirlo en una ventana nueva.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-116">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **Console Javascript Example** to open in a new window.</span></span>  
    
    *   [<span data-ttu-id="e3ceb-117">Ejemplo de JavaScript de consola</span><span class="sxs-lookup"><span data-stu-id="e3ceb-117">Console Javascript Example</span></span>][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="La página de ejemplo de JavaScript de la consola de la izquierda y DevTools a la derecha" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       <span data-ttu-id="e3ceb-119">La página de ejemplo de JavaScript de la consola de la izquierda y DevTools a la derecha</span><span class="sxs-lookup"><span data-stu-id="e3ceb-119">The Console JavaScript Example page on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e3ceb-120">Ver y cambiar el JavaScript o el DOM de la página</span><span class="sxs-lookup"><span data-stu-id="e3ceb-120">View and change the JavaScript or DOM of the page</span></span>   

<span data-ttu-id="e3ceb-121">Al crear o depurar una página, a menudo es útil ejecutar instrucciones en la **consola** para cambiar el aspecto o la ejecución de la página.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-121">When building or debugging a page, it is often useful to run statements in the **Console** in order to change how the page looks or runs.</span></span>  
    
1.  <span data-ttu-id="e3ceb-122">Observe el texto en el botón.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-122">Notice the text in the button.</span></span>  
1.  <span data-ttu-id="e3ceb-123">Escriba `document.getElementById('hello').textContent = 'Hello, Console!'` la **consola** y, a continuación, pulse `Enter` para evaluar la expresión.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-123">Type `document.getElementById('hello').textContent = 'Hello, Console!'` in the **Console** and then press `Enter` to evaluate the expression.</span></span>  <span data-ttu-id="e3ceb-124">Observe cómo cambia el texto que se encuentra dentro del botón.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-124">Notice how the text inside the button changes.</span></span>  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Aspecto de la consola después de la evaluación de la expresión" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       <span data-ttu-id="e3ceb-126">Aspecto de la **consola** después de la evaluación de la expresión</span><span class="sxs-lookup"><span data-stu-id="e3ceb-126">How the **Console** looks after evaluating the expression</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="e3ceb-127">Debajo del código que hayas evaluado verás `"Hello, Console!"` .</span><span class="sxs-lookup"><span data-stu-id="e3ceb-127">Below the code that you evaluated you see `"Hello, Console!"`.</span></span>  <span data-ttu-id="e3ceb-128">Recupere los cuatro pasos de REPL: leer, evaluar, imprimir, repetir.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-128">Recall the 4 steps of REPL: read, evaluate, print, loop.</span></span>  <span data-ttu-id="e3ceb-129">Después de evaluar el código, una REPL imprime el resultado de la expresión.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-129">After evaluating your code, a REPL prints the result of the expression.</span></span>  <span data-ttu-id="e3ceb-130">Por lo tanto, `"Hello, Console!"` debe ser el resultado de la evaluación `document.getElementById('hello').textContent = 'Hello, Console!'` .</span><span class="sxs-lookup"><span data-stu-id="e3ceb-130">So `"Hello, Console!"` must be the result of evaluating `document.getElementById('hello').textContent = 'Hello, Console!'`.</span></span>  
    
## <span data-ttu-id="e3ceb-131">Ejecutar JavaScript arbitrario que no está relacionado con la página</span><span class="sxs-lookup"><span data-stu-id="e3ceb-131">Run arbitrary JavaScript that is not related to the page</span></span>   

<span data-ttu-id="e3ceb-132">A veces, solo deseas un código de animación donde puedas probar algún código o probar nuevas características de JavaScript con las que no estás familiarizado.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-132">Sometimes, you just want a code playground where you are able to test some code, or try out new JavaScript features you are not familiar with.</span></span>  <span data-ttu-id="e3ceb-133">La consola es un lugar ideal para estos tipos de experimentos.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-133">The Console is a perfect place for these kinds of experiments.</span></span>  

1.  <span data-ttu-id="e3ceb-134">Escriba `5 + 15` la consola y pulse `Enter` para evaluar la expresión.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-134">Type `5 + 15` in the Console and press `Enter` to evaluate the expression.</span></span> <span data-ttu-id="e3ceb-135">La consola imprime el resultado de la expresión que está debajo del código.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-135">The Console prints out the result of the expression below your code.</span></span>  <span data-ttu-id="e3ceb-136">En la siguiente ilustración, la **consola** debería mostrar el resultado después de evaluar la expresión.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-136">In the following figure, your **Console** should display the result after evaluating the expression.</span></span>  

1.  <span data-ttu-id="e3ceb-137">Escriba el código siguiente en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-137">Type the following code into the **Console**.</span></span>  <span data-ttu-id="e3ceb-138">Pruebe a escribirla, carácter a carácter, en lugar de pegarla.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-138">Try typing it out, character-by-character, rather than copy-pasting it.</span></span>  
    
    ```javascript
    function add(a, b=20) { return a + b; }
    ```  
    
    <span data-ttu-id="e3ceb-139">Si no está familiarizado con la `b=20` sintaxis, consulte [definir valores predeterminados para los argumentos de una función][Esma6DefaultParameterValues].</span><span class="sxs-lookup"><span data-stu-id="e3ceb-139">If you are unfamiliar with the `b=20` syntax, see [define default values for function arguments][Esma6DefaultParameterValues].</span></span>  
    
1.  <span data-ttu-id="e3ceb-140">Ahora, ejecute la función que acaba de definir.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-140">Now, run the function that you just defined.</span></span>  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="La consola se muestra después de evaluar las expresiones en el fragmento de código." lightbox="../media/console-javascript-example-console-playground.msft.png":::
             <span data-ttu-id="e3ceb-142">La **consola** se muestra después de evaluar las expresiones en el fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-142">The **Console** displays after evaluating the expressions in the code snippet</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` <span data-ttu-id="e3ceb-143">se evalúa como `45` porque cuando `add` se llama a la función sin un segundo argumento, el `b` valor predeterminado es `20` .</span><span class="sxs-lookup"><span data-stu-id="e3ceb-143">evaluates to `45` because when the `add` function is called without a second argument, `b` defaults to `20`.</span></span>  

## <span data-ttu-id="e3ceb-144">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="e3ceb-144">Next steps</span></span>   

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

<span data-ttu-id="e3ceb-145">DevTools le permite pausar un script en mitad de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-145">DevTools lets you pause a script in the middle of running.</span></span>  <span data-ttu-id="e3ceb-146">Mientras está pausado, puede usar la **consola** para ver y cambiar la `window` o `DOM` de la página en ese momento.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-146">While you are paused, you may use the **Console** to view and change the `window` or `DOM` of the page at that moment in time.</span></span>  <span data-ttu-id="e3ceb-147">El flujo de trabajo hace que el flujo de trabajo de depuración sea eficaz.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-147">The workflow makes for a powerful debugging workflow.</span></span>  <span data-ttu-id="e3ceb-148">Para obtener un tutorial interactivo, consulte [Introducción a la depuración de JavaScript][DevToolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="e3ceb-148">For an interactive tutorial, see [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

<span data-ttu-id="e3ceb-149">La **consola** también tiene un conjunto de funciones de comodidad que hacen que sea más fácil interactuar con una página.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-149">The **Console** also has a set of convenience functions that make it easier to interact with a page.</span></span>  <span data-ttu-id="e3ceb-150">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e3ceb-150">For example:</span></span>  

*   <span data-ttu-id="e3ceb-151">En lugar de escribir `document.querySelector()` para seleccionar un elemento, escriba `$()` .</span><span class="sxs-lookup"><span data-stu-id="e3ceb-151">Rather than typing `document.querySelector()` to select an element, type `$()`.</span></span>  <span data-ttu-id="e3ceb-152">Esta sintaxis está inspirada en jQuery, pero en realidad no es jQuery.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-152">This syntax is inspired by jQuery, but it is not actually jQuery.</span></span>  <span data-ttu-id="e3ceb-153">Es solo un alias para `document.querySelector()` .</span><span class="sxs-lookup"><span data-stu-id="e3ceb-153">It is just an alias for `document.querySelector()`.</span></span>  
*   `debug(function)` <span data-ttu-id="e3ceb-154">establece de forma eficaz un punto de interrupción en la primera línea de esa función.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-154">effectively sets a breakpoint on the first line of that function.</span></span>  
*   `keys(object)` <span data-ttu-id="e3ceb-155">Devuelve una matriz que contiene las claves del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="e3ceb-155">returns an array containing the keys of the specified object.</span></span>  

<!--See [Console Utilities API Reference][DevToolsConsoleUtilities] to explore all the convenience functions.  -->  

<!--todo: add console utilities api reference section when available  -->  

 



<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Introducción a la creación de mensajes de registro en la consola | Microsoft docs"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Referencia de consola | Microsoft docs"  
[DevToolsConsoleUtilities]: ./utilities.md "Referencia de API de utilidades de consola | Microsoft docs"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Expresiones frente a instrucciones en JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Valores de parámetro predeterminados: administración de parámetros ampliada-ECMAScript 6 — características nuevas: información general & la comparación"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Ejemplo de JavaScript de la consola | Intento"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Lectura: eval – imprimir bucle-Wikipedia"  

> [!NOTE]
> <span data-ttu-id="e3ceb-164">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e3ceb-164">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e3ceb-165">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/javascript) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e3ceb-165">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/javascript) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e3ceb-167">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e3ceb-167">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

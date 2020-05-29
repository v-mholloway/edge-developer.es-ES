---
title: Introducción a la ejecución de JavaScript en la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 724d0e3c7c8439551538383e68a5fc4465eade94
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601729"
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







# <span data-ttu-id="9b443-103">Introducción a la ejecución de JavaScript en la consola</span><span class="sxs-lookup"><span data-stu-id="9b443-103">Get Started With Running JavaScript In The Console</span></span>   



<span data-ttu-id="9b443-104">Este tutorial interactivo muestra cómo ejecutar JavaScript en la consola de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="9b443-104">This interactive tutorial shows you how to run JavaScript in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="9b443-105">Consulte Introducción al [registro de mensajes][DevToolsConsoleLoggingMessages] para obtener información sobre cómo registrar mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="9b443-105">See [Get Started With Logging Messages][DevToolsConsoleLoggingMessages] to learn how to log messages to the Console.</span></span>  <span data-ttu-id="9b443-106">Consulta Introducción a la [depuración de JavaScript][DevToolsJavascriptIndex] para obtener información sobre cómo pausar el código de JavaScript y resaltarlo de línea en línea.</span><span class="sxs-lookup"><span data-stu-id="9b443-106">See [Get Started With Debugging JavaScript][DevToolsJavascriptIndex] to learn how to pause JavaScript code and step through it one line at a time.</span></span>  

> ##### <span data-ttu-id="9b443-107">Figura 1</span><span class="sxs-lookup"><span data-stu-id="9b443-107">Figure 1</span></span>  
> <span data-ttu-id="9b443-108">La **consola**</span><span class="sxs-lookup"><span data-stu-id="9b443-108">The **Console**</span></span>  
> ![La consola][ImageConsole]  

## <span data-ttu-id="9b443-110">Introducción</span><span class="sxs-lookup"><span data-stu-id="9b443-110">Overview</span></span>   

<span data-ttu-id="9b443-111">La **consola** es una [REPL][WikiReadEvalPrintLoop], lo que significa lectura, evaluación, impresión y bucle.</span><span class="sxs-lookup"><span data-stu-id="9b443-111">The **Console** is a [REPL][WikiReadEvalPrintLoop], which stands for Read, Evaluate, Print, and Loop.</span></span>  <span data-ttu-id="9b443-112">Lee el código JavaScript que escribe en él, evalúa el código, imprime el resultado de la [expresión][2alityExpressionsVersusStatements]y, a continuación, retrocede al primer paso.</span><span class="sxs-lookup"><span data-stu-id="9b443-112">It reads the JavaScript that you type into it, evaluates your code, prints out the result of your [expression][2alityExpressionsVersusStatements], and then loops back to the first step.</span></span>  

## <span data-ttu-id="9b443-113">Configurar DevTools</span><span class="sxs-lookup"><span data-stu-id="9b443-113">Set up DevTools</span></span>   

<span data-ttu-id="9b443-114">Este tutorial está diseñado para que abras la demostración y pruebe todos los flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9b443-114">This tutorial is designed for you to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="9b443-115">Cuando sigues físicamente, es más probable que recuerdes los flujos de trabajo más adelante.</span><span class="sxs-lookup"><span data-stu-id="9b443-115">When you physically follow along, you are more likely to remember the workflows later.</span></span>

1.  <span data-ttu-id="9b443-116">Pulse `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \) para abrir la **consola**.</span><span class="sxs-lookup"><span data-stu-id="9b443-116">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console**.</span></span>  
1.  <span data-ttu-id="9b443-117">Mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y haga clic en **ejemplo de JavaScript de consola** para abrirlo en una ventana nueva.</span><span class="sxs-lookup"><span data-stu-id="9b443-117">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **Console Javascript Example** to open in a new window.</span></span>  
    
    [<span data-ttu-id="9b443-118">Ejemplo de JavaScript de consola</span><span class="sxs-lookup"><span data-stu-id="9b443-118">Console Javascript Example</span></span>][GlitchConsoleJavascriptExample]  
    
    > ##### <span data-ttu-id="9b443-119">Figura 2</span><span class="sxs-lookup"><span data-stu-id="9b443-119">Figure 2</span></span>  
    > <span data-ttu-id="9b443-120">La página de ejemplo de JavaScript de la consola de la izquierda y DevTools a la derecha</span><span class="sxs-lookup"><span data-stu-id="9b443-120">The Console JavaScript Example page on the left, and DevTools on the right</span></span>  
    > ![La página de ejemplo de JavaScript de la consola de la izquierda y DevTools a la derecha][ImageTutorialDevToolsJs]  

## <span data-ttu-id="9b443-122">Ver y cambiar el JavaScript o el DOM de la página</span><span class="sxs-lookup"><span data-stu-id="9b443-122">View and change the JavaScript or DOM of the page</span></span>   

<span data-ttu-id="9b443-123">Al crear o depurar una página, a menudo es útil ejecutar instrucciones en la **consola** para cambiar el aspecto o la ejecución de la página.</span><span class="sxs-lookup"><span data-stu-id="9b443-123">When building or debugging a page, it is often useful to run statements in the **Console** in order to change how the page looks or runs.</span></span>  
    
1.  <span data-ttu-id="9b443-124">Observe el texto en el botón.</span><span class="sxs-lookup"><span data-stu-id="9b443-124">Notice the text in the button.</span></span>  
1.  <span data-ttu-id="9b443-125">Escriba `document.getElementById('hello').textContent = 'Hello, Console!'` la **consola** y, a continuación, pulse `Enter` para evaluar la expresión.</span><span class="sxs-lookup"><span data-stu-id="9b443-125">Type `document.getElementById('hello').textContent = 'Hello, Console!'` in the **Console** and then press `Enter` to evaluate the expression.</span></span>  <span data-ttu-id="9b443-126">Observe cómo cambia el texto que se encuentra dentro del botón.</span><span class="sxs-lookup"><span data-stu-id="9b443-126">Notice how the text inside the button changes.</span></span>  
    
    > ##### <span data-ttu-id="9b443-127">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="9b443-127">Figure 3</span></span>  
    > <span data-ttu-id="9b443-128">Aspecto de la consola después de la evaluación de la expresión</span><span class="sxs-lookup"><span data-stu-id="9b443-128">How the Console looks after evaluating the expression</span></span>  
    > ![Aspecto de la consola después de la evaluación de la expresión][ImageConsoleAfterEvaluating]  
    
    <span data-ttu-id="9b443-130">Debajo del código que hayas evaluado verás `"Hello, Console!"` .</span><span class="sxs-lookup"><span data-stu-id="9b443-130">Below the code that you evaluated you see `"Hello, Console!"`.</span></span>  <span data-ttu-id="9b443-131">Recupere los cuatro pasos de REPL: leer, evaluar, imprimir, repetir.</span><span class="sxs-lookup"><span data-stu-id="9b443-131">Recall the 4 steps of REPL: read, evaluate, print, loop.</span></span>  <span data-ttu-id="9b443-132">Después de evaluar el código, una REPL imprime el resultado de la expresión.</span><span class="sxs-lookup"><span data-stu-id="9b443-132">After evaluating your code, a REPL prints the result of the expression.</span></span>  <span data-ttu-id="9b443-133">Por lo tanto, `"Hello, Console!"` debe ser el resultado de la evaluación `document.getElementById('hello').textContent = 'Hello, Console!'` .</span><span class="sxs-lookup"><span data-stu-id="9b443-133">So `"Hello, Console!"` must be the result of evaluating `document.getElementById('hello').textContent = 'Hello, Console!'`.</span></span>  
    
## <span data-ttu-id="9b443-134">Ejecutar JavaScript arbitrario que no está relacionado con la página</span><span class="sxs-lookup"><span data-stu-id="9b443-134">Run arbitrary JavaScript that is not related to the page</span></span>   

<span data-ttu-id="9b443-135">A veces, solo deseas un código de animación donde puedas probar algún código o probar nuevas características de JavaScript con las que no estás familiarizado.</span><span class="sxs-lookup"><span data-stu-id="9b443-135">Sometimes, you just want a code playground where you are able to test some code, or try out new JavaScript features you are not familiar with.</span></span>  <span data-ttu-id="9b443-136">La consola es un lugar ideal para estos tipos de experimentos.</span><span class="sxs-lookup"><span data-stu-id="9b443-136">The Console is a perfect place for these kinds of experiments.</span></span>  

1.  <span data-ttu-id="9b443-137">Escriba `5 + 15` la consola y pulse `Enter` para evaluar la expresión.</span><span class="sxs-lookup"><span data-stu-id="9b443-137">Type `5 + 15` in the Console and press `Enter` to evaluate the expression.</span></span> <span data-ttu-id="9b443-138">La consola imprime el resultado de la expresión que está debajo del código.</span><span class="sxs-lookup"><span data-stu-id="9b443-138">The Console prints out the result of the expression below your code.</span></span>  <span data-ttu-id="9b443-139">La **figura 4** a continuación muestra el aspecto que tendrá la consola después de evaluar esta expresión.</span><span class="sxs-lookup"><span data-stu-id="9b443-139">**Figure 4** below shows how your Console should look after evaluating this expression.</span></span>  

1.  <span data-ttu-id="9b443-140">Escriba el código siguiente en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="9b443-140">Type the following code into the **Console**.</span></span>  <span data-ttu-id="9b443-141">Pruebe a escribirla, carácter a carácter, en lugar de pegarla.</span><span class="sxs-lookup"><span data-stu-id="9b443-141">Try typing it out, character-by-character, rather than copy-pasting it.</span></span>  
    
    ```javascript
    function add(a, b=20) {
        return a + b;
    }
    ```  
    
    <span data-ttu-id="9b443-142">Vea [definir valores predeterminados para argumentos de función][Esma6DefaultParameterValues] si no está familiarizado con la `b=20` Sintaxis.</span><span class="sxs-lookup"><span data-stu-id="9b443-142">See [define default values for function arguments][Esma6DefaultParameterValues] if you are unfamiliar with the `b=20` syntax.</span></span>  
    
1.  <span data-ttu-id="9b443-143">Ahora, llama a la función que acabas de definir.</span><span class="sxs-lookup"><span data-stu-id="9b443-143">Now, call the function that you just defined.</span></span>  
    
    ```javascript
    add(25);
    ```  
    
    > ##### <span data-ttu-id="9b443-144">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="9b443-144">Figure 4</span></span>  
    > <span data-ttu-id="9b443-145">Aspecto de la consola después de la evaluación de las expresiones anteriores</span><span class="sxs-lookup"><span data-stu-id="9b443-145">How the Console looks after evaluating the expressions above</span></span>  
    > ![Aspecto de la consola después de la evaluación de las expresiones anteriores][ImagePlayground]  
    
    `add(25)` <span data-ttu-id="9b443-147">se evalúa como `45` porque cuando `add` se llama a la función sin un segundo argumento, el `b` valor predeterminado es `20` .</span><span class="sxs-lookup"><span data-stu-id="9b443-147">evaluates to `45` because when the `add` function is called without a second argument, `b` defaults to `20`.</span></span>  

## <span data-ttu-id="9b443-148">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="9b443-148">Next steps</span></span>   

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

<span data-ttu-id="9b443-149">DevTools le permite pausar un script en mitad de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="9b443-149">DevTools lets you pause a script in the middle of running.</span></span>  <span data-ttu-id="9b443-150">Mientras está pausado, puede usar la **consola** para ver y cambiar la `window` o `DOM` de la página en ese momento.</span><span class="sxs-lookup"><span data-stu-id="9b443-150">While you are paused, you may use the **Console** to view and change the `window` or `DOM` of the page at that moment in time.</span></span>  <span data-ttu-id="9b443-151">Esto hace que el flujo de trabajo de depuración sea eficaz.</span><span class="sxs-lookup"><span data-stu-id="9b443-151">This makes for a powerful debugging workflow.</span></span>  <span data-ttu-id="9b443-152">Consulta Introducción [a la depuración de JavaScript][DevToolsJavascriptIndex] para un tutorial interactivo.</span><span class="sxs-lookup"><span data-stu-id="9b443-152">See [Get Started With Debugging JavaScript][DevToolsJavascriptIndex] for an interactive tutorial.</span></span>  

<span data-ttu-id="9b443-153">La **consola** también tiene un conjunto de funciones de comodidad que hacen que sea más fácil interactuar con una página.</span><span class="sxs-lookup"><span data-stu-id="9b443-153">The **Console** also has a set of convenience functions that make it easier to interact with a page.</span></span>  <span data-ttu-id="9b443-154">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9b443-154">For example:</span></span>  

*   <span data-ttu-id="9b443-155">En lugar de escribir `document.querySelector()` para seleccionar un elemento, escriba `$()` .</span><span class="sxs-lookup"><span data-stu-id="9b443-155">Rather than typing `document.querySelector()` to select an element, type `$()`.</span></span>  <span data-ttu-id="9b443-156">Esta sintaxis está inspirada en jQuery, pero en realidad no es jQuery.</span><span class="sxs-lookup"><span data-stu-id="9b443-156">This syntax is inspired by jQuery, but it is not actually jQuery.</span></span>  <span data-ttu-id="9b443-157">Es solo un alias para `document.querySelector()` .</span><span class="sxs-lookup"><span data-stu-id="9b443-157">It is just an alias for `document.querySelector()`.</span></span>  
*   `debug(function)` <span data-ttu-id="9b443-158">establece de forma eficaz un punto de interrupción en la primera línea de esa función.</span><span class="sxs-lookup"><span data-stu-id="9b443-158">effectively sets a breakpoint on the first line of that function.</span></span>  
*   `keys(object)` <span data-ttu-id="9b443-159">Devuelve una matriz que contiene las claves del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="9b443-159">returns an array containing the keys of the specified object.</span></span>  

<!--See [Console Utilities API Reference][DevToolsConsoleUtilities] to explore all the convenience functions.  -->  

<!--todo: add console utilities api reference section when available  -->  

 



<!-- image links -->  

[ImageConsole]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-playground.msft.png "Ilustración 1: la consola"  
[ImageTutorialDevToolsJs]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-empty.msft.png "Ilustración 2: la página de ejemplo de JavaScript de la consola de la izquierda y DevTools a la derecha"  
[ImageConsoleAfterEvaluating]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-change-button-text.msft.png "Ilustración 3: el aspecto de la consola después de la evaluación de la expresión"  
[ImagePlayground]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-playground.msft.png "Ilustración 4: el aspecto de la consola después de evaluar las expresiones anteriores"  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: /microsoft-edge/devtools-guide-chromium/console/log "Introducción al registro de mensajes en la consola"  
[DevToolsConsoleReference]: /microsoft-edge/devtools-guide-chromium/console/reference#run-javascript "Referencia de consola"  
[DevToolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium//console/utilities "Referencia de API de utilidades de consola"  

[DevToolsJavascriptIndex]: /microsoft-edge/devtools-guide-chromium/javascript/index "Introducción a la depuración de JavaScript en Microsoft Edge DevTools"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Expresiones frente a instrucciones en JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Valores de parámetro predeterminados: administración de parámetros ampliada-ECMAScript 6 — características nuevas: información general & la comparación"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Ejemplo de JavaScript de la consola | Intento"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Lectura: eval – imprimir bucle-Wikipedia"  

> [!NOTE]
> <span data-ttu-id="9b443-172">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9b443-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9b443-173">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/javascript) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="9b443-173">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/javascript) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9b443-175">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9b443-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

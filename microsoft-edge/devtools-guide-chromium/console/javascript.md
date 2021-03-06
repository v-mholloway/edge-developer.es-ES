---
description: Obtenga información sobre cómo ejecutar JavaScript en la consola.
title: Introducción a la ejecución de JavaScript en la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: c1d6c393b6278f4622cf80576ccc8f9c70bdb6b5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398822"
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

# <a name="get-started-with-running-javascript-in-the-console"></a><span data-ttu-id="52e8e-104">Introducción a la ejecución de JavaScript en la consola</span><span class="sxs-lookup"><span data-stu-id="52e8e-104">Get started with running JavaScript in the Console</span></span>  

<span data-ttu-id="52e8e-105">En este tutorial interactivo se muestra cómo ejecutar JavaScript en la consola de Microsoft Edge **DevTools**.</span><span class="sxs-lookup"><span data-stu-id="52e8e-105">This interactive tutorial shows you how to run JavaScript in the Microsoft Edge DevTools **Console**.</span></span>  <span data-ttu-id="52e8e-106">Para obtener más información acerca de cómo registrar mensajes en la **consola,** vaya a [Introducción al registro de mensajes][DevToolsConsoleLoggingMessages].</span><span class="sxs-lookup"><span data-stu-id="52e8e-106">For more information about how to log messages to the **Console**, navigate to [Get Started With Logging Messages][DevToolsConsoleLoggingMessages].</span></span>  <span data-ttu-id="52e8e-107">Para obtener más información acerca de cómo pausar código JavaScript y recorrerlo de una línea a la vez, vaya a Introducción a [La depuración de JavaScript][DevToolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="52e8e-107">For more information about how to pause JavaScript code and step through it one line at a time, navigate to [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="La consola" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   <span data-ttu-id="52e8e-109">La **consola**</span><span class="sxs-lookup"><span data-stu-id="52e8e-109">The **Console**</span></span>  
:::image-end:::  

## <a name="overview"></a><span data-ttu-id="52e8e-110">Introducción</span><span class="sxs-lookup"><span data-stu-id="52e8e-110">Overview</span></span>  

<span data-ttu-id="52e8e-111">La **consola** es [una REPL][WikiReadEvalPrintLoop], que significa Leer, Evaluar, Imprimir y Bucle.</span><span class="sxs-lookup"><span data-stu-id="52e8e-111">The **Console** is a [REPL][WikiReadEvalPrintLoop], which stands for Read, Evaluate, Print, and Loop.</span></span>  <span data-ttu-id="52e8e-112">Lee el JavaScript que escribe en él, evalúa el código, imprime [][2alityExpressionsVersusStatements]el resultado de la expresión y, a continuación, vuelve al primer paso.</span><span class="sxs-lookup"><span data-stu-id="52e8e-112">It reads the JavaScript that you type into it, evaluates your code, prints out the result of your [expression][2alityExpressionsVersusStatements], and then loops back to the first step.</span></span>  

## <a name="set-up-devtools"></a><span data-ttu-id="52e8e-113">Configurar DevTools</span><span class="sxs-lookup"><span data-stu-id="52e8e-113">Set up DevTools</span></span>  

<span data-ttu-id="52e8e-114">Este tutorial está diseñado para que abra la demostración y pruebe todos los flujos de trabajo usted mismo.</span><span class="sxs-lookup"><span data-stu-id="52e8e-114">This tutorial is designed for you to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="52e8e-115">Cuando se sigue físicamente, es más probable que recuerde los flujos de trabajo más adelante.</span><span class="sxs-lookup"><span data-stu-id="52e8e-115">When you physically follow along, you are more likely to remember the workflows later.</span></span>

1.  <span data-ttu-id="52e8e-116">Seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\) para abrir la **consola**.</span><span class="sxs-lookup"><span data-stu-id="52e8e-116">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open the **Console**.</span></span>  
1.  <span data-ttu-id="52e8e-117">Mantenga `Control` presionado \(Windows, Linux\) o `Command` \(macOS\) y elija Ejemplo **de Javascript** de consola para abrir en una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="52e8e-117">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Javascript Example** to open in a new window.</span></span>  
    
    *   [<span data-ttu-id="52e8e-118">Ejemplo de Javascript de consola</span><span class="sxs-lookup"><span data-stu-id="52e8e-118">Console Javascript Example</span></span>][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="Página ejemplo de JavaScript de consola a la izquierda y DevTools a la derecha" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       <span data-ttu-id="52e8e-120">Página ejemplo de JavaScript de consola a la izquierda y DevTools a la derecha</span><span class="sxs-lookup"><span data-stu-id="52e8e-120">The Console JavaScript Example page on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
## <a name="view-and-change-the-javascript-or-dom-of-the-page"></a><span data-ttu-id="52e8e-121">Ver y cambiar javascript o DOM de la página</span><span class="sxs-lookup"><span data-stu-id="52e8e-121">View and change the JavaScript or DOM of the page</span></span>  

<span data-ttu-id="52e8e-122">Al compilar o depurar una página, a menudo resulta \*\*\*\* útil ejecutar instrucciones en la consola para cambiar el aspecto o la ejecución de la página.</span><span class="sxs-lookup"><span data-stu-id="52e8e-122">When building or debugging a page, it is often useful to run statements in the **Console** in order to change how the page looks or runs.</span></span>  
    
1.  <span data-ttu-id="52e8e-123">Observe el texto del botón.</span><span class="sxs-lookup"><span data-stu-id="52e8e-123">Notice the text in the button.</span></span>  
1.  <span data-ttu-id="52e8e-124">Escriba `document.getElementById('hello').textContent = 'Hello, Console!'` la **consola y,** a continuación, `Enter` seleccione para evaluar la expresión.</span><span class="sxs-lookup"><span data-stu-id="52e8e-124">Type `document.getElementById('hello').textContent = 'Hello, Console!'` in the **Console** and then select `Enter` to evaluate the expression.</span></span>  <span data-ttu-id="52e8e-125">Observe cómo cambia el texto dentro del botón.</span><span class="sxs-lookup"><span data-stu-id="52e8e-125">Notice how the text inside the button changes.</span></span>  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Cómo se ve la consola después de evaluar la expresión" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       <span data-ttu-id="52e8e-127">Cómo se **ve la consola** después de evaluar la expresión</span><span class="sxs-lookup"><span data-stu-id="52e8e-127">How the **Console** looks after evaluating the expression</span></span>  
    :::image-end:::  
    
    `"Hello, Console!"`<span data-ttu-id="52e8e-128">, se muestra debajo del código que ha evaluado.</span><span class="sxs-lookup"><span data-stu-id="52e8e-128">, is displayed below the code that you evaluated.</span></span>  <span data-ttu-id="52e8e-129">Recuerde los 4 pasos de REPL: leer, evaluar, imprimir, bucle.</span><span class="sxs-lookup"><span data-stu-id="52e8e-129">Remember the 4 steps of REPL: read, evaluate, print, loop.</span></span>  <span data-ttu-id="52e8e-130">Después de evaluar el código, una REPL imprime el resultado de la expresión.</span><span class="sxs-lookup"><span data-stu-id="52e8e-130">After evaluating your code, a REPL prints the result of the expression.</span></span>  <span data-ttu-id="52e8e-131">Por `"Hello, Console!"` lo tanto, debe ser el resultado de la evaluación `document.getElementById('hello').textContent = 'Hello, Console!'` .</span><span class="sxs-lookup"><span data-stu-id="52e8e-131">So `"Hello, Console!"` must be the result of evaluating `document.getElementById('hello').textContent = 'Hello, Console!'`.</span></span>  
    
## <a name="run-arbitrary-javascript-that-is-not-related-to-the-page"></a><span data-ttu-id="52e8e-132">Ejecutar JavaScript arbitrario que no esté relacionado con la página</span><span class="sxs-lookup"><span data-stu-id="52e8e-132">Run arbitrary JavaScript that is not related to the page</span></span>  

<span data-ttu-id="52e8e-133">A veces, solo quieres un área de juegos de código donde puedas probar código o probar nuevas características de JavaScript con las que no estás familiarizado.</span><span class="sxs-lookup"><span data-stu-id="52e8e-133">Sometimes, you just want a code playground where you are able to test some code, or try out new JavaScript features you are not familiar with.</span></span>  <span data-ttu-id="52e8e-134">La **consola** es un lugar perfecto para este tipo de experimentos.</span><span class="sxs-lookup"><span data-stu-id="52e8e-134">The **Console** is a perfect place for these kinds of experiments.</span></span>  

1.  <span data-ttu-id="52e8e-135">Escriba `5 + 15` la consola y seleccione para evaluar la `Enter` expresión.</span><span class="sxs-lookup"><span data-stu-id="52e8e-135">Type `5 + 15` in the Console and select `Enter` to evaluate the expression.</span></span> <span data-ttu-id="52e8e-136">La consola imprime el resultado de la expresión debajo del código.</span><span class="sxs-lookup"><span data-stu-id="52e8e-136">The Console prints out the result of the expression below your code.</span></span>  <span data-ttu-id="52e8e-137">En la siguiente figura, la **consola** debe mostrar el resultado después de evaluar la expresión.</span><span class="sxs-lookup"><span data-stu-id="52e8e-137">In the following figure, your **Console** should display the result after evaluating the expression.</span></span>  

1.  <span data-ttu-id="52e8e-138">Escriba el siguiente código en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="52e8e-138">Type the following code into the **Console**.</span></span>  <span data-ttu-id="52e8e-139">Intenta escribirlo, carácter por carácter, en lugar de copiarlo.</span><span class="sxs-lookup"><span data-stu-id="52e8e-139">Try typing it out, character-by-character, rather than copy-pasting it.</span></span>  
    
    ```javascript
    function add(a, b=20)
    ```  
    
    <span data-ttu-id="52e8e-140">Si no está familiarizado con la sintaxis, navegue para definir los `b=20` valores predeterminados de los [argumentos de función][Esma6DefaultParameterValues].</span><span class="sxs-lookup"><span data-stu-id="52e8e-140">If you are unfamiliar with the `b=20` syntax, navigate to [define default values for function arguments][Esma6DefaultParameterValues].</span></span>  
    
1.  <span data-ttu-id="52e8e-141">Ahora, ejecute la función que acaba de definir.</span><span class="sxs-lookup"><span data-stu-id="52e8e-141">Now, run the function that you just defined.</span></span>  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="La consola se muestra después de evaluar las expresiones del fragmento de código" lightbox="../media/console-javascript-example-console-playground.msft.png":::
             <span data-ttu-id="52e8e-143">La **consola** se muestra después de evaluar las expresiones del fragmento de código</span><span class="sxs-lookup"><span data-stu-id="52e8e-143">The **Console** displays after evaluating the expressions in the code snippet</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` <span data-ttu-id="52e8e-144">se evalúa porque cuando se llama a la `45` función sin un segundo `add` argumento, el valor predeterminado es `b` `20` .</span><span class="sxs-lookup"><span data-stu-id="52e8e-144">evaluates to `45` because when the `add` function is called without a second argument, `b` defaults to `20`.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="52e8e-145">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="52e8e-145">Next steps</span></span>  

<!--To explore more features related to running JavaScript in the **Console**, navigate to [Run JavaScript][DevToolsConsoleReference].  -->  

<!--todo: add console reference (run javascript) section when available  -->  

<span data-ttu-id="52e8e-146">DevTools te permite pausar un script en medio de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="52e8e-146">DevTools lets you pause a script in the middle of running.</span></span>  <span data-ttu-id="52e8e-147">Mientras está en pausa, puede \*\*\*\* usar la consola para ver y cambiar la página en `window` ese `DOM` momento.</span><span class="sxs-lookup"><span data-stu-id="52e8e-147">While you are paused, you may use the **Console** to view and change the `window` or `DOM` of the page at that moment in time.</span></span>  <span data-ttu-id="52e8e-148">El flujo de trabajo crea un flujo de trabajo de depuración eficaz.</span><span class="sxs-lookup"><span data-stu-id="52e8e-148">The workflow makes for a powerful debugging workflow.</span></span>  <span data-ttu-id="52e8e-149">Para obtener un tutorial interactivo, vaya a [Introducción a La depuración de JavaScript][DevToolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="52e8e-149">For an interactive tutorial, navigate to [Get Started With Debugging JavaScript][DevToolsJavascriptIndex].</span></span>  

<span data-ttu-id="52e8e-150">La **consola** también tiene un conjunto de funciones de comodidad que facilitan la interacción con una página.</span><span class="sxs-lookup"><span data-stu-id="52e8e-150">The **Console** also has a set of convenience functions that make it easier to interact with a page.</span></span>  <span data-ttu-id="52e8e-151">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="52e8e-151">For example:</span></span>  

*   <span data-ttu-id="52e8e-152">En lugar de escribir `document.querySelector()` para seleccionar un elemento, escriba `$()` .</span><span class="sxs-lookup"><span data-stu-id="52e8e-152">Rather than typing `document.querySelector()` to select an element, type `$()`.</span></span>  <span data-ttu-id="52e8e-153">Esta sintaxis se inspira en jQuery, pero en realidad no es jQuery.</span><span class="sxs-lookup"><span data-stu-id="52e8e-153">This syntax is inspired by jQuery, but it is not actually jQuery.</span></span>  <span data-ttu-id="52e8e-154">Es solo un alias para `document.querySelector()` .</span><span class="sxs-lookup"><span data-stu-id="52e8e-154">It is just an alias for `document.querySelector()`.</span></span>  
*   `debug(function)` <span data-ttu-id="52e8e-155">establece de forma eficaz un punto de interrupción en la primera línea de esa función.</span><span class="sxs-lookup"><span data-stu-id="52e8e-155">effectively sets a breakpoint on the first line of that function.</span></span>  
*   `keys(object)` <span data-ttu-id="52e8e-156">devuelve una matriz que contiene las claves del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="52e8e-156">returns an array containing the keys of the specified object.</span></span>  

<span data-ttu-id="52e8e-157">Para obtener más información acerca de las funciones de comodidad, vaya a [Console Utilities API Reference][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="52e8e-157">For more information about the convenience functions, navigate to [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="52e8e-158">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="52e8e-158">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Introducción al registro de mensajes en la consola | Microsoft Docs"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Referencia de consola | Microsoft Docs"  
[DevToolsConsoleUtilities]: ./utilities.md "Referencia de api de utilidades de consola | Microsoft Docs"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft Docs"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Expresiones frente a instrucciones en JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Valores de parámetros predeterminados : control de parámetros extendidos - ECMAScript 6 : nuevas características: información general & comparación"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Ejemplo de Javascript de consola | Glitch"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Bucle read-eval-print - Wikipedia"  

> [!NOTE]
> <span data-ttu-id="52e8e-167">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="52e8e-167">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="52e8e-168">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/javascript) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="52e8e-168">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/javascript) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="52e8e-170">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="52e8e-170">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
description: Una introducción al uso de la herramienta consola dentro del Microsoft Edge Developer Tools como un entorno JavaScript.
title: La consola como entorno de JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, JavaScript, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: f75ac6d728c9a69542b2f58df85248759267f76d
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483660"
---
# <a name="the-console-as-a-javascript-environment"></a><span data-ttu-id="79b59-104">La consola como entorno de JavaScript</span><span class="sxs-lookup"><span data-stu-id="79b59-104">The Console as a JavaScript environment</span></span>  

<span data-ttu-id="79b59-105">La **herramienta Consola** dentro del explorador DevTools es un entorno [REPL.][WikiReadEvalPrintLoop]</span><span class="sxs-lookup"><span data-stu-id="79b59-105">The **Console** tool inside the browser DevTools is a [REPL][WikiReadEvalPrintLoop] environment.</span></span>  <span data-ttu-id="79b59-106">Significa que puede escribir cualquier JavaScript en la **consola que se** ejecute inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="79b59-106">It means that you may write any JavaScript in the **Console** that runs immediately.</span></span>

<span data-ttu-id="79b59-107">Para probarlo, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="79b59-107">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="79b59-108">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="79b59-108">Open the **Console**.</span></span>  
    *   <span data-ttu-id="79b59-109">Seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="79b59-109">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
1.  <span data-ttu-id="79b59-110">Escriba `2 + 2`.</span><span class="sxs-lookup"><span data-stu-id="79b59-110">Type `2 + 2`.</span></span>  <span data-ttu-id="79b59-111">La **consola** ya muestra el resultado `4` en la siguiente línea mientras lo escribe.</span><span class="sxs-lookup"><span data-stu-id="79b59-111">The **Console** already displays the result `4` on the next line while you type it.</span></span>  <span data-ttu-id="79b59-112">La `Eager evaluation` característica le ayuda a escribir JavaScript válido.</span><span class="sxs-lookup"><span data-stu-id="79b59-112">The `Eager evaluation` feature helps you write valid JavaScript.</span></span>  <span data-ttu-id="79b59-113">Muestra el resultado mientras escribe si es incorrecto o si existe un resultado válido.</span><span class="sxs-lookup"><span data-stu-id="79b59-113">It displays the result while you type whether it's wrong or if a valid result exists.</span></span>  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="La consola muestra el resultado de 2 + 2 en directo al escribirlo" lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   <span data-ttu-id="79b59-115">**La** consola muestra el resultado `2 + 2` de live a medida que lo escribe</span><span class="sxs-lookup"><span data-stu-id="79b59-115">**Console** displays the result of `2 + 2` live as you type it</span></span>  
:::image-end:::  

<span data-ttu-id="79b59-116">Si selecciona , la consola ejecuta el comando JavaScript, le proporciona el resultado y le permite `Enter` escribir el siguiente comando. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="79b59-116">If you select `Enter`, the **Console** runs the JavaScript command, gives you the result, and allows you to write the next command.</span></span>  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Ejecutar varias expresiones de JavaScript sucesivamente" lightbox="../media/console-javascript-several-expressions.msft.png":::
   <span data-ttu-id="79b59-118">Ejecutar varias expresiones de JavaScript sucesivamente</span><span class="sxs-lookup"><span data-stu-id="79b59-118">Run several JavaScript expressions in succession</span></span>  
:::image-end:::  

## <a name="autocompletion-to-write-complex-expressions"></a><span data-ttu-id="79b59-119">Autocompletion to write complex expressions</span><span class="sxs-lookup"><span data-stu-id="79b59-119">Autocompletion to write complex expressions</span></span>

<span data-ttu-id="79b59-120">El último ejemplo puede parecer espantoso, pero **la consola** le ayuda a escribir JavaScript complejo con una excelente característica de autocompleción.</span><span class="sxs-lookup"><span data-stu-id="79b59-120">The last example may seem scary, but the **Console** helps you write complex JavaScript using an excellent autocompletion feature.</span></span>  <span data-ttu-id="79b59-121">Esta característica es una excelente manera de obtener información sobre los métodos que no conocías antes.</span><span class="sxs-lookup"><span data-stu-id="79b59-121">This feature is a great way to learn about methods you didn't know before.</span></span>  

<span data-ttu-id="79b59-122">Para probarlo, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="79b59-122">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="79b59-123">Escriba `doc`.</span><span class="sxs-lookup"><span data-stu-id="79b59-123">Type `doc`.</span></span>  
1.  <span data-ttu-id="79b59-124">Elija `document` en el menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="79b59-124">Choose `document` from the dropdown menu.</span></span>  
1.  <span data-ttu-id="79b59-125">Seleccione la `tab` clave para elegirla.</span><span class="sxs-lookup"><span data-stu-id="79b59-125">Select the `tab` key to choose it.</span></span>  
1.  <span data-ttu-id="79b59-126">Escriba `.bo`.</span><span class="sxs-lookup"><span data-stu-id="79b59-126">Type `.bo`.</span></span>  
1.  <span data-ttu-id="79b59-127">Seleccione `tab` para obtener `document.body` .</span><span class="sxs-lookup"><span data-stu-id="79b59-127">Select `tab` to get `document.body`.</span></span>  
1.  <span data-ttu-id="79b59-128">Escriba otro para obtener una lista grande de posibles propiedades y métodos `.` disponibles en el cuerpo de la página web actual.</span><span class="sxs-lookup"><span data-stu-id="79b59-128">Type another `.` to get a large list of possible properties and methods available on the body of the current webpage.</span></span>  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Autocompletion de consola de expresiones de JavaScript" lightbox="../media/console-javascript-autocomplete.msft.png":::
   <span data-ttu-id="79b59-130">**Autocompletion** de consola de expresiones de JavaScript</span><span class="sxs-lookup"><span data-stu-id="79b59-130">**Console** autocompletion of JavaScript expressions</span></span>  
:::image-end:::  

## <a name="console-history"></a><span data-ttu-id="79b59-131">Historial de consolas</span><span class="sxs-lookup"><span data-stu-id="79b59-131">Console history</span></span>

<span data-ttu-id="79b59-132">Al igual que con muchas otras experiencias de línea de comandos, también tiene un historial de comandos.</span><span class="sxs-lookup"><span data-stu-id="79b59-132">As with many other command-line experiences, you also have a history of commands.</span></span>  <span data-ttu-id="79b59-133">Seleccione `Arrow Up` esta opción para mostrar los comandos que ha escrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="79b59-133">Select `Arrow Up` to display the commands you entered before.</span></span>  <span data-ttu-id="79b59-134">La autocompleción también conserva un historial de los comandos que ha especificado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="79b59-134">Autocompletion also keeps a history of the commands you previously typed.</span></span>  <span data-ttu-id="79b59-135">Puede escribir las primeras letras de los comandos anteriores y las opciones anteriores se muestran en un cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="79b59-135">You may type the first few letters of earlier commands and your previous choices display in a textbox.</span></span>  

<span data-ttu-id="79b59-136">Además, la **consola** también ofrece bastantes métodos de [utilidad][DevtoolsConsoleUtilities] que te facilitan la vida.</span><span class="sxs-lookup"><span data-stu-id="79b59-136">Also, the **Console** also offers quite a few [utility methods][DevtoolsConsoleUtilities] that make your life easier.</span></span>  <span data-ttu-id="79b59-137">Por ejemplo, `$_` siempre contiene el resultado de la última expresión que ejecutó en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="79b59-137">For example, `$_` always contains the result of the last expression you ran in the **Console**.</span></span>

:::image type="complex" source="../media/console-javascript-console-history.msft.png" alt-text="La expresión $_ en la consola siempre contiene el último resultado" lightbox="../media/console-javascript-console-history.msft.png":::
    <span data-ttu-id="79b59-139">La `$_` expresión de la **consola** siempre contiene el último resultado</span><span class="sxs-lookup"><span data-stu-id="79b59-139">The `$_` expression in the **Console** always contains the last result</span></span>  
:::image-end:::  

## <a name="multiline-edits"></a><span data-ttu-id="79b59-140">Ediciones multilínea</span><span class="sxs-lookup"><span data-stu-id="79b59-140">Multiline edits</span></span>

<span data-ttu-id="79b59-141">De forma predeterminada, **la consola** solo proporciona una línea para escribir la expresión de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="79b59-141">By default, the **Console** only gives you one line to write your JavaScript expression.</span></span>  <span data-ttu-id="79b59-142">El código se ejecuta al seleccionar `Enter` .</span><span class="sxs-lookup"><span data-stu-id="79b59-142">You code runs when you select `Enter`.</span></span> <span data-ttu-id="79b59-143">La limitación de una línea puede frustrarse.</span><span class="sxs-lookup"><span data-stu-id="79b59-143">The one line limitation may frustrate you.</span></span>  <span data-ttu-id="79b59-144">Para evitar la limitación de una línea, seleccione `Shift` + `Enter` en lugar de `Enter` .</span><span class="sxs-lookup"><span data-stu-id="79b59-144">To work around the one line limitation, select `Shift`+`Enter` instead of `Enter`.</span></span>  <span data-ttu-id="79b59-145">En el siguiente ejemplo, el valor mostrado es el resultado de todas las líneas que se ejecutan en orden.</span><span class="sxs-lookup"><span data-stu-id="79b59-145">In the following example, the value displayed is the result of all the lines run in order.</span></span>  

:::image type="complex" source="../media/console-javascript-multiline.msft.png" alt-text="Seleccione Mayús+Entrar para escribir varias líneas de JavaScript y el valor resultante se ejecuta en orden" lightbox="../media/console-javascript-multiline.msft.png":::
   <span data-ttu-id="79b59-147">Seleccione `Shift` + `Enter` para escribir varias líneas de JavaScript y el valor resultante se ejecuta en orden</span><span class="sxs-lookup"><span data-stu-id="79b59-147">Select `Shift`+`Enter` to write several lines of JavaScript and the resulting value is run in order</span></span>  
:::image-end:::  

<span data-ttu-id="79b59-148">Si inicia una instrucción multilínea en **la consola,** se reconoce automáticamente y se aplica sangría.</span><span class="sxs-lookup"><span data-stu-id="79b59-148">If you start a multiline statement in the **Console**, it gets automatically recognized and indented.</span></span>  <span data-ttu-id="79b59-149">Por ejemplo, si inicia una instrucción block con una llave.</span><span class="sxs-lookup"><span data-stu-id="79b59-149">For example, if you start a block statement with a curly brace.</span></span>  

:::image type="complex" source="../media/console-javascript-automatic-lineindent.msft.png" alt-text="La consola ya reconoce expresiones multilínea con llaves y sangrías cada una." lightbox="../media/console-javascript-automatic-lineindent.msft.png":::
    <span data-ttu-id="79b59-151">**La** consola ya reconoce expresiones multilínea con llaves y sangrías cada una.</span><span class="sxs-lookup"><span data-stu-id="79b59-151">**Console** already recognizes multiline expressions using curly braces and indents each for you</span></span>  
:::image-end:::  

## <a name="network-requests-using-top-level-await"></a><span data-ttu-id="79b59-152">Solicitudes de red con await() de nivel superior</span><span class="sxs-lookup"><span data-stu-id="79b59-152">Network requests using top-level await()</span></span>  

<span data-ttu-id="79b59-153">Aparte de en sus propios scripts, **la** consola admite la espera de [nivel][GithubTc39ProposalTopLevelAwait] superior para ejecutar JavaScript asincrónico arbitrario en él.</span><span class="sxs-lookup"><span data-stu-id="79b59-153">Other than in your own scripts, **Console** supports [top level await][GithubTc39ProposalTopLevelAwait] to run arbitrary asynchronous JavaScript in it.</span></span>  <span data-ttu-id="79b59-154">Por ejemplo, use la `fetch` API sin ajustar la instrucción con una función `await` asincrónica.</span><span class="sxs-lookup"><span data-stu-id="79b59-154">For example, use the `fetch` API without wrapping the `await` statement with an async function.</span></span>  

<span data-ttu-id="79b59-155">Para obtener los últimos 50 problemas que se han presentado en el repositorio Microsoft Edge [Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] GitHub, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="79b59-155">To get the last 50 issues filed on the [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] GitHub repo, complete the following actions.</span></span>  

1.  <span data-ttu-id="79b59-156">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="79b59-156">Open the **Console**.</span></span>  
1.  <span data-ttu-id="79b59-157">Copie y pegue el siguiente fragmento de código para obtener un objeto que contenga 10 entradas.</span><span class="sxs-lookup"><span data-stu-id="79b59-157">Copy and paste the following code snippet to get an object that contains 10 entries.</span></span>  
    
    ```javascript
    await ( await fetch(
    'https://api.github.com/repos/microsoft/vscode-edge-devtools/issues?state=all&per_page=50&page=1'
    )).json();
    ```  
    
:::image type="complex" source="../media/console-javascript-top-level-await.msft.png" alt-text="La consola muestra el resultado de una solicitud de captura asincrónica de nivel superior" lightbox="../media/console-javascript-top-level-await.msft.png":::
    <span data-ttu-id="79b59-159">**La** consola muestra el resultado de una solicitud asincrónica de nivel `fetch` superior</span><span class="sxs-lookup"><span data-stu-id="79b59-159">**Console** displays the result of a top-level async `fetch` request</span></span>  
:::image-end:::  

<span data-ttu-id="79b59-160">Las 10 entradas son difíciles de reconocer, ya que se muestra mucha información.</span><span class="sxs-lookup"><span data-stu-id="79b59-160">The 10 entries are hard to recognize, since a lot of information is displayed.</span></span>  <span data-ttu-id="79b59-161">Afortunadamente, puede usar el método log para recibir solo la información en la que `console.table()` está interesado.</span><span class="sxs-lookup"><span data-stu-id="79b59-161">Luckily enough, you may use the `console.table()` log method to only receive the information in which you're interested.</span></span>  

:::image type="complex" source="../media/console-javascript-filtered-with-table.msft.png" alt-text="Mostrar el último resultado en un formato legible con console.table" lightbox="../media/console-javascript-filtered-with-table.msft.png":::
    <span data-ttu-id="79b59-163">Mostrar el último resultado en un formato de lectura humana mediante</span><span class="sxs-lookup"><span data-stu-id="79b59-163">Display the last result in a human readable format using</span></span> `console.table`  
:::image-end:::  

<span data-ttu-id="79b59-164">Para volver a usar los datos devueltos de una expresión, puede usar el método `copy()` de utilidad de console . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="79b59-164">To reuse the data returned from an expression, you may use the `copy()` utility method of the **Console**.</span></span>  <span data-ttu-id="79b59-165">El siguiente fragmento de código envía la solicitud y copia los datos de la respuesta al Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="79b59-165">The following code snippet sends the request and copies the data from the response to the clipboard.</span></span>  

```javascript
copy(await (await fetch(
'https://api.github.com/repos/microsoft/vscode-edge-devtools/issues?state=all&per_page=50&page=1'
)).json())
```  

<span data-ttu-id="79b59-166">Use la **consola como** una excelente manera de practicar la funcionalidad de JavaScript y realizar algunos cálculos rápidos.</span><span class="sxs-lookup"><span data-stu-id="79b59-166">Use the **Console** as a great way to practice JavaScript functionality and to do some quick calculations.</span></span>  <span data-ttu-id="79b59-167">La potencia real es el hecho de que tiene acceso al objeto [window.][MdnDocsWebApiWindow]</span><span class="sxs-lookup"><span data-stu-id="79b59-167">The real power is the fact that you have access to the [window][MdnDocsWebApiWindow] object.</span></span>  <span data-ttu-id="79b59-168">Puede interactuar [con el DOM en la consola][DevtoolsConsoleConsoleDomInteraction].</span><span class="sxs-lookup"><span data-stu-id="79b59-168">You may [interact with the DOM in Console][DevtoolsConsoleConsoleDomInteraction].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="79b59-169">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="79b59-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleDomInteraction]: ./console-dom-interaction.md "Use la consola para interactuar con el dom | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Referencia de api de utilidades de consola | Microsoft Docs"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubTc39ProposalTopLevelAwait]: https://github.com/tc39/proposal-top-level-await "Propuesta ecmascript: espera de nivel superior - tc39/proposal-top-level-await | GitHub"

[MdnDocsWebApiWindow]: https://developer.mozilla.org/docs/Web/API/Window "Ventana | MDN"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Bucle read–eval–print | Wikipedia"  

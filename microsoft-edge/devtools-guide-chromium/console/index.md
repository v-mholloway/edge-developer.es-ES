---
description: Una introducción a la herramienta consola dentro de Microsoft Edge Developer Tools.
title: Usar la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: badcaae0ad637fe7a027f78d00daf9133789693e
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624748"
---
# <a name="use-the-console"></a><span data-ttu-id="e576f-104">Usar la consola</span><span class="sxs-lookup"><span data-stu-id="e576f-104">Use the Console</span></span>  

<span data-ttu-id="e576f-105">La **herramienta Consola** de DevTools le ayuda con varias tareas.</span><span class="sxs-lookup"><span data-stu-id="e576f-105">The **Console** tool of the DevTools helps you with several tasks.</span></span>  <span data-ttu-id="e576f-106">La siguiente lista incluye algunas de las tareas.</span><span class="sxs-lookup"><span data-stu-id="e576f-106">The following list includes some of the tasks.</span></span>  

*   <span data-ttu-id="e576f-107">Descubra por qué algo no funciona en el proyecto actual y [realice un seguimiento de los problemas][DevtoolsConsoleConsoleDebugJavascript].</span><span class="sxs-lookup"><span data-stu-id="e576f-107">Find out why something isn't working in the current project and [track down problems][DevtoolsConsoleConsoleDebugJavascript].</span></span>  
*   <span data-ttu-id="e576f-108">[Obtenga información sobre el proyecto web en][DevtoolsConsoleConsoleFilters] el explorador como mensajes de registro.</span><span class="sxs-lookup"><span data-stu-id="e576f-108">[Get information about the web project][DevtoolsConsoleConsoleFilters] in the browser as log messages.</span></span>  
*   <span data-ttu-id="e576f-109">[Información de registro][DevtoolsConsoleConsoleLog] en scripts con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="e576f-109">[Log information][DevtoolsConsoleConsoleLog] in scripts for debugging purposes.</span></span>  
*   <span data-ttu-id="e576f-110">[Pruebe las expresiones de JavaScript][DevtoolsConsoleConsoleJavascript] en un [entorno REPL.][WikiReadEvalPrintLoop]</span><span class="sxs-lookup"><span data-stu-id="e576f-110">[Try JavaScript expressions][DevtoolsConsoleConsoleJavascript] live in a [REPL][WikiReadEvalPrintLoop] environment.</span></span>  
*   <span data-ttu-id="e576f-111">[Interactúe con el proyecto web en el explorador][DevtoolsConsoleConsoleDomInteraction] con JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e576f-111">[Interact with the web project in the browser][DevtoolsConsoleConsoleDomInteraction] using JavaScript.</span></span>  
    
<span data-ttu-id="e576f-112">La **consola** es una excelente herramienta complementaria para usarla con otras herramientas.</span><span class="sxs-lookup"><span data-stu-id="e576f-112">The **Console** is a great companion tool to use with others tools.</span></span>  <span data-ttu-id="e576f-113">La **consola** proporciona una forma eficaz de crear scripts de funcionalidad, inspeccionar y manipular la página web actual mediante JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e576f-113">The **Console** provides a powerful way to script functionality, inspect, and manipulate the current webpage using JavaScript.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-main.msft.png" alt-text="La herramienta Consola abierta en el panel superior" lightbox="../media/console-intro-console-main.msft.png":::
         <span data-ttu-id="e576f-115">La **herramienta Consola** abierta en el panel superior</span><span class="sxs-lookup"><span data-stu-id="e576f-115">The **Console** tool open in the upper panel</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-panel.msft.png" alt-text="Consola en el panel inferior con la herramienta Elementos abierta encima de ella" lightbox="../media/console-intro-console-panel.msft.png":::
         <span data-ttu-id="e576f-117">**Consola** en el panel inferior con la **herramienta Elementos** abierta encima de ella</span><span class="sxs-lookup"><span data-stu-id="e576f-117">**Console** in the lower panel with the **Elements** tool open above it</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e576f-118">La forma más rápida de abrir directamente la **consola** es `Control` + `Shift` + `J` seleccionar \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="e576f-118">The fastest way to directly open the **Console** is to select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

## <a name="error-reports-and-console"></a><span data-ttu-id="e576f-119">Informes de errores y consola</span><span class="sxs-lookup"><span data-stu-id="e576f-119">Error reports and Console</span></span>  

<span data-ttu-id="e576f-120">**La** consola es el lugar predeterminado donde se notifican los errores de conectividad y JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e576f-120">**Console** is the default place where JavaScript and connectivity errors are reported.</span></span>  <span data-ttu-id="e576f-121">Si se produce \*\*\*\* algún error, el contador Problemas se muestra junto al icono **Configuración** en DevTools que proporciona el número de errores y advertencias.</span><span class="sxs-lookup"><span data-stu-id="e576f-121">If any errors occur, the **Issues counter** is displayed next to the **Settings** icon in DevTools that provides the number of errors and warnings.</span></span>  <span data-ttu-id="e576f-122">Seleccione el **contador Problemas** para abrir la **herramienta Problemas** y mostrar el problema.</span><span class="sxs-lookup"><span data-stu-id="e576f-122">Select the **Issues counter** to open the **Issues** tool and display the problem.</span></span>  <span data-ttu-id="e576f-123">Para obtener más información, vaya [a Depurar errores notificados en consola][DevtoolsConsoleConsoleDebugJavascript].</span><span class="sxs-lookup"><span data-stu-id="e576f-123">For more information, navigate to [Debug errors reported in Console][DevtoolsConsoleConsoleDebugJavascript].</span></span>

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="DevTools proporciona información detallada sobre el error en la consola" lightbox="../media/console-debug-displays-error.msft.png":::
   <span data-ttu-id="e576f-125">DevTools proporciona información detallada sobre el error en la **consola**</span><span class="sxs-lookup"><span data-stu-id="e576f-125">DevTools gives detailed information about the error in the **Console**</span></span>  
:::image-end:::  

## <a name="inspect-and-filter-information-on-the-current-webpage"></a><span data-ttu-id="e576f-126">Inspeccionar y filtrar información en la página web actual</span><span class="sxs-lookup"><span data-stu-id="e576f-126">Inspect and filter information on the current webpage</span></span>  

<span data-ttu-id="e576f-127">Al abrir DevTools en una página web, puede haber una cantidad abrumadora de información en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e576f-127">When you open DevTools on a webpage, there may be an overwhelming amount of information in the **Console**.</span></span>  <span data-ttu-id="e576f-128">La cantidad de información se convierte en un problema cuando necesita identificar información importante.</span><span class="sxs-lookup"><span data-stu-id="e576f-128">The amount of information becomes a problem when you need to identify important information.</span></span>  <span data-ttu-id="e576f-129">Para ver la información importante que necesita acción, use la [herramienta Problemas][DevtoolsIssuesIndex] en DevTools.</span><span class="sxs-lookup"><span data-stu-id="e576f-129">To view the important information that needs action, use the [Issues][DevtoolsIssuesIndex] tool in DevTools.</span></span>

<span data-ttu-id="e576f-130">Los problemas se mueven gradualmente de la **consola** a la **herramienta** Problemas.</span><span class="sxs-lookup"><span data-stu-id="e576f-130">Issues are gradually being moved from the **Console** to the **Issues** tool.</span></span>  <span data-ttu-id="e576f-131">Sin embargo, todavía hay mucha información en **console**, por lo que es una buena idea conocer las opciones automatizadas de registro y filtro en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e576f-131">However, there's still a lot of information in **Console**, which is why it's a good idea to know about the automated log and filter options in the **Console**.</span></span>  <span data-ttu-id="e576f-132">Para obtener más información, vaya a [Filtrar mensajes de consola][DevtoolsConsoleConsoleFilters].</span><span class="sxs-lookup"><span data-stu-id="e576f-132">For more information, navigate to [Filter Console messages][DevtoolsConsoleConsoleFilters].</span></span>

:::image type="complex" source="../media/console-intro-noise.msft.png" alt-text="DevTools con una consola llena de mensajes" lightbox="../media/console-intro-noise.msft.png":::
   <span data-ttu-id="e576f-134">DevTools con una **consola llena** de mensajes</span><span class="sxs-lookup"><span data-stu-id="e576f-134">DevTools with a **Console** full of messages</span></span>  
:::image-end:::  

## <a name="log-information-to-display-in-the-console"></a><span data-ttu-id="e576f-135">Información de registro que se mostrará en la consola</span><span class="sxs-lookup"><span data-stu-id="e576f-135">Log information to display in the Console</span></span>  

<span data-ttu-id="e576f-136">El caso de uso más popular para la **consola** es registrar información de los scripts mediante el `console.log()` método u otros métodos similares.</span><span class="sxs-lookup"><span data-stu-id="e576f-136">The most popular use case for the **Console** is logging information from your scripts using the `console.log()` method or other similar methods.</span></span>  <span data-ttu-id="e576f-137">Para probarlo, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e576f-137">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="e576f-138">Para abrir **consola**, `Control` + `Shift` + `J` seleccione \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="e576f-138">To open **Console**, select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
1.  <span data-ttu-id="e576f-139">Vaya a [Ejemplos de mensajes de consola: registro, información, error][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]y advertencia, o copie y ejecute el siguiente fragmento de código en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e576f-139">Navigate to [Console messages examples: log, info, error and warn][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml], or copy and run the following code snippet in the **Console**.</span></span>  
    
    ```javascript
    console.log('This is a log message');
    console.info('This is some information'); 
    console.error('This is an error');
    console.warn('This is a warning');
    console.log(document.body.getBoundingClientRect());
    console.table(document.body.getBoundingClientRect());
    let technologies = ["HTML", "CSS", "SVG", "ECMAScript"];
    console.groupCollapsed('Technolgies');
    technologies.forEach(tech => {console.info(tech);})
    console.groupEnd('Technolgies');
    ```  
    
1.  <span data-ttu-id="e576f-140">La **consola** muestra los resultados.</span><span class="sxs-lookup"><span data-stu-id="e576f-140">The **Console** displays the results.</span></span>  
    
    :::image type="complex" source="../media/console-intro-logging.msft.png" alt-text="Consola llena de mensajes causados por código de demostración" lightbox="../media/console-intro-logging.msft.png":::
       <span data-ttu-id="e576f-142">**Consola** llena de mensajes causados por código de demostración</span><span class="sxs-lookup"><span data-stu-id="e576f-142">**Console** full of messages caused by demo code</span></span>  
    :::image-end:::  
    
<span data-ttu-id="e576f-143">Hay muchos métodos útiles disponibles cuando se trabaja con la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e576f-143">Many useful methods are available when you work with the **Console**.</span></span>  <span data-ttu-id="e576f-144">Para obtener más información, vaya [a Registrar mensajes en la herramienta Consola][DevtoolsConsoleConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="e576f-144">For more information, navigate to [Log messages in the Console tool][DevtoolsConsoleConsoleLog].</span></span>  

## <a name="try-your-javascript-live-in-the-console"></a><span data-ttu-id="e576f-145">Pruebe JavaScript en directo en la consola</span><span class="sxs-lookup"><span data-stu-id="e576f-145">Try your JavaScript live in the Console</span></span>  

<span data-ttu-id="e576f-146">La **consola** no es solo un lugar para registrar información.</span><span class="sxs-lookup"><span data-stu-id="e576f-146">The **Console** isn't only a place to log information.</span></span>  <span data-ttu-id="e576f-147">La **consola** es un [entorno REPL.][WikiReadEvalPrintLoop]</span><span class="sxs-lookup"><span data-stu-id="e576f-147">The **Console** is a [REPL][WikiReadEvalPrintLoop] environment.</span></span>  <span data-ttu-id="e576f-148">Al escribir cualquier JavaScript en la **consola,** el código se ejecuta inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="e576f-148">When you write any JavaScript in the **Console**, the code runs immediately.</span></span>  <span data-ttu-id="e576f-149">Puede resultar útil probar algunas nuevas características de JavaScript o realizar algunos cálculos rápidos.</span><span class="sxs-lookup"><span data-stu-id="e576f-149">You may find it useful to test some new JavaScript features or to do some quick calculations.</span></span>  <span data-ttu-id="e576f-150">Además, obtiene todas las características que espera de un entorno de edición moderno, como la autocompleción, el resaltado de sintaxis y el historial.</span><span class="sxs-lookup"><span data-stu-id="e576f-150">Also, you get all of the features you expect from a modern editing environment, such as autocompletion, syntax highlighting, and history.</span></span>  <span data-ttu-id="e576f-151">Para probarlo, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e576f-151">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="e576f-152">Vaya a la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e576f-152">Navigate to the **Console**.</span></span>  
1.  <span data-ttu-id="e576f-153">Escriba `2 + 2`.</span><span class="sxs-lookup"><span data-stu-id="e576f-153">Type `2 + 2`.</span></span>  
    
<span data-ttu-id="e576f-154">La **consola** muestra el resultado `4` en la siguiente línea.</span><span class="sxs-lookup"><span data-stu-id="e576f-154">The **Console** displays the result `4` on the following line.</span></span>  <span data-ttu-id="e576f-155">Esta **característica de evaluación** de Eager es útil para depurar y comprobar que no está cometiendo errores en el código.</span><span class="sxs-lookup"><span data-stu-id="e576f-155">This **Eager evaluation** feature is useful to debug and verify that you aren't making mistakes in your code.</span></span>  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="La consola muestra el resultado de 2 + 2 en directo a medida que lo escribe" lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   <span data-ttu-id="e576f-157">La **consola** muestra el resultado de `2 + 2` live al escribirlo</span><span class="sxs-lookup"><span data-stu-id="e576f-157">The **Console** displays the result of `2 + 2` live as you type it</span></span>  
:::image-end:::  

<span data-ttu-id="e576f-158">Para ejecutar la expresión JavaScript en la **consola** y, opcionalmente, mostrar un resultado, seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e576f-158">To run the JavaScript expression in the **Console** and optionally display a result, select `Enter`.</span></span>  <span data-ttu-id="e576f-159">A continuación, puede escribir el siguiente código JavaScript que se ejecutará en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e576f-159">Then, you can write the next JavaScript code to run in the **Console**.</span></span>  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Ejecutar varias líneas de código JavaScript sucesivamente" lightbox="../media/console-javascript-several-expressions.msft.png":::
   <span data-ttu-id="e576f-161">Ejecutar varias líneas de código JavaScript sucesivamente</span><span class="sxs-lookup"><span data-stu-id="e576f-161">Run several lines of JavaScript code in succession</span></span>  
:::image-end:::  

<span data-ttu-id="e576f-162">De forma predeterminada, se ejecuta código JavaScript en una sola línea.</span><span class="sxs-lookup"><span data-stu-id="e576f-162">By default, you run JavaScript code on a single line.</span></span>  <span data-ttu-id="e576f-163">Para ejecutar una línea, escriba JavaScript y, a continuación, seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e576f-163">To run a line, type your JavaScript and then select `Enter`.</span></span>  <span data-ttu-id="e576f-164">Para evitar la limitación de una sola línea, seleccione `Shift` + `Enter` en lugar de `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e576f-164">To work around the single-line limitation, select `Shift`+`Enter` instead of `Enter`.</span></span>  <span data-ttu-id="e576f-165">De forma similar a otras experiencias de línea de comandos, para obtener acceso a los comandos de JavaScript anteriores, seleccione `Arrow-Up` .</span><span class="sxs-lookup"><span data-stu-id="e576f-165">Similar to other command-line experiences, to access your previous JavaScript commands, select `Arrow-Up`.</span></span>  <span data-ttu-id="e576f-166">La característica de autocompletion de **la consola** es una excelente manera de obtener información sobre métodos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="e576f-166">The autocompletion feature of the **Console** is a great way to learn about unfamiliar methods.</span></span>  <span data-ttu-id="e576f-167">Para probarlo, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e576f-167">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="e576f-168">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e576f-168">Open the **Console**.</span></span>  
1.  <span data-ttu-id="e576f-169">Escriba `doc`.</span><span class="sxs-lookup"><span data-stu-id="e576f-169">Type `doc`.</span></span>  
1.  <span data-ttu-id="e576f-170">Elija `document` en el menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="e576f-170">Choose `document` from the dropdown menu.</span></span>  
1.  <span data-ttu-id="e576f-171">Seleccione la `tab` clave para elegirla.</span><span class="sxs-lookup"><span data-stu-id="e576f-171">Select the `tab` key to choose it.</span></span>  
1.  <span data-ttu-id="e576f-172">Escriba `.bo`.</span><span class="sxs-lookup"><span data-stu-id="e576f-172">Type `.bo`.</span></span>  
1.  <span data-ttu-id="e576f-173">Seleccione `tab` para obtener `document.body` .</span><span class="sxs-lookup"><span data-stu-id="e576f-173">Select `tab` to get `document.body`.</span></span>  
1.  <span data-ttu-id="e576f-174">Escriba otro `.` para mostrar la lista completa de propiedades y métodos disponibles en el cuerpo de la página web actual.</span><span class="sxs-lookup"><span data-stu-id="e576f-174">Type another `.` to display the complete list of properties and methods available on the body of the current webpage.</span></span>  
    
<span data-ttu-id="e576f-175">Para obtener más información acerca de todas las formas de trabajar con **la consola,** vaya [a Consola como un entorno JavaScript][DevtoolsConsoleConsoleJavascript].</span><span class="sxs-lookup"><span data-stu-id="e576f-175">For more information about all the ways to work with **Console**, navigate to [Console as a JavaScript environment][DevtoolsConsoleConsoleJavascript].</span></span>  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Autocompletion de consola de expresiones de JavaScript" lightbox="../media/console-javascript-autocomplete.msft.png":::
   <span data-ttu-id="e576f-177">**Autocompletion** de consola de expresiones de JavaScript</span><span class="sxs-lookup"><span data-stu-id="e576f-177">**Console** autocompletion of JavaScript expressions</span></span>  
:::image-end:::  

## <a name="interact-with-the-current-webpage-in-the-browser"></a><span data-ttu-id="e576f-178">Interactuar con la página web actual en el explorador</span><span class="sxs-lookup"><span data-stu-id="e576f-178">Interact with the current webpage in the browser</span></span>  

<span data-ttu-id="e576f-179">La **consola** tiene acceso al [objeto Window][MdnDocsWebApiWindow] del explorador.</span><span class="sxs-lookup"><span data-stu-id="e576f-179">The **Console** has access to the [Window][MdnDocsWebApiWindow] object of the browser.</span></span>  <span data-ttu-id="e576f-180">Puede escribir scripts que interactúen con la página web actual.</span><span class="sxs-lookup"><span data-stu-id="e576f-180">You can write scripts that interact with the current webpage.</span></span>  <span data-ttu-id="e576f-181">Para probarlo, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e576f-181">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="e576f-182">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e576f-182">Open the **Console**.</span></span>  
1.  <span data-ttu-id="e576f-183">Copie y pegue el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="e576f-183">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    document.querySelector('h1').innerHTML
    ```  
    
:::image type="complex" source="../media/console-intro-reading-DOM.msft.png" alt-text="Copiar el contenido del encabezado superior (h1) del DOM y mostrarlo en la consola" lightbox="../media/console-intro-reading-DOM.msft.png":::
   <span data-ttu-id="e576f-185">Copiar el encabezado superior \( `h1` \) contenido del DOM y mostrarlo en la **consola**</span><span class="sxs-lookup"><span data-stu-id="e576f-185">Copy the top heading \(`h1`\) content from the DOM and display in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="e576f-186">En lugar de solo leer desde la página web, también puedes cambiarla.</span><span class="sxs-lookup"><span data-stu-id="e576f-186">Instead of only reading from the webpage, you can also change it.</span></span>  <span data-ttu-id="e576f-187">Para intentar cambiar la página web, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e576f-187">To try changing the webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="e576f-188">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e576f-188">Open the **Console**.</span></span>  
1.  <span data-ttu-id="e576f-189">Copie y pegue el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="e576f-189">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    document.querySelector('h1').innerHTML = 'Rocking the Console';
    ```  
    
:::image type="complex" source="../media/console-intro-wrtiting-DOM.msft.png" alt-text="Escribir texto en el DOM en la consola" lightbox="../media/console-intro-wrtiting-DOM.msft.png":::
   <span data-ttu-id="e576f-191">Escribir texto en el DOM en la **consola**</span><span class="sxs-lookup"><span data-stu-id="e576f-191">Write text to the DOM in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="e576f-192">Ha cambiado el encabezado principal de la página web a **Rocking the Console**.</span><span class="sxs-lookup"><span data-stu-id="e576f-192">You changed the main heading of the webpage to **Rocking the Console**.</span></span>  <span data-ttu-id="e576f-193">Los **métodos de utilidad de** consola facilita el acceso y la manipulación de la página web actual.</span><span class="sxs-lookup"><span data-stu-id="e576f-193">The **Console Utility** methods make it easy to access and manipulate the current webpage.</span></span>  <span data-ttu-id="e576f-194">Para obtener más información, vaya a [Console Utilities API reference][DevtoolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="e576f-194">For more information, navigate to [Console Utilities API reference][DevtoolsConsoleUtilities].</span></span>  <span data-ttu-id="e576f-195">Por ejemplo, para agregar un borde verde alrededor de todos los vínculos de la página web actual, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e576f-195">For example, to add a green border around all the links in the current webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="e576f-196">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e576f-196">Open the **Console**.</span></span>  
1.  <span data-ttu-id="e576f-197">Copie y pegue el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="e576f-197">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    $$('a').forEach(a => a.style.border='1px solid lime');
    ```  
    
:::image type="complex" source="../media/console-intro-changing-styles.msft.png" alt-text="Manipular una selección de elementos mediante la consola" lightbox="../media/console-intro-changing-styles.msft.png":::
    <span data-ttu-id="e576f-199">Manipular una selección de elementos mediante la **consola**</span><span class="sxs-lookup"><span data-stu-id="e576f-199">Manipulate a selection of elements using the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="e576f-200">Para obtener más información sobre cómo trabajar con el DOM, vaya [a Usar la consola para interactuar con el DOM][DevtoolsConsoleConsoleDomInteraction].</span><span class="sxs-lookup"><span data-stu-id="e576f-200">For more information about working with the DOM, navigate to [Use the Console to interact with the DOM][DevtoolsConsoleConsoleDomInteraction].</span></span>  

## <a name="learn-more-about-console"></a><span data-ttu-id="e576f-201">Más información sobre la consola</span><span class="sxs-lookup"><span data-stu-id="e576f-201">Learn more about Console</span></span>  

<span data-ttu-id="e576f-202">Para obtener más información acerca de **console**, vaya a [Console reference][DevtoolsConsoleReference], Console Utilities [API reference][DevtoolsConsoleUtilities]y Console [API reference][DevtoolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="e576f-202">For more information about the **Console**, navigate to [Console reference][DevtoolsConsoleReference], [Console Utilities API reference][DevtoolsConsoleUtilities], and [Console API reference][DevtoolsConsoleApi].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="e576f-203">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e576f-203">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  
[DevtoolsConsoleApi]: ./api.md "Referencia de api de consola | Microsoft Docs"  
[DevtoolsConsoleConsoleDebugJavascript]: ./console-debug-javascript.md "Errores de depuración notificados en la consola | Microsoft Docs"  
[DevtoolsConsoleConsoleDomInteraction]: ./console-dom-interaction.md "Use la consola para interactuar con el dom | Microsoft Docs" 
[DevtoolsConsoleConsoleFilters]: ./console-filters.md "Filtrar mensajes de consola | Microsoft Docs"  
[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Consola como entorno de JavaScript | Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Registrar mensajes en la herramienta consola | Microsoft Docs"  
[DevtoolsConsoleReference]: ./reference.md "Referencia de consola | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Referencia de api de utilidades de consola | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas | Microsoft Docs"  
<!-- external links -->
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-demo.html "Ejemplos de mensajes de consola: registro, información, error y advertencia | GitHub"  
[MdnDocsWebApiWindow]: https://developer.mozilla.org/docs/Web/API/Window "Ventana | MDN"  
[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Bucle read–eval–print | Wikipedia"  

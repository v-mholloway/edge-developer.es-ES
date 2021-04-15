---
description: Una introducción a la herramienta consola dentro de Microsoft Edge Developer Tools.
title: Usar la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 3f2f8c01a9bc9c4f40158f0959ba5b60e03bfb80
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483243"
---
# <a name="use-the-console"></a><span data-ttu-id="e9bde-104">Usar la consola</span><span class="sxs-lookup"><span data-stu-id="e9bde-104">Use the Console</span></span>  

<span data-ttu-id="e9bde-105">La **herramienta Consola** de DevTools le ayuda con varias tareas.</span><span class="sxs-lookup"><span data-stu-id="e9bde-105">The **Console** tool of the DevTools helps you with several tasks.</span></span>  <span data-ttu-id="e9bde-106">La siguiente lista incluye algunas de las tareas.</span><span class="sxs-lookup"><span data-stu-id="e9bde-106">The following list includes some of the tasks.</span></span>  

*   <span data-ttu-id="e9bde-107">Descubra por qué algo no funciona en el proyecto actual y [realice un seguimiento de los problemas][DevtoolsConsoleConsoleDebugJavascript].</span><span class="sxs-lookup"><span data-stu-id="e9bde-107">Find out why something isn't working in the current project and [track down problems][DevtoolsConsoleConsoleDebugJavascript].</span></span>  
*   <span data-ttu-id="e9bde-108">[Obtenga información sobre el proyecto web en][DevtoolsConsoleConsoleFilters] el explorador como mensajes de registro.</span><span class="sxs-lookup"><span data-stu-id="e9bde-108">[Get information about the web project][DevtoolsConsoleConsoleFilters] in the browser as log messages.</span></span>  
*   <span data-ttu-id="e9bde-109">[Información de registro][DevtoolsConsoleConsoleLog] en scripts con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="e9bde-109">[Log information][DevtoolsConsoleConsoleLog] in scripts for debugging purposes.</span></span>  
*   <span data-ttu-id="e9bde-110">[Pruebe las expresiones de JavaScript][DevtoolsConsoleConsoleJavascript] en un [entorno REPL.][WikiReadEvalPrintLoop]</span><span class="sxs-lookup"><span data-stu-id="e9bde-110">[Try JavaScript expressions][DevtoolsConsoleConsoleJavascript] live in a [REPL][WikiReadEvalPrintLoop] environment.</span></span>  
*   <span data-ttu-id="e9bde-111">[Interactúe con el proyecto web en el explorador][DevtoolsConsoleConsoleDomInteraction] con JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e9bde-111">[Interact with the web project in the browser][DevtoolsConsoleConsoleDomInteraction] using JavaScript.</span></span>  
    
<span data-ttu-id="e9bde-112">La **consola** es una excelente herramienta complementaria para usarla con otras herramientas.</span><span class="sxs-lookup"><span data-stu-id="e9bde-112">The **Console** is a great companion tool to use with others tools.</span></span>  <span data-ttu-id="e9bde-113">La **consola** proporciona una forma eficaz de crear scripts de funcionalidad, inspeccionar y manipular la página web actual mediante JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e9bde-113">The **Console** provides a powerful way to script functionality, inspect, and manipulate the current webpage using JavaScript.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-main.msft.png" alt-text="La herramienta Consola abierta en el panel superior" lightbox="../media/console-intro-console-main.msft.png":::
         <span data-ttu-id="e9bde-115">La **herramienta Consola** abierta en el panel superior</span><span class="sxs-lookup"><span data-stu-id="e9bde-115">The **Console** tool open in the upper panel</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-intro-console-panel.msft.png" alt-text="Consola en el panel inferior con la herramienta Elementos abierta encima de ella" lightbox="../media/console-intro-console-panel.msft.png":::
         <span data-ttu-id="e9bde-117">**Consola** en el panel inferior con la **herramienta Elementos** abierta encima de ella</span><span class="sxs-lookup"><span data-stu-id="e9bde-117">**Console** in the lower panel with the **Elements** tool open above it</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="e9bde-118">La forma más rápida de abrir directamente la **consola** es `Control` + `Shift` + `J` seleccionar \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="e9bde-118">The fastest way to directly open the **Console** is to select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

## <a name="error-reports-and-console"></a><span data-ttu-id="e9bde-119">Informes de errores y consola</span><span class="sxs-lookup"><span data-stu-id="e9bde-119">Error reports and Console</span></span>  

<span data-ttu-id="e9bde-120">**La** consola es el lugar predeterminado donde se notifican los errores de conectividad y JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e9bde-120">**Console** is the default place where JavaScript and connectivity errors are reported.</span></span>  <span data-ttu-id="e9bde-121">Si se produce algún error, se muestra un botón junto al icono **Configuración** de DevTools que proporciona el número de errores y advertencias.</span><span class="sxs-lookup"><span data-stu-id="e9bde-121">If any errors occur, a button displays next to the **Settings** icon in DevTools that provides the number of errors and warnings.</span></span>  <span data-ttu-id="e9bde-122">Elija para abrir la **consola y** mostrar el problema.</span><span class="sxs-lookup"><span data-stu-id="e9bde-122">Choose it to open the **Console** and display the problem.</span></span>  <span data-ttu-id="e9bde-123">Para obtener más información, vaya [a Depurar errores notificados en consola][DevtoolsConsoleConsoleDebugJavascript].</span><span class="sxs-lookup"><span data-stu-id="e9bde-123">For more information, navigate to [Debug errors reported in Console][DevtoolsConsoleConsoleDebugJavascript].</span></span>  

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="DevTools proporciona información detallada sobre el error en la consola" lightbox="../media/console-debug-displays-error.msft.png":::
   <span data-ttu-id="e9bde-125">DevTools proporciona información detallada sobre el error en la **consola**</span><span class="sxs-lookup"><span data-stu-id="e9bde-125">DevTools gives detailed information about the error in the **Console**</span></span>  
:::image-end:::  

## <a name="inspect-and-filter-information-on-the-current-webpage"></a><span data-ttu-id="e9bde-126">Inspeccionar y filtrar información en la página web actual</span><span class="sxs-lookup"><span data-stu-id="e9bde-126">Inspect and filter information on the current webpage</span></span>  

<span data-ttu-id="e9bde-127">Al abrir DevTools en una página web, es probable que muestre un auge de la información registrada en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e9bde-127">When you open the DevTools on a webpage, you're likely to display a deluge of information logged to the **Console**.</span></span>  <span data-ttu-id="e9bde-128">La cantidad de información se convierte en un problema cuando necesita identificar información importante.</span><span class="sxs-lookup"><span data-stu-id="e9bde-128">The amount of information becomes a problem when you need to identify important information.</span></span>  <span data-ttu-id="e9bde-129">Para ver la información importante que necesita acción, use la [herramienta Problemas][DevtoolsIssuesIndex] en DevTools.</span><span class="sxs-lookup"><span data-stu-id="e9bde-129">To view the important information that needs action, use the [Issues][DevtoolsIssuesIndex] tool in DevTools.</span></span>  <span data-ttu-id="e9bde-130">Gran parte del ruido permanece, por lo que es una buena idea conocer las opciones automatizadas de registro y [filtro][DevtoolsConsoleConsoleFilters] en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e9bde-130">Much of the noise remains, which is why it's a good idea to know about the [automated log and filter options][DevtoolsConsoleConsoleFilters] in the **Console**.</span></span>  

:::image type="complex" source="../media/console-intro-noise.msft.png" alt-text="DevTools con una consola llena de mensajes" lightbox="../media/console-intro-noise.msft.png":::
   <span data-ttu-id="e9bde-132">DevTools con una **consola llena** de mensajes</span><span class="sxs-lookup"><span data-stu-id="e9bde-132">DevTools with a **Console** full of messages</span></span>  
:::image-end:::  

## <a name="log-information-to-display-in-the-console"></a><span data-ttu-id="e9bde-133">Información de registro que se mostrará en la consola</span><span class="sxs-lookup"><span data-stu-id="e9bde-133">Log information to display in the Console</span></span>  

<span data-ttu-id="e9bde-134">El caso de uso más popular para la **consola** es registrar información de los scripts mediante el `console.log()` método u otros métodos similares.</span><span class="sxs-lookup"><span data-stu-id="e9bde-134">The most popular use case for the **Console** is logging information from your scripts using the `console.log()` method or other similar methods.</span></span>  <span data-ttu-id="e9bde-135">Para probarlo, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e9bde-135">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="e9bde-136">Para abrir **consola,** seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="e9bde-136">To open **Console**, select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\).</span></span>  
1.  <span data-ttu-id="e9bde-137">Vaya a [Ejemplos de mensajes de consola: registro, información, error][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]y advertencia, o copie y ejecute el siguiente fragmento de código en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e9bde-137">Navigate to [Console messages examples: log, info, error and warn][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml], or copy and run the following code snippet in the **Console**.</span></span>  
    
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
    
1.  <span data-ttu-id="e9bde-138">La **consola** muestra los resultados.</span><span class="sxs-lookup"><span data-stu-id="e9bde-138">The **Console** displays the results.</span></span>  
    
    :::image type="complex" source="../media/console-intro-logging.msft.png" alt-text="Consola llena de mensajes causados por código de demostración" lightbox="../media/console-intro-logging.msft.png":::
       <span data-ttu-id="e9bde-140">**Consola** llena de mensajes causados por código de demostración</span><span class="sxs-lookup"><span data-stu-id="e9bde-140">**Console** full of messages caused by demo code</span></span>  
    :::image-end:::  
    
<span data-ttu-id="e9bde-141">Hay muchos métodos útiles disponibles cuando se trabaja con la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e9bde-141">Many useful methods are available when you work with the **Console**.</span></span>  <span data-ttu-id="e9bde-142">Para obtener más información, vaya [a Registrar mensajes en la herramienta Consola][DevtoolsConsoleConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="e9bde-142">For more information, navigate to [Log messages in the Console tool][DevtoolsConsoleConsoleLog].</span></span>  

## <a name="try-your-javascript-live-in-the-console"></a><span data-ttu-id="e9bde-143">Pruebe JavaScript en directo en la consola</span><span class="sxs-lookup"><span data-stu-id="e9bde-143">Try your JavaScript live in the Console</span></span>  

<span data-ttu-id="e9bde-144">La **consola** no es solo un lugar para registrar información.</span><span class="sxs-lookup"><span data-stu-id="e9bde-144">The **Console** isn't only a place to log information.</span></span>  <span data-ttu-id="e9bde-145">La **consola** es un [entorno REPL.][WikiReadEvalPrintLoop]</span><span class="sxs-lookup"><span data-stu-id="e9bde-145">The **Console** is a [REPL][WikiReadEvalPrintLoop] environment.</span></span>  <span data-ttu-id="e9bde-146">Al escribir cualquier JavaScript en la **consola,** el código se ejecuta inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="e9bde-146">When you write any JavaScript in the **Console**, the code runs immediately.</span></span>  <span data-ttu-id="e9bde-147">Puede resultar útil probar algunas nuevas características de JavaScript o realizar algunos cálculos rápidos.</span><span class="sxs-lookup"><span data-stu-id="e9bde-147">You may find it useful to test some new JavaScript features or to do some quick calculations.</span></span>  <span data-ttu-id="e9bde-148">Además, obtiene todas las características que espera de un entorno de edición moderno, como la autocompleción, el resaltado de sintaxis y el historial.</span><span class="sxs-lookup"><span data-stu-id="e9bde-148">Also, you get all of the features you expect from a modern editing environment, such as autocompletion, syntax highlighting, and history.</span></span>  <span data-ttu-id="e9bde-149">Para probarlo, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e9bde-149">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="e9bde-150">Vaya a la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e9bde-150">Navigate to the **Console**.</span></span>  
1.  <span data-ttu-id="e9bde-151">Escriba `2 + 2`.</span><span class="sxs-lookup"><span data-stu-id="e9bde-151">Type `2 + 2`.</span></span>  
    
<span data-ttu-id="e9bde-152">La **consola** muestra el resultado `4` en la siguiente línea.</span><span class="sxs-lookup"><span data-stu-id="e9bde-152">The **Console** displays the result `4` on the following line.</span></span>  <span data-ttu-id="e9bde-153">Esta **característica de evaluación** de Eager es útil para depurar y comprobar que no está cometiendo errores en el código.</span><span class="sxs-lookup"><span data-stu-id="e9bde-153">This **Eager evaluation** feature is useful to debug and verify that you aren't making mistakes in your code.</span></span>  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="La consola muestra el resultado de 2 + 2 en directo a medida que lo escribe" lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   <span data-ttu-id="e9bde-155">La **consola** muestra el resultado de `2 + 2` live al escribirlo</span><span class="sxs-lookup"><span data-stu-id="e9bde-155">The **Console** displays the result of `2 + 2` live as you type it</span></span>  
:::image-end:::  

<span data-ttu-id="e9bde-156">Para ejecutar la expresión JavaScript en la **consola** y, opcionalmente, mostrar un resultado, seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e9bde-156">To run the JavaScript expression in the **Console** and optionally display a result, select `Enter`.</span></span>  <span data-ttu-id="e9bde-157">A continuación, puede escribir el siguiente código JavaScript que se ejecutará en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e9bde-157">Then, you may write the next JavaScript code to run in the **Console**.</span></span>  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Ejecutar varias líneas de código JavaScript sucesivamente" lightbox="../media/console-javascript-several-expressions.msft.png":::
   <span data-ttu-id="e9bde-159">Ejecutar varias líneas de código JavaScript sucesivamente</span><span class="sxs-lookup"><span data-stu-id="e9bde-159">Run several lines of JavaScript code in succession</span></span>  
:::image-end:::  

<span data-ttu-id="e9bde-160">De forma predeterminada, se ejecuta código JavaScript en una sola línea.</span><span class="sxs-lookup"><span data-stu-id="e9bde-160">By default, you run JavaScript code on a single line.</span></span>  <span data-ttu-id="e9bde-161">Para ejecutar una línea, escriba JavaScript y, a continuación, seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e9bde-161">To run a line, type your JavaScript and then select `Enter`.</span></span>  <span data-ttu-id="e9bde-162">Para evitar la limitación de una sola línea, seleccione `Shift` + `Enter` en lugar de `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e9bde-162">To work around the single-line limitation, select `Shift`+`Enter` instead of `Enter`.</span></span>  <span data-ttu-id="e9bde-163">De forma similar a otras experiencias de línea de comandos, para obtener acceso a los comandos de JavaScript anteriores, seleccione `Arrow-Up` .</span><span class="sxs-lookup"><span data-stu-id="e9bde-163">Similar to other command-line experiences, to access your previous JavaScript commands, select `Arrow-Up`.</span></span>  <span data-ttu-id="e9bde-164">La característica de autocompletion de **la consola** es una excelente manera de obtener información sobre métodos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="e9bde-164">The autocompletion feature of the **Console** is a great way to learn about unfamiliar methods.</span></span>  <span data-ttu-id="e9bde-165">Para probarlo, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e9bde-165">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="e9bde-166">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e9bde-166">Open the **Console**.</span></span>  
1.  <span data-ttu-id="e9bde-167">Escriba `doc`.</span><span class="sxs-lookup"><span data-stu-id="e9bde-167">Type `doc`.</span></span>  
1.  <span data-ttu-id="e9bde-168">Elija `document` en el menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="e9bde-168">Choose `document` from the dropdown menu.</span></span>  
1.  <span data-ttu-id="e9bde-169">Seleccione la `tab` clave para elegirla.</span><span class="sxs-lookup"><span data-stu-id="e9bde-169">Select the `tab` key to choose it.</span></span>  
1.  <span data-ttu-id="e9bde-170">Escriba `.bo`.</span><span class="sxs-lookup"><span data-stu-id="e9bde-170">Type `.bo`.</span></span>  
1.  <span data-ttu-id="e9bde-171">Seleccione `tab` para obtener `document.body` .</span><span class="sxs-lookup"><span data-stu-id="e9bde-171">Select `tab` to get `document.body`.</span></span>  
1.  <span data-ttu-id="e9bde-172">Escriba otro `.` para mostrar la lista completa de propiedades y métodos disponibles en el cuerpo de la página web actual.</span><span class="sxs-lookup"><span data-stu-id="e9bde-172">Type another `.` to display the complete list of properties and methods available on the body of the current webpage.</span></span>  
    
<span data-ttu-id="e9bde-173">Para obtener más información acerca de todas las formas de trabajar con **la consola,** vaya [a Consola como un entorno JavaScript][DevtoolsConsoleConsoleJavascript].</span><span class="sxs-lookup"><span data-stu-id="e9bde-173">For more information about all the ways to work with **Console**, navigate to [Console as a JavaScript environment][DevtoolsConsoleConsoleJavascript].</span></span>  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Autocompletion de consola de expresiones de JavaScript" lightbox="../media/console-javascript-autocomplete.msft.png":::
   <span data-ttu-id="e9bde-175">**Autocompletion** de consola de expresiones de JavaScript</span><span class="sxs-lookup"><span data-stu-id="e9bde-175">**Console** autocompletion of JavaScript expressions</span></span>  
:::image-end:::  

## <a name="interact-with-the-current-webpage-in-the-browser"></a><span data-ttu-id="e9bde-176">Interactuar con la página web actual en el explorador</span><span class="sxs-lookup"><span data-stu-id="e9bde-176">Interact with the current webpage in the browser</span></span>  

<span data-ttu-id="e9bde-177">La **consola** tiene acceso al [objeto Window][MdnDocsWebApiWindow] del explorador.</span><span class="sxs-lookup"><span data-stu-id="e9bde-177">The **Console** has access to the [Window][MdnDocsWebApiWindow] object of the browser.</span></span>  <span data-ttu-id="e9bde-178">Puede escribir scripts que interactúen con la página web actual.</span><span class="sxs-lookup"><span data-stu-id="e9bde-178">You may write scripts that interact with the current webpage.</span></span>  <span data-ttu-id="e9bde-179">Para probarlo, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e9bde-179">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="e9bde-180">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e9bde-180">Open the **Console**.</span></span>  
1.  <span data-ttu-id="e9bde-181">Copie y pegue el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="e9bde-181">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    document.querySelector('h1').innerHTML
    ```  
    
:::image type="complex" source="../media/console-intro-reading-DOM.msft.png" alt-text="Copiar el contenido del encabezado superior (h1) del DOM y mostrarlo en la consola" lightbox="../media/console-intro-reading-DOM.msft.png":::
   <span data-ttu-id="e9bde-183">Copiar el encabezado superior \( `h1` \) contenido del DOM y mostrarlo en la **consola**</span><span class="sxs-lookup"><span data-stu-id="e9bde-183">Copy the top heading \(`h1`\) content from the DOM and display in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="e9bde-184">En lugar de solo leer desde la página web, también puede cambiarla.</span><span class="sxs-lookup"><span data-stu-id="e9bde-184">Instead of only reading from the webpage, you may also change it.</span></span>  <span data-ttu-id="e9bde-185">Para probarlo, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e9bde-185">To try it, complete the following actions.</span></span>  

1.  <span data-ttu-id="e9bde-186">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e9bde-186">Open the **Console**.</span></span>  
1.  <span data-ttu-id="e9bde-187">Copie y pegue el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="e9bde-187">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    document.querySelector('h1').innerHTML = 'Rocking the Console';
    ```  
    
:::image type="complex" source="../media/console-intro-wrtiting-DOM.msft.png" alt-text="Escribir texto en el DOM en la consola" lightbox="../media/console-intro-wrtiting-DOM.msft.png":::
   <span data-ttu-id="e9bde-189">Escribir texto en el DOM en la **consola**</span><span class="sxs-lookup"><span data-stu-id="e9bde-189">Write text to the DOM in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="e9bde-190">Ha cambiado el encabezado principal de la página web a **Rocking the Console**.</span><span class="sxs-lookup"><span data-stu-id="e9bde-190">You changed the main heading of the webpage to **Rocking the Console**.</span></span>  <span data-ttu-id="e9bde-191">Los **métodos de utilidad de** consola facilita el acceso y la manipulación de la página web actual.</span><span class="sxs-lookup"><span data-stu-id="e9bde-191">The **Console Utility** methods make it easy to access and manipulate the current webpage.</span></span>  <span data-ttu-id="e9bde-192">Para obtener más información, vaya a [Console Utilities API reference][DevtoolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="e9bde-192">For more information, navigate to [Console Utilities API reference][DevtoolsConsoleUtilities].</span></span>  <span data-ttu-id="e9bde-193">Por ejemplo, para agregar un borde verde alrededor de todos los vínculos de la página web actual, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="e9bde-193">For example, to add a green border around all the links in the current webpage, complete the following actions.</span></span>  

1.  <span data-ttu-id="e9bde-194">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="e9bde-194">Open the **Console**.</span></span>  
1.  <span data-ttu-id="e9bde-195">Copie y pegue el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="e9bde-195">Copy and paste the following code snippet.</span></span>  
    
    ```javascript
    $$('a').forEach(a => a.style.border='1px solid lime');
    ```  
    

:::image type="complex" source="../media/console-intro-changing-styles.msft.png" alt-text="Manipular una selección de elementos mediante la consola" lightbox="../media/console-intro-changing-styles.msft.png":::
    <span data-ttu-id="e9bde-197">Manipular una selección de elementos mediante la **consola**</span><span class="sxs-lookup"><span data-stu-id="e9bde-197">Manipulate a selection of elements using the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="e9bde-198">Para obtener más información sobre cómo trabajar con el DOM, vaya [a Usar la consola para interactuar con el DOM][DevtoolsConsoleConsoleDomInteraction].</span><span class="sxs-lookup"><span data-stu-id="e9bde-198">For more information about working with the DOM, navigate to [Use the Console to interact with the DOM][DevtoolsConsoleConsoleDomInteraction].</span></span>  

## <a name="learn-more-about-console"></a><span data-ttu-id="e9bde-199">Más información sobre la consola</span><span class="sxs-lookup"><span data-stu-id="e9bde-199">Learn more about Console</span></span>  

<span data-ttu-id="e9bde-200">Para obtener más información acerca de **console**, vaya a [Console reference][DevtoolsConsoleReference], Console Utilities [API reference][DevtoolsConsoleUtilities]y Console [API reference][DevtoolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="e9bde-200">For more information about the **Console**, navigate to [Console reference][DevtoolsConsoleReference], [Console Utilities API reference][DevtoolsConsoleUtilities], and [Console API reference][DevtoolsConsoleApi].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="e9bde-201">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e9bde-201">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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

[DevtoolsIssuesIndex]: ../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas de Microsoft Edge DevTools | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingDemoHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-demo.html "Ejemplos de mensajes de consola: registro, información, error y advertencia | GitHub"  

[MdnDocsWebApiWindow]: https://developer.mozilla.org/docs/Web/API/Window "Ventana | MDN"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Bucle read–eval–print | Wikipedia"  

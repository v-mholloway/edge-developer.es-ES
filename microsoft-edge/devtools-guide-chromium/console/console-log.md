---
description: Cómo registrar mensajes y ejecutar JavaScript en la Microsoft Edge DevTools Console.
title: Registrar mensajes en la herramienta consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: d48a48de7b261a628ac99f58680deb119268a980
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483666"
---
# <a name="log-messages-in-the-console-tool"></a><span data-ttu-id="23a39-104">Registrar mensajes en la herramienta consola</span><span class="sxs-lookup"><span data-stu-id="23a39-104">Log messages in the Console tool</span></span>  

<span data-ttu-id="23a39-105">Desde que los exploradores empezaron a ofrecer herramientas para **desarrolladores, la consola** es un favorito.</span><span class="sxs-lookup"><span data-stu-id="23a39-105">Ever since browsers started to offer developer tools, the **Console** is a favorite.</span></span>  <span data-ttu-id="23a39-106">La razón es sencilla.</span><span class="sxs-lookup"><span data-stu-id="23a39-106">The reason is simple.</span></span>  

*   <span data-ttu-id="23a39-107">En la mayoría de los cursos de programación, aprendes a generar algún tipo de comando de impresión para obtener información sobre lo que sucede.</span><span class="sxs-lookup"><span data-stu-id="23a39-107">In most programming courses, you learn to output some kind of print command to gain insights about what happens.</span></span>  

<span data-ttu-id="23a39-108">Antes de DevTools, estaba limitado a una `alert()` instrucción or para depurar en el `document.write()` explorador.</span><span class="sxs-lookup"><span data-stu-id="23a39-108">Before the DevTools, you were limited to an `alert()` or `document.write()` statement to debug in the browser.</span></span>  

<span data-ttu-id="23a39-109">Si desea registrar información en la **consola,** hay muchos métodos disponibles.</span><span class="sxs-lookup"><span data-stu-id="23a39-109">If you want to log information in the **Console**, lots of methods are available to you.</span></span>  <span data-ttu-id="23a39-110">Revise todos los métodos disponibles en la [referencia de api][DevtoolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="23a39-110">Review all of available methods in the [API reference][DevtoolsConsoleApi].</span></span>  <span data-ttu-id="23a39-111">En el siguiente fragmento de código se enumeran los métodos más importantes.</span><span class="sxs-lookup"><span data-stu-id="23a39-111">The following code snippet lists the most important methods.</span></span>  

```javascript
// prints the text to the console as  a log message
console.log('This is a log message')
// prints the text to the console as an informational message
console.info('This is some information') 
// prints the text to the console as an error message
console.error('This is an error')
// prints the text to the console as a warning
console.warn('This is a warning') 
```  

<span data-ttu-id="23a39-112">Copie y pegue el fragmento de código anterior en la **consola** o vaya a Ejemplos de mensajes de [consola: registro, información, error y advertencia][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingExamplesHtml].</span><span class="sxs-lookup"><span data-stu-id="23a39-112">Copy and paste the previous code snippet in the **Console** or navigate to [Console messages examples: log, info, error, and warn][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingExamplesHtml].</span></span>  <span data-ttu-id="23a39-113">Al probar cualquier método en la **consola,** los métodos y parecen hacer lo mismo, mientras que los métodos and muestran un icono junto al mensaje y una forma de inspeccionar el seguimiento de pila del `log()` `info()` `error()` `warn()` mensaje. [][WikiStackTrace]</span><span class="sxs-lookup"><span data-stu-id="23a39-113">When you try any method in the **Console**, the `log()` and `info()` methods seem to do the same thing, while the `error()` and `warn()` methods display an icon next to the message and a way to inspect the [stack trace][WikiStackTrace] of the message.</span></span>  

:::image type="complex" source="../media/console-log-examples.msft.png" alt-text="La consola muestra los mensajes de distintas API de registro" lightbox="../media/console-log-examples.msft.png":::
   <span data-ttu-id="23a39-115">La **consola muestra** los mensajes de distintas API de registro</span><span class="sxs-lookup"><span data-stu-id="23a39-115">The **Console** displays the messages from different log APIs</span></span>  
:::image-end:::  

<span data-ttu-id="23a39-116">Sin embargo, sigue siendo una buena idea usar y para distintas tareas de registro, ya que permite filtrar mediante el tipo `info()` `log()` en la [consola][DevtoolsConsoleConsoleFilters].</span><span class="sxs-lookup"><span data-stu-id="23a39-116">It is, however, still a good idea to use `info()` and `log()` for different log tasks as that allows you to [filter using type in the Console][DevtoolsConsoleConsoleFilters].</span></span>  

## <a name="different-types-of-logs"></a><span data-ttu-id="23a39-117">Distintos tipos de registros</span><span class="sxs-lookup"><span data-stu-id="23a39-117">Different types of logs</span></span>  

<span data-ttu-id="23a39-118">En lugar de texto de registro, puede enviar cualquier referencia válida de JavaScript o DOM a la **consola**.</span><span class="sxs-lookup"><span data-stu-id="23a39-118">Instead of log text you may send any valid JavaScript or DOM references to the **Console**.</span></span>  <span data-ttu-id="23a39-119">La **consola** es elegante y determina el tipo que se envía.</span><span class="sxs-lookup"><span data-stu-id="23a39-119">The **Console** is elegant and it determines the type that you send it.</span></span>  <span data-ttu-id="23a39-120">A continuación, le ofrece la mejor representación posible.</span><span class="sxs-lookup"><span data-stu-id="23a39-120">It then gives you the best possible representation.</span></span>  <span data-ttu-id="23a39-121">Copie y pegue el siguiente fragmento de código en la **consola** o para mostrar los resultados, vaya a Ejemplos de mensajes de [consola: registro de diferentes tipos][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingTypesHtml].</span><span class="sxs-lookup"><span data-stu-id="23a39-121">Copy and paste the following code snippet in the **Console** or to display the results, navigate to [Console messages examples: logging different types][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingTypesHtml].</span></span>  

```javascript
let x = 2;
// logs the value of x
console.log(x);
// logs the name x and value of x
console.log({x})   
// logs a DOM reference  
console.log(document.querySelector('body'));
// logs an Object
console.log({"type":"life", "meaning": 42});
let w3techs = ['HTML', 'CSS', 'SVG', 'MathML'];
// logs an Array
console.log(w3techs);
```  

<span data-ttu-id="23a39-122">Cada resultado se muestra de una manera diferente.</span><span class="sxs-lookup"><span data-stu-id="23a39-122">Each result is displayed in a different way.</span></span>  <span data-ttu-id="23a39-123">Use los triángulos para alternar la información y analizar cada uno con más detalle.</span><span class="sxs-lookup"><span data-stu-id="23a39-123">Use the triangles to toggle the information and analyze each one in more detail.</span></span>  <span data-ttu-id="23a39-124">Los caracteres de llave alrededor de la variable son un buen truco para evitar muchos mensajes de registro en los que solo obtienes un valor, pero no sabes dónde `{}` `x` se originó.</span><span class="sxs-lookup"><span data-stu-id="23a39-124">The curly brace characters `{}` around the `x` variable are a nice little trick to avoid lots of log messages where you only get a value but you don't know where it originated.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-types.msft.png" alt-text="Registrar variables de diferentes tipos en la consola" lightbox="../media/console-log-types.msft.png":::
         <span data-ttu-id="23a39-126">Registrar variables de diferentes tipos en la **consola**</span><span class="sxs-lookup"><span data-stu-id="23a39-126">Log variables of different types in the **Console**</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-types-expanded.msft.png" alt-text="Registrar variables de diferentes tipos en la consola con información adicional expandida" lightbox="../media/console-log-types-expanded.msft.png":::
         <span data-ttu-id="23a39-128">Registrar variables de diferentes tipos en la **consola con** información adicional expandida</span><span class="sxs-lookup"><span data-stu-id="23a39-128">Log variables of different types in the **Console** with expanded extra information</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="format-and-convert-values-with-specifiers"></a><span data-ttu-id="23a39-129">Dar formato y convertir valores con especificadores</span><span class="sxs-lookup"><span data-stu-id="23a39-129">Format and convert values with specifiers</span></span>

<span data-ttu-id="23a39-130">Una característica especial de todos los métodos de registro es que puede usar especificadores en el mensaje de registro.</span><span class="sxs-lookup"><span data-stu-id="23a39-130">A special feature of all the log methods is that you may use specifiers in your log message.</span></span>  <span data-ttu-id="23a39-131">Los especificadores forman parte de un mensaje de registro y comienzan con un signo de porcentaje \( \) carácter y permiten registrar determinados valores en diferentes formatos e incluso `%` convertir cada uno.</span><span class="sxs-lookup"><span data-stu-id="23a39-131">Specifiers are part of a log message and start with a percentage sign \(`%`\) character and allow you to log certain values in different formats and even convert each.</span></span>  

*   `%s` <span data-ttu-id="23a39-132">registros como cadenas</span><span class="sxs-lookup"><span data-stu-id="23a39-132">logs as Strings</span></span>
*   `%i` <span data-ttu-id="23a39-133">o `%d` registros como enteros</span><span class="sxs-lookup"><span data-stu-id="23a39-133">or `%d` logs as Integers</span></span>
*   `%f` <span data-ttu-id="23a39-134">registros como un valor de punto flotante</span><span class="sxs-lookup"><span data-stu-id="23a39-134">logs as a floating-point value</span></span>
*   `%o` <span data-ttu-id="23a39-135">registros como un elemento DOM expandible</span><span class="sxs-lookup"><span data-stu-id="23a39-135">logs as an expandable DOM element</span></span>
*   `%O` <span data-ttu-id="23a39-136">registros como un objeto JavaScript expandible</span><span class="sxs-lookup"><span data-stu-id="23a39-136">logs as an expandable JavaScript object</span></span>
*   `%c` <span data-ttu-id="23a39-137">le permite dar estilo al mensaje con CSS</span><span class="sxs-lookup"><span data-stu-id="23a39-137">allows you to style you message with CSS</span></span>

```javascript
// logs "10x console developer"
console.log('%ix %s developer', 10, 'console');
// logs PI => 3.141592653589793
console.log(Math.PI); 
// logs PI as an integer = 3
console.log('%i', Math.PI); 
// logs the webpage body as a DOM node
console.log('%o', document.body); 
// logs the body of the webpage as a JavaScript object with all properties
console.log('%O', document.body); 
// Displays the message as red and big
console.log('%cImportant message follows','color:red;font-size:40px');
```  

<span data-ttu-id="23a39-138">En el primer ejemplo se muestra que el orden de reemplazo de los especificadores es el orden de parámetro que sigue a la cadena.</span><span class="sxs-lookup"><span data-stu-id="23a39-138">The first example displays that the order of replacement of specifiers is the parameter order following the string.</span></span>  <span data-ttu-id="23a39-139">Para mostrar los resultados, copie y \*\*\*\* pegue el fragmento de código anterior en la consola o vaya a Ejemplos de mensajes de [consola: Registro con especificadores][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithSpecifiersHtml].</span><span class="sxs-lookup"><span data-stu-id="23a39-139">To display the results, copy and paste the previous code snippet in the **Console** or navigate to [Console messages examples: Logging with specifiers][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithSpecifiersHtml].</span></span>  <span data-ttu-id="23a39-140">Expanda la información del registro para mostrar la gran diferencia entre `%o` y `%O` .</span><span class="sxs-lookup"><span data-stu-id="23a39-140">Expand the information in the log to display the huge difference between `%o` and `%O`.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-specifiers.msft.png" alt-text="Usar especificadores para registrar y convertir valores" lightbox="../media/console-log-specifiers.msft.png":::
         <span data-ttu-id="23a39-142">Usar especificadores para registrar y convertir valores</span><span class="sxs-lookup"><span data-stu-id="23a39-142">Use specifiers to log and convert values</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-specifiers-expanded.msft.png" alt-text="Expandir los resultados muestra la diferencia entre el %O y %o especificador: el cuerpo se muestra como un nodo DOM expandible o como una lista completa de todas las propiedades de JavaScript en el cuerpo de la página web" lightbox="../media/console-log-specifiers-expanded.msft.png":::
        <span data-ttu-id="23a39-144">Expandir los resultados muestra la diferencia entre el especificador y: el cuerpo se muestra como un nodo DOM expandible o como una lista completa de todas las propiedades de JavaScript en el cuerpo de `%O` `%o` la página web</span><span class="sxs-lookup"><span data-stu-id="23a39-144">Expand the results displays the difference between the `%O` and `%o` specifier - the body is either displayed as an expandable DOM node or as a full list of all JavaScript properties on the webpage body</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="group-log-messages"></a><span data-ttu-id="23a39-145">Mensajes de registro de grupo</span><span class="sxs-lookup"><span data-stu-id="23a39-145">Group log messages</span></span>

<span data-ttu-id="23a39-146">Si registra mucha información, puede usar los métodos and para mostrar los mensajes de registro como grupos `group` `groupCollapsed` expandibles y contraibles en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="23a39-146">If you log much information, you may use the `group` and `groupCollapsed` methods to display log messages as expandable and collapsible groups in the **Console**.</span></span>  <span data-ttu-id="23a39-147">Es posible que los grupos se anidan y se nombren para que los datos sean mucho más fáciles de comprender.</span><span class="sxs-lookup"><span data-stu-id="23a39-147">Groups may be nested and named to make the data much easier to understand.</span></span>  

```javascript
console.group("Passengers: Heart of Gold");
console.log('Zaphod');
console.log('Trillian');
console.log('Ford');
console.log('Arthur');
console.log('Marvin');
console.groupCollapsed("Hidden");
console.log('(Frankie & Benjy)');
console.groupEnd("Hidden");
console.groupEnd("Passengers: Heart of Gold");

let technologies = {
  "Standards": ["HTML", "CSS", "SVG", "ECMAScript"],
  "Others": ["jQuery", "Markdown", "Textile", "Sass", "Pug"]
}
for (tech in technologies) {
  console.groupCollapsed(tech);
  technologies[tech].forEach(t => console.log(t));
  console.groupEnd(tech);
}
```  

<span data-ttu-id="23a39-148">También en el segundo ejemplo, los nombres de grupo se pueden generar opcionalmente.</span><span class="sxs-lookup"><span data-stu-id="23a39-148">Also in the second example, the group names may be optionally generated.</span></span>  <span data-ttu-id="23a39-149">Para mostrar los resultados, copie y \*\*\*\* pegue el fragmento de código anterior en la consola o vaya a Ejemplos de mensajes de [consola: agrupación de registros][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithGroupsHtml].</span><span class="sxs-lookup"><span data-stu-id="23a39-149">To display the results, copy and paste the previous code snippet in the **Console** or navigate to [Console messages examples: grouping logs][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithGroupsHtml].</span></span>  <span data-ttu-id="23a39-150">Puede expandir y contraer cada una de las secciones.</span><span class="sxs-lookup"><span data-stu-id="23a39-150">You may expand and collapse each of the sections.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-groups.msft.png" alt-text="Registrar muchos valores como grupos" lightbox="../media/console-log-groups.msft.png":::
         <span data-ttu-id="23a39-152">Registrar muchos valores como grupos</span><span class="sxs-lookup"><span data-stu-id="23a39-152">Log lots of values as groups</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-groups-expanded.msft.png" alt-text="Cada grupo puede expandirse y contraerse" lightbox="../media/console-log-groups-expanded.msft.png":::
        <span data-ttu-id="23a39-154">Cada grupo puede expandirse y contraerse</span><span class="sxs-lookup"><span data-stu-id="23a39-154">Each group may be expanded and collapsed</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="display-complex-data-as-tables"></a><span data-ttu-id="23a39-155">Mostrar datos complejos como tablas</span><span class="sxs-lookup"><span data-stu-id="23a39-155">Display complex data as tables</span></span>  

<span data-ttu-id="23a39-156">El método registra datos complejos no como un objeto que se puede contraer y expandir, sino como una tabla que puede `console.table()` ordenar con distintos encabezados.</span><span class="sxs-lookup"><span data-stu-id="23a39-156">The `console.table()` method logs complex data not as a collapsible and expandable object, but as a table that you may sort using different headers.</span></span>  <span data-ttu-id="23a39-157">Una tabla ordenada facilita a los usuarios revisar la información.</span><span class="sxs-lookup"><span data-stu-id="23a39-157">A sorted table makes it much easier for people to review the information.</span></span>  <span data-ttu-id="23a39-158">Para mostrarlo en un ejemplo, vaya a [Ejemplos de mensajes de consola: Uso de tabla][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithTableHtml].</span><span class="sxs-lookup"><span data-stu-id="23a39-158">To display it in an example, navigate to [Console messages examples: Using table][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithTableHtml].</span></span>

```javascript
let technologies = {
  "Standards": ["HTML", "CSS", "SVG", "ECMAScript"],
  "Others": ["jQuery", "Markdown", "Textile", "Sass", "Pug"]
}
// log technologies as an object
console.log(technologies);
// display technologies as a table
console.table(technologies);

// get the dimensions of the webpage body
let bodyDimensions = document.body.getBoundingClientRect();
// display dimensions as an object
console.log(bodyDimensions);
// display dimensions as a table
console.table(bodyDimensions);
```  

:::image type="complex" source="../media/console-log-table.msft.png" alt-text="Mostrar datos con console.table para facilitar la lectura" lightbox="../media/console-log-table.msft.png":::
   <span data-ttu-id="23a39-160">Mostrar datos `console.table` con para facilitar la lectura</span><span class="sxs-lookup"><span data-stu-id="23a39-160">Display data with `console.table` to make it much easier to read</span></span>
:::image-end:::  

<span data-ttu-id="23a39-161">El resultado de tiene un formato de tabla no solo `console.table` cuando se muestra en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="23a39-161">The output of `console.table` has a table format not only when it displays in the **Console**.</span></span>    <span data-ttu-id="23a39-162">Por ejemplo, si copia y pega una tabla en Excel, Word o cualquier otro producto que admita datos tabulares, la estructura permanece intacta.</span><span class="sxs-lookup"><span data-stu-id="23a39-162">For example, if you copy and paste a table into Excel, Word, or any other product that supports tabular data, the structure remains intact.</span></span>  

<!--  The output of `console.table` has a table format not only when it displays in the **Console**.  For example, copy and paste a table in Excel, Word, or any other products that support tabular data.  -->  

<span data-ttu-id="23a39-163">Si los datos tienen parámetros con nombre, el método también permite especificar una de las columnas para que cada propiedad se muestre `console.table()` `Array` como un segundo parámetro.</span><span class="sxs-lookup"><span data-stu-id="23a39-163">If the data has named parameters, the `console.table()` method also allows you to specify an `Array` of columns for each property to display as a second parameter.</span></span>  <span data-ttu-id="23a39-164">En el ejemplo siguiente se muestra cómo especificar una matriz de columnas que sea más legible.</span><span class="sxs-lookup"><span data-stu-id="23a39-164">The following example displays how to specify an array of columns that is more readable.</span></span>  

```javascript
// get all the h1, p and script elements 
let contentElements = document.querySelectorAll(':is(h1,p,script)');
// display the elements as an unfiltered table 
console.table(contentElements)
// display only relevant columns 
console.table(contentElements,['nodeName', 'innerText', 'offsetHeight'])
```  

:::image type="complex" source="../media/console-log-table-filtered.msft.png" alt-text="Filtrar información que console.table muestra y proporcionar una matriz de propiedades para mostrar como segundo parámetro" lightbox="../media/console-log-table-filtered.msft.png":::
   <span data-ttu-id="23a39-166">Filtrar información que `console.table` muestra y proporciona una matriz de propiedades para mostrar como segundo parámetro</span><span class="sxs-lookup"><span data-stu-id="23a39-166">Filter information that `console.table` displays and provide an array of properties to display as a second parameter</span></span>  
:::image-end:::  

<span data-ttu-id="23a39-167">Puede que tenga la tentación de usar los métodos de registro como medio principal para depurar páginas web, ya que los métodos de registro son fáciles de usar.</span><span class="sxs-lookup"><span data-stu-id="23a39-167">You may be tempted to use the log methods as your main means to debug webpages, because log methods are simple to use.</span></span>  <span data-ttu-id="23a39-168">Tenga en cuenta el resultado de cualquier `console.log()` solicitud.</span><span class="sxs-lookup"><span data-stu-id="23a39-168">Consider the result of any `console.log()` request.</span></span>  <span data-ttu-id="23a39-169">Los productos live no deben usar ningún registro que se usó para depurar.</span><span class="sxs-lookup"><span data-stu-id="23a39-169">Live products shouldn't use any log that was used to debug.</span></span>  <span data-ttu-id="23a39-170">Puede revelar información interna a las personas.</span><span class="sxs-lookup"><span data-stu-id="23a39-170">It may reveal inside information to people.</span></span>  <span data-ttu-id="23a39-171">Y el ruido creado en la **consola es** abrumador.</span><span class="sxs-lookup"><span data-stu-id="23a39-171">And the noise created in the **Console** is overwhelming.</span></span>  <span data-ttu-id="23a39-172">Al usar la [depuración de puntos de][DevtoolsJavascriptBreakpoints] interrupción o [expresiones][DevtoolsConsoleLiveExpressions]en directo, puede encontrar que los flujos de trabajo son más eficaces y obtiene mejores resultados.</span><span class="sxs-lookup"><span data-stu-id="23a39-172">When you use [Breakpoint Debugging][DevtoolsJavascriptBreakpoints] or [Live Expressions][DevtoolsConsoleLiveExpressions], you may find that your workflows are more effective and you get better results.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="23a39-173">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="23a39-173">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Referencia de api de consola | Microsoft Docs"  
[DevtoolsConsoleConsoleFilters]: ./console-filters.md "Filtrar mensajes de consola | Microsoft Docs"  
[DevtoolsConsoleLiveExpressions]: ./live-expressions.md "Supervisar los cambios en JavaScript mediante expresiones live | Microsoft Docs"  

[DevtoolsJavascriptBreakpoints]: ../javascript/breakpoints.md "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft Docs"  

[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingExamplesHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-examples.html "Ejemplos de mensajes de consola: registro, información, error y advertencia | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingTypesHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-types.html "Ejemplos de mensajes de consola: registro de diferentes tipos | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithGroupsHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-with-groups.html "Ejemplos de mensajes de consola: agrupación de registros | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithSpecifiersHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-with-specifiers.html "Ejemplos de mensajes de consola: registro con especificadores | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithTableHtml]: https://microsoftedge.github.io/DevToolsSamples/console/logging-with-table.html "Ejemplos de mensajes de consola: Uso de tablas | GitHub"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Pila de seguimiento | Wikipedia"  

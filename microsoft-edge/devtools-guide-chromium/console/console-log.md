---
description: Cómo registrar mensajes y ejecutar JavaScript en la consola de Microsoft Edge DevTools.
title: Registrar mensajes en la herramienta consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: d48a48de7b261a628ac99f58680deb119268a980
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483666"
---
# <a name="log-messages-in-the-console-tool"></a>Registrar mensajes en la herramienta consola  

Desde que los exploradores empezaron a ofrecer herramientas para **desarrolladores, la consola** es un favorito.  La razón es sencilla.  

*   En la mayoría de los cursos de programación, aprendes a generar algún tipo de comando de impresión para obtener información sobre lo que sucede.  

Antes de DevTools, estaba limitado a una `alert()` instrucción or para depurar en el `document.write()` explorador.  

Si desea registrar información en la **consola,** hay muchos métodos disponibles.  Revise todos los métodos disponibles en la [referencia de api][DevtoolsConsoleApi].  En el siguiente fragmento de código se enumeran los métodos más importantes.  

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

Copie y pegue el fragmento de código anterior en la **consola** o vaya a Ejemplos de mensajes de [consola: registro, información, error y advertencia][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingExamplesHtml].  Al probar cualquier método en la **consola,** los métodos y parecen hacer lo mismo, mientras que los métodos and muestran un icono junto al mensaje y una forma de inspeccionar el seguimiento de pila del `log()` `info()` `error()` `warn()` mensaje. [][WikiStackTrace]  

:::image type="complex" source="../media/console-log-examples.msft.png" alt-text="La consola muestra los mensajes de distintas API de registro" lightbox="../media/console-log-examples.msft.png":::
   La **consola muestra** los mensajes de distintas API de registro  
:::image-end:::  

Sin embargo, sigue siendo una buena idea usar y para distintas tareas de registro, ya que permite filtrar mediante el tipo `info()` `log()` en la [consola][DevtoolsConsoleConsoleFilters].  

## <a name="different-types-of-logs"></a>Distintos tipos de registros  

En lugar de texto de registro, puede enviar cualquier referencia válida de JavaScript o DOM a la **consola**.  La **consola** es elegante y determina el tipo que se envía.  A continuación, le ofrece la mejor representación posible.  Copie y pegue el siguiente fragmento de código en la **consola** o para mostrar los resultados, vaya a Ejemplos de mensajes de [consola: registro de diferentes tipos][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingTypesHtml].  

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

Cada resultado se muestra de una manera diferente.  Use los triángulos para alternar la información y analizar cada uno con más detalle.  Los caracteres de llave alrededor de la variable son un buen truco para evitar muchos mensajes de registro en los que solo obtienes un valor, pero no sabes dónde `{}` `x` se originó.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-types.msft.png" alt-text="Registrar variables de diferentes tipos en la consola" lightbox="../media/console-log-types.msft.png":::
         Registrar variables de diferentes tipos en la **consola**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-types-expanded.msft.png" alt-text="Registrar variables de diferentes tipos en la consola con información adicional expandida" lightbox="../media/console-log-types-expanded.msft.png":::
         Registrar variables de diferentes tipos en la **consola con** información adicional expandida  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="format-and-convert-values-with-specifiers"></a>Dar formato y convertir valores con especificadores

Una característica especial de todos los métodos de registro es que puede usar especificadores en el mensaje de registro.  Los especificadores forman parte de un mensaje de registro y comienzan con un signo de porcentaje \( \) carácter y permiten registrar determinados valores en diferentes formatos e incluso `%` convertir cada uno.  

*   `%s` registros como cadenas
*   `%i` o `%d` registros como enteros
*   `%f` registros como un valor de punto flotante
*   `%o` registros como un elemento DOM expandible
*   `%O` registros como un objeto JavaScript expandible
*   `%c` le permite dar estilo al mensaje con CSS

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

En el primer ejemplo se muestra que el orden de reemplazo de los especificadores es el orden de parámetro que sigue a la cadena.  Para mostrar los resultados, copie y **** pegue el fragmento de código anterior en la consola o vaya a Ejemplos de mensajes de [consola: Registro con especificadores][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithSpecifiersHtml].  Expanda la información del registro para mostrar la gran diferencia entre `%o` y `%O` .  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-specifiers.msft.png" alt-text="Usar especificadores para registrar y convertir valores" lightbox="../media/console-log-specifiers.msft.png":::
         Usar especificadores para registrar y convertir valores  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-specifiers-expanded.msft.png" alt-text="Expandir los resultados muestra la diferencia entre el %O y %o especificador: el cuerpo se muestra como un nodo DOM expandible o como una lista completa de todas las propiedades de JavaScript en el cuerpo de la página web" lightbox="../media/console-log-specifiers-expanded.msft.png":::
        Expandir los resultados muestra la diferencia entre el especificador y: el cuerpo se muestra como un nodo DOM expandible o como una lista completa de todas las propiedades de JavaScript en el cuerpo de `%O` `%o` la página web  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="group-log-messages"></a>Mensajes de registro de grupo

Si registra mucha información, puede usar los métodos and para mostrar los mensajes de registro como grupos `group` `groupCollapsed` expandibles y contraibles en la **consola**.  Es posible que los grupos se anidan y se nombren para que los datos sean mucho más fáciles de comprender.  

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

También en el segundo ejemplo, los nombres de grupo se pueden generar opcionalmente.  Para mostrar los resultados, copie y **** pegue el fragmento de código anterior en la consola o vaya a Ejemplos de mensajes de [consola: agrupación de registros][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithGroupsHtml].  Puede expandir y contraer cada una de las secciones.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-groups.msft.png" alt-text="Registrar muchos valores como grupos" lightbox="../media/console-log-groups.msft.png":::
         Registrar muchos valores como grupos  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-log-groups-expanded.msft.png" alt-text="Cada grupo puede expandirse y contraerse" lightbox="../media/console-log-groups-expanded.msft.png":::
        Cada grupo puede expandirse y contraerse  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="display-complex-data-as-tables"></a>Mostrar datos complejos como tablas  

El método registra datos complejos no como un objeto que se puede contraer y expandir, sino como una tabla que puede `console.table()` ordenar con distintos encabezados.  Una tabla ordenada facilita a los usuarios revisar la información.  Para mostrarlo en un ejemplo, vaya a [Ejemplos de mensajes de consola: Uso de tabla][GithubMicrosoftedgeDevtoolssamplesConsoleLoggingWithTableHtml].

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
   Mostrar datos `console.table` con para facilitar la lectura
:::image-end:::  

El resultado de tiene un formato de tabla no solo `console.table` cuando se muestra en la **consola**.    Por ejemplo, si copia y pega una tabla en Excel, Word o cualquier otro producto que admita datos tabulares, la estructura permanece intacta.  

<!--  The output of `console.table` has a table format not only when it displays in the **Console**.  For example, copy and paste a table in Excel, Word, or any other products that support tabular data.  -->  

Si los datos tienen parámetros con nombre, el método también permite especificar una de las columnas para que cada propiedad se muestre `console.table()` `Array` como un segundo parámetro.  En el ejemplo siguiente se muestra cómo especificar una matriz de columnas que sea más legible.  

```javascript
// get all the h1, p and script elements 
let contentElements = document.querySelectorAll(':is(h1,p,script)');
// display the elements as an unfiltered table 
console.table(contentElements)
// display only relevant columns 
console.table(contentElements,['nodeName', 'innerText', 'offsetHeight'])
```  

:::image type="complex" source="../media/console-log-table-filtered.msft.png" alt-text="Filtrar información que console.table muestra y proporcionar una matriz de propiedades para mostrar como segundo parámetro" lightbox="../media/console-log-table-filtered.msft.png":::
   Filtrar información que `console.table` muestra y proporciona una matriz de propiedades para mostrar como segundo parámetro  
:::image-end:::  

Puede que tenga la tentación de usar los métodos de registro como medio principal para depurar páginas web, ya que los métodos de registro son fáciles de usar.  Tenga en cuenta el resultado de cualquier `console.log()` solicitud.  Los productos live no deben usar ningún registro que se usó para depurar.  Puede revelar información interna a las personas.  Y el ruido creado en la **consola es** abrumador.  Al usar la [depuración de puntos de][DevtoolsJavascriptBreakpoints] interrupción o [expresiones][DevtoolsConsoleLiveExpressions]en directo, puede encontrar que los flujos de trabajo son más eficaces y obtiene mejores resultados.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

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

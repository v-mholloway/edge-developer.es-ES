---
description: Una introducción al uso de la herramienta consola dentro del Microsoft Edge Developer Tools como un entorno JavaScript.
title: La consola como entorno de JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, JavaScript, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 7f70d2fef3b1f2a7055a2ee26a92fa579ca9fb8dca68abee3ec95affd6eaeb80
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11801384"
---
# <a name="the-console-as-a-javascript-environment"></a>La consola como entorno de JavaScript  

La **herramienta Consola** dentro del explorador DevTools es un entorno [REPL.][WikiReadEvalPrintLoop]  Significa que puede escribir cualquier JavaScript en la **consola que se** ejecute inmediatamente.

Para probarlo, complete las siguientes acciones.  

1.  Abra la **consola**.  
    *   Seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).  
1.  Escriba `2 + 2`.  La **consola** ya muestra el resultado `4` en la siguiente línea mientras lo escribe.  La `Eager evaluation` característica le ayuda a escribir JavaScript válido.  Muestra el resultado mientras escribe si es incorrecto o si existe un resultado válido.  

:::image type="complex" source="../media/console-javascript-eager-evaluation.msft.png" alt-text="La consola muestra el resultado de 2 + 2 en directo al escribirlo" lightbox="../media/console-javascript-eager-evaluation.msft.png":::
   **La** consola muestra el resultado `2 + 2` de live a medida que lo escribe  
:::image-end:::  

Si selecciona , la consola ejecuta el comando JavaScript, le proporciona el resultado y le permite `Enter` escribir el siguiente comando. ****  

:::image type="complex" source="../media/console-javascript-several-expressions.msft.png" alt-text="Ejecutar varias expresiones de JavaScript sucesivamente" lightbox="../media/console-javascript-several-expressions.msft.png":::
   Ejecutar varias expresiones de JavaScript sucesivamente  
:::image-end:::  

## <a name="autocompletion-to-write-complex-expressions"></a>Autocompletion to write complex expressions

El último ejemplo puede parecer espantoso, pero **la consola** le ayuda a escribir JavaScript complejo con una excelente característica de autocompleción.  Esta característica es una excelente manera de obtener información sobre los métodos que no conocías antes.  

Para probarlo, complete las siguientes acciones.  

1.  Escriba `doc`.  
1.  Elija `document` en el menú desplegable.  
1.  Seleccione la `tab` clave para elegirla.  
1.  Escriba `.bo`.  
1.  Seleccione `tab` para obtener `document.body` .  
1.  Escriba otro para obtener una lista grande de posibles propiedades y métodos `.` disponibles en el cuerpo de la página web actual.  

:::image type="complex" source="../media/console-javascript-autocomplete.msft.png" alt-text="Autocompletion de consola de expresiones de JavaScript" lightbox="../media/console-javascript-autocomplete.msft.png":::
   **Autocompletion** de consola de expresiones de JavaScript  
:::image-end:::  

## <a name="console-history"></a>Historial de consolas

Al igual que con muchas otras experiencias de línea de comandos, también tiene un historial de comandos.  Seleccione `Arrow Up` esta opción para mostrar los comandos que ha escrito anteriormente.  La autocompleción también conserva un historial de los comandos que ha especificado anteriormente.  Puede escribir las primeras letras de los comandos anteriores y las opciones anteriores se muestran en un cuadro de texto.  

Además, la **consola** también ofrece bastantes métodos de [utilidad][DevtoolsConsoleUtilities] que te facilitan la vida.  Por ejemplo, `$_` siempre contiene el resultado de la última expresión que ejecutó en la **consola**.

:::image type="complex" source="../media/console-javascript-console-history.msft.png" alt-text="La expresión $_ en la consola siempre contiene el último resultado" lightbox="../media/console-javascript-console-history.msft.png":::
    La `$_` expresión de la **consola** siempre contiene el último resultado  
:::image-end:::  

## <a name="multiline-edits"></a>Ediciones multilínea

De forma predeterminada, **la consola** solo proporciona una línea para escribir la expresión de JavaScript.  El código se ejecuta al seleccionar `Enter` . La limitación de una línea puede frustrarse.  Para evitar la limitación de una línea, seleccione `Shift` + `Enter` en lugar de `Enter` .  En el siguiente ejemplo, el valor mostrado es el resultado de todas las líneas que se ejecutan en orden.  

:::image type="complex" source="../media/console-javascript-multiline.msft.png" alt-text="Seleccione Mayús+Entrar para escribir varias líneas de JavaScript y el valor resultante se ejecuta en orden" lightbox="../media/console-javascript-multiline.msft.png":::
   Seleccione `Shift` + `Enter` para escribir varias líneas de JavaScript y el valor resultante se ejecuta en orden  
:::image-end:::  

Si inicia una instrucción multilínea en **la consola,** se reconoce automáticamente y se aplica sangría.  Por ejemplo, si inicia una instrucción block con una llave.  

:::image type="complex" source="../media/console-javascript-automatic-lineindent.msft.png" alt-text="La consola ya reconoce expresiones multilínea con llaves y sangrías cada una." lightbox="../media/console-javascript-automatic-lineindent.msft.png":::
    **La** consola ya reconoce expresiones multilínea con llaves y sangrías cada una.  
:::image-end:::  

## <a name="network-requests-using-top-level-await"></a>Solicitudes de red con await() de nivel superior  

Aparte de en sus propios scripts, **la** consola admite la espera de [nivel][GithubTc39ProposalTopLevelAwait] superior para ejecutar JavaScript asincrónico arbitrario en él.  Por ejemplo, use la `fetch` API sin ajustar la instrucción con una función `await` asincrónica.  

Para obtener los últimos 50 problemas que se han presentado en el repositorio Microsoft Edge [Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] GitHub, complete las siguientes acciones.  

1.  Abra la **consola**.  
1.  Copie y pegue el siguiente fragmento de código para obtener un objeto que contenga 10 entradas.  
    
    ```javascript
    await ( await fetch(
    'https://api.github.com/repos/microsoft/vscode-edge-devtools/issues?state=all&per_page=50&page=1'
    )).json();
    ```  
    
:::image type="complex" source="../media/console-javascript-top-level-await.msft.png" alt-text="La consola muestra el resultado de una solicitud de captura asincrónica de nivel superior" lightbox="../media/console-javascript-top-level-await.msft.png":::
    **La** consola muestra el resultado de una solicitud asincrónica de nivel `fetch` superior  
:::image-end:::  

Las 10 entradas son difíciles de reconocer, ya que se muestra mucha información.  Afortunadamente, puede usar el método log para recibir solo la información en la que `console.table()` está interesado.  

:::image type="complex" source="../media/console-javascript-filtered-with-table.msft.png" alt-text="Mostrar el último resultado en un formato legible con console.table" lightbox="../media/console-javascript-filtered-with-table.msft.png":::
    Mostrar el último resultado en un formato de lectura humana mediante `console.table`  
:::image-end:::  

Para volver a usar los datos devueltos de una expresión, puede usar el método `copy()` de utilidad de console . ****  El siguiente fragmento de código envía la solicitud y copia los datos de la respuesta al Portapapeles.  

```javascript
copy(await (await fetch(
'https://api.github.com/repos/microsoft/vscode-edge-devtools/issues?state=all&per_page=50&page=1'
)).json())
```  

Use la **consola como** una excelente manera de practicar la funcionalidad de JavaScript y realizar algunos cálculos rápidos.  La potencia real es el hecho de que tiene acceso al objeto [window.][MdnDocsWebApiWindow]  Puede interactuar [con el DOM en la consola][DevtoolsConsoleConsoleDomInteraction].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleDomInteraction]: ./console-dom-interaction.md "Use la consola para interactuar con el dom | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Referencia de api de utilidades de consola | Microsoft Docs"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubTc39ProposalTopLevelAwait]: https://github.com/tc39/proposal-top-level-await "Propuesta ecmascript: espera de nivel superior - tc39/proposal-top-level-await | GitHub"

[MdnDocsWebApiWindow]: https://developer.mozilla.org/docs/Web/API/Window "Ventana | MDN"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Bucle read–eval–print | Wikipedia"  

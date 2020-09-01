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







# Introducción a la ejecución de JavaScript en la consola   



Este tutorial interactivo muestra cómo ejecutar JavaScript en la **consola**de Microsoft Edge DevTools.  Para obtener más información sobre cómo registrar mensajes en la **consola**, consulte Introducción a [los mensajes de registro][DevToolsConsoleLoggingMessages].  Para obtener más información sobre cómo pausar código JavaScript y resaltarlo de línea en línea, consulte Introducción a la [depuración de JavaScript][DevToolsJavascriptIndex].  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="La consola" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   La **consola**  
:::image-end:::  

## Introducción   

La **consola** es una [REPL][WikiReadEvalPrintLoop], lo que significa lectura, evaluación, impresión y bucle.  Lee el código JavaScript que escribe en él, evalúa el código, imprime el resultado de la [expresión][2alityExpressionsVersusStatements]y, a continuación, retrocede al primer paso.  

## Configurar DevTools   

Este tutorial está diseñado para que abras la demostración y pruebe todos los flujos de trabajo.  Cuando sigues físicamente, es más probable que recuerdes los flujos de trabajo más adelante.

1.  Pulse `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \) para abrir la **consola**.  
1.  Mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y haga clic en **ejemplo de JavaScript de consola** para abrirlo en una ventana nueva.  
    
    *   [Ejemplo de JavaScript de consola][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="La página de ejemplo de JavaScript de la consola de la izquierda y DevTools a la derecha" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       La página de ejemplo de JavaScript de la consola de la izquierda y DevTools a la derecha  
    :::image-end:::  
    
## Ver y cambiar el JavaScript o el DOM de la página   

Al crear o depurar una página, a menudo es útil ejecutar instrucciones en la **consola** para cambiar el aspecto o la ejecución de la página.  
    
1.  Observe el texto en el botón.  
1.  Escriba `document.getElementById('hello').textContent = 'Hello, Console!'` la **consola** y, a continuación, pulse `Enter` para evaluar la expresión.  Observe cómo cambia el texto que se encuentra dentro del botón.  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Aspecto de la consola después de la evaluación de la expresión" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       Aspecto de la **consola** después de la evaluación de la expresión  
    :::image-end:::  
    
    Debajo del código que hayas evaluado verás `"Hello, Console!"` .  Recupere los cuatro pasos de REPL: leer, evaluar, imprimir, repetir.  Después de evaluar el código, una REPL imprime el resultado de la expresión.  Por lo tanto, `"Hello, Console!"` debe ser el resultado de la evaluación `document.getElementById('hello').textContent = 'Hello, Console!'` .  
    
## Ejecutar JavaScript arbitrario que no está relacionado con la página   

A veces, solo deseas un código de animación donde puedas probar algún código o probar nuevas características de JavaScript con las que no estás familiarizado.  La consola es un lugar ideal para estos tipos de experimentos.  

1.  Escriba `5 + 15` la consola y pulse `Enter` para evaluar la expresión. La consola imprime el resultado de la expresión que está debajo del código.  En la siguiente ilustración, la **consola** debería mostrar el resultado después de evaluar la expresión.  

1.  Escriba el código siguiente en la **consola**.  Pruebe a escribirla, carácter a carácter, en lugar de pegarla.  
    
    ```javascript
    function add(a, b=20) { return a + b; }
    ```  
    
    Si no está familiarizado con la `b=20` sintaxis, consulte [definir valores predeterminados para los argumentos de una función][Esma6DefaultParameterValues].  
    
1.  Ahora, ejecute la función que acaba de definir.  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="La consola se muestra después de evaluar las expresiones en el fragmento de código." lightbox="../media/console-javascript-example-console-playground.msft.png":::
             La **consola** se muestra después de evaluar las expresiones en el fragmento de código.  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` se evalúa como `45` porque cuando `add` se llama a la función sin un segundo argumento, el `b` valor predeterminado es `20` .  

## Pasos siguientes   

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

DevTools le permite pausar un script en mitad de la ejecución.  Mientras está pausado, puede usar la **consola** para ver y cambiar la `window` o `DOM` de la página en ese momento.  El flujo de trabajo hace que el flujo de trabajo de depuración sea eficaz.  Para obtener un tutorial interactivo, consulte [Introducción a la depuración de JavaScript][DevToolsJavascriptIndex].  

La **consola** también tiene un conjunto de funciones de comodidad que hacen que sea más fácil interactuar con una página.  Por ejemplo:  

*   En lugar de escribir `document.querySelector()` para seleccionar un elemento, escriba `$()` .  Esta sintaxis está inspirada en jQuery, pero en realidad no es jQuery.  Es solo un alias para `document.querySelector()` .  
*   `debug(function)` establece de forma eficaz un punto de interrupción en la primera línea de esa función.  
*   `keys(object)` Devuelve una matriz que contiene las claves del objeto especificado.  

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
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/javascript) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

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

# <a name="get-started-with-running-javascript-in-the-console"></a>Introducción a la ejecución de JavaScript en la consola  

En este tutorial interactivo se muestra cómo ejecutar JavaScript en la consola de Microsoft Edge **DevTools**.  Para obtener más información acerca de cómo registrar mensajes en la **consola,** vaya a [Introducción al registro de mensajes][DevToolsConsoleLoggingMessages].  Para obtener más información acerca de cómo pausar código JavaScript y recorrerlo de una línea a la vez, vaya a Introducción a [La depuración de JavaScript][DevToolsJavascriptIndex].  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="La consola" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   La **consola**  
:::image-end:::  

## <a name="overview"></a>Introducción  

La **consola** es [una REPL][WikiReadEvalPrintLoop], que significa Leer, Evaluar, Imprimir y Bucle.  Lee el JavaScript que escribe en él, evalúa el código, imprime [][2alityExpressionsVersusStatements]el resultado de la expresión y, a continuación, vuelve al primer paso.  

## <a name="set-up-devtools"></a>Configurar DevTools  

Este tutorial está diseñado para que abra la demostración y pruebe todos los flujos de trabajo usted mismo.  Cuando se sigue físicamente, es más probable que recuerde los flujos de trabajo más adelante.

1.  Seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\) para abrir la **consola**.  
1.  Mantenga `Control` presionado \(Windows, Linux\) o `Command` \(macOS\) y elija Ejemplo **de Javascript** de consola para abrir en una nueva ventana.  
    
    *   [Ejemplo de Javascript de consola][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="Página ejemplo de JavaScript de consola a la izquierda y DevTools a la derecha" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       Página ejemplo de JavaScript de consola a la izquierda y DevTools a la derecha  
    :::image-end:::  
    
## <a name="view-and-change-the-javascript-or-dom-of-the-page"></a>Ver y cambiar javascript o DOM de la página  

Al compilar o depurar una página, a menudo resulta **** útil ejecutar instrucciones en la consola para cambiar el aspecto o la ejecución de la página.  
    
1.  Observe el texto del botón.  
1.  Escriba `document.getElementById('hello').textContent = 'Hello, Console!'` la **consola y,** a continuación, `Enter` seleccione para evaluar la expresión.  Observe cómo cambia el texto dentro del botón.  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Cómo se ve la consola después de evaluar la expresión" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       Cómo se **ve la consola** después de evaluar la expresión  
    :::image-end:::  
    
    `"Hello, Console!"`, se muestra debajo del código que ha evaluado.  Recuerde los 4 pasos de REPL: leer, evaluar, imprimir, bucle.  Después de evaluar el código, una REPL imprime el resultado de la expresión.  Por `"Hello, Console!"` lo tanto, debe ser el resultado de la evaluación `document.getElementById('hello').textContent = 'Hello, Console!'` .  
    
## <a name="run-arbitrary-javascript-that-is-not-related-to-the-page"></a>Ejecutar JavaScript arbitrario que no esté relacionado con la página  

A veces, solo quieres un área de juegos de código donde puedas probar código o probar nuevas características de JavaScript con las que no estás familiarizado.  La **consola** es un lugar perfecto para este tipo de experimentos.  

1.  Escriba `5 + 15` la consola y seleccione para evaluar la `Enter` expresión. La consola imprime el resultado de la expresión debajo del código.  En la siguiente figura, la **consola** debe mostrar el resultado después de evaluar la expresión.  

1.  Escriba el siguiente código en la **consola**.  Intenta escribirlo, carácter por carácter, en lugar de copiarlo.  
    
    ```javascript
    function add(a, b=20)
    ```  
    
    Si no está familiarizado con la sintaxis, navegue para definir los `b=20` valores predeterminados de los [argumentos de función][Esma6DefaultParameterValues].  
    
1.  Ahora, ejecute la función que acaba de definir.  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="La consola se muestra después de evaluar las expresiones del fragmento de código" lightbox="../media/console-javascript-example-console-playground.msft.png":::
             La **consola** se muestra después de evaluar las expresiones del fragmento de código  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` se evalúa porque cuando se llama a la `45` función sin un segundo `add` argumento, el valor predeterminado es `b` `20` .  

## <a name="next-steps"></a>Pasos siguientes  

<!--To explore more features related to running JavaScript in the **Console**, navigate to [Run JavaScript][DevToolsConsoleReference].  -->  

<!--todo: add console reference (run javascript) section when available  -->  

DevTools te permite pausar un script en medio de la ejecución.  Mientras está en pausa, puede **** usar la consola para ver y cambiar la página en `window` ese `DOM` momento.  El flujo de trabajo crea un flujo de trabajo de depuración eficaz.  Para obtener un tutorial interactivo, vaya a [Introducción a La depuración de JavaScript][DevToolsJavascriptIndex].  

La **consola** también tiene un conjunto de funciones de comodidad que facilitan la interacción con una página.  Por ejemplo:  

*   En lugar de escribir `document.querySelector()` para seleccionar un elemento, escriba `$()` .  Esta sintaxis se inspira en jQuery, pero en realidad no es jQuery.  Es solo un alias para `document.querySelector()` .  
*   `debug(function)` establece de forma eficaz un punto de interrupción en la primera línea de esa función.  
*   `keys(object)` devuelve una matriz que contiene las claves del objeto especificado.  

Para obtener más información acerca de las funciones de comodidad, vaya a [Console Utilities API Reference][DevToolsConsoleUtilities].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

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
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/javascript) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

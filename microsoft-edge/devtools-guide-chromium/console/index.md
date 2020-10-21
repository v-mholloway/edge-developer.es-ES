---
description: Los usos principales de la consola de Microsoft Edge DevTools son el registro de mensajes y la ejecución de JavaScript.
title: Descripción general de la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 32272c3f76f715566ced66d11346985dc95dd290
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125268"
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

# Descripción general de la consola  

  

Esta página explica cómo la consola de Microsoft Edge DevTools facilita el desarrollo de páginas Web.  La consola tiene 2 usos principales: [ver los mensajes registrados](#viewing-logged-messages) y [ejecutar JavaScript](#running-javascript).  

## Ver mensajes registrados  

Los desarrolladores web suelen registrar mensajes en la consola para asegurarse de que su JavaScript funciona según lo esperado.  Para registrar un mensaje, debe insertar una expresión como `console.log('Hello, Console!')` en su código JavaScript.  Cuando el explorador ejecuta el JavaScript y ve una expresión como esta, registra el mensaje en la consola.  

:::row:::
   :::column span="":::
      El código HTML y JavaScript de la página.  
      
      ```html
      <!doctype html>
      <html>
          <head>
              <title>Console Demo</title>
          </head>
          <body>
              <h1>Hello, World!</h1>
              <script>
                  console.log('Loading!');
                  const h1 = document.querySelector('h1');
                  console.log(h1.textContent);
                  console.assert(document.querySelector('h2'), 'h2 not found!');
                  const artists = [
                      { first: 'René', last: 'Magritte' },
                      { first: 'Chaim', last: 'Soutine' },
                        
                  ];
                  console.table(artists);
                  setTimeout(() => {
                      h1.textContent = 'Hello, Console!';
                      console.log(h1.textContent);
                  }, 3000);
              </script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      En la siguiente ilustración, la **consola** muestra los resultados de cargar la página y esperar 3 segundos.  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="Panel de consola" lightbox="../media/console-console-demo.msft.png":::
         Panel de **consola**  
      :::image-end:::  
      
      Intente determinar qué líneas de código hicieron que el explorador registre los mensajes.  
   :::column-end:::
:::row-end:::  

Los programadores de web registran los mensajes por las siguientes 2 razones generales.  

*   Asegurarse de que el código se esté ejecutando en el orden correcto.  
*   Inspeccionar los valores de variables en un momento determinado.  

Consulte Introducción al [registro de mensajes][DevtoolsConsoleLoggingMessages] para obtener experiencia práctica con el registro.  Consulta la [referencia][DevToolsConsoleAPI] de la API de consola para examinar la lista completa de `console` métodos.  La principal diferencia entre los métodos radica en la forma en que se muestran los datos que se registran.  

## Ejecutar JavaScript  

La **consola** también es una [REPL][WikiREPLoop].  Puede ejecutar JavaScript en la **consola** para interactuar con la página que se está inspeccionando.   

:::row:::
   :::column span="":::
      En la siguiente ilustración, la **consola** se muestra junto a la página de inicio de DevTools.  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="Panel de consola" lightbox="../media/devtools-console-empty.msft.png":::
         Panel de **consola** junto a la Página principal de DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      En la siguiente ilustración, se muestra la misma página después de usar la **consola** para cambiar el encabezado superior de la página.
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Panel de consola" lightbox="../media/devtools-console-h1-changed.msft.png":::
         Usar la **consola** para cambiar el encabezado superior de la página  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Es posible modificar la página desde la **consola** porque la **consola** tiene acceso completo a la [ventana][MDNWindow] de la página.  DevTools tiene varias funciones útiles que hacen que sea más fácil inspeccionar una página.  Por ejemplo, supongamos que su código JavaScript contiene una función llamada `hideModal` .  La ejecución `debug(hideModal)` pausa el código en la primera línea de `hideModal` la próxima vez que lo ejecute.  Para obtener más información sobre la lista completa de funciones de utilidades, vaya a referencia de la [API de utilidades de consola][DevtoolsConsoleUtilitiesDebug].  

Al ejecutar JavaScript, no es necesario que interactúe con la página.  Puede usar la **consola** para probar código nuevo no relacionado con la página.  Por ejemplo, supongamos que acaba de conocer el método de asignación de matriz [()][MDNMap] integrado de JavaScript y quiere experimentar con él.  
La **consola** es un buen lugar para probar la función.  

Para obtener más experiencia práctica con la ejecución de JavaScript en la **consola**, vaya a introducción a la [ejecución de JavaScript][DevtoolsConsoleRunningJavascript].  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleAPI]: ./api.md "Referencia de la API de consola | Microsoft docs"  
[DevtoolsConsoleLoggingMessages]: ./log.md "Introducción a la creación de mensajes de registro en la consola | Microsoft docs"  
[DevtoolsConsoleRunningJavascript]: ./javascript.md "Introducción a la ejecución de JavaScript en la consola | Microsoft docs"  
[DevtoolsConsoleUtilitiesDebug]: ./utilities.md#debug "Debug: referencia de API de utilidades de consola | Microsoft docs"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array. prototype. map () | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Ventana | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lectura: eval – imprimir bucle-Wikipedia"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

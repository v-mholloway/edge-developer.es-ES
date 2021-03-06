---
description: Los principales usos de la consola de Microsoft Edge DevTools son el registro de mensajes y la ejecución de JavaScript.
title: Información general sobre la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 496caa4d304d9511d4b1c341846f377899ba4597
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399123"
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

# <a name="console-overview"></a>Información general sobre la consola  

  

En esta página se explica cómo la consola DevTools de Microsoft Edge facilita el desarrollo de páginas web.  La **consola** tiene dos usos principales: [ver mensajes registrados](#viewing-logged-messages) y [ejecutar JavaScript](#running-javascript).  

## <a name="viewing-logged-messages"></a>Visualización de mensajes registrados  

Los desarrolladores web suelen registrar mensajes en la consola para asegurarse de que su JavaScript funciona según lo esperado.  Para registrar un mensaje, inserte una expresión como `console.log('Hello, Console!')` en su JavaScript.  Cuando el explorador ejecuta JavaScript y procesa una expresión como esta, el explorador registra el mensaje en la **consola**.  

:::row:::
   :::column span="":::
      Html y JavaScript para la página.  
      
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
      En la siguiente figura, la **consola** muestra los resultados de cargar la página y esperar 3 segundos.  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="Panel consola" lightbox="../media/console-console-demo.msft.png":::
         La **herramienta Consola**  
      :::image-end:::  
      
      Intente determinar qué líneas de código provocaron que el explorador registrara los mensajes.  
   :::column-end:::
:::row-end:::  

Los desarrolladores web registrarán mensajes por los siguientes 2 motivos generales.  

*   Asegurarse de que el código se ejecuta en el orden correcto.  
*   Inspeccionar los valores de las variables en un momento determinado.  

Para obtener experiencia práctica con el registro, vaya a Introducción a Los mensajes [de registro.][DevtoolsConsoleLoggingMessages]  Para examinar la lista completa de `console` métodos, vaya a La referencia [de la API de consola.][DevToolsConsoleAPI]  La diferencia principal entre los métodos es cómo se muestran los datos que se registran.  

## <a name="running-javascript"></a>Ejecución de JavaScript  

La **consola** también es [una REPL][WikiREPLoop].  Puede ejecutar JavaScript en la **consola para** interactuar con la página que se va a inspeccionar.   

:::row:::
   :::column span="":::
      En la siguiente figura, la **consola** se muestra junto a la página principal de DevTools.  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="La herramienta Consola junto a la página principal de DevTools" lightbox="../media/devtools-console-empty.msft.png":::
         La **herramienta Consola** junto a la página principal de DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      En la siguiente figura, se muestra la misma página después de usar la **consola** para cambiar el encabezado superior de la página.
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Usar la consola para cambiar el encabezado superior de la página" lightbox="../media/devtools-console-h1-changed.msft.png":::
         Usar la **consola** para cambiar el encabezado superior de la página  
      :::image-end:::  
   :::column-end:::
:::row-end:::

La modificación de la página desde la **consola** es posible porque **la consola** tiene acceso completo a la [ventana][MDNWindow] de la página.  DevTools tiene algunas funciones de comodidad que facilitan la inspección de una página.  Por ejemplo, supongamos que JavaScript contiene una función denominada `hideModal` .  La `debug(hideModal)` ejecución pausa el código en la primera línea de la próxima vez que lo `hideModal` ejecute.  Para obtener más información acerca de la lista completa de funciones de utilidad, vaya a [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug].  

Al ejecutar JavaScript no es necesario interactuar con la página.  Puede usar la consola **para** probar código nuevo que no esté relacionado con la página.  Por ejemplo, supongamos que acaba de aprender sobre el método integrado [map()][MDNMap] de matriz de JavaScript y desea experimentar con él.  
La **consola** es un buen lugar para probar la función.  

Para obtener más experiencia práctica con la ejecución de JavaScript en la **consola,** vaya a Introducción a [La ejecución de JavaScript][DevtoolsConsoleRunningJavascript].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleAPI]: ./api.md "Referencia de api de consola | Microsoft Docs"  
[DevtoolsConsoleLoggingMessages]: ./log.md "Introducción al registro de mensajes en la consola | Microsoft Docs"  
[DevtoolsConsoleRunningJavascript]: ./javascript.md "Introducción a la ejecución de JavaScript en la consola | Microsoft Docs"  
[DevtoolsConsoleUtilitiesDebug]: ./utilities.md#debug "debug: referencia de api de utilidades de consola | Microsoft Docs"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array.prototype.map() | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Ventana | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Bucle read-eval-print - Wikipedia"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

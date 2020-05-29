---
title: Descripción general de la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 6062afb929a5d763c095d4915a2960993bc5ab4c
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601792"
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

Los desarrolladores web suelen registrar mensajes en la consola para asegurarse de que su JavaScript funciona según lo esperado.  Para registrar un mensaje, debe insertar una expresión como `console.log('Hello, Console!')` en su código JavaScript.  Cuando el explorador ejecuta el JavaScript y ve una expresión como esta, registra el mensaje en la consola.  Por ejemplo, supongamos que está escribiendo HTML y JavaScript para una página:  

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
        {
          first: 'René',
          last: 'Magritte'
        },
        {
          first: 'Chaim',
          last: 'Soutine'
        },
        {
          first: 'Henri',
          last: 'Matisse'
        }
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

En la [Ilustración 1](#figure-1) se muestra el aspecto que tiene la consola después de cargar la página y esperar 3 segundos.  Intenta averiguar qué líneas de código hicieron que el explorador registre los mensajes.  

> ##### Figura 1  
> Panel de consola  
> ![Panel de consola][ImageConsole]  

Los programadores web registran los mensajes por dos razones generales:  

*   Asegurarse de que el código se esté ejecutando en el orden correcto.  
*   Inspeccionar los valores de variables en un momento determinado.  

Consulte Introducción al [registro de mensajes][DevtoolsConsoleLoggingMessages] para obtener experiencia práctica con el registro.  Consulta la [referencia][DevToolsConsoleAPI] de la API de consola para examinar la lista completa de `console` métodos.  La principal diferencia entre los métodos radica en la forma en que se muestran los datos que se registran.  

## Ejecutar JavaScript   

La consola también es una [REPL][WikiREPLoop].  Puede ejecutar JavaScript en la consola para interactuar con la página que se está inspeccionando.  Por ejemplo, la [ilustración 2](#figure-2) muestra la consola junto a la página de inicio de DevTools, y la [figura 3](#figure-3) muestra la misma página después de usar la consola para cambiar el encabezado superior de la página.  

> ##### Figura 2  
> Panel de consola junto a la Página principal de DevTools  
> ![Panel de consola junto a la Página principal de DevTools][ImageConsoleOverview]  

> ##### Imagen 3  
> Usar la consola para cambiar el encabezado superior de la página  
> ![Usar la consola para cambiar el encabezado superior de la página][ImageConsoleChangeTitle]  

Es posible modificar la página desde la consola porque la consola tiene acceso completo a la [ventana][MDNWindow] de la página.  DevTools tiene varias funciones útiles que hacen que sea más fácil inspeccionar una página.  Por ejemplo, supongamos que su código JavaScript contiene una función llamada `hideModal` .  La ejecución `debug(hideModal)` pausa el código en la primera línea de `hideModal` la próxima vez que lo ejecute.  Consulte [referencia][DevtoolsConsoleUtilitiesDebug] de la API de utilidades de consola para ver la lista completa de funciones de utilidades.  

Al ejecutar JavaScript, no es necesario que interactúe con la página.  Puede usar la consola para probar código nuevo no relacionado con la página.  Por ejemplo, supongamos que acaba de conocer el método de asignación de matriz [()][MDNMap] integrado de JavaScript y quiere experimentar con él.  
La **consola** es un buen lugar para probar la función.  

Consulte Introducción a la [ejecución de JavaScript][ImageConsoleChangeTitle] para obtener experiencia práctica de ejecución de JavaScript en la consola.  

   

  

<!-- image links -->  

[ImageConsole]: /microsoft-edge/devtools-guide-chromium/media/console-console-demo.msft.png "Ilustración 1: panel de consola"  
[ImageConsoleChangeTitle]: /microsoft-edge/devtools-guide-chromium/media/devtools-console-h1-changed.msft.png "Ilustración 3: usar la consola para cambiar el encabezado superior de la página"  
[ImageConsoleOverview]: /microsoft-edge/devtools-guide-chromium/media/devtools-console-empty.msft.png "Ilustración 2: el panel de la consola junto a la Página principal de DevTools"  

<!-- links -->  

[DevToolsConsoleAPI]: /microsoft-edge/devtools-guide-chromium/console/api "Referencia de la API de consola"  
[DevtoolsConsoleLoggingMessages]: /microsoft-edge/devtools-guide-chromium/console/log "Introducción al registro de mensajes en la consola"  
[DevtoolsConsoleRunningJavascript]: /microsoft-edge/devtools-guide-chromium/console/javascript "Introducción a la ejecución de JavaScript en la consola"  
[DevtoolsConsoleUtilitiesDebug]: /microsoft-edge/devtools-guide-chromium/console/utilities#debug "Debug: referencia de API de utilidades de consola"  

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

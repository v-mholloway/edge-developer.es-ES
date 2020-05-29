---
title: Referencia de la API de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e54bae7c7c61584ccd39568f1bb54312cc2082c0
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601757"
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





# Referencia de la API de consola   

  

Usa los métodos de la API de consola para escribir mensajes en la consola desde tu JavaScript.  Consulte Introducción al [registro de mensajes en la consola][DevtoolsConsoleLog] para obtener una introducción interactiva al tema.  Consulte [referencia] [DevtoolConsoleUtilities] de la API de utilidades de consola si busca los métodos útiles como `debug()` o `monitorEvents()` que solo están disponibles en la consola.  

## aserciones  

```javascript
console.assert(expression, object)
```

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

Escribe un [error](#error) en la consola cuando `expression` se evalúa en `false` .  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

> ##### Figura 1  
> El resultado del `console.assert()` ejemplo  
> ![El resultado del ejemplo de Console. Assert ()][ImageAssert]  

## Libere  

```javascript
console.clear()
```

Borra la consola.  

```javascript
console.clear();  
```  

Si se habilita [preservar registro][DevtoolsConsoleReferenceLevel] , el método [Borrar](#clear) estará desactivado.  

Consulte también: [borrar la consola][DevtoolsConsoleReferenceClear]  

## encuentra  

```javascript
console.count([label])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Escribe el número de veces que se ha invocado al método [Count](#count) en la misma línea y con el mismo `label` .  Usa el método [countReset](#countreset) para restablecer el recuento.  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

> ##### Figura 2  
> El resultado del `console.count()` ejemplo  
> ![El resultado del ejemplo de Console. Count ()][ImageCount]  

## countReset  

```javascript
console.countReset([label])
```  

Restablece un recuento.  

```javascript
console.countReset();
console.countReset('coffee');
```  

## depurar  

```javascript
console.debug(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Es idéntico al método de [registro](#log) .  

```javascript
console.debug('debug');  
```  

> ##### Imagen 3  
> El resultado del `console.debug()` ejemplo  
> ![El resultado del ejemplo de Console. debug ()][ImageDebug]  

## dir  

```javascript
console.dir(object)
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Imprime una representación JSON del objeto especificado.  

```javascript
console.dir(document.head);
```  

> ##### Imagen 4  
> El resultado del `console.dir()` ejemplo  
> ![El resultado del ejemplo de Console. dir ()][ImageDir]  

## dirxml  

```javascript
console.dirxml(node)
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Imprime una representación XML de los descendientes de `node` .  

```javascript
console.dirxml(document);
```  

> ##### Imagen 5  
> El resultado del `console.dirxml()` ejemplo  
> ![El resultado del ejemplo de Console. dirxml ()][ImageDirXml]  

## error  

```javascript
console.error(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Error`  

Imprime `object` en la consola, le da formato de error e incluye un seguimiento de la pila.  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

> ##### Imagen 6  
> El resultado del `console.error()` ejemplo  
> ![El resultado de la consola. ejemplo de error ()][ImageError]  

## grupo  

```javascript
console.group(label)
```  

Agrupa visualmente los mensajes hasta que se usa el método [groupEnd](#groupend) .  Use el método [groupCollapsed](#groupcollapsed) para contraer el grupo cuando se haya registrado inicialmente en la consola.  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

> ##### Imagen 7  
> El resultado del `console.group()` ejemplo  
> ![El resultado del ejemplo de Console. Group ()][ImageGroup]  

## groupCollapsed  

```javascript
console.groupCollapsed(label)
```  

Igual que el método [log](#log) , excepto que el grupo se contraiga inicialmente cuando se registra en la consola.  

## groupEnd  

```javascript
console.groupEnd(label)
```  

Detiene la agrupación visual de mensajes.  Consulta el método [Group](#group) .  

## información  

```javascript
console.info(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Es idéntico al método de [registro](#log) .  

```javascript
console.info('info');
```  

> ##### Imagen 8  
> El resultado del `console.info()` ejemplo  
> ![El resultado del ejemplo console.info ()][ImageInfo]  

## registros  

```javascript
console.log(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Imprime un mensaje en la consola.  

```javascript
console.log('log');
```  

> ##### Imagen 9  
> El resultado del `console.log()` ejemplo  
> ![El resultado del ejemplo de Console. log ()][ImageLog]  

## Table  

```javascript
console.table(array)
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Registra una matriz de objetos como una tabla.  

```javascript
console.table([
    {
        first: 'René',
        last: 'Magritte',
    },
    {
        first: 'Chaim',
        last: 'Soutine',
        birthday: '18930113',
    },
    {
        first: 'Henri',
        last: 'Matisse',
    }
]);
```  

> ##### Imagen 10  
> El resultado del `console.table()` ejemplo  
> ![El resultado del ejemplo de Console. Table ()][ImageTable]  

## time  

```javascript
console.time([label])
```  

Inicia un nuevo temporizador.  Use el método [timeEnd](#timeend) para detener el temporizador e imprimir el tiempo transcurrido en la consola.  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

> ##### Imagen 11  
> El resultado del `console.time()` ejemplo  
> ![El resultado del ejemplo de Console. Time ()][ImageTime]  

## timeEnd  

```javascript
console.timeEnd([label])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Detiene un temporizador.  Consulta el método de [hora](#time) .  

## trazabilidad  

```javascript
console.trace()
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Imprime un seguimiento de la pila en la consola.  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

> ##### Imagen 12  
> El resultado del `console.trace()` ejemplo  
> ![El resultado del ejemplo de Console. Trace ()][ImageTrace]  

## advertir  

```javascript
console.warn(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Warning`  

Imprime una advertencia en la consola.  

```javascript
console.warn('warn');
```  

> ##### Imagen 13  
> El resultado del `console.warn()` ejemplo  
> ![El resultado del ejemplo de Console. WARN ()][ImageWarn]  

   

  

<!-- image links -->  

[ImageAssert]: /microsoft-edge/devtools-guide-chromium/media/console-demo-assert-button.msft.png "Ilustración 1: ejemplo de Console. Assert ()"  
[ImageCount]: /microsoft-edge/devtools-guide-chromium/media/console-demo-count-button.msft.png "Ilustración 2: ejemplo de Console. Count ()"  
[ImageDebug]: /microsoft-edge/devtools-guide-chromium/media/console-demo-debug-button.msft.png "Ilustración 3: el resultado del ejemplo de Console. debug ()"  
[ImageDir]: /microsoft-edge/devtools-guide-chromium/media/console-demo-dir-button.msft.png "Ilustración 4: ejemplo de Console. dir ()"  
[ImageDirXml]: /microsoft-edge/devtools-guide-chromium/media/console-demo-dirxml-button.msft.png "Ilustración 5: el resultado del ejemplo de Console. dirxml ()"  
[ImageError]: /microsoft-edge/devtools-guide-chromium/media/console-demo-error-button.msft.png "Ilustración 6: el resultado de la consola. error () ejemplo"  
[ImageGroup]: /microsoft-edge/devtools-guide-chromium/media/console-demo-group-button.msft.png "Ilustración 7: ejemplo de Console. Group ()"  
[ImageInfo]: /microsoft-edge/devtools-guide-chromium/media/console-demo-info-button.msft.png "Ilustración 8: el resultado del ejemplo console.info ()"  
[ImageLog]: /microsoft-edge/devtools-guide-chromium/media/console-demo-log-button.msft.png "Ilustración 9: el resultado del ejemplo de Console. log ()"  
[ImageTable]: /microsoft-edge/devtools-guide-chromium/media/console-demo-table-button.msft.png "Ilustración 10: el resultado del ejemplo de Console. Table ()"  
[ImageTime]: /microsoft-edge/devtools-guide-chromium/media/console-demo-time-button.msft.png "Ilustración 11: el resultado de la consola. Time () ejemplo"  
[ImageTrace]: /microsoft-edge/devtools-guide-chromium/media/console-demo-trace-button.msft.png "Ilustración 12: el resultado del ejemplo Console. Trace ()"  
[ImageWarn]: /microsoft-edge/devtools-guide-chromium/media/console-demo-warn-button.msft.png "Ilustración 13: el resultado del ejemplo de Console. WARN ()"  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Introducción al registro de mensajes en la consola"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Referencia de API de utilidades de consola"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Borrar la consola: referencia de consola"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Conservar mensajes en la carga de páginas: referencia de consola"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrar por nivel de registro-referencia de consola"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/api) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

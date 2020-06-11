---
title: Referencia de la API de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/09/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 19545759ede4252f2e7ba21329d482f4eb96f0c6
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "10708532"
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

Usa los métodos de la API de consola para escribir mensajes en la consola desde tu JavaScript.  Para obtener una introducción interactiva al tema, consulte Introducción al [registro de mensajes en la consola][DevtoolsConsoleLog].  Para obtener los métodos útiles como `debug()` o `monitorEvents()` que solo están disponibles en el panel de **consola** , consulte referencia de API de utilidades de [consola][DevtoolConsoleUtilities].  

---  

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

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="El resultado del ejemplo de Console. Assert ()" lightbox="../media/console-demo-assert-button.msft.png":::
   Ilustración 1: el resultado del `console.assert()` ejemplo  
:::image-end:::  

---  

## Libere  

```javascript
console.clear()
```

Borra la consola.  

```javascript
console.clear();  
```  

Si se habilita [preservar registro][DevtoolsConsoleReferenceLevel] , el método [Borrar](#clear) estará desactivado.  

### Consulte también  

*   [Borrar la consola][DevtoolsConsoleReferenceClear]  

---  

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

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="El resultado del ejemplo de Console. Count ()" lightbox="../media/console-demo-count-button.msft.png":::
   Ilustración 2: el resultado del `console.count()` ejemplo  
:::image-end:::  

---  

## countReset  

```javascript
console.countReset([label])
```  

Restablece un recuento.  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## depurar  

```javascript
console.debug(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Verbose`

Es idéntico a [log](#log) , excepto el nivel de registro diferente.  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="El resultado del ejemplo de Console. debug ()" lightbox="../media/console-demo-debug-button.msft.png":::
   Ilustración 3: el resultado del `console.debug()` ejemplo  
:::image-end:::  

---  

## dir  

```javascript
console.dir(object)
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Imprime una representación JSON del objeto especificado.  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="El resultado del ejemplo de Console. dir ()" lightbox="../media/console-demo-dir-button.msft.png":::
   Ilustración 4: el resultado del `console.dir()` ejemplo  
:::image-end:::  

---  

## dirxml  

```javascript
console.dirxml(node)
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Imprime una representación XML de los descendientes de `node` .  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="El resultado del ejemplo de Console. dirxml ()" lightbox="../media/console-demo-dirxml-button.msft.png":::
   Ilustración 5: el resultado del `console.dirxml()` ejemplo  
:::image-end:::  

---  

## error  

```javascript
console.error(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Error`  

Imprime `object` en la consola, le da formato de error e incluye un seguimiento de la pila.  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="El resultado de la consola. ejemplo de error ()" lightbox="../media/console-demo-error-button.msft.png":::
   Ilustración 6: el resultado del `console.error()` ejemplo  
:::image-end:::  

---  

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

:::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="El resultado del ejemplo de Console. Group ()" lightbox="../media/console-demo-group-button.msft.png":::
   Ilustración 7: el resultado del `console.group()` ejemplo  
:::image-end:::  

---  

## groupCollapsed  

```javascript
console.groupCollapsed(label)
```  

Igual que el método [log](#log) , excepto que el grupo se contraiga inicialmente cuando se registra en la consola.  

---  

## groupEnd  

```javascript
console.groupEnd(label)
```  

Detiene la agrupación visual de mensajes.  Consulta el método [Group](#group) .  

---  

## información  

```javascript
console.info(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Es idéntico al método de [registro](#log) .  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="El resultado del ejemplo console.info ()" lightbox="../media/console-demo-info-button.msft.png":::
   Ilustración 8: el resultado del `console.info()` ejemplo  
:::image-end:::  

---  

## registros  

```javascript
console.log(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Imprime un mensaje en la consola.  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="El resultado del ejemplo de Console. log ()" lightbox="../media/console-demo-log-button.msft.png":::
   Ilustración 9: el resultado del `console.log()` ejemplo  
:::image-end:::  

---  

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

:::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="El resultado del ejemplo de Console. Table ()" lightbox="../media/console-demo-table-button.msft.png":::
   Ilustración 10: el resultado del `console.table()` ejemplo  
:::image-end:::  

---  

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

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="El resultado del ejemplo de Console. Time ()" lightbox="../media/console-demo-time-button.msft.png":::
   Ilustración 11: el resultado del `console.time()` ejemplo  
:::image-end:::  

---  

## timeEnd  

```javascript
console.timeEnd([label])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Detiene un temporizador.  Consulta el método de [hora](#time) .  

---  

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

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="El resultado del ejemplo de Console. Trace ()" lightbox="../media/console-demo-trace-button.msft.png":::
   Ilustración 12: el resultado del `console.trace()` ejemplo  
:::image-end:::  

---  

## advertir  

```javascript
console.warn(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Warning`  

Imprime una advertencia en la consola.  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="El resultado del ejemplo de Console. WARN ()" lightbox="../media/console-demo-warn-button.msft.png":::
   Ilustración 13: el resultado del `console.warn()` ejemplo  
:::image-end:::  

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

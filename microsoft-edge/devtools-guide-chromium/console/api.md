---
description: Use la API de consola para escribir mensajes en la consola.
title: Referencia de api de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f38a7403cf11fbec5f5833fc0b1ed10207b436de
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398052"
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

# <a name="console-api-reference"></a>Referencia de api de consola  

Use los métodos de la API de consola para escribir mensajes en la consola desde JavaScript.  Para obtener una introducción interactiva al tema, vaya a Introducción al registro [de mensajes en la consola][DevtoolsConsoleLog].  Para los métodos de comodidad como o que solo están disponibles en el panel Consola, vaya a `debug()` Console Utilities API `monitorEvents()` [Reference][DevtoolConsoleUtilities]. ****  

---  

## <a name="assert"></a>assert  

```javascript
console.assert(expression, object)
```

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

Escribe un [error en](#error) la consola cuando se evalúa como `expression` `false` .  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="El resultado del ejemplo console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
   Figura 1: El resultado del `console.assert()` ejemplo  
:::image-end:::  

---  

## <a name="clear"></a>clear  

```javascript
console.clear()
```

Borra la consola.  

```javascript
console.clear();  
```  

Si [Preserve Log][DevtoolsConsoleReferenceLevel] está habilitado, el método [clear](#clear) está deshabilitado.  

### <a name="see-also"></a>Consulte también  

*   [Borrar la consola][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a>count  

```javascript
console.count([label])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Escribe el número de veces que se ha invocado el [método count](#count) en la misma línea y con la misma `label` .  Use el [método countReset](#countreset) para restablecer el recuento.  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="El resultado del ejemplo console.count()" lightbox="../media/console-demo-count-button.msft.png":::
   Figura 2: El resultado del `console.count()` ejemplo  
:::image-end:::  

---  

## <a name="countreset"></a>countReset  

```javascript
console.countReset([label])
```  

Restablece un recuento.  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## <a name="debug"></a>depurar  

```javascript
console.debug(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Verbose`

Idéntico al [registro excepto](#log) a otro nivel de registro.  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="El resultado del ejemplo console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
   Figura 3: El resultado del `console.debug()` ejemplo  
:::image-end:::  

---  

## <a name="dir"></a>dir  

```javascript
console.dir(object)
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Imprime una representación JSON del objeto especificado.  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="El resultado del ejemplo console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
   Figura 4: El resultado del `console.dir()` ejemplo  
:::image-end:::  

---  

## <a name="dirxml"></a>dirxml  

```javascript
console.dirxml(node)
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Imprime una representación XML de los descendientes de `node` .  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="El resultado del ejemplo console.dirxml()" lightbox="../media/console-demo-dirxml-button.msft.png":::
   Figura 5: El resultado del `console.dirxml()` ejemplo  
:::image-end:::  

---  

## <a name="error"></a>error  

```javascript
console.error(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Error`  

Imprime la `object` consola, la da formato como un error e incluye un seguimiento de la pila.  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="El resultado del ejemplo console.error()" lightbox="../media/console-demo-error-button.msft.png":::
   Figura 6: El resultado del `console.error()` ejemplo  
:::image-end:::  

---  

## <a name="group"></a>grupo  

```javascript
console.group(label)
```  

Agrupa visualmente mensajes hasta que [se usa el método groupEnd.](#groupend)  Use el [método groupCollapsed](#groupcollapsed) para contraer el grupo cuando se registra inicialmente en la consola.  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

:::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="El resultado del ejemplo console.group()" lightbox="../media/console-demo-group-button.msft.png":::
   Figura 7: El resultado del `console.group()` ejemplo  
:::image-end:::  

---  

## <a name="groupcollapsed"></a>groupCollapsed  

```javascript
console.groupCollapsed(label)
```  

Igual que el [método de registro,](#log) excepto que el grupo se contrae inicialmente cuando se registra en la consola.  

---  

## <a name="groupend"></a>groupEnd  

```javascript
console.groupEnd(label)
```  

Detiene la agrupación visual de mensajes.  Vaya al [método group.](#group)  

---  

## <a name="info"></a>información  

```javascript
console.info(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Idéntico al método [log.](#log)  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="El resultado del ejemplo console.info()" lightbox="../media/console-demo-info-button.msft.png":::
   Figura 8: El resultado del `console.info()` ejemplo  
:::image-end:::  

---  

## <a name="log"></a>log  

```javascript
console.log(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Imprime un mensaje en la consola.  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="El resultado del ejemplo console.log()" lightbox="../media/console-demo-log-button.msft.png":::
   Figura 9: El resultado del `console.log()` ejemplo  
:::image-end:::  

---  

## <a name="table"></a>tabla  

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

:::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="El resultado del ejemplo console.table()" lightbox="../media/console-demo-table-button.msft.png":::
   Figura 10: El resultado del `console.table()` ejemplo  
:::image-end:::  

---  

## <a name="time"></a>time  

```javascript
console.time([label])
```  

Inicia un nuevo temporizador.  Use el [método timeEnd](#timeend) para detener el temporizador e imprimir el tiempo transcurrido en la consola.  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="El resultado del ejemplo console.time()" lightbox="../media/console-demo-time-button.msft.png":::
   Figura 11: El resultado del `console.time()` ejemplo  
:::image-end:::  

---  

## <a name="timeend"></a>timeEnd  

```javascript
console.timeEnd([label])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Detiene un temporizador.  Vaya al método [time.](#time)  

---  

## <a name="trace"></a>seguimiento  

```javascript
console.trace()
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

Imprime un seguimiento de pila en la consola.  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="El resultado del ejemplo console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
   Figura 12: El resultado del `console.trace()` ejemplo  
:::image-end:::  

---  

## <a name="warn"></a>warn  

```javascript
console.warn(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Warning`  

Imprime una advertencia en la consola.  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="El resultado del ejemplo console.warn()" lightbox="../media/console-demo-warn-button.msft.png":::
   Figura 13: El resultado del `console.warn()` ejemplo  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Introducción al registro de mensajes en la consola"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Referencia de api de utilidades de consola"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Borrar la consola: referencia de consola"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Persist messages across page loads - Console Reference"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrar por nivel de registro: referencia de consola"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (Chromium)"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/api) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

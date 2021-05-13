---
description: Use la API de consola para escribir mensajes en la consola.
title: Referencia de la API de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 08a29db4dec05de0a21a0e6a9de9a0fb6e0d3f56
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564521"
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
# <a name="console-api-reference"></a>Referencia de la API de consola  

La **herramienta Consola** es útil cuando se completan varias tareas en DevTools.  Las API están disponibles para incluir en los scripts. Los métodos de comodidad solo están disponibles para su uso en la **herramienta Consola,** como los `debug()` métodos `monitorEvents()` and.  Para obtener más información sobre cómo empezar con la **consola,** vaya a Introducción al registro [de mensajes en la consola][DevtoolsConsoleConsoleLog].  Para obtener más información sobre los métodos de comodidad en **la consola,** vaya a [Console Utilities API Reference][DevtoolConsoleUtilities].  

---  

## <a name="assert"></a>assert  

Este método escribe un [error](#error) en la **consola** cuando `expression` se evalúa como `false` .  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.assert(expression, object)
```

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Error`  

### <a name="javascript-example"></a>Ejemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      const x = 5;
      const y = 3;
      const reason = 'x is expected to be less than y';
      console.assert(x < y, {x, y, reason});
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Salida
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="El resultado del ejemplo console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
         El resultado del `console.assert()` ejemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="clear"></a>clear  

Este método borra la **consola**.  

Si [Preserve Log][DevtoolsConsoleReferenceFilter] está activado, el método [clear](#clear) se desactivará.  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.clear()
```

### <a name="javascript-example"></a>Ejemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.clear();  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Salida
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

### <a name="see-also"></a>Consulte también  

*   [Borrar la consola][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a>count  

Este método escribe el número de veces que el [método count](#count) se ha invocado en la misma línea y con la misma `label` .  Use el [método countReset](#countreset) para restablecer el recuento.  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.count([label])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Ejemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.count();
      console.count('coffee');
      console.count();
      console.count();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Salida
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="El resultado del ejemplo console.count()" lightbox="../media/console-demo-count-button.msft.png":::
         El resultado del `console.count()` ejemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="countreset"></a>countReset  

Este método restablece un recuento.  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.countReset([label])
```  

### <a name="javascript-example"></a>Ejemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.countReset();
      console.countReset('coffee');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Salida
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

---  

## <a name="debug"></a>depurar  

Este método es idéntico al método [log,](#log) excepto el nivel de registro diferente.  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.debug(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Verbose`  

### <a name="javascript-example"></a>Ejemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.debug('debug');  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Salida
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="El resultado del ejemplo console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
         El resultado del `console.debug()` ejemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dir"></a>dir  

Este método imprime una representación JSON del objeto especificado.  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.dir(object)
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Ejemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dir(document.head);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Salida
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="El resultado del ejemplo console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
         El resultado del `console.dir()` ejemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dirxml"></a>dirxml  

Este método imprime una representación XML de los descendientes de `node` .  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.dirxml(node)
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Ejemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dirxml(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Salida
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="El resultado del ejemplo console.dirxml()" lightbox="../media/console-demo-dirxml-button.msft.png":::
         El resultado del `console.dirxml()` ejemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="error"></a>error  

Este método imprime la consola, la da `object` formato como un error e incluye un seguimiento de la pila. ****  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.error(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Error`  

### <a name="javascript-example"></a>Ejemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Salida
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="El resultado del ejemplo console.error()" lightbox="../media/console-demo-error-button.msft.png":::
         El resultado del `console.error()` ejemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="group"></a>grupo  

Este método agrupa visualmente mensajes hasta que se usa el [método groupEnd.](#groupend)  Use el [método groupCollapsed](#groupcollapsed) para contraer el grupo cuando inicia sesión inicialmente en la **consola**.  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.group(label)
```  

### <a name="javascript-example"></a>Ejemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      const label = 'Adolescent Irradiated Espionage Tortoises';
      console.group(label);
      console.info('Leo');
      console.info('Mike');
      console.info('Don');
      console.info('Raph');
      console.groupEnd(label);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Salida
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="El resultado del ejemplo console.group()" lightbox="../media/console-demo-group-button.msft.png":::
         El resultado del `console.group()` ejemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="groupcollapsed"></a>groupCollapsed  

Este método es idéntico al método [log,](#log) excepto que el grupo se contrae inicialmente cuando inicia sesión en la **consola**.  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.groupCollapsed(label)
```  

---  

## <a name="groupend"></a>groupEnd  

Este método detiene la agrupación visual de mensajes.  Vaya al [método group.](#group)  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.groupEnd(label)
```  

---  

## <a name="info"></a>información  

Este método es idéntico al método [log.](#log)  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.info(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Ejemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.info('info');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Salida
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="El resultado del ejemplo console.info()" lightbox="../media/console-demo-info-button.msft.png":::
         El resultado del `console.info()` ejemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="log"></a>log  

Este método imprime un mensaje en la **consola**.  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.log(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Ejemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.log('log');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Salida
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="El resultado del ejemplo console.log()" lightbox="../media/console-demo-log-button.msft.png":::
         El resultado del `console.log()` ejemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a>tabla  

Este método registra una matriz de objetos como una tabla.  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.table(array)
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Ejemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
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
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Salida
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="El resultado del ejemplo console.table()" lightbox="../media/console-demo-table-button.msft.png":::
         El resultado del `console.table()` ejemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="time"></a>time  

Este método inicia un nuevo temporizador.  Utilice el [método timeEnd](#timeend) para detener el temporizador e imprimir el tiempo transcurrido en la **consola**.  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.time([label])
```  

### <a name="javascript-example"></a>Ejemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.time();
      for (var i = 0; i < 100000; i++) {
          let square = i ** 2;
      }
      console.timeEnd();
      ```
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Salida
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="El resultado del ejemplo console.time()" lightbox="../media/console-demo-time-button.msft.png":::
         El resultado del `console.time()` ejemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="timeend"></a>timeEnd  

Este método detiene un temporizador.  Para obtener más información, vaya al [método time.](#time)  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.timeEnd([label])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

---  

## <a name="trace"></a>seguimiento  

Este método imprime un seguimiento de pila en la **consola**.  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.trace()
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Info`  

### <a name="javascript-example"></a>Ejemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      const first = () => { second(); };
      const second = () => { third(); };
      const third = () => { fourth(); };
      const fourth = () => { console.trace(); };
      first();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Salida
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="El resultado del ejemplo console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
         El resultado del `console.trace()` ejemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="warn"></a>warn  

Este método imprime una advertencia en la **consola**.  

### <a name="javascript-syntax"></a>Sintaxis de JavaScript  

```javascript
console.warn(object [, object, ...])
```  

[Nivel de registro][DevtoolsConsoleReferencePersist]: `Warning`  

### <a name="javascript-example"></a>Ejemplo de JavaScript  

:::row:::
   :::column span="1":::
      Entrada  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.warn('warn');
      ```
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Salida
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="El resultado del ejemplo console.warn()" lightbox="../media/console-demo-warn-button.msft.png":::
         El resultado del `console.warn()` ejemplo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleLog]: ./console-log.md "Inicia sesión en la herramienta consola | Microsoft Docs"  
[DevtoolConsoleUtilities]: ./utilities.md "Referencia de api de utilidades de consola | Microsoft Docs"  
[DevtoolsConsoleReferenceClear]: ./reference.md#clear-the-console "Borrar la consola: referencia de consola | Microsoft Docs"  
[DevtoolsConsoleReferenceFilter]: ./reference.md#filter-by-log-level "Filtrar por nivel de registro: referencia de consola | Microsoft Docs"  
[DevtoolsConsoleReferencePersist]: ./reference.md#persist-messages-across-page-loads "Conservar mensajes entre cargas de página: referencia de consola | Microsoft Docs"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Introducción a las herramientas de desarrollador de Microsoft Edge (Chromium) | Microsoft Docs"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/api) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

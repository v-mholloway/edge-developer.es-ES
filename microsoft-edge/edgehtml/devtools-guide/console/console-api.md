---
description: Usar la API de consola para depurar y perfilar el código mediante programación
title: DevTools-consola-API de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, API de consola
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 46a74b80b504358ff7dbea40970528c8e2b228cf
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236032"
---
# API de la consola

La *API de consola* ofrece acceso a la línea de comandos y mediante programación a la consola de DevTools a través del `console` objeto global, lo que permite:

 - [Registrar mensajes personalizados](#logging-custom-messages) de tu código
 - [Inspeccionar objetos y elementos](#inspecting-objects-and-elements) y registrar su información
 - [Pruebe y mida su código](#testing-and-measuring) estableciendo aserciones, temporizadores y contadores
 - [Tomar instantáneas del montón](#taking-heap-snapshots) para evaluar el consumo de memoria del código que se está ejecutando y para identificar pérdidas de memoria
 - Realiza [un seguimiento de tu callstacks](#tracing-callstacks) para saber dónde se llama a tu código 
 - [Organice su salida de registro](#organizing-log-output) para simplificar la depuración

A continuación se muestran los comandos y los parámetros de formato compatibles actualmente con Microsoft Edge. Funcionan de forma similar en exploradores principales.

## Registrar mensajes personalizados

El código puede enviar varios tipos de mensajes personalizados a la consola, entre los que se incluyen:

Tipo de mensaje  | &nbsp;   |
:------------------- | :------ |
[**error ()**](https://developer.mozilla.org/docs/Web/API/Console/error) y [ **excepción ()**](https://developer.mozilla.org/docs/Web/API/Console/error)| Errores graves y errores
[**WARN ()**](https://developer.mozilla.org/docs/Web/API/Console/warn) | Posibles errores o comportamientos inesperados 
[**info ()**](https://developer.mozilla.org/docs/Web/API/Console/info) | Información útil, pero no crítica
[**log ()**](https://developer.mozilla.org/docs/Web/API/Console/log) y [ **debug ()**](https://developer.mozilla.org/docs/Web/API/Console/log) | Depuración general (sin generar un icono de alerta del sistema en la consola)

   
Puedes agruparlos y filtrarlos junto con el resto de los mensajes generados desde Microsoft Edge desde el panel de la consola. Todos los métodos de mensaje personalizados requieren un parámetro de cadena (mensaje) y parámetros de sustitución de formato opcional. Microsoft Edge admite las siguientes opciones de formato:

Parámetro de formato | &nbsp;
:------------------- | :--- |
**% b** | Binario
**% c** | Estilo CSS en línea (vea el ejemplo siguiente)
**% d**, **% i** | Integer 
**% f** | Flotante  
**% s** | Cadena 
**% x** | Hexadecimal 
**% e** | Exponente 

Por ejemplo, aquí se muestra cómo incluir variables de cadena y de enteros en el mensaje de registro:

```javascript
var myText = 'pieces';
var myVal = 5;
console.log("The number of %s is %d.", myText, myVal);
```

>`The number of pieces is 5.`

Y aquí se muestra cómo puede Agregar un efecto de resaltado verde a un mensaje de registro con CSS en línea ( `%c` ):

```javascript
console.log("%cHighlight this log message in green", "background-color: #10ff00; text-transform: uppercase;");
```

![Registro de consola con estilos en línea](../media/console_api_css.png)

## Inspeccionar objetos y elementos

Los objetos inspeccionables aparecen en la consola en una vista de árbol contraída con nodos expansibles. La consola detecta si está enviando un nodo DOM (como un div) o un objeto de JavaScript (como un evento) y los muestra automáticamente como el tipo detectado.

También puede forzar una salida específica:

Comando | &nbsp;
:------------------- | :--- |
[**DIR ()**](https://developer.mozilla.org/docs/Web/API/Console/dir) | Se muestra como objeto de JavaScript inspeccionable
[**dirxml()**](https://developer.mozilla.org/docs/Web/API/Console/dirxml) | Se muestra como un nodo DOM inspeccionable

Por ejemplo, intente abrir la consola y compare los resultados siguientes con el `<div id='main'>` elemento de esta página:

```javascript
console.dir(document.querySelector('#main'));
console.dirxml(document.querySelector('#main'));
```

![Comparación de ' dir ' con la salida de ' dirxml '](../media/console_api_dir.png)

### Selección de un elemento en el panel **elementos**

Puede seleccionar un elemento dentro del contexto de árbol HTML de la página directamente desde la consola para el diseño inmediato y la depuración de estilo.

Comando | &nbsp;
:------------------- | :--- |
**seleccionar ()** | Cambia al panel **elementos** y establece el foco en el elemento especificado.

Por ejemplo, si abre la consola en esta página y escribe:

```javascript
console.select(document.querySelector("body"));
```

El DevTools cambiará al panel **elementos** (si aún no es el actual) y establecerá el foco en la [*vista de árbol html*](../elements.md#html-tree-view) en el elemento especificado.

![Ejemplo del método ' Select '](../media/console_api_select.png)

## Pruebas y medición

### Probar el código

Agrega aserciones de prueba de la API de consola al código para las pruebas unitarias y la depuración del código a medida que se ejecuta en el explorador.

Comando | &nbsp;
:------------ | :-------------
[**Assert ()**](https://developer.mozilla.org/docs/Web/API/Console/assert) | Registra un mensaje de error de consola si la expresión proporcionada se evalúa como *falso*.

Además de la expresión lógica que suministre como aserción, puede Agregar un mensaje opcional y parámetros de formato como usaría con otros [mensajes de consola personalizados](#logging-custom-messages). Por ejemplo:

```javascript
var x = 26.8;
console.assert(x < 25, 'The value of x is %f (it is NOT less than %i)', x, 25);
```

![Ejemplo del método ' Assert '](../media/console_api_assert.png)

### Contar las ejecuciones en el código

Puedes establecer contadores en el código para seguir el número de veces que se ejecuta el código circundante. El establecimiento de contadores puede ayudar a garantizar que el código se ejecuta según lo esperado y ayudarle a diagnosticar los cuellos de botella de rendimiento.

Comando | &nbsp;
:------------ | :-------------
[**contar ()**](https://developer.mozilla.org/docs/Web/API/Console/count) | Incrementos y registros se ha ejecutado el número de veces que se ha realizado la *cuenta ()* para la etiqueta dada.
[**countReset()**](https://developer.mozilla.org/docs/Web/API/Console/countReset) | Restablece el recuento a cero para la etiqueta de contador dada.

Por ejemplo, ejecutando las siguientes líneas en la consola:

```javascript
console.count('My Counter');
console.count('My Counter');
console.countReset('My Counter');
console.count('My Counter');
```

 . . . dará como resultado:
> Mi contador: 1

### Cómo cronometrar tu código

Instrumente tu código con los temporizadores etiquetados para medir cuánto tiempo se tarda en completar una determinada operación.

Comando | &nbsp;
:------------ | :-------------
[**hora ()**](https://developer.mozilla.org/docs/Web/API/Console/time) | Inicia un temporizador con la etiqueta dada.
[**timeEnd()**](https://developer.mozilla.org/docs/Web/API/Console/timeEnd) | Finaliza el temporizador con la etiqueta dada e informa del tiempo transcurrido (en milisegundos).
[**timeStamp ()**](https://developer.mozilla.org/docs/Web/API/Console/timeStamp) | Informa de la hora actual del sistema (en milisegundos).

Por ejemplo, intente ejecutar las siguientes líneas en la consola:

```javascript
console.time('My Timer');
console.timeEnd('My Timer');
```

### Tomar instantáneas de montones

Tomar instantáneas del montón para evaluar el consumo de memoria del código que se está ejecutando y para identificar las pérdidas de memoria.

Comando | &nbsp;
:------------ | :-------------
**takeHeapSnapshot()** | Captura detalles sobre el montón de JavaScript actual y los objetos asignados.

El [generador de perfiles de memoria](../memory.md#toolbar) de DevTools debe estar ejecutándose para poder tomar instantáneas de montones. Cada instantánea aparecerá como un mosaico en el [*Resumen de instantáneas*](../memory.md#snapshot-summary) del panel [**memoria**](../memory.md) para una posterior inspección.

## Seguimiento callstacks

Comprender desde dónde se llama el código, qué código se ejecuta y cuánto tiempo tarda la ejecución puede ser útil para analizar la lentitud o el comportamiento inesperado. Un seguimiento de pila muestra la ruta de ejecución que el código ha tomado para comunicarse con él, desde la solicitud de seguimiento hacia arriba a través de la ruta de acceso. 

Comando | &nbsp;
:------------ | :-------------
[**Trace ()**](https://developer.mozilla.org/docs/Web/API/Console/trace) | Genera un seguimiento de la pila de llamadas de ejecución de script actuales.

Por ejemplo, ejecutando el siguiente código en la consola:

```javascript
function a(){
  c();
}
function b(){
  c();
}
function c(){
  console.trace()
}
function d(){
  b();
}

a();
d();
```

. . . dará como resultado los siguientes seguimientos de la pila:
> Console. Trace () en c (código de evaluación: 8:3) a (código de evaluación: 2:3) en código de evaluación (código de evaluación: 14:1)
> 
> Console. Trace () en c (código de evaluación: 8:3) en b (código de evaluación: 5:3) en d (código de evaluación: 11:3) en código de evaluación (código de evaluación: 15:1)

## Organizar la salida del registro

Para borrar simplemente todo el resultado de la consola anterior, usa *Console. Clear ()* (o `CTRL + L` ). Esto no elimina la configuración de la pila de comandos de la consola (aún puede recorrerla con las teclas de flecha arriba y abajo).

Comando | &nbsp;
:------------ | :-------------
[**borrar ()**](https://developer.mozilla.org/docs/Web/API/Console/clear) | Borra todo el resultado de la consola anterior.

Si el código genera una gran cantidad de mensajes de consola, puedes organizarlos visualmente en bloques anidados con los siguientes comandos:

 Comando | &nbsp;
:------------ | :-------------
[**Group ()**](https://developer.mozilla.org/docs/Web/API/Console/group) | Inicia un nuevo nivel de anidamiento de la salida de la consola con la etiqueta especificada (optional).
[**groupCollapsed()**](https://developer.mozilla.org/docs/Web/API/Console/groupCollapsed) | Inicia un nuevo nivel de anidamiento de la salida de la consola con la etiqueta especificada (opcional), sin embargo, el control de agrupación se contrae de forma predeterminada y debe expandirse (haciendo clic en el control de flecha) para mostrar el resultado secundario.
[**groupEnd()**](https://developer.mozilla.org/docs/Web/API/Console/groupEnd) | Termina el grupo de anidamiento de la etiqueta especificada.

Por ejemplo, pruebe a escribir los siguientes comandos en la consola:

```javascript
console.groupCollapsed('Group 1');
console.log('In Group 1');
console.groupCollapsed('Group 1.1');
console.log('In Group 1.1');
console.groupEnd('Group 1.1');
console.groupEnd('Group 1');
console.log('No longer in a group');
```

. . . a continuación, expanda los controles *Grupo 1* y *Grupo 1,1* para ver cómo se anidan los comentarios del registro:

![Agrupar mensajes en la consola](../media/console_api_group.png)

A veces es más fácil visualizar un objeto o matriz de JavaScript en formato tabular, en lugar de una lista plana. Para ello, puedes usar el comando *Console. Table ()* :

Comando | &nbsp;
:------------ | :-------------
[**Table ()**](https://developer.mozilla.org/docs/Web/API/Console/table) | Envía la matriz u objeto suministrados a la consola en formato de tabla.

Por ejemplo, la siguiente matriz de objetos:

```javascript
var orders = [{'Size':'XL', 'Quantity':1},{'Size':'M', 'Quantity':3}, {'Size':'L', 'Quantity':2}];
console.table(orders);
```

. . . se representará como esta tabla en la consola:

![Mostrar una matriz de objetos como una tabla en la consola](../media/console_api_table.png)

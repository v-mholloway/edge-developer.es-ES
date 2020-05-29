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





# <span data-ttu-id="e8895-103">Referencia de la API de consola</span><span class="sxs-lookup"><span data-stu-id="e8895-103">Console API Reference</span></span>   

  

<span data-ttu-id="e8895-104">Usa los métodos de la API de consola para escribir mensajes en la consola desde tu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e8895-104">Use the Console API methods to write messages to the Console from your JavaScript.</span></span>  <span data-ttu-id="e8895-105">Consulte Introducción al [registro de mensajes en la consola][DevtoolsConsoleLog] para obtener una introducción interactiva al tema.</span><span class="sxs-lookup"><span data-stu-id="e8895-105">See [Get Started With Logging Messages To The Console][DevtoolsConsoleLog] for an interactive introduction to the topic.</span></span>  <span data-ttu-id="e8895-106">Consulte [referencia] [DevtoolConsoleUtilities] de la API de utilidades de consola si busca los métodos útiles como `debug()` o `monitorEvents()` que solo están disponibles en la consola.</span><span class="sxs-lookup"><span data-stu-id="e8895-106">See [Console Utilities API Reference] [DevtoolConsoleUtilities] if you are looking for the convenience methods like `debug()` or `monitorEvents()` which are only available from the Console.</span></span>  

## <span data-ttu-id="e8895-107">aserciones</span><span class="sxs-lookup"><span data-stu-id="e8895-107">assert</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="e8895-108">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="e8895-108">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

<span data-ttu-id="e8895-109">Escribe un [error](#error) en la consola cuando `expression` se evalúa en `false` .</span><span class="sxs-lookup"><span data-stu-id="e8895-109">Writes an [error](#error) to the console when `expression` evaluates to `false`.</span></span>  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

> ##### <span data-ttu-id="e8895-110">Figura 1</span><span class="sxs-lookup"><span data-stu-id="e8895-110">Figure 1</span></span>  
> <span data-ttu-id="e8895-111">El resultado del `console.assert()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8895-111">The result of the `console.assert()` example</span></span>  
> ![El resultado del ejemplo de Console. Assert ()][ImageAssert]  

## <span data-ttu-id="e8895-113">Libere</span><span class="sxs-lookup"><span data-stu-id="e8895-113">clear</span></span>  

```javascript
console.clear()
```

<span data-ttu-id="e8895-114">Borra la consola.</span><span class="sxs-lookup"><span data-stu-id="e8895-114">Clears the console.</span></span>  

```javascript
console.clear();  
```  

<span data-ttu-id="e8895-115">Si se habilita [preservar registro][DevtoolsConsoleReferenceLevel] , el método [Borrar](#clear) estará desactivado.</span><span class="sxs-lookup"><span data-stu-id="e8895-115">If [Preserve Log][DevtoolsConsoleReferenceLevel] is enabled, the [clear](#clear) method is disabled.</span></span>  

<span data-ttu-id="e8895-116">Consulte también: [borrar la consola][DevtoolsConsoleReferenceClear]</span><span class="sxs-lookup"><span data-stu-id="e8895-116">See also: [Clear the Console][DevtoolsConsoleReferenceClear]</span></span>  

## <span data-ttu-id="e8895-117">encuentra</span><span class="sxs-lookup"><span data-stu-id="e8895-117">count</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="e8895-118">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="e8895-118">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="e8895-119">Escribe el número de veces que se ha invocado al método [Count](#count) en la misma línea y con el mismo `label` .</span><span class="sxs-lookup"><span data-stu-id="e8895-119">Writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="e8895-120">Usa el método [countReset](#countreset) para restablecer el recuento.</span><span class="sxs-lookup"><span data-stu-id="e8895-120">Use the [countReset](#countreset) method to reset the count.</span></span>  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

> ##### <span data-ttu-id="e8895-121">Figura 2</span><span class="sxs-lookup"><span data-stu-id="e8895-121">Figure 2</span></span>  
> <span data-ttu-id="e8895-122">El resultado del `console.count()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8895-122">The result of the `console.count()` example</span></span>  
> ![El resultado del ejemplo de Console. Count ()][ImageCount]  

## <span data-ttu-id="e8895-124">countReset</span><span class="sxs-lookup"><span data-stu-id="e8895-124">countReset</span></span>  

```javascript
console.countReset([label])
```  

<span data-ttu-id="e8895-125">Restablece un recuento.</span><span class="sxs-lookup"><span data-stu-id="e8895-125">Resets a count.</span></span>  

```javascript
console.countReset();
console.countReset('coffee');
```  

## <span data-ttu-id="e8895-126">depurar</span><span class="sxs-lookup"><span data-stu-id="e8895-126">debug</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="e8895-127">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="e8895-127">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="e8895-128">Es idéntico al método de [registro](#log) .</span><span class="sxs-lookup"><span data-stu-id="e8895-128">Identical to the [log](#log) method.</span></span>  

```javascript
console.debug('debug');  
```  

> ##### <span data-ttu-id="e8895-129">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="e8895-129">Figure 3</span></span>  
> <span data-ttu-id="e8895-130">El resultado del `console.debug()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8895-130">The result of the `console.debug()` example</span></span>  
> ![El resultado del ejemplo de Console. debug ()][ImageDebug]  

## <span data-ttu-id="e8895-132">dir</span><span class="sxs-lookup"><span data-stu-id="e8895-132">dir</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="e8895-133">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="e8895-133">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="e8895-134">Imprime una representación JSON del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="e8895-134">Prints a JSON representation of the specified object.</span></span>  

```javascript
console.dir(document.head);
```  

> ##### <span data-ttu-id="e8895-135">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="e8895-135">Figure 4</span></span>  
> <span data-ttu-id="e8895-136">El resultado del `console.dir()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8895-136">The result of the `console.dir()` example</span></span>  
> ![El resultado del ejemplo de Console. dir ()][ImageDir]  

## <span data-ttu-id="e8895-138">dirxml</span><span class="sxs-lookup"><span data-stu-id="e8895-138">dirxml</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="e8895-139">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="e8895-139">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="e8895-140">Imprime una representación XML de los descendientes de `node` .</span><span class="sxs-lookup"><span data-stu-id="e8895-140">Prints an XML representation of the descendants of `node`.</span></span>  

```javascript
console.dirxml(document);
```  

> ##### <span data-ttu-id="e8895-141">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="e8895-141">Figure 5</span></span>  
> <span data-ttu-id="e8895-142">El resultado del `console.dirxml()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8895-142">The result of the `console.dirxml()` example</span></span>  
> ![El resultado del ejemplo de Console. dirxml ()][ImageDirXml]  

## <span data-ttu-id="e8895-144">error</span><span class="sxs-lookup"><span data-stu-id="e8895-144">error</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="e8895-145">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="e8895-145">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<span data-ttu-id="e8895-146">Imprime `object` en la consola, le da formato de error e incluye un seguimiento de la pila.</span><span class="sxs-lookup"><span data-stu-id="e8895-146">Prints the `object` to the Console, formats it as an error, and includes a stack trace.</span></span>  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

> ##### <span data-ttu-id="e8895-147">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="e8895-147">Figure 6</span></span>  
> <span data-ttu-id="e8895-148">El resultado del `console.error()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8895-148">The result of the `console.error()` example</span></span>  
> ![El resultado de la consola. ejemplo de error ()][ImageError]  

## <span data-ttu-id="e8895-150">grupo</span><span class="sxs-lookup"><span data-stu-id="e8895-150">group</span></span>  

```javascript
console.group(label)
```  

<span data-ttu-id="e8895-151">Agrupa visualmente los mensajes hasta que se usa el método [groupEnd](#groupend) .</span><span class="sxs-lookup"><span data-stu-id="e8895-151">Visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="e8895-152">Use el método [groupCollapsed](#groupcollapsed) para contraer el grupo cuando se haya registrado inicialmente en la consola.</span><span class="sxs-lookup"><span data-stu-id="e8895-152">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it is initially logged to the Console.</span></span>  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

> ##### <span data-ttu-id="e8895-153">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="e8895-153">Figure 7</span></span>  
> <span data-ttu-id="e8895-154">El resultado del `console.group()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8895-154">The result of the `console.group()` example</span></span>  
> ![El resultado del ejemplo de Console. Group ()][ImageGroup]  

## <span data-ttu-id="e8895-156">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="e8895-156">groupCollapsed</span></span>  

```javascript
console.groupCollapsed(label)
```  

<span data-ttu-id="e8895-157">Igual que el método [log](#log) , excepto que el grupo se contraiga inicialmente cuando se registra en la consola.</span><span class="sxs-lookup"><span data-stu-id="e8895-157">Same as the [log](#log) method, except the group is initially collapsed when it is logged to the Console.</span></span>  

## <span data-ttu-id="e8895-158">groupEnd</span><span class="sxs-lookup"><span data-stu-id="e8895-158">groupEnd</span></span>  

```javascript
console.groupEnd(label)
```  

<span data-ttu-id="e8895-159">Detiene la agrupación visual de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e8895-159">Stops visually grouping messages.</span></span>  <span data-ttu-id="e8895-160">Consulta el método [Group](#group) .</span><span class="sxs-lookup"><span data-stu-id="e8895-160">See the [group](#group) method.</span></span>  

## <span data-ttu-id="e8895-161">información</span><span class="sxs-lookup"><span data-stu-id="e8895-161">info</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="e8895-162">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="e8895-162">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="e8895-163">Es idéntico al método de [registro](#log) .</span><span class="sxs-lookup"><span data-stu-id="e8895-163">Identical to the [log](#log) method.</span></span>  

```javascript
console.info('info');
```  

> ##### <span data-ttu-id="e8895-164">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="e8895-164">Figure 8</span></span>  
> <span data-ttu-id="e8895-165">El resultado del `console.info()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8895-165">The result of the `console.info()` example</span></span>  
> ![El resultado del ejemplo console.info ()][ImageInfo]  

## <span data-ttu-id="e8895-167">registros</span><span class="sxs-lookup"><span data-stu-id="e8895-167">log</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="e8895-168">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="e8895-168">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="e8895-169">Imprime un mensaje en la consola.</span><span class="sxs-lookup"><span data-stu-id="e8895-169">Prints a message to the Console.</span></span>  

```javascript
console.log('log');
```  

> ##### <span data-ttu-id="e8895-170">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="e8895-170">Figure 9</span></span>  
> <span data-ttu-id="e8895-171">El resultado del `console.log()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8895-171">The result of the `console.log()` example</span></span>  
> ![El resultado del ejemplo de Console. log ()][ImageLog]  

## <span data-ttu-id="e8895-173">Table</span><span class="sxs-lookup"><span data-stu-id="e8895-173">table</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="e8895-174">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="e8895-174">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="e8895-175">Registra una matriz de objetos como una tabla.</span><span class="sxs-lookup"><span data-stu-id="e8895-175">Logs an array of objects as a table.</span></span>  

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

> ##### <span data-ttu-id="e8895-176">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="e8895-176">Figure 10</span></span>  
> <span data-ttu-id="e8895-177">El resultado del `console.table()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8895-177">The result of the `console.table()` example</span></span>  
> ![El resultado del ejemplo de Console. Table ()][ImageTable]  

## <span data-ttu-id="e8895-179">time</span><span class="sxs-lookup"><span data-stu-id="e8895-179">time</span></span>  

```javascript
console.time([label])
```  

<span data-ttu-id="e8895-180">Inicia un nuevo temporizador.</span><span class="sxs-lookup"><span data-stu-id="e8895-180">Starts a new timer.</span></span>  <span data-ttu-id="e8895-181">Use el método [timeEnd](#timeend) para detener el temporizador e imprimir el tiempo transcurrido en la consola.</span><span class="sxs-lookup"><span data-stu-id="e8895-181">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the Console.</span></span>  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

> ##### <span data-ttu-id="e8895-182">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="e8895-182">Figure 11</span></span>  
> <span data-ttu-id="e8895-183">El resultado del `console.time()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8895-183">The result of the `console.time()` example</span></span>  
> ![El resultado del ejemplo de Console. Time ()][ImageTime]  

## <span data-ttu-id="e8895-185">timeEnd</span><span class="sxs-lookup"><span data-stu-id="e8895-185">timeEnd</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="e8895-186">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="e8895-186">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="e8895-187">Detiene un temporizador.</span><span class="sxs-lookup"><span data-stu-id="e8895-187">Stops a timer.</span></span>  <span data-ttu-id="e8895-188">Consulta el método de [hora](#time) .</span><span class="sxs-lookup"><span data-stu-id="e8895-188">See the [time](#time) method.</span></span>  

## <span data-ttu-id="e8895-189">trazabilidad</span><span class="sxs-lookup"><span data-stu-id="e8895-189">trace</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="e8895-190">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="e8895-190">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="e8895-191">Imprime un seguimiento de la pila en la consola.</span><span class="sxs-lookup"><span data-stu-id="e8895-191">Prints a stack trace to the Console.</span></span>  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

> ##### <span data-ttu-id="e8895-192">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="e8895-192">Figure 12</span></span>  
> <span data-ttu-id="e8895-193">El resultado del `console.trace()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8895-193">The result of the `console.trace()` example</span></span>  
> ![El resultado del ejemplo de Console. Trace ()][ImageTrace]  

## <span data-ttu-id="e8895-195">advertir</span><span class="sxs-lookup"><span data-stu-id="e8895-195">warn</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="e8895-196">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="e8895-196">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

<span data-ttu-id="e8895-197">Imprime una advertencia en la consola.</span><span class="sxs-lookup"><span data-stu-id="e8895-197">Prints a warning to the Console.</span></span>  

```javascript
console.warn('warn');
```  

> ##### <span data-ttu-id="e8895-198">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="e8895-198">Figure 13</span></span>  
> <span data-ttu-id="e8895-199">El resultado del `console.warn()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8895-199">The result of the `console.warn()` example</span></span>  
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
> <span data-ttu-id="e8895-220">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e8895-220">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e8895-221">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/api) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e8895-221">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e8895-223">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e8895-223">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

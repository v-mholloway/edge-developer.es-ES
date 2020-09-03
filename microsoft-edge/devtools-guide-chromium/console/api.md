---
description: Use la API de consola para escribir mensajes en la consola.
title: Referencia de la API de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 684c0a1e42357ceca0a0295859e64447251f191a
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993257"
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

# <span data-ttu-id="9f749-104">Referencia de la API de consola</span><span class="sxs-lookup"><span data-stu-id="9f749-104">Console API Reference</span></span>  

<span data-ttu-id="9f749-105">Usa los métodos de la API de consola para escribir mensajes en la consola desde tu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9f749-105">Use the Console API methods to write messages to the Console from your JavaScript.</span></span>  <span data-ttu-id="9f749-106">Para obtener una introducción interactiva al tema, consulte Introducción al [registro de mensajes en la consola][DevtoolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="9f749-106">For an interactive introduction to the topic, see [Get Started With Logging Messages To The Console][DevtoolsConsoleLog].</span></span>  <span data-ttu-id="9f749-107">Para obtener los métodos útiles como `debug()` o `monitorEvents()` que solo están disponibles en el panel de **consola** , consulte referencia de API de utilidades de [consola][DevtoolConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="9f749-107">For the convenience methods like `debug()` or `monitorEvents()` which are only available from the **Console** pane, see [Console Utilities API Reference][DevtoolConsoleUtilities].</span></span>  

---  

## <span data-ttu-id="9f749-108">aserciones</span><span class="sxs-lookup"><span data-stu-id="9f749-108">assert</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="9f749-109">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="9f749-109">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

<span data-ttu-id="9f749-110">Escribe un [error](#error) en la consola cuando `expression` se evalúa en `false` .</span><span class="sxs-lookup"><span data-stu-id="9f749-110">Writes an [error](#error) to the console when `expression` evaluates to `false`.</span></span>  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="El resultado del ejemplo de Console. Assert ()" lightbox="../media/console-demo-assert-button.msft.png":::
   <span data-ttu-id="9f749-112">Ilustración 1: el resultado del `console.assert()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f749-112">Figure 1:  The result of the `console.assert()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="9f749-113">Libere</span><span class="sxs-lookup"><span data-stu-id="9f749-113">clear</span></span>  

```javascript
console.clear()
```

<span data-ttu-id="9f749-114">Borra la consola.</span><span class="sxs-lookup"><span data-stu-id="9f749-114">Clears the console.</span></span>  

```javascript
console.clear();  
```  

<span data-ttu-id="9f749-115">Si se habilita [preservar registro][DevtoolsConsoleReferenceLevel] , el método [Borrar](#clear) estará desactivado.</span><span class="sxs-lookup"><span data-stu-id="9f749-115">If [Preserve Log][DevtoolsConsoleReferenceLevel] is enabled, the [clear](#clear) method is disabled.</span></span>  

### <span data-ttu-id="9f749-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9f749-116">See also</span></span>  

*   [<span data-ttu-id="9f749-117">Borrar la consola</span><span class="sxs-lookup"><span data-stu-id="9f749-117">Clear the Console</span></span>][DevtoolsConsoleReferenceClear]  

---  

## <span data-ttu-id="9f749-118">encuentra</span><span class="sxs-lookup"><span data-stu-id="9f749-118">count</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="9f749-119">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="9f749-119">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="9f749-120">Escribe el número de veces que se ha invocado al método [Count](#count) en la misma línea y con el mismo `label` .</span><span class="sxs-lookup"><span data-stu-id="9f749-120">Writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="9f749-121">Usa el método [countReset](#countreset) para restablecer el recuento.</span><span class="sxs-lookup"><span data-stu-id="9f749-121">Use the [countReset](#countreset) method to reset the count.</span></span>  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="El resultado del ejemplo de Console. Count ()" lightbox="../media/console-demo-count-button.msft.png":::
   <span data-ttu-id="9f749-123">Ilustración 2: el resultado del `console.count()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f749-123">Figure 2:  The result of the `console.count()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="9f749-124">countReset</span><span class="sxs-lookup"><span data-stu-id="9f749-124">countReset</span></span>  

```javascript
console.countReset([label])
```  

<span data-ttu-id="9f749-125">Restablece un recuento.</span><span class="sxs-lookup"><span data-stu-id="9f749-125">Resets a count.</span></span>  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## <span data-ttu-id="9f749-126">depurar</span><span class="sxs-lookup"><span data-stu-id="9f749-126">debug</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="9f749-127">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="9f749-127">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Verbose`

<span data-ttu-id="9f749-128">Es idéntico a [log](#log) , excepto el nivel de registro diferente.</span><span class="sxs-lookup"><span data-stu-id="9f749-128">Identical to [log](#log) except different log level.</span></span>  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="El resultado del ejemplo de Console. debug ()" lightbox="../media/console-demo-debug-button.msft.png":::
   <span data-ttu-id="9f749-130">Ilustración 3: el resultado del `console.debug()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f749-130">Figure 3:  The result of the `console.debug()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="9f749-131">dir</span><span class="sxs-lookup"><span data-stu-id="9f749-131">dir</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="9f749-132">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="9f749-132">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="9f749-133">Imprime una representación JSON del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="9f749-133">Prints a JSON representation of the specified object.</span></span>  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="El resultado del ejemplo de Console. dir ()" lightbox="../media/console-demo-dir-button.msft.png":::
   <span data-ttu-id="9f749-135">Ilustración 4: el resultado del `console.dir()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f749-135">Figure 4:  The result of the `console.dir()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="9f749-136">dirxml</span><span class="sxs-lookup"><span data-stu-id="9f749-136">dirxml</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="9f749-137">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="9f749-137">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="9f749-138">Imprime una representación XML de los descendientes de `node` .</span><span class="sxs-lookup"><span data-stu-id="9f749-138">Prints an XML representation of the descendants of `node`.</span></span>  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="El resultado del ejemplo de Console. dirxml ()" lightbox="../media/console-demo-dirxml-button.msft.png":::
   <span data-ttu-id="9f749-140">Ilustración 5: el resultado del `console.dirxml()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f749-140">Figure 5:  The result of the `console.dirxml()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="9f749-141">error</span><span class="sxs-lookup"><span data-stu-id="9f749-141">error</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="9f749-142">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="9f749-142">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<span data-ttu-id="9f749-143">Imprime `object` en la consola, le da formato de error e incluye un seguimiento de la pila.</span><span class="sxs-lookup"><span data-stu-id="9f749-143">Prints the `object` to the Console, formats it as an error, and includes a stack trace.</span></span>  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="El resultado de la consola. ejemplo de error ()" lightbox="../media/console-demo-error-button.msft.png":::
   <span data-ttu-id="9f749-145">Ilustración 6: el resultado del `console.error()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f749-145">Figure 6:  The result of the `console.error()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="9f749-146">grupo</span><span class="sxs-lookup"><span data-stu-id="9f749-146">group</span></span>  

```javascript
console.group(label)
```  

<span data-ttu-id="9f749-147">Agrupa visualmente los mensajes hasta que se usa el método [groupEnd](#groupend) .</span><span class="sxs-lookup"><span data-stu-id="9f749-147">Visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="9f749-148">Use el método [groupCollapsed](#groupcollapsed) para contraer el grupo cuando se haya registrado inicialmente en la consola.</span><span class="sxs-lookup"><span data-stu-id="9f749-148">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it is initially logged to the Console.</span></span>  

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
   <span data-ttu-id="9f749-150">Ilustración 7: el resultado del `console.group()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f749-150">Figure 7:  The result of the `console.group()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="9f749-151">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="9f749-151">groupCollapsed</span></span>  

```javascript
console.groupCollapsed(label)
```  

<span data-ttu-id="9f749-152">Igual que el método [log](#log) , excepto que el grupo se contraiga inicialmente cuando se registra en la consola.</span><span class="sxs-lookup"><span data-stu-id="9f749-152">Same as the [log](#log) method, except the group is initially collapsed when it is logged to the Console.</span></span>  

---  

## <span data-ttu-id="9f749-153">groupEnd</span><span class="sxs-lookup"><span data-stu-id="9f749-153">groupEnd</span></span>  

```javascript
console.groupEnd(label)
```  

<span data-ttu-id="9f749-154">Detiene la agrupación visual de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9f749-154">Stops visually grouping messages.</span></span>  <span data-ttu-id="9f749-155">Consulta el método [Group](#group) .</span><span class="sxs-lookup"><span data-stu-id="9f749-155">See the [group](#group) method.</span></span>  

---  

## <span data-ttu-id="9f749-156">información</span><span class="sxs-lookup"><span data-stu-id="9f749-156">info</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="9f749-157">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="9f749-157">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="9f749-158">Es idéntico al método de [registro](#log) .</span><span class="sxs-lookup"><span data-stu-id="9f749-158">Identical to the [log](#log) method.</span></span>  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="El resultado del ejemplo console.info ()" lightbox="../media/console-demo-info-button.msft.png":::
   <span data-ttu-id="9f749-160">Ilustración 8: el resultado del `console.info()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f749-160">Figure 8:  The result of the `console.info()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="9f749-161">registros</span><span class="sxs-lookup"><span data-stu-id="9f749-161">log</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="9f749-162">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="9f749-162">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="9f749-163">Imprime un mensaje en la consola.</span><span class="sxs-lookup"><span data-stu-id="9f749-163">Prints a message to the Console.</span></span>  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="El resultado del ejemplo de Console. log ()" lightbox="../media/console-demo-log-button.msft.png":::
   <span data-ttu-id="9f749-165">Ilustración 9: el resultado del `console.log()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f749-165">Figure 9:  The result of the `console.log()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="9f749-166">Table</span><span class="sxs-lookup"><span data-stu-id="9f749-166">table</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="9f749-167">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="9f749-167">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="9f749-168">Registra una matriz de objetos como una tabla.</span><span class="sxs-lookup"><span data-stu-id="9f749-168">Logs an array of objects as a table.</span></span>  

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
   <span data-ttu-id="9f749-170">Ilustración 10: el resultado del `console.table()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f749-170">Figure 10:  The result of the `console.table()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="9f749-171">time</span><span class="sxs-lookup"><span data-stu-id="9f749-171">time</span></span>  

```javascript
console.time([label])
```  

<span data-ttu-id="9f749-172">Inicia un nuevo temporizador.</span><span class="sxs-lookup"><span data-stu-id="9f749-172">Starts a new timer.</span></span>  <span data-ttu-id="9f749-173">Use el método [timeEnd](#timeend) para detener el temporizador e imprimir el tiempo transcurrido en la consola.</span><span class="sxs-lookup"><span data-stu-id="9f749-173">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the Console.</span></span>  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="El resultado del ejemplo de Console. Time ()" lightbox="../media/console-demo-time-button.msft.png":::
   <span data-ttu-id="9f749-175">Ilustración 11: el resultado del `console.time()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f749-175">Figure 11:  The result of the `console.time()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="9f749-176">timeEnd</span><span class="sxs-lookup"><span data-stu-id="9f749-176">timeEnd</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="9f749-177">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="9f749-177">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="9f749-178">Detiene un temporizador.</span><span class="sxs-lookup"><span data-stu-id="9f749-178">Stops a timer.</span></span>  <span data-ttu-id="9f749-179">Consulta el método de [hora](#time) .</span><span class="sxs-lookup"><span data-stu-id="9f749-179">See the [time](#time) method.</span></span>  

---  

## <span data-ttu-id="9f749-180">trazabilidad</span><span class="sxs-lookup"><span data-stu-id="9f749-180">trace</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="9f749-181">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="9f749-181">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="9f749-182">Imprime un seguimiento de la pila en la consola.</span><span class="sxs-lookup"><span data-stu-id="9f749-182">Prints a stack trace to the Console.</span></span>  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="El resultado del ejemplo de Console. Trace ()" lightbox="../media/console-demo-trace-button.msft.png":::
   <span data-ttu-id="9f749-184">Ilustración 12: el resultado del `console.trace()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f749-184">Figure 12:  The result of the `console.trace()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="9f749-185">advertir</span><span class="sxs-lookup"><span data-stu-id="9f749-185">warn</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="9f749-186">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="9f749-186">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

<span data-ttu-id="9f749-187">Imprime una advertencia en la consola.</span><span class="sxs-lookup"><span data-stu-id="9f749-187">Prints a warning to the Console.</span></span>  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="El resultado del ejemplo de Console. WARN ()" lightbox="../media/console-demo-warn-button.msft.png":::
   <span data-ttu-id="9f749-189">Ilustración 13: el resultado del `console.warn()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f749-189">Figure 13:  The result of the `console.warn()` example</span></span>  
:::image-end:::  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Introducción al registro de mensajes en la consola"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Referencia de API de utilidades de consola"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Borrar la consola: referencia de consola"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Conservar mensajes en la carga de páginas: referencia de consola"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrar por nivel de registro-referencia de consola"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  

> [!NOTE]
> <span data-ttu-id="9f749-196">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9f749-196">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9f749-197">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/api) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="9f749-197">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9f749-199">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9f749-199">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

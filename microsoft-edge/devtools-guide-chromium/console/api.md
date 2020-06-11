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

# <span data-ttu-id="f7556-103">Referencia de la API de consola</span><span class="sxs-lookup"><span data-stu-id="f7556-103">Console API Reference</span></span>  

<span data-ttu-id="f7556-104">Usa los métodos de la API de consola para escribir mensajes en la consola desde tu JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f7556-104">Use the Console API methods to write messages to the Console from your JavaScript.</span></span>  <span data-ttu-id="f7556-105">Para obtener una introducción interactiva al tema, consulte Introducción al [registro de mensajes en la consola][DevtoolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="f7556-105">For an interactive introduction to the topic, see [Get Started With Logging Messages To The Console][DevtoolsConsoleLog].</span></span>  <span data-ttu-id="f7556-106">Para obtener los métodos útiles como `debug()` o `monitorEvents()` que solo están disponibles en el panel de **consola** , consulte referencia de API de utilidades de [consola][DevtoolConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="f7556-106">For the convenience methods like `debug()` or `monitorEvents()` which are only available from the **Console** pane, see [Console Utilities API Reference][DevtoolConsoleUtilities].</span></span>  

---  

## <span data-ttu-id="f7556-107">aserciones</span><span class="sxs-lookup"><span data-stu-id="f7556-107">assert</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="f7556-108">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="f7556-108">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

<span data-ttu-id="f7556-109">Escribe un [error](#error) en la consola cuando `expression` se evalúa en `false` .</span><span class="sxs-lookup"><span data-stu-id="f7556-109">Writes an [error](#error) to the console when `expression` evaluates to `false`.</span></span>  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="El resultado del ejemplo de Console. Assert ()" lightbox="../media/console-demo-assert-button.msft.png":::
   <span data-ttu-id="f7556-111">Ilustración 1: el resultado del `console.assert()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7556-111">Figure 1:  The result of the `console.assert()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="f7556-112">Libere</span><span class="sxs-lookup"><span data-stu-id="f7556-112">clear</span></span>  

```javascript
console.clear()
```

<span data-ttu-id="f7556-113">Borra la consola.</span><span class="sxs-lookup"><span data-stu-id="f7556-113">Clears the console.</span></span>  

```javascript
console.clear();  
```  

<span data-ttu-id="f7556-114">Si se habilita [preservar registro][DevtoolsConsoleReferenceLevel] , el método [Borrar](#clear) estará desactivado.</span><span class="sxs-lookup"><span data-stu-id="f7556-114">If [Preserve Log][DevtoolsConsoleReferenceLevel] is enabled, the [clear](#clear) method is disabled.</span></span>  

### <span data-ttu-id="f7556-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f7556-115">See also</span></span>  

*   [<span data-ttu-id="f7556-116">Borrar la consola</span><span class="sxs-lookup"><span data-stu-id="f7556-116">Clear the Console</span></span>][DevtoolsConsoleReferenceClear]  

---  

## <span data-ttu-id="f7556-117">encuentra</span><span class="sxs-lookup"><span data-stu-id="f7556-117">count</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="f7556-118">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="f7556-118">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="f7556-119">Escribe el número de veces que se ha invocado al método [Count](#count) en la misma línea y con el mismo `label` .</span><span class="sxs-lookup"><span data-stu-id="f7556-119">Writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="f7556-120">Usa el método [countReset](#countreset) para restablecer el recuento.</span><span class="sxs-lookup"><span data-stu-id="f7556-120">Use the [countReset](#countreset) method to reset the count.</span></span>  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="El resultado del ejemplo de Console. Count ()" lightbox="../media/console-demo-count-button.msft.png":::
   <span data-ttu-id="f7556-122">Ilustración 2: el resultado del `console.count()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7556-122">Figure 2:  The result of the `console.count()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="f7556-123">countReset</span><span class="sxs-lookup"><span data-stu-id="f7556-123">countReset</span></span>  

```javascript
console.countReset([label])
```  

<span data-ttu-id="f7556-124">Restablece un recuento.</span><span class="sxs-lookup"><span data-stu-id="f7556-124">Resets a count.</span></span>  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## <span data-ttu-id="f7556-125">depurar</span><span class="sxs-lookup"><span data-stu-id="f7556-125">debug</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="f7556-126">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="f7556-126">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Verbose`

<span data-ttu-id="f7556-127">Es idéntico a [log](#log) , excepto el nivel de registro diferente.</span><span class="sxs-lookup"><span data-stu-id="f7556-127">Identical to [log](#log) except different log level.</span></span>  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="El resultado del ejemplo de Console. debug ()" lightbox="../media/console-demo-debug-button.msft.png":::
   <span data-ttu-id="f7556-129">Ilustración 3: el resultado del `console.debug()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7556-129">Figure 3:  The result of the `console.debug()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="f7556-130">dir</span><span class="sxs-lookup"><span data-stu-id="f7556-130">dir</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="f7556-131">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="f7556-131">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="f7556-132">Imprime una representación JSON del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="f7556-132">Prints a JSON representation of the specified object.</span></span>  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="El resultado del ejemplo de Console. dir ()" lightbox="../media/console-demo-dir-button.msft.png":::
   <span data-ttu-id="f7556-134">Ilustración 4: el resultado del `console.dir()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7556-134">Figure 4:  The result of the `console.dir()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="f7556-135">dirxml</span><span class="sxs-lookup"><span data-stu-id="f7556-135">dirxml</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="f7556-136">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="f7556-136">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="f7556-137">Imprime una representación XML de los descendientes de `node` .</span><span class="sxs-lookup"><span data-stu-id="f7556-137">Prints an XML representation of the descendants of `node`.</span></span>  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="El resultado del ejemplo de Console. dirxml ()" lightbox="../media/console-demo-dirxml-button.msft.png":::
   <span data-ttu-id="f7556-139">Ilustración 5: el resultado del `console.dirxml()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7556-139">Figure 5:  The result of the `console.dirxml()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="f7556-140">error</span><span class="sxs-lookup"><span data-stu-id="f7556-140">error</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="f7556-141">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="f7556-141">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<span data-ttu-id="f7556-142">Imprime `object` en la consola, le da formato de error e incluye un seguimiento de la pila.</span><span class="sxs-lookup"><span data-stu-id="f7556-142">Prints the `object` to the Console, formats it as an error, and includes a stack trace.</span></span>  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="El resultado de la consola. ejemplo de error ()" lightbox="../media/console-demo-error-button.msft.png":::
   <span data-ttu-id="f7556-144">Ilustración 6: el resultado del `console.error()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7556-144">Figure 6:  The result of the `console.error()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="f7556-145">grupo</span><span class="sxs-lookup"><span data-stu-id="f7556-145">group</span></span>  

```javascript
console.group(label)
```  

<span data-ttu-id="f7556-146">Agrupa visualmente los mensajes hasta que se usa el método [groupEnd](#groupend) .</span><span class="sxs-lookup"><span data-stu-id="f7556-146">Visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="f7556-147">Use el método [groupCollapsed](#groupcollapsed) para contraer el grupo cuando se haya registrado inicialmente en la consola.</span><span class="sxs-lookup"><span data-stu-id="f7556-147">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it is initially logged to the Console.</span></span>  

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
   <span data-ttu-id="f7556-149">Ilustración 7: el resultado del `console.group()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7556-149">Figure 7:  The result of the `console.group()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="f7556-150">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="f7556-150">groupCollapsed</span></span>  

```javascript
console.groupCollapsed(label)
```  

<span data-ttu-id="f7556-151">Igual que el método [log](#log) , excepto que el grupo se contraiga inicialmente cuando se registra en la consola.</span><span class="sxs-lookup"><span data-stu-id="f7556-151">Same as the [log](#log) method, except the group is initially collapsed when it is logged to the Console.</span></span>  

---  

## <span data-ttu-id="f7556-152">groupEnd</span><span class="sxs-lookup"><span data-stu-id="f7556-152">groupEnd</span></span>  

```javascript
console.groupEnd(label)
```  

<span data-ttu-id="f7556-153">Detiene la agrupación visual de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f7556-153">Stops visually grouping messages.</span></span>  <span data-ttu-id="f7556-154">Consulta el método [Group](#group) .</span><span class="sxs-lookup"><span data-stu-id="f7556-154">See the [group](#group) method.</span></span>  

---  

## <span data-ttu-id="f7556-155">información</span><span class="sxs-lookup"><span data-stu-id="f7556-155">info</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="f7556-156">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="f7556-156">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="f7556-157">Es idéntico al método de [registro](#log) .</span><span class="sxs-lookup"><span data-stu-id="f7556-157">Identical to the [log](#log) method.</span></span>  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="El resultado del ejemplo console.info ()" lightbox="../media/console-demo-info-button.msft.png":::
   <span data-ttu-id="f7556-159">Ilustración 8: el resultado del `console.info()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7556-159">Figure 8:  The result of the `console.info()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="f7556-160">registros</span><span class="sxs-lookup"><span data-stu-id="f7556-160">log</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="f7556-161">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="f7556-161">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="f7556-162">Imprime un mensaje en la consola.</span><span class="sxs-lookup"><span data-stu-id="f7556-162">Prints a message to the Console.</span></span>  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="El resultado del ejemplo de Console. log ()" lightbox="../media/console-demo-log-button.msft.png":::
   <span data-ttu-id="f7556-164">Ilustración 9: el resultado del `console.log()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7556-164">Figure 9:  The result of the `console.log()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="f7556-165">Table</span><span class="sxs-lookup"><span data-stu-id="f7556-165">table</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="f7556-166">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="f7556-166">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="f7556-167">Registra una matriz de objetos como una tabla.</span><span class="sxs-lookup"><span data-stu-id="f7556-167">Logs an array of objects as a table.</span></span>  

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
   <span data-ttu-id="f7556-169">Ilustración 10: el resultado del `console.table()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7556-169">Figure 10:  The result of the `console.table()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="f7556-170">time</span><span class="sxs-lookup"><span data-stu-id="f7556-170">time</span></span>  

```javascript
console.time([label])
```  

<span data-ttu-id="f7556-171">Inicia un nuevo temporizador.</span><span class="sxs-lookup"><span data-stu-id="f7556-171">Starts a new timer.</span></span>  <span data-ttu-id="f7556-172">Use el método [timeEnd](#timeend) para detener el temporizador e imprimir el tiempo transcurrido en la consola.</span><span class="sxs-lookup"><span data-stu-id="f7556-172">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the Console.</span></span>  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="El resultado del ejemplo de Console. Time ()" lightbox="../media/console-demo-time-button.msft.png":::
   <span data-ttu-id="f7556-174">Ilustración 11: el resultado del `console.time()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7556-174">Figure 11:  The result of the `console.time()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="f7556-175">timeEnd</span><span class="sxs-lookup"><span data-stu-id="f7556-175">timeEnd</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="f7556-176">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="f7556-176">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="f7556-177">Detiene un temporizador.</span><span class="sxs-lookup"><span data-stu-id="f7556-177">Stops a timer.</span></span>  <span data-ttu-id="f7556-178">Consulta el método de [hora](#time) .</span><span class="sxs-lookup"><span data-stu-id="f7556-178">See the [time](#time) method.</span></span>  

---  

## <span data-ttu-id="f7556-179">trazabilidad</span><span class="sxs-lookup"><span data-stu-id="f7556-179">trace</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="f7556-180">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="f7556-180">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="f7556-181">Imprime un seguimiento de la pila en la consola.</span><span class="sxs-lookup"><span data-stu-id="f7556-181">Prints a stack trace to the Console.</span></span>  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="El resultado del ejemplo de Console. Trace ()" lightbox="../media/console-demo-trace-button.msft.png":::
   <span data-ttu-id="f7556-183">Ilustración 12: el resultado del `console.trace()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7556-183">Figure 12:  The result of the `console.trace()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="f7556-184">advertir</span><span class="sxs-lookup"><span data-stu-id="f7556-184">warn</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="f7556-185">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="f7556-185">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

<span data-ttu-id="f7556-186">Imprime una advertencia en la consola.</span><span class="sxs-lookup"><span data-stu-id="f7556-186">Prints a warning to the Console.</span></span>  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="El resultado del ejemplo de Console. WARN ()" lightbox="../media/console-demo-warn-button.msft.png":::
   <span data-ttu-id="f7556-188">Ilustración 13: el resultado del `console.warn()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7556-188">Figure 13:  The result of the `console.warn()` example</span></span>  
:::image-end:::  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Introducción al registro de mensajes en la consola"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Referencia de API de utilidades de consola"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Borrar la consola: referencia de consola"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Conservar mensajes en la carga de páginas: referencia de consola"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrar por nivel de registro-referencia de consola"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  

> [!NOTE]
> <span data-ttu-id="f7556-195">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f7556-195">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f7556-196">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/api) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="f7556-196">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f7556-198">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f7556-198">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

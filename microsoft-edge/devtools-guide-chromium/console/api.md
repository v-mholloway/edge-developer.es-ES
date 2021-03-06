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

# <a name="console-api-reference"></a><span data-ttu-id="7ffe4-104">Referencia de api de consola</span><span class="sxs-lookup"><span data-stu-id="7ffe4-104">Console API reference</span></span>  

<span data-ttu-id="7ffe4-105">Use los métodos de la API de consola para escribir mensajes en la consola desde JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-105">Use the Console API methods to write messages to the Console from your JavaScript.</span></span>  <span data-ttu-id="7ffe4-106">Para obtener una introducción interactiva al tema, vaya a Introducción al registro [de mensajes en la consola][DevtoolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="7ffe4-106">For an interactive introduction to the topic, navigate to [Get Started With Logging Messages To The Console][DevtoolsConsoleLog].</span></span>  <span data-ttu-id="7ffe4-107">Para los métodos de comodidad como o que solo están disponibles en el panel Consola, vaya a `debug()` Console Utilities API `monitorEvents()` [Reference][DevtoolConsoleUtilities]. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7ffe4-107">For the convenience methods like `debug()` or `monitorEvents()` which are only available from the **Console** pane, navigate to [Console Utilities API Reference][DevtoolConsoleUtilities].</span></span>  

---  

## <a name="assert"></a><span data-ttu-id="7ffe4-108">assert</span><span class="sxs-lookup"><span data-stu-id="7ffe4-108">assert</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="7ffe4-109">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="7ffe4-109">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

<span data-ttu-id="7ffe4-110">Escribe un [error en](#error) la consola cuando se evalúa como `expression` `false` .</span><span class="sxs-lookup"><span data-stu-id="7ffe4-110">Writes an [error](#error) to the console when `expression` evaluates to `false`.</span></span>  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="El resultado del ejemplo console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
   <span data-ttu-id="7ffe4-112">Figura 1: El resultado del `console.assert()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ffe4-112">Figure 1:  The result of the `console.assert()` example</span></span>  
:::image-end:::  

---  

## <a name="clear"></a><span data-ttu-id="7ffe4-113">clear</span><span class="sxs-lookup"><span data-stu-id="7ffe4-113">clear</span></span>  

```javascript
console.clear()
```

<span data-ttu-id="7ffe4-114">Borra la consola.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-114">Clears the console.</span></span>  

```javascript
console.clear();  
```  

<span data-ttu-id="7ffe4-115">Si [Preserve Log][DevtoolsConsoleReferenceLevel] está habilitado, el método [clear](#clear) está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-115">If [Preserve Log][DevtoolsConsoleReferenceLevel] is enabled, the [clear](#clear) method is disabled.</span></span>  

### <a name="see-also"></a><span data-ttu-id="7ffe4-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7ffe4-116">See also</span></span>  

*   [<span data-ttu-id="7ffe4-117">Borrar la consola</span><span class="sxs-lookup"><span data-stu-id="7ffe4-117">Clear the Console</span></span>][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a><span data-ttu-id="7ffe4-118">count</span><span class="sxs-lookup"><span data-stu-id="7ffe4-118">count</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="7ffe4-119">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="7ffe4-119">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="7ffe4-120">Escribe el número de veces que se ha invocado el [método count](#count) en la misma línea y con la misma `label` .</span><span class="sxs-lookup"><span data-stu-id="7ffe4-120">Writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="7ffe4-121">Use el [método countReset](#countreset) para restablecer el recuento.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-121">Use the [countReset](#countreset) method to reset the count.</span></span>  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="El resultado del ejemplo console.count()" lightbox="../media/console-demo-count-button.msft.png":::
   <span data-ttu-id="7ffe4-123">Figura 2: El resultado del `console.count()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ffe4-123">Figure 2:  The result of the `console.count()` example</span></span>  
:::image-end:::  

---  

## <a name="countreset"></a><span data-ttu-id="7ffe4-124">countReset</span><span class="sxs-lookup"><span data-stu-id="7ffe4-124">countReset</span></span>  

```javascript
console.countReset([label])
```  

<span data-ttu-id="7ffe4-125">Restablece un recuento.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-125">Resets a count.</span></span>  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## <a name="debug"></a><span data-ttu-id="7ffe4-126">depurar</span><span class="sxs-lookup"><span data-stu-id="7ffe4-126">debug</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="7ffe4-127">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="7ffe4-127">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Verbose`

<span data-ttu-id="7ffe4-128">Idéntico al [registro excepto](#log) a otro nivel de registro.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-128">Identical to [log](#log) except different log level.</span></span>  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="El resultado del ejemplo console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
   <span data-ttu-id="7ffe4-130">Figura 3: El resultado del `console.debug()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ffe4-130">Figure 3:  The result of the `console.debug()` example</span></span>  
:::image-end:::  

---  

## <a name="dir"></a><span data-ttu-id="7ffe4-131">dir</span><span class="sxs-lookup"><span data-stu-id="7ffe4-131">dir</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="7ffe4-132">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="7ffe4-132">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="7ffe4-133">Imprime una representación JSON del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-133">Prints a JSON representation of the specified object.</span></span>  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="El resultado del ejemplo console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
   <span data-ttu-id="7ffe4-135">Figura 4: El resultado del `console.dir()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ffe4-135">Figure 4:  The result of the `console.dir()` example</span></span>  
:::image-end:::  

---  

## <a name="dirxml"></a><span data-ttu-id="7ffe4-136">dirxml</span><span class="sxs-lookup"><span data-stu-id="7ffe4-136">dirxml</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="7ffe4-137">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="7ffe4-137">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="7ffe4-138">Imprime una representación XML de los descendientes de `node` .</span><span class="sxs-lookup"><span data-stu-id="7ffe4-138">Prints an XML representation of the descendants of `node`.</span></span>  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="El resultado del ejemplo console.dirxml()" lightbox="../media/console-demo-dirxml-button.msft.png":::
   <span data-ttu-id="7ffe4-140">Figura 5: El resultado del `console.dirxml()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ffe4-140">Figure 5:  The result of the `console.dirxml()` example</span></span>  
:::image-end:::  

---  

## <a name="error"></a><span data-ttu-id="7ffe4-141">error</span><span class="sxs-lookup"><span data-stu-id="7ffe4-141">error</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="7ffe4-142">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="7ffe4-142">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<span data-ttu-id="7ffe4-143">Imprime la `object` consola, la da formato como un error e incluye un seguimiento de la pila.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-143">Prints the `object` to the Console, formats it as an error, and includes a stack trace.</span></span>  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="El resultado del ejemplo console.error()" lightbox="../media/console-demo-error-button.msft.png":::
   <span data-ttu-id="7ffe4-145">Figura 6: El resultado del `console.error()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ffe4-145">Figure 6:  The result of the `console.error()` example</span></span>  
:::image-end:::  

---  

## <a name="group"></a><span data-ttu-id="7ffe4-146">grupo</span><span class="sxs-lookup"><span data-stu-id="7ffe4-146">group</span></span>  

```javascript
console.group(label)
```  

<span data-ttu-id="7ffe4-147">Agrupa visualmente mensajes hasta que [se usa el método groupEnd.](#groupend)</span><span class="sxs-lookup"><span data-stu-id="7ffe4-147">Visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="7ffe4-148">Use el [método groupCollapsed](#groupcollapsed) para contraer el grupo cuando se registra inicialmente en la consola.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-148">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it is initially logged to the Console.</span></span>  

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
   <span data-ttu-id="7ffe4-150">Figura 7: El resultado del `console.group()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ffe4-150">Figure 7:  The result of the `console.group()` example</span></span>  
:::image-end:::  

---  

## <a name="groupcollapsed"></a><span data-ttu-id="7ffe4-151">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="7ffe4-151">groupCollapsed</span></span>  

```javascript
console.groupCollapsed(label)
```  

<span data-ttu-id="7ffe4-152">Igual que el [método de registro,](#log) excepto que el grupo se contrae inicialmente cuando se registra en la consola.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-152">Same as the [log](#log) method, except the group is initially collapsed when it is logged to the Console.</span></span>  

---  

## <a name="groupend"></a><span data-ttu-id="7ffe4-153">groupEnd</span><span class="sxs-lookup"><span data-stu-id="7ffe4-153">groupEnd</span></span>  

```javascript
console.groupEnd(label)
```  

<span data-ttu-id="7ffe4-154">Detiene la agrupación visual de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-154">Stops visually grouping messages.</span></span>  <span data-ttu-id="7ffe4-155">Vaya al [método group.](#group)</span><span class="sxs-lookup"><span data-stu-id="7ffe4-155">Navigate to the [group](#group) method.</span></span>  

---  

## <a name="info"></a><span data-ttu-id="7ffe4-156">información</span><span class="sxs-lookup"><span data-stu-id="7ffe4-156">info</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="7ffe4-157">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="7ffe4-157">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="7ffe4-158">Idéntico al método [log.](#log)</span><span class="sxs-lookup"><span data-stu-id="7ffe4-158">Identical to the [log](#log) method.</span></span>  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="El resultado del ejemplo console.info()" lightbox="../media/console-demo-info-button.msft.png":::
   <span data-ttu-id="7ffe4-160">Figura 8: El resultado del `console.info()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ffe4-160">Figure 8:  The result of the `console.info()` example</span></span>  
:::image-end:::  

---  

## <a name="log"></a><span data-ttu-id="7ffe4-161">log</span><span class="sxs-lookup"><span data-stu-id="7ffe4-161">log</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="7ffe4-162">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="7ffe4-162">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="7ffe4-163">Imprime un mensaje en la consola.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-163">Prints a message to the Console.</span></span>  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="El resultado del ejemplo console.log()" lightbox="../media/console-demo-log-button.msft.png":::
   <span data-ttu-id="7ffe4-165">Figura 9: El resultado del `console.log()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ffe4-165">Figure 9:  The result of the `console.log()` example</span></span>  
:::image-end:::  

---  

## <a name="table"></a><span data-ttu-id="7ffe4-166">tabla</span><span class="sxs-lookup"><span data-stu-id="7ffe4-166">table</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="7ffe4-167">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="7ffe4-167">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="7ffe4-168">Registra una matriz de objetos como una tabla.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-168">Logs an array of objects as a table.</span></span>  

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
   <span data-ttu-id="7ffe4-170">Figura 10: El resultado del `console.table()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ffe4-170">Figure 10:  The result of the `console.table()` example</span></span>  
:::image-end:::  

---  

## <a name="time"></a><span data-ttu-id="7ffe4-171">time</span><span class="sxs-lookup"><span data-stu-id="7ffe4-171">time</span></span>  

```javascript
console.time([label])
```  

<span data-ttu-id="7ffe4-172">Inicia un nuevo temporizador.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-172">Starts a new timer.</span></span>  <span data-ttu-id="7ffe4-173">Use el [método timeEnd](#timeend) para detener el temporizador e imprimir el tiempo transcurrido en la consola.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-173">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the Console.</span></span>  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="El resultado del ejemplo console.time()" lightbox="../media/console-demo-time-button.msft.png":::
   <span data-ttu-id="7ffe4-175">Figura 11: El resultado del `console.time()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ffe4-175">Figure 11:  The result of the `console.time()` example</span></span>  
:::image-end:::  

---  

## <a name="timeend"></a><span data-ttu-id="7ffe4-176">timeEnd</span><span class="sxs-lookup"><span data-stu-id="7ffe4-176">timeEnd</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="7ffe4-177">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="7ffe4-177">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="7ffe4-178">Detiene un temporizador.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-178">Stops a timer.</span></span>  <span data-ttu-id="7ffe4-179">Vaya al método [time.](#time)</span><span class="sxs-lookup"><span data-stu-id="7ffe4-179">Navigate to the [time](#time) method.</span></span>  

---  

## <a name="trace"></a><span data-ttu-id="7ffe4-180">seguimiento</span><span class="sxs-lookup"><span data-stu-id="7ffe4-180">trace</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="7ffe4-181">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="7ffe4-181">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="7ffe4-182">Imprime un seguimiento de pila en la consola.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-182">Prints a stack trace to the Console.</span></span>  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="El resultado del ejemplo console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
   <span data-ttu-id="7ffe4-184">Figura 12: El resultado del `console.trace()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ffe4-184">Figure 12:  The result of the `console.trace()` example</span></span>  
:::image-end:::  

---  

## <a name="warn"></a><span data-ttu-id="7ffe4-185">warn</span><span class="sxs-lookup"><span data-stu-id="7ffe4-185">warn</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="7ffe4-186">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="7ffe4-186">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

<span data-ttu-id="7ffe4-187">Imprime una advertencia en la consola.</span><span class="sxs-lookup"><span data-stu-id="7ffe4-187">Prints a warning to the Console.</span></span>  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="El resultado del ejemplo console.warn()" lightbox="../media/console-demo-warn-button.msft.png":::
   <span data-ttu-id="7ffe4-189">Figura 13: El resultado del `console.warn()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ffe4-189">Figure 13:  The result of the `console.warn()` example</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="7ffe4-190">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7ffe4-190">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Introducción al registro de mensajes en la consola"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Referencia de api de utilidades de consola"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Borrar la consola: referencia de consola"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Persist messages across page loads - Console Reference"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Filtrar por nivel de registro: referencia de consola"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (Chromium)"  

> [!NOTE]
> <span data-ttu-id="7ffe4-197">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7ffe4-197">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7ffe4-198">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/api) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="7ffe4-198">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7ffe4-200">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7ffe4-200">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

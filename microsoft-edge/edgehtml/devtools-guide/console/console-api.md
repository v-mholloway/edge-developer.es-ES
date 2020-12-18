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
# <span data-ttu-id="4799a-104">API de la consola</span><span class="sxs-lookup"><span data-stu-id="4799a-104">Console API</span></span>

<span data-ttu-id="4799a-105">La *API de consola* ofrece acceso a la línea de comandos y mediante programación a la consola de DevTools a través del `console` objeto global, lo que permite:</span><span class="sxs-lookup"><span data-stu-id="4799a-105">The *Console API* provides command-line and programmatic access to the  DevTools Console through the global `console` object, allowing you to:</span></span>

 - <span data-ttu-id="4799a-106">[Registrar mensajes personalizados](#logging-custom-messages) de tu código</span><span class="sxs-lookup"><span data-stu-id="4799a-106">[Log custom messages](#logging-custom-messages) from you code</span></span>
 - <span data-ttu-id="4799a-107">[Inspeccionar objetos y elementos](#inspecting-objects-and-elements) y registrar su información</span><span class="sxs-lookup"><span data-stu-id="4799a-107">[Inspect objects and elements](#inspecting-objects-and-elements) and log their information</span></span>
 - <span data-ttu-id="4799a-108">[Pruebe y mida su código](#testing-and-measuring) estableciendo aserciones, temporizadores y contadores</span><span class="sxs-lookup"><span data-stu-id="4799a-108">[Test and measure your code](#testing-and-measuring) by setting assertions, timers and counters</span></span>
 - <span data-ttu-id="4799a-109">[Tomar instantáneas del montón](#taking-heap-snapshots) para evaluar el consumo de memoria del código que se está ejecutando y para identificar pérdidas de memoria</span><span class="sxs-lookup"><span data-stu-id="4799a-109">[Take snapshots of the heap](#taking-heap-snapshots) to assess the memory consumption of your running code and identify memory leaks</span></span>
 - <span data-ttu-id="4799a-110">Realiza [un seguimiento de tu callstacks](#tracing-callstacks) para saber dónde se llama a tu código</span><span class="sxs-lookup"><span data-stu-id="4799a-110">[Trace your callstacks](#tracing-callstacks) to understand where your code is being called from</span></span> 
 - <span data-ttu-id="4799a-111">[Organice su salida de registro](#organizing-log-output) para simplificar la depuración</span><span class="sxs-lookup"><span data-stu-id="4799a-111">[Organize your log output](#organizing-log-output) to streamline your debugging</span></span>

<span data-ttu-id="4799a-112">A continuación se muestran los comandos y los parámetros de formato compatibles actualmente con Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4799a-112">The following are the commands and formatting parameters currently supported by Microsoft Edge.</span></span> <span data-ttu-id="4799a-113">Funcionan de forma similar en exploradores principales.</span><span class="sxs-lookup"><span data-stu-id="4799a-113">They work similarly on major browsers.</span></span>

## <span data-ttu-id="4799a-114">Registrar mensajes personalizados</span><span class="sxs-lookup"><span data-stu-id="4799a-114">Logging custom messages</span></span>

<span data-ttu-id="4799a-115">El código puede enviar varios tipos de mensajes personalizados a la consola, entre los que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="4799a-115">Your code can send several types of custom messages to the console, including:</span></span>

<span data-ttu-id="4799a-116">Tipo de mensaje</span><span class="sxs-lookup"><span data-stu-id="4799a-116">Message type</span></span>  | &nbsp;   |
:------------------- | :------ |
<span data-ttu-id="4799a-117">[**error ()**](https://developer.mozilla.org/docs/Web/API/Console/error) y [ **excepción ()**](https://developer.mozilla.org/docs/Web/API/Console/error)</span><span class="sxs-lookup"><span data-stu-id="4799a-117">[**error()**](https://developer.mozilla.org/docs/Web/API/Console/error) and [**exception()**](https://developer.mozilla.org/docs/Web/API/Console/error)</span></span>| <span data-ttu-id="4799a-118">Errores graves y errores</span><span class="sxs-lookup"><span data-stu-id="4799a-118">Critical errors and failures</span></span>
[**<span data-ttu-id="4799a-119">WARN ()</span><span class="sxs-lookup"><span data-stu-id="4799a-119">warn()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/warn) | <span data-ttu-id="4799a-120">Posibles errores o comportamientos inesperados</span><span class="sxs-lookup"><span data-stu-id="4799a-120">Possible errors or unexpected behavior</span></span> 
[**<span data-ttu-id="4799a-121">info ()</span><span class="sxs-lookup"><span data-stu-id="4799a-121">info()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/info) | <span data-ttu-id="4799a-122">Información útil, pero no crítica</span><span class="sxs-lookup"><span data-stu-id="4799a-122">Useful, but non-critical information</span></span>
<span data-ttu-id="4799a-123">[**log ()**](https://developer.mozilla.org/docs/Web/API/Console/log) y [ **debug ()**](https://developer.mozilla.org/docs/Web/API/Console/log)</span><span class="sxs-lookup"><span data-stu-id="4799a-123">[**log()**](https://developer.mozilla.org/docs/Web/API/Console/log) and [**debug()**](https://developer.mozilla.org/docs/Web/API/Console/log)</span></span> | <span data-ttu-id="4799a-124">Depuración general (sin generar un icono de alerta del sistema en la consola)</span><span class="sxs-lookup"><span data-stu-id="4799a-124">General debugging (without generating a system alert icon in the console)</span></span>

   
<span data-ttu-id="4799a-125">Puedes agruparlos y filtrarlos junto con el resto de los mensajes generados desde Microsoft Edge desde el panel de la consola.</span><span class="sxs-lookup"><span data-stu-id="4799a-125">You can group and filter these along with the other messages generated from Microsoft Edge from the  Console panel.</span></span> <span data-ttu-id="4799a-126">Todos los métodos de mensaje personalizados requieren un parámetro de cadena (mensaje) y parámetros de sustitución de formato opcional.</span><span class="sxs-lookup"><span data-stu-id="4799a-126">All custom message methods require a string (message) parameter and optional format substitution parameters.</span></span> <span data-ttu-id="4799a-127">Microsoft Edge admite las siguientes opciones de formato:</span><span class="sxs-lookup"><span data-stu-id="4799a-127">Microsoft Edge supports the following formatting options:</span></span>

<span data-ttu-id="4799a-128">Parámetro de formato</span><span class="sxs-lookup"><span data-stu-id="4799a-128">Format parameter</span></span> | &nbsp;
:------------------- | :--- |
**<span data-ttu-id="4799a-129">% b</span><span class="sxs-lookup"><span data-stu-id="4799a-129">%b</span></span>** | <span data-ttu-id="4799a-130">Binario</span><span class="sxs-lookup"><span data-stu-id="4799a-130">Binary</span></span>
**<span data-ttu-id="4799a-131">% c</span><span class="sxs-lookup"><span data-stu-id="4799a-131">%c</span></span>** | <span data-ttu-id="4799a-132">Estilo CSS en línea (vea el ejemplo siguiente)</span><span class="sxs-lookup"><span data-stu-id="4799a-132">Inline CSS style (see example below)</span></span>
<span data-ttu-id="4799a-133">**% d**, **% i**</span><span class="sxs-lookup"><span data-stu-id="4799a-133">**%d**, **%i**</span></span> | <span data-ttu-id="4799a-134">Integer</span><span class="sxs-lookup"><span data-stu-id="4799a-134">Integer</span></span> 
**<span data-ttu-id="4799a-135">% f</span><span class="sxs-lookup"><span data-stu-id="4799a-135">%f</span></span>** | <span data-ttu-id="4799a-136">Flotante</span><span class="sxs-lookup"><span data-stu-id="4799a-136">Float</span></span>  
**<span data-ttu-id="4799a-137">% s</span><span class="sxs-lookup"><span data-stu-id="4799a-137">%s</span></span>** | <span data-ttu-id="4799a-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="4799a-138">String</span></span> 
**<span data-ttu-id="4799a-139">% x</span><span class="sxs-lookup"><span data-stu-id="4799a-139">%x</span></span>** | <span data-ttu-id="4799a-140">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="4799a-140">Hexadecimal</span></span> 
**<span data-ttu-id="4799a-141">% e</span><span class="sxs-lookup"><span data-stu-id="4799a-141">%e</span></span>** | <span data-ttu-id="4799a-142">Exponente</span><span class="sxs-lookup"><span data-stu-id="4799a-142">Exponent</span></span> 

<span data-ttu-id="4799a-143">Por ejemplo, aquí se muestra cómo incluir variables de cadena y de enteros en el mensaje de registro:</span><span class="sxs-lookup"><span data-stu-id="4799a-143">For example, here's how you would include string and integer variables in your log message:</span></span>

```javascript
var myText = 'pieces';
var myVal = 5;
console.log("The number of %s is %d.", myText, myVal);
```

>`The number of pieces is 5.`

<span data-ttu-id="4799a-144">Y aquí se muestra cómo puede Agregar un efecto de resaltado verde a un mensaje de registro con CSS en línea ( `%c` ):</span><span class="sxs-lookup"><span data-stu-id="4799a-144">And here's how you might add a green highlight effect to a log message with inline CSS (`%c`):</span></span>

```javascript
console.log("%cHighlight this log message in green", "background-color: #10ff00; text-transform: uppercase;");
```

![Registro de consola con estilos en línea](../media/console_api_css.png)

## <span data-ttu-id="4799a-146">Inspeccionar objetos y elementos</span><span class="sxs-lookup"><span data-stu-id="4799a-146">Inspecting objects and elements</span></span>

<span data-ttu-id="4799a-147">Los objetos inspeccionables aparecen en la consola en una vista de árbol contraída con nodos expansibles.</span><span class="sxs-lookup"><span data-stu-id="4799a-147">Inspectable objects appear in the console in a collapsed tree view with expandable nodes.</span></span> <span data-ttu-id="4799a-148">La consola detecta si está enviando un nodo DOM (como un div) o un objeto de JavaScript (como un evento) y los muestra automáticamente como el tipo detectado.</span><span class="sxs-lookup"><span data-stu-id="4799a-148">The console detects whether you are sending a DOM node (like a div) or a JavaScript object (like an event) and displays them as the detected type automatically.</span></span>

<span data-ttu-id="4799a-149">También puede forzar una salida específica:</span><span class="sxs-lookup"><span data-stu-id="4799a-149">You can also force a specific output:</span></span>

<span data-ttu-id="4799a-150">Comando</span><span class="sxs-lookup"><span data-stu-id="4799a-150">Command</span></span> | &nbsp;
:------------------- | :--- |
[**<span data-ttu-id="4799a-151">DIR ()</span><span class="sxs-lookup"><span data-stu-id="4799a-151">dir()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/dir) | <span data-ttu-id="4799a-152">Se muestra como objeto de JavaScript inspeccionable</span><span class="sxs-lookup"><span data-stu-id="4799a-152">Displays as inspectable JavaScript object</span></span>
[**<span data-ttu-id="4799a-153">dirxml()</span><span class="sxs-lookup"><span data-stu-id="4799a-153">dirxml()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/dirxml) | <span data-ttu-id="4799a-154">Se muestra como un nodo DOM inspeccionable</span><span class="sxs-lookup"><span data-stu-id="4799a-154">Displays as inspectable DOM node</span></span>

<span data-ttu-id="4799a-155">Por ejemplo, intente abrir la consola y compare los resultados siguientes con el `<div id='main'>` elemento de esta página:</span><span class="sxs-lookup"><span data-stu-id="4799a-155">For example, try opening the console and compare the following outputs for the `<div id='main'>` element on this page:</span></span>

```javascript
console.dir(document.querySelector('#main'));
console.dirxml(document.querySelector('#main'));
```

![Comparación de ' dir ' con la salida de ' dirxml '](../media/console_api_dir.png)

### <span data-ttu-id="4799a-157">Selección de un elemento en el panel **elementos**</span><span class="sxs-lookup"><span data-stu-id="4799a-157">Selecting an element in the **Elements** panel</span></span>

<span data-ttu-id="4799a-158">Puede seleccionar un elemento dentro del contexto de árbol HTML de la página directamente desde la consola para el diseño inmediato y la depuración de estilo.</span><span class="sxs-lookup"><span data-stu-id="4799a-158">You can select an element within the HTML tree context of the page directly from the console for immediate layout and style debugging.</span></span>

<span data-ttu-id="4799a-159">Comando</span><span class="sxs-lookup"><span data-stu-id="4799a-159">Command</span></span> | &nbsp;
:------------------- | :--- |
**<span data-ttu-id="4799a-160">seleccionar ()</span><span class="sxs-lookup"><span data-stu-id="4799a-160">select()</span></span>** | <span data-ttu-id="4799a-161">Cambia al panel **elementos** y establece el foco en el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="4799a-161">Switches to the **Elements** panel and sets focus to the specified element.</span></span>

<span data-ttu-id="4799a-162">Por ejemplo, si abre la consola en esta página y escribe:</span><span class="sxs-lookup"><span data-stu-id="4799a-162">For example, if you open the console on this page and type:</span></span>

```javascript
console.select(document.querySelector("body"));
```

<span data-ttu-id="4799a-163">El DevTools cambiará al panel **elementos** (si aún no es el actual) y establecerá el foco en la [*vista de árbol html*](../elements.md#html-tree-view) en el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="4799a-163">The DevTools will switch to the **Elements** panel (if its not already the current) and set focus in the [*HTML tree view*](../elements.md#html-tree-view) to the specified element.</span></span>

![Ejemplo del método ' Select '](../media/console_api_select.png)

## <span data-ttu-id="4799a-165">Pruebas y medición</span><span class="sxs-lookup"><span data-stu-id="4799a-165">Testing and measuring</span></span>

### <span data-ttu-id="4799a-166">Probar el código</span><span class="sxs-lookup"><span data-stu-id="4799a-166">Testing your code</span></span>

<span data-ttu-id="4799a-167">Agrega aserciones de prueba de la API de consola al código para las pruebas unitarias y la depuración del código a medida que se ejecuta en el explorador.</span><span class="sxs-lookup"><span data-stu-id="4799a-167">Add Console API test assertions to your code for unit testing and debugging your code as it runs in the browser.</span></span>

<span data-ttu-id="4799a-168">Comando</span><span class="sxs-lookup"><span data-stu-id="4799a-168">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="4799a-169">Assert ()</span><span class="sxs-lookup"><span data-stu-id="4799a-169">assert()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/assert) | <span data-ttu-id="4799a-170">Registra un mensaje de error de consola si la expresión proporcionada se evalúa como *falso*.</span><span class="sxs-lookup"><span data-stu-id="4799a-170">Logs a console error message if the provided expression evaluates to *false*.</span></span>

<span data-ttu-id="4799a-171">Además de la expresión lógica que suministre como aserción, puede Agregar un mensaje opcional y parámetros de formato como usaría con otros [mensajes de consola personalizados](#logging-custom-messages).</span><span class="sxs-lookup"><span data-stu-id="4799a-171">In addition to the logical expression you supply as the testable assertion, you can add an optional message and formatting parameters as you would use with other [custom console messages](#logging-custom-messages).</span></span> <span data-ttu-id="4799a-172">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4799a-172">For example:</span></span>

```javascript
var x = 26.8;
console.assert(x < 25, 'The value of x is %f (it is NOT less than %i)', x, 25);
```

![Ejemplo del método ' Assert '](../media/console_api_assert.png)

### <span data-ttu-id="4799a-174">Contar las ejecuciones en el código</span><span class="sxs-lookup"><span data-stu-id="4799a-174">Counting executions in your code</span></span>

<span data-ttu-id="4799a-175">Puedes establecer contadores en el código para seguir el número de veces que se ejecuta el código circundante.</span><span class="sxs-lookup"><span data-stu-id="4799a-175">You can set counters in your code to keep track of how many times the surrounding code gets executed.</span></span> <span data-ttu-id="4799a-176">El establecimiento de contadores puede ayudar a garantizar que el código se ejecuta según lo esperado y ayudarle a diagnosticar los cuellos de botella de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4799a-176">Setting counters can help ensure your code is running as expected and assist you in diagnosing performance bottlenecks.</span></span>

<span data-ttu-id="4799a-177">Comando</span><span class="sxs-lookup"><span data-stu-id="4799a-177">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="4799a-178">contar ()</span><span class="sxs-lookup"><span data-stu-id="4799a-178">count()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/count) | <span data-ttu-id="4799a-179">Incrementos y registros se ha ejecutado el número de veces que se ha realizado la *cuenta ()* para la etiqueta dada.</span><span class="sxs-lookup"><span data-stu-id="4799a-179">Increments and logs the number of times *count()* for the given label has been executed.</span></span>
[**<span data-ttu-id="4799a-180">countReset()</span><span class="sxs-lookup"><span data-stu-id="4799a-180">countReset()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/countReset) | <span data-ttu-id="4799a-181">Restablece el recuento a cero para la etiqueta de contador dada.</span><span class="sxs-lookup"><span data-stu-id="4799a-181">Resets the count to zero for the given counter label.</span></span>

<span data-ttu-id="4799a-182">Por ejemplo, ejecutando las siguientes líneas en la consola:</span><span class="sxs-lookup"><span data-stu-id="4799a-182">For example, executing the following lines in console:</span></span>

```javascript
console.count('My Counter');
console.count('My Counter');
console.countReset('My Counter');
console.count('My Counter');
```

 <span data-ttu-id="4799a-183">.</span><span class="sxs-lookup"><span data-stu-id="4799a-183">.</span></span> <span data-ttu-id="4799a-184">.</span><span class="sxs-lookup"><span data-stu-id="4799a-184">.</span></span> <span data-ttu-id="4799a-185">.</span><span class="sxs-lookup"><span data-stu-id="4799a-185">.</span></span> <span data-ttu-id="4799a-186">dará como resultado:</span><span class="sxs-lookup"><span data-stu-id="4799a-186">will result in:</span></span>
> <span data-ttu-id="4799a-187">Mi contador: 1</span><span class="sxs-lookup"><span data-stu-id="4799a-187">My Counter: 1</span></span>

### <span data-ttu-id="4799a-188">Cómo cronometrar tu código</span><span class="sxs-lookup"><span data-stu-id="4799a-188">Timing your code</span></span>

<span data-ttu-id="4799a-189">Instrumente tu código con los temporizadores etiquetados para medir cuánto tiempo se tarda en completar una determinada operación.</span><span class="sxs-lookup"><span data-stu-id="4799a-189">Instrument your code with labeled timers to measure how long it takes to complete a given operation.</span></span>

<span data-ttu-id="4799a-190">Comando</span><span class="sxs-lookup"><span data-stu-id="4799a-190">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="4799a-191">hora ()</span><span class="sxs-lookup"><span data-stu-id="4799a-191">time()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/time) | <span data-ttu-id="4799a-192">Inicia un temporizador con la etiqueta dada.</span><span class="sxs-lookup"><span data-stu-id="4799a-192">Starts a timer with the given label.</span></span>
[**<span data-ttu-id="4799a-193">timeEnd()</span><span class="sxs-lookup"><span data-stu-id="4799a-193">timeEnd()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/timeEnd) | <span data-ttu-id="4799a-194">Finaliza el temporizador con la etiqueta dada e informa del tiempo transcurrido (en milisegundos).</span><span class="sxs-lookup"><span data-stu-id="4799a-194">Ends the timer with the given label and reports the time elapsed (in milliseconds).</span></span>
[**<span data-ttu-id="4799a-195">timeStamp ()</span><span class="sxs-lookup"><span data-stu-id="4799a-195">timeStamp()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/timeStamp) | <span data-ttu-id="4799a-196">Informa de la hora actual del sistema (en milisegundos).</span><span class="sxs-lookup"><span data-stu-id="4799a-196">Reports the current system time (in milliseconds).</span></span>

<span data-ttu-id="4799a-197">Por ejemplo, intente ejecutar las siguientes líneas en la consola:</span><span class="sxs-lookup"><span data-stu-id="4799a-197">For example, try executing the following lines in console:</span></span>

```javascript
console.time('My Timer');
console.timeEnd('My Timer');
```

### <span data-ttu-id="4799a-198">Tomar instantáneas de montones</span><span class="sxs-lookup"><span data-stu-id="4799a-198">Taking heap snapshots</span></span>

<span data-ttu-id="4799a-199">Tomar instantáneas del montón para evaluar el consumo de memoria del código que se está ejecutando y para identificar las pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="4799a-199">Take snapshots of the heap to assess the memory consumption of your running code and identify memory leaks.</span></span>

<span data-ttu-id="4799a-200">Comando</span><span class="sxs-lookup"><span data-stu-id="4799a-200">Command</span></span> | &nbsp;
:------------ | :-------------
**<span data-ttu-id="4799a-201">takeHeapSnapshot()</span><span class="sxs-lookup"><span data-stu-id="4799a-201">takeHeapSnapshot()</span></span>** | <span data-ttu-id="4799a-202">Captura detalles sobre el montón de JavaScript actual y los objetos asignados.</span><span class="sxs-lookup"><span data-stu-id="4799a-202">Captures details about the current JavaScript heap and its allocated objects.</span></span>

<span data-ttu-id="4799a-203">El [generador de perfiles de memoria](../memory.md#toolbar) de DevTools debe estar ejecutándose para poder tomar instantáneas de montones.</span><span class="sxs-lookup"><span data-stu-id="4799a-203">The  DevTools [memory profiler](../memory.md#toolbar) must be running in order to take heap snapshots.</span></span> <span data-ttu-id="4799a-204">Cada instantánea aparecerá como un mosaico en el [*Resumen de instantáneas*](../memory.md#snapshot-summary) del panel [**memoria**](../memory.md) para una posterior inspección.</span><span class="sxs-lookup"><span data-stu-id="4799a-204">Each snapshot will appear as a tile in the [*Snapshot summary*](../memory.md#snapshot-summary) of the [**Memory**](../memory.md) panel for further inspection.</span></span>

## <span data-ttu-id="4799a-205">Seguimiento callstacks</span><span class="sxs-lookup"><span data-stu-id="4799a-205">Tracing callstacks</span></span>

<span data-ttu-id="4799a-206">Comprender desde dónde se llama el código, qué código se ejecuta y cuánto tiempo tarda la ejecución puede ser útil para analizar la lentitud o el comportamiento inesperado.</span><span class="sxs-lookup"><span data-stu-id="4799a-206">Understanding where your code is being called from, what code is running, and how long that execution takes can be useful in analyzing slowness or unexpected behavior.</span></span> <span data-ttu-id="4799a-207">Un seguimiento de pila muestra la ruta de ejecución que el código ha tomado para comunicarse con él, desde la solicitud de seguimiento hacia arriba a través de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="4799a-207">A stack trace shows you the execution path your code took to reach it, from the trace request upward through the path.</span></span> 

<span data-ttu-id="4799a-208">Comando</span><span class="sxs-lookup"><span data-stu-id="4799a-208">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="4799a-209">Trace ()</span><span class="sxs-lookup"><span data-stu-id="4799a-209">trace()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/trace) | <span data-ttu-id="4799a-210">Genera un seguimiento de la pila de llamadas de ejecución de script actuales.</span><span class="sxs-lookup"><span data-stu-id="4799a-210">Outputs a trace of the current script execution callstack.</span></span>

<span data-ttu-id="4799a-211">Por ejemplo, ejecutando el siguiente código en la consola:</span><span class="sxs-lookup"><span data-stu-id="4799a-211">For example, running the following code in the console:</span></span>

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

<span data-ttu-id="4799a-212">.</span><span class="sxs-lookup"><span data-stu-id="4799a-212">.</span></span> <span data-ttu-id="4799a-213">.</span><span class="sxs-lookup"><span data-stu-id="4799a-213">.</span></span> <span data-ttu-id="4799a-214">.</span><span class="sxs-lookup"><span data-stu-id="4799a-214">.</span></span> <span data-ttu-id="4799a-215">dará como resultado los siguientes seguimientos de la pila:</span><span class="sxs-lookup"><span data-stu-id="4799a-215">will output the following stack traces:</span></span>
> <span data-ttu-id="4799a-216">Console. Trace () en c (código de evaluación: 8:3) a (código de evaluación: 2:3) en código de evaluación (código de evaluación: 14:1)</span><span class="sxs-lookup"><span data-stu-id="4799a-216">console.trace() at c (eval code:8:3) at a (eval code:2:3) at eval code (eval code:14:1)</span></span>
> 
> <span data-ttu-id="4799a-217">Console. Trace () en c (código de evaluación: 8:3) en b (código de evaluación: 5:3) en d (código de evaluación: 11:3) en código de evaluación (código de evaluación: 15:1)</span><span class="sxs-lookup"><span data-stu-id="4799a-217">console.trace() at c (eval code:8:3) at b (eval code:5:3) at d (eval code:11:3) at eval code (eval code:15:1)</span></span>

## <span data-ttu-id="4799a-218">Organizar la salida del registro</span><span class="sxs-lookup"><span data-stu-id="4799a-218">Organizing log output</span></span>

<span data-ttu-id="4799a-219">Para borrar simplemente todo el resultado de la consola anterior, usa *Console. Clear ()* (o `CTRL + L` ).</span><span class="sxs-lookup"><span data-stu-id="4799a-219">To simply clear all previous console output, use *console.clear()* (or `CTRL + L`).</span></span> <span data-ttu-id="4799a-220">Esto no elimina la configuración de la pila de comandos de la consola (aún puede recorrerla con las teclas de flecha arriba y abajo).</span><span class="sxs-lookup"><span data-stu-id="4799a-220">This does not clear the backstack of your console command history (you can still traverse it with the up and down arrow keys).</span></span>

<span data-ttu-id="4799a-221">Comando</span><span class="sxs-lookup"><span data-stu-id="4799a-221">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="4799a-222">borrar ()</span><span class="sxs-lookup"><span data-stu-id="4799a-222">clear()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/clear) | <span data-ttu-id="4799a-223">Borra todo el resultado de la consola anterior.</span><span class="sxs-lookup"><span data-stu-id="4799a-223">Clears all previous console output.</span></span>

<span data-ttu-id="4799a-224">Si el código genera una gran cantidad de mensajes de consola, puedes organizarlos visualmente en bloques anidados con los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="4799a-224">If your code outputs a lot of console messages, you can visually organize them into nested blocks with the following commands:</span></span>

 <span data-ttu-id="4799a-225">Comando</span><span class="sxs-lookup"><span data-stu-id="4799a-225">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="4799a-226">Group ()</span><span class="sxs-lookup"><span data-stu-id="4799a-226">group()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/group) | <span data-ttu-id="4799a-227">Inicia un nuevo nivel de anidamiento de la salida de la consola con la etiqueta especificada (optional).</span><span class="sxs-lookup"><span data-stu-id="4799a-227">Starts a new level of nesting for console output with the specified (optional) label.</span></span>
[**<span data-ttu-id="4799a-228">groupCollapsed()</span><span class="sxs-lookup"><span data-stu-id="4799a-228">groupCollapsed()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/groupCollapsed) | <span data-ttu-id="4799a-229">Inicia un nuevo nivel de anidamiento de la salida de la consola con la etiqueta especificada (opcional), sin embargo, el control de agrupación se contrae de forma predeterminada y debe expandirse (haciendo clic en el control de flecha) para mostrar el resultado secundario.</span><span class="sxs-lookup"><span data-stu-id="4799a-229">Starts a new level of nesting for console output with the specified (optional) label, however the grouping control is collapsed by default and must be expanded (by clicking on the arrow control) to display the child output.</span></span>
[**<span data-ttu-id="4799a-230">groupEnd()</span><span class="sxs-lookup"><span data-stu-id="4799a-230">groupEnd()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/groupEnd) | <span data-ttu-id="4799a-231">Termina el grupo de anidamiento de la etiqueta especificada.</span><span class="sxs-lookup"><span data-stu-id="4799a-231">Ends the nesting group for the specified label.</span></span>

<span data-ttu-id="4799a-232">Por ejemplo, pruebe a escribir los siguientes comandos en la consola:</span><span class="sxs-lookup"><span data-stu-id="4799a-232">For example, try entering the following commands in the console:</span></span>

```javascript
console.groupCollapsed('Group 1');
console.log('In Group 1');
console.groupCollapsed('Group 1.1');
console.log('In Group 1.1');
console.groupEnd('Group 1.1');
console.groupEnd('Group 1');
console.log('No longer in a group');
```

<span data-ttu-id="4799a-233">.</span><span class="sxs-lookup"><span data-stu-id="4799a-233">.</span></span> <span data-ttu-id="4799a-234">.</span><span class="sxs-lookup"><span data-stu-id="4799a-234">.</span></span> <span data-ttu-id="4799a-235">.</span><span class="sxs-lookup"><span data-stu-id="4799a-235">.</span></span> <span data-ttu-id="4799a-236">a continuación, expanda los controles *Grupo 1* y *Grupo 1,1* para ver cómo se anidan los comentarios del registro:</span><span class="sxs-lookup"><span data-stu-id="4799a-236">and then expand the *Group 1* and *Group 1.1* controls to see how the log comments are nested:</span></span>

![Agrupar mensajes en la consola](../media/console_api_group.png)

<span data-ttu-id="4799a-238">A veces es más fácil visualizar un objeto o matriz de JavaScript en formato tabular, en lugar de una lista plana.</span><span class="sxs-lookup"><span data-stu-id="4799a-238">Sometimes its easier to visualize a JavaScript object or array in tabular form, rather than a flat list.</span></span> <span data-ttu-id="4799a-239">Para ello, puedes usar el comando *Console. Table ()* :</span><span class="sxs-lookup"><span data-stu-id="4799a-239">For that, you can use the *console.table()* command:</span></span>

<span data-ttu-id="4799a-240">Comando</span><span class="sxs-lookup"><span data-stu-id="4799a-240">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="4799a-241">Table ()</span><span class="sxs-lookup"><span data-stu-id="4799a-241">table()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/table) | <span data-ttu-id="4799a-242">Envía la matriz u objeto suministrados a la consola en formato de tabla.</span><span class="sxs-lookup"><span data-stu-id="4799a-242">Outputs the supplied array or object to the console in tabular form.</span></span>

<span data-ttu-id="4799a-243">Por ejemplo, la siguiente matriz de objetos:</span><span class="sxs-lookup"><span data-stu-id="4799a-243">For example, the following object array:</span></span>

```javascript
var orders = [{'Size':'XL', 'Quantity':1},{'Size':'M', 'Quantity':3}, {'Size':'L', 'Quantity':2}];
console.table(orders);
```

<span data-ttu-id="4799a-244">.</span><span class="sxs-lookup"><span data-stu-id="4799a-244">.</span></span> <span data-ttu-id="4799a-245">.</span><span class="sxs-lookup"><span data-stu-id="4799a-245">.</span></span> <span data-ttu-id="4799a-246">.</span><span class="sxs-lookup"><span data-stu-id="4799a-246">.</span></span> <span data-ttu-id="4799a-247">se representará como esta tabla en la consola:</span><span class="sxs-lookup"><span data-stu-id="4799a-247">will render as this table in the console:</span></span>

![Mostrar una matriz de objetos como una tabla en la consola](../media/console_api_table.png)

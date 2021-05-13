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
# <a name="console-api-reference"></a><span data-ttu-id="aa302-104">Referencia de la API de consola</span><span class="sxs-lookup"><span data-stu-id="aa302-104">Console API reference</span></span>  

<span data-ttu-id="aa302-105">La **herramienta Consola** es útil cuando se completan varias tareas en DevTools.</span><span class="sxs-lookup"><span data-stu-id="aa302-105">The **Console** tool is helpful when you complete multiple tasks in the DevTools.</span></span>  <span data-ttu-id="aa302-106">Las API están disponibles para incluir en los scripts.</span><span class="sxs-lookup"><span data-stu-id="aa302-106">APIs are available to include in your scripts.</span></span> <span data-ttu-id="aa302-107">Los métodos de comodidad solo están disponibles para su uso en la **herramienta Consola,** como los `debug()` métodos `monitorEvents()` and.</span><span class="sxs-lookup"><span data-stu-id="aa302-107">Convenience methods are only available for use in the **Console** tool, such as the `debug()` and `monitorEvents()` methods.</span></span>  <span data-ttu-id="aa302-108">Para obtener más información sobre cómo empezar con la **consola,** vaya a Introducción al registro [de mensajes en la consola][DevtoolsConsoleConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="aa302-108">For more information on getting started with the **Console**, navigate to [Get started with logging messages to the Console][DevtoolsConsoleConsoleLog].</span></span>  <span data-ttu-id="aa302-109">Para obtener más información sobre los métodos de comodidad en **la consola,** vaya a [Console Utilities API Reference][DevtoolConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="aa302-109">For more information on the convenience methods in the **Console**, navigate to [Console Utilities API Reference][DevtoolConsoleUtilities].</span></span>  

---  

## <a name="assert"></a><span data-ttu-id="aa302-110">assert</span><span class="sxs-lookup"><span data-stu-id="aa302-110">assert</span></span>  

<span data-ttu-id="aa302-111">Este método escribe un [error](#error) en la **consola** cuando `expression` se evalúa como `false` .</span><span class="sxs-lookup"><span data-stu-id="aa302-111">This method writes an [error](#error) to the **Console** when `expression` evaluates to `false`.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-112">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-112">JavaScript syntax</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="aa302-113">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa302-113">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

### <a name="javascript-example"></a><span data-ttu-id="aa302-114">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-114">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-115">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa302-115">Input</span></span>  
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
      <span data-ttu-id="aa302-116">Salida</span><span class="sxs-lookup"><span data-stu-id="aa302-116">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="El resultado del ejemplo console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
         <span data-ttu-id="aa302-118">El resultado del `console.assert()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa302-118">The result of the `console.assert()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="clear"></a><span data-ttu-id="aa302-119">clear</span><span class="sxs-lookup"><span data-stu-id="aa302-119">clear</span></span>  

<span data-ttu-id="aa302-120">Este método borra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="aa302-120">This method clears the **Console**.</span></span>  

<span data-ttu-id="aa302-121">Si [Preserve Log][DevtoolsConsoleReferenceFilter] está activado, el método [clear](#clear) se desactivará.</span><span class="sxs-lookup"><span data-stu-id="aa302-121">If [Preserve Log][DevtoolsConsoleReferenceFilter] is turned on, the [clear](#clear) method is turned off.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-122">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-122">JavaScript syntax</span></span>  

```javascript
console.clear()
```

### <a name="javascript-example"></a><span data-ttu-id="aa302-123">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-123">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-124">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa302-124">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.clear();  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-125">Salida</span><span class="sxs-lookup"><span data-stu-id="aa302-125">Output</span></span>
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

### <a name="see-also"></a><span data-ttu-id="aa302-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="aa302-126">See also</span></span>  

*   [<span data-ttu-id="aa302-127">Borrar la consola</span><span class="sxs-lookup"><span data-stu-id="aa302-127">Clear the Console</span></span>][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a><span data-ttu-id="aa302-128">count</span><span class="sxs-lookup"><span data-stu-id="aa302-128">count</span></span>  

<span data-ttu-id="aa302-129">Este método escribe el número de veces que el [método count](#count) se ha invocado en la misma línea y con la misma `label` .</span><span class="sxs-lookup"><span data-stu-id="aa302-129">This method writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="aa302-130">Use el [método countReset](#countreset) para restablecer el recuento.</span><span class="sxs-lookup"><span data-stu-id="aa302-130">Use the [countReset](#countreset) method to reset the count.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-131">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-131">JavaScript syntax</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="aa302-132">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa302-132">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="aa302-133">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-133">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa302-134">Input</span></span>  
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
      <span data-ttu-id="aa302-135">Salida</span><span class="sxs-lookup"><span data-stu-id="aa302-135">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="El resultado del ejemplo console.count()" lightbox="../media/console-demo-count-button.msft.png":::
         <span data-ttu-id="aa302-137">El resultado del `console.count()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa302-137">The result of the `console.count()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="countreset"></a><span data-ttu-id="aa302-138">countReset</span><span class="sxs-lookup"><span data-stu-id="aa302-138">countReset</span></span>  

<span data-ttu-id="aa302-139">Este método restablece un recuento.</span><span class="sxs-lookup"><span data-stu-id="aa302-139">This method resets a count.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-140">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-140">JavaScript syntax</span></span>  

```javascript
console.countReset([label])
```  

### <a name="javascript-example"></a><span data-ttu-id="aa302-141">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-141">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-142">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa302-142">Input</span></span>  
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
      <span data-ttu-id="aa302-143">Salida</span><span class="sxs-lookup"><span data-stu-id="aa302-143">Output</span></span>
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

---  

## <a name="debug"></a><span data-ttu-id="aa302-144">depurar</span><span class="sxs-lookup"><span data-stu-id="aa302-144">debug</span></span>  

<span data-ttu-id="aa302-145">Este método es idéntico al método [log,](#log) excepto el nivel de registro diferente.</span><span class="sxs-lookup"><span data-stu-id="aa302-145">This method is identical to the [log](#log) method, except different log level.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-146">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-146">JavaScript syntax</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="aa302-147">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa302-147">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Verbose`  

### <a name="javascript-example"></a><span data-ttu-id="aa302-148">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-148">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa302-149">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.debug('debug');  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-150">Salida</span><span class="sxs-lookup"><span data-stu-id="aa302-150">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="El resultado del ejemplo console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
         <span data-ttu-id="aa302-152">El resultado del `console.debug()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa302-152">The result of the `console.debug()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dir"></a><span data-ttu-id="aa302-153">dir</span><span class="sxs-lookup"><span data-stu-id="aa302-153">dir</span></span>  

<span data-ttu-id="aa302-154">Este método imprime una representación JSON del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="aa302-154">This method prints a JSON representation of the specified object.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-155">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-155">JavaScript syntax</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="aa302-156">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa302-156">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="aa302-157">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-157">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa302-158">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dir(document.head);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-159">Salida</span><span class="sxs-lookup"><span data-stu-id="aa302-159">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="El resultado del ejemplo console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
         <span data-ttu-id="aa302-161">El resultado del `console.dir()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa302-161">The result of the `console.dir()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dirxml"></a><span data-ttu-id="aa302-162">dirxml</span><span class="sxs-lookup"><span data-stu-id="aa302-162">dirxml</span></span>  

<span data-ttu-id="aa302-163">Este método imprime una representación XML de los descendientes de `node` .</span><span class="sxs-lookup"><span data-stu-id="aa302-163">This method prints an XML representation of the descendants of `node`.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-164">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-164">JavaScript syntax</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="aa302-165">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa302-165">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="aa302-166">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-166">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-167">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa302-167">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dirxml(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-168">Salida</span><span class="sxs-lookup"><span data-stu-id="aa302-168">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="El resultado del ejemplo console.dirxml()" lightbox="../media/console-demo-dirxml-button.msft.png":::
         <span data-ttu-id="aa302-170">El resultado del `console.dirxml()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa302-170">The result of the `console.dirxml()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="error"></a><span data-ttu-id="aa302-171">error</span><span class="sxs-lookup"><span data-stu-id="aa302-171">error</span></span>  

<span data-ttu-id="aa302-172">Este método imprime la consola, la da `object` formato como un error e incluye un seguimiento de la pila. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="aa302-172">This method prints the `object` to the **Console**, formats it as an error, and includes a stack trace.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-173">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-173">JavaScript syntax</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="aa302-174">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa302-174">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

### <a name="javascript-example"></a><span data-ttu-id="aa302-175">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-175">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa302-176">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-177">Salida</span><span class="sxs-lookup"><span data-stu-id="aa302-177">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="El resultado del ejemplo console.error()" lightbox="../media/console-demo-error-button.msft.png":::
         <span data-ttu-id="aa302-179">El resultado del `console.error()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa302-179">The result of the `console.error()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="group"></a><span data-ttu-id="aa302-180">grupo</span><span class="sxs-lookup"><span data-stu-id="aa302-180">group</span></span>  

<span data-ttu-id="aa302-181">Este método agrupa visualmente mensajes hasta que se usa el [método groupEnd.](#groupend)</span><span class="sxs-lookup"><span data-stu-id="aa302-181">This method visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="aa302-182">Use el [método groupCollapsed](#groupcollapsed) para contraer el grupo cuando inicia sesión inicialmente en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="aa302-182">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it initially logs to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-183">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-183">JavaScript syntax</span></span>  

```javascript
console.group(label)
```  

### <a name="javascript-example"></a><span data-ttu-id="aa302-184">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-184">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa302-185">Input</span></span>  
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
      <span data-ttu-id="aa302-186">Salida</span><span class="sxs-lookup"><span data-stu-id="aa302-186">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="El resultado del ejemplo console.group()" lightbox="../media/console-demo-group-button.msft.png":::
         <span data-ttu-id="aa302-188">El resultado del `console.group()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa302-188">The result of the `console.group()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="groupcollapsed"></a><span data-ttu-id="aa302-189">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="aa302-189">groupCollapsed</span></span>  

<span data-ttu-id="aa302-190">Este método es idéntico al método [log,](#log) excepto que el grupo se contrae inicialmente cuando inicia sesión en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="aa302-190">This method is identical to the [log](#log) method, except the group is initially collapsed when it logs to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-191">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-191">JavaScript syntax</span></span>  

```javascript
console.groupCollapsed(label)
```  

---  

## <a name="groupend"></a><span data-ttu-id="aa302-192">groupEnd</span><span class="sxs-lookup"><span data-stu-id="aa302-192">groupEnd</span></span>  

<span data-ttu-id="aa302-193">Este método detiene la agrupación visual de mensajes.</span><span class="sxs-lookup"><span data-stu-id="aa302-193">This method stops visually grouping messages.</span></span>  <span data-ttu-id="aa302-194">Vaya al [método group.](#group)</span><span class="sxs-lookup"><span data-stu-id="aa302-194">Navigate to the [group](#group) method.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-195">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-195">JavaScript syntax</span></span>  

```javascript
console.groupEnd(label)
```  

---  

## <a name="info"></a><span data-ttu-id="aa302-196">información</span><span class="sxs-lookup"><span data-stu-id="aa302-196">info</span></span>  

<span data-ttu-id="aa302-197">Este método es idéntico al método [log.](#log)</span><span class="sxs-lookup"><span data-stu-id="aa302-197">This method is identical to the [log](#log) method.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-198">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-198">JavaScript syntax</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="aa302-199">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa302-199">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="aa302-200">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-200">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa302-201">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.info('info');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-202">Salida</span><span class="sxs-lookup"><span data-stu-id="aa302-202">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="El resultado del ejemplo console.info()" lightbox="../media/console-demo-info-button.msft.png":::
         <span data-ttu-id="aa302-204">El resultado del `console.info()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa302-204">The result of the `console.info()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="log"></a><span data-ttu-id="aa302-205">log</span><span class="sxs-lookup"><span data-stu-id="aa302-205">log</span></span>  

<span data-ttu-id="aa302-206">Este método imprime un mensaje en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="aa302-206">This method prints a message to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-207">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-207">JavaScript syntax</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="aa302-208">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa302-208">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="aa302-209">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-209">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa302-210">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.log('log');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-211">Salida</span><span class="sxs-lookup"><span data-stu-id="aa302-211">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="El resultado del ejemplo console.log()" lightbox="../media/console-demo-log-button.msft.png":::
         <span data-ttu-id="aa302-213">El resultado del `console.log()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa302-213">The result of the `console.log()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a><span data-ttu-id="aa302-214">tabla</span><span class="sxs-lookup"><span data-stu-id="aa302-214">table</span></span>  

<span data-ttu-id="aa302-215">Este método registra una matriz de objetos como una tabla.</span><span class="sxs-lookup"><span data-stu-id="aa302-215">This method logs an array of objects as a table.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-216">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-216">JavaScript syntax</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="aa302-217">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa302-217">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="aa302-218">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-218">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-219">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa302-219">Input</span></span>  
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
      <span data-ttu-id="aa302-220">Salida</span><span class="sxs-lookup"><span data-stu-id="aa302-220">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="El resultado del ejemplo console.table()" lightbox="../media/console-demo-table-button.msft.png":::
         <span data-ttu-id="aa302-222">El resultado del `console.table()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa302-222">The result of the `console.table()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="time"></a><span data-ttu-id="aa302-223">time</span><span class="sxs-lookup"><span data-stu-id="aa302-223">time</span></span>  

<span data-ttu-id="aa302-224">Este método inicia un nuevo temporizador.</span><span class="sxs-lookup"><span data-stu-id="aa302-224">This method starts a new timer.</span></span>  <span data-ttu-id="aa302-225">Utilice el [método timeEnd](#timeend) para detener el temporizador e imprimir el tiempo transcurrido en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="aa302-225">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-226">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-226">JavaScript syntax</span></span>  

```javascript
console.time([label])
```  

### <a name="javascript-example"></a><span data-ttu-id="aa302-227">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-227">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa302-228">Input</span></span>  
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
      <span data-ttu-id="aa302-229">Salida</span><span class="sxs-lookup"><span data-stu-id="aa302-229">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="El resultado del ejemplo console.time()" lightbox="../media/console-demo-time-button.msft.png":::
         <span data-ttu-id="aa302-231">El resultado del `console.time()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa302-231">The result of the `console.time()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="timeend"></a><span data-ttu-id="aa302-232">timeEnd</span><span class="sxs-lookup"><span data-stu-id="aa302-232">timeEnd</span></span>  

<span data-ttu-id="aa302-233">Este método detiene un temporizador.</span><span class="sxs-lookup"><span data-stu-id="aa302-233">This method stops a timer.</span></span>  <span data-ttu-id="aa302-234">Para obtener más información, vaya al [método time.](#time)</span><span class="sxs-lookup"><span data-stu-id="aa302-234">For more information, navigate to the [time](#time) method.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-235">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-235">JavaScript syntax</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="aa302-236">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa302-236">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

---  

## <a name="trace"></a><span data-ttu-id="aa302-237">seguimiento</span><span class="sxs-lookup"><span data-stu-id="aa302-237">trace</span></span>  

<span data-ttu-id="aa302-238">Este método imprime un seguimiento de pila en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="aa302-238">This method prints a stack trace to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-239">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-239">JavaScript syntax</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="aa302-240">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa302-240">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="aa302-241">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-241">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-242">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa302-242">Input</span></span>  
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
      <span data-ttu-id="aa302-243">Salida</span><span class="sxs-lookup"><span data-stu-id="aa302-243">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="El resultado del ejemplo console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
         <span data-ttu-id="aa302-245">El resultado del `console.trace()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa302-245">The result of the `console.trace()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="warn"></a><span data-ttu-id="aa302-246">warn</span><span class="sxs-lookup"><span data-stu-id="aa302-246">warn</span></span>  

<span data-ttu-id="aa302-247">Este método imprime una advertencia en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="aa302-247">This method prints a warning to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="aa302-248">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-248">JavaScript syntax</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="aa302-249">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="aa302-249">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

### <a name="javascript-example"></a><span data-ttu-id="aa302-250">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="aa302-250">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="aa302-251">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.warn('warn');
      ```
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="aa302-252">Salida</span><span class="sxs-lookup"><span data-stu-id="aa302-252">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="El resultado del ejemplo console.warn()" lightbox="../media/console-demo-warn-button.msft.png":::
         <span data-ttu-id="aa302-254">El resultado del `console.warn()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa302-254">The result of the `console.warn()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="aa302-255">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="aa302-255">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleLog]: ./console-log.md "Inicia sesión en la herramienta consola | Microsoft Docs"  
[DevtoolConsoleUtilities]: ./utilities.md "Referencia de api de utilidades de consola | Microsoft Docs"  
[DevtoolsConsoleReferenceClear]: ./reference.md#clear-the-console "Borrar la consola: referencia de consola | Microsoft Docs"  
[DevtoolsConsoleReferenceFilter]: ./reference.md#filter-by-log-level "Filtrar por nivel de registro: referencia de consola | Microsoft Docs"  
[DevtoolsConsoleReferencePersist]: ./reference.md#persist-messages-across-page-loads "Conservar mensajes entre cargas de página: referencia de consola | Microsoft Docs"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Introducción a las herramientas de desarrollador de Microsoft Edge (Chromium) | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="aa302-262">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aa302-262">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="aa302-263">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/api) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="aa302-263">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="aa302-265">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aa302-265">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

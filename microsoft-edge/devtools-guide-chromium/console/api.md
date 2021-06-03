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
# <a name="console-api-reference"></a><span data-ttu-id="304c5-104">Referencia de la API de consola</span><span class="sxs-lookup"><span data-stu-id="304c5-104">Console API reference</span></span>  

<span data-ttu-id="304c5-105">La **herramienta Consola** es útil cuando se completan varias tareas en DevTools.</span><span class="sxs-lookup"><span data-stu-id="304c5-105">The **Console** tool is helpful when you complete multiple tasks in the DevTools.</span></span>  <span data-ttu-id="304c5-106">Las API están disponibles para incluir en los scripts.</span><span class="sxs-lookup"><span data-stu-id="304c5-106">APIs are available to include in your scripts.</span></span> <span data-ttu-id="304c5-107">Los métodos de comodidad solo están disponibles para su uso en la **herramienta Consola,** como los `debug()` métodos `monitorEvents()` and.</span><span class="sxs-lookup"><span data-stu-id="304c5-107">Convenience methods are only available for use in the **Console** tool, such as the `debug()` and `monitorEvents()` methods.</span></span>  <span data-ttu-id="304c5-108">Para obtener más información sobre cómo empezar con la **consola,** vaya a Introducción al registro [de mensajes en la consola][DevtoolsConsoleConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="304c5-108">For more information on getting started with the **Console**, navigate to [Get started with logging messages to the Console][DevtoolsConsoleConsoleLog].</span></span>  <span data-ttu-id="304c5-109">Para obtener más información sobre los métodos de comodidad en **la consola,** vaya a [Console Utilities API Reference][DevtoolConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="304c5-109">For more information on the convenience methods in the **Console**, navigate to [Console Utilities API Reference][DevtoolConsoleUtilities].</span></span>  

---  

## <a name="assert"></a><span data-ttu-id="304c5-110">assert</span><span class="sxs-lookup"><span data-stu-id="304c5-110">assert</span></span>  

<span data-ttu-id="304c5-111">Este método escribe un [error](#error) en la **consola** cuando `expression` se evalúa como `false` .</span><span class="sxs-lookup"><span data-stu-id="304c5-111">This method writes an [error](#error) to the **Console** when `expression` evaluates to `false`.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-112">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-112">JavaScript syntax</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="304c5-113">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="304c5-113">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

### <a name="javascript-example"></a><span data-ttu-id="304c5-114">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-114">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-115">Entrada</span><span class="sxs-lookup"><span data-stu-id="304c5-115">Input</span></span>  
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
      <span data-ttu-id="304c5-116">Salida</span><span class="sxs-lookup"><span data-stu-id="304c5-116">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="El resultado del ejemplo console.assert()" lightbox="../media/console-demo-assert-button.msft.png":::
         <span data-ttu-id="304c5-118">El resultado del `console.assert()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="304c5-118">The result of the `console.assert()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="clear"></a><span data-ttu-id="304c5-119">clear</span><span class="sxs-lookup"><span data-stu-id="304c5-119">clear</span></span>  

<span data-ttu-id="304c5-120">Este método borra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="304c5-120">This method clears the **Console**.</span></span>  

<span data-ttu-id="304c5-121">Si [Preserve Log][DevtoolsConsoleReferenceFilter] está activado, el método [clear](#clear) se desactivará.</span><span class="sxs-lookup"><span data-stu-id="304c5-121">If [Preserve Log][DevtoolsConsoleReferenceFilter] is turned on, the [clear](#clear) method is turned off.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-122">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-122">JavaScript syntax</span></span>  

```javascript
console.clear()
```

### <a name="javascript-example"></a><span data-ttu-id="304c5-123">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-123">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-124">Entrada</span><span class="sxs-lookup"><span data-stu-id="304c5-124">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.clear();  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-125">Salida</span><span class="sxs-lookup"><span data-stu-id="304c5-125">Output</span></span>
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

### <a name="see-also"></a><span data-ttu-id="304c5-126">Consulta también</span><span class="sxs-lookup"><span data-stu-id="304c5-126">See also</span></span>  

*   [<span data-ttu-id="304c5-127">Borrar la consola</span><span class="sxs-lookup"><span data-stu-id="304c5-127">Clear the Console</span></span>][DevtoolsConsoleReferenceClear]  

---  

## <a name="count"></a><span data-ttu-id="304c5-128">count</span><span class="sxs-lookup"><span data-stu-id="304c5-128">count</span></span>  

<span data-ttu-id="304c5-129">Este método escribe el número de veces que el [método count](#count) se ha invocado en la misma línea y con la misma `label` .</span><span class="sxs-lookup"><span data-stu-id="304c5-129">This method writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="304c5-130">Use el [método countReset](#countreset) para restablecer el recuento.</span><span class="sxs-lookup"><span data-stu-id="304c5-130">Use the [countReset](#countreset) method to reset the count.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-131">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-131">JavaScript syntax</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="304c5-132">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="304c5-132">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="304c5-133">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-133">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="304c5-134">Input</span></span>  
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
      <span data-ttu-id="304c5-135">Salida</span><span class="sxs-lookup"><span data-stu-id="304c5-135">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="El resultado del ejemplo console.count()" lightbox="../media/console-demo-count-button.msft.png":::
         <span data-ttu-id="304c5-137">El resultado del `console.count()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="304c5-137">The result of the `console.count()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="countreset"></a><span data-ttu-id="304c5-138">countReset</span><span class="sxs-lookup"><span data-stu-id="304c5-138">countReset</span></span>  

<span data-ttu-id="304c5-139">Este método restablece un recuento.</span><span class="sxs-lookup"><span data-stu-id="304c5-139">This method resets a count.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-140">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-140">JavaScript syntax</span></span>  

```javascript
console.countReset([label])
```  

### <a name="javascript-example"></a><span data-ttu-id="304c5-141">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-141">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-142">Entrada</span><span class="sxs-lookup"><span data-stu-id="304c5-142">Input</span></span>  
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
      <span data-ttu-id="304c5-143">Salida</span><span class="sxs-lookup"><span data-stu-id="304c5-143">Output</span></span>
   :::column-end:::
   :::column span="3":::
      
   :::column-end:::
:::row-end:::  

---  

## <a name="debug"></a><span data-ttu-id="304c5-144">depurar</span><span class="sxs-lookup"><span data-stu-id="304c5-144">debug</span></span>  

<span data-ttu-id="304c5-145">Este método es idéntico al método [log,](#log) excepto el nivel de registro diferente.</span><span class="sxs-lookup"><span data-stu-id="304c5-145">This method is identical to the [log](#log) method, except different log level.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-146">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-146">JavaScript syntax</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="304c5-147">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="304c5-147">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Verbose`  

### <a name="javascript-example"></a><span data-ttu-id="304c5-148">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-148">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="304c5-149">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.debug('debug');  
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-150">Salida</span><span class="sxs-lookup"><span data-stu-id="304c5-150">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="El resultado del ejemplo console.debug()" lightbox="../media/console-demo-debug-button.msft.png":::
         <span data-ttu-id="304c5-152">El resultado del `console.debug()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="304c5-152">The result of the `console.debug()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dir"></a><span data-ttu-id="304c5-153">dir</span><span class="sxs-lookup"><span data-stu-id="304c5-153">dir</span></span>  

<span data-ttu-id="304c5-154">Este método imprime una representación JSON del objeto especificado.</span><span class="sxs-lookup"><span data-stu-id="304c5-154">This method prints a JSON representation of the specified object.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-155">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-155">JavaScript syntax</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="304c5-156">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="304c5-156">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="304c5-157">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-157">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="304c5-158">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dir(document.head);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-159">Salida</span><span class="sxs-lookup"><span data-stu-id="304c5-159">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="El resultado del ejemplo console.dir()" lightbox="../media/console-demo-dir-button.msft.png":::
         <span data-ttu-id="304c5-161">El resultado del `console.dir()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="304c5-161">The result of the `console.dir()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="dirxml"></a><span data-ttu-id="304c5-162">dirxml</span><span class="sxs-lookup"><span data-stu-id="304c5-162">dirxml</span></span>  

<span data-ttu-id="304c5-163">Este método imprime una representación XML de los descendientes de `node` .</span><span class="sxs-lookup"><span data-stu-id="304c5-163">This method prints an XML representation of the descendants of `node`.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-164">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-164">JavaScript syntax</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="304c5-165">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="304c5-165">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="304c5-166">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-166">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-167">Entrada</span><span class="sxs-lookup"><span data-stu-id="304c5-167">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.dirxml(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-168">Salida</span><span class="sxs-lookup"><span data-stu-id="304c5-168">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="El resultado del ejemplo console.dirxml()" lightbox="../media/console-demo-dirxml-button.msft.png":::
         <span data-ttu-id="304c5-170">El resultado del `console.dirxml()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="304c5-170">The result of the `console.dirxml()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="error"></a><span data-ttu-id="304c5-171">error</span><span class="sxs-lookup"><span data-stu-id="304c5-171">error</span></span>  

<span data-ttu-id="304c5-172">Este método imprime la consola, la da `object` formato como un error e incluye un seguimiento de la pila. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="304c5-172">This method prints the `object` to the **Console**, formats it as an error, and includes a stack trace.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-173">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-173">JavaScript syntax</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="304c5-174">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="304c5-174">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

### <a name="javascript-example"></a><span data-ttu-id="304c5-175">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-175">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="304c5-176">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-177">Salida</span><span class="sxs-lookup"><span data-stu-id="304c5-177">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="El resultado del ejemplo console.error()" lightbox="../media/console-demo-error-button.msft.png":::
         <span data-ttu-id="304c5-179">El resultado del `console.error()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="304c5-179">The result of the `console.error()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="group"></a><span data-ttu-id="304c5-180">grupo</span><span class="sxs-lookup"><span data-stu-id="304c5-180">group</span></span>  

<span data-ttu-id="304c5-181">Este método agrupa visualmente mensajes hasta que se usa el [método groupEnd.](#groupend)</span><span class="sxs-lookup"><span data-stu-id="304c5-181">This method visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="304c5-182">Use el [método groupCollapsed](#groupcollapsed) para contraer el grupo cuando inicia sesión inicialmente en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="304c5-182">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it initially logs to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-183">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-183">JavaScript syntax</span></span>  

```javascript
console.group(label)
```  

### <a name="javascript-example"></a><span data-ttu-id="304c5-184">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-184">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="304c5-185">Input</span></span>  
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
      <span data-ttu-id="304c5-186">Salida</span><span class="sxs-lookup"><span data-stu-id="304c5-186">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="El resultado del ejemplo console.group()" lightbox="../media/console-demo-group-button.msft.png":::
         <span data-ttu-id="304c5-188">El resultado del `console.group()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="304c5-188">The result of the `console.group()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="groupcollapsed"></a><span data-ttu-id="304c5-189">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="304c5-189">groupCollapsed</span></span>  

<span data-ttu-id="304c5-190">Este método es idéntico al método [log,](#log) excepto que el grupo se contrae inicialmente cuando inicia sesión en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="304c5-190">This method is identical to the [log](#log) method, except the group is initially collapsed when it logs to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-191">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-191">JavaScript syntax</span></span>  

```javascript
console.groupCollapsed(label)
```  

---  

## <a name="groupend"></a><span data-ttu-id="304c5-192">groupEnd</span><span class="sxs-lookup"><span data-stu-id="304c5-192">groupEnd</span></span>  

<span data-ttu-id="304c5-193">Este método detiene la agrupación visual de mensajes.</span><span class="sxs-lookup"><span data-stu-id="304c5-193">This method stops visually grouping messages.</span></span>  <span data-ttu-id="304c5-194">Vaya al [método group.](#group)</span><span class="sxs-lookup"><span data-stu-id="304c5-194">Navigate to the [group](#group) method.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-195">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-195">JavaScript syntax</span></span>  

```javascript
console.groupEnd(label)
```  

---  

## <a name="info"></a><span data-ttu-id="304c5-196">información</span><span class="sxs-lookup"><span data-stu-id="304c5-196">info</span></span>  

<span data-ttu-id="304c5-197">Este método es idéntico al método [log.](#log)</span><span class="sxs-lookup"><span data-stu-id="304c5-197">This method is identical to the [log](#log) method.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-198">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-198">JavaScript syntax</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="304c5-199">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="304c5-199">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="304c5-200">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-200">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-201">Entrada</span><span class="sxs-lookup"><span data-stu-id="304c5-201">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.info('info');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-202">Salida</span><span class="sxs-lookup"><span data-stu-id="304c5-202">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="El resultado del ejemplo console.info()" lightbox="../media/console-demo-info-button.msft.png":::
         <span data-ttu-id="304c5-204">El resultado del `console.info()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="304c5-204">The result of the `console.info()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="log"></a><span data-ttu-id="304c5-205">log</span><span class="sxs-lookup"><span data-stu-id="304c5-205">log</span></span>  

<span data-ttu-id="304c5-206">Este método imprime un mensaje en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="304c5-206">This method prints a message to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-207">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-207">JavaScript syntax</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="304c5-208">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="304c5-208">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="304c5-209">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-209">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-210">Entrada</span><span class="sxs-lookup"><span data-stu-id="304c5-210">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.log('log');
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-211">Salida</span><span class="sxs-lookup"><span data-stu-id="304c5-211">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="El resultado del ejemplo console.log()" lightbox="../media/console-demo-log-button.msft.png":::
         <span data-ttu-id="304c5-213">El resultado del `console.log()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="304c5-213">The result of the `console.log()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a><span data-ttu-id="304c5-214">tabla</span><span class="sxs-lookup"><span data-stu-id="304c5-214">table</span></span>  

<span data-ttu-id="304c5-215">Este método registra una matriz de objetos como una tabla.</span><span class="sxs-lookup"><span data-stu-id="304c5-215">This method logs an array of objects as a table.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-216">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-216">JavaScript syntax</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="304c5-217">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="304c5-217">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="304c5-218">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-218">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-219">Entrada</span><span class="sxs-lookup"><span data-stu-id="304c5-219">Input</span></span>  
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
      <span data-ttu-id="304c5-220">Salida</span><span class="sxs-lookup"><span data-stu-id="304c5-220">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="El resultado del ejemplo console.table()" lightbox="../media/console-demo-table-button.msft.png":::
         <span data-ttu-id="304c5-222">El resultado del `console.table()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="304c5-222">The result of the `console.table()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="time"></a><span data-ttu-id="304c5-223">time</span><span class="sxs-lookup"><span data-stu-id="304c5-223">time</span></span>  

<span data-ttu-id="304c5-224">Este método inicia un nuevo temporizador.</span><span class="sxs-lookup"><span data-stu-id="304c5-224">This method starts a new timer.</span></span>  <span data-ttu-id="304c5-225">Utilice el [método timeEnd](#timeend) para detener el temporizador e imprimir el tiempo transcurrido en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="304c5-225">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-226">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-226">JavaScript syntax</span></span>  

```javascript
console.time([label])
```  

### <a name="javascript-example"></a><span data-ttu-id="304c5-227">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-227">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="304c5-228">Input</span></span>  
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
      <span data-ttu-id="304c5-229">Salida</span><span class="sxs-lookup"><span data-stu-id="304c5-229">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="El resultado del ejemplo console.time()" lightbox="../media/console-demo-time-button.msft.png":::
         <span data-ttu-id="304c5-231">El resultado del `console.time()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="304c5-231">The result of the `console.time()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="timeend"></a><span data-ttu-id="304c5-232">timeEnd</span><span class="sxs-lookup"><span data-stu-id="304c5-232">timeEnd</span></span>  

<span data-ttu-id="304c5-233">Este método detiene un temporizador.</span><span class="sxs-lookup"><span data-stu-id="304c5-233">This method stops a timer.</span></span>  <span data-ttu-id="304c5-234">Para obtener más información, vaya al [método time.](#time)</span><span class="sxs-lookup"><span data-stu-id="304c5-234">For more information, navigate to the [time](#time) method.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-235">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-235">JavaScript syntax</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="304c5-236">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="304c5-236">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

---  

## <a name="trace"></a><span data-ttu-id="304c5-237">seguimiento</span><span class="sxs-lookup"><span data-stu-id="304c5-237">trace</span></span>  

<span data-ttu-id="304c5-238">Este método imprime un seguimiento de pila en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="304c5-238">This method prints a stack trace to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-239">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-239">JavaScript syntax</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="304c5-240">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="304c5-240">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

### <a name="javascript-example"></a><span data-ttu-id="304c5-241">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-241">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-242">Entrada</span><span class="sxs-lookup"><span data-stu-id="304c5-242">Input</span></span>  
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
      <span data-ttu-id="304c5-243">Salida</span><span class="sxs-lookup"><span data-stu-id="304c5-243">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="El resultado del ejemplo console.trace()" lightbox="../media/console-demo-trace-button.msft.png":::
         <span data-ttu-id="304c5-245">El resultado del `console.trace()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="304c5-245">The result of the `console.trace()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="warn"></a><span data-ttu-id="304c5-246">warn</span><span class="sxs-lookup"><span data-stu-id="304c5-246">warn</span></span>  

<span data-ttu-id="304c5-247">Este método imprime una advertencia en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="304c5-247">This method prints a warning to the **Console**.</span></span>  

### <a name="javascript-syntax"></a><span data-ttu-id="304c5-248">Sintaxis de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-248">JavaScript syntax</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="304c5-249">[Nivel de registro][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="304c5-249">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

### <a name="javascript-example"></a><span data-ttu-id="304c5-250">Ejemplo de JavaScript</span><span class="sxs-lookup"><span data-stu-id="304c5-250">JavaScript example</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="304c5-251">Input</span></span>  
   :::column-end:::
   :::column span="3":::
      ```javascript
      console.warn('warn');
      ```
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="304c5-252">Salida</span><span class="sxs-lookup"><span data-stu-id="304c5-252">Output</span></span>
   :::column-end:::
   :::column span="3":::
      :::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="El resultado del ejemplo console.warn()" lightbox="../media/console-demo-warn-button.msft.png":::
         <span data-ttu-id="304c5-254">El resultado del `console.warn()` ejemplo</span><span class="sxs-lookup"><span data-stu-id="304c5-254">The result of the `console.warn()` example</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

---  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="304c5-255">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="304c5-255">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleLog]: ./console-log.md "Inicia sesión en la herramienta consola | Microsoft Docs"  
[DevtoolConsoleUtilities]: ./utilities.md "Referencia de api de utilidades de consola | Microsoft Docs"  
[DevtoolsConsoleReferenceClear]: ./reference.md#clear-the-console "Borrar la consola: referencia de consola | Microsoft Docs"  
[DevtoolsConsoleReferenceFilter]: ./reference.md#filter-by-log-level "Filtrar por nivel de registro: referencia de consola | Microsoft Docs"  
[DevtoolsConsoleReferencePersist]: ./reference.md#persist-messages-across-page-loads "Conservar mensajes entre cargas de página: referencia de consola | Microsoft Docs"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Introducción a las herramientas de desarrollador de Microsoft Edge (Chromium) | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="304c5-262">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="304c5-262">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="304c5-263">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/api) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="304c5-263">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="304c5-265">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="304c5-265">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

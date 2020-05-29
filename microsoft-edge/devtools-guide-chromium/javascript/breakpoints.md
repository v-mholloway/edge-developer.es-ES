---
title: Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 2afa4b7dbe96b65747ec17b147f0a82c16efa288
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581806"
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







# <span data-ttu-id="e2b60-103">Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e2b60-103">How To Pause Your Code With Breakpoints In Microsoft Edge DevTools</span></span>   



<span data-ttu-id="e2b60-104">Usa puntos de interrupción para pausar el código de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e2b60-104">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="e2b60-105">En esta guía se explica cada tipo de punto de interrupción que está disponible en DevTools, así como Cuándo usar y cómo establecer cada tipo.</span><span class="sxs-lookup"><span data-stu-id="e2b60-105">This guide explains each type of breakpoint that is available in DevTools, as well as when to use and how to set each type.</span></span>  <span data-ttu-id="e2b60-106">Para obtener un tutorial práctico del proceso de depuración, consulte Introducción [a la depuración de JavaScript en Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="e2b60-106">For a hands-on tutorial of the debugging process, see [Get Started with Debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>  

## <span data-ttu-id="e2b60-107">Información general sobre Cuándo usar cada tipo de punto de interrupción</span><span class="sxs-lookup"><span data-stu-id="e2b60-107">Overview of when to use each breakpoint type</span></span>   

<span data-ttu-id="e2b60-108">El tipo de punto de interrupción más conocido es la línea de código.</span><span class="sxs-lookup"><span data-stu-id="e2b60-108">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="e2b60-109">Pero los puntos de interrupción de línea de código pueden resultar ineficaces para establecerlos, sobre todo si no sabe exactamente dónde mirar o si está trabajando con un código base grande.</span><span class="sxs-lookup"><span data-stu-id="e2b60-109">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="e2b60-110">Puede ahorrar tiempo al depurar si conoce cómo y Cuándo usar los otros tipos de puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e2b60-110">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="e2b60-111">Tipo de punto de interrupción</span><span class="sxs-lookup"><span data-stu-id="e2b60-111">Breakpoint Type</span></span> | <span data-ttu-id="e2b60-112">Use esto cuando quiera hacer una pausa...</span><span class="sxs-lookup"><span data-stu-id="e2b60-112">Use This When You Want To Pause...</span></span>  |  
|:--- |:--- |  
| [<span data-ttu-id="e2b60-113">Línea de código</span><span class="sxs-lookup"><span data-stu-id="e2b60-113">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="e2b60-114">En una región exacta del código.</span><span class="sxs-lookup"><span data-stu-id="e2b60-114">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="e2b60-115">Línea de código condicional</span><span class="sxs-lookup"><span data-stu-id="e2b60-115">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="e2b60-116">En una región exacta de código, pero solo cuando alguna otra condición sea verdadera.</span><span class="sxs-lookup"><span data-stu-id="e2b60-116">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="e2b60-117">DOM</span><span class="sxs-lookup"><span data-stu-id="e2b60-117">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="e2b60-118">En el código que cambia o quita un nodo DOM específico o los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="e2b60-118">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="e2b60-119">XHR</span><span class="sxs-lookup"><span data-stu-id="e2b60-119">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="e2b60-120">Cuando una dirección URL de XHR contiene un patrón de cadena.</span><span class="sxs-lookup"><span data-stu-id="e2b60-120">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="e2b60-121">Detector de eventos</span><span class="sxs-lookup"><span data-stu-id="e2b60-121">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="e2b60-122">En el código que se ejecuta después de que se ejecute un evento, como, por ejemplo `click` ,.</span><span class="sxs-lookup"><span data-stu-id="e2b60-122">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="e2b60-123">Excepción</span><span class="sxs-lookup"><span data-stu-id="e2b60-123">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="e2b60-124">En la línea de código que produce una excepción detectada o no detectada.</span><span class="sxs-lookup"><span data-stu-id="e2b60-124">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="e2b60-125">Función</span><span class="sxs-lookup"><span data-stu-id="e2b60-125">Function</span></span>](#function-breakpoints) | <span data-ttu-id="e2b60-126">Siempre que se ejecute un comando, una función o un método específico.</span><span class="sxs-lookup"><span data-stu-id="e2b60-126">Whenever a specific command, function, or method is run.</span></span>  |  

## <span data-ttu-id="e2b60-127">Puntos de interrupción de línea de código</span><span class="sxs-lookup"><span data-stu-id="e2b60-127">Line-of-code breakpoints</span></span>   

<span data-ttu-id="e2b60-128">Use un punto de interrupción de línea de código cuando Conozca la región exacta de código que necesita investigar.</span><span class="sxs-lookup"><span data-stu-id="e2b60-128">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="e2b60-129">DevTools **siempre** se pausa antes de que se ejecute esta línea de código.</span><span class="sxs-lookup"><span data-stu-id="e2b60-129">DevTools **always** pauses before this line of code is run.</span></span>  

<span data-ttu-id="e2b60-130">Para establecer un punto de interrupción de línea de código en DevTools:</span><span class="sxs-lookup"><span data-stu-id="e2b60-130">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="e2b60-131">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="e2b60-131">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="e2b60-132">Abra el archivo que contiene la línea de código en la que desea interrumpir.</span><span class="sxs-lookup"><span data-stu-id="e2b60-132">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="e2b60-133">Ir a la línea de código.</span><span class="sxs-lookup"><span data-stu-id="e2b60-133">Go the line of code.</span></span>  
1.  <span data-ttu-id="e2b60-134">A la izquierda de la línea de código se encuentra la columna de número de línea.</span><span class="sxs-lookup"><span data-stu-id="e2b60-134">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="e2b60-135">Haz clic en él.</span><span class="sxs-lookup"><span data-stu-id="e2b60-135">Click on it.</span></span>  <span data-ttu-id="e2b60-136">Aparece un icono rojo junto a la columna número de línea.</span><span class="sxs-lookup"><span data-stu-id="e2b60-136">A red icon appears next to the line number column.</span></span>  

> ##### <span data-ttu-id="e2b60-137">Figura 1</span><span class="sxs-lookup"><span data-stu-id="e2b60-137">Figure 1</span></span>  
> <span data-ttu-id="e2b60-138">Un punto de interrupción de línea de código establecido en la línea 30</span><span class="sxs-lookup"><span data-stu-id="e2b60-138">A line-of-code breakpoint set on line 30</span></span>  
> ![Un punto de interrupción de línea de código][ImageLocBreakpoint]  

### <span data-ttu-id="e2b60-140">Puntos de interrupción de línea de código en el código</span><span class="sxs-lookup"><span data-stu-id="e2b60-140">Line-of-code breakpoints in your code</span></span>   

<span data-ttu-id="e2b60-141">Ejecuta el `debugger` método desde tu código para hacer una pausa en esa línea.</span><span class="sxs-lookup"><span data-stu-id="e2b60-141">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="e2b60-142">Es equivalente a un [punto de interrupción de línea de código](#line-of-code-breakpoints), excepto en que el punto de interrupción se establece en el código, no en la interfaz de usuario de DevTools.</span><span class="sxs-lookup"><span data-stu-id="e2b60-142">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <span data-ttu-id="e2b60-143">Puntos de interrupción de línea de código condicional</span><span class="sxs-lookup"><span data-stu-id="e2b60-143">Conditional line-of-code breakpoints</span></span>   

<span data-ttu-id="e2b60-144">Use un punto de interrupción de línea de código condicional cuando Conozca la región exacta de código que necesita investigar, pero solo desea pausarla cuando se cumpla otra condición.</span><span class="sxs-lookup"><span data-stu-id="e2b60-144">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="e2b60-145">Para establecer un punto de interrupción de línea de código condicional:</span><span class="sxs-lookup"><span data-stu-id="e2b60-145">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="e2b60-146">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="e2b60-146">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="e2b60-147">Abra el archivo que contiene la línea de código en la que desea interrumpir.</span><span class="sxs-lookup"><span data-stu-id="e2b60-147">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="e2b60-148">Ir a la línea de código.</span><span class="sxs-lookup"><span data-stu-id="e2b60-148">Go the line of code.</span></span>  
1.  <span data-ttu-id="e2b60-149">A la izquierda de la línea de código se encuentra la columna de número de línea.</span><span class="sxs-lookup"><span data-stu-id="e2b60-149">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="e2b60-150">Haga clic con el botón secundario en el número de línea.</span><span class="sxs-lookup"><span data-stu-id="e2b60-150">Right-click the line number.</span></span>  
1.  <span data-ttu-id="e2b60-151">Seleccione **Agregar punto de interrupción condicional**.</span><span class="sxs-lookup"><span data-stu-id="e2b60-151">Select **Add conditional breakpoint**.</span></span>  <span data-ttu-id="e2b60-152">Aparece un cuadro de diálogo debajo de la línea de código.</span><span class="sxs-lookup"><span data-stu-id="e2b60-152">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="e2b60-153">Escriba la condición en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e2b60-153">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="e2b60-154">Pulse `Enter` para activar el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e2b60-154">Press `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="e2b60-155">Un icono junto a la columna de números de línea.</span><span class="sxs-lookup"><span data-stu-id="e2b60-155">An icon next to the line number column.</span></span>  

> ##### <span data-ttu-id="e2b60-156">Figura 2</span><span class="sxs-lookup"><span data-stu-id="e2b60-156">Figure 2</span></span>  
> <span data-ttu-id="e2b60-157">Un punto de interrupción de línea de código condicional establecido en la línea 34</span><span class="sxs-lookup"><span data-stu-id="e2b60-157">A conditional line-of-code breakpoint set on line 34</span></span>  
> ![Punto de interrupción de línea de código condicional][ImageConditionalLocBreakpoint]  

### <span data-ttu-id="e2b60-159">Administrar puntos de interrupción de línea de código</span><span class="sxs-lookup"><span data-stu-id="e2b60-159">Manage line-of-code breakpoints</span></span>   

<span data-ttu-id="e2b60-160">Use el panel **puntos de interrupción** para deshabilitar o quitar puntos de interrupción de línea de código de una sola ubicación.</span><span class="sxs-lookup"><span data-stu-id="e2b60-160">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

> ##### <span data-ttu-id="e2b60-161">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="e2b60-161">Figure 3</span></span>  
> <span data-ttu-id="e2b60-162">El panel **puntos de interrupción** que muestra dos puntos de interrupción de línea de código: uno en la línea `16` de `get-started.js` , otro en la línea</span><span class="sxs-lookup"><span data-stu-id="e2b60-162">The **Breakpoints** panel showing two line-of-code breakpoints: one on line `16` of `get-started.js`, another on line</span></span> `33`  
> ![Panel puntos de interrupción][ImageBreakpointsPanel]  

*   <span data-ttu-id="e2b60-164">Active la casilla situada junto a una entrada para deshabilitar el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e2b60-164">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="e2b60-165">Haga clic con el botón secundario en una entrada para quitar ese punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e2b60-165">Right-click an entry to remove that breakpoint.</span></span>  
*   <span data-ttu-id="e2b60-166">Haga clic con el botón secundario en cualquier parte del panel **puntos de interrupción** para desactivar todos los puntos de interrupción, deshabilitar todos los puntos de interrupción o quitar todos los puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e2b60-166">Right-click anywhere in the **Breakpoints** pane to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="e2b60-167">Deshabilitar todos los puntos de interrupción es equivalente a desactivarlo.</span><span class="sxs-lookup"><span data-stu-id="e2b60-167">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="e2b60-168">Desactivar todos los puntos de interrupción indica a DevTools que pase por alto todos los puntos de interrupción de línea de código, pero también debe mantener el estado habilitado para que cada uno esté en el mismo estado que antes cuando reactive cada uno.</span><span class="sxs-lookup"><span data-stu-id="e2b60-168">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  

> ##### <span data-ttu-id="e2b60-169">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="e2b60-169">Figure 4</span></span>  
> <span data-ttu-id="e2b60-170">Los puntos de interrupción desactivados en el panel de **puntos de interrupción** están deshabilitados y son transparentes</span><span class="sxs-lookup"><span data-stu-id="e2b60-170">Deactivated breakpoints in the **Breakpoints** pane are disabled and transparent</span></span>  
> ![Puntos de interrupción desactivados en el panel de puntos de interrupción][ImageDeactivatedBreakpoints]  

## <span data-ttu-id="e2b60-172">DOM cambiar puntos de interrupción</span><span class="sxs-lookup"><span data-stu-id="e2b60-172">DOM change breakpoints</span></span>   

<span data-ttu-id="e2b60-173">Use un punto de interrupción de cambio de DOM cuando desee pausar el código que cambia un nodo DOM o los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="e2b60-173">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="e2b60-174">Para establecer un punto de interrupción de cambio de DOM:</span><span class="sxs-lookup"><span data-stu-id="e2b60-174">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="e2b60-175">Haga clic en la pestaña **elementos** .</span><span class="sxs-lookup"><span data-stu-id="e2b60-175">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="e2b60-176">Desplazarse por el elemento en el que desea establecer el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e2b60-176">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="e2b60-177">Haga clic con el botón secundario en el elemento.</span><span class="sxs-lookup"><span data-stu-id="e2b60-177">Right-click the element.</span></span>  
1.  <span data-ttu-id="e2b60-178">Mantenga el mouse sobre **break on**y, a continuación, seleccione **modificaciones de subárbol**, **modificaciones de atributos**o eliminación de **nodos**.</span><span class="sxs-lookup"><span data-stu-id="e2b60-178">Hover over **Break on**, then select **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  

> ##### <span data-ttu-id="e2b60-179">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="e2b60-179">Figure 5</span></span>  
> <span data-ttu-id="e2b60-180">Menú contextual para crear un punto de interrupción de cambio de DOM</span><span class="sxs-lookup"><span data-stu-id="e2b60-180">The context menu for creating a DOM change breakpoint</span></span>  
> ![Menú contextual para crear un punto de interrupción de cambio de DOM][ImageDomChangeBreakpoint]  

### <span data-ttu-id="e2b60-182">Tipos de puntos de interrupción de cambio de DOM</span><span class="sxs-lookup"><span data-stu-id="e2b60-182">Types of DOM change breakpoints</span></span>   

*   <span data-ttu-id="e2b60-183">**Modificaciones en el subárbol**.</span><span class="sxs-lookup"><span data-stu-id="e2b60-183">**Subtree modifications**.</span></span>  <span data-ttu-id="e2b60-184">Se desencadena cuando se quita o agrega un elemento secundario del nodo que se encuentra seleccionado, o se cambia el contenido de un elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="e2b60-184">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="e2b60-185">No se desencadena en cambios en los atributos del nodo secundario o en los cambios realizados en el nodo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="e2b60-185">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  

*   <span data-ttu-id="e2b60-186">**Modificaciones de atributos**: se desencadena cuando se agrega o se quita un atributo en el nodo seleccionado actualmente o cuando cambia un valor de atributo.</span><span class="sxs-lookup"><span data-stu-id="e2b60-186">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  

*   <span data-ttu-id="e2b60-187">**Eliminación de nodos**: se desencadena cuando se quita el nodo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="e2b60-187">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  

## <span data-ttu-id="e2b60-188">XHR/capturar puntos de interrupción</span><span class="sxs-lookup"><span data-stu-id="e2b60-188">XHR/Fetch breakpoints</span></span>   

<span data-ttu-id="e2b60-189">Use un punto de interrupción de XHR cuando desee interrumpir cuando la dirección URL de la solicitud de un XHR contiene una cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="e2b60-189">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="e2b60-190">DevTools se detiene en la línea de código donde el XHR ejecuta el `send()` método.</span><span class="sxs-lookup"><span data-stu-id="e2b60-190">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="e2b60-191">Esta característica también funciona con las solicitudes de [API de captura][MDNFetchApi] .</span><span class="sxs-lookup"><span data-stu-id="e2b60-191">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="e2b60-192">Un ejemplo de cuándo resulta útil es cuando ve que la página está solicitando una dirección URL incorrecta y desea buscar rápidamente los códigos de origen de AJAX o fetch que causan la solicitud incorrecta.</span><span class="sxs-lookup"><span data-stu-id="e2b60-192">One example of when this is helpful is when you see that your page is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="e2b60-193">Para establecer un punto de interrupción de XHR:</span><span class="sxs-lookup"><span data-stu-id="e2b60-193">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="e2b60-194">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="e2b60-194">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="e2b60-195">Expanda el panel de **puntos de interrupción XHR** .</span><span class="sxs-lookup"><span data-stu-id="e2b60-195">Expand the **XHR Breakpoints** pane.</span></span>  
1.  <span data-ttu-id="e2b60-196">Haga clic en **Agregar punto de interrupción**.</span><span class="sxs-lookup"><span data-stu-id="e2b60-196">Click **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="e2b60-197">Escriba la cadena en la que desea interrumpir.</span><span class="sxs-lookup"><span data-stu-id="e2b60-197">Enter the string which you want to break on.</span></span>  <span data-ttu-id="e2b60-198">DevTools se detiene cuando esta cadena está presente en cualquier lugar de una dirección URL de solicitud de XHR.</span><span class="sxs-lookup"><span data-stu-id="e2b60-198">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="e2b60-199">Pulse `Enter` para confirmar.</span><span class="sxs-lookup"><span data-stu-id="e2b60-199">Press `Enter` to confirm.</span></span>  

> ##### <span data-ttu-id="e2b60-200">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="e2b60-200">Figure 6</span></span>  
> <span data-ttu-id="e2b60-201">Crear un punto de interrupción de XHR en los **puntos de interrupción de XHR** para cualquier solicitud que contenga `org` la dirección URL</span><span class="sxs-lookup"><span data-stu-id="e2b60-201">Creating an XHR breakpoint in the **XHR Breakpoints** for any request that contains `org` in the URL</span></span>  
> ![Crear un punto de interrupción de XHR][ImageXhrBreakpoint]  

## <span data-ttu-id="e2b60-203">Puntos de interrupción de escucha de eventos</span><span class="sxs-lookup"><span data-stu-id="e2b60-203">Event listener breakpoints</span></span> 

<span data-ttu-id="e2b60-204">Use puntos de interrupción de escucha de eventos cuando desee pausar el código del agente de escucha de eventos que se ejecuta después de desencadenar un evento.</span><span class="sxs-lookup"><span data-stu-id="e2b60-204">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="e2b60-205">Puede seleccionar eventos específicos, como `click` o categorías de eventos, como todos los eventos del mouse.</span><span class="sxs-lookup"><span data-stu-id="e2b60-205">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="e2b60-206">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="e2b60-206">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="e2b60-207">Expanda el panel de **puntos de interrupción de escucha de eventos** .</span><span class="sxs-lookup"><span data-stu-id="e2b60-207">Expand the **Event Listener Breakpoints** pane.</span></span>  <span data-ttu-id="e2b60-208">DevTools muestra una lista de categorías de eventos, como la **animación**.</span><span class="sxs-lookup"><span data-stu-id="e2b60-208">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="e2b60-209">Active una de estas categorías para pausar cada vez que se desencadene un evento de la categoría o expanda la categoría y compruebe un evento específico.</span><span class="sxs-lookup"><span data-stu-id="e2b60-209">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  

> ##### <span data-ttu-id="e2b60-210">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="e2b60-210">Figure 7</span></span>  
> <span data-ttu-id="e2b60-211">Crear un punto de interrupción de detector de eventos para</span><span class="sxs-lookup"><span data-stu-id="e2b60-211">Creating an event listener breakpoint for</span></span> `deviceorientation`  
> ![Crear un punto de interrupción de detector de eventos][ImageEventListenerBreakpoint]  

## <span data-ttu-id="e2b60-213">Puntos de interrupción de excepción</span><span class="sxs-lookup"><span data-stu-id="e2b60-213">Exception breakpoints</span></span>   

<span data-ttu-id="e2b60-214">Use puntos de interrupción de excepción cuando desee hacer una pausa en la línea de código que produce una excepción detectada o no detectada.</span><span class="sxs-lookup"><span data-stu-id="e2b60-214">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="e2b60-215">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="e2b60-215">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="e2b60-216">Haga clic en pausar **en excepciones** ![ en excepciones ][ImagePauseOnExceptionsIcon] .</span><span class="sxs-lookup"><span data-stu-id="e2b60-216">Click **Pause on exceptions** ![Pause on exceptions][ImagePauseOnExceptionsIcon].</span></span>  <span data-ttu-id="e2b60-217">El icono se vuelve azul al habilitarlo.</span><span class="sxs-lookup"><span data-stu-id="e2b60-217">The icon turns blue when enabled.</span></span>  
    
    > ##### <span data-ttu-id="e2b60-218">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="e2b60-218">Figure 8</span></span>  
    > <span data-ttu-id="e2b60-219">El botón **pausar en las excepciones**</span><span class="sxs-lookup"><span data-stu-id="e2b60-219">The **Pause on exceptions** button</span></span>  
    > ![El botón pausar en las excepciones][ImagePauseExceptionsHighlight]  

1.  <span data-ttu-id="e2b60-221">**Opcional**.</span><span class="sxs-lookup"><span data-stu-id="e2b60-221">**Optional**.</span></span> <span data-ttu-id="e2b60-222">Active la casilla **pausar las excepciones capturadas** si también desea pausar las excepciones detectadas, además de las no capturadas.</span><span class="sxs-lookup"><span data-stu-id="e2b60-222">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  

> ##### <span data-ttu-id="e2b60-223">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="e2b60-223">Figure 9</span></span>  
> <span data-ttu-id="e2b60-224">Pausado en una excepción no detectada</span><span class="sxs-lookup"><span data-stu-id="e2b60-224">Paused on an uncaught exception</span></span>  
> ![Pausado en una excepción no detectada][ImageUncaughtException]  

## <span data-ttu-id="e2b60-226">Puntos de interrupción de función</span><span class="sxs-lookup"><span data-stu-id="e2b60-226">Function breakpoints</span></span>   

<span data-ttu-id="e2b60-227">Ejecute el `debug(method)` método, donde `method` es el comando, la función o el método que desea depurar, cuando desee pausarlo siempre que se ejecute una función específica.</span><span class="sxs-lookup"><span data-stu-id="e2b60-227">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="e2b60-228">Puede insertar `debug()` el código (como una `console.log()` instrucción) o ejecutar el método desde la consola de DevTools.</span><span class="sxs-lookup"><span data-stu-id="e2b60-228">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="e2b60-229">es equivalente a establecer un [punto de interrupción de línea de código](#line-of-code-breakpoints) en la primera línea de la función.</span><span class="sxs-lookup"><span data-stu-id="e2b60-229">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <span data-ttu-id="e2b60-230">Asegurarse de que la función de destino está en el ámbito</span><span class="sxs-lookup"><span data-stu-id="e2b60-230">Make sure the target function is in scope</span></span>   

<span data-ttu-id="e2b60-231">DevTools inicia una `ReferenceError` si la función que desea depurar no está en el ámbito.</span><span class="sxs-lookup"><span data-stu-id="e2b60-231">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

```javascript
(function () {
    function hey() {
        console.log('hey');
    }
    function yo() {
        console.log('yo');
    }
    debug(yo); // This works.
    yo();
})();
debug(hey); // This does not work.  hey() is out of scope.
```  

<span data-ttu-id="e2b60-232">Garantizar que la función de destino esté dentro del ámbito es complicada si está ejecutando el `debug()` método desde la consola de DevTools.</span><span class="sxs-lookup"><span data-stu-id="e2b60-232">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="e2b60-233">Esta es una estrategia:</span><span class="sxs-lookup"><span data-stu-id="e2b60-233">Here is one strategy:</span></span>  

1.  <span data-ttu-id="e2b60-234">Establezca un [punto de interrupción de línea de código](#line-of-code-breakpoints) en el lugar donde se encuentra la función en el ámbito.</span><span class="sxs-lookup"><span data-stu-id="e2b60-234">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="e2b60-235">Desencadenar el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="e2b60-235">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="e2b60-236">Ejecuta el `debug()` método en la consola de DevTools mientras el código está en pausa en el punto de interrupción de línea de código.</span><span class="sxs-lookup"><span data-stu-id="e2b60-236">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  

 



<!-- image links -->  

[ImagePauseOnExceptionsIcon]: /microsoft-edge/devtools-guide-chromium/media/pause-on-exceptions-icon.msft.png  

[ImageLocBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-breakpoint-30.msft.png "Ilustración 1: un punto de interrupción de línea de código"  
[ImageConditionalLocBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-conditional-breakpoint.msft.png "Ilustración 2: un punto de interrupción de línea de código condicional"  
[ImageBreakpointsPanel]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-breakpoints-16-33.msft.png "Ilustración 3: el panel puntos de interrupción"  
[ImageDeactivatedBreakpoints]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png "Ilustración 4: puntos de interrupción desactivados en el panel de puntos de interrupción"  
[ImageDomChangeBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-elements-break-on-subtree-modifications.msft.png "Ilustración 5: el menú contextual para crear un punto de interrupción de cambio de DOM"  
[ImageXhrBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png "Ilustración 6: crear un punto de interrupción de XHR"  
[ImageEventListenerBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png "Ilustración 7: crear un punto de interrupción de detector de eventos"  
[ImagePauseExceptionsHighlight]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-pause-on-exceptions.msft.png "Ilustración 8: el botón pausar en las excepciones"  
[ImageUncaughtException]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-js-paused-on-exception.msft.png "Ilustración 9: pausado en una excepción no detectada"  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Fetch API | MDN"  

> [!NOTE]
> <span data-ttu-id="e2b60-248">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e2b60-248">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e2b60-249">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) y está creada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e2b60-249">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  
[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e2b60-251">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e2b60-251">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

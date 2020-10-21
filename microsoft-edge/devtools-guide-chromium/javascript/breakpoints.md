---
description: Obtén más información sobre las formas en que puedes pausar tu código en Microsoft Edge DevTools.
title: Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 98c0e42657d9b0900d3eaca8af69f1c17abfcf06
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124813"
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

# <span data-ttu-id="ee131-104">Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ee131-104">How to pause your code with breakpoints in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="ee131-105">Usa puntos de interrupción para pausar el código de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ee131-105">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="ee131-106">En esta guía se explica cada tipo de punto de interrupción que está disponible en DevTools, así como Cuándo usar y cómo establecer cada tipo.</span><span class="sxs-lookup"><span data-stu-id="ee131-106">This guide explains each type of breakpoint that is available in DevTools, as well as when to use and how to set each type.</span></span>  <span data-ttu-id="ee131-107">Para obtener un tutorial práctico del proceso de depuración, vaya a [Introducción a la depuración de JavaScript en Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="ee131-107">For a hands-on tutorial of the debugging process, navigate to [Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>  

## <span data-ttu-id="ee131-108">Información general sobre Cuándo usar cada tipo de punto de interrupción</span><span class="sxs-lookup"><span data-stu-id="ee131-108">Overview of when to use each breakpoint type</span></span>  

<span data-ttu-id="ee131-109">El tipo de punto de interrupción más conocido es la línea de código.</span><span class="sxs-lookup"><span data-stu-id="ee131-109">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="ee131-110">Pero los puntos de interrupción de línea de código pueden resultar ineficaces para establecerlos, sobre todo si no sabe exactamente dónde mirar o si está trabajando con un código base grande.</span><span class="sxs-lookup"><span data-stu-id="ee131-110">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="ee131-111">Puede ahorrar tiempo al depurar si conoce cómo y Cuándo usar los otros tipos de puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ee131-111">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="ee131-112">Tipo de punto de interrupción</span><span class="sxs-lookup"><span data-stu-id="ee131-112">Breakpoint Type</span></span> | <span data-ttu-id="ee131-113">Use esto cuando quiera hacer una pausa...</span><span class="sxs-lookup"><span data-stu-id="ee131-113">Use This When You Want To Pause...</span></span>  |  
|:--- |:--- |  
| [<span data-ttu-id="ee131-114">Línea de código</span><span class="sxs-lookup"><span data-stu-id="ee131-114">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="ee131-115">En una región exacta del código.</span><span class="sxs-lookup"><span data-stu-id="ee131-115">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="ee131-116">Línea de código condicional</span><span class="sxs-lookup"><span data-stu-id="ee131-116">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="ee131-117">En una región exacta de código, pero solo cuando alguna otra condición sea verdadera.</span><span class="sxs-lookup"><span data-stu-id="ee131-117">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="ee131-118">DOM</span><span class="sxs-lookup"><span data-stu-id="ee131-118">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="ee131-119">En el código que cambia o quita un nodo DOM específico o los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="ee131-119">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="ee131-120">XHR</span><span class="sxs-lookup"><span data-stu-id="ee131-120">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="ee131-121">Cuando una dirección URL de XHR contiene un patrón de cadena.</span><span class="sxs-lookup"><span data-stu-id="ee131-121">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="ee131-122">Detector de eventos</span><span class="sxs-lookup"><span data-stu-id="ee131-122">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="ee131-123">En el código que se ejecuta después de que se ejecute un evento, como, por ejemplo `click` ,.</span><span class="sxs-lookup"><span data-stu-id="ee131-123">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="ee131-124">Excepción</span><span class="sxs-lookup"><span data-stu-id="ee131-124">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="ee131-125">En la línea de código que produce una excepción detectada o no detectada.</span><span class="sxs-lookup"><span data-stu-id="ee131-125">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="ee131-126">Función</span><span class="sxs-lookup"><span data-stu-id="ee131-126">Function</span></span>](#function-breakpoints) | <span data-ttu-id="ee131-127">Siempre que se ejecute un comando, una función o un método específico.</span><span class="sxs-lookup"><span data-stu-id="ee131-127">Whenever a specific command, function, or method is run.</span></span>  |  

## <span data-ttu-id="ee131-128">Puntos de interrupción de línea de código</span><span class="sxs-lookup"><span data-stu-id="ee131-128">Line-of-code breakpoints</span></span>  

<span data-ttu-id="ee131-129">Use un punto de interrupción de línea de código cuando Conozca la región exacta de código que necesita investigar.</span><span class="sxs-lookup"><span data-stu-id="ee131-129">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="ee131-130">DevTools siempre se pausa antes de que se ejecute esta línea de código.</span><span class="sxs-lookup"><span data-stu-id="ee131-130">DevTools always pauses before this line of code is run.</span></span>  

<span data-ttu-id="ee131-131">Para establecer un punto de interrupción de línea de código en DevTools:</span><span class="sxs-lookup"><span data-stu-id="ee131-131">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="ee131-132">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="ee131-132">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="ee131-133">Abra el archivo que contiene la línea de código en la que desea interrumpir.</span><span class="sxs-lookup"><span data-stu-id="ee131-133">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="ee131-134">Ir a la línea de código.</span><span class="sxs-lookup"><span data-stu-id="ee131-134">Go the line of code.</span></span>  
1.  <span data-ttu-id="ee131-135">A la izquierda de la línea de código se encuentra la columna de número de línea.</span><span class="sxs-lookup"><span data-stu-id="ee131-135">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="ee131-136">Haz clic en él.</span><span class="sxs-lookup"><span data-stu-id="ee131-136">Click on it.</span></span>  <span data-ttu-id="ee131-137">Aparece un icono rojo junto a la columna número de línea.</span><span class="sxs-lookup"><span data-stu-id="ee131-137">A red icon appears next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Un punto de interrupción de línea de código" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="ee131-139">Un punto de interrupción de línea de código</span><span class="sxs-lookup"><span data-stu-id="ee131-139">A line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="ee131-140">Puntos de interrupción de línea de código en el código</span><span class="sxs-lookup"><span data-stu-id="ee131-140">Line-of-code breakpoints in your code</span></span>  

<span data-ttu-id="ee131-141">Ejecuta el `debugger` método desde tu código para hacer una pausa en esa línea.</span><span class="sxs-lookup"><span data-stu-id="ee131-141">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="ee131-142">Es equivalente a un [punto de interrupción de línea de código](#line-of-code-breakpoints), excepto en que el punto de interrupción se establece en el código, no en la interfaz de usuario de DevTools.</span><span class="sxs-lookup"><span data-stu-id="ee131-142">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <span data-ttu-id="ee131-143">Puntos de interrupción de línea de código condicional</span><span class="sxs-lookup"><span data-stu-id="ee131-143">Conditional line-of-code breakpoints</span></span>  

<span data-ttu-id="ee131-144">Use un punto de interrupción de línea de código condicional cuando Conozca la región exacta de código que necesita investigar, pero solo desea pausarla cuando se cumpla otra condición.</span><span class="sxs-lookup"><span data-stu-id="ee131-144">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="ee131-145">Para establecer un punto de interrupción de línea de código condicional:</span><span class="sxs-lookup"><span data-stu-id="ee131-145">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="ee131-146">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="ee131-146">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="ee131-147">Abra el archivo que contiene la línea de código en la que desea interrumpir.</span><span class="sxs-lookup"><span data-stu-id="ee131-147">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="ee131-148">Ir a la línea de código.</span><span class="sxs-lookup"><span data-stu-id="ee131-148">Go the line of code.</span></span>  
1.  <span data-ttu-id="ee131-149">A la izquierda de la línea de código se encuentra la columna de número de línea.</span><span class="sxs-lookup"><span data-stu-id="ee131-149">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="ee131-150">Haga clic con el botón secundario en el número de línea.</span><span class="sxs-lookup"><span data-stu-id="ee131-150">Right-click the line number.</span></span>  
1.  <span data-ttu-id="ee131-151">Elija **Agregar punto de interrupción condicional**.</span><span class="sxs-lookup"><span data-stu-id="ee131-151">Choose **Add conditional breakpoint**.</span></span>  <span data-ttu-id="ee131-152">Aparece un cuadro de diálogo debajo de la línea de código.</span><span class="sxs-lookup"><span data-stu-id="ee131-152">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="ee131-153">Escriba la condición en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ee131-153">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="ee131-154">Seleccione `Enter` esta para activar el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ee131-154">Select `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="ee131-155">Un icono junto a la columna de números de línea.</span><span class="sxs-lookup"><span data-stu-id="ee131-155">An icon next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Un punto de interrupción de línea de código" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       <span data-ttu-id="ee131-157">Punto de interrupción de línea de código condicional</span><span class="sxs-lookup"><span data-stu-id="ee131-157">A conditional line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="ee131-158">Administrar puntos de interrupción de línea de código</span><span class="sxs-lookup"><span data-stu-id="ee131-158">Manage line-of-code breakpoints</span></span>  

<span data-ttu-id="ee131-159">Use el panel **puntos de interrupción** para deshabilitar o quitar puntos de interrupción de línea de código de una sola ubicación.</span><span class="sxs-lookup"><span data-stu-id="ee131-159">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Un punto de interrupción de línea de código" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   <span data-ttu-id="ee131-161">Panel **puntos de interrupción**</span><span class="sxs-lookup"><span data-stu-id="ee131-161">The **Breakpoints** panel</span></span>  
:::image-end:::  

*   <span data-ttu-id="ee131-162">Active la casilla situada junto a una entrada para deshabilitar el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ee131-162">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="ee131-163">Haga clic con el botón secundario en una entrada para quitar ese punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ee131-163">Right-click an entry to remove that breakpoint.</span></span>  
*   <span data-ttu-id="ee131-164">Haga clic con el botón secundario en cualquier parte del panel **puntos de interrupción** para desactivar todos los puntos de interrupción, deshabilitar todos los puntos de interrupción o quitar todos los puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ee131-164">Right-click anywhere in the **Breakpoints** pane to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="ee131-165">Deshabilitar todos los puntos de interrupción es equivalente a desactivarlo.</span><span class="sxs-lookup"><span data-stu-id="ee131-165">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="ee131-166">Desactivar todos los puntos de interrupción indica a DevTools que pase por alto todos los puntos de interrupción de línea de código, pero también debe mantener el estado habilitado para que cada uno esté en el mismo estado que antes cuando reactive cada uno.</span><span class="sxs-lookup"><span data-stu-id="ee131-166">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Un punto de interrupción de línea de código" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       <span data-ttu-id="ee131-168">Puntos de interrupción desactivados en el panel de **puntos de interrupción**</span><span class="sxs-lookup"><span data-stu-id="ee131-168">Deactivated breakpoints in the **Breakpoints** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ee131-169">DOM cambiar puntos de interrupción</span><span class="sxs-lookup"><span data-stu-id="ee131-169">DOM change breakpoints</span></span>  

<span data-ttu-id="ee131-170">Use un punto de interrupción de cambio de DOM cuando desee pausar el código que cambia un nodo DOM o los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="ee131-170">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="ee131-171">Para establecer un punto de interrupción de cambio de DOM:</span><span class="sxs-lookup"><span data-stu-id="ee131-171">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="ee131-172">Haga clic en la pestaña **elementos** .</span><span class="sxs-lookup"><span data-stu-id="ee131-172">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="ee131-173">Desplazarse por el elemento en el que desea establecer el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ee131-173">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="ee131-174">Haga clic con el botón secundario en el elemento.</span><span class="sxs-lookup"><span data-stu-id="ee131-174">Right-click the element.</span></span>  
1.  <span data-ttu-id="ee131-175">Desplace el puntero sobre **interrumpir**y, a continuación, elija **modificaciones de subárbol**, **modificaciones de atributos**o eliminación de **nodos**.</span><span class="sxs-lookup"><span data-stu-id="ee131-175">Hover over **Break on**, then choose **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Un punto de interrupción de línea de código" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       <span data-ttu-id="ee131-177">Menú contextual para crear un punto de interrupción de cambio de DOM</span><span class="sxs-lookup"><span data-stu-id="ee131-177">The context menu for creating a DOM change breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="ee131-178">Tipos de puntos de interrupción de cambio de DOM</span><span class="sxs-lookup"><span data-stu-id="ee131-178">Types of DOM change breakpoints</span></span>  

*   <span data-ttu-id="ee131-179">**Modificaciones en el subárbol**.</span><span class="sxs-lookup"><span data-stu-id="ee131-179">**Subtree modifications**.</span></span>  <span data-ttu-id="ee131-180">Se desencadena cuando se quita o agrega un elemento secundario del nodo que se encuentra seleccionado, o se cambia el contenido de un elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="ee131-180">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="ee131-181">No se desencadena en cambios en los atributos del nodo secundario o en los cambios realizados en el nodo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="ee131-181">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  
*   <span data-ttu-id="ee131-182">**Modificaciones de atributos**: se desencadena cuando se agrega o se quita un atributo en el nodo seleccionado actualmente o cuando cambia un valor de atributo.</span><span class="sxs-lookup"><span data-stu-id="ee131-182">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  
*   <span data-ttu-id="ee131-183">**Eliminación de nodos**: se desencadena cuando se quita el nodo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="ee131-183">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  
    
## <span data-ttu-id="ee131-184">XHR/capturar puntos de interrupción</span><span class="sxs-lookup"><span data-stu-id="ee131-184">XHR/Fetch breakpoints</span></span>  

<span data-ttu-id="ee131-185">Use un punto de interrupción de XHR cuando desee interrumpir cuando la dirección URL de la solicitud de un XHR contiene una cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="ee131-185">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="ee131-186">DevTools se detiene en la línea de código donde el XHR ejecuta el `send()` método.</span><span class="sxs-lookup"><span data-stu-id="ee131-186">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="ee131-187">Esta característica también funciona con las solicitudes de [API de captura][MDNFetchApi] .</span><span class="sxs-lookup"><span data-stu-id="ee131-187">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="ee131-188">Un ejemplo de cuándo resulta útil es cuando ve que la página está solicitando una dirección URL incorrecta y desea buscar rápidamente los códigos de origen de AJAX o fetch que causan la solicitud incorrecta.</span><span class="sxs-lookup"><span data-stu-id="ee131-188">One example of when this is helpful is when you see that your page is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="ee131-189">Para establecer un punto de interrupción de XHR:</span><span class="sxs-lookup"><span data-stu-id="ee131-189">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="ee131-190">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="ee131-190">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="ee131-191">Expanda el panel de **puntos de interrupción XHR** .</span><span class="sxs-lookup"><span data-stu-id="ee131-191">Expand the **XHR Breakpoints** pane.</span></span>  
1.  <span data-ttu-id="ee131-192">Elija **Agregar punto de interrupción**.</span><span class="sxs-lookup"><span data-stu-id="ee131-192">Choose **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="ee131-193">Escriba la cadena en la que desea interrumpir.</span><span class="sxs-lookup"><span data-stu-id="ee131-193">Enter the string which you want to break on.</span></span>  <span data-ttu-id="ee131-194">DevTools se detiene cuando esta cadena está presente en cualquier lugar de una dirección URL de solicitud de XHR.</span><span class="sxs-lookup"><span data-stu-id="ee131-194">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="ee131-195">Seleccione `Enter` para confirmar.</span><span class="sxs-lookup"><span data-stu-id="ee131-195">Select `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Un punto de interrupción de línea de código" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       <span data-ttu-id="ee131-197">Crear un punto de interrupción de XHR</span><span class="sxs-lookup"><span data-stu-id="ee131-197">Create an XHR breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ee131-198">Puntos de interrupción de escucha de eventos</span><span class="sxs-lookup"><span data-stu-id="ee131-198">Event listener breakpoints</span></span>   

<span data-ttu-id="ee131-199">Use puntos de interrupción de escucha de eventos cuando desee pausar el código del agente de escucha de eventos que se ejecuta después de desencadenar un evento.</span><span class="sxs-lookup"><span data-stu-id="ee131-199">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="ee131-200">Puede seleccionar eventos específicos, como `click` o categorías de eventos, como todos los eventos del mouse.</span><span class="sxs-lookup"><span data-stu-id="ee131-200">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="ee131-201">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="ee131-201">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="ee131-202">Expanda el panel de **puntos de interrupción de escucha de eventos** .</span><span class="sxs-lookup"><span data-stu-id="ee131-202">Expand the **Event Listener Breakpoints** pane.</span></span>  <span data-ttu-id="ee131-203">DevTools muestra una lista de categorías de eventos, como la **animación**.</span><span class="sxs-lookup"><span data-stu-id="ee131-203">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="ee131-204">Active una de estas categorías para pausar cada vez que se desencadene un evento de la categoría o expanda la categoría y compruebe un evento específico.</span><span class="sxs-lookup"><span data-stu-id="ee131-204">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Un punto de interrupción de línea de código" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       <span data-ttu-id="ee131-206">Crear un punto de interrupción de detector de eventos</span><span class="sxs-lookup"><span data-stu-id="ee131-206">Create an event listener breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ee131-207">Puntos de interrupción de excepción</span><span class="sxs-lookup"><span data-stu-id="ee131-207">Exception breakpoints</span></span>  

<span data-ttu-id="ee131-208">Use puntos de interrupción de excepción cuando desee hacer una pausa en la línea de código que produce una excepción detectada o no detectada.</span><span class="sxs-lookup"><span data-stu-id="ee131-208">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="ee131-209">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="ee131-209">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="ee131-210">Elija **pausar en excepciones** \ ( ![ pausar en excepciones ][ImagePauseOnExceptionsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="ee131-210">Choose **Pause on exceptions** \(![Pause on exceptions][ImagePauseOnExceptionsIcon]\).</span></span>  <span data-ttu-id="ee131-211">El icono se vuelve azul al habilitarlo.</span><span class="sxs-lookup"><span data-stu-id="ee131-211">The icon turns blue when enabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Un punto de interrupción de línea de código" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       <span data-ttu-id="ee131-213">El botón **pausar en las excepciones**</span><span class="sxs-lookup"><span data-stu-id="ee131-213">The **Pause on exceptions** button</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ee131-214">**Opcional**.</span><span class="sxs-lookup"><span data-stu-id="ee131-214">**Optional**.</span></span>  <span data-ttu-id="ee131-215">Active la casilla **pausar las excepciones capturadas** si también desea pausar las excepciones detectadas, además de las no capturadas.</span><span class="sxs-lookup"><span data-stu-id="ee131-215">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Un punto de interrupción de línea de código" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       <span data-ttu-id="ee131-217">Pausado en una excepción no detectada</span><span class="sxs-lookup"><span data-stu-id="ee131-217">Paused on an uncaught exception</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ee131-218">Puntos de interrupción de función</span><span class="sxs-lookup"><span data-stu-id="ee131-218">Function breakpoints</span></span>  

<span data-ttu-id="ee131-219">Ejecute el `debug(method)` método, donde `method` es el comando, la función o el método que desea depurar, cuando desee pausarlo siempre que se ejecute una función específica.</span><span class="sxs-lookup"><span data-stu-id="ee131-219">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="ee131-220">Puede insertar `debug()` el código (como una `console.log()` instrucción) o ejecutar el método desde la consola de DevTools.</span><span class="sxs-lookup"><span data-stu-id="ee131-220">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="ee131-221">es equivalente a establecer un [punto de interrupción de línea de código](#line-of-code-breakpoints) en la primera línea de la función.</span><span class="sxs-lookup"><span data-stu-id="ee131-221">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <span data-ttu-id="ee131-222">Asegurarse de que la función de destino está en el ámbito</span><span class="sxs-lookup"><span data-stu-id="ee131-222">Make sure the target function is in scope</span></span>  

<span data-ttu-id="ee131-223">DevTools inicia una `ReferenceError` si la función que desea depurar no está en el ámbito.</span><span class="sxs-lookup"><span data-stu-id="ee131-223">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

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

<span data-ttu-id="ee131-224">Garantizar que la función de destino esté dentro del ámbito es complicada si está ejecutando el `debug()` método desde la consola de DevTools.</span><span class="sxs-lookup"><span data-stu-id="ee131-224">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="ee131-225">Esta es una estrategia:</span><span class="sxs-lookup"><span data-stu-id="ee131-225">Here is one strategy:</span></span>  

1.  <span data-ttu-id="ee131-226">Establezca un [punto de interrupción de línea de código](#line-of-code-breakpoints) en el lugar donde se encuentra la función en el ámbito.</span><span class="sxs-lookup"><span data-stu-id="ee131-226">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="ee131-227">Desencadenar el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="ee131-227">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="ee131-228">Ejecuta el `debug()` método en la consola de DevTools mientras el código está en pausa en el punto de interrupción de línea de código.</span><span class="sxs-lookup"><span data-stu-id="ee131-228">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  
    
## <span data-ttu-id="ee131-229">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ee131-229">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft docs"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Fetch API | MDN"  

> [!NOTE]
> <span data-ttu-id="ee131-232">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ee131-232">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ee131-233">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="ee131-233">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ee131-235">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ee131-235">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

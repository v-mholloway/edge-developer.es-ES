---
title: Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 804e864ee3029a49ba1ef2ac1f2deb61c3ba5ec3
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983229"
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







# <span data-ttu-id="31ac3-103">Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="31ac3-103">How to pause your code with breakpoints in Microsoft Edge DevTools</span></span>   



<span data-ttu-id="31ac3-104">Usa puntos de interrupción para pausar el código de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="31ac3-104">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="31ac3-105">En esta guía se explica cada tipo de punto de interrupción que está disponible en DevTools, así como Cuándo usar y cómo establecer cada tipo.</span><span class="sxs-lookup"><span data-stu-id="31ac3-105">This guide explains each type of breakpoint that is available in DevTools, as well as when to use and how to set each type.</span></span>  <span data-ttu-id="31ac3-106">Para obtener un tutorial práctico del proceso de depuración, consulte Introducción [a la depuración de JavaScript en Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="31ac3-106">For a hands-on tutorial of the debugging process, see [Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>  

## <span data-ttu-id="31ac3-107">Información general sobre Cuándo usar cada tipo de punto de interrupción</span><span class="sxs-lookup"><span data-stu-id="31ac3-107">Overview of when to use each breakpoint type</span></span>   

<span data-ttu-id="31ac3-108">El tipo de punto de interrupción más conocido es la línea de código.</span><span class="sxs-lookup"><span data-stu-id="31ac3-108">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="31ac3-109">Pero los puntos de interrupción de línea de código pueden resultar ineficaces para establecerlos, sobre todo si no sabe exactamente dónde mirar o si está trabajando con un código base grande.</span><span class="sxs-lookup"><span data-stu-id="31ac3-109">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="31ac3-110">Puede ahorrar tiempo al depurar si conoce cómo y Cuándo usar los otros tipos de puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="31ac3-110">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="31ac3-111">Tipo de punto de interrupción</span><span class="sxs-lookup"><span data-stu-id="31ac3-111">Breakpoint Type</span></span> | <span data-ttu-id="31ac3-112">Use esto cuando quiera hacer una pausa...</span><span class="sxs-lookup"><span data-stu-id="31ac3-112">Use This When You Want To Pause...</span></span>  |  
|:--- |:--- |  
| [<span data-ttu-id="31ac3-113">Línea de código</span><span class="sxs-lookup"><span data-stu-id="31ac3-113">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="31ac3-114">En una región exacta del código.</span><span class="sxs-lookup"><span data-stu-id="31ac3-114">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="31ac3-115">Línea de código condicional</span><span class="sxs-lookup"><span data-stu-id="31ac3-115">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="31ac3-116">En una región exacta de código, pero solo cuando alguna otra condición sea verdadera.</span><span class="sxs-lookup"><span data-stu-id="31ac3-116">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="31ac3-117">DOM</span><span class="sxs-lookup"><span data-stu-id="31ac3-117">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="31ac3-118">En el código que cambia o quita un nodo DOM específico o los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="31ac3-118">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="31ac3-119">XHR</span><span class="sxs-lookup"><span data-stu-id="31ac3-119">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="31ac3-120">Cuando una dirección URL de XHR contiene un patrón de cadena.</span><span class="sxs-lookup"><span data-stu-id="31ac3-120">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="31ac3-121">Detector de eventos</span><span class="sxs-lookup"><span data-stu-id="31ac3-121">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="31ac3-122">En el código que se ejecuta después de que se ejecute un evento, como, por ejemplo `click` ,.</span><span class="sxs-lookup"><span data-stu-id="31ac3-122">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="31ac3-123">Excepción</span><span class="sxs-lookup"><span data-stu-id="31ac3-123">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="31ac3-124">En la línea de código que produce una excepción detectada o no detectada.</span><span class="sxs-lookup"><span data-stu-id="31ac3-124">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="31ac3-125">Función</span><span class="sxs-lookup"><span data-stu-id="31ac3-125">Function</span></span>](#function-breakpoints) | <span data-ttu-id="31ac3-126">Siempre que se ejecute un comando, una función o un método específico.</span><span class="sxs-lookup"><span data-stu-id="31ac3-126">Whenever a specific command, function, or method is run.</span></span>  |  

## <span data-ttu-id="31ac3-127">Puntos de interrupción de línea de código</span><span class="sxs-lookup"><span data-stu-id="31ac3-127">Line-of-code breakpoints</span></span>   

<span data-ttu-id="31ac3-128">Use un punto de interrupción de línea de código cuando Conozca la región exacta de código que necesita investigar.</span><span class="sxs-lookup"><span data-stu-id="31ac3-128">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="31ac3-129">DevTools siempre se pausa antes de que se ejecute esta línea de código.</span><span class="sxs-lookup"><span data-stu-id="31ac3-129">DevTools always pauses before this line of code is run.</span></span>  

<span data-ttu-id="31ac3-130">Para establecer un punto de interrupción de línea de código en DevTools:</span><span class="sxs-lookup"><span data-stu-id="31ac3-130">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="31ac3-131">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="31ac3-131">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="31ac3-132">Abra el archivo que contiene la línea de código en la que desea interrumpir.</span><span class="sxs-lookup"><span data-stu-id="31ac3-132">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="31ac3-133">Ir a la línea de código.</span><span class="sxs-lookup"><span data-stu-id="31ac3-133">Go the line of code.</span></span>  
1.  <span data-ttu-id="31ac3-134">A la izquierda de la línea de código se encuentra la columna de número de línea.</span><span class="sxs-lookup"><span data-stu-id="31ac3-134">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="31ac3-135">Haz clic en él.</span><span class="sxs-lookup"><span data-stu-id="31ac3-135">Click on it.</span></span>  <span data-ttu-id="31ac3-136">Aparece un icono rojo junto a la columna número de línea.</span><span class="sxs-lookup"><span data-stu-id="31ac3-136">A red icon appears next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Un punto de interrupción de línea de código" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="31ac3-138">Un punto de interrupción de línea de código</span><span class="sxs-lookup"><span data-stu-id="31ac3-138">A line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="31ac3-139">Puntos de interrupción de línea de código en el código</span><span class="sxs-lookup"><span data-stu-id="31ac3-139">Line-of-code breakpoints in your code</span></span>   

<span data-ttu-id="31ac3-140">Ejecuta el `debugger` método desde tu código para hacer una pausa en esa línea.</span><span class="sxs-lookup"><span data-stu-id="31ac3-140">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="31ac3-141">Es equivalente a un [punto de interrupción de línea de código](#line-of-code-breakpoints), excepto en que el punto de interrupción se establece en el código, no en la interfaz de usuario de DevTools.</span><span class="sxs-lookup"><span data-stu-id="31ac3-141">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <span data-ttu-id="31ac3-142">Puntos de interrupción de línea de código condicional</span><span class="sxs-lookup"><span data-stu-id="31ac3-142">Conditional line-of-code breakpoints</span></span>   

<span data-ttu-id="31ac3-143">Use un punto de interrupción de línea de código condicional cuando Conozca la región exacta de código que necesita investigar, pero solo desea pausarla cuando se cumpla otra condición.</span><span class="sxs-lookup"><span data-stu-id="31ac3-143">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="31ac3-144">Para establecer un punto de interrupción de línea de código condicional:</span><span class="sxs-lookup"><span data-stu-id="31ac3-144">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="31ac3-145">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="31ac3-145">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="31ac3-146">Abra el archivo que contiene la línea de código en la que desea interrumpir.</span><span class="sxs-lookup"><span data-stu-id="31ac3-146">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="31ac3-147">Ir a la línea de código.</span><span class="sxs-lookup"><span data-stu-id="31ac3-147">Go the line of code.</span></span>  
1.  <span data-ttu-id="31ac3-148">A la izquierda de la línea de código se encuentra la columna de número de línea.</span><span class="sxs-lookup"><span data-stu-id="31ac3-148">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="31ac3-149">Haga clic con el botón secundario en el número de línea.</span><span class="sxs-lookup"><span data-stu-id="31ac3-149">Right-click the line number.</span></span>  
1.  <span data-ttu-id="31ac3-150">Seleccione **Agregar punto de interrupción condicional**.</span><span class="sxs-lookup"><span data-stu-id="31ac3-150">Select **Add conditional breakpoint**.</span></span>  <span data-ttu-id="31ac3-151">Aparece un cuadro de diálogo debajo de la línea de código.</span><span class="sxs-lookup"><span data-stu-id="31ac3-151">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="31ac3-152">Escriba la condición en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="31ac3-152">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="31ac3-153">Pulse `Enter` para activar el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="31ac3-153">Press `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="31ac3-154">Un icono junto a la columna de números de línea.</span><span class="sxs-lookup"><span data-stu-id="31ac3-154">An icon next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Punto de interrupción de línea de código condicional" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       <span data-ttu-id="31ac3-156">Punto de interrupción de línea de código condicional</span><span class="sxs-lookup"><span data-stu-id="31ac3-156">A conditional line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="31ac3-157">Administrar puntos de interrupción de línea de código</span><span class="sxs-lookup"><span data-stu-id="31ac3-157">Manage line-of-code breakpoints</span></span>   

<span data-ttu-id="31ac3-158">Use el panel **puntos de interrupción** para deshabilitar o quitar puntos de interrupción de línea de código de una sola ubicación.</span><span class="sxs-lookup"><span data-stu-id="31ac3-158">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Panel puntos de interrupción" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   <span data-ttu-id="31ac3-160">Panel **puntos de interrupción**</span><span class="sxs-lookup"><span data-stu-id="31ac3-160">The **Breakpoints** panel</span></span>  
:::image-end:::  

*   <span data-ttu-id="31ac3-161">Active la casilla situada junto a una entrada para deshabilitar el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="31ac3-161">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="31ac3-162">Haga clic con el botón secundario en una entrada para quitar ese punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="31ac3-162">Right-click an entry to remove that breakpoint.</span></span>  
*   <span data-ttu-id="31ac3-163">Haga clic con el botón secundario en cualquier parte del panel **puntos de interrupción** para desactivar todos los puntos de interrupción, deshabilitar todos los puntos de interrupción o quitar todos los puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="31ac3-163">Right-click anywhere in the **Breakpoints** pane to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="31ac3-164">Deshabilitar todos los puntos de interrupción es equivalente a desactivarlo.</span><span class="sxs-lookup"><span data-stu-id="31ac3-164">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="31ac3-165">Desactivar todos los puntos de interrupción indica a DevTools que pase por alto todos los puntos de interrupción de línea de código, pero también debe mantener el estado habilitado para que cada uno esté en el mismo estado que antes cuando reactive cada uno.</span><span class="sxs-lookup"><span data-stu-id="31ac3-165">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Puntos de interrupción desactivados en el panel de puntos de interrupción" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       <span data-ttu-id="31ac3-167">Puntos de interrupción desactivados en el panel de **puntos de interrupción**</span><span class="sxs-lookup"><span data-stu-id="31ac3-167">Deactivated breakpoints in the **Breakpoints** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="31ac3-168">DOM cambiar puntos de interrupción</span><span class="sxs-lookup"><span data-stu-id="31ac3-168">DOM change breakpoints</span></span>   

<span data-ttu-id="31ac3-169">Use un punto de interrupción de cambio de DOM cuando desee pausar el código que cambia un nodo DOM o los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="31ac3-169">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="31ac3-170">Para establecer un punto de interrupción de cambio de DOM:</span><span class="sxs-lookup"><span data-stu-id="31ac3-170">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="31ac3-171">Haga clic en la pestaña **elementos** .</span><span class="sxs-lookup"><span data-stu-id="31ac3-171">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="31ac3-172">Desplazarse por el elemento en el que desea establecer el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="31ac3-172">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="31ac3-173">Haga clic con el botón secundario en el elemento.</span><span class="sxs-lookup"><span data-stu-id="31ac3-173">Right-click the element.</span></span>  
1.  <span data-ttu-id="31ac3-174">Mantenga el mouse sobre **break on**y, a continuación, seleccione **modificaciones de subárbol**, **modificaciones de atributos**o eliminación de **nodos**.</span><span class="sxs-lookup"><span data-stu-id="31ac3-174">Hover over **Break on**, then select **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Menú contextual para crear un punto de interrupción de cambio de DOM" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       <span data-ttu-id="31ac3-176">Menú contextual para crear un punto de interrupción de cambio de DOM</span><span class="sxs-lookup"><span data-stu-id="31ac3-176">The context menu for creating a DOM change breakpoint</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="31ac3-177">Tipos de puntos de interrupción de cambio de DOM</span><span class="sxs-lookup"><span data-stu-id="31ac3-177">Types of DOM change breakpoints</span></span>   

*   <span data-ttu-id="31ac3-178">**Modificaciones en el subárbol**.</span><span class="sxs-lookup"><span data-stu-id="31ac3-178">**Subtree modifications**.</span></span>  <span data-ttu-id="31ac3-179">Se desencadena cuando se quita o agrega un elemento secundario del nodo que se encuentra seleccionado, o se cambia el contenido de un elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="31ac3-179">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="31ac3-180">No se desencadena en cambios en los atributos del nodo secundario o en los cambios realizados en el nodo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="31ac3-180">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  
*   <span data-ttu-id="31ac3-181">**Modificaciones de atributos**: se desencadena cuando se agrega o se quita un atributo en el nodo seleccionado actualmente o cuando cambia un valor de atributo.</span><span class="sxs-lookup"><span data-stu-id="31ac3-181">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  
*   <span data-ttu-id="31ac3-182">**Eliminación de nodos**: se desencadena cuando se quita el nodo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="31ac3-182">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  
    
## <span data-ttu-id="31ac3-183">XHR/capturar puntos de interrupción</span><span class="sxs-lookup"><span data-stu-id="31ac3-183">XHR/Fetch breakpoints</span></span>   

<span data-ttu-id="31ac3-184">Use un punto de interrupción de XHR cuando desee interrumpir cuando la dirección URL de la solicitud de un XHR contiene una cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="31ac3-184">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="31ac3-185">DevTools se detiene en la línea de código donde el XHR ejecuta el `send()` método.</span><span class="sxs-lookup"><span data-stu-id="31ac3-185">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="31ac3-186">Esta característica también funciona con las solicitudes de [API de captura][MDNFetchApi] .</span><span class="sxs-lookup"><span data-stu-id="31ac3-186">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="31ac3-187">Un ejemplo de cuándo resulta útil es cuando ve que la página está solicitando una dirección URL incorrecta y desea buscar rápidamente los códigos de origen de AJAX o fetch que causan la solicitud incorrecta.</span><span class="sxs-lookup"><span data-stu-id="31ac3-187">One example of when this is helpful is when you see that your page is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="31ac3-188">Para establecer un punto de interrupción de XHR:</span><span class="sxs-lookup"><span data-stu-id="31ac3-188">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="31ac3-189">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="31ac3-189">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="31ac3-190">Expanda el panel de **puntos de interrupción XHR** .</span><span class="sxs-lookup"><span data-stu-id="31ac3-190">Expand the **XHR Breakpoints** pane.</span></span>  
1.  <span data-ttu-id="31ac3-191">Haga clic en **Agregar punto de interrupción**.</span><span class="sxs-lookup"><span data-stu-id="31ac3-191">Click **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="31ac3-192">Escriba la cadena en la que desea interrumpir.</span><span class="sxs-lookup"><span data-stu-id="31ac3-192">Enter the string which you want to break on.</span></span>  <span data-ttu-id="31ac3-193">DevTools se detiene cuando esta cadena está presente en cualquier lugar de una dirección URL de solicitud de XHR.</span><span class="sxs-lookup"><span data-stu-id="31ac3-193">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="31ac3-194">Pulse `Enter` para confirmar.</span><span class="sxs-lookup"><span data-stu-id="31ac3-194">Press `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Crear un punto de interrupción de XHR" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       <span data-ttu-id="31ac3-196">Crear un punto de interrupción de XHR</span><span class="sxs-lookup"><span data-stu-id="31ac3-196">Create an XHR breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="31ac3-197">Puntos de interrupción de escucha de eventos</span><span class="sxs-lookup"><span data-stu-id="31ac3-197">Event listener breakpoints</span></span> 

<span data-ttu-id="31ac3-198">Use puntos de interrupción de escucha de eventos cuando desee pausar el código del agente de escucha de eventos que se ejecuta después de desencadenar un evento.</span><span class="sxs-lookup"><span data-stu-id="31ac3-198">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="31ac3-199">Puede seleccionar eventos específicos, como `click` o categorías de eventos, como todos los eventos del mouse.</span><span class="sxs-lookup"><span data-stu-id="31ac3-199">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="31ac3-200">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="31ac3-200">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="31ac3-201">Expanda el panel de **puntos de interrupción de escucha de eventos** .</span><span class="sxs-lookup"><span data-stu-id="31ac3-201">Expand the **Event Listener Breakpoints** pane.</span></span>  <span data-ttu-id="31ac3-202">DevTools muestra una lista de categorías de eventos, como la **animación**.</span><span class="sxs-lookup"><span data-stu-id="31ac3-202">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="31ac3-203">Active una de estas categorías para pausar cada vez que se desencadene un evento de la categoría o expanda la categoría y compruebe un evento específico.</span><span class="sxs-lookup"><span data-stu-id="31ac3-203">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Crear un punto de interrupción de detector de eventos" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       <span data-ttu-id="31ac3-205">Crear un punto de interrupción de detector de eventos</span><span class="sxs-lookup"><span data-stu-id="31ac3-205">Create an event listener breakpoint</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="31ac3-206">Puntos de interrupción de excepción</span><span class="sxs-lookup"><span data-stu-id="31ac3-206">Exception breakpoints</span></span>   

<span data-ttu-id="31ac3-207">Use puntos de interrupción de excepción cuando desee hacer una pausa en la línea de código que produce una excepción detectada o no detectada.</span><span class="sxs-lookup"><span data-stu-id="31ac3-207">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="31ac3-208">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="31ac3-208">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="31ac3-209">Haga clic en **pausar en excepciones** \ ( ![ pausar en excepciones ][ImagePauseOnExceptionsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="31ac3-209">Click **Pause on exceptions** \(![Pause on exceptions][ImagePauseOnExceptionsIcon]\).</span></span>  <span data-ttu-id="31ac3-210">El icono se vuelve azul al habilitarlo.</span><span class="sxs-lookup"><span data-stu-id="31ac3-210">The icon turns blue when enabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="El botón pausar en las excepciones" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       <span data-ttu-id="31ac3-212">El botón **pausar en las excepciones**</span><span class="sxs-lookup"><span data-stu-id="31ac3-212">The **Pause on exceptions** button</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31ac3-213">**Opcional**.</span><span class="sxs-lookup"><span data-stu-id="31ac3-213">**Optional**.</span></span>  <span data-ttu-id="31ac3-214">Active la casilla **pausar las excepciones capturadas** si también desea pausar las excepciones detectadas, además de las no capturadas.</span><span class="sxs-lookup"><span data-stu-id="31ac3-214">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Pausado en una excepción no detectada" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       <span data-ttu-id="31ac3-216">Pausado en una excepción no detectada</span><span class="sxs-lookup"><span data-stu-id="31ac3-216">Paused on an uncaught exception</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="31ac3-217">Puntos de interrupción de función</span><span class="sxs-lookup"><span data-stu-id="31ac3-217">Function breakpoints</span></span>   

<span data-ttu-id="31ac3-218">Ejecute el `debug(method)` método, donde `method` es el comando, la función o el método que desea depurar, cuando desee pausarlo siempre que se ejecute una función específica.</span><span class="sxs-lookup"><span data-stu-id="31ac3-218">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="31ac3-219">Puede insertar `debug()` el código (como una `console.log()` instrucción) o ejecutar el método desde la consola de DevTools.</span><span class="sxs-lookup"><span data-stu-id="31ac3-219">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="31ac3-220">es equivalente a establecer un [punto de interrupción de línea de código](#line-of-code-breakpoints) en la primera línea de la función.</span><span class="sxs-lookup"><span data-stu-id="31ac3-220">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <span data-ttu-id="31ac3-221">Asegurarse de que la función de destino está en el ámbito</span><span class="sxs-lookup"><span data-stu-id="31ac3-221">Make sure the target function is in scope</span></span>   

<span data-ttu-id="31ac3-222">DevTools inicia una `ReferenceError` si la función que desea depurar no está en el ámbito.</span><span class="sxs-lookup"><span data-stu-id="31ac3-222">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

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

<span data-ttu-id="31ac3-223">Garantizar que la función de destino esté dentro del ámbito es complicada si está ejecutando el `debug()` método desde la consola de DevTools.</span><span class="sxs-lookup"><span data-stu-id="31ac3-223">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="31ac3-224">Esta es una estrategia:</span><span class="sxs-lookup"><span data-stu-id="31ac3-224">Here is one strategy:</span></span>  

1.  <span data-ttu-id="31ac3-225">Establezca un [punto de interrupción de línea de código](#line-of-code-breakpoints) en el lugar donde se encuentra la función en el ámbito.</span><span class="sxs-lookup"><span data-stu-id="31ac3-225">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="31ac3-226">Desencadenar el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="31ac3-226">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="31ac3-227">Ejecuta el `debug()` método en la consola de DevTools mientras el código está en pausa en el punto de interrupción de línea de código.</span><span class="sxs-lookup"><span data-stu-id="31ac3-227">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  
    
<!---  
 


-->  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft docs"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Fetch API | MDN"  

> [!NOTE]
> <span data-ttu-id="31ac3-230">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="31ac3-230">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="31ac3-231">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) y está creada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="31ac3-231">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="31ac3-233">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="31ac3-233">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

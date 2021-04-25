---
description: Obtenga información sobre todas las formas en que puede pausar el código en Microsoft Edge DevTools.
title: Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: dd865f346046cb6706e71fdb3cc869950b2b4352
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519362"
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

# <a name="how-to-pause-your-code-with-breakpoints-in-microsoft-edge-devtools"></a><span data-ttu-id="c7dfc-104">Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c7dfc-104">How to pause your code with breakpoints in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="c7dfc-105">Use puntos de interrupción para pausar el código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-105">Use breakpoints to pause your JavaScript code.</span></span>  <span data-ttu-id="c7dfc-106">En este artículo se explica cada tipo de punto de interrupción disponible en DevTools, así como cuándo usar y cómo establecer cada tipo.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-106">This article explains each type of breakpoint available in DevTools, as well as when to use and how to set each type.</span></span>

<span data-ttu-id="c7dfc-107">Para obtener un tutorial introductorio con una página web existente, vaya a Introducción a la [depuración de JavaScript en Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span><span class="sxs-lookup"><span data-stu-id="c7dfc-107">For an introductory tutorial using an existing webpage, navigate to [Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex].</span></span>

## <a name="overview-of-when-to-use-each-breakpoint-type"></a><span data-ttu-id="c7dfc-108">Información general sobre cuándo usar cada tipo de punto de interrupción</span><span class="sxs-lookup"><span data-stu-id="c7dfc-108">Overview of when to use each breakpoint type</span></span>  

<span data-ttu-id="c7dfc-109">El tipo de punto de interrupción más conocido es la línea de código.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-109">The most well-known type of breakpoint is line-of-code.</span></span>  <span data-ttu-id="c7dfc-110">Pero los puntos de interrupción de línea de código pueden ser ineficientes para establecer, especialmente si no sabe exactamente dónde buscar o si está trabajando con una base de código grande.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-110">But line-of-code breakpoints may be inefficient to set, especially if you do not know exactly where to look, or if you are working with a large codebase.</span></span>  <span data-ttu-id="c7dfc-111">Puede ahorrar tiempo al depurar al saber cómo y cuándo usar los otros tipos de puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-111">You may save yourself time when debugging by knowing how and when to use the other types of breakpoints.</span></span>  

| <span data-ttu-id="c7dfc-112">Tipo de punto de interrupción</span><span class="sxs-lookup"><span data-stu-id="c7dfc-112">Breakpoint Type</span></span> | <span data-ttu-id="c7dfc-113">Úsalo cuando quieras pausar...</span><span class="sxs-lookup"><span data-stu-id="c7dfc-113">Use This When You Want To Pause...</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="c7dfc-114">Línea de código</span><span class="sxs-lookup"><span data-stu-id="c7dfc-114">Line-of-code</span></span>](#line-of-code-breakpoints) | <span data-ttu-id="c7dfc-115">En una región exacta del código.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-115">On an exact region of code.</span></span>  |  
| [<span data-ttu-id="c7dfc-116">Línea de código condicional</span><span class="sxs-lookup"><span data-stu-id="c7dfc-116">Conditional line-of-code</span></span>](#conditional-line-of-code-breakpoints) | <span data-ttu-id="c7dfc-117">En una región exacta del código, pero solo cuando alguna otra condición es true.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-117">On an exact region of code, but only when some other condition is true.</span></span>  |  
| [<span data-ttu-id="c7dfc-118">DOM</span><span class="sxs-lookup"><span data-stu-id="c7dfc-118">DOM</span></span>](#dom-change-breakpoints) | <span data-ttu-id="c7dfc-119">En el código que cambia o quita un nodo DOM específico o los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-119">On the code that changes or removes a specific DOM node, or the children.</span></span>  |  
| [<span data-ttu-id="c7dfc-120">XHR</span><span class="sxs-lookup"><span data-stu-id="c7dfc-120">XHR</span></span>](#xhrfetch-breakpoints) | <span data-ttu-id="c7dfc-121">Cuando una dirección URL XHR contiene un patrón de cadena.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-121">When an XHR URL contains a string pattern.</span></span>  |  
| [<span data-ttu-id="c7dfc-122">Escucha de eventos</span><span class="sxs-lookup"><span data-stu-id="c7dfc-122">Event listener</span></span>](#event-listener-breakpoints) | <span data-ttu-id="c7dfc-123">En el código que se ejecuta después de que se ejecute un evento, como `click` , .</span><span class="sxs-lookup"><span data-stu-id="c7dfc-123">On the code that runs after an event, such as `click`, runs.</span></span>  |  
| [<span data-ttu-id="c7dfc-124">Excepción</span><span class="sxs-lookup"><span data-stu-id="c7dfc-124">Exception</span></span>](#exception-breakpoints) | <span data-ttu-id="c7dfc-125">En la línea de código que está generando una excepción capturada o no capturada.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-125">On the line of code that is throwing a caught or uncaught exception.</span></span>  |  
| [<span data-ttu-id="c7dfc-126">Función</span><span class="sxs-lookup"><span data-stu-id="c7dfc-126">Function</span></span>](#function-breakpoints) | <span data-ttu-id="c7dfc-127">Siempre que se ejecute un comando, una función o un método específicos.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-127">Whenever a specific command, function, or method is run.</span></span>  |  

## <a name="line-of-code-breakpoints"></a><span data-ttu-id="c7dfc-128">Puntos de interrupción de línea de código</span><span class="sxs-lookup"><span data-stu-id="c7dfc-128">Line-of-code breakpoints</span></span>  

<span data-ttu-id="c7dfc-129">Use un punto de interrupción de línea de código cuando sepa la región exacta del código que necesita investigar.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-129">Use a line-of-code breakpoint when you know the exact region of code that you need to investigate.</span></span>  <span data-ttu-id="c7dfc-130">DevTools siempre se pausa antes de que se ejecute esta línea de código.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-130">DevTools always pauses before this line of code is run.</span></span>  

<span data-ttu-id="c7dfc-131">Para establecer un punto de interrupción de línea de código en DevTools:</span><span class="sxs-lookup"><span data-stu-id="c7dfc-131">To set a line-of-code breakpoint in DevTools:</span></span>  

1.  <span data-ttu-id="c7dfc-132">Elija la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="c7dfc-132">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="c7dfc-133">Abra el archivo que contiene la línea de código en la que desea interrumpir.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-133">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="c7dfc-134">Vaya a la línea de código.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-134">Go the line of code.</span></span>  
1.  <span data-ttu-id="c7dfc-135">A la izquierda de la línea de código se encuentra la columna de número de línea.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-135">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="c7dfc-136">Elija.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-136">Choose it.</span></span>  <span data-ttu-id="c7dfc-137">Aparece un icono rojo junto a la columna de número de línea.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-137">A red icon appears next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Punto de interrupción de línea de código" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       <span data-ttu-id="c7dfc-139">Punto de interrupción de línea de código</span><span class="sxs-lookup"><span data-stu-id="c7dfc-139">A line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <a name="line-of-code-breakpoints-in-your-code"></a><span data-ttu-id="c7dfc-140">Puntos de interrupción de línea de código en el código</span><span class="sxs-lookup"><span data-stu-id="c7dfc-140">Line-of-code breakpoints in your code</span></span>  

<span data-ttu-id="c7dfc-141">Ejecute el `debugger` método desde el código para pausar en esa línea.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-141">Run the `debugger` method from your code to pause on that line.</span></span>  <span data-ttu-id="c7dfc-142">Esto equivale a un [punto de](#line-of-code-breakpoints)interrupción de línea de código , excepto que el punto de interrupción se establece en el código, no en la interfaz de usuario de DevTools.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-142">This is equivalent to a [line-of-code breakpoint](#line-of-code-breakpoints), except that the breakpoint is set in your code, not in the DevTools UI.</span></span>  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <a name="conditional-line-of-code-breakpoints"></a><span data-ttu-id="c7dfc-143">Puntos de interrupción de línea de código condicionales</span><span class="sxs-lookup"><span data-stu-id="c7dfc-143">Conditional line-of-code breakpoints</span></span>  

<span data-ttu-id="c7dfc-144">Use un punto de interrupción de línea de código condicional cuando sepa la región exacta del código que necesita investigar, pero desea pausar solo cuando se cumple alguna otra condición.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-144">Use a conditional line-of-code breakpoint when you know the exact region of code that you need to investigate, but you want to pause only when some other condition is true.</span></span>  

<span data-ttu-id="c7dfc-145">Para establecer un punto de interrupción de línea de código condicional:</span><span class="sxs-lookup"><span data-stu-id="c7dfc-145">To set a conditional line-of-code breakpoint:</span></span>  

1.  <span data-ttu-id="c7dfc-146">Elija la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="c7dfc-146">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="c7dfc-147">Abra el archivo que contiene la línea de código en la que desea interrumpir.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-147">Open the file containing the line of code on which you want to break.</span></span>  
1.  <span data-ttu-id="c7dfc-148">Vaya a la línea de código.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-148">Go the line of code.</span></span>  
1.  <span data-ttu-id="c7dfc-149">A la izquierda de la línea de código se encuentra la columna de número de línea.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-149">To the left of the line of code is the line number column.</span></span>  <span data-ttu-id="c7dfc-150">Mantenga el mouse en el número de línea y abra el menú contextual \(haga clic con el botón secundario\).</span><span class="sxs-lookup"><span data-stu-id="c7dfc-150">Hover on the line number and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="c7dfc-151">Elija **Agregar punto de interrupción condicional**.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-151">Choose **Add conditional breakpoint**.</span></span>  <span data-ttu-id="c7dfc-152">Se muestra un cuadro de diálogo debajo de la línea de código.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-152">A dialog displays underneath the line of code.</span></span>  
1.  <span data-ttu-id="c7dfc-153">Escriba la condición en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-153">Enter your condition in the dialog.</span></span>  
1.  <span data-ttu-id="c7dfc-154">Seleccione `Enter` para activar el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-154">Select `Enter` to activate the breakpoint.</span></span>  <span data-ttu-id="c7dfc-155">Icono junto a la columna de número de línea.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-155">An icon next to the line number column.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Punto de interrupción de línea de código condicional" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       <span data-ttu-id="c7dfc-157">Punto de interrupción de línea de código condicional</span><span class="sxs-lookup"><span data-stu-id="c7dfc-157">A conditional line-of-code breakpoint</span></span>  
    :::image-end:::  
    
### <a name="manage-line-of-code-breakpoints"></a><span data-ttu-id="c7dfc-158">Administrar puntos de interrupción de línea de código</span><span class="sxs-lookup"><span data-stu-id="c7dfc-158">Manage line-of-code breakpoints</span></span>  

<span data-ttu-id="c7dfc-159">Use el **panel Puntos de interrupción** para deshabilitar o quitar puntos de interrupción de línea de código de una única ubicación.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-159">Use the **Breakpoints** pane to disable or remove line-of-code breakpoints from a single location.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Panel Puntos de interrupción" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   <span data-ttu-id="c7dfc-161">Panel **Puntos de interrupción**</span><span class="sxs-lookup"><span data-stu-id="c7dfc-161">The **Breakpoints** panel</span></span>  
:::image-end:::  

*   <span data-ttu-id="c7dfc-162">Active la casilla junto a una entrada para deshabilitar ese punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-162">Check the checkbox next to an entry to disable that breakpoint.</span></span>  
*   <span data-ttu-id="c7dfc-163">Mantenga el mouse sobre una entrada y abra el menú contextual \(clic con el botón secundario\) para quitar ese punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-163">Hover on an entry and open the contextual menu \(right-click\) to remove that breakpoint.</span></span>  
*   <span data-ttu-id="c7dfc-164">Mantenga el mouse en cualquier lugar del panel **Puntos** de interrupción y abra el menú contextual \(clic con el botón secundario\) para desactivar todos los puntos de interrupción, deshabilitar todos los puntos de interrupción o quitar todos los puntos de interrupción.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-164">Hover anywhere in the **Breakpoints** pane and open the contextual menu \(right-click\) to deactivate all breakpoints, disable all breakpoints, or remove all breakpoints.</span></span>  <span data-ttu-id="c7dfc-165">Deshabilitar todos los puntos de interrupción equivale a desactivar cada uno.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-165">Disabling all breakpoints is equivalent to unchecking each one.</span></span>  <span data-ttu-id="c7dfc-166">La desactivación de todos los puntos de interrupción indica a DevTools que ignore todos los puntos de interrupción de línea de código, pero que también mantenga el estado habilitado para que cada uno esté en el mismo estado que antes al reactivar cada uno.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-166">Deactivating all breakpoints instructs DevTools to ignore all line-of-code breakpoints, but to also maintain the enabled state so that each are in the same state as before when you reactivate each one.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Puntos de interrupción desactivados en el panel Puntos de interrupción" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       <span data-ttu-id="c7dfc-168">Puntos de interrupción desactivados en el **panel Puntos de** interrupción</span><span class="sxs-lookup"><span data-stu-id="c7dfc-168">Deactivated breakpoints in the **Breakpoints** pane</span></span>  
    :::image-end:::  
    
## <a name="dom-change-breakpoints"></a><span data-ttu-id="c7dfc-169">Puntos de interrupción de cambios dom</span><span class="sxs-lookup"><span data-stu-id="c7dfc-169">DOM change breakpoints</span></span>  

<span data-ttu-id="c7dfc-170">Use un punto de interrupción de cambio dom cuando desee pausar el código que cambia un nodo DOM o los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-170">Use a DOM change breakpoint when you want to pause on the code that changes a DOM node or the children.</span></span>  

<span data-ttu-id="c7dfc-171">Para establecer un punto de interrupción de cambio dom:</span><span class="sxs-lookup"><span data-stu-id="c7dfc-171">To set a DOM change breakpoint:</span></span>  

1.  <span data-ttu-id="c7dfc-172">Elija la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-172">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="c7dfc-173">Vaya al elemento en el que desea establecer el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-173">Go the element on which you want to set the breakpoint.</span></span>  
1.  <span data-ttu-id="c7dfc-174">Mantenga el mouse en el elemento y abra el menú contextual \(clic con el botón secundario\).</span><span class="sxs-lookup"><span data-stu-id="c7dfc-174">Hover on the element and open the contextual menu \(right-click\).</span></span>  
1.  <span data-ttu-id="c7dfc-175">Mantenga el **mouse en Interrumpir ,** luego elija Modificaciones de **subárbol,** **Modificaciones de atributo**o **Eliminación de nodos.**</span><span class="sxs-lookup"><span data-stu-id="c7dfc-175">Hover on **Break on**, then choose **Subtree modifications**, **Attribute modifications**, or **Node removal**.</span></span>  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Menú contextual para crear un punto de interrupción de cambio dom" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       <span data-ttu-id="c7dfc-177">Menú contextual para crear un punto de interrupción de cambio dom</span><span class="sxs-lookup"><span data-stu-id="c7dfc-177">The context menu for creating a DOM change breakpoint</span></span>  
    :::image-end:::  
    
### <a name="types-of-dom-change-breakpoints"></a><span data-ttu-id="c7dfc-178">Tipos de puntos de interrupción de cambios dom</span><span class="sxs-lookup"><span data-stu-id="c7dfc-178">Types of DOM change breakpoints</span></span>  

*   <span data-ttu-id="c7dfc-179">**Modificaciones de subárbol**.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-179">**Subtree modifications**.</span></span>  <span data-ttu-id="c7dfc-180">Se desencadena cuando se quita o se agrega un elemento secundario del nodo seleccionado actualmente, o cuando se cambia el contenido de un elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-180">Triggered when a child of the currently-selected node is removed or added, or the contents of a child are changed.</span></span>  <span data-ttu-id="c7dfc-181">No se desencadena en los cambios de atributo de nodo secundario ni en los cambios realizados en el nodo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-181">Not triggered on child node attribute changes, or on any changes to the currently-selected node.</span></span>  
*   <span data-ttu-id="c7dfc-182">**Modificaciones de atributos:** se desencadenan cuando se agrega o quita un atributo en el nodo seleccionado actualmente, o cuando cambia un valor de atributo.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-182">**Attributes modifications**: Triggered when an attribute is added or removed on the currently-selected node, or when an attribute value changes.</span></span>  
*   <span data-ttu-id="c7dfc-183">**Eliminación de nodos:** se desencadena cuando se quita el nodo seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-183">**Node Removal**: Triggered when the currently-selected node is removed.</span></span>  
    
## <a name="xhrfetch-breakpoints"></a><span data-ttu-id="c7dfc-184">Puntos de interrupción XHR/Fetch</span><span class="sxs-lookup"><span data-stu-id="c7dfc-184">XHR/Fetch breakpoints</span></span>  

<span data-ttu-id="c7dfc-185">Use un punto de interrupción XHR cuando desee interrumpir cuando la dirección URL de solicitud de un XHR contenga una cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-185">Use an XHR breakpoint when you want to break when the request URL of an XHR contains a specified string.</span></span>  <span data-ttu-id="c7dfc-186">DevTools se detiene en la línea de código donde XHR ejecuta el `send()` método.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-186">DevTools pauses on the line of code where the XHR runs the `send()` method.</span></span>  

> [!NOTE]
> <span data-ttu-id="c7dfc-187">Esta característica también funciona con [solicitudes de API de Fetch.][MDNFetchApi]</span><span class="sxs-lookup"><span data-stu-id="c7dfc-187">This feature also works with [Fetch API][MDNFetchApi] requests.</span></span>  

<span data-ttu-id="c7dfc-188">Un ejemplo de cuándo esto es útil es cuando la página web solicita una dirección URL incorrecta y desea encontrar rápidamente el código fuente AJAX o Fetch que está provocando la solicitud incorrecta.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-188">One example of when this is helpful is when your webpage is requesting an incorrect URL, and you want to quickly find the AJAX or Fetch source code that is causing the incorrect request.</span></span>  

<span data-ttu-id="c7dfc-189">Para establecer un punto de interrupción XHR:</span><span class="sxs-lookup"><span data-stu-id="c7dfc-189">To set an XHR breakpoint:</span></span>  

1.  <span data-ttu-id="c7dfc-190">Elija la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="c7dfc-190">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="c7dfc-191">Expanda el **panel Puntos de interrupción XHR.**</span><span class="sxs-lookup"><span data-stu-id="c7dfc-191">Expand the **XHR Breakpoints** panel.</span></span>  
1.  <span data-ttu-id="c7dfc-192">Elija **Agregar punto de interrupción**.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-192">Choose **Add breakpoint**.</span></span>  
1.  <span data-ttu-id="c7dfc-193">Escriba la cadena en la que desea romper.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-193">Enter the string which you want to break on.</span></span>  <span data-ttu-id="c7dfc-194">DevTools se detiene cuando esta cadena está presente en cualquier lugar de una dirección URL de solicitud XHR.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-194">DevTools pauses when this string is present anywhere in an XHR request URL.</span></span>  
1.  <span data-ttu-id="c7dfc-195">Seleccione `Enter` para confirmar.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-195">Select `Enter` to confirm.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Crear un punto de interrupción XHR" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       <span data-ttu-id="c7dfc-197">Crear un punto de interrupción XHR</span><span class="sxs-lookup"><span data-stu-id="c7dfc-197">Create an XHR breakpoint</span></span>  
    :::image-end:::  
    
## <a name="event-listener-breakpoints"></a><span data-ttu-id="c7dfc-198">Puntos de interrupción de escucha de eventos</span><span class="sxs-lookup"><span data-stu-id="c7dfc-198">Event listener breakpoints</span></span>  

<span data-ttu-id="c7dfc-199">Use puntos de interrupción de escucha de eventos cuando desee pausar el código de escucha de eventos que se ejecuta después de que se desencadena un evento.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-199">Use event listener breakpoints when you want to pause on the event listener code that runs after an event is fired.</span></span>  <span data-ttu-id="c7dfc-200">Puede seleccionar eventos específicos, como , o `click` categorías de eventos, como todos los eventos del mouse.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-200">You are able to select specific events, such as `click`, or categories of events, such as all mouse events.</span></span>  

1.  <span data-ttu-id="c7dfc-201">Elija la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="c7dfc-201">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="c7dfc-202">Expanda el **panel Puntos de interrupción de escucha de eventos.**</span><span class="sxs-lookup"><span data-stu-id="c7dfc-202">Expand the **Event Listener Breakpoints** panel.</span></span>  <span data-ttu-id="c7dfc-203">DevTools muestra una lista de categorías de eventos, como **Animation**.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-203">DevTools shows a list of event categories, such as **Animation**.</span></span>  
1.  <span data-ttu-id="c7dfc-204">Comprueba una de estas categorías para pausar cada vez que se desencadena cualquier evento de esa categoría, o expande la categoría y comprueba un evento específico.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-204">Check one of these categories to pause whenever any event from that category is fired, or expand the category and check a specific event.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Crear un punto de interrupción de escucha de eventos" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       <span data-ttu-id="c7dfc-206">Crear un punto de interrupción de escucha de eventos</span><span class="sxs-lookup"><span data-stu-id="c7dfc-206">Create an event listener breakpoint</span></span>  
    :::image-end:::  
    
## <a name="exception-breakpoints"></a><span data-ttu-id="c7dfc-207">Puntos de interrupción de excepción</span><span class="sxs-lookup"><span data-stu-id="c7dfc-207">Exception breakpoints</span></span>  

<span data-ttu-id="c7dfc-208">Use puntos de interrupción de excepción cuando desee pausar en la línea de código que inicia una excepción capturada o no capturada.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-208">Use exception breakpoints when you want to pause on the line of code that is throwing a caught or uncaught exception.</span></span>  

1.  <span data-ttu-id="c7dfc-209">Elija la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="c7dfc-209">Choose the **Sources** tool.</span></span>  
1.  <span data-ttu-id="c7dfc-210">Elija **Pausar en excepciones** \( ![ Pausar en excepciones ](../media/pause-on-exceptions-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="c7dfc-210">Choose **Pause on exceptions** \(![Pause on exceptions](../media/pause-on-exceptions-icon.msft.png)\).</span></span>  <span data-ttu-id="c7dfc-211">El icono se vuelve azul cuando está habilitado.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-211">The icon turns blue when enabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Botón Pausar en excepciones" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       <span data-ttu-id="c7dfc-213">Botón **Pausar en excepciones**</span><span class="sxs-lookup"><span data-stu-id="c7dfc-213">The **Pause on exceptions** button</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c7dfc-214">**Opcional**.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-214">**Optional**.</span></span>  <span data-ttu-id="c7dfc-215">Active la **casilla Pausar en** excepciones capturadas si también desea pausar las excepciones capturadas, además de las no capturadas.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-215">Check the **Pause On Caught Exceptions** checkbox if you also want to pause on caught exceptions, in addition to uncaught ones.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Pausada en una excepción no detectada" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       <span data-ttu-id="c7dfc-217">Pausada en una excepción no detectada</span><span class="sxs-lookup"><span data-stu-id="c7dfc-217">Paused on an uncaught exception</span></span>  
    :::image-end:::  
    
## <a name="function-breakpoints"></a><span data-ttu-id="c7dfc-218">Puntos de interrupción de funciones</span><span class="sxs-lookup"><span data-stu-id="c7dfc-218">Function breakpoints</span></span>  

<span data-ttu-id="c7dfc-219">Ejecute el método, donde está el comando, la función o el método que desea depurar, cuando desee pausar cada vez que se ejecute `debug(method)` `method` una función específica.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-219">Run the `debug(method)` method, where `method` is the command, function, or method you want to debug, when you want to pause whenever a specific function is run.</span></span>  <span data-ttu-id="c7dfc-220">Puede insertar en `debug()` el código (como una `console.log()` instrucción) o ejecutar el método desde la consola de DevTools.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-220">You may insert `debug()` into your code (like a `console.log()` statement) or run the method from the DevTools Console.</span></span>  `debug()` <span data-ttu-id="c7dfc-221">equivale a establecer un [punto de interrupción de](#line-of-code-breakpoints) línea de código en la primera línea de la función.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-221">is equivalent to setting a [line-of-code breakpoint](#line-of-code-breakpoints) on the first line of the function.</span></span>  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <a name="make-sure-the-target-function-is-in-scope"></a><span data-ttu-id="c7dfc-222">Asegúrese de que la función de destino está en el ámbito</span><span class="sxs-lookup"><span data-stu-id="c7dfc-222">Make sure the target function is in scope</span></span>  

<span data-ttu-id="c7dfc-223">DevTools inicia un `ReferenceError` si la función que desea depurar no está en el ámbito.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-223">DevTools throws a `ReferenceError` if the function you want to debug is not in scope.</span></span>  

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

<span data-ttu-id="c7dfc-224">Asegurarse de que la función de destino está en el ámbito es complicado si está ejecutando el `debug()` método desde la consola de DevTools.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-224">Ensuring the target function is in scope is tricky if you are running the `debug()` method from the DevTools Console.</span></span>  <span data-ttu-id="c7dfc-225">Esta es una estrategia:</span><span class="sxs-lookup"><span data-stu-id="c7dfc-225">Here is one strategy:</span></span>  

1.  <span data-ttu-id="c7dfc-226">Establezca un [punto de interrupción de línea de código en](#line-of-code-breakpoints) algún lugar donde la función esté en el ámbito.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-226">Set a [line-of-code breakpoint](#line-of-code-breakpoints) somewhere where the function is in scope.</span></span>
1.  <span data-ttu-id="c7dfc-227">Desencadene el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-227">Trigger the breakpoint.</span></span>  
1.  <span data-ttu-id="c7dfc-228">Ejecute el `debug()` método en la Consola de DevTools mientras el código aún está en pausa en el punto de interrupción de línea de código.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-228">Run the `debug()` method in the DevTools Console while the code is still paused on your line-of-code breakpoint.</span></span>  
    
## <a name="related-articles"></a><span data-ttu-id="c7dfc-229">Artículos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7dfc-229">Related articles</span></span>

*   <span data-ttu-id="c7dfc-230">[Usar las características del depurador:][DevtoolsJavascriptReference] usar la interfaz de usuario del depurador en la **herramienta** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-230">[Use the debugger features][DevtoolsJavascriptReference] - Using the UI of the debugger in the **Sources** tool.</span></span>
*   <span data-ttu-id="c7dfc-231">[Introducción a la depuración de JavaScript en Microsoft Edge DevTools:][DevtoolsJavascriptIndex] un tutorial introductorio con una página web existente.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-231">[Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsJavascriptIndex] - An introductory tutorial using an existing webpage.</span></span>
*   <span data-ttu-id="c7dfc-232">[Introducción a la][DevtoolsSourcesIndex] herramienta Sources: el depurador forma parte de **la herramienta Orígenes,** que incluye un editor de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c7dfc-232">[Sources tool overview][DevtoolsSourcesIndex] - The debugger is part of the **Sources** tool, which includes a JavaScript editor.</span></span>

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="c7dfc-233">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c7dfc-233">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsJavascriptReference]: ./reference.md "Usar las características del depurador | Microsoft Docs"  

[DevtoolsJavascriptIndex]: index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft Docs"  

[DevtoolsSourcesIndex]: ../sources/index.md "Información general sobre la herramienta sources | Microsoft Docs"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Recuperación de api | MDN"  

> [!NOTE]
> <span data-ttu-id="c7dfc-238">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c7dfc-238">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c7dfc-239">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="c7dfc-239">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c7dfc-241">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c7dfc-241">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

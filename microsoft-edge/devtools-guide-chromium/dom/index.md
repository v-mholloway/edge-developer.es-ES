---
description: Cómo ver nodos, buscar nodos, editar nodos, nodos de referencia en la consola, interrumpir los cambios de nodo y mucho más.
title: Introducción a la visualización y cambio del DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 66078844730ebb22664c9ce89517511d7eb99ee7
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564290"
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
# <a name="get-started-with-viewing-and-changing-the-dom"></a><span data-ttu-id="253ee-104">Introducción a la visualización y cambio del DOM</span><span class="sxs-lookup"><span data-stu-id="253ee-104">Get started with viewing and changing the DOM</span></span>  

<span data-ttu-id="253ee-105">Complete estos tutoriales interactivos para aprender los conceptos básicos de ver y cambiar el DOM de una página mediante Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="253ee-105">Complete these interactive tutorials to learn the basics of viewing and changing the DOM of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="253ee-106">En este tutorial se supone que conoce la diferencia entre DOM y HTML.</span><span class="sxs-lookup"><span data-stu-id="253ee-106">This tutorial assumes that you know the difference between the DOM and HTML.</span></span>  <span data-ttu-id="253ee-107">Vaya a [Apéndice: HTML frente al DOM](#appendix-html-versus-the-dom) para obtener una explicación.</span><span class="sxs-lookup"><span data-stu-id="253ee-107">Navigate to [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <a name="open-dom-examples"></a><span data-ttu-id="253ee-108">Ejemplos de OPEN DOM</span><span class="sxs-lookup"><span data-stu-id="253ee-108">Open DOM examples</span></span>  

1.  <span data-ttu-id="253ee-109">Mantenga `Control` presionado \(Windows, Linux\) o `Command` \(macOS\) y elija **Ejemplos de DOM** para abrir en una pestaña nueva.</span><span class="sxs-lookup"><span data-stu-id="253ee-109">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="253ee-110">Ejemplos de DOM</span><span class="sxs-lookup"><span data-stu-id="253ee-110">DOM Examples</span></span>][GlitchDomExamples]  
    
## <a name="view-dom-nodes"></a><span data-ttu-id="253ee-111">Ver nodos DOM</span><span class="sxs-lookup"><span data-stu-id="253ee-111">View DOM nodes</span></span>  

<span data-ttu-id="253ee-112">El árbol DOM del panel Elementos es donde se hacen todas las actividades relacionadas con DOM en DevTools.</span><span class="sxs-lookup"><span data-stu-id="253ee-112">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <a name="inspect-a-node"></a><span data-ttu-id="253ee-113">Inspeccionar un nodo</span><span class="sxs-lookup"><span data-stu-id="253ee-113">Inspect a node</span></span>  

<span data-ttu-id="253ee-114">Cuando está interesado en un nodo DOM determinado, **Inspect** es una forma rápida de abrir DevTools e investigar ese nodo.</span><span class="sxs-lookup"><span data-stu-id="253ee-114">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="253ee-115">[Abra ejemplos de DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="253ee-115">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="253ee-116">En **Inspeccionar un nodo,** elija **Miguel Ángel** con el botón secundario y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="253ee-116">Under **Inspect a Node**, right-choose **Michelangelo** and choose **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       <span data-ttu-id="253ee-118">Inspeccionar un nodo</span><span class="sxs-lookup"><span data-stu-id="253ee-118">Inspect a node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="253ee-119">Se **abre** la herramienta Elementos de DevTools.</span><span class="sxs-lookup"><span data-stu-id="253ee-119">The **Elements** tool of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="253ee-120">se resalta en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="253ee-120">is highlighted in the **DOM Tree**.</span></span>  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Resaltar el nodo Miguel Ángel" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           <span data-ttu-id="253ee-122">Resaltar el `Michelangelo` nodo</span><span class="sxs-lookup"><span data-stu-id="253ee-122">Highlight the `Michelangelo` node</span></span>  
        :::image-end:::  
        
        1.  <span data-ttu-id="253ee-123">Elija el **icono Inspeccionar** \( Inspeccionar \) en la esquina superior izquierda ![ de ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="253ee-123">Choose the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) icon in the top-left corner of DevTools.</span></span>  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="El icono Inspeccionar" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               <span data-ttu-id="253ee-125">El **icono Inspeccionar**</span><span class="sxs-lookup"><span data-stu-id="253ee-125">The **Inspect** icon</span></span>  
            :::image-end:::  
            
1.  <span data-ttu-id="253ee-126">En **Inspeccionar un nodo,** elija el **texto de** Tokio.</span><span class="sxs-lookup"><span data-stu-id="253ee-126">Under **Inspect a Node**, choose the **Tokyo** text.</span></span>  <span data-ttu-id="253ee-127">Ahora, `<li>Tokyo</li>` se resalta en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="253ee-127">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="253ee-128">Inspeccionar un nodo también es el primer paso para ver y cambiar los estilos de un nodo.</span><span class="sxs-lookup"><span data-stu-id="253ee-128">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="253ee-129">Vaya a [Introducción con ver y cambiar CSS][DevToolsCssGetStarted].</span><span class="sxs-lookup"><span data-stu-id="253ee-129">Navigate to [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <a name="navigate-the-dom-tree-with-a-keyboard"></a><span data-ttu-id="253ee-130">Navegar por el árbol DOM con un teclado</span><span class="sxs-lookup"><span data-stu-id="253ee-130">Navigate the DOM Tree with a keyboard</span></span>  

<span data-ttu-id="253ee-131">Una vez que haya seleccionado un nodo en el árbol DOM, puede navegar por el árbol DOM con el teclado.</span><span class="sxs-lookup"><span data-stu-id="253ee-131">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="253ee-132">[Abra ejemplos de DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="253ee-132">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="253ee-133">En **Navegar por el árbol DOM con un teclado**, elija Anillo con el botón **derecho** y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="253ee-133">Under **Navigate the DOM Tree with a Keyboard**, right-choose **Ringo** and choose **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="253ee-134">se selecciona en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="253ee-134">is selected in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Inspeccionar el nodo Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       <span data-ttu-id="253ee-136">Inspeccionar el `Ringo` nodo</span><span class="sxs-lookup"><span data-stu-id="253ee-136">Inspect the `Ringo` node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="253ee-137">Seleccione la `Up` tecla de flecha 2 veces.</span><span class="sxs-lookup"><span data-stu-id="253ee-137">Select the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="253ee-138">.</span><span class="sxs-lookup"><span data-stu-id="253ee-138">is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Inspeccionar el nodo ul" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           <span data-ttu-id="253ee-140">Inspeccionar el `ul` nodo</span><span class="sxs-lookup"><span data-stu-id="253ee-140">Inspect the `ul` node</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="253ee-141">Seleccione la `Left` tecla de flecha.</span><span class="sxs-lookup"><span data-stu-id="253ee-141">Select the `Left` arrow key.</span></span>  <span data-ttu-id="253ee-142">La `<ul>` lista se contrae.</span><span class="sxs-lookup"><span data-stu-id="253ee-142">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="253ee-143">Vuelva a `Left` seleccionar la tecla de flecha.</span><span class="sxs-lookup"><span data-stu-id="253ee-143">Select the `Left` arrow key again.</span></span>  <span data-ttu-id="253ee-144">Se selecciona el elemento `<ul>` primario del nodo.</span><span class="sxs-lookup"><span data-stu-id="253ee-144">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="253ee-145">En este caso, es el `<div>` con el identificador `navigate-the-dom-tree-with-a-keyboard-1` .</span><span class="sxs-lookup"><span data-stu-id="253ee-145">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="253ee-146">Seleccione la tecla de flecha 2 veces para volver a seleccionar `Down` la lista que acaba de `<ul>` contraer.</span><span class="sxs-lookup"><span data-stu-id="253ee-146">Select the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="253ee-147">Debe tener el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="253ee-147">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="253ee-148">Seleccione la `Right` tecla de flecha.</span><span class="sxs-lookup"><span data-stu-id="253ee-148">Select the `Right` arrow key.</span></span>  <span data-ttu-id="253ee-149">La lista se expande.</span><span class="sxs-lookup"><span data-stu-id="253ee-149">The list expands.</span></span>  

### <a name="scroll-into-view"></a><span data-ttu-id="253ee-150">Desplazarse a la vista</span><span class="sxs-lookup"><span data-stu-id="253ee-150">Scroll into view</span></span>  

<span data-ttu-id="253ee-151">Al ver el árbol DOM, es posible que te interese un nodo DOM que no esté actualmente en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="253ee-151">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="253ee-152">Por ejemplo, supongamos que se desplazó hasta la parte inferior de la página y que le interesa el nodo situado en `<h1>` la parte superior de la página.</span><span class="sxs-lookup"><span data-stu-id="253ee-152">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="253ee-153">**Desplazarse a la** vista le permite cambiar rápidamente la posición de la ventanilla para que pueda revisar el nodo.</span><span class="sxs-lookup"><span data-stu-id="253ee-153">**Scroll into view** lets you quickly reposition the viewport so that you are able to review the node.</span></span>  

1.  <span data-ttu-id="253ee-154">[Abra ejemplos de DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="253ee-154">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="253ee-155">En **Desplazarse a la vista**, elija **Magritte con** el botón derecho y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="253ee-155">Under **Scroll into View**, right-choose **Magritte** and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="253ee-156">Desplácese hasta la parte inferior de la página Ejemplos de DOM.</span><span class="sxs-lookup"><span data-stu-id="253ee-156">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="253ee-157">El `<li>Magritte</li>` nodo todavía debe estar seleccionado en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="253ee-157">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="253ee-158">Si no es así, vuelva a [Desplazarse a la vista](#scroll-into-view) y vuelva a empezar.</span><span class="sxs-lookup"><span data-stu-id="253ee-158">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="253ee-159">Mantenga el mouse en `<li>Magritte</li>` el nodo, abra el menú contextual \(hacer clic con el botón secundario\) y elija **Desplazarse a la vista**.</span><span class="sxs-lookup"><span data-stu-id="253ee-159">Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.</span></span>  <span data-ttu-id="253ee-160">La ventanilla se desplaza hacia arriba para que pueda revisar el **nodo Magritte.**</span><span class="sxs-lookup"><span data-stu-id="253ee-160">Your viewport scrolls back up so that you may review the **Magritte** node.</span></span>  <span data-ttu-id="253ee-161">Vaya a [Apéndice: faltan opciones](#appendix-missing-options) si no puede revisar la **opción Desplazarse a la** vista.</span><span class="sxs-lookup"><span data-stu-id="253ee-161">Navigate to [Appendix: Missing options](#appendix-missing-options) if you are not able to review the **Scroll into view** option.</span></span>
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Desplazarse a la vista" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **<span data-ttu-id="253ee-163">Desplazarse a la vista</span><span class="sxs-lookup"><span data-stu-id="253ee-163">Scroll into view</span></span>**  
    :::image-end:::  

### <a name="search-for-nodes"></a><span data-ttu-id="253ee-164">Buscar nodos</span><span class="sxs-lookup"><span data-stu-id="253ee-164">Search for nodes</span></span>  

<span data-ttu-id="253ee-165">Puede buscar en el árbol DOM por cadena, selector CSS o selector XPath.</span><span class="sxs-lookup"><span data-stu-id="253ee-165">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="253ee-166">Centra el cursor en la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="253ee-166">Focus your cursor on the **Elements** tool.</span></span>  
1.  <span data-ttu-id="253ee-167">Seleccione `Control` + `F` \(Windows, Linux\) o `Command` + `F` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="253ee-167">Select `Control`+`F` \(Windows, Linux\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="253ee-168">La barra de búsqueda se abre en la parte inferior del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="253ee-168">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="253ee-169">Escriba `The Moon is a Harsh Mistress`.</span><span class="sxs-lookup"><span data-stu-id="253ee-169">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="253ee-170">La última oración se resalta en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="253ee-170">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Resaltar la consulta en la barra de búsqueda" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       <span data-ttu-id="253ee-172">Resaltar la consulta en la barra de búsqueda</span><span class="sxs-lookup"><span data-stu-id="253ee-172">Highlight the query in the Search bar</span></span>  
    :::image-end:::  
    
<span data-ttu-id="253ee-173">Como se mencionó anteriormente, la barra de búsqueda también admite selectores CSS y XPath.</span><span class="sxs-lookup"><span data-stu-id="253ee-173">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <a name="edit-the-dom"></a><span data-ttu-id="253ee-174">Editar el DOM</span><span class="sxs-lookup"><span data-stu-id="253ee-174">Edit the DOM</span></span>  

<span data-ttu-id="253ee-175">Puede editar el DOM al instante y revisar cómo afectan los cambios a la página.</span><span class="sxs-lookup"><span data-stu-id="253ee-175">You may edit the DOM on the fly and review how the changes affect the page.</span></span>  

### <a name="edit-content"></a><span data-ttu-id="253ee-176">Editar contenido</span><span class="sxs-lookup"><span data-stu-id="253ee-176">Edit content</span></span>  

<span data-ttu-id="253ee-177">Para editar el contenido de un nodo, haga doble clic en el contenido del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="253ee-177">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="253ee-178">[Abra ejemplos de DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="253ee-178">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="253ee-179">En **Editar contenido,** elija **Michelle** con el botón derecho y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="253ee-179">Under **Edit Content**, right-choose **Michelle** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="253ee-180">En el árbol DOM, haga doble clic en `Michelle` .</span><span class="sxs-lookup"><span data-stu-id="253ee-180">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="253ee-181">En otras palabras, haga doble clic en el texto entre `<li>` y `</li>` .</span><span class="sxs-lookup"><span data-stu-id="253ee-181">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="253ee-182">El texto se resalta para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="253ee-182">The text is highlighted to indicate that it is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Editar el texto" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           <span data-ttu-id="253ee-184">Editar el texto</span><span class="sxs-lookup"><span data-stu-id="253ee-184">Edit the text</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="253ee-185">Eliminar `Michelle` , escriba `Leela` y, a continuación, `Enter` seleccione para confirmar el cambio.</span><span class="sxs-lookup"><span data-stu-id="253ee-185">Delete `Michelle`, type `Leela`, then select `Enter` to confirm the change.</span></span>  <span data-ttu-id="253ee-186">El texto del DOM cambia de **Michelle** a **Leela**.</span><span class="sxs-lookup"><span data-stu-id="253ee-186">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <a name="edit-attributes"></a><span data-ttu-id="253ee-187">Editar atributos</span><span class="sxs-lookup"><span data-stu-id="253ee-187">Edit attributes</span></span>  

<span data-ttu-id="253ee-188">Para editar atributos, haga doble clic en el nombre o el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="253ee-188">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="253ee-189">Siga las instrucciones para obtener información sobre cómo agregar atributos a un nodo.</span><span class="sxs-lookup"><span data-stu-id="253ee-189">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="253ee-190">[Abra ejemplos de DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="253ee-190">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="253ee-191">En **Editar atributos**, elija Howard con el botón **derecho** y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="253ee-191">Under **Edit Attributes**, right-choose **Howard** and choose **Inspect**.</span></span>  
1.  <span data-ttu-id="253ee-192">Haga doble clic `<li>` en .</span><span class="sxs-lookup"><span data-stu-id="253ee-192">Double-click `<li>`.</span></span>  <span data-ttu-id="253ee-193">El texto se resalta para indicar que el nodo está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="253ee-193">The text is highlighted to indicate that the node is selected.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Editar el nodo" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       <span data-ttu-id="253ee-195">Editar el nodo</span><span class="sxs-lookup"><span data-stu-id="253ee-195">Edit the node</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="253ee-196">Seleccione la `Right` tecla de flecha, agregue un espacio, escriba y, a `style="background-color:gold"` continuación, seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="253ee-196">Select the `Right` arrow key, add a space, type `style="background-color:gold"`, and then select `Enter`.</span></span>  <span data-ttu-id="253ee-197">El color de fondo del nodo cambia a oro.</span><span class="sxs-lookup"><span data-stu-id="253ee-197">The background color of the node changes to gold.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Agregar un atributo style al nodo" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       <span data-ttu-id="253ee-199">Agregar un `style` atributo al nodo</span><span class="sxs-lookup"><span data-stu-id="253ee-199">Add a `style` attribute to the node</span></span>  
    :::image-end:::  
    
### <a name="edit-node-type"></a><span data-ttu-id="253ee-200">Editar tipo de nodo</span><span class="sxs-lookup"><span data-stu-id="253ee-200">Edit node type</span></span>  

<span data-ttu-id="253ee-201">Para editar el tipo de un nodo, haga doble clic en el tipo y, a continuación, escriba el nuevo tipo.</span><span class="sxs-lookup"><span data-stu-id="253ee-201">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="253ee-202">[Abra ejemplos de DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="253ee-202">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="253ee-203">En **Editar tipo de nodo**, elija Hank con el botón **secundario** y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="253ee-203">Under **Edit Node Type**, right-choose **Hank** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="253ee-204">Haga doble clic `<li>` en .</span><span class="sxs-lookup"><span data-stu-id="253ee-204">Double-click `<li>`.</span></span>  <span data-ttu-id="253ee-205">El texto `li` está resaltado.</span><span class="sxs-lookup"><span data-stu-id="253ee-205">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="253ee-206">Eliminar `li` , escribir `button` y, a continuación, seleccionar `Enter` .</span><span class="sxs-lookup"><span data-stu-id="253ee-206">Delete `li`, type `button`, then select `Enter`.</span></span>  <span data-ttu-id="253ee-207">El `<li>` nodo cambia a un `<button>` nodo.</span><span class="sxs-lookup"><span data-stu-id="253ee-207">The `<li>` node changes to a `<button>` node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Cambiar el tipo de nodo a botón" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           <span data-ttu-id="253ee-209">Cambiar el tipo de nodo a</span><span class="sxs-lookup"><span data-stu-id="253ee-209">Change the node type to</span></span> `button`  
        :::image-end:::  
        
### <a name="reorder-dom-nodes"></a><span data-ttu-id="253ee-210">Reordenar nodos DOM</span><span class="sxs-lookup"><span data-stu-id="253ee-210">Reorder DOM nodes</span></span>  

<span data-ttu-id="253ee-211">Arrastre nodos para volver a ordenarlos.</span><span class="sxs-lookup"><span data-stu-id="253ee-211">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="253ee-212">[Abra ejemplos de DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="253ee-212">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="253ee-213">En **Reordenar nodos DOM,** elija **Elvis Presley con** el botón derecho y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="253ee-213">Under **Reorder DOM Nodes**, right-choose **Elvis Presley** and choose **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="253ee-214">Es el último elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="253ee-214">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="253ee-215">En el árbol DOM, arrastre `<li>Elvis Presley</li>` hasta la parte superior de la lista.</span><span class="sxs-lookup"><span data-stu-id="253ee-215">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Arrastre el nodo a la parte superior de la lista" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           <span data-ttu-id="253ee-217">Arrastre el nodo a la parte superior de la lista</span><span class="sxs-lookup"><span data-stu-id="253ee-217">Drag the node to the top of the list</span></span>  
        :::image-end:::  
        
### <a name="force-state"></a><span data-ttu-id="253ee-218">Estado de fuerza</span><span class="sxs-lookup"><span data-stu-id="253ee-218">Force state</span></span>  

<span data-ttu-id="253ee-219">Puede forzar a los nodos a permanecer en estados como `:active` , , , y `:hover` `:focus` `:visited` `:focus-within` .</span><span class="sxs-lookup"><span data-stu-id="253ee-219">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="253ee-220">[Abra ejemplos de DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="253ee-220">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="253ee-221">En **Estado de fuerza**, mantenga el mouse en El señor de las **moscas**.</span><span class="sxs-lookup"><span data-stu-id="253ee-221">Under **Force state**, hover on **The Lord of the Flies**.</span></span>  <span data-ttu-id="253ee-222">El color de fondo se convierte en naranja.</span><span class="sxs-lookup"><span data-stu-id="253ee-222">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="253ee-223">Mantenga el **mouse en El señor de las moscas**, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="253ee-223">Hover on **The Lord of the Flies**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="253ee-224">Mantenga el `<li class="demo--hover">The Lord of the Flies</li>` mouse sobre , abra el menú contextual \(haga clic con el botón secundario\) y elija Forzar **estado**  >  **:hover**.</span><span class="sxs-lookup"><span data-stu-id="253ee-224">Hover on `<li class="demo--hover">The Lord of the Flies</li>`, open the contextual menu \(right-click\), and choose **Force State** > **:hover**.</span></span>  <span data-ttu-id="253ee-225">Vaya a [Apéndice: faltan opciones](#appendix-missing-options) si no se muestra la opción.</span><span class="sxs-lookup"><span data-stu-id="253ee-225">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  <span data-ttu-id="253ee-226">El color de fondo permanece naranja aunque no se mantenga el puntero sobre el nodo.</span><span class="sxs-lookup"><span data-stu-id="253ee-226">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <a name="hide-a-node"></a><span data-ttu-id="253ee-227">Ocultar un nodo</span><span class="sxs-lookup"><span data-stu-id="253ee-227">Hide a node</span></span>  

<span data-ttu-id="253ee-228">Seleccione `H` para ocultar un nodo.</span><span class="sxs-lookup"><span data-stu-id="253ee-228">Select `H` to hide a node.</span></span>  

1.  <span data-ttu-id="253ee-229">[Abra ejemplos de DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="253ee-229">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="253ee-230">En **Ocultar un nodo,** elija **Las estrellas mi destino y** elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="253ee-230">Under **Hide a node**, right-choose **The Stars My Destination** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="253ee-231">Seleccione la `H` clave.</span><span class="sxs-lookup"><span data-stu-id="253ee-231">Select the `H` key.</span></span>  <span data-ttu-id="253ee-232">El nodo está oculto.</span><span class="sxs-lookup"><span data-stu-id="253ee-232">The node is hidden.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Cómo es el nodo en el árbol DOM después de que esté oculto" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           <span data-ttu-id="253ee-234">Cómo es el nodo en el árbol DOM después de que esté oculto</span><span class="sxs-lookup"><span data-stu-id="253ee-234">What the node looks like in the DOM Tree after it is hidden</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="253ee-235">Vuelva a `H` seleccionar la clave.</span><span class="sxs-lookup"><span data-stu-id="253ee-235">Select the `H` key again.</span></span>  <span data-ttu-id="253ee-236">El nodo se muestra de nuevo.</span><span class="sxs-lookup"><span data-stu-id="253ee-236">The node is shown again.</span></span>  

### <a name="delete-a-node"></a><span data-ttu-id="253ee-237">Eliminar un nodo</span><span class="sxs-lookup"><span data-stu-id="253ee-237">Delete a node</span></span>  

<span data-ttu-id="253ee-238">Seleccione `Delete` para eliminar un nodo.</span><span class="sxs-lookup"><span data-stu-id="253ee-238">Select `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="253ee-239">[Abra ejemplos de DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="253ee-239">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="253ee-240">En **Eliminar un nodo,** elija **Foundation** con el botón secundario y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="253ee-240">Under **Delete a Node**, right-choose **Foundation** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="253ee-241">Seleccione la `Delete` clave.</span><span class="sxs-lookup"><span data-stu-id="253ee-241">Select the `Delete` key.</span></span>  <span data-ttu-id="253ee-242">El nodo se elimina.</span><span class="sxs-lookup"><span data-stu-id="253ee-242">The node is deleted.</span></span>  
    1.  <span data-ttu-id="253ee-243">Seleccione `Control` + `Z` \(Windows, Linux\) o `Command` + `Z` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="253ee-243">Select `Control`+`Z` \(Windows, Linux\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="253ee-244">La última acción es deshacer y el nodo vuelve a aparecer.</span><span class="sxs-lookup"><span data-stu-id="253ee-244">The last action is undone and the node reappears.</span></span>  

## <a name="access-nodes-in-the-console"></a><span data-ttu-id="253ee-245">Nodos de acceso en la consola</span><span class="sxs-lookup"><span data-stu-id="253ee-245">Access nodes in the Console</span></span>  

<span data-ttu-id="253ee-246">DevTools proporciona algunos accesos directos para obtener acceso a los nodos DOM desde la consola o para obtener referencias de JavaScript a cada uno.</span><span class="sxs-lookup"><span data-stu-id="253ee-246">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <a name="reference-the-currently-selected-node-with-0"></a><span data-ttu-id="253ee-247">Hacer referencia al nodo seleccionado actualmente con $0</span><span class="sxs-lookup"><span data-stu-id="253ee-247">Reference the currently-selected node with $0</span></span>  

<span data-ttu-id="253ee-248">Al inspeccionar un nodo, el texto junto al nodo significa que puede hacer referencia a este nodo en la `== $0` consola con la variable `$0` .</span><span class="sxs-lookup"><span data-stu-id="253ee-248">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="253ee-249">[Abra ejemplos de DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="253ee-249">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="253ee-250">En **Referencia al nodo seleccionado actualmente con $0**, elija La mano izquierda de **la** oscuridad y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="253ee-250">Under **Reference the currently-selected node with $0**, right-choose **The Left Hand of Darkness** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="253ee-251">Seleccione la `Escape` tecla para abrir el cajón de consola.</span><span class="sxs-lookup"><span data-stu-id="253ee-251">Select the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="253ee-252">Escriba `$0` y seleccione la `Enter` clave.</span><span class="sxs-lookup"><span data-stu-id="253ee-252">Type `$0` and select the `Enter` key.</span></span>  <span data-ttu-id="253ee-253">El resultado de la expresión muestra que `$0` se evalúa como `<li>The Left Hand of Darkness</li>` .</span><span class="sxs-lookup"><span data-stu-id="253ee-253">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="El resultado de la primera expresión $0 en la consola" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            <span data-ttu-id="253ee-255">El resultado de la primera `$0` expresión de la **consola**</span><span class="sxs-lookup"><span data-stu-id="253ee-255">The result of the first `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="253ee-256">Mantenga el mouse sobre el resultado.</span><span class="sxs-lookup"><span data-stu-id="253ee-256">Hover on the result.</span></span>  <span data-ttu-id="253ee-257">El nodo se resalta en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="253ee-257">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="253ee-258">Elija en el árbol DOM, escriba de nuevo en la consola y, a `<li>Dune</li>` `$0` continuación, vuelva a `Enter` seleccionar.</span><span class="sxs-lookup"><span data-stu-id="253ee-258">Choose `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then select `Enter` again.</span></span>  <span data-ttu-id="253ee-259">Ahora, `$0` se evalúa como `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="253ee-259">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="El resultado de la segunda expresión $0 en la consola" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           <span data-ttu-id="253ee-261">El resultado de la segunda `$0` expresión en la **consola**</span><span class="sxs-lookup"><span data-stu-id="253ee-261">The result of the second `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
### <a name="store-as-global-variable"></a><span data-ttu-id="253ee-262">Almacenar como variable global</span><span class="sxs-lookup"><span data-stu-id="253ee-262">Store as global variable</span></span>  

<span data-ttu-id="253ee-263">Si necesita volver a hacer referencia a un nodo muchas veces, guárdalo como una variable global.</span><span class="sxs-lookup"><span data-stu-id="253ee-263">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="253ee-264">[Abra ejemplos de DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="253ee-264">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="253ee-265">En **Almacenar como variable global**, mantenga el mouse en **El**gran reposo , abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="253ee-265">Under **Store as global variable**, hover on **The Big Sleep**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="253ee-266">Mantenga el mouse en el árbol DOM, abra el menú contextual \(hacer clic con el `<li>The Big Sleep</li>` botón secundario\) y elija Almacenar como variable **global**.</span><span class="sxs-lookup"><span data-stu-id="253ee-266">Hover on `<li>The Big Sleep</li>` in the DOM Tree, open the contextual menu \(right-click\), and choose **Store as global variable**.</span></span>  <span data-ttu-id="253ee-267">Vaya a [Apéndice: faltan opciones](#appendix-missing-options) si no se muestra la opción.</span><span class="sxs-lookup"><span data-stu-id="253ee-267">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="253ee-268">Escriba `temp1` la consola y, a continuación, seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="253ee-268">Type `temp1` in the Console and then select `Enter`.</span></span>  <span data-ttu-id="253ee-269">El resultado de la expresión muestra que la variable evalúa el nodo.</span><span class="sxs-lookup"><span data-stu-id="253ee-269">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="El resultado de la expresión temp1" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           <span data-ttu-id="253ee-271">El resultado de la `temp1` expresión</span><span class="sxs-lookup"><span data-stu-id="253ee-271">The result of the `temp1` expression</span></span>  
        :::image-end:::  
        
### <a name="copy-js-path"></a><span data-ttu-id="253ee-272">Copiar ruta de acceso DE JS</span><span class="sxs-lookup"><span data-stu-id="253ee-272">Copy JS path</span></span>  

<span data-ttu-id="253ee-273">Copie la ruta de acceso de JavaScript en un nodo cuando necesite hacer referencia a ella en una prueba automatizada.</span><span class="sxs-lookup"><span data-stu-id="253ee-273">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="253ee-274">[Abra ejemplos de DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="253ee-274">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="253ee-275">En **Copiar ruta de acceso JS**, mantenga el mouse en Los **hermanos Karamazov**, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="253ee-275">Under **Copy JS path**, hover on **The Brothers Karamazov**, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="253ee-276">Mantenga el mouse en el árbol DOM, abra el menú contextual \(hacer clic con el `<li>The Brothers Karamazov</li>` botón secundario\) y elija **Copiar**  >  **ruta js**.</span><span class="sxs-lookup"><span data-stu-id="253ee-276">Hover on `<li>The Brothers Karamazov</li>` in the DOM Tree, open the contextual menu \(right-click\), and choose **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="253ee-277">Una `document.querySelector()` expresión que se resuelve en el nodo se ha copiado en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="253ee-277">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="253ee-278">Seleccione `Control` + `V` \(Windows, Linux\) o `Command` + `V` \(macOS\) para pegar la expresión en la consola.</span><span class="sxs-lookup"><span data-stu-id="253ee-278">Select `Control`+`V` \(Windows, Linux\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="253ee-279">Seleccione `Enter` esta opción para evaluar la expresión.</span><span class="sxs-lookup"><span data-stu-id="253ee-279">Select `Enter` to evaluate the expression.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="El resultado de la expresión Copy JS Path" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           <span data-ttu-id="253ee-281">El resultado de la **expresión Copy JS Path**</span><span class="sxs-lookup"><span data-stu-id="253ee-281">The result of the **Copy JS Path** expression</span></span>  
        :::image-end:::  
        
## <a name="break-on-dom-changes"></a><span data-ttu-id="253ee-282">Interrupción de los cambios dom</span><span class="sxs-lookup"><span data-stu-id="253ee-282">Break on DOM changes</span></span>  

<span data-ttu-id="253ee-283">DevTools permite pausar el JavaScript de una página cuando JavaScript modifica el DOM.</span><span class="sxs-lookup"><span data-stu-id="253ee-283">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <a name="break-on-attribute-modifications"></a><span data-ttu-id="253ee-284">Interrupción en las modificaciones de atributos</span><span class="sxs-lookup"><span data-stu-id="253ee-284">Break on attribute modifications</span></span>  

<span data-ttu-id="253ee-285">Use puntos de interrupción de modificación de atributos cuando desee pausar JavaScript que haga que cambie cualquier atributo de un nodo.</span><span class="sxs-lookup"><span data-stu-id="253ee-285">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="253ee-286">[Abra ejemplos de DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="253ee-286">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="253ee-287">En **Interrumpir las modificaciones de atributo,** elija **Sauerkraut con el botón** derecho y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="253ee-287">Under **Break on attribute modifications**, right-choose **Sauerkraut** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="253ee-288">En el árbol DOM, mantenga el mouse sobre , abra el menú contextual \(haga clic con el `<li id="target">Sauerkraut</li>` botón secundario\) y elija Interrumpir las modificaciones **de**  >  **atributo**.</span><span class="sxs-lookup"><span data-stu-id="253ee-288">In the DOM Tree, hover on `<li id="target">Sauerkraut</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="253ee-289">Vaya a [Apéndice: faltan opciones](#appendix-missing-options) si no se muestra la opción.</span><span class="sxs-lookup"><span data-stu-id="253ee-289">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Interrupción en las modificaciones de atributos" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **<span data-ttu-id="253ee-291">Interrupción en las modificaciones de atributos</span><span class="sxs-lookup"><span data-stu-id="253ee-291">Break on attribute modifications</span></span>**  
        :::image-end:::  
        
    1.  <span data-ttu-id="253ee-292">En el siguiente paso, se le indicará que elija un botón que detenga el código de la página.</span><span class="sxs-lookup"><span data-stu-id="253ee-292">In the next step you are going to be instructed to choose a button that pauses the code of the page.</span></span>  <span data-ttu-id="253ee-293">Después de pausar la página, ya no podrá desplazarse por la página.</span><span class="sxs-lookup"><span data-stu-id="253ee-293">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="253ee-294">Debe elegir **Reanudar script** \( Reanudar script \) para que la página se pueda desplazar de ![ ](../media/resume-script-icon.msft.png) nuevo.</span><span class="sxs-lookup"><span data-stu-id="253ee-294">You must choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\) in order to make the page scrollable again.</span></span>
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Dónde reanudar la ejecución de scripts" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           <span data-ttu-id="253ee-296">Dónde reanudar la ejecución de scripts</span><span class="sxs-lookup"><span data-stu-id="253ee-296">Where to resume script running</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="253ee-297">Elija el **botón Establecer fondo** anterior.</span><span class="sxs-lookup"><span data-stu-id="253ee-297">Choose the **Set Background** button above.</span></span>  <span data-ttu-id="253ee-298">Esto establece el `style` atributo del nodo en `background-color:thistle` .</span><span class="sxs-lookup"><span data-stu-id="253ee-298">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="253ee-299">DevTools pausa la página y resalta el código que hizo que el atributo cambiara.</span><span class="sxs-lookup"><span data-stu-id="253ee-299">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="253ee-300">Elija **Resume Script** \( Resume Script ![ ](../media/resume-script-icon.msft.png) \), como se mencionó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="253ee-300">Choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\), as mentioned earlier.</span></span>  
    
### <a name="break-on-node-removal"></a><span data-ttu-id="253ee-301">Interrupción en la eliminación de nodos</span><span class="sxs-lookup"><span data-stu-id="253ee-301">Break on node removal</span></span>  

<span data-ttu-id="253ee-302">Si desea pausar cuando se quita un nodo determinado, use puntos de interrupción de eliminación de nodos.</span><span class="sxs-lookup"><span data-stu-id="253ee-302">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="253ee-303">[Abra ejemplos de DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="253ee-303">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="253ee-304">En **Interrumpir la eliminación de nodos,** elija **Neuromancer con** el botón secundario y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="253ee-304">Under **Break on Node Removal**, right-choose **Neuromancer** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="253ee-305">En el árbol DOM, mantenga el mouse sobre , abra el menú contextual \(haga clic con el botón `<li id="target">Neuromancer</li>` secundario\) y elija Interrumpir al **quitar**  >  **nodo**.</span><span class="sxs-lookup"><span data-stu-id="253ee-305">In the DOM Tree, hover on `<li id="target">Neuromancer</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="253ee-306">Vaya a [Apéndice: faltan opciones](#appendix-missing-options) si no se muestra la opción.</span><span class="sxs-lookup"><span data-stu-id="253ee-306">Navigate to [Appendix: Missing options](#appendix-missing-options) if the option is not displayed.</span></span>  
    1.  <span data-ttu-id="253ee-307">Elija el **botón Eliminar** anterior.</span><span class="sxs-lookup"><span data-stu-id="253ee-307">Choose the **Delete** button above.</span></span>  <span data-ttu-id="253ee-308">DevTools pausa la página y resalta el código que hizo que se quitara el nodo.</span><span class="sxs-lookup"><span data-stu-id="253ee-308">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="253ee-309">Elija **Reanudar script** \( Reanudar script ![ ](../media/resume-script-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="253ee-309">Choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\).</span></span>  
    
### <a name="break-on-subtree-modifications"></a><span data-ttu-id="253ee-310">Interrupción de las modificaciones del subárbol</span><span class="sxs-lookup"><span data-stu-id="253ee-310">Break on subtree modifications</span></span>  

<span data-ttu-id="253ee-311">Después de colocar un punto de interrupción de modificación de subárbol en un nodo, DevTools pausa la página cuando se agrega o quita cualquiera de los descendientes del nodo.</span><span class="sxs-lookup"><span data-stu-id="253ee-311">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="253ee-312">[Abra ejemplos de DOM](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="253ee-312">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="253ee-313">En **Interrumpir las modificaciones del subárbol,** elija A Fire Upon The **Deep** y elija **Inspect**.</span><span class="sxs-lookup"><span data-stu-id="253ee-313">Under **Break on Subtree Modifications**, right-choose **A Fire Upon The Deep** and choose **Inspect**.</span></span>  
    1.  <span data-ttu-id="253ee-314">En el árbol DOM, mantenga el mouse sobre , que es el nodo anterior , abra el menú contextual \(haga clic con el botón secundario\) y elija `<ul id="target">` `<li>A Fire Upon the Deep</li>` Interrumpir en **modificaciones**  >  **del subárbol**.</span><span class="sxs-lookup"><span data-stu-id="253ee-314">In the DOM Tree, hover on `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, open the contextual menu \(right-click\), and choose **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="253ee-315">Si no se muestra la opción, vaya a [Apéndice: Falta opciones](#appendix-missing-options).</span><span class="sxs-lookup"><span data-stu-id="253ee-315">If the option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).</span></span>  
    1.  <span data-ttu-id="253ee-316">Elija **Agregar elemento**secundario .</span><span class="sxs-lookup"><span data-stu-id="253ee-316">Choose **Add Child**.</span></span>  <span data-ttu-id="253ee-317">El código se detiene porque se `<li>` agregó un nodo a la lista.</span><span class="sxs-lookup"><span data-stu-id="253ee-317">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="253ee-318">Elija **Reanudar script** \( Reanudar script ![ ](../media/resume-script-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="253ee-318">Choose **Resume Script** \(![Resume Script](../media/resume-script-icon.msft.png)\).</span></span>  
    
## <a name="next-steps"></a><span data-ttu-id="253ee-319">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="253ee-319">Next steps</span></span>  

<span data-ttu-id="253ee-320">Eso cubre la mayoría de las características relacionadas con DOM en DevTools.</span><span class="sxs-lookup"><span data-stu-id="253ee-320">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="253ee-321">Para descubrir el resto de las características, mantenga el mouse en los nodos del árbol DOM, abra el menú contextual \(haga clic con el botón secundario\) y experimente con las otras opciones que no se han cubierto en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="253ee-321">You are able to discover the rest of the features by hovering on nodes in the DOM Tree, opening the contextual menu \(right-click\), and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="253ee-322">Vaya a [Métodos abreviados de teclado del panel Elementos][DevToolsShortcutsElements].</span><span class="sxs-lookup"><span data-stu-id="253ee-322">Navigate to [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="253ee-323">Echa un vistazo a Microsoft Edge página principal [de DevTools][MicrosoftEdgeDevTools] para descubrir todo lo que puedes hacer con DevTools.</span><span class="sxs-lookup"><span data-stu-id="253ee-323">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--Navigate to [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## <a name="appendix-html-versus-the-dom"></a><span data-ttu-id="253ee-324">Apéndice: HTML frente al DOM</span><span class="sxs-lookup"><span data-stu-id="253ee-324">Appendix: HTML versus the DOM</span></span>  

<span data-ttu-id="253ee-325">En la siguiente sección se explica rápidamente la diferencia entre HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="253ee-325">The following section quickly explains the difference between HTML and the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="253ee-326">Cuando se usa un explorador web para solicitar una página, el servidor devuelve HTML como el siguiente fragmento de código</span><span class="sxs-lookup"><span data-stu-id="253ee-326">When you use a web browser to request a page, the server returns HTML like the following code snippet</span></span>  

      ```html
      <!doctype html>
      <html>
          <head>
              <title>Hello, world!</title>
          </head>
          <body>
              <h1>Hello, world!</h1>
              <p>This is a hypertext document on the World Wide Web.</p>
              <script src="/script.js" async></script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="253ee-327">El explorador analiza el HTML y crea un árbol de objetos como la siguiente lista.</span><span class="sxs-lookup"><span data-stu-id="253ee-327">The browser parses the HTML and creates a tree of objects like the following list.</span></span>  
      
      ```dom
      html
          head
              title
          body
              h1
              p
              script
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="253ee-328">Este árbol de objetos o nodos que representa el contenido de la página se denomina DOM.</span><span class="sxs-lookup"><span data-stu-id="253ee-328">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="253ee-329">Ahora mismo tiene el mismo aspecto que el HTML, pero supongamos que el script al que se hace referencia en la parte inferior del HTML ejecuta el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="253ee-329">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs the following code snippet.</span></span>  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="253ee-330">Ese código quita el `h1` nodo y agrega otro nodo al `p` DOM.</span><span class="sxs-lookup"><span data-stu-id="253ee-330">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="253ee-331">El DOM completo ahora muestra la siguiente lista.</span><span class="sxs-lookup"><span data-stu-id="253ee-331">The complete DOM now displays the following list.</span></span>  
      
      ```dom
      html
          head
              title
          body
              p
              script
              p
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="253ee-332">El CÓDIGO HTML de la página ahora es diferente del DOM.</span><span class="sxs-lookup"><span data-stu-id="253ee-332">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="253ee-333">En otras palabras, HTML representa el contenido inicial de la página y el DOM representa el contenido actual de la página.</span><span class="sxs-lookup"><span data-stu-id="253ee-333">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="253ee-334">Cuando JavaScript agrega, quita o edita nodos, el DOM se convierte en diferente que el HTML.</span><span class="sxs-lookup"><span data-stu-id="253ee-334">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="253ee-335">Vaya a [Introducción al DOM][MDNIntroductionToDOM] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="253ee-335">Navigate to [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.  Your viewport scrolls back up so that the **Magritte** node is displayed.  If you the **Scroll into view** option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## <a name="appendix-missing-options"></a><span data-ttu-id="253ee-336">Apéndice: Faltan opciones</span><span class="sxs-lookup"><span data-stu-id="253ee-336">Appendix: Missing options</span></span>  

<span data-ttu-id="253ee-337">Muchas de las instrucciones de este tutorial le indican que mantenga el mouse en un nodo del árbol DOM, abra el menú contextual \(hacer clic con el botón secundario\) y, a continuación, elija una opción en el menú contextual que aparece.</span><span class="sxs-lookup"><span data-stu-id="253ee-337">Many of the instructions in this tutorial instruct you to hover on a node in the DOM Tree, open the contextual menu \(right-click\), and then choose an option from the context menu that pops up.</span></span>  <span data-ttu-id="253ee-338">Si no se muestra la opción especificada en el menú contextual, intente alejarse del texto del nodo y abrir el menú contextual \(hacer clic con el botón secundario\).</span><span class="sxs-lookup"><span data-stu-id="253ee-338">If the specified option in the context menu is not displayed, try hovering away from the node text and opening the contextual menu \(right-click\).</span></span>  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Dónde elegir si no se muestran todas las opciones" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   <span data-ttu-id="253ee-340">Dónde elegir si no se muestran todas las opciones</span><span class="sxs-lookup"><span data-stu-id="253ee-340">Where to choose if all of the options are not displayed</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="253ee-341">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="253ee-341">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge \(Chromium\) Developer Tools | Microsoft Docs"  
[DevToolsCssGetStarted]: ../css/index.md "Introducción Con vista y cambio de CSS | Microsoft Docs"  
[DevToolsShortcutsElements]: ../shortcuts/index.md#elements-tool-keyboard-shortcuts "Métodos abreviados de teclado de la herramienta Elements: Microsoft Edge métodos abreviados de teclado de DevTools | Microsoft Docs"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Microsoft Edge (Chromium) DevTools DOM Ejemplo | Glitch"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introducción al dom | MDN"  

> [!NOTE]
> <span data-ttu-id="253ee-347">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="253ee-347">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="253ee-348">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/dom/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="253ee-348">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="253ee-350">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="253ee-350">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

---
title: Introducción a la visualización y el cambio de DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 6d41b072a8bd19ae728cc02b43eb2f843d91b332
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991207"
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





# <span data-ttu-id="e5ed8-103">Introducción a la visualización y el cambio de DOM</span><span class="sxs-lookup"><span data-stu-id="e5ed8-103">Get started with viewing and changing the DOM</span></span>   



<span data-ttu-id="e5ed8-104">Complete estos tutoriales interactivos para obtener información básica sobre cómo ver y cambiar el DOM de una página con Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-104">Complete these interactive tutorials to learn the basics of viewing and changing the DOM of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="e5ed8-105">En este tutorial se supone que conoce la diferencia entre DOM y HTML.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-105">This tutorial assumes that you know the difference between the DOM and HTML.</span></span>  <span data-ttu-id="e5ed8-106">Consulta [el apéndice: HTML en comparación con Dom](#appendix-html-versus-the-dom) para obtener una explicación.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-106">See [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <span data-ttu-id="e5ed8-107">Ejemplos de Open DOM</span><span class="sxs-lookup"><span data-stu-id="e5ed8-107">Open DOM examples</span></span>  

1.  <span data-ttu-id="e5ed8-108">Mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y haga clic en **ejemplos de Dom** para abrir en una nueva pestaña.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-108">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="e5ed8-109">Ejemplos de DOM</span><span class="sxs-lookup"><span data-stu-id="e5ed8-109">DOM Examples</span></span>][GlitchDomExamples]  
    
## <span data-ttu-id="e5ed8-110">Ver nodos DOM</span><span class="sxs-lookup"><span data-stu-id="e5ed8-110">View DOM nodes</span></span>   

<span data-ttu-id="e5ed8-111">El árbol DOM del panel elementos es el lugar donde se realizan todas las actividades relacionadas con DOM en DevTools.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-111">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <span data-ttu-id="e5ed8-112">Inspeccionar un nodo</span><span class="sxs-lookup"><span data-stu-id="e5ed8-112">Inspect a node</span></span>   

<span data-ttu-id="e5ed8-113">Cuando esté interesado en un nodo DOM determinado, **inspeccionar** es una forma rápida de abrir DevTools e investigar ese nodo.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-113">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="e5ed8-114">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-114">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="e5ed8-115">En **inspeccionar un nodo**, haga clic con el botón derecho en **Michelangelo** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-115">Under **Inspect a Node**, right-click **Michelangelo** and select **Inspect**.</span></span>  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       <span data-ttu-id="e5ed8-117">Inspeccionar un nodo</span><span class="sxs-lookup"><span data-stu-id="e5ed8-117">Inspect a node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="e5ed8-118">Se abre el panel **elementos** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-118">The **Elements** panel of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="e5ed8-119">está resaltado en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-119">is highlighted in the **DOM Tree**.</span></span>  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Resalte el nodo Michelangelo" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           <span data-ttu-id="e5ed8-121">Resaltar el `Michelangelo` nodo</span><span class="sxs-lookup"><span data-stu-id="e5ed8-121">Highlight the `Michelangelo` node</span></span>  
        :::image-end:::  
        
        1.  <span data-ttu-id="e5ed8-122">Haga clic en el icono de **inspeccionar** \ ( ![ inspeccionar ][ImageInspectIcon] \) en la esquina superior izquierda de DevTools.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-122">Click the **Inspect** \(![Inspect][ImageInspectIcon]\) icon in the top-left corner of DevTools.</span></span>  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Icono de inspección" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               <span data-ttu-id="e5ed8-124">Icono de **inspección**</span><span class="sxs-lookup"><span data-stu-id="e5ed8-124">The **Inspect** icon</span></span>  
            :::image-end:::  
            
1.  <span data-ttu-id="e5ed8-125">En **inspeccionar un nodo**, haga clic en el texto de **Tokio** .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-125">Under **Inspect a Node**, click the **Tokyo** text.</span></span>  <span data-ttu-id="e5ed8-126">Ahora, `<li>Tokyo</li>` está resaltado en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-126">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="e5ed8-127">Inspeccionar un nodo también es el primer paso para ver y cambiar los estilos de un nodo.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-127">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="e5ed8-128">Consulte Introducción [a la visualización y el cambio de CSS][DevToolsCssGetStarted].</span><span class="sxs-lookup"><span data-stu-id="e5ed8-128">See [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <span data-ttu-id="e5ed8-129">Navegar por el árbol DOM con un teclado</span><span class="sxs-lookup"><span data-stu-id="e5ed8-129">Navigate the DOM Tree with a keyboard</span></span>   

<span data-ttu-id="e5ed8-130">Una vez que haya seleccionado un nodo en el árbol DOM, puede desplazarse por el árbol DOM con el teclado.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-130">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="e5ed8-131">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-131">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="e5ed8-132">En **navegar por el árbol DOM con un teclado**, haga clic con el botón derecho en **Ringo** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-132">Under **Navigate the DOM Tree with a Keyboard**, right-click **Ringo** and select **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="e5ed8-133">está seleccionado en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-133">is selected in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Inspeccionar el nodo Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       <span data-ttu-id="e5ed8-135">Inspeccionar el `Ringo` nodo</span><span class="sxs-lookup"><span data-stu-id="e5ed8-135">Inspect the `Ringo` node</span></span>  
    :::image-end:::  
    
    1.  <span data-ttu-id="e5ed8-136">Presione la `Up` tecla de dirección dos veces.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-136">Press the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="e5ed8-137">.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-137">is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Inspeccionar el nodo UL" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           <span data-ttu-id="e5ed8-139">Inspeccionar el `ul` nodo</span><span class="sxs-lookup"><span data-stu-id="e5ed8-139">Inspect the `ul` node</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="e5ed8-140">Presione la `Left` tecla de dirección.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-140">Press the `Left` arrow key.</span></span>  <span data-ttu-id="e5ed8-141">La `<ul>` lista se contraerá.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-141">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="e5ed8-142">`Left`Vuelva a presionar la tecla de dirección.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-142">Press the `Left` arrow key again.</span></span>  <span data-ttu-id="e5ed8-143">Se selecciona el elemento primario del `<ul>` nodo.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-143">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="e5ed8-144">En este caso, es el `<div>` con el identificador `navigate-the-dom-tree-with-a-keyboard-1` .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-144">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="e5ed8-145">Presione la `Down` tecla de dirección dos veces para que se vuelva a seleccionar la `<ul>` lista que acaba de contraer.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-145">Press the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="e5ed8-146">Debe tener el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="e5ed8-146">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="e5ed8-147">Presione la `Right` tecla de dirección.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-147">Press the `Right` arrow key.</span></span>  <span data-ttu-id="e5ed8-148">Se expande la lista.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-148">The list expands.</span></span>  

### <span data-ttu-id="e5ed8-149">Desplazarse en la vista</span><span class="sxs-lookup"><span data-stu-id="e5ed8-149">Scroll into view</span></span>   

<span data-ttu-id="e5ed8-150">Al ver el árbol DOM, es posible que te encuentres interesado en un nodo DOM que actualmente no está en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-150">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="e5ed8-151">Por ejemplo, supongamos que se ha desplazado a la parte inferior de la página y está interesado en el `<h1>` nodo de la parte superior de la página.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-151">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="e5ed8-152">**Desplazarse hacia la vista** le permite cambiar rápidamente la posición de la ventanilla para poder ver el nodo.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-152">**Scroll into view** lets you quickly reposition the viewport so that you are able to see the node.</span></span>  

1.  <span data-ttu-id="e5ed8-153">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-153">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="e5ed8-154">En **desplazarse hacia la vista**, haga clic con el botón derecho en **Magritte** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-154">Under **Scroll into View**, right-click **Magritte** and select **Inspect**.</span></span>  
1.  <span data-ttu-id="e5ed8-155">Desplácese hasta la parte inferior de la página de ejemplos de DOM.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-155">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="e5ed8-156">El `<li>Magritte</li>` nodo debe seguir estando seleccionado en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-156">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="e5ed8-157">Si no es así, vuelva a [desplazarse](#scroll-into-view) hacia la vista y volver a empezar.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-157">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="e5ed8-158">Haga clic con el botón derecho en el `<li>Magritte</li>` nodo y seleccione **desplazarse a la vista**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-158">Right-click the `<li>Magritte</li>` node and select **Scroll into view**.</span></span>  <span data-ttu-id="e5ed8-159">Su ventanilla se desplaza hacia arriba para que pueda ver el nodo **Magritte** .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-159">Your viewport scrolls back up so that you may see the **Magritte** node.</span></span>  <span data-ttu-id="e5ed8-160">Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no puede ver la opción **desplazarse a la vista** .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-160">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.</span></span>
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Desplazarse en la vista" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **<span data-ttu-id="e5ed8-162">Desplazarse en la vista</span><span class="sxs-lookup"><span data-stu-id="e5ed8-162">Scroll into view</span></span>**  
    :::image-end:::  

### <span data-ttu-id="e5ed8-163">Buscar nodos</span><span class="sxs-lookup"><span data-stu-id="e5ed8-163">Search for nodes</span></span>   

<span data-ttu-id="e5ed8-164">Puede buscar en el árbol DOM por cadena, selector de CSS o selector XPath.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-164">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="e5ed8-165">Centre el cursor en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-165">Focus your cursor on the **Elements** panel.</span></span>  
1.  <span data-ttu-id="e5ed8-166">Pulse `Control` + `F` \ (Windows \) o `Command` + `F` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-166">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="e5ed8-167">La barra de búsqueda se abre en la parte inferior del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-167">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="e5ed8-168">Escribe `The Moon is a Harsh Mistress`.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-168">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="e5ed8-169">La última oración se resalta en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-169">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Resaltar la consulta en la barra de búsqueda" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       <span data-ttu-id="e5ed8-171">Resaltar la consulta en la barra de búsqueda</span><span class="sxs-lookup"><span data-stu-id="e5ed8-171">Highlight the query in the Search bar</span></span>  
    :::image-end:::  
    
<span data-ttu-id="e5ed8-172">Como se mencionó anteriormente, la barra de búsqueda también admite los selectores CSS y CSS.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-172">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <span data-ttu-id="e5ed8-173">Editar el DOM</span><span class="sxs-lookup"><span data-stu-id="e5ed8-173">Edit the DOM</span></span>   

<span data-ttu-id="e5ed8-174">Puede editar el DOM sobre la marcha y ver cómo afectan esos cambios a la página.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-174">You may edit the DOM on the fly and see how those changes affect the page.</span></span>  

### <span data-ttu-id="e5ed8-175">Editar contenido</span><span class="sxs-lookup"><span data-stu-id="e5ed8-175">Edit content</span></span>   

<span data-ttu-id="e5ed8-176">Para editar el contenido de un nodo, haga doble clic en el contenido del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-176">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="e5ed8-177">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-177">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="e5ed8-178">En **editar contenido**, haga clic con el botón derecho en **Michelle** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-178">Under **Edit Content**, right-click **Michelle** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="e5ed8-179">En el árbol DOM, haga doble clic `Michelle` .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-179">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="e5ed8-180">En otras palabras, haga doble clic en el texto entre `<li>` y `</li>` .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-180">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="e5ed8-181">El texto se resalta para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-181">The text is highlighted to indicate that it is selected.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Editar el texto" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           <span data-ttu-id="e5ed8-183">Editar el texto</span><span class="sxs-lookup"><span data-stu-id="e5ed8-183">Edit the text</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="e5ed8-184">Eliminar `Michelle` , escriba `Leela` y, a continuación, pulse `Enter` para confirmar el cambio.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-184">Delete `Michelle`, type `Leela`, then press `Enter` to confirm the change.</span></span>  <span data-ttu-id="e5ed8-185">El texto del DOM cambia de **Michelle** a **Leela**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-185">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <span data-ttu-id="e5ed8-186">Editar atributos</span><span class="sxs-lookup"><span data-stu-id="e5ed8-186">Edit attributes</span></span>   

<span data-ttu-id="e5ed8-187">Para editar atributos, haga doble clic en el nombre o valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-187">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="e5ed8-188">Siga las instrucciones para obtener información sobre cómo agregar atributos a un nodo.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-188">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="e5ed8-189">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-189">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="e5ed8-190">En **Editar atributos**, haga clic con el botón derecho en **Howard** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-190">Under **Edit Attributes**, right-click **Howard** and select **Inspect**.</span></span>  
1.  <span data-ttu-id="e5ed8-191">Haga doble clic `<li>` .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-191">Double-click `<li>`.</span></span>  <span data-ttu-id="e5ed8-192">El texto se resalta para indicar que el nodo está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-192">The text is highlighted to indicate that the node is selected.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Editar el nodo" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       <span data-ttu-id="e5ed8-194">Editar el nodo</span><span class="sxs-lookup"><span data-stu-id="e5ed8-194">Edit the node</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e5ed8-195">Presione la `Right` tecla de dirección, agregue un espacio, escriba `style="background-color:gold"` y, a continuación, presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-195">Press the `Right` arrow key, add a space, type `style="background-color:gold"`, and then press `Enter`.</span></span>  <span data-ttu-id="e5ed8-196">El color de fondo del nodo cambia a oro.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-196">The background color of the node changes to gold.</span></span>  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Agregar un atributo de estilo al nodo" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       <span data-ttu-id="e5ed8-198">Agregar un `style` atributo al nodo</span><span class="sxs-lookup"><span data-stu-id="e5ed8-198">Add a `style` attribute to the node</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="e5ed8-199">Editar tipo de nodo</span><span class="sxs-lookup"><span data-stu-id="e5ed8-199">Edit node type</span></span>   

<span data-ttu-id="e5ed8-200">Para editar el tipo de un nodo, haga doble clic en el tipo y, a continuación, escriba el nuevo tipo.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-200">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="e5ed8-201">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-201">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="e5ed8-202">En **Editar tipo de nodo**, haga clic con el botón derecho en **Hank** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-202">Under **Edit Node Type**, right-click **Hank** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="e5ed8-203">Haga doble clic `<li>` .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-203">Double-click `<li>`.</span></span>  <span data-ttu-id="e5ed8-204">`li`Se resalta el texto.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-204">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="e5ed8-205">Eliminar `li` , escriba `button` y, a continuación, pulse `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-205">Delete `li`, type `button`, then press `Enter`.</span></span>  <span data-ttu-id="e5ed8-206">El `<li>` nodo cambia a un `<button>` nodo.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-206">The `<li>` node changes to a `<button>` node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Cambiar el tipo de nodo a botón" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           <span data-ttu-id="e5ed8-208">Cambiar el tipo de nodo a</span><span class="sxs-lookup"><span data-stu-id="e5ed8-208">Change the node type to</span></span> `button`  
        :::image-end:::  
        
### <span data-ttu-id="e5ed8-209">Reordenar los nodos DOM</span><span class="sxs-lookup"><span data-stu-id="e5ed8-209">Reorder DOM nodes</span></span>   

<span data-ttu-id="e5ed8-210">Arrastre los nodos para reordenarlos.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-210">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="e5ed8-211">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-211">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="e5ed8-212">En **Reordenar los nodos DOM**, haga clic con el botón derecho en **Elvis Presley** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-212">Under **Reorder DOM Nodes**, right-click **Elvis Presley** and select **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e5ed8-213">Es el último elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-213">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="e5ed8-214">En el árbol DOM, arrastre `<li>Elvis Presley</li>` hasta la parte superior de la lista.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-214">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Arrastre el nodo a la parte superior de la lista" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           <span data-ttu-id="e5ed8-216">Arrastre el nodo a la parte superior de la lista</span><span class="sxs-lookup"><span data-stu-id="e5ed8-216">Drag the node to the top of the list</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="e5ed8-217">Estado de fuerza</span><span class="sxs-lookup"><span data-stu-id="e5ed8-217">Force state</span></span>   

<span data-ttu-id="e5ed8-218">Puede obligar a que los nodos permanezcan en Estados incluidos `:active` ,, `:hover` `:focus` , `:visited` y `:focus-within` .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-218">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="e5ed8-219">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-219">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="e5ed8-220">En **Estado de fuerza**, desplace el puntero sobre **el Señor de la vuela**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-220">Under **Force state**, hover over **The Lord of the Flies**.</span></span>  <span data-ttu-id="e5ed8-221">El color de fondo se convierte en naranja.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-221">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="e5ed8-222">Haga clic con el botón derecho en **el Señor de la vuela** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-222">Right-click **The Lord of the Flies** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="e5ed8-223">Haga clic con el botón derecho `<li class="demo--hover">The Lord of the Flies</li>` y seleccione **Estado de fuerza**  >  **: mantener**el mouse.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-223">Right-click `<li class="demo--hover">The Lord of the Flies</li>` and select **Force State** > **:hover**.</span></span>  <span data-ttu-id="e5ed8-224">Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no ve esta opción.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-224">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  <span data-ttu-id="e5ed8-225">El color de fondo sigue siendo naranja aunque no se esté colocando el puntero sobre el nodo.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-225">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <span data-ttu-id="e5ed8-226">Ocultar un nodo</span><span class="sxs-lookup"><span data-stu-id="e5ed8-226">Hide a node</span></span>   

<span data-ttu-id="e5ed8-227">Pulse `H` para ocultar un nodo.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-227">Press `H` to hide a node.</span></span>  

1.  <span data-ttu-id="e5ed8-228">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-228">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="e5ed8-229">En **ocultar un nodo**, haga clic con el botón derecho en **las estrellas mi destino** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-229">Under **Hide a node**, right-click **The Stars My Destination** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="e5ed8-230">Presione la `H` tecla.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-230">Press the `H` key.</span></span>  <span data-ttu-id="e5ed8-231">El nodo está oculto.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-231">The node is hidden.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="El aspecto del nodo en el árbol DOM después de ocultarlo" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           <span data-ttu-id="e5ed8-233">El aspecto del nodo en el árbol DOM después de ocultarlo</span><span class="sxs-lookup"><span data-stu-id="e5ed8-233">What the node looks like in the DOM Tree after it is hidden</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="e5ed8-234">`H`Vuelva a presionar la tecla.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-234">Press the `H` key again.</span></span>  <span data-ttu-id="e5ed8-235">Se vuelve a mostrar el nodo.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-235">The node is shown again.</span></span>  

### <span data-ttu-id="e5ed8-236">Eliminar un nodo</span><span class="sxs-lookup"><span data-stu-id="e5ed8-236">Delete a node</span></span>   

<span data-ttu-id="e5ed8-237">Pulse `Delete` para eliminar un nodo.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-237">Press `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="e5ed8-238">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-238">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="e5ed8-239">En **eliminar un nodo**, haga clic con el botón derecho en **Foundation** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-239">Under **Delete a Node**, right-click **Foundation** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="e5ed8-240">Presione la `Delete` tecla.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-240">Press the `Delete` key.</span></span>  <span data-ttu-id="e5ed8-241">Se elimina el nodo.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-241">The node is deleted.</span></span>  
    1.  <span data-ttu-id="e5ed8-242">Pulse `Control` + `Z` \ (Windows \) o `Command` + `Z` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-242">Press `Control`+`Z` \(Windows\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="e5ed8-243">La última acción se deshará y el nodo reaparecerá.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-243">The last action is undone and the node reappears.</span></span>  

## <span data-ttu-id="e5ed8-244">Nodos de acceso en la consola</span><span class="sxs-lookup"><span data-stu-id="e5ed8-244">Access nodes in the Console</span></span>   

<span data-ttu-id="e5ed8-245">DevTools proporciona algunos métodos abreviados para acceder a los nodos DOM desde la consola o para obtener referencias de JavaScript a cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-245">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <span data-ttu-id="e5ed8-246">Hacer referencia al nodo actualmente seleccionado con $0</span><span class="sxs-lookup"><span data-stu-id="e5ed8-246">Reference the currently-selected node with $0</span></span>   

<span data-ttu-id="e5ed8-247">Al inspeccionar un nodo, el `== $0` texto que se encuentra junto al nodo significa que puede hacer referencia a este nodo en la consola con la variable `$0` .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-247">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="e5ed8-248">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-248">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="e5ed8-249">En **referencia el nodo seleccionado actualmente con $0**, haga clic con el botón derecho en **el lado izquierdo de la oscuridad** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-249">Under **Reference the currently-selected node with $0**, right-click **The Left Hand of Darkness** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="e5ed8-250">Presione la `Escape` tecla para abrir el cajón de consola.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-250">Press the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="e5ed8-251">Escriba `$0` y presione la `Enter` tecla.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-251">Type `$0` and press the `Enter` key.</span></span>  <span data-ttu-id="e5ed8-252">El resultado de la expresión muestra que `$0` se evalúa `<li>The Left Hand of Darkness</li>` .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-252">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="El resultado de la primera expresión $0 en la consola" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            <span data-ttu-id="e5ed8-254">El resultado de la primera `$0` expresión en la **consola**</span><span class="sxs-lookup"><span data-stu-id="e5ed8-254">The result of the first `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="e5ed8-255">Desplace el puntero sobre el resultado.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-255">Hover over the result.</span></span>  <span data-ttu-id="e5ed8-256">El nodo se resalta en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-256">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="e5ed8-257">Haga clic `<li>Dune</li>` en el árbol DOM, escriba `$0` la consola de nuevo y, a continuación, vuelva a presionar `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-257">Click `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then press `Enter` again.</span></span>  <span data-ttu-id="e5ed8-258">Ahora, `$0` evalúa a `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-258">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="El resultado de la segunda expresión $0 en la consola" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           <span data-ttu-id="e5ed8-260">Resultado de la segunda `$0` expresión en la **consola**</span><span class="sxs-lookup"><span data-stu-id="e5ed8-260">The result of the second `$0` expression in the **Console**</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="e5ed8-261">Almacenar como variable global</span><span class="sxs-lookup"><span data-stu-id="e5ed8-261">Store as global variable</span></span>   

<span data-ttu-id="e5ed8-262">Si necesita hacer referencia a un nodo varias veces, almacénelo como una variable global.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-262">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="e5ed8-263">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-263">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="e5ed8-264">En **almacenar como variable global**, haga clic con el botón secundario en **el gran sueño** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-264">Under **Store as global variable**, right-click **The Big Sleep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="e5ed8-265">Haga clic con el botón derecho `<li>The Big Sleep</li>` en el árbol DOM y seleccione **almacenar como variable global**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-265">Right-click `<li>The Big Sleep</li>` in the DOM Tree and select **Store as global variable**.</span></span>  <span data-ttu-id="e5ed8-266">Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no ve esta opción.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-266">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  
    1.  <span data-ttu-id="e5ed8-267">Escriba `temp1` la consola y, a continuación, pulse `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-267">Type `temp1` in the Console and then press `Enter`.</span></span>  <span data-ttu-id="e5ed8-268">El resultado de la expresión muestra que la variable se evalúa en el nodo.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-268">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="El resultado de la expresión temp1" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           <span data-ttu-id="e5ed8-270">El resultado de la `temp1` expresión</span><span class="sxs-lookup"><span data-stu-id="e5ed8-270">The result of the `temp1` expression</span></span>  
        :::image-end:::  
        
### <span data-ttu-id="e5ed8-271">Copiar ruta JS</span><span class="sxs-lookup"><span data-stu-id="e5ed8-271">Copy JS path</span></span>   

<span data-ttu-id="e5ed8-272">Copie la ruta de acceso de JavaScript en un nodo cuando necesite hacer referencia a él en una prueba automatizada.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-272">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="e5ed8-273">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-273">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="e5ed8-274">En **copiar JS path**, haga clic con el botón secundario en **el Karamazov de Brothers** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-274">Under **Copy JS path**, right-click **The Brothers Karamazov** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="e5ed8-275">Haga clic con el botón derecho `<li>The Brothers Karamazov</li>` en el árbol DOM y seleccione **copiar**  >  **copia JS ruta**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-275">Right-click `<li>The Brothers Karamazov</li>` in the DOM Tree and select **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="e5ed8-276">Una `document.querySelector()` expresión que se resuelve en el nodo se ha copiado en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-276">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="e5ed8-277">Pulse `Control` + `V` \ (Windows \) o `Command` + `V` \ (MacOS \) para pegar la expresión en la consola.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-277">Press `Control`+`V` \(Windows\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="e5ed8-278">Pulse `Enter` para evaluar la expresión.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-278">Press `Enter` to evaluate the expression.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Resultado de la expresión de ruta de copia JS" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           <span data-ttu-id="e5ed8-280">Resultado de la expresión de **ruta de copia JS**</span><span class="sxs-lookup"><span data-stu-id="e5ed8-280">The result of the **Copy JS Path** expression</span></span>  
        :::image-end:::  
        
## <span data-ttu-id="e5ed8-281">Interrupción en cambios de DOM</span><span class="sxs-lookup"><span data-stu-id="e5ed8-281">Break on DOM changes</span></span>   

<span data-ttu-id="e5ed8-282">DevTools le permite pausar el JavaScript de una página cuando el JavaScript modifica el DOM.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-282">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <span data-ttu-id="e5ed8-283">Interrupciones en las modificaciones de atributos</span><span class="sxs-lookup"><span data-stu-id="e5ed8-283">Break on attribute modifications</span></span>   

<span data-ttu-id="e5ed8-284">Use puntos de interrupción de modificación de atributos cuando desee pausar el código JavaScript que hace que los atributos de un nodo cambien.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-284">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="e5ed8-285">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-285">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="e5ed8-286">En **interrupción en las modificaciones de atributos**, haga clic con el botón derecho en **sauerkraut** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-286">Under **Break on attribute modifications**, right-click **Sauerkraut** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="e5ed8-287">En el árbol DOM, haga clic con el botón derecho `<li id="target">Sauerkraut</li>` y seleccione **interrumpir**las  >  **modificaciones de atributos**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-287">In the DOM Tree, right-click `<li id="target">Sauerkraut</li>` and select **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="e5ed8-288">Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no puede ver esta opción.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-288">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Interrupciones en las modificaciones de atributos" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **<span data-ttu-id="e5ed8-290">Interrupciones en las modificaciones de atributos</span><span class="sxs-lookup"><span data-stu-id="e5ed8-290">Break on attribute modifications</span></span>**  
        :::image-end:::  
        
    1.  <span data-ttu-id="e5ed8-291">En el siguiente paso, se le indicará que haga clic en un botón que pausa el código de la página.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-291">In the next step you are going to be instructed to click a button that pauses the code of the page.</span></span>  <span data-ttu-id="e5ed8-292">Una vez que la página se haya pausado, ya no podrás desplazarse por la página.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-292">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="e5ed8-293">Debe hacer clic en **resume script** \ ( ![ resume script ][ImageResumeScriptIcon] \) para hacer que la página se vuelva a desplazar.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-293">You must click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\) in order to make the page scrollable again.</span></span>
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Dónde reanudar la secuencia de comandos que se ejecuta" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           <span data-ttu-id="e5ed8-295">Dónde reanudar la secuencia de comandos que se ejecuta</span><span class="sxs-lookup"><span data-stu-id="e5ed8-295">Where to resume script running</span></span>  
        :::image-end:::  
        
    1.  <span data-ttu-id="e5ed8-296">Haga clic en el botón **establecer fondo** de arriba.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-296">Click the **Set Background** button above.</span></span>  <span data-ttu-id="e5ed8-297">Esto establece el `style` atributo del nodo en `background-color:thistle` .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-297">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="e5ed8-298">DevTools pausa la página y resalta el código que hizo que el atributo cambie.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-298">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="e5ed8-299">Haga clic en **reanudar script** \ ( ![ resume script ][ImageResumeScriptIcon] \), como se mencionó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-299">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\), as mentioned earlier.</span></span>  
    
### <span data-ttu-id="e5ed8-300">Interrupción en eliminación de nodo</span><span class="sxs-lookup"><span data-stu-id="e5ed8-300">Break on node removal</span></span>   

<span data-ttu-id="e5ed8-301">Si desea hacer una pausa cuando se quita un nodo en particular, use los puntos de interrupción de eliminación de nodos.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-301">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="e5ed8-302">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-302">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="e5ed8-303">En **interrupción en eliminación de nodo**, haga clic con el botón derecho en **Neuromancer** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-303">Under **Break on Node Removal**, right-click **Neuromancer** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="e5ed8-304">En el árbol DOM, haga clic con el botón derecho `<li id="target">Neuromancer</li>` y seleccione **interrumpir**  >  **eliminación de nodo**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-304">In the DOM Tree, right-click `<li id="target">Neuromancer</li>` and select **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="e5ed8-305">Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no puede ver esta opción.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-305">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="e5ed8-306">Haga clic en el botón **eliminar** .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-306">Click the **Delete** button above.</span></span>  <span data-ttu-id="e5ed8-307">DevTools pausa la página y resalta el código que ha provocado la eliminación del nodo.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-307">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="e5ed8-308">Haga clic en **reanudar script** \ ( ![ resume script ][ImageResumeScriptIcon] \).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-308">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
### <span data-ttu-id="e5ed8-309">Saltos en las modificaciones del subárbol</span><span class="sxs-lookup"><span data-stu-id="e5ed8-309">Break on subtree modifications</span></span>   

<span data-ttu-id="e5ed8-310">Después de poner un punto de interrupción de modificación de un subárbol en un nodo, DevTools hace una pausa en la página cuando se agrega o se quita cualquiera de los descendientes del nodo.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-310">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="e5ed8-311">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-311">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="e5ed8-312">En **interrupciones en las modificaciones de subárbol**, haga clic con el botón derecho en **un incendio** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-312">Under **Break on Subtree Modifications**, right-click **A Fire Upon The Deep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="e5ed8-313">En el árbol DOM, haga clic con el botón derecho `<ul id="target">` , que es el nodo de arriba `<li>A Fire Upon the Deep</li>` y seleccione **interrumpir en**las  >  **modificaciones del subárbol**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-313">In the DOM Tree, right-click `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, and select **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="e5ed8-314">Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no puede ver esta opción.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-314">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="e5ed8-315">Haga clic en **Agregar hijo**.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-315">Click **Add Child**.</span></span>  <span data-ttu-id="e5ed8-316">El código se detiene porque `<li>` se ha agregado un nodo a la lista.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-316">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="e5ed8-317">Haga clic en **reanudar script** \ ( ![ resume script ][ImageResumeScriptIcon] \).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-317">Click **Resume Script** \(![Resume Script][ImageResumeScriptIcon]\).</span></span>  
    
## <span data-ttu-id="e5ed8-318">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="e5ed8-318">Next steps</span></span>   

<span data-ttu-id="e5ed8-319">Que cubre la mayoría de las características relacionadas con DOM de DevTools.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-319">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="e5ed8-320">Puede descubrir el resto de ellos haciendo clic con el botón secundario en los nodos del árbol DOM y experimentando con las otras opciones que no se han descrito en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-320">You are able to discover the rest of them by right-clicking nodes in the DOM Tree and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="e5ed8-321">Consulte también [métodos abreviados de teclado del panel elementos][DevToolsShortcutsElements].</span><span class="sxs-lookup"><span data-stu-id="e5ed8-321">See also [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="e5ed8-322">Visite la [Página principal de Microsoft Edge DevTools][MicrosoftEdgeDevTools] para descubrir todo lo que pueda hacer con DevTools.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-322">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--See [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  



## <span data-ttu-id="e5ed8-323">Apéndice: HTML frente a DOM</span><span class="sxs-lookup"><span data-stu-id="e5ed8-323">Appendix: HTML versus the DOM</span></span>   

<span data-ttu-id="e5ed8-324">En la siguiente sección se explica rápidamente la diferencia entre HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-324">The following section quickly explains the difference between HTML and the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e5ed8-325">Cuando se usa un explorador Web para solicitar una página, el servidor devuelve HTML como el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-325">When you use a web browser to request a page, the server returns HTML like the following code snippet</span></span>  

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
      <span data-ttu-id="e5ed8-326">El explorador analiza el código HTML y crea un árbol de objetos como la siguiente lista.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-326">The browser parses the HTML and creates a tree of objects like the following list.</span></span>  
      
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

<span data-ttu-id="e5ed8-327">Este árbol de objetos, o nodos, que representa el contenido de la página, se denomina DOM.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-327">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="e5ed8-328">Ahora es lo mismo que el código HTML, pero Supongamos que la secuencia de comandos a la que se hace referencia en la parte inferior del HTML ejecuta el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-328">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs the following code snippet.</span></span>  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="e5ed8-329">Ese código quita el `h1` nodo y agrega otro `p` nodo al Dom.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-329">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="e5ed8-330">El DOM completo ahora muestra la siguiente lista.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-330">The complete DOM now displays the following list.</span></span>  
      
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

<span data-ttu-id="e5ed8-331">El código HTML de la página es ahora diferente al del DOM.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-331">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="e5ed8-332">En otras palabras, HTML representa el contenido inicial de la página y DOM representa el contenido de la página actual.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-332">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="e5ed8-333">Cuando JavaScript agrega, quita o modifica nodos, el DOM es diferente del HTML.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-333">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="e5ed8-334">Para obtener más información, consulta [Introducción al Dom][MDNIntroductionToDOM] .</span><span class="sxs-lookup"><span data-stu-id="e5ed8-334">See [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

<!--
## Appendix: Scroll into view   

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and select **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    > ##### Figure 19  
    > Scroll into view  
    > :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
   Scroll into view  
:::image-end:::  
    -->  

## <span data-ttu-id="e5ed8-335">Apéndice: opciones perdidas</span><span class="sxs-lookup"><span data-stu-id="e5ed8-335">Appendix: Missing options</span></span>   

<span data-ttu-id="e5ed8-336">Muchas de las instrucciones de este tutorial le indican que debe hacer clic con el botón secundario del mouse en un nodo del árbol DOM y, a continuación, seleccionar una opción en el menú contextual que aparece.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-336">Many of the instructions in this tutorial instruct you to right-click a node in the DOM Tree and then select an option from the context menu that pops up.</span></span>  <span data-ttu-id="e5ed8-337">Si no ve la opción especificada en el menú contextual, intente hacer clic con el botón secundario del ratón fuera del texto del nodo.</span><span class="sxs-lookup"><span data-stu-id="e5ed8-337">If you do not see the specified option in the context menu, try right-clicking away from the node text.</span></span>  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Dónde hacer clic si no ve todas las opciones" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   <span data-ttu-id="e5ed8-339">Dónde hacer clic si no ve todas las opciones</span><span class="sxs-lookup"><span data-stu-id="e5ed8-339">Where to click if you are not seeing all the options</span></span>  
:::image-end:::  

<!-- image links -->  

[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: ../media/resume-script-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas de desarrollador de Microsoft Edge \ (cromo \) | Microsoft docs"  
[DevToolsCssGetStarted]: ../css/index.md "Introducción a la visualización y el cambio de CSS | Microsoft docs"  
[DevToolsShortcutsElements]: ../shortcuts.md#elements-panel-keyboard-shortcuts "Métodos abreviados de teclado del panel elementos-métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft docs"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Ejemplo de DOM de DevTools Microsoft Edge (cromo) | Intento"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introducción a DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="e5ed8-345">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e5ed8-345">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e5ed8-346">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/dom/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="e5ed8-346">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e5ed8-348">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e5ed8-348">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

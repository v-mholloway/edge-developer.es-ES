---
title: Introducción a la visualización y el cambio de DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 4dee8b4e3ea927e72c0f98517f264b2c1d453013
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607450"
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





# <span data-ttu-id="91ff5-103">Introducción a la visualización y el cambio de DOM</span><span class="sxs-lookup"><span data-stu-id="91ff5-103">Get Started With Viewing And Changing The DOM</span></span>   



<span data-ttu-id="91ff5-104">Complete estos tutoriales interactivos para obtener información básica sobre cómo ver y cambiar el DOM de una página con Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="91ff5-104">Complete these interactive tutorials to learn the basics of viewing and changing the DOM of a page using Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="91ff5-105">En este tutorial se supone que conoce la diferencia entre DOM y HTML.</span><span class="sxs-lookup"><span data-stu-id="91ff5-105">This tutorial assumes that you know the difference between the DOM and HTML.</span></span>  <span data-ttu-id="91ff5-106">Consulta [el apéndice: HTML en comparación con Dom](#appendix-html-versus-the-dom) para obtener una explicación.</span><span class="sxs-lookup"><span data-stu-id="91ff5-106">See [Appendix: HTML versus the DOM](#appendix-html-versus-the-dom) for an explanation.</span></span>  

## <span data-ttu-id="91ff5-107">Ejemplos de Open DOM</span><span class="sxs-lookup"><span data-stu-id="91ff5-107">Open DOM Examples</span></span>  

1.  <span data-ttu-id="91ff5-108">Mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y haga clic en **ejemplos de Dom** para abrir en una nueva pestaña.</span><span class="sxs-lookup"><span data-stu-id="91ff5-108">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **DOM Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="91ff5-109">Ejemplos de DOM</span><span class="sxs-lookup"><span data-stu-id="91ff5-109">DOM Examples</span></span>][GlitchDomExamples]  
    
## <span data-ttu-id="91ff5-110">Ver nodos DOM</span><span class="sxs-lookup"><span data-stu-id="91ff5-110">View DOM nodes</span></span>   

<span data-ttu-id="91ff5-111">El árbol DOM del panel elementos es el lugar donde se realizan todas las actividades relacionadas con DOM en DevTools.</span><span class="sxs-lookup"><span data-stu-id="91ff5-111">The DOM Tree of the Elements panel is where you do all DOM-related activities in DevTools.</span></span>  

### <span data-ttu-id="91ff5-112">Inspeccionar un nodo</span><span class="sxs-lookup"><span data-stu-id="91ff5-112">Inspect a node</span></span>   

<span data-ttu-id="91ff5-113">Cuando esté interesado en un nodo DOM determinado, **inspeccionar** es una forma rápida de abrir DevTools e investigar ese nodo.</span><span class="sxs-lookup"><span data-stu-id="91ff5-113">When you are interested in a particular DOM node, **Inspect** is a fast way to open DevTools and investigate that node.</span></span>  

1.  <span data-ttu-id="91ff5-114">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="91ff5-114">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="91ff5-115">En **inspeccionar un nodo**, haga clic con el botón derecho en **Michelangelo** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-115">Under **Inspect a Node**, right-click **Michelangelo** and select **Inspect**.</span></span>  
    
    > ##### <span data-ttu-id="91ff5-116">Figura 1</span><span class="sxs-lookup"><span data-stu-id="91ff5-116">Figure 1</span></span>  
    > <span data-ttu-id="91ff5-117">Inspeccionar un nodo</span><span class="sxs-lookup"><span data-stu-id="91ff5-117">Inspecting a node</span></span>  
    > ![Inspeccionar un nodo][ImageInspectingNode]  
    
    1.  <span data-ttu-id="91ff5-119">Se abre el panel **elementos** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="91ff5-119">The **Elements** panel of DevTools opens.</span></span>  `<li>Michelangelo</li>` <span data-ttu-id="91ff5-120">está resaltado en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-120">is highlighted in the **DOM Tree**.</span></span>  
        
        > ##### <span data-ttu-id="91ff5-121">Figura 2</span><span class="sxs-lookup"><span data-stu-id="91ff5-121">Figure 2</span></span>  
        > <span data-ttu-id="91ff5-122">Resaltar el nodo Michelangelo</span><span class="sxs-lookup"><span data-stu-id="91ff5-122">Highlighting the Michelangelo node</span></span>  
        > ![Resaltar el nodo Michelangelo][ImageHighlightingMichelangeloNode]  
        
        1.  <span data-ttu-id="91ff5-124">Haga clic en el icono **inspeccionar** ![ inspección ][ImageInspectIcon] en la esquina superior izquierda de DevTools.</span><span class="sxs-lookup"><span data-stu-id="91ff5-124">Click the **Inspect** ![Inspect][ImageInspectIcon] icon in the top-left corner of DevTools.</span></span>  
            
            > ##### <span data-ttu-id="91ff5-125">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="91ff5-125">Figure 3</span></span>  
            > <span data-ttu-id="91ff5-126">Icono de inspección</span><span class="sxs-lookup"><span data-stu-id="91ff5-126">The Inspect icon</span></span>  
            > ![Icono de inspección][ImageInspect]  
            
1.  <span data-ttu-id="91ff5-128">En **inspeccionar un nodo**, haga clic en el texto de **Tokio** .</span><span class="sxs-lookup"><span data-stu-id="91ff5-128">Under **Inspect a Node**, click the **Tokyo** text.</span></span>  <span data-ttu-id="91ff5-129">Ahora, `<li>Tokyo</li>` está resaltado en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="91ff5-129">Now, `<li>Tokyo</li>` is highlighted in the DOM Tree.</span></span>  

<span data-ttu-id="91ff5-130">Inspeccionar un nodo también es el primer paso para ver y cambiar los estilos de un nodo.</span><span class="sxs-lookup"><span data-stu-id="91ff5-130">Inspecting a node is also the first step towards viewing and changing the styles of a node.</span></span>  <span data-ttu-id="91ff5-131">Consulte Introducción [a la visualización y el cambio de CSS][DevToolsCssGetStarted].</span><span class="sxs-lookup"><span data-stu-id="91ff5-131">See [Get Started With Viewing And Changing CSS][DevToolsCssGetStarted].</span></span>  

### <span data-ttu-id="91ff5-132">Navegar por el árbol DOM con un teclado</span><span class="sxs-lookup"><span data-stu-id="91ff5-132">Navigate the DOM Tree with a keyboard</span></span>   

<span data-ttu-id="91ff5-133">Una vez que haya seleccionado un nodo en el árbol DOM, puede desplazarse por el árbol DOM con el teclado.</span><span class="sxs-lookup"><span data-stu-id="91ff5-133">Once you have selected a node in the DOM Tree, you may navigate the DOM Tree with your keyboard.</span></span>  

1.  <span data-ttu-id="91ff5-134">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="91ff5-134">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="91ff5-135">En **navegar por el árbol DOM con un teclado**, haga clic con el botón derecho en **Ringo** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-135">Under **Navigate the DOM Tree with a Keyboard**, right-click **Ringo** and select **Inspect**.</span></span>  `<li>Ringo</li>` <span data-ttu-id="91ff5-136">está seleccionado en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="91ff5-136">is selected in the DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="91ff5-137">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="91ff5-137">Figure 4</span></span>  
    > <span data-ttu-id="91ff5-138">Inspeccionar el nodo Ringo</span><span class="sxs-lookup"><span data-stu-id="91ff5-138">Inspecting the Ringo node</span></span>  
    > ![Inspeccionar el nodo Ringo][ImageInspectingRingoNode]  
    
    1.  <span data-ttu-id="91ff5-140">Presione la `Up` tecla de dirección dos veces.</span><span class="sxs-lookup"><span data-stu-id="91ff5-140">Press the `Up` arrow key 2 times.</span></span>  `<ul>` <span data-ttu-id="91ff5-141">.</span><span class="sxs-lookup"><span data-stu-id="91ff5-141">is selected.</span></span>  
        
        > ##### <span data-ttu-id="91ff5-142">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="91ff5-142">Figure 5</span></span>  
        > <span data-ttu-id="91ff5-143">Inspeccionar el nodo UL</span><span class="sxs-lookup"><span data-stu-id="91ff5-143">Inspecting the ul node</span></span>  
        > ![Inspeccionar el nodo UL][ImageInspectingUlNode]  
        
    1.  <span data-ttu-id="91ff5-145">Presione la `Left` tecla de dirección.</span><span class="sxs-lookup"><span data-stu-id="91ff5-145">Press the `Left` arrow key.</span></span>  <span data-ttu-id="91ff5-146">La `<ul>` lista se contraerá.</span><span class="sxs-lookup"><span data-stu-id="91ff5-146">The `<ul>` list collapses.</span></span>  
    1.  <span data-ttu-id="91ff5-147">`Left`Vuelva a presionar la tecla de dirección.</span><span class="sxs-lookup"><span data-stu-id="91ff5-147">Press the `Left` arrow key again.</span></span>  <span data-ttu-id="91ff5-148">Se selecciona el elemento primario del `<ul>` nodo.</span><span class="sxs-lookup"><span data-stu-id="91ff5-148">The parent of the `<ul>` node is selected.</span></span>  <span data-ttu-id="91ff5-149">En este caso, es el `<div>` con el identificador `navigate-the-dom-tree-with-a-keyboard-1` .</span><span class="sxs-lookup"><span data-stu-id="91ff5-149">In this case it is the `<div>` with the ID `navigate-the-dom-tree-with-a-keyboard-1`.</span></span>  
    1.  <span data-ttu-id="91ff5-150">Presione la `Down` tecla de dirección dos veces para que se vuelva a seleccionar la `<ul>` lista que acaba de contraer.</span><span class="sxs-lookup"><span data-stu-id="91ff5-150">Press the `Down` arrow key 2 times so that you have re-selected the `<ul>` list that you just collapsed.</span></span>  <span data-ttu-id="91ff5-151">Debe tener el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="91ff5-151">It should look like this:</span></span> `<ul>... </ul>`  
    1.  <span data-ttu-id="91ff5-152">Presione la `Right` tecla de dirección.</span><span class="sxs-lookup"><span data-stu-id="91ff5-152">Press the `Right` arrow key.</span></span>  <span data-ttu-id="91ff5-153">Se expande la lista.</span><span class="sxs-lookup"><span data-stu-id="91ff5-153">The list expands.</span></span>  

### <span data-ttu-id="91ff5-154">Desplazarse en la vista</span><span class="sxs-lookup"><span data-stu-id="91ff5-154">Scroll into view</span></span>   

<span data-ttu-id="91ff5-155">Al ver el árbol DOM, es posible que te encuentres interesado en un nodo DOM que actualmente no está en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="91ff5-155">When viewing the DOM Tree, you may find yourself interested in a DOM node that is not currently in the viewport.</span></span>  <span data-ttu-id="91ff5-156">Por ejemplo, supongamos que se ha desplazado a la parte inferior de la página y está interesado en el `<h1>` nodo de la parte superior de la página.</span><span class="sxs-lookup"><span data-stu-id="91ff5-156">For example, suppose that you scrolled to the bottom of the page, and you are interested in the `<h1>` node at the top of the page.</span></span>  <span data-ttu-id="91ff5-157">**Desplazarse hacia la vista** le permite cambiar rápidamente la posición de la ventanilla para poder ver el nodo.</span><span class="sxs-lookup"><span data-stu-id="91ff5-157">**Scroll into view** lets you quickly reposition the viewport so that you are able to see the node.</span></span>  

1.  <span data-ttu-id="91ff5-158">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="91ff5-158">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="91ff5-159">En **desplazarse hacia la vista**, haga clic con el botón derecho en **Magritte** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-159">Under **Scroll into View**, right-click **Magritte** and select **Inspect**.</span></span>  
1.  <span data-ttu-id="91ff5-160">Desplácese hasta la parte inferior de la página de ejemplos de DOM.</span><span class="sxs-lookup"><span data-stu-id="91ff5-160">Scroll to the bottom of the DOM Examples page.</span></span>  
1.  <span data-ttu-id="91ff5-161">El `<li>Magritte</li>` nodo debe seguir estando seleccionado en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="91ff5-161">The `<li>Magritte</li>` node should still be selected in your DOM Tree.</span></span>  <span data-ttu-id="91ff5-162">Si no es así, vuelva a [desplazarse](#scroll-into-view) hacia la vista y volver a empezar.</span><span class="sxs-lookup"><span data-stu-id="91ff5-162">If not, go back to [Scroll into view](#scroll-into-view) and start over.</span></span>  
1.  <span data-ttu-id="91ff5-163">Haga clic con el botón derecho en el `<li>Magritte</li>` nodo y seleccione **desplazarse a la vista**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-163">Right-click the `<li>Magritte</li>` node and select **Scroll into view**.</span></span>  <span data-ttu-id="91ff5-164">Su ventanilla se desplaza hacia arriba para que pueda ver el nodo **Magritte** .</span><span class="sxs-lookup"><span data-stu-id="91ff5-164">Your viewport scrolls back up so that you may see the **Magritte** node.</span></span>  <span data-ttu-id="91ff5-165">Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no puede ver la opción **desplazarse a la vista** .</span><span class="sxs-lookup"><span data-stu-id="91ff5-165">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.</span></span>
    
    > ##### <span data-ttu-id="91ff5-166">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="91ff5-166">Figure 6</span></span>  
    > <span data-ttu-id="91ff5-167">Desplazarse en la vista</span><span class="sxs-lookup"><span data-stu-id="91ff5-167">Scroll into view</span></span>  
    > ![Desplazarse en la vista][ImageScrollView]  

### <span data-ttu-id="91ff5-169">Buscar nodos</span><span class="sxs-lookup"><span data-stu-id="91ff5-169">Search for nodes</span></span>   

<span data-ttu-id="91ff5-170">Puede buscar en el árbol DOM por cadena, selector de CSS o selector XPath.</span><span class="sxs-lookup"><span data-stu-id="91ff5-170">You may search the DOM Tree by string, CSS selector, or XPath selector.</span></span>  

1.  <span data-ttu-id="91ff5-171">Centre el cursor en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="91ff5-171">Focus your cursor on the **Elements** panel.</span></span>  
1.  <span data-ttu-id="91ff5-172">Pulse `Control` + `F` \ (Windows \) o `Command` + `F` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="91ff5-172">Press `Control`+`F` \(Windows\) or `Command`+`F` \(macOS\).</span></span>  <span data-ttu-id="91ff5-173">La barra de búsqueda se abre en la parte inferior del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="91ff5-173">The Search bar opens at the bottom of the DOM Tree.</span></span>  
1.  <span data-ttu-id="91ff5-174">Escribe `The Moon is a Harsh Mistress`.</span><span class="sxs-lookup"><span data-stu-id="91ff5-174">Type `The Moon is a Harsh Mistress`.</span></span>  <span data-ttu-id="91ff5-175">La última oración se resalta en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="91ff5-175">The last sentence is highlighted in the DOM Tree.</span></span>  
    
    > ##### <span data-ttu-id="91ff5-176">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="91ff5-176">Figure 7</span></span>  
    > <span data-ttu-id="91ff5-177">Resaltar la consulta en la barra de búsqueda</span><span class="sxs-lookup"><span data-stu-id="91ff5-177">Highlighting the query in the Search bar</span></span>  
    > ![Resaltar la consulta en la barra de búsqueda][ImageHighlightingQuerySearchBar]  
    
<span data-ttu-id="91ff5-179">Como se mencionó anteriormente, la barra de búsqueda también admite los selectores CSS y CSS.</span><span class="sxs-lookup"><span data-stu-id="91ff5-179">As mentioned above, the Search bar also supports CSS and XPath selectors.</span></span>  

## <span data-ttu-id="91ff5-180">Editar el DOM</span><span class="sxs-lookup"><span data-stu-id="91ff5-180">Edit the DOM</span></span>   

<span data-ttu-id="91ff5-181">Puede editar el DOM sobre la marcha y ver cómo afectan esos cambios a la página.</span><span class="sxs-lookup"><span data-stu-id="91ff5-181">You may edit the DOM on the fly and see how those changes affect the page.</span></span>  

### <span data-ttu-id="91ff5-182">Editar contenido</span><span class="sxs-lookup"><span data-stu-id="91ff5-182">Edit content</span></span>   

<span data-ttu-id="91ff5-183">Para editar el contenido de un nodo, haga doble clic en el contenido del árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="91ff5-183">To edit the content of a node, double-click the content in the DOM Tree.</span></span>  

1.  <span data-ttu-id="91ff5-184">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="91ff5-184">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="91ff5-185">En **editar contenido**, haga clic con el botón derecho en **Michelle** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-185">Under **Edit Content**, right-click **Michelle** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="91ff5-186">En el árbol DOM, haga doble clic `Michelle` .</span><span class="sxs-lookup"><span data-stu-id="91ff5-186">In the DOM Tree, double-click `Michelle`.</span></span>  <span data-ttu-id="91ff5-187">En otras palabras, haga doble clic en el texto entre `<li>` y `</li>` .</span><span class="sxs-lookup"><span data-stu-id="91ff5-187">In other words, double-click the text between `<li>` and `</li>`.</span></span>  <span data-ttu-id="91ff5-188">El texto se resalta para indicar que está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="91ff5-188">The text is highlighted to indicate that it is selected.</span></span>  
        
        > ##### <span data-ttu-id="91ff5-189">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="91ff5-189">Figure 8</span></span>  
        > <span data-ttu-id="91ff5-190">Editar el texto</span><span class="sxs-lookup"><span data-stu-id="91ff5-190">Editing the text</span></span>  
        > ![Editar el texto][ImageEditingText]  
        
    1.  <span data-ttu-id="91ff5-192">Eliminar `Michelle` , escriba `Leela` y, a continuación, pulse `Enter` para confirmar el cambio.</span><span class="sxs-lookup"><span data-stu-id="91ff5-192">Delete `Michelle`, type `Leela`, then press `Enter` to confirm the change.</span></span>  <span data-ttu-id="91ff5-193">El texto del DOM cambia de **Michelle** a **Leela**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-193">The text in the DOM changes from **Michelle** to **Leela**.</span></span>  

### <span data-ttu-id="91ff5-194">Editar atributos</span><span class="sxs-lookup"><span data-stu-id="91ff5-194">Edit attributes</span></span>   

<span data-ttu-id="91ff5-195">Para editar atributos, haga doble clic en el nombre o valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="91ff5-195">To edit attributes, double-click the attribute name or value.</span></span>  <span data-ttu-id="91ff5-196">Siga las instrucciones para obtener información sobre cómo agregar atributos a un nodo.</span><span class="sxs-lookup"><span data-stu-id="91ff5-196">Follow the instructions to learn how to add attributes to a node.</span></span>  

1.  <span data-ttu-id="91ff5-197">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="91ff5-197">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="91ff5-198">En **Editar atributos**, haga clic con el botón derecho en **Howard** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-198">Under **Edit Attributes**, right-click **Howard** and select **Inspect**.</span></span>  

1.  <span data-ttu-id="91ff5-199">Haga doble clic `<li>` .</span><span class="sxs-lookup"><span data-stu-id="91ff5-199">Double-click `<li>`.</span></span>  <span data-ttu-id="91ff5-200">El texto se resalta para indicar que el nodo está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="91ff5-200">The text is highlighted to indicate that the node is selected.</span></span>  
    
    > ##### <span data-ttu-id="91ff5-201">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="91ff5-201">Figure 9</span></span>  
    > <span data-ttu-id="91ff5-202">Editar el nodo</span><span class="sxs-lookup"><span data-stu-id="91ff5-202">Editing the node</span></span>  
    > ![Editar el nodo][ImageEditingNode]  
    
1.  <span data-ttu-id="91ff5-204">Presione la `Right` tecla de dirección, agregue un espacio, escriba `style="background-color:gold"` y, a continuación, presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="91ff5-204">Press the `Right` arrow key, add a space, type `style="background-color:gold"`, and then press `Enter`.</span></span>  <span data-ttu-id="91ff5-205">El color de fondo del nodo cambia a oro.</span><span class="sxs-lookup"><span data-stu-id="91ff5-205">The background color of the node changes to gold.</span></span>  
    
    > ##### <span data-ttu-id="91ff5-206">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="91ff5-206">Figure 10</span></span>  
    > <span data-ttu-id="91ff5-207">Agregar un atributo de estilo al nodo</span><span class="sxs-lookup"><span data-stu-id="91ff5-207">Adding a style attribute to the node</span></span>  
    > ![Agregar un atributo de estilo al nodo][ImageAddingStyleAttributeNode]  
    
### <span data-ttu-id="91ff5-209">Editar tipo de nodo</span><span class="sxs-lookup"><span data-stu-id="91ff5-209">Edit node type</span></span>   

<span data-ttu-id="91ff5-210">Para editar el tipo de un nodo, haga doble clic en el tipo y, a continuación, escriba el nuevo tipo.</span><span class="sxs-lookup"><span data-stu-id="91ff5-210">To edit the type of a node, double-click the type and then type in the new type.</span></span>  

1.  <span data-ttu-id="91ff5-211">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="91ff5-211">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="91ff5-212">En **Editar tipo de nodo**, haga clic con el botón derecho en **Hank** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-212">Under **Edit Node Type**, right-click **Hank** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="91ff5-213">Haga doble clic `<li>` .</span><span class="sxs-lookup"><span data-stu-id="91ff5-213">Double-click `<li>`.</span></span>  <span data-ttu-id="91ff5-214">`li`Se resalta el texto.</span><span class="sxs-lookup"><span data-stu-id="91ff5-214">The text `li` is highlighted.</span></span>  
    1.  <span data-ttu-id="91ff5-215">Eliminar `li` , escriba `button` y, a continuación, pulse `Enter` .</span><span class="sxs-lookup"><span data-stu-id="91ff5-215">Delete `li`, type `button`, then press `Enter`.</span></span>  <span data-ttu-id="91ff5-216">El `<li>` nodo cambia a un `<button>` nodo.</span><span class="sxs-lookup"><span data-stu-id="91ff5-216">The `<li>` node changes to a `<button>` node.</span></span>  
        
        > ##### <span data-ttu-id="91ff5-217">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="91ff5-217">Figure 11</span></span>  
        > <span data-ttu-id="91ff5-218">Cambiar el tipo de nodo a botón</span><span class="sxs-lookup"><span data-stu-id="91ff5-218">Changing the node type to button</span></span>  
        > ![Cambiar el tipo de nodo a botón][ImageChangingNodeButton]  
        
### <span data-ttu-id="91ff5-220">Reordenar los nodos DOM</span><span class="sxs-lookup"><span data-stu-id="91ff5-220">Reorder DOM nodes</span></span>   

<span data-ttu-id="91ff5-221">Arrastre los nodos para reordenarlos.</span><span class="sxs-lookup"><span data-stu-id="91ff5-221">Drag nodes to reorder them.</span></span>  

1.  <span data-ttu-id="91ff5-222">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="91ff5-222">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="91ff5-223">En **Reordenar los nodos DOM**, haga clic con el botón derecho en **Elvis Presley** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-223">Under **Reorder DOM Nodes**, right-click **Elvis Presley** and select **Inspect**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="91ff5-224">Es el último elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="91ff5-224">It is the last item in the list.</span></span>  
    
    1.  <span data-ttu-id="91ff5-225">En el árbol DOM, arrastre `<li>Elvis Presley</li>` hasta la parte superior de la lista.</span><span class="sxs-lookup"><span data-stu-id="91ff5-225">In the DOM Tree, drag `<li>Elvis Presley</li>` to the top of the list.</span></span>  
        
        > ##### <span data-ttu-id="91ff5-226">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="91ff5-226">Figure 12</span></span>  
        > <span data-ttu-id="91ff5-227">Arrastrar el nodo a la parte superior de la lista</span><span class="sxs-lookup"><span data-stu-id="91ff5-227">Dragging the node to the top of the list</span></span>  
        > ![Arrastrar el nodo a la parte superior de la lista][ImageDraggingNodeTopList]  
        
### <span data-ttu-id="91ff5-229">Estado de fuerza</span><span class="sxs-lookup"><span data-stu-id="91ff5-229">Force state</span></span>   

<span data-ttu-id="91ff5-230">Puede obligar a que los nodos permanezcan en Estados incluidos `:active` ,, `:hover` `:focus` , `:visited` y `:focus-within` .</span><span class="sxs-lookup"><span data-stu-id="91ff5-230">You are able to force nodes to remain in states including `:active`, `:hover`, `:focus`, `:visited`, and `:focus-within`.</span></span>  

1.  <span data-ttu-id="91ff5-231">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="91ff5-231">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="91ff5-232">En **Estado de fuerza**, desplace el puntero sobre **el Señor de la vuela**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-232">Under **Force state**, hover over **The Lord of the Flies**.</span></span>  <span data-ttu-id="91ff5-233">El color de fondo se convierte en naranja.</span><span class="sxs-lookup"><span data-stu-id="91ff5-233">The background color becomes orange.</span></span>  
    1.  <span data-ttu-id="91ff5-234">Haga clic con el botón derecho en **el Señor de la vuela** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-234">Right-click **The Lord of the Flies** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="91ff5-235">Haga clic con el botón derecho `<li class="demo--hover">The Lord of the Flies</li>` y seleccione **Estado de fuerza**  >  **: mantener**el mouse.</span><span class="sxs-lookup"><span data-stu-id="91ff5-235">Right-click `<li class="demo--hover">The Lord of the Flies</li>` and select **Force State** > **:hover**.</span></span>  <span data-ttu-id="91ff5-236">Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no ve esta opción.</span><span class="sxs-lookup"><span data-stu-id="91ff5-236">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  <span data-ttu-id="91ff5-237">El color de fondo sigue siendo naranja aunque no se esté colocando el puntero sobre el nodo.</span><span class="sxs-lookup"><span data-stu-id="91ff5-237">The background color remains orange even though you are not actually hovering over the node.</span></span>  

### <span data-ttu-id="91ff5-238">Ocultar un nodo</span><span class="sxs-lookup"><span data-stu-id="91ff5-238">Hide a node</span></span>   

<span data-ttu-id="91ff5-239">Pulse `H` para ocultar un nodo.</span><span class="sxs-lookup"><span data-stu-id="91ff5-239">Press `H` to hide a node.</span></span>  

1.  <span data-ttu-id="91ff5-240">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="91ff5-240">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="91ff5-241">En **ocultar un nodo**, haga clic con el botón derecho en **las estrellas mi destino** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-241">Under **Hide a node**, right-click **The Stars My Destination** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="91ff5-242">Presione la `H` tecla.</span><span class="sxs-lookup"><span data-stu-id="91ff5-242">Press the `H` key.</span></span>  <span data-ttu-id="91ff5-243">El nodo está oculto.</span><span class="sxs-lookup"><span data-stu-id="91ff5-243">The node is hidden.</span></span>  
        
        > ##### <span data-ttu-id="91ff5-244">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="91ff5-244">Figure 13</span></span>  
        > <span data-ttu-id="91ff5-245">El aspecto del nodo en el árbol DOM después de ocultarlo</span><span class="sxs-lookup"><span data-stu-id="91ff5-245">What the node looks like in the DOM Tree after it is hidden</span></span>  
        > ![El aspecto del nodo en el árbol DOM después de ocultarlo][ImageNodeDomTreeAfterHidden]  
        
    1.  <span data-ttu-id="91ff5-247">`H`Vuelva a presionar la tecla.</span><span class="sxs-lookup"><span data-stu-id="91ff5-247">Press the `H` key again.</span></span>  <span data-ttu-id="91ff5-248">Se vuelve a mostrar el nodo.</span><span class="sxs-lookup"><span data-stu-id="91ff5-248">The node is shown again.</span></span>  

### <span data-ttu-id="91ff5-249">Eliminar un nodo</span><span class="sxs-lookup"><span data-stu-id="91ff5-249">Delete a node</span></span>   

<span data-ttu-id="91ff5-250">Pulse `Delete` para eliminar un nodo.</span><span class="sxs-lookup"><span data-stu-id="91ff5-250">Press `Delete` to delete a node.</span></span>  

1.  <span data-ttu-id="91ff5-251">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="91ff5-251">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="91ff5-252">En **eliminar un nodo**, haga clic con el botón derecho en **Foundation** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-252">Under **Delete a Node**, right-click **Foundation** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="91ff5-253">Presione la `Delete` tecla.</span><span class="sxs-lookup"><span data-stu-id="91ff5-253">Press the `Delete` key.</span></span>  <span data-ttu-id="91ff5-254">Se elimina el nodo.</span><span class="sxs-lookup"><span data-stu-id="91ff5-254">The node is deleted.</span></span>  
    1.  <span data-ttu-id="91ff5-255">Pulse `Control` + `Z` \ (Windows \) o `Command` + `Z` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="91ff5-255">Press `Control`+`Z` \(Windows\) or `Command`+`Z` \(macOS\).</span></span>  <span data-ttu-id="91ff5-256">La última acción se deshará y el nodo reaparecerá.</span><span class="sxs-lookup"><span data-stu-id="91ff5-256">The last action is undone and the node reappears.</span></span>  

## <span data-ttu-id="91ff5-257">Nodos de acceso en la consola</span><span class="sxs-lookup"><span data-stu-id="91ff5-257">Access nodes in the Console</span></span>   

<span data-ttu-id="91ff5-258">DevTools proporciona algunos métodos abreviados para acceder a los nodos DOM desde la consola o para obtener referencias de JavaScript a cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="91ff5-258">DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to each one.</span></span>  

### <span data-ttu-id="91ff5-259">Hacer referencia al nodo actualmente seleccionado con $0</span><span class="sxs-lookup"><span data-stu-id="91ff5-259">Reference the currently-selected node with $0</span></span>   

<span data-ttu-id="91ff5-260">Al inspeccionar un nodo, el `== $0` texto que se encuentra junto al nodo significa que puede hacer referencia a este nodo en la consola con la variable `$0` .</span><span class="sxs-lookup"><span data-stu-id="91ff5-260">When you inspect a node, the `== $0` text next to the node means that you may reference this node in the Console with the variable `$0`.</span></span>  

1.  <span data-ttu-id="91ff5-261">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="91ff5-261">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="91ff5-262">En **referencia el nodo seleccionado actualmente con $0**, haga clic con el botón derecho en **el lado izquierdo de la oscuridad** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-262">Under **Reference the currently-selected node with $0**, right-click **The Left Hand of Darkness** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="91ff5-263">Presione la `Escape` tecla para abrir el cajón de consola.</span><span class="sxs-lookup"><span data-stu-id="91ff5-263">Press the `Escape` key to open the Console Drawer.</span></span>  
    1.  <span data-ttu-id="91ff5-264">Escriba `$0` y presione la `Enter` tecla.</span><span class="sxs-lookup"><span data-stu-id="91ff5-264">Type `$0` and press the `Enter` key.</span></span>  <span data-ttu-id="91ff5-265">El resultado de la expresión muestra que `$0` se evalúa `<li>The Left Hand of Darkness</li>` .</span><span class="sxs-lookup"><span data-stu-id="91ff5-265">The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>`.</span></span>  
        
        > ##### <span data-ttu-id="91ff5-266">Imagen 14</span><span class="sxs-lookup"><span data-stu-id="91ff5-266">Figure 14</span></span>  
        > <span data-ttu-id="91ff5-267">El resultado de la primera `$0` expresión en la consola</span><span class="sxs-lookup"><span data-stu-id="91ff5-267">The result of the first `$0` expression in the Console</span></span>  
        > ![El resultado de la primera expresión $0 en la consola][ImageFirstConsole]  
        
    1.  <span data-ttu-id="91ff5-269">Desplace el puntero sobre el resultado.</span><span class="sxs-lookup"><span data-stu-id="91ff5-269">Hover over the result.</span></span>  <span data-ttu-id="91ff5-270">El nodo se resalta en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="91ff5-270">The node is highlighted in the viewport.</span></span>  
    1.  <span data-ttu-id="91ff5-271">Haga clic `<li>Dune</li>` en el árbol DOM, escriba `$0` la consola de nuevo y, a continuación, vuelva a presionar `Enter` .</span><span class="sxs-lookup"><span data-stu-id="91ff5-271">Click `<li>Dune</li>` in the DOM Tree, type `$0` in the Console again, and then press `Enter` again.</span></span>  <span data-ttu-id="91ff5-272">Ahora, `$0` evalúa a `<li>Dune</li>` .</span><span class="sxs-lookup"><span data-stu-id="91ff5-272">Now, `$0` evaluates to `<li>Dune</li>`.</span></span>  
        
        > ##### <span data-ttu-id="91ff5-273">Imagen 15</span><span class="sxs-lookup"><span data-stu-id="91ff5-273">Figure 15</span></span>  
        > <span data-ttu-id="91ff5-274">Resultado de la segunda `$0` expresión en la consola ![ el resultado de la segunda expresión $0 en la consola][ImageSecondConsole]</span><span class="sxs-lookup"><span data-stu-id="91ff5-274">The result of the second `$0` expression in the Console ![The result of the second $0 expression in the Console][ImageSecondConsole]</span></span>  
        
### <span data-ttu-id="91ff5-275">Almacenar como variable global</span><span class="sxs-lookup"><span data-stu-id="91ff5-275">Store as global variable</span></span>   

<span data-ttu-id="91ff5-276">Si necesita hacer referencia a un nodo varias veces, almacénelo como una variable global.</span><span class="sxs-lookup"><span data-stu-id="91ff5-276">If you need to refer back to a node many times, store it as a global variable.</span></span>  

1.  <span data-ttu-id="91ff5-277">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="91ff5-277">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="91ff5-278">En **almacenar como variable global**, haga clic con el botón secundario en **el gran sueño** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-278">Under **Store as global variable**, right-click **The Big Sleep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="91ff5-279">Haga clic con el botón derecho `<li>The Big Sleep</li>` en el árbol DOM y seleccione **almacenar como variable global**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-279">Right-click `<li>The Big Sleep</li>` in the DOM Tree and select **Store as global variable**.</span></span>  <span data-ttu-id="91ff5-280">Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no ve esta opción.</span><span class="sxs-lookup"><span data-stu-id="91ff5-280">See [Appendix: Missing options](#appendix-missing-options) if you do not see this option.</span></span>  
    1.  <span data-ttu-id="91ff5-281">Escriba `temp1` la consola y, a continuación, pulse `Enter` .</span><span class="sxs-lookup"><span data-stu-id="91ff5-281">Type `temp1` in the Console and then press `Enter`.</span></span>  <span data-ttu-id="91ff5-282">El resultado de la expresión muestra que la variable se evalúa en el nodo.</span><span class="sxs-lookup"><span data-stu-id="91ff5-282">The result of the expression shows that the variable evaluates to the node.</span></span>  
        
        > ##### <span data-ttu-id="91ff5-283">Imagen 16</span><span class="sxs-lookup"><span data-stu-id="91ff5-283">Figure 16</span></span>  
        > <span data-ttu-id="91ff5-284">El resultado de la expresión temp1</span><span class="sxs-lookup"><span data-stu-id="91ff5-284">The result of the temp1 expression</span></span>  
        > ![El resultado de la expresión temp1][ImageResultTemp1]  
        
### <span data-ttu-id="91ff5-286">Copiar ruta JS</span><span class="sxs-lookup"><span data-stu-id="91ff5-286">Copy JS path</span></span>   

<span data-ttu-id="91ff5-287">Copie la ruta de acceso de JavaScript en un nodo cuando necesite hacer referencia a él en una prueba automatizada.</span><span class="sxs-lookup"><span data-stu-id="91ff5-287">Copy the JavaScript path to a node when you need to reference it in an automated test.</span></span>  

1.  <span data-ttu-id="91ff5-288">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="91ff5-288">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="91ff5-289">En **copiar JS path**, haga clic con el botón secundario en **el Karamazov de Brothers** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-289">Under **Copy JS path**, right-click **The Brothers Karamazov** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="91ff5-290">Haga clic con el botón derecho `<li>The Brothers Karamazov</li>` en el árbol DOM y seleccione **copiar**  >  **copia JS ruta**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-290">Right-click `<li>The Brothers Karamazov</li>` in the DOM Tree and select **Copy** > **Copy JS Path**.</span></span>  <span data-ttu-id="91ff5-291">Una `document.querySelector()` expresión que se resuelve en el nodo se ha copiado en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="91ff5-291">A `document.querySelector()` expression that resolves to the node has been copied to your clipboard.</span></span>  
    1.  <span data-ttu-id="91ff5-292">Pulse `Control` + `V` \ (Windows \) o `Command` + `V` \ (MacOS \) para pegar la expresión en la consola.</span><span class="sxs-lookup"><span data-stu-id="91ff5-292">Press `Control`+`V` \(Windows\) or `Command`+`V` \(macOS\) to paste the expression into the Console.</span></span>  
    1.  <span data-ttu-id="91ff5-293">Pulse `Enter` para evaluar la expresión.</span><span class="sxs-lookup"><span data-stu-id="91ff5-293">Press `Enter` to evaluate the expression.</span></span>
        
        > ##### <span data-ttu-id="91ff5-294">Imagen 17</span><span class="sxs-lookup"><span data-stu-id="91ff5-294">Figure 17</span></span>  
        > <span data-ttu-id="91ff5-295">Resultado de la expresión de ruta de copia JS</span><span class="sxs-lookup"><span data-stu-id="91ff5-295">The result of the Copy JS Path expression</span></span>  
        > ![Resultado de la expresión de ruta de copia JS][ImageResultCopyJSPath]  
        
## <span data-ttu-id="91ff5-297">Interrupción en cambios de DOM</span><span class="sxs-lookup"><span data-stu-id="91ff5-297">Break on DOM changes</span></span>   

<span data-ttu-id="91ff5-298">DevTools le permite pausar el JavaScript de una página cuando el JavaScript modifica el DOM.</span><span class="sxs-lookup"><span data-stu-id="91ff5-298">DevTools enables you to pause the JavaScript of a page when the JavaScript modifies the DOM.</span></span>  

### <span data-ttu-id="91ff5-299">Interrupciones en las modificaciones de atributos</span><span class="sxs-lookup"><span data-stu-id="91ff5-299">Break on attribute modifications</span></span>   

<span data-ttu-id="91ff5-300">Use puntos de interrupción de modificación de atributos cuando desee pausar el código JavaScript que hace que los atributos de un nodo cambien.</span><span class="sxs-lookup"><span data-stu-id="91ff5-300">Use attribute modification breakpoints when you want to pause the JavaScript that causes any attribute of a node to change.</span></span>  

1.  <span data-ttu-id="91ff5-301">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="91ff5-301">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="91ff5-302">En **interrupción en las modificaciones de atributos**, haga clic con el botón derecho en **sauerkraut** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-302">Under **Break on attribute modifications**, right-click **Sauerkraut** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="91ff5-303">En el árbol DOM, haga clic con el botón derecho `<li id="target">Sauerkraut</li>` y seleccione **interrumpir**las  >  **modificaciones de atributos**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-303">In the DOM Tree, right-click `<li id="target">Sauerkraut</li>` and select **Break On** > **Attribute Modifications**.</span></span>  <span data-ttu-id="91ff5-304">Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no puede ver esta opción.</span><span class="sxs-lookup"><span data-stu-id="91ff5-304">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>
        
        > ##### <span data-ttu-id="91ff5-305">Ilustración 18</span><span class="sxs-lookup"><span data-stu-id="91ff5-305">Figure 18</span></span>  
        > <span data-ttu-id="91ff5-306">Interrupciones en las modificaciones de atributos</span><span class="sxs-lookup"><span data-stu-id="91ff5-306">Break on attribute modifications</span></span>  
        > ![Interrupciones en las modificaciones de atributos][ImageBreakAttributeModification]  
        
    1.  <span data-ttu-id="91ff5-308">En el siguiente paso, se le indicará que haga clic en un botón que pausa el código de la página.</span><span class="sxs-lookup"><span data-stu-id="91ff5-308">In the next step you are going to be instructed to click a button that pauses the code of the page.</span></span>  <span data-ttu-id="91ff5-309">Una vez que la página se haya pausado, ya no podrás desplazarse por la página.</span><span class="sxs-lookup"><span data-stu-id="91ff5-309">After the page is paused you are no longer able to scroll the page.</span></span>  <span data-ttu-id="91ff5-310">Debe hacer clic en **reanudar** ![ script ][ImageResumeScriptIcon] de currículo para que la página se vuelva a desplazar.</span><span class="sxs-lookup"><span data-stu-id="91ff5-310">You must click **Resume Script** ![Resume Script][ImageResumeScriptIcon] in order to make the page scrollable again.</span></span>
        
        > ##### <span data-ttu-id="91ff5-311">Ilustración 19</span><span class="sxs-lookup"><span data-stu-id="91ff5-311">Figure 19</span></span>  
        > <span data-ttu-id="91ff5-312">Dónde reanudar la secuencia de comandos que se ejecuta</span><span class="sxs-lookup"><span data-stu-id="91ff5-312">Where to resume script running</span></span>  
        > ![Dónde reanudar la secuencia de comandos que se ejecuta][ImageResumeScript]  
        
    1.  <span data-ttu-id="91ff5-314">Haga clic en el botón **establecer fondo** de arriba.</span><span class="sxs-lookup"><span data-stu-id="91ff5-314">Click the **Set Background** button above.</span></span>  <span data-ttu-id="91ff5-315">Esto establece el `style` atributo del nodo en `background-color:thistle` .</span><span class="sxs-lookup"><span data-stu-id="91ff5-315">This sets the `style` attribute of the node to `background-color:thistle`.</span></span>  <span data-ttu-id="91ff5-316">DevTools pausa la página y resalta el código que hizo que el atributo cambie.</span><span class="sxs-lookup"><span data-stu-id="91ff5-316">DevTools pauses the page and highlights the code that caused the attribute to change.</span></span>  
    1.  <span data-ttu-id="91ff5-317">Haga clic en **reanudar** script ![ ][ImageResumeScriptIcon] de currículo, como se mencionó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="91ff5-317">Click **Resume Script** ![Resume Script][ImageResumeScriptIcon], as mentioned earlier.</span></span>  
    
### <span data-ttu-id="91ff5-318">Interrupción en eliminación de nodo</span><span class="sxs-lookup"><span data-stu-id="91ff5-318">Break on node removal</span></span>   

<span data-ttu-id="91ff5-319">Si desea hacer una pausa cuando se quita un nodo en particular, use los puntos de interrupción de eliminación de nodos.</span><span class="sxs-lookup"><span data-stu-id="91ff5-319">If you want to pause when a particular node is removed, use node removal breakpoints.</span></span>  

1.  <span data-ttu-id="91ff5-320">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="91ff5-320">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="91ff5-321">En **interrupción en eliminación de nodo**, haga clic con el botón derecho en **Neuromancer** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-321">Under **Break on Node Removal**, right-click **Neuromancer** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="91ff5-322">En el árbol DOM, haga clic con el botón derecho `<li id="target">Neuromancer</li>` y seleccione **interrumpir**  >  **eliminación de nodo**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-322">In the DOM Tree, right-click `<li id="target">Neuromancer</li>` and select **Break On** > **Node Removal**.</span></span>  <span data-ttu-id="91ff5-323">Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no puede ver esta opción.</span><span class="sxs-lookup"><span data-stu-id="91ff5-323">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="91ff5-324">Haga clic en el botón **eliminar** .</span><span class="sxs-lookup"><span data-stu-id="91ff5-324">Click the **Delete** button above.</span></span>  <span data-ttu-id="91ff5-325">DevTools pausa la página y resalta el código que ha provocado la eliminación del nodo.</span><span class="sxs-lookup"><span data-stu-id="91ff5-325">DevTools pauses the page and highlights the code that caused the node to be removed.</span></span>  
    1.  <span data-ttu-id="91ff5-326">Haga clic en **reanudar** script de ![ currículo ][ImageResumeScriptIcon] .</span><span class="sxs-lookup"><span data-stu-id="91ff5-326">Click **Resume Script** ![Resume Script][ImageResumeScriptIcon].</span></span>  
    
### <span data-ttu-id="91ff5-327">Saltos en las modificaciones del subárbol</span><span class="sxs-lookup"><span data-stu-id="91ff5-327">Break on subtree modifications</span></span>   

<span data-ttu-id="91ff5-328">Después de poner un punto de interrupción de modificación de un subárbol en un nodo, DevTools hace una pausa en la página cuando se agrega o se quita cualquiera de los descendientes del nodo.</span><span class="sxs-lookup"><span data-stu-id="91ff5-328">After you put a subtree modification breakpoint on a node, DevTools pauses the page when any of the descendants of the node are added or removed.</span></span>  

1.  <span data-ttu-id="91ff5-329">[Abra ejemplos de Dom](#open-dom-examples).</span><span class="sxs-lookup"><span data-stu-id="91ff5-329">[Open DOM Examples](#open-dom-examples).</span></span>  
1.  <span data-ttu-id="91ff5-330">En **interrupciones en las modificaciones de subárbol**, haga clic con el botón derecho en **un incendio** y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-330">Under **Break on Subtree Modifications**, right-click **A Fire Upon The Deep** and select **Inspect**.</span></span>  
    1.  <span data-ttu-id="91ff5-331">En el árbol DOM, haga clic con el botón derecho `<ul id="target">` , que es el nodo de arriba `<li>A Fire Upon the Deep</li>` y seleccione **interrumpir en**las  >  **modificaciones del subárbol**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-331">In the DOM Tree, right-click `<ul id="target">`, which is the node above `<li>A Fire Upon the Deep</li>`, and select **Break On** > **Subtree Modifications**.</span></span>  <span data-ttu-id="91ff5-332">Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no puede ver esta opción.</span><span class="sxs-lookup"><span data-stu-id="91ff5-332">See [Appendix: Missing options](#appendix-missing-options) if you are not able to see this option.</span></span>  
    1.  <span data-ttu-id="91ff5-333">Haga clic en **Agregar hijo**.</span><span class="sxs-lookup"><span data-stu-id="91ff5-333">Click **Add Child**.</span></span>  <span data-ttu-id="91ff5-334">El código se detiene porque `<li>` se ha agregado un nodo a la lista.</span><span class="sxs-lookup"><span data-stu-id="91ff5-334">The code pauses because a `<li>` node was added to the list.</span></span>  
    1.  <span data-ttu-id="91ff5-335">Haga clic en **reanudar** script de ![ currículo ][ImageResumeScriptIcon] .</span><span class="sxs-lookup"><span data-stu-id="91ff5-335">Click **Resume Script** ![Resume Script][ImageResumeScriptIcon].</span></span>  
    
## <span data-ttu-id="91ff5-336">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="91ff5-336">Next steps</span></span>   

<span data-ttu-id="91ff5-337">Que cubre la mayoría de las características relacionadas con DOM de DevTools.</span><span class="sxs-lookup"><span data-stu-id="91ff5-337">That covers most of the DOM-related features in DevTools.</span></span>  <span data-ttu-id="91ff5-338">Puede descubrir el resto de ellos haciendo clic con el botón secundario en los nodos del árbol DOM y experimentando con las otras opciones que no se han descrito en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="91ff5-338">You are able to discover the rest of them by right-clicking nodes in the DOM Tree and experimenting with the other options that were not covered in this tutorial.</span></span>  <span data-ttu-id="91ff5-339">Consulte también [métodos abreviados de teclado del panel elementos][DevToolsShortcutsElements].</span><span class="sxs-lookup"><span data-stu-id="91ff5-339">See also [Elements panel keyboard shortcuts][DevToolsShortcutsElements].</span></span>  

<span data-ttu-id="91ff5-340">Visite la [Página principal de Microsoft Edge DevTools][MicrosoftEdgeDevTools] para descubrir todo lo que pueda hacer con DevTools.</span><span class="sxs-lookup"><span data-stu-id="91ff5-340">Check out the [Microsoft Edge DevTools homepage][MicrosoftEdgeDevTools] to discover everything else you are able to do with DevTools.</span></span>  

<!--See [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  



## <span data-ttu-id="91ff5-341">Apéndice: HTML frente a DOM</span><span class="sxs-lookup"><span data-stu-id="91ff5-341">Appendix: HTML versus the DOM</span></span>   

<span data-ttu-id="91ff5-342">Esta sección explica rápidamente la diferencia entre HTML y DOM.</span><span class="sxs-lookup"><span data-stu-id="91ff5-342">This section quickly explains the difference between HTML and the DOM.</span></span>  

<span data-ttu-id="91ff5-343">Cuando se usa un explorador Web para solicitar una página, el servidor devuelve HTML como este:</span><span class="sxs-lookup"><span data-stu-id="91ff5-343">When you use a web browser to request a page, the server returns HTML like this:</span></span>  

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

<span data-ttu-id="91ff5-344">El explorador analiza el código HTML y crea un árbol de objetos como este:</span><span class="sxs-lookup"><span data-stu-id="91ff5-344">The browser parses the HTML and creates a tree of objects like this:</span></span>  

```dom
html
  head
    title
  body
    h1
    p
    script
```  

<span data-ttu-id="91ff5-345">Este árbol de objetos, o nodos, que representa el contenido de la página, se denomina DOM.</span><span class="sxs-lookup"><span data-stu-id="91ff5-345">This tree of objects, or nodes, representing the content of the page is called the DOM.</span></span>  <span data-ttu-id="91ff5-346">Ahora es lo mismo que el código HTML, pero Supongamos que la secuencia de comandos a la que se hace referencia en la parte inferior del HTML ejecuta este código:</span><span class="sxs-lookup"><span data-stu-id="91ff5-346">Right now it looks the same as the HTML, but suppose that the script referenced at the bottom of the HTML runs this code:</span></span>  

```javascript
const h1 = document.querySelector('h1');
h1.parentElement.removeChild(h1);
const p = document.createElement('p');
p.textContent = 'Wildcard!';
document.body.appendChild(p);
```  

<span data-ttu-id="91ff5-347">Ese código quita el `h1` nodo y agrega otro `p` nodo al Dom.</span><span class="sxs-lookup"><span data-stu-id="91ff5-347">That code removes the `h1` node and adds another `p` node to the DOM.</span></span>  <span data-ttu-id="91ff5-348">El DOM completo ahora tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="91ff5-348">The complete DOM now looks like this:</span></span>  

```dom
html
  head
    title
  body
    p
    script
    p
```  

<span data-ttu-id="91ff5-349">El código HTML de la página es ahora diferente al del DOM.</span><span class="sxs-lookup"><span data-stu-id="91ff5-349">The HTML for the page is now different than the DOM.</span></span>  <span data-ttu-id="91ff5-350">En otras palabras, HTML representa el contenido inicial de la página y DOM representa el contenido de la página actual.</span><span class="sxs-lookup"><span data-stu-id="91ff5-350">In other words, HTML represents initial page content, and the DOM represents current page content.</span></span>  <span data-ttu-id="91ff5-351">Cuando JavaScript agrega, quita o modifica nodos, el DOM es diferente del HTML.</span><span class="sxs-lookup"><span data-stu-id="91ff5-351">When JavaScript adds, removes, or edits nodes, the DOM becomes different than the HTML.</span></span>  

<span data-ttu-id="91ff5-352">Para obtener más información, consulta [Introducción al Dom][MDNIntroductionToDOM] .</span><span class="sxs-lookup"><span data-stu-id="91ff5-352">See [Introduction to the DOM][MDNIntroductionToDOM] to learn more.</span></span>  

<!--
## Appendix: Scroll into view   

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and select **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    > ##### Figure 19  
    > Scroll into view  
    > ![Scroll into view][ImageScrollView]  
    -->  

## <span data-ttu-id="91ff5-353">Apéndice: opciones perdidas</span><span class="sxs-lookup"><span data-stu-id="91ff5-353">Appendix: Missing options</span></span>   

<span data-ttu-id="91ff5-354">Muchas de las instrucciones de este tutorial le indican que debe hacer clic con el botón secundario del mouse en un nodo del árbol DOM y, a continuación, seleccionar una opción en el menú contextual que aparece.</span><span class="sxs-lookup"><span data-stu-id="91ff5-354">Many of the instructions in this tutorial instruct you to right-click a node in the DOM Tree and then select an option from the context menu that pops up.</span></span>  <span data-ttu-id="91ff5-355">Si no ve la opción especificada en el menú contextual, intente hacer clic con el botón secundario del ratón fuera del texto del nodo.</span><span class="sxs-lookup"><span data-stu-id="91ff5-355">If you do not see the specified option in the context menu, try right-clicking away from the node text.</span></span>  

> ##### <span data-ttu-id="91ff5-356">Ilustración 20</span><span class="sxs-lookup"><span data-stu-id="91ff5-356">Figure 20</span></span>  
> <span data-ttu-id="91ff5-357">Dónde hacer clic si no ve todas las opciones</span><span class="sxs-lookup"><span data-stu-id="91ff5-357">Where to click if you are not seeing all the options</span></span>  
> ![Dónde hacer clic si no ve todas las opciones][ImageNotSeeingAllOptions]  

<!-- image links -->  

[ImageInspectIcon]: /microsoft-edge/devtools-guide-chromium/media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-icon.msft.png  

[ImageInspectingNode]: /microsoft-edge/devtools-guide-chromium/media/dom-glitch-dom-examples-michelangelo-inspect.msft.png "Ilustración 1: inspeccionar un nodo"  
[ImageHighlightingMichelangeloNode]: /microsoft-edge/devtools-guide-chromium/media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png "Ilustración 2: resaltado del nodo Michelangelo"  
[ImageInspect]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-select-element-page-inspect.msft.png "Ilustración 3: el icono de inspección"  
[ImageInspectingRingoNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png "Ilustración 4: inspeccionar el nodo Ringo"  
[ImageInspectingUlNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png "Ilustración 5: inspeccionar el nodo UL"  
[ImageScrollView]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png "Ilustración 6: desplazarse en la vista"  
[ImageHighlightingQuerySearchBar]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-search-nodes-highlight.msft.png "Ilustración 7: resaltado de la consulta en la barra de búsqueda"  
[ImageEditingText]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-content.msft.png "Ilustración 8: edición del texto"  
[ImageEditingNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-attributes-highlighted.msft.png "Ilustración 9: edición del nodo"  
[ImageAddingStyleAttributeNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-attributes-inline-css.msft.png "Ilustración 10: agregar un atributo de estilo al nodo"  
[ImageChangingNodeButton]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-node-type-button.msft.png "Ilustración 11: cambiar el tipo de nodo a botón"  
[ImageDraggingNodeTopList]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-reorder-dom-nodes.msft.png "Ilustración 12: arrastrar el nodo a la parte superior de la lista"  
[ImageNodeDomTreeAfterHidden]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-hide-a-node.msft.png "Ilustración 13: el aspecto del nodo en el árbol DOM después de ocultarlo"  
[ImageFirstConsole]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png "Ilustración 14: el resultado de la primera expresión $0 en la consola"  
[ImageSecondConsole]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png "Ilustración 15: el resultado de la segunda expresión $0 en la consola"  
[ImageResultTemp1]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png "Ilustración 16: el resultado de la expresión temp1"  
[ImageResultCopyJSPath]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png "Ilustración 17: el resultado de la expresión de ruta de la copia JS"  
[ImageBreakAttributeModification]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png "Ilustración 18: interrupciones en las modificaciones de atributos"  
[ImageResumeScript]: /microsoft-edge/devtools-guide-chromium/media/dom-break-attribute-modifications-sources-paused-on.msft.png "Ilustración 19: Dónde reanudar la secuencia de comandos que se ejecuta"  
[ImageNotSeeingAllOptions]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-right-click-right-side.msft.png "Ilustración 20: Dónde hacer clic si no ve todas las opciones"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas de desarrollador de Microsoft Edge \ (cromo \)"  
[DevToolsCssGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Introducción a la visualización y el cambio de CSS"  
[DevToolsShortcutsElements]: /microsoft-edge/devtools-guide-chromium/shortcuts#elements-panel-keyboard-shortcuts "Métodos abreviados de teclado del panel elementos-métodos abreviados de teclado de Microsoft Edge DevTools"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Ejemplo de DOM de DevTools Microsoft Edge (cromo) | Intento"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introducción a DOM | MDN"  

> [!NOTE]
> <span data-ttu-id="91ff5-384">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="91ff5-384">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="91ff5-385">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/dom/index) y está creada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="91ff5-385">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/dom/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="91ff5-387">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="91ff5-387">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

---
title: Referencia de CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 005d2650a1633d49a8c6c2550c4b2c0c2e3f3be6
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601850"
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







# <span data-ttu-id="5b80e-103">Referencia de CSS</span><span class="sxs-lookup"><span data-stu-id="5b80e-103">CSS Reference</span></span>   



<span data-ttu-id="5b80e-104">Descubra nuevos flujos de trabajo en esta referencia completa de las características de Microsoft Edge DevTools relacionadas con la visualización y el cambio de CSS.</span><span class="sxs-lookup"><span data-stu-id="5b80e-104">Discover new workflows in this comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="5b80e-105">Consulte Introducción a la [visualización y el cambio de CSS][DevToolsCSSGetStarted] para conocer los conceptos básicos.</span><span class="sxs-lookup"><span data-stu-id="5b80e-105">See [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted] to learn the basics.</span></span>  

## <span data-ttu-id="5b80e-106">Seleccionar un elemento</span><span class="sxs-lookup"><span data-stu-id="5b80e-106">Select an element</span></span>   

<span data-ttu-id="5b80e-107">El panel **elementos** de DevTools le permite ver o cambiar la CSS de un elemento a la vez.</span><span class="sxs-lookup"><span data-stu-id="5b80e-107">The **Elements** panel of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="5b80e-108">El elemento seleccionado está resaltado en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-108">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="5b80e-109">Los estilos del elemento se muestran en el panel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="5b80e-109">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="5b80e-110">Vea [ver las CSS de un elemento][DevToolsCSSGetStartedTutorial] para obtener un tutorial.</span><span class="sxs-lookup"><span data-stu-id="5b80e-110">See [View the CSS for an element][DevToolsCSSGetStartedTutorial] for a tutorial.</span></span>  

> [!NOTE]
> <span data-ttu-id="5b80e-111">En la [Ilustración 1](#figure-1), el `h1` elemento que está resaltado en el **árbol DOM** es el elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="5b80e-111">In [Figure 1](#figure-1), the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="5b80e-112">A la derecha, los estilos del elemento se muestran en el panel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="5b80e-112">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="5b80e-113">A la izquierda, el elemento se resalta en la ventanilla, pero solo porque el mouse se desplaza en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-113">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

> ##### <span data-ttu-id="5b80e-114">Figura 1</span><span class="sxs-lookup"><span data-stu-id="5b80e-114">Figure 1</span></span>  
> <span data-ttu-id="5b80e-115">Ejemplo de un elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="5b80e-115">An example of a selected element</span></span>  
> ![Ejemplo de un elemento seleccionado][ImageSelectedElement]  

<span data-ttu-id="5b80e-117">Hay muchas maneras de seleccionar un elemento:</span><span class="sxs-lookup"><span data-stu-id="5b80e-117">There are many ways to select an element:</span></span>  

*   <span data-ttu-id="5b80e-118">En su ventanilla, haga clic con el botón derecho en el elemento y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-118">In your viewport, right-click the element and select **Inspect**.</span></span>  
*   <span data-ttu-id="5b80e-119">En DevTools, haga clic en **seleccionar un elemento** , ![ Seleccione un elemento ][ImageSelectAnElementIcon] o pulse `Control` + `Shift` + `C` \ (Windows \) o `Command` + `Shift` + `C` \ (MacOS \) y, a continuación, haga clic en el elemento de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="5b80e-119">In DevTools, click **Select an element** ![Select an element][ImageSelectAnElementIcon] or press `Control`+`Shift`+`C` \(Windows\) or `Command`+`Shift`+`C` \(macOS\), and then click the element in the viewport.</span></span>  
*   <span data-ttu-id="5b80e-120">En DevTools, haga clic en el elemento del **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-120">In DevTools, click the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="5b80e-121">En DevTools, ejecute una consulta como `document.querySelector('p')` en la **consola**, haga clic con el botón derecho en el resultado y, a continuación, seleccione **Mostrar en el panel elementos**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-121">In DevTools, run a query like `document.querySelector('p')` in the **Console**, right-click the result, and then select **Reveal in Elements panel**.</span></span>  

## <span data-ttu-id="5b80e-122">Ver CSS</span><span class="sxs-lookup"><span data-stu-id="5b80e-122">View CSS</span></span>   

### <span data-ttu-id="5b80e-123">Ver la hoja de estilos externa donde se define una regla</span><span class="sxs-lookup"><span data-stu-id="5b80e-123">View the external stylesheet where a rule is defined</span></span>   

<span data-ttu-id="5b80e-124">En el panel **estilos** , haga clic en el vínculo junto a una regla CSS para abrir la hoja de estilos externa que define la regla.</span><span class="sxs-lookup"><span data-stu-id="5b80e-124">In the **Styles** pane, click the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  

<span data-ttu-id="5b80e-125">Si la hoja de estilos es minified, vea [hacer que un archivo minified sea legible][DevToolsJavascriptReferenceFormat].</span><span class="sxs-lookup"><span data-stu-id="5b80e-125">If the stylesheet is minified, see [Make a minified file readable][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="5b80e-126">En la [ilustración 2](#figure-2), al hacer clic se `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` le lleva a la línea 2 de `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , donde `.content h1:first-of-type` se define la regla CSS.</span><span class="sxs-lookup"><span data-stu-id="5b80e-126">In [Figure 2](#figure-2), clicking `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` takes you to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

> ##### <span data-ttu-id="5b80e-127">Figura 2</span><span class="sxs-lookup"><span data-stu-id="5b80e-127">Figure 2</span></span>  
> <span data-ttu-id="5b80e-128">Ver la hoja de estilos donde se define una regla</span><span class="sxs-lookup"><span data-stu-id="5b80e-128">Viewing the stylesheet where a rule is defined</span></span>  
> ![Ver la hoja de estilos donde se define una regla][ImageViewRuleStylesheet]  

### <span data-ttu-id="5b80e-130">Ver solo la CSS que se aplica realmente a un elemento</span><span class="sxs-lookup"><span data-stu-id="5b80e-130">View only the CSS that is actually applied to an element</span></span>   

<span data-ttu-id="5b80e-131">La pestaña **estilos** muestra todas las reglas que se aplican a un elemento, incluidas las declaraciones que se han reemplazado.</span><span class="sxs-lookup"><span data-stu-id="5b80e-131">The **Styles** tab shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="5b80e-132">Si no está interesado en las declaraciones reemplazadas, use la pestaña **calculada** para ver solo la CSS que se está aplicando realmente a un elemento.</span><span class="sxs-lookup"><span data-stu-id="5b80e-132">When you are not interested in overridden declarations, use the **Computed** tab to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="5b80e-133">[Seleccione un elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5b80e-133">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5b80e-134">Vaya a la pestaña **calculada** en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="5b80e-134">Go to the **Computed** tab in the **Elements** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="5b80e-135">En una ventana de DevTools ancha, la pestaña **calculada** no existe.</span><span class="sxs-lookup"><span data-stu-id="5b80e-135">On a wide DevTools window, the **Computed** tab does not exist.</span></span>  <span data-ttu-id="5b80e-136">El contenido de la pestaña **calculada** se muestra en la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="5b80e-136">The contents of the **Computed** tab are shown on the **Styles** tab.</span></span>  

<span data-ttu-id="5b80e-137">Las propiedades heredadas son opacas.</span><span class="sxs-lookup"><span data-stu-id="5b80e-137">Inherited properties are opaque.</span></span>  <span data-ttu-id="5b80e-138">Active la casilla **Mostrar todo** para ver todos los valores heredados.</span><span class="sxs-lookup"><span data-stu-id="5b80e-138">Check the **Show All** checkbox to see all inherited values.</span></span>  

> [!NOTE]
> <span data-ttu-id="5b80e-139">En la [figura 3](#figure-3), la pestaña **calculada** muestra las propiedades de CSS que se están aplicando al elemento actualmente seleccionado `h1` .</span><span class="sxs-lookup"><span data-stu-id="5b80e-139">In [Figure 3](#figure-3), the **Computed** tab shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

> ##### <span data-ttu-id="5b80e-140">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="5b80e-140">Figure 3</span></span>  
> <span data-ttu-id="5b80e-141">La pestaña **calculada**</span><span class="sxs-lookup"><span data-stu-id="5b80e-141">The **Computed** tab</span></span>  
> ![La pestaña calculada][ImageComputedTab]  

### <span data-ttu-id="5b80e-143">Ver las propiedades de CSS por orden alfabético</span><span class="sxs-lookup"><span data-stu-id="5b80e-143">View CSS properties in alphabetical order</span></span>   

<span data-ttu-id="5b80e-144">Use la pestaña **calculada** .  Vea [ver solo la CSS que se aplica realmente a un elemento](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="5b80e-144">Use the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="5b80e-145">Ver las propiedades heredadas de CSS</span><span class="sxs-lookup"><span data-stu-id="5b80e-145">View inherited CSS properties</span></span>   

<span data-ttu-id="5b80e-146">Active la casilla **Mostrar todo** en la pestaña **calculada** .  Vea [ver solo la CSS que se aplica realmente a un elemento](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="5b80e-146">Check the **Show All** checkbox in the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="5b80e-147">Ver el modelo de cuadro de un elemento</span><span class="sxs-lookup"><span data-stu-id="5b80e-147">View the box model for an element</span></span>   

<span data-ttu-id="5b80e-148">Para ver [el modelo de cuadro][MDNBoxModel] de un elemento, vaya a la pestaña **estilos** .  Si la ventana de DevTools es estrecha, el diagrama de **modelo de cuadro** se encuentra en la parte inferior de la pestaña.</span><span class="sxs-lookup"><span data-stu-id="5b80e-148">To view [the box model][MDNBoxModel] of an element, go to the **Styles** tab.  If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the tab.</span></span>  

<span data-ttu-id="5b80e-149">Para cambiar un valor, haga doble clic en él.</span><span class="sxs-lookup"><span data-stu-id="5b80e-149">To change a value, double-click on it.</span></span>  

> [!NOTE]
> <span data-ttu-id="5b80e-150">En la [figura 4](#figure-4), el diagrama de **modelo de cuadro** de la pestaña **estilos** muestra el modelo de cuadro para el elemento seleccionado actualmente `h1` .</span><span class="sxs-lookup"><span data-stu-id="5b80e-150">In [Figure 4](#figure-4), the **Box Model** diagram in the **Styles** tab shows the box model for the currently selected `h1` element.</span></span>  

> ##### <span data-ttu-id="5b80e-151">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="5b80e-151">Figure 4</span></span>  
> <span data-ttu-id="5b80e-152">El diagrama de **modelo de cuadro**</span><span class="sxs-lookup"><span data-stu-id="5b80e-152">The **Box Model** diagram</span></span>  
> ![El diagrama de modelo de cuadro][ImageBoxModel]  

### <span data-ttu-id="5b80e-154">Buscar y filtrar la CSS de un elemento</span><span class="sxs-lookup"><span data-stu-id="5b80e-154">Search and filter the CSS of an element</span></span>   

<span data-ttu-id="5b80e-155">Use el cuadro de texto **filtrar** en los **estilos** y las pestañas **calculadas** para buscar propiedades o valores específicos de CSS.</span><span class="sxs-lookup"><span data-stu-id="5b80e-155">Use the **Filter** text box on the **Styles** and **Computed** tabs to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="5b80e-156">Para buscar también las propiedades heredadas en la pestaña **calculada** , active la casilla **Mostrar todo** .</span><span class="sxs-lookup"><span data-stu-id="5b80e-156">To also search inherited properties in the **Computed** tab, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="5b80e-157">En la [figura 5](#figure-5), la pestaña **estilos** se filtra para mostrar únicamente las reglas que incluyen la consulta de búsqueda `color` .</span><span class="sxs-lookup"><span data-stu-id="5b80e-157">In [Figure 5](#figure-5), the **Styles** tab is filtered to only show rules that include the search query `color`.</span></span>  

> ##### <span data-ttu-id="5b80e-158">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="5b80e-158">Figure 5</span></span>  
> <span data-ttu-id="5b80e-159">Filtrar la pestaña **estilos**</span><span class="sxs-lookup"><span data-stu-id="5b80e-159">Filtering the **Styles** tab</span></span>  
> ![Filtrar la pestaña estilos][ImageStylesFilter]  

> [!NOTE]
> <span data-ttu-id="5b80e-161">En la [figura 6](#figure-6), la pestaña **calculada** se filtra para mostrar únicamente las declaraciones que incluyen la consulta de búsqueda `100%` .</span><span class="sxs-lookup"><span data-stu-id="5b80e-161">In [Figure 6](#figure-6), the **Computed** tab is filtered to only show declarations that include the search query `100%`.</span></span>  

> ##### <span data-ttu-id="5b80e-162">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="5b80e-162">Figure 6</span></span>  
> <span data-ttu-id="5b80e-163">Filtrar la pestaña **calculada**</span><span class="sxs-lookup"><span data-stu-id="5b80e-163">Filtering the **Computed** tab</span></span>  
> ![Filtrar la pestaña calculada][ImageComputerFilter]  

### <span data-ttu-id="5b80e-165">Alternar una seudoclase</span><span class="sxs-lookup"><span data-stu-id="5b80e-165">Toggle a pseudo-class</span></span>   

<span data-ttu-id="5b80e-166">Para alternar una seudoclase como,, `:active` `:focus` `:hover` o `:visited` :</span><span class="sxs-lookup"><span data-stu-id="5b80e-166">To toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`:</span></span>  

1.  <span data-ttu-id="5b80e-167">[Seleccione un elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5b80e-167">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5b80e-168">En el panel **elementos** , vaya a la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="5b80e-168">On the **Elements** panel, go to the **Styles** tab.</span></span>  
1.  <span data-ttu-id="5b80e-169">Haga clic en **: HOV**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-169">Click **:hov**.</span></span>  
1.  <span data-ttu-id="5b80e-170">Compruebe la pseudo-clase que desea habilitar.</span><span class="sxs-lookup"><span data-stu-id="5b80e-170">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="5b80e-171">En la [figura 7](#figure-7), alterne la `:hover` pseudo-clase.</span><span class="sxs-lookup"><span data-stu-id="5b80e-171">In [Figure 7](#figure-7), toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="5b80e-172">En la ventanilla, compruebe que la `background-color: cornflowerblue` declaración se aplica al elemento, aunque no se esté colocando el elemento en realidad.</span><span class="sxs-lookup"><span data-stu-id="5b80e-172">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

> ##### <span data-ttu-id="5b80e-173">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="5b80e-173">Figure 7</span></span>  
> <span data-ttu-id="5b80e-174">Alternar la `:hover` pseudo-clase</span><span class="sxs-lookup"><span data-stu-id="5b80e-174">Toggling the `:hover` pseudo-class</span></span>  
> ![Alternar la seudoclase: hover][ImagePseudoClass]  

<span data-ttu-id="5b80e-176">Consulte [Agregar un PseudoState a una clase][DevToolsCSSGetStartedAddPseudoState] para obtener un tutorial interactivo.</span><span class="sxs-lookup"><span data-stu-id="5b80e-176">See [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState] for an interactive tutorial.</span></span> 

### <span data-ttu-id="5b80e-177">Ver una página en modo de impresión</span><span class="sxs-lookup"><span data-stu-id="5b80e-177">View a page in print mode</span></span>   

<span data-ttu-id="5b80e-178">Para ver una página en modo impresión:</span><span class="sxs-lookup"><span data-stu-id="5b80e-178">To view a page in print mode:</span></span>  

1.  <span data-ttu-id="5b80e-179">[Abrir el menú de comandos][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="5b80e-179">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="5b80e-180">Empiece `Rendering` a escribir y seleccione `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="5b80e-180">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="5b80e-181">Para la lista desplegable **emular multimedia de CSS** , seleccione **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-181">For the **Emulate CSS Media** dropdown, select **print**.</span></span>  

### <span data-ttu-id="5b80e-182">Ver las CSS usadas y sin usar con la pestaña cobertura</span><span class="sxs-lookup"><span data-stu-id="5b80e-182">View used and unused CSS with the Coverage tab</span></span>   

<span data-ttu-id="5b80e-183">La pestaña cobertura le muestra qué CSS usa una página en realidad.</span><span class="sxs-lookup"><span data-stu-id="5b80e-183">The Coverage tab shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="5b80e-184">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) mientras DevTools el foco para abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="5b80e-184">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to open the Command Menu.</span></span>  
1.  <span data-ttu-id="5b80e-185">Empiece `coverage` a escribir y seleccione **Mostrar cobertura**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-185">Start typing `coverage` and select **Show Coverage**.</span></span>  <span data-ttu-id="5b80e-186">Aparece la ficha cobertura.</span><span class="sxs-lookup"><span data-stu-id="5b80e-186">The Coverage tab appears.</span></span>  
    
    > ##### <span data-ttu-id="5b80e-187">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="5b80e-187">Figure 8</span></span>  
    > <span data-ttu-id="5b80e-188">Abrir la ficha cobertura desde el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="5b80e-188">Opening the Coverage tab from the Command Menu</span></span>  
    > ![Abrir la ficha cobertura desde el menú de comandos][ImageCommandMenu]  
    
    > ##### <span data-ttu-id="5b80e-190">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="5b80e-190">Figure 9</span></span>  
    > <span data-ttu-id="5b80e-191">La ficha cobertura</span><span class="sxs-lookup"><span data-stu-id="5b80e-191">The Coverage tab</span></span>  
    > ![La ficha cobertura][ImageCoverageEmpty]  
    
1.  <span data-ttu-id="5b80e-193">Haga clic en **iniciar cobertura de instrumentación y actualice la página** ![ comenzar la cobertura de la instrumentación y actualice la página ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="5b80e-193">Click **Start instrumenting coverage and refresh the page** ![Start instrumenting coverage and refresh the page][ImageRefreshIcon].</span></span>  <span data-ttu-id="5b80e-194">La página se actualiza y la pestaña cobertura proporciona una descripción general de la cantidad de CSS \ (y JavaScript \) que se usa en cada archivo que carga el explorador.</span><span class="sxs-lookup"><span data-stu-id="5b80e-194">The page refreshes and the Coverage tab provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="5b80e-195">El verde representa CSS usado.</span><span class="sxs-lookup"><span data-stu-id="5b80e-195">Green represents used CSS.</span></span>  <span data-ttu-id="5b80e-196">Rojo representa un CSS no usado.</span><span class="sxs-lookup"><span data-stu-id="5b80e-196">Red represents unused CSS.</span></span>  
    
    > ##### <span data-ttu-id="5b80e-197">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="5b80e-197">Figure 10</span></span>  
    > <span data-ttu-id="5b80e-198">Información general sobre la cantidad de CSS (y JavaScript) que se usa y que no se usa</span><span class="sxs-lookup"><span data-stu-id="5b80e-198">An overview of how much CSS (and JavaScript) is used and unused</span></span>  
    > ![Información general sobre la cantidad de CSS (y JavaScript) que se usa y que no se usa][ImageCoverageOverview]  

1.  <span data-ttu-id="5b80e-200">Haga clic en un archivo CSS para ver un desglose línea por línea de qué usa CSS.</span><span class="sxs-lookup"><span data-stu-id="5b80e-200">Click a CSS file to see a line-by-line breakdown of what CSS it uses.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5b80e-201">En la [ilustración 11](#figure-11), las líneas 145 a 147 y 149 a 151 de `b66bc881.site-ltr.css` no se usan, mientras que las líneas 163 a 166 se usan.</span><span class="sxs-lookup"><span data-stu-id="5b80e-201">In [Figure 11](#figure-11), lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    > ##### <span data-ttu-id="5b80e-202">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="5b80e-202">Figure 11</span></span>  
    > <span data-ttu-id="5b80e-203">Un desglose línea a línea de CSS utilizadas y sin usar</span><span class="sxs-lookup"><span data-stu-id="5b80e-203">A line-by-line breakdown of used and unused CSS</span></span>  
    > ![Un desglose línea a línea de CSS utilizadas y sin usar][ImageCoverageDetail]  
    
### <span data-ttu-id="5b80e-205">Forzar el modo vista previa de impresión</span><span class="sxs-lookup"><span data-stu-id="5b80e-205">Force print preview mode</span></span>   

<span data-ttu-id="5b80e-206">Consulte [forzar DevTools en el modo de vista previa de impresión][DevToolsCssPrintPreview].</span><span class="sxs-lookup"><span data-stu-id="5b80e-206">See [Force DevTools Into Print Preview Mode][DevToolsCssPrintPreview].</span></span>  

## <span data-ttu-id="5b80e-207">Cambiar CSS</span><span class="sxs-lookup"><span data-stu-id="5b80e-207">Change CSS</span></span>   

<!-- todo s/CSS declaration/declaration/ -->  

### <span data-ttu-id="5b80e-208">Agregar una declaración CSS a un elemento</span><span class="sxs-lookup"><span data-stu-id="5b80e-208">Add a CSS declaration to an element</span></span>   

<span data-ttu-id="5b80e-209">Dado que el orden de las declaraciones afecta a la forma en que se aplica el estilo de un elemento, puede Agregar declaraciones de varias maneras:</span><span class="sxs-lookup"><span data-stu-id="5b80e-209">Since the order of declarations affects how an element is styled, you may add declarations in different ways:</span></span>  

*   <span data-ttu-id="5b80e-210">[Agregue una declaración en línea](#add-an-inline-declaration).</span><span class="sxs-lookup"><span data-stu-id="5b80e-210">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="5b80e-211">Es equivalente a agregar un `style` atributo al código HTML de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5b80e-211">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="5b80e-212">[Agregue una declaración a una regla de estilo](#add-a-declaration-to-a-style-rule).</span><span class="sxs-lookup"><span data-stu-id="5b80e-212">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="5b80e-213">¿Qué flujo de trabajo debe usar?</span><span class="sxs-lookup"><span data-stu-id="5b80e-213">What workflow should you use?</span></span>** <span data-ttu-id="5b80e-214">En la mayoría de los casos, probablemente quieras usar el flujo de trabajo de declaración en línea.</span><span class="sxs-lookup"><span data-stu-id="5b80e-214">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="5b80e-215">Las declaraciones en línea tienen una mayor especificidad que las externas, por lo que el flujo de trabajo insertado garantiza que los cambios se apliquen en el elemento como cabría esperar.</span><span class="sxs-lookup"><span data-stu-id="5b80e-215">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in the element as you would expect.</span></span>  <span data-ttu-id="5b80e-216">Para obtener más información sobre la especificidad, consulta [tipos de selector][MDNSelectorTypes] .</span><span class="sxs-lookup"><span data-stu-id="5b80e-216">See [Selector Types][MDNSelectorTypes] for more on specificity.</span></span>  

<span data-ttu-id="5b80e-217">Si depura cualquier estilo del elemento y necesita comprobar específicamente lo que ocurre cuando se define una declaración en distintos lugares, use el otro flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="5b80e-217">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <span data-ttu-id="5b80e-218">Agregar una declaración en línea</span><span class="sxs-lookup"><span data-stu-id="5b80e-218">Add an inline declaration</span></span>   

<span data-ttu-id="5b80e-219">Para agregar una declaración en línea:</span><span class="sxs-lookup"><span data-stu-id="5b80e-219">To add an inline declaration:</span></span>  

1.  <span data-ttu-id="5b80e-220">[Seleccione un elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5b80e-220">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5b80e-221">En el panel **estilos** , haga clic entre los corchetes del **elemento. sección Style** .</span><span class="sxs-lookup"><span data-stu-id="5b80e-221">In the **Styles** pane, click between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="5b80e-222">El cursor se centra, lo que le permite escribir texto.</span><span class="sxs-lookup"><span data-stu-id="5b80e-222">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="5b80e-223">Escriba un nombre de propiedad y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5b80e-223">Enter a property name and press `Enter`.</span></span>  
1.  <span data-ttu-id="5b80e-224">Escriba un valor válido para esa propiedad y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5b80e-224">Enter a valid value for that property and press `Enter`.</span></span>  <span data-ttu-id="5b80e-225">En el **árbol DOM**, compruebe que se ha `style` agregado un atributo al elemento.</span><span class="sxs-lookup"><span data-stu-id="5b80e-225">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="5b80e-226">En la [figura 12](#figure-12), `margin-top` `background-color` se han aplicado las propiedades y al elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="5b80e-226">In [Figure 12](#figure-12), the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="5b80e-227">En el **árbol DOM** , compruebe que las declaraciones se reflejan en el `style` atributo de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5b80e-227">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

> ##### <span data-ttu-id="5b80e-228">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="5b80e-228">Figure 12</span></span>  
> <span data-ttu-id="5b80e-229">Agregar declaraciones en línea</span><span class="sxs-lookup"><span data-stu-id="5b80e-229">Adding inline declarations</span></span>  
> ![Agregar declaraciones en línea][ImageInlineDeclarations]  

#### <span data-ttu-id="5b80e-231">Agregar una declaración a una regla de estilo</span><span class="sxs-lookup"><span data-stu-id="5b80e-231">Add a declaration to a style rule</span></span>   

<span data-ttu-id="5b80e-232">Para agregar una declaración a una regla de estilo existente:</span><span class="sxs-lookup"><span data-stu-id="5b80e-232">To add a declaration to an existing style rule:</span></span>  

1.  <span data-ttu-id="5b80e-233">[Seleccione un elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5b80e-233">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5b80e-234">En el panel **estilos** , haga clic entre los corchetes de la regla de estilo a los que desea agregar la declaración.</span><span class="sxs-lookup"><span data-stu-id="5b80e-234">In the **Styles** pane, click between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="5b80e-235">El cursor se centra, lo que le permite escribir texto.</span><span class="sxs-lookup"><span data-stu-id="5b80e-235">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="5b80e-236">Escriba un nombre de propiedad y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5b80e-236">Enter a property name and press `Enter`.</span></span>  
1.  <span data-ttu-id="5b80e-237">Escriba un valor válido para esa propiedad y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5b80e-237">Enter a valid value for that property and press `Enter`.</span></span>  

> ##### <span data-ttu-id="5b80e-238">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="5b80e-238">Figure 13</span></span>  
> <span data-ttu-id="5b80e-239">Agregar la `border-bottom-style:groove` declaración a una regla de estilo</span><span class="sxs-lookup"><span data-stu-id="5b80e-239">Adding the `border-bottom-style:groove` declaration to a style rule</span></span>  
> ![Agregar una declaración a una regla de estilo][ImageAddDeclarationExistingRule]  

### <span data-ttu-id="5b80e-241">Cambiar un nombre o valor de declaración</span><span class="sxs-lookup"><span data-stu-id="5b80e-241">Change a declaration name or value</span></span>   

<span data-ttu-id="5b80e-242">Haga doble clic en el nombre o valor de una declaración para cambiarlo.</span><span class="sxs-lookup"><span data-stu-id="5b80e-242">Double-click the name or value of a declaration to change it.</span></span>  <span data-ttu-id="5b80e-243">Vea [cambiar valores de declaración con métodos abreviados de teclado](#change-declaration-values-with-keyboard-shortcuts) para métodos abreviados para aumentar o disminuir rápidamente un valor por `0.1` `1` unidades,, `10` o `100` .</span><span class="sxs-lookup"><span data-stu-id="5b80e-243">See [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts) for shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units.</span></span>  

> ##### <span data-ttu-id="5b80e-244">Imagen 14</span><span class="sxs-lookup"><span data-stu-id="5b80e-244">Figure 14</span></span>  
> <span data-ttu-id="5b80e-245">Cambiar el valor de la</span><span class="sxs-lookup"><span data-stu-id="5b80e-245">Changing the value of the</span></span> `border-bottom-style`  
> ![Cambiar el valor de una declaración][ImageAddDeclarationExistingRule2]  

### <span data-ttu-id="5b80e-247">Cambiar los valores de declaración con métodos abreviados de teclado</span><span class="sxs-lookup"><span data-stu-id="5b80e-247">Change declaration values with keyboard shortcuts</span></span>   

<span data-ttu-id="5b80e-248">Al editar el valor de una declaración, puede usar los siguientes métodos abreviados de teclado para incrementar el valor en una cantidad fija:</span><span class="sxs-lookup"><span data-stu-id="5b80e-248">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a fixed amount:</span></span>  

*   <span data-ttu-id="5b80e-249">Pulsa `Alt` + `Up` \ (Windows \) o `Option` + `Up` \ (MacOS \) para incrementar `0.1` .</span><span class="sxs-lookup"><span data-stu-id="5b80e-249">Press `Alt`+`Up` \(Windows\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="5b80e-250">Pulse `Up` para cambiar el valor por `1` , o bien, `0.1` si el valor actual está comprendido entre `-1` y `1` .</span><span class="sxs-lookup"><span data-stu-id="5b80e-250">Press `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="5b80e-251">Pulsa `Shift` + `Up` para incrementar `10` .</span><span class="sxs-lookup"><span data-stu-id="5b80e-251">Press `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="5b80e-252">Pulse `Shift` + `Page Up` \ (Windows \) o `Shift` + `Command` + `Up` \ (MacOS \) para incrementar el valor `100` .</span><span class="sxs-lookup"><span data-stu-id="5b80e-252">Press `Shift`+`Page Up` \(Windows\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="5b80e-253">También funciona la reducción.</span><span class="sxs-lookup"><span data-stu-id="5b80e-253">Decrementing also works.</span></span>  <span data-ttu-id="5b80e-254">Solo tiene que reemplazar cada instancia de la `Up` mencionada anteriormente con `Down` .</span><span class="sxs-lookup"><span data-stu-id="5b80e-254">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <span data-ttu-id="5b80e-255">Agregar una clase a un elemento</span><span class="sxs-lookup"><span data-stu-id="5b80e-255">Add a class to an element</span></span>   

<span data-ttu-id="5b80e-256">Para agregar una clase a un elemento:</span><span class="sxs-lookup"><span data-stu-id="5b80e-256">To add a class to an element:</span></span>  

1.  <span data-ttu-id="5b80e-257">[Seleccione el elemento](#select-an-element) en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-257">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="5b80e-258">Haga clic en **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-258">Click **.cls**.</span></span>  
1.  <span data-ttu-id="5b80e-259">Escriba el nombre de la clase en el cuadro de texto **Agregar nueva clase** .</span><span class="sxs-lookup"><span data-stu-id="5b80e-259">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="5b80e-260">Presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="5b80e-260">Press `Enter`.</span></span>  

> ##### <span data-ttu-id="5b80e-261">Imagen 15</span><span class="sxs-lookup"><span data-stu-id="5b80e-261">Figure 15</span></span>  
> <span data-ttu-id="5b80e-262">Panel **clases de elementos**</span><span class="sxs-lookup"><span data-stu-id="5b80e-262">The **Element Classes** pane</span></span>  
> ![Panel clases de elementos][ImageElementClasses]  

### <span data-ttu-id="5b80e-264">Activar o desactivar una clase</span><span class="sxs-lookup"><span data-stu-id="5b80e-264">Toggle a class</span></span>   

<span data-ttu-id="5b80e-265">Para habilitar o deshabilitar una clase en un elemento:</span><span class="sxs-lookup"><span data-stu-id="5b80e-265">To enable or disable a class on an element:</span></span>  

1.  <span data-ttu-id="5b80e-266">[Seleccione el elemento](#select-an-element) en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-266">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="5b80e-267">Abra el panel **clases de elementos** .</span><span class="sxs-lookup"><span data-stu-id="5b80e-267">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="5b80e-268">Vea [Agregar una clase a un elemento](#add-a-class-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="5b80e-268">See [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="5b80e-269">Debajo del cuadro de texto **Agregar nueva clase** se encuentran todas las clases que se están aplicando a este elemento.</span><span class="sxs-lookup"><span data-stu-id="5b80e-269">Below the **Add New Class** text box are all of the classes that are being applied to this element.</span></span>  
1.  <span data-ttu-id="5b80e-270">Active la casilla situada junto a la clase que desea habilitar o deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="5b80e-270">Toggle the checkbox next to the class that you want to enable or disable.</span></span>  

### <span data-ttu-id="5b80e-271">Agregar una regla de estilo</span><span class="sxs-lookup"><span data-stu-id="5b80e-271">Add a style rule</span></span>   

<span data-ttu-id="5b80e-272">Para agregar una nueva regla de estilo:</span><span class="sxs-lookup"><span data-stu-id="5b80e-272">To add a new style rule:</span></span>  

1.  <span data-ttu-id="5b80e-273">[Seleccione un elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5b80e-273">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5b80e-274">Haga clic en **nueva regla de estilo** nueva ![ regla de estilo ][ImageNewStyleRuleIcon] .</span><span class="sxs-lookup"><span data-stu-id="5b80e-274">Click **New Style Rule** ![New Style Rule][ImageNewStyleRuleIcon].</span></span>  <span data-ttu-id="5b80e-275">DevTools inserta una nueva regla debajo del **elemento.** regla de estilo.</span><span class="sxs-lookup"><span data-stu-id="5b80e-275">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="5b80e-276">En la [figura 16](#figure-16), DevTools agrega la `h1.devsite-page-title` regla de estilo después de hacer clic en **nueva regla de estilo**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-276">In [Figure 16](#figure-16), DevTools adds the `h1.devsite-page-title` style rule after clicking **New Style Rule**.</span></span>  

> ##### <span data-ttu-id="5b80e-277">Imagen 16</span><span class="sxs-lookup"><span data-stu-id="5b80e-277">Figure 16</span></span>  
> <span data-ttu-id="5b80e-278">Agregar una nueva regla de estilo</span><span class="sxs-lookup"><span data-stu-id="5b80e-278">Adding a new style rule</span></span>  
> ![Agregar una nueva regla de estilo][ImageStyleRule]  

#### <span data-ttu-id="5b80e-280">Elegir la hoja de estilos a la que se va a agregar una regla</span><span class="sxs-lookup"><span data-stu-id="5b80e-280">Choose which stylesheet to add a rule to</span></span>   

<span data-ttu-id="5b80e-281">Al [Agregar una nueva regla de estilo](#add-a-style-rule), haga clic en nueva regla **de estilo Nueva** regla de estilo ![ ][ImageNewStyleRuleIcon] para elegir la hoja de estilos a la que desea agregar la regla de estilo.</span><span class="sxs-lookup"><span data-stu-id="5b80e-281">When [adding a new style rule](#add-a-style-rule), click and hold **New Style Rule** ![New Style Rule][ImageNewStyleRuleIcon] to choose which stylesheet to add the style rule to.</span></span>  

> ##### <span data-ttu-id="5b80e-282">Imagen 17</span><span class="sxs-lookup"><span data-stu-id="5b80e-282">Figure 17</span></span>  
> <span data-ttu-id="5b80e-283">Elegir una hoja de estilos</span><span class="sxs-lookup"><span data-stu-id="5b80e-283">Choosing a stylesheet</span></span>  
> ![Elegir una hoja de estilos][ImageChooseStylesheet]  

#### <span data-ttu-id="5b80e-285">Agregar una regla de estilo a una ubicación específica</span><span class="sxs-lookup"><span data-stu-id="5b80e-285">Add a style rule to a specific location</span></span>   

<span data-ttu-id="5b80e-286">Para agregar una regla de estilo a una ubicación específica en la pestaña **estilos** :</span><span class="sxs-lookup"><span data-stu-id="5b80e-286">To add a style rule to a specific location in the **Styles** tab:</span></span>  

1.  <span data-ttu-id="5b80e-287">Desplace el puntero sobre la regla de estilo que está justo encima del lugar donde desea agregar la nueva regla de estilo.</span><span class="sxs-lookup"><span data-stu-id="5b80e-287">Hover over the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="5b80e-288">[Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5b80e-288">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5b80e-289">Haga clic en **Insertar regla de estilo debajo** de ![ Insertar regla de estilo ][ImageNewStyleRuleIcon] .</span><span class="sxs-lookup"><span data-stu-id="5b80e-289">Click **Insert Style Rule Below** ![Insert Style Rule Below][ImageNewStyleRuleIcon].</span></span>  

> ##### <span data-ttu-id="5b80e-290">Ilustración 18</span><span class="sxs-lookup"><span data-stu-id="5b80e-290">Figure 18</span></span>  
> **<span data-ttu-id="5b80e-291">Insertar regla de estilo a continuación</span><span class="sxs-lookup"><span data-stu-id="5b80e-291">Insert Style Rule Below</span></span>**  
> ![Insertar regla de estilo a continuación][ImageInsertStyleRuleBelow]  

### <span data-ttu-id="5b80e-293">Mostrar la barra de herramientas más acciones</span><span class="sxs-lookup"><span data-stu-id="5b80e-293">Reveal the More Actions toolbar</span></span>   

<span data-ttu-id="5b80e-294">La barra de herramientas **más acciones** le permite:</span><span class="sxs-lookup"><span data-stu-id="5b80e-294">The **More Actions** toolbar lets you:</span></span>  

*   <span data-ttu-id="5b80e-295">Inserte una regla de estilo directamente debajo de la que se le está concentrando.</span><span class="sxs-lookup"><span data-stu-id="5b80e-295">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="5b80e-296">Agregue una `background-color` `color` declaración, `box-shadow` o `text-shadow` a la regla de estilo en la que se concentra.</span><span class="sxs-lookup"><span data-stu-id="5b80e-296">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="5b80e-297">Para mostrar la barra de herramientas **más acciones** :</span><span class="sxs-lookup"><span data-stu-id="5b80e-297">To reveal the **More Actions** toolbar:</span></span>  

1.  <span data-ttu-id="5b80e-298">En la pestaña **estilos** , desplace el puntero sobre una regla de estilo.</span><span class="sxs-lookup"><span data-stu-id="5b80e-298">In the **Styles** tab, hover over a style rule.</span></span>  <span data-ttu-id="5b80e-299">**Más acciones** `...` se revela en la parte inferior derecha de la sección regla de estilo.</span><span class="sxs-lookup"><span data-stu-id="5b80e-299">**More Actions** `...` is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5b80e-300">En la [Ilustración 19](#figure-19), desplace el puntero sobre la `.header-holder.has-default-focus` regla de estilo y se revela **más acciones** en la parte inferior derecha de la sección regla de estilo.</span><span class="sxs-lookup"><span data-stu-id="5b80e-300">In [Figure 19](#figure-19), hover over the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    > ##### <span data-ttu-id="5b80e-301">Ilustración 19</span><span class="sxs-lookup"><span data-stu-id="5b80e-301">Figure 19</span></span>  
    > <span data-ttu-id="5b80e-302">Mostrar **más acciones**</span><span class="sxs-lookup"><span data-stu-id="5b80e-302">Revealing **More Actions**</span></span>  
    > ![Mostrar más acciones][ImageRevealMore]  
    
1.  <span data-ttu-id="5b80e-304">Mantenga el mouse sobre **más acciones** `...` para mostrar las acciones mencionadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5b80e-304">Hover over **More Actions** `...` to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5b80e-305">La acción **Insertar regla de estilo se muestra** después de mantener el mouse sobre **más acciones**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-305">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    > ##### <span data-ttu-id="5b80e-306">Ilustración 20</span><span class="sxs-lookup"><span data-stu-id="5b80e-306">Figure 20</span></span>  
    > <span data-ttu-id="5b80e-307">La barra de herramientas **más acciones**</span><span class="sxs-lookup"><span data-stu-id="5b80e-307">The **More Actions** toolbar</span></span>  
    > ![La barra de herramientas más acciones][ImageInsertStyleRuleBelow2]  
    
### <span data-ttu-id="5b80e-309">Activar o desactivar una declaración</span><span class="sxs-lookup"><span data-stu-id="5b80e-309">Toggle a declaration</span></span>   

<span data-ttu-id="5b80e-310">Para activar o desactivar una única declaración:</span><span class="sxs-lookup"><span data-stu-id="5b80e-310">To toggle a single declaration on or off:</span></span>  

1.  <span data-ttu-id="5b80e-311">[Seleccione un elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5b80e-311">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5b80e-312">En el panel **estilos** , desplace el puntero sobre la regla que define la declaración.</span><span class="sxs-lookup"><span data-stu-id="5b80e-312">In the **Styles** pane, hover over the rule that defines the declaration.</span></span>  <span data-ttu-id="5b80e-313">Las casillas aparecerán junto a cada declaración.</span><span class="sxs-lookup"><span data-stu-id="5b80e-313">Checkboxes appear next to each declaration.</span></span>  
1.  <span data-ttu-id="5b80e-314">Active o desactive la casilla situada junto a la declaración.</span><span class="sxs-lookup"><span data-stu-id="5b80e-314">Check or uncheck the checkbox next to the declaration.</span></span>  <span data-ttu-id="5b80e-315">Al desactivar una declaración, DevTools la cruza para indicar que ya no está activa.</span><span class="sxs-lookup"><span data-stu-id="5b80e-315">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="5b80e-316">En la [figura 21](#figure-21), la `margin-top` propiedad del elemento seleccionado está desactivada.</span><span class="sxs-lookup"><span data-stu-id="5b80e-316">In [Figure 21](#figure-21), the `margin-top` property for the currently selected element has been toggled off.</span></span>  

> ##### <span data-ttu-id="5b80e-317">Ilustración 21</span><span class="sxs-lookup"><span data-stu-id="5b80e-317">Figure 21</span></span>  
> <span data-ttu-id="5b80e-318">Alternar una declaración</span><span class="sxs-lookup"><span data-stu-id="5b80e-318">Toggling a declaration</span></span>  
> ![Alternar una declaración][ImageToggleDeclaration]  

### <span data-ttu-id="5b80e-320">Agregar una declaración de color de fondo</span><span class="sxs-lookup"><span data-stu-id="5b80e-320">Add a background-color declaration</span></span>   

<span data-ttu-id="5b80e-321">Para agregar una `background-color` declaración a un elemento:</span><span class="sxs-lookup"><span data-stu-id="5b80e-321">To add a `background-color` declaration to an element:</span></span>  

1.  <span data-ttu-id="5b80e-322">Pase el puntero sobre la regla de estilo a la que desea agregar la `background-color` declaración.</span><span class="sxs-lookup"><span data-stu-id="5b80e-322">Hover over the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="5b80e-323">[Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5b80e-323">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5b80e-324">Haga clic en **agregar color de fondo** para ![ agregar color de fondo ][ImageAddBackgroundColorIcon] .</span><span class="sxs-lookup"><span data-stu-id="5b80e-324">Click **Add Background Color** ![Add Background Color][ImageAddBackgroundColorIcon].</span></span>  

> ##### <span data-ttu-id="5b80e-325">Ilustración 22</span><span class="sxs-lookup"><span data-stu-id="5b80e-325">Figure 22</span></span>  
> **<span data-ttu-id="5b80e-326">Agregar color de fondo</span><span class="sxs-lookup"><span data-stu-id="5b80e-326">Add Background Color</span></span>**  
> ![Agregar color de fondo][ImageAddBackgroundColor]  

### <span data-ttu-id="5b80e-328">Agregar una declaración de color</span><span class="sxs-lookup"><span data-stu-id="5b80e-328">Add a color declaration</span></span>   

<span data-ttu-id="5b80e-329">Para agregar una `color` declaración a un elemento:</span><span class="sxs-lookup"><span data-stu-id="5b80e-329">To add a `color` declaration to an element:</span></span>  

1.  <span data-ttu-id="5b80e-330">Pase el puntero sobre la regla de estilo a la que desea agregar la `color` declaración.</span><span class="sxs-lookup"><span data-stu-id="5b80e-330">Hover over the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="5b80e-331">[Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5b80e-331">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5b80e-332">Haga clic en **Agregar** color ![ agregar color ][ImageAddColorIcon] .</span><span class="sxs-lookup"><span data-stu-id="5b80e-332">Click **Add Color** ![Add Color][ImageAddColorIcon].</span></span>  

> ##### <span data-ttu-id="5b80e-333">Ilustración 23</span><span class="sxs-lookup"><span data-stu-id="5b80e-333">Figure 23</span></span>  
> **<span data-ttu-id="5b80e-334">Agregar color</span><span class="sxs-lookup"><span data-stu-id="5b80e-334">Add Color</span></span>**  
> ![Agregar color][ImageAddColor]  

### <span data-ttu-id="5b80e-336">Agregar una declaración de sombra de cuadro</span><span class="sxs-lookup"><span data-stu-id="5b80e-336">Add a box-shadow declaration</span></span>   

<span data-ttu-id="5b80e-337">Para agregar una `box-shadow` declaración a un elemento:</span><span class="sxs-lookup"><span data-stu-id="5b80e-337">To add a `box-shadow` declaration to an element:</span></span>  

1.  <span data-ttu-id="5b80e-338">Pase el puntero sobre la regla de estilo a la que desea agregar la `box-shadow` declaración.</span><span class="sxs-lookup"><span data-stu-id="5b80e-338">Hover over the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="5b80e-339">[Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5b80e-339">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5b80e-340">Haga clic en **Agregar cuadro** sombra del ![ cuadro Agregar sombra ][ImageAddBoxShadowIcon] .</span><span class="sxs-lookup"><span data-stu-id="5b80e-340">Click **Add Box Shadow** ![Add Box Shadow][ImageAddBoxShadowIcon].</span></span>  

> ##### <span data-ttu-id="5b80e-341">Ilustración 24</span><span class="sxs-lookup"><span data-stu-id="5b80e-341">Figure 24</span></span>  
> **<span data-ttu-id="5b80e-342">Cuadro Agregar sombra</span><span class="sxs-lookup"><span data-stu-id="5b80e-342">Add Box Shadow</span></span>**  
> ![Cuadro Agregar sombra][ImageAddBoxShadow]  

### <span data-ttu-id="5b80e-344">Agregar una declaración de sombra de texto</span><span class="sxs-lookup"><span data-stu-id="5b80e-344">Add a text-shadow declaration</span></span>   

<span data-ttu-id="5b80e-345">Para agregar una `text-shadow` declaración a un elemento:</span><span class="sxs-lookup"><span data-stu-id="5b80e-345">To add a `text-shadow` declaration to an element:</span></span>  

1.  <span data-ttu-id="5b80e-346">Pase el puntero sobre la regla de estilo a la que desea agregar la `text-shadow` declaración.</span><span class="sxs-lookup"><span data-stu-id="5b80e-346">Hover over the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="5b80e-347">[Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="5b80e-347">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="5b80e-348">Haga clic en **Agregar sombra de texto** y ![ agregue sombra de texto ][ImageAddTextShadowIcon] .</span><span class="sxs-lookup"><span data-stu-id="5b80e-348">Click **Add Text Shadow** ![Add Text Shadow][ImageAddTextShadowIcon].</span></span>  

> ##### <span data-ttu-id="5b80e-349">Ilustración 25</span><span class="sxs-lookup"><span data-stu-id="5b80e-349">Figure 25</span></span>  
> **<span data-ttu-id="5b80e-350">Agregar sombra de texto</span><span class="sxs-lookup"><span data-stu-id="5b80e-350">Add Text Shadow</span></span>**  
> ![Agregar sombra de texto][ImageAddTextShadow]  

### <span data-ttu-id="5b80e-352">Cambiar los colores con el selector de colores</span><span class="sxs-lookup"><span data-stu-id="5b80e-352">Change colors with the Color Picker</span></span>   

<span data-ttu-id="5b80e-353">El **selector de colores** proporciona una interfaz gráfica de usuario para el cambio `color` y las `background-color` declaraciones.</span><span class="sxs-lookup"><span data-stu-id="5b80e-353">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="5b80e-354">Para abrir el **selector de colores**:</span><span class="sxs-lookup"><span data-stu-id="5b80e-354">To open the **Color Picker**:</span></span>  

1.  <span data-ttu-id="5b80e-355">[Seleccione un elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="5b80e-355">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="5b80e-356">En la pestaña **estilos** , busque la `color` `background-color` declaración similar que desea cambiar.</span><span class="sxs-lookup"><span data-stu-id="5b80e-356">In the **Styles** tab, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="5b80e-357">A la izquierda del `color` valor, `background-color` o similar, hay un pequeño cuadrado, que es una vista previa del color.</span><span class="sxs-lookup"><span data-stu-id="5b80e-357">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5b80e-358">En la [ilustración 26](#figure-26), el pequeño cuadrado a la izquierda de `rgba(0, 0, 0, 0.7)` es una versión preliminar de ese color.</span><span class="sxs-lookup"><span data-stu-id="5b80e-358">In [Figure 26](#figure-26), the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    > ##### <span data-ttu-id="5b80e-359">Ilustración 26</span><span class="sxs-lookup"><span data-stu-id="5b80e-359">Figure 26</span></span>  
    > <span data-ttu-id="5b80e-360">Vista previa del color</span><span class="sxs-lookup"><span data-stu-id="5b80e-360">Color preview</span></span>  
    > ![Vista previa del color][ImageColorPreview]  
    
1.  <span data-ttu-id="5b80e-362">Haga clic en la vista previa para abrir el **selector de color**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-362">Click the preview to open the **Color Picker**.</span></span>  
    
    > ##### <span data-ttu-id="5b80e-363">Ilustración 27</span><span class="sxs-lookup"><span data-stu-id="5b80e-363">Figure 27</span></span>  
    > <span data-ttu-id="5b80e-364">El **selector de colores**</span><span class="sxs-lookup"><span data-stu-id="5b80e-364">The **Color Picker**</span></span>  
    > ![El selector de colores][ImageColorPicker]  
    
<span data-ttu-id="5b80e-366">A continuación se muestra una descripción de cada uno de los elementos de la interfaz de usuario del **selector de colores**:</span><span class="sxs-lookup"><span data-stu-id="5b80e-366">Here is a description of each of the UI elements of the **Color Picker**:</span></span>  

> ##### <span data-ttu-id="5b80e-367">Ilustración 28</span><span class="sxs-lookup"><span data-stu-id="5b80e-367">Figure 28</span></span>  
> <span data-ttu-id="5b80e-368">El selector de color, anotado</span><span class="sxs-lookup"><span data-stu-id="5b80e-368">The Color Picker, annotated</span></span>  
> ![El selector de color, anotado][ImageColorPickerAnnotated]  

1.  <span data-ttu-id="5b80e-370">**Sombras**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-370">**Shades**.</span></span>  
1.  <span data-ttu-id="5b80e-371">**Cuentagotas**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-371">**Eyedropper**.</span></span>  <span data-ttu-id="5b80e-372">Vea [el ejemplo de color en la página con el cuentagotas](#sample-a-color-off-the-page-with-the-eyedropper).</span><span class="sxs-lookup"><span data-stu-id="5b80e-372">See [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
1.  <span data-ttu-id="5b80e-373">**Copiar al portapapeles**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-373">**Copy To Clipboard**.</span></span>  <span data-ttu-id="5b80e-374">Copie el **valor para mostrar** en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="5b80e-374">Copy the **Display Value** to your clipboard.</span></span>  
1.  <span data-ttu-id="5b80e-375">**Valor para mostrar**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-375">**Display Value**.</span></span>  <span data-ttu-id="5b80e-376">La representación RGBA, HSLA o hexadecimal del color.</span><span class="sxs-lookup"><span data-stu-id="5b80e-376">The RGBA, HSLA, or Hex representation of the color.</span></span>  
1.  <span data-ttu-id="5b80e-377">**Paleta de colores**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-377">**Color Palette**.</span></span>  <span data-ttu-id="5b80e-378">Haga clic en uno de estos cuadrados para cambiar el color de ese cuadrado.</span><span class="sxs-lookup"><span data-stu-id="5b80e-378">Click one of these squares to change the color to that square.</span></span>  
1.  <span data-ttu-id="5b80e-379">**Matiz**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-379">**Hue**.</span></span>  
1.  <span data-ttu-id="5b80e-380">**Opacidad**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-380">**Opacity**.</span></span>  
1.  <span data-ttu-id="5b80e-381">**Display Value Switcher**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-381">**Display Value Switcher**.</span></span>  <span data-ttu-id="5b80e-382">Alternar entre las representaciones RGBA, HSLA y hexadecimal del color actual.</span><span class="sxs-lookup"><span data-stu-id="5b80e-382">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
1.  <span data-ttu-id="5b80e-383">**Conmutador de paleta de colores**.</span><span class="sxs-lookup"><span data-stu-id="5b80e-383">**Color Palette Switcher**.</span></span>  <span data-ttu-id="5b80e-384">Cambiar entre la [paleta de diseño de material][MaterialDesignColorSystem], una paleta personalizada o una paleta de colores de página.</span><span class="sxs-lookup"><span data-stu-id="5b80e-384">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="5b80e-385">DevTools genera la paleta de colores de la página en función de los colores que encuentre en las hojas de estilo.</span><span class="sxs-lookup"><span data-stu-id="5b80e-385">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  

#### <span data-ttu-id="5b80e-386">Muestra un color de la página con el cuentagotas</span><span class="sxs-lookup"><span data-stu-id="5b80e-386">Sample a color off the page with the Eyedropper</span></span>   

<span data-ttu-id="5b80e-387">Al abrir el **selector de colores**, el cuentagotas **cuentagotas** ![ ][ImageEyedropperIcon] está activado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5b80e-387">When you open the **Color Picker**, the **Eyedropper** ![Eyedropper][ImageEyedropperIcon] is on by default.</span></span>  <span data-ttu-id="5b80e-388">Para cambiar el color seleccionado a otro color de la página:</span><span class="sxs-lookup"><span data-stu-id="5b80e-388">To change the selected color to some other color on the page:</span></span>  

1.  <span data-ttu-id="5b80e-389">Desplace el puntero sobre el color de destino en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="5b80e-389">Hover over the target color in the viewport.</span></span>  
1.  <span data-ttu-id="5b80e-390">Haga clic para confirmar.</span><span class="sxs-lookup"><span data-stu-id="5b80e-390">Click to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5b80e-391">En la [ilustración 29](#figure-29), el **selector de colores** muestra un valor de color actual de `rgba(0,0,0,0.7)` , que está cerca del negro.</span><span class="sxs-lookup"><span data-stu-id="5b80e-391">In [Figure 29](#figure-29), the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="5b80e-392">Este color debe cambiar al negro que está resaltado en la ventanilla cuando se hizo clic en el negro.</span><span class="sxs-lookup"><span data-stu-id="5b80e-392">This color should change to the black that is currently highlighted in the viewport once the black was clicked.</span></span>  
    
    > ##### <span data-ttu-id="5b80e-393">Ilustración 29</span><span class="sxs-lookup"><span data-stu-id="5b80e-393">Figure 29</span></span>  
    > <span data-ttu-id="5b80e-394">Usar el cuentagotas</span><span class="sxs-lookup"><span data-stu-id="5b80e-394">Using the Eyedropper</span></span>  
    > ![Usar el cuentagotas][ImageUsingEyedropper]  
    
 



<!-- image links -->  

[ImageAddBackgroundColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: /microsoft-edge/devtools-guide-chromium/media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-an-element-icon.msft.png  

[ImageSelectedElement]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1.msft.png "Ilustración 1: un ejemplo de un elemento seleccionado"  
[ImageViewRuleStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-highlight.msft.png "Ilustración 2: ver la hoja de estilos donde se define una regla"  
[ImageComputedTab]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-h1.msft.png "Ilustración 3: la pestaña calculada"  
[ImageBoxModel]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-2.msft.png "Ilustración 4: el diagrama de modelo de cuadro"  
[ImageStylesFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-color.msft.png "Ilustración 5: filtrar la pestaña estilos"  
[ImageComputerFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-filter-100.msft.png "Ilustración 6: filtrar la pestaña calculada"  
[ImagePseudoClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-hov-hover.msft.png "Ilustración 7: alternar la seudoclase: hover"  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-coverage.msft.png "Ilustración 8: abrir la pestaña cobertura desde el menú de comandos"  
[ImageCoverageEmpty]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-empty.msft.png "Ilustración 9: la pestaña cobertura"  
[ImageCoverageOverview]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-run.msft.png "Ilustración 10: información general sobre la cantidad de CSS (y JavaScript) que se usa y que no se usa"  
[ImageCoverageDetail]: /microsoft-edge/devtools-guide-chromium/media/css-sources-css-coverage.msft.png "Ilustración 11: División línea a línea de CSS utilizadas y sin usar"  
[ImageInlineDeclarations]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-margin-top-background-color.msft.png "Ilustración 12: agregar declaraciones en línea"  
[ImageAddDeclarationExistingRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style.msft.png "Ilustración 13: agregar una declaración a una regla de estilo"  
[ImageAddDeclarationExistingRule2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style-dropdown.msft.png "Ilustración 14: cambiar el valor de una declaración"  
[ImageElementClasses]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-classes.msft.png "Ilustración 15: el panel clases de elementos"  
[ImageStyleRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new.msft.png "Ilustración 16: agregar una nueva regla de estilo"  
[ImageChooseStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new-select-exisiting.msft.png "Ilustración 17: elegir una hoja de estilos"  
[ImageInsertStyleRuleBelow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-insert-style-rule-below.msft.png "Ilustración 18: insertar regla de estilo a continuación"  
[ImageRevealMore]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-new-rule-styles.msft.png "Ilustración 19: revelar más acciones"  
[ImageInsertStyleRuleBelow2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png "Ilustración 20: la barra de herramientas más acciones"  
[ImageToggleDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-deactivated.msft.png "Ilustración 21: cambiar una declaración"  
[ImageAddBackgroundColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-background-color.msft.png "Ilustración 22: agregar color de fondo"  
[ImageAddColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-color.msft.png "Ilustración 23: agregar color"  
[ImageAddBoxShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-box-shadow.msft.png "Ilustración 24: sombra del cuadro Agregar"  
[ImageAddTextShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-text-shadow.msft.png "Ilustración 25: agregar sombra de texto"  
[ImageColorPreview]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-overlay-color-box.msft.png "Ilustración 26: vista previa del color"  
[ImageColorPicker]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker.msft.png "Ilustración 27: el selector de colores"  
[ImageColorPickerAnnotated]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker-annotated.msft.png "Ilustración 28: el selector de color, anotado"  
[ImageUsingEyedropper]: /microsoft-edge/devtools-guide-chromium/media/css-color-picker-eye-dropper.msft.png "Ilustración 29: uso del cuentagotas"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  
[DevToolsCSSGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Introducción a la visualización y el cambio de CSS"  
[DevToolsCSSGetStartedAddPseudoState]: /microsoft-edge/devtools-guide-chromium/css/index#add-a-pseudostate-to-a-class "Agregar un PseudoState a una clase: Introducción a la visualización y el cambio de CSS"  
[DevToolsCSSGetStartedTutorial]: /microsoft-edge/devtools-guide-chromium/css/index#view-the-css-for-an-element "Ver las CSS de un elemento: Introducción a la visualización y el cambio de CSS"  
[DevToolsCssPrintPreview]: /microsoft-edge/devtools-guide-chromium/css/print-preview "Forzar que Microsoft Edge DevTools al modo de vista previa de impresión (tipo de archivo CSS de impresión)"  
[DevToolsJavascriptReferenceFormat]: /microsoft-edge/devtools-guide-chromium/javascript/reference#make-a-minified-file-readable "Hacer que un archivo minified sea legible: referencia de depuración de JavaScript"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "El diseño de material del sistema de colores"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "El modelo de cuadro | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Especificidad de los tipos de selector | MDN"  

> [!NOTE]
> <span data-ttu-id="5b80e-434">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5b80e-434">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5b80e-435">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5b80e-435">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5b80e-437">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5b80e-437">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

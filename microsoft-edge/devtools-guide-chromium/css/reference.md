---
title: Referencia de CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 908e32140d9deb89489089442055e188cd2d9378
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931500"
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

# <span data-ttu-id="239af-103">Referencia de CSS</span><span class="sxs-lookup"><span data-stu-id="239af-103">CSS reference</span></span>  

<span data-ttu-id="239af-104">Descubra nuevos flujos de trabajo en la siguiente referencia completa de las características de Microsoft Edge DevTools relacionadas con la visualización y el cambio de CSS.</span><span class="sxs-lookup"><span data-stu-id="239af-104">Discover new workflows in the following comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="239af-105">Consulte Introducción a la [visualización y el cambio de CSS][DevToolsCSSGetStarted] para conocer los conceptos básicos.</span><span class="sxs-lookup"><span data-stu-id="239af-105">See [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted] to learn the basics.</span></span>  

## <span data-ttu-id="239af-106">Seleccionar un elemento</span><span class="sxs-lookup"><span data-stu-id="239af-106">Select an element</span></span>  

<span data-ttu-id="239af-107">El panel **elementos** de DevTools le permite ver o cambiar la CSS de un elemento a la vez.</span><span class="sxs-lookup"><span data-stu-id="239af-107">The **Elements** panel of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="239af-108">El elemento seleccionado está resaltado en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="239af-108">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="239af-109">Los estilos del elemento se muestran en el panel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="239af-109">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="239af-110">Vea [ver las CSS de un elemento][DevToolsCSSGetStartedTutorial] para obtener un tutorial.</span><span class="sxs-lookup"><span data-stu-id="239af-110">See [View the CSS for an element][DevToolsCSSGetStartedTutorial] for a tutorial.</span></span>  

> [!NOTE]
> <span data-ttu-id="239af-111">En la siguiente ilustración, el `h1` elemento que está resaltado en el **árbol DOM** es el elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="239af-111">In the following figure, the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="239af-112">A la derecha, los estilos del elemento se muestran en el panel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="239af-112">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="239af-113">A la izquierda, el elemento se resalta en la ventanilla, pero solo porque el mouse se desplaza en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="239af-113">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Ejemplo de un elemento seleccionado" lightbox="../media/css-elements-styles-h1.msft.png":::
   <span data-ttu-id="239af-115">Ejemplo de un elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="239af-115">An example of a selected element</span></span>  
:::image-end:::  

<span data-ttu-id="239af-116">Use una de las siguientes acciones para seleccionar un elemento.</span><span class="sxs-lookup"><span data-stu-id="239af-116">Use one the following actions to select an element.</span></span>  

*   <span data-ttu-id="239af-117">En su ventanilla, desplace el puntero sobre el elemento, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="239af-117">In your viewport, hover on the element, open the contextual menu \(right-click\), and select **Inspect**.</span></span>  
*   <span data-ttu-id="239af-118">En DevTools, elija **seleccionar un elemento** \ ( ![ Seleccione un elemento ][ImageSelectAnElementIcon] \) o \ `Control` + `Shift` + `C` (Windows \) o `Command` + `Shift` + `C` \ (MacOS \) y, a continuación, elija el elemento en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="239af-118">In DevTools, choose **Select an element** \(![Select an element][ImageSelectAnElementIcon]\) or select `Control`+`Shift`+`C` \(Windows\) or `Command`+`Shift`+`C` \(macOS\), and then choose the element in the viewport.</span></span>  
*   <span data-ttu-id="239af-119">En DevTools, elija el elemento en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="239af-119">In DevTools, choose the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="239af-120">En DevTools, ejecute una consulta como `document.querySelector('p')` en la **consola**, coloque el puntero sobre el resultado, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **Mostrar en el panel de elementos**.</span><span class="sxs-lookup"><span data-stu-id="239af-120">In DevTools, run a query like `document.querySelector('p')` in the **Console**, hover on the result, open the contextual menu \(right-click\), and select **Reveal in Elements panel**.</span></span>  

## <span data-ttu-id="239af-121">Ver CSS</span><span class="sxs-lookup"><span data-stu-id="239af-121">View CSS</span></span>  

### <span data-ttu-id="239af-122">Ver la hoja de estilos externa donde se define una regla</span><span class="sxs-lookup"><span data-stu-id="239af-122">View the external stylesheet where a rule is defined</span></span>  

<span data-ttu-id="239af-123">En el panel **estilos** , elija el vínculo junto a una regla CSS para abrir la hoja de estilos externa que define la regla.</span><span class="sxs-lookup"><span data-stu-id="239af-123">In the **Styles** pane, choose the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  

<span data-ttu-id="239af-124">Si la hoja de estilos es minified, vea [hacer que un archivo minified sea legible][DevToolsJavascriptReferenceFormat].</span><span class="sxs-lookup"><span data-stu-id="239af-124">If the stylesheet is minified, see [Make a minified file readable][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="239af-125">En la siguiente ilustración, después de elegir, `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` se le dirigirá a la línea 2 de `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , donde `.content h1:first-of-type` se define la regla CSS.</span><span class="sxs-lookup"><span data-stu-id="239af-125">In the following figure, after you choose `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` you are taken to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Ver la hoja de estilos donde se define una regla" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  <span data-ttu-id="239af-127">Ver la hoja de estilos donde se define una regla</span><span class="sxs-lookup"><span data-stu-id="239af-127">Viewing the stylesheet where a rule is defined</span></span>  
:::image-end:::  

### <span data-ttu-id="239af-128">Ver solo la CSS que se aplica realmente a un elemento</span><span class="sxs-lookup"><span data-stu-id="239af-128">View only the CSS that is actually applied to an element</span></span>  

<span data-ttu-id="239af-129">La pestaña **estilos** muestra todas las reglas que se aplican a un elemento, incluidas las declaraciones que se han reemplazado.</span><span class="sxs-lookup"><span data-stu-id="239af-129">The **Styles** tab shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="239af-130">Si no está interesado en las declaraciones reemplazadas, use la pestaña **calculada** para ver solo la CSS que se está aplicando realmente a un elemento.</span><span class="sxs-lookup"><span data-stu-id="239af-130">When you are not interested in overridden declarations, use the **Computed** tab to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="239af-131">[Seleccione un elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="239af-131">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="239af-132">Vaya a la pestaña **calculada** en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="239af-132">Go to the **Computed** tab in the **Elements** panel.</span></span>  

> [!NOTE]
> <span data-ttu-id="239af-133">En una ventana de DevTools ancha, la pestaña **calculada** no existe.</span><span class="sxs-lookup"><span data-stu-id="239af-133">On a wide DevTools window, the **Computed** tab does not exist.</span></span>  <span data-ttu-id="239af-134">El contenido de la pestaña **calculada** se muestra en la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="239af-134">The contents of the **Computed** tab are shown on the **Styles** tab.</span></span>  

<span data-ttu-id="239af-135">Las propiedades heredadas son opacas.</span><span class="sxs-lookup"><span data-stu-id="239af-135">Inherited properties are opaque.</span></span>  <span data-ttu-id="239af-136">Active la casilla **Mostrar todo** para ver todos los valores heredados.</span><span class="sxs-lookup"><span data-stu-id="239af-136">Check the **Show All** checkbox to see all inherited values.</span></span>  

> [!NOTE]
> <span data-ttu-id="239af-137">En la siguiente ilustración, la pestaña **calculada** muestra las propiedades de CSS que se aplican al elemento seleccionado actualmente `h1` .</span><span class="sxs-lookup"><span data-stu-id="239af-137">In the following figure, the **Computed** tab shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="La pestaña calculada" lightbox="../media/css-elements-computed-h1.msft.png":::
   <span data-ttu-id="239af-139">La pestaña **calculada**</span><span class="sxs-lookup"><span data-stu-id="239af-139">The **Computed** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="239af-140">Ver las propiedades de CSS por orden alfabético</span><span class="sxs-lookup"><span data-stu-id="239af-140">View CSS properties in alphabetical order</span></span>  

<span data-ttu-id="239af-141">Use la pestaña **calculada** .  Vea [ver solo la CSS que se aplica realmente a un elemento](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="239af-141">Use the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="239af-142">Ver las propiedades heredadas de CSS</span><span class="sxs-lookup"><span data-stu-id="239af-142">View inherited CSS properties</span></span>  

<span data-ttu-id="239af-143">Active la casilla **Mostrar todo** en la pestaña **calculada** .  Vea [ver solo la CSS que se aplica realmente a un elemento](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="239af-143">Check the **Show All** checkbox in the **Computed** tab.  See [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <span data-ttu-id="239af-144">Ver el modelo de cuadro de un elemento</span><span class="sxs-lookup"><span data-stu-id="239af-144">View the box model for an element</span></span>  

<span data-ttu-id="239af-145">Para ver [el modelo de cuadro][MDNBoxModel] de un elemento, vaya a la pestaña **estilos** .  Si la ventana de DevTools es estrecha, el diagrama de **modelo de cuadro** se encuentra en la parte inferior de la pestaña.</span><span class="sxs-lookup"><span data-stu-id="239af-145">To view [the box model][MDNBoxModel] of an element, go to the **Styles** tab.  If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the tab.</span></span>  

<span data-ttu-id="239af-146">Elija y edite en un valor para cambiar un valor.</span><span class="sxs-lookup"><span data-stu-id="239af-146">Choose and edit on a value to change a value.</span></span>  

> [!NOTE]
> <span data-ttu-id="239af-147">En la siguiente ilustración, el diagrama de **modelo de cuadro** de la pestaña **estilos** muestra el modelo de cuadro para el elemento seleccionado actualmente `h1` .</span><span class="sxs-lookup"><span data-stu-id="239af-147">In the following figure, the **Box Model** diagram in the **Styles** tab shows the box model for the currently selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="El diagrama de modelo de cuadro" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   <span data-ttu-id="239af-149">El diagrama de **modelo de cuadro**</span><span class="sxs-lookup"><span data-stu-id="239af-149">The **Box Model** diagram</span></span>  
:::image-end:::  

### <span data-ttu-id="239af-150">Buscar y filtrar la CSS de un elemento</span><span class="sxs-lookup"><span data-stu-id="239af-150">Search and filter the CSS of an element</span></span>  

<span data-ttu-id="239af-151">Use el cuadro de texto **filtrar** en los **estilos** y las pestañas **calculadas** para buscar propiedades o valores específicos de CSS.</span><span class="sxs-lookup"><span data-stu-id="239af-151">Use the **Filter** text box on the **Styles** and **Computed** tabs to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="239af-152">Para buscar también las propiedades heredadas en la pestaña **calculada** , active la casilla **Mostrar todo** .</span><span class="sxs-lookup"><span data-stu-id="239af-152">To also search inherited properties in the **Computed** tab, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="239af-153">En la siguiente ilustración, la pestaña **estilos** se filtra para mostrar únicamente las reglas que incluyen la consulta de búsqueda `color` .</span><span class="sxs-lookup"><span data-stu-id="239af-153">In the following figure, the **Styles** tab is filtered to only show rules that include the search query `color`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Filtrar la pestaña estilos" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   <span data-ttu-id="239af-155">Filtrar la pestaña **estilos**</span><span class="sxs-lookup"><span data-stu-id="239af-155">Filter the **Styles** tab</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="239af-156">En la siguiente ilustración, la pestaña **calculada** se filtra para mostrar únicamente las declaraciones que incluyen la consulta de búsqueda `100%` .</span><span class="sxs-lookup"><span data-stu-id="239af-156">In the following figure, the **Computed** tab is filtered to only show declarations that include the search query `100%`.</span></span>  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Filtrar la pestaña calculada" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   <span data-ttu-id="239af-158">Filtrar la pestaña **calculada**</span><span class="sxs-lookup"><span data-stu-id="239af-158">Filter the **Computed** tab</span></span>  
:::image-end:::  

### <span data-ttu-id="239af-159">Alternar una seudoclase</span><span class="sxs-lookup"><span data-stu-id="239af-159">Toggle a pseudo-class</span></span>  

<span data-ttu-id="239af-160">Complete las acciones siguientes para cambiar una seudoclase como `:active` ,, `:focus` `:hover` o `:visited` .</span><span class="sxs-lookup"><span data-stu-id="239af-160">Complete the following actions to toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`.</span></span>  

1.  <span data-ttu-id="239af-161">[Seleccione un elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="239af-161">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="239af-162">En el panel **elementos** , vaya a la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="239af-162">On the **Elements** panel, go to the **Styles** tab.</span></span>  
1.  <span data-ttu-id="239af-163">Elija **: HOV**.</span><span class="sxs-lookup"><span data-stu-id="239af-163">Choose **:hov**.</span></span>  
1.  <span data-ttu-id="239af-164">Compruebe la pseudo-clase que desea habilitar.</span><span class="sxs-lookup"><span data-stu-id="239af-164">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="239af-165">En la siguiente ilustración, alterne la `:hover` pseudo-clase.</span><span class="sxs-lookup"><span data-stu-id="239af-165">In the following figure, toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="239af-166">En la ventanilla, compruebe que la `background-color: cornflowerblue` declaración se aplica al elemento, aunque no se esté colocando el elemento en realidad.</span><span class="sxs-lookup"><span data-stu-id="239af-166">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Activar o desactivar la seudoclase: hover" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   <span data-ttu-id="239af-168">Activar o desactivar la `:hover` seudoclase</span><span class="sxs-lookup"><span data-stu-id="239af-168">Toggle the `:hover` pseudo-class</span></span>  
:::image-end:::  

<span data-ttu-id="239af-169">Para obtener un tutorial interactivo, consulte [Agregar un PseudoState a una clase][DevToolsCSSGetStartedAddPseudoState].</span><span class="sxs-lookup"><span data-stu-id="239af-169">For an interactive tutorial, see [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState].</span></span>  

### <span data-ttu-id="239af-170">Ver una página en modo de impresión</span><span class="sxs-lookup"><span data-stu-id="239af-170">View a page in print mode</span></span>  

<span data-ttu-id="239af-171">Complete las acciones siguientes para ver una página en modo de impresión.</span><span class="sxs-lookup"><span data-stu-id="239af-171">Complete the following actions to view a page in print mode.</span></span>  

1.  <span data-ttu-id="239af-172">[Abrir el menú de comandos][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="239af-172">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="239af-173">Empiece `Rendering` a escribir y seleccione `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="239af-173">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="239af-174">Para la lista desplegable **emular multimedia de CSS** , seleccione **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="239af-174">For the **Emulate CSS Media** dropdown, select **print**.</span></span>  

### <span data-ttu-id="239af-175">Ver las CSS usadas y sin usar con la pestaña cobertura</span><span class="sxs-lookup"><span data-stu-id="239af-175">View used and unused CSS with the Coverage tab</span></span>  

<span data-ttu-id="239af-176">La pestaña cobertura le muestra qué CSS usa una página en realidad.</span><span class="sxs-lookup"><span data-stu-id="239af-176">The Coverage tab shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="239af-177">Seleccione `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) mientras DevTools el foco para [abrir el menú de comandos][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="239af-177">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to [open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="239af-178">Empiece `coverage` a escribir y seleccione **Mostrar cobertura**.</span><span class="sxs-lookup"><span data-stu-id="239af-178">Start typing `coverage` and select **Show Coverage**.</span></span>  <span data-ttu-id="239af-179">Aparece la ficha cobertura.</span><span class="sxs-lookup"><span data-stu-id="239af-179">The Coverage tab appears.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Abrir la ficha cobertura desde el menú de comandos" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             <span data-ttu-id="239af-181">Abrir la pestaña **cobertura** desde el **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="239af-181">Open the **Coverage** tab from the **Command Menu**</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="La ficha cobertura" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             <span data-ttu-id="239af-183">La ficha **cobertura**</span><span class="sxs-lookup"><span data-stu-id="239af-183">The **Coverage** tab</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="239af-184">Elija **iniciar la cobertura de la instrumentación y actualice la página** \ ( ![ empezar la cobertura de la instrumentación y actualizar la página ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="239af-184">Choose **Start instrumenting coverage and refresh the page** \(![Start instrumenting coverage and refresh the page][ImageRefreshIcon]\).</span></span>  <span data-ttu-id="239af-185">La página se actualiza y la pestaña cobertura proporciona una descripción general de la cantidad de CSS \ (y JavaScript \) que se usa en cada archivo que carga el explorador.</span><span class="sxs-lookup"><span data-stu-id="239af-185">The page refreshes and the Coverage tab provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="239af-186">El verde representa CSS usado.</span><span class="sxs-lookup"><span data-stu-id="239af-186">Green represents used CSS.</span></span>  <span data-ttu-id="239af-187">Rojo representa un CSS no usado.</span><span class="sxs-lookup"><span data-stu-id="239af-187">Red represents unused CSS.</span></span>  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Información general sobre la cantidad de CSS (y JavaScript) que se usa y que no se usa" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       <span data-ttu-id="239af-189">Información general sobre la cantidad de CSS \ (y JavaScript \) que se usa y que no se usa</span><span class="sxs-lookup"><span data-stu-id="239af-189">An overview of how much CSS \(and JavaScript\) is used and unused</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="239af-190">Elija un archivo CSS para ver un desglose línea por línea de qué usa CSS.</span><span class="sxs-lookup"><span data-stu-id="239af-190">Choose a CSS file to see a line-by-line breakdown of what CSS it uses.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="239af-191">En la siguiente ilustración, las líneas 145 a 147 y 149 a 151 de no `b66bc881.site-ltr.css` se usan, mientras que las líneas 163 a 166 se usan.</span><span class="sxs-lookup"><span data-stu-id="239af-191">In the following figure, lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Un desglose línea a línea de CSS utilizadas y sin usar" lightbox="../media/css-sources-css-coverage.msft.png":::
       <span data-ttu-id="239af-193">Un desglose línea a línea de CSS utilizadas y sin usar</span><span class="sxs-lookup"><span data-stu-id="239af-193">A line-by-line breakdown of used and unused CSS</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="239af-194">Forzar el modo vista previa de impresión</span><span class="sxs-lookup"><span data-stu-id="239af-194">Force print preview mode</span></span>  

<span data-ttu-id="239af-195">Consulte [forzar DevTools en el modo de vista previa de impresión][DevToolsCssPrintPreview].</span><span class="sxs-lookup"><span data-stu-id="239af-195">See [Force DevTools into Print Preview mode][DevToolsCssPrintPreview].</span></span>  

## <span data-ttu-id="239af-196">Cambiar CSS</span><span class="sxs-lookup"><span data-stu-id="239af-196">Change CSS</span></span>  

<!-- todo s/CSS declaration/declaration/ -->  

### <span data-ttu-id="239af-197">Agregar una declaración CSS a un elemento</span><span class="sxs-lookup"><span data-stu-id="239af-197">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="239af-198">El orden de las declaraciones afecta a la forma en que se aplica el estilo de un elemento, use la siguiente lista para ayudarle a agregar declaraciones de diferentes maneras.</span><span class="sxs-lookup"><span data-stu-id="239af-198">The order of declarations affects how an element is styled, use the following list to help you add declarations in different ways.</span></span>  

*   <span data-ttu-id="239af-199">[Agregue una declaración en línea](#add-an-inline-declaration).</span><span class="sxs-lookup"><span data-stu-id="239af-199">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="239af-200">Es equivalente a agregar un `style` atributo al código HTML de un elemento.</span><span class="sxs-lookup"><span data-stu-id="239af-200">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="239af-201">[Agregue una declaración a una regla de estilo](#add-a-declaration-to-a-style-rule).</span><span class="sxs-lookup"><span data-stu-id="239af-201">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="239af-202">¿Qué flujo de trabajo debe usar?</span><span class="sxs-lookup"><span data-stu-id="239af-202">What workflow should you use?</span></span>** <span data-ttu-id="239af-203">En la mayoría de los casos, probablemente quieras usar el flujo de trabajo de declaración en línea.</span><span class="sxs-lookup"><span data-stu-id="239af-203">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="239af-204">Las declaraciones en línea tienen una mayor especificidad que las externas, por lo que el flujo de trabajo insertado garantiza que los cambios se apliquen en el elemento esperado.</span><span class="sxs-lookup"><span data-stu-id="239af-204">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in your expected element.</span></span>  <span data-ttu-id="239af-205">Para obtener más información sobre la especificidad, consulte [tipos de selector][MDNSelectorTypes].</span><span class="sxs-lookup"><span data-stu-id="239af-205">For more information about specificity, see [Selector Types][MDNSelectorTypes].</span></span>  

<span data-ttu-id="239af-206">Si depura cualquier estilo del elemento y necesita comprobar específicamente lo que ocurre cuando se define una declaración en distintos lugares, use el otro flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="239af-206">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <span data-ttu-id="239af-207">Agregar una declaración en línea</span><span class="sxs-lookup"><span data-stu-id="239af-207">Add an inline declaration</span></span>  

<span data-ttu-id="239af-208">Complete las acciones siguientes para agregar una declaración en línea.</span><span class="sxs-lookup"><span data-stu-id="239af-208">Complete the following actions to add an inline declaration.</span></span>  

1.  <span data-ttu-id="239af-209">[Seleccione un elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="239af-209">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="239af-210">En el panel **estilos** , elija entre los corchetes del **elemento. sección Style** .</span><span class="sxs-lookup"><span data-stu-id="239af-210">In the **Styles** pane, choose between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="239af-211">El cursor se centra, lo que le permite escribir texto.</span><span class="sxs-lookup"><span data-stu-id="239af-211">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="239af-212">Escriba un nombre de propiedad y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="239af-212">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="239af-213">Escriba un valor válido para esa propiedad y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="239af-213">Enter a valid value for that property and select `Enter`.</span></span>  <span data-ttu-id="239af-214">En el **árbol DOM**, compruebe que se ha `style` agregado un atributo al elemento.</span><span class="sxs-lookup"><span data-stu-id="239af-214">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="239af-215">En la siguiente ilustración, `margin-top` se han `background-color` aplicado las propiedades y al elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="239af-215">In the following figure, the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="239af-216">En el **árbol DOM** , compruebe que las declaraciones se reflejan en el `style` atributo de un elemento.</span><span class="sxs-lookup"><span data-stu-id="239af-216">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Agregar declaraciones en línea" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   <span data-ttu-id="239af-218">Agregar declaraciones en línea</span><span class="sxs-lookup"><span data-stu-id="239af-218">Add inline declarations</span></span>  
:::image-end:::  

#### <span data-ttu-id="239af-219">Agregar una declaración a una regla de estilo</span><span class="sxs-lookup"><span data-stu-id="239af-219">Add a declaration to a style rule</span></span>  

<span data-ttu-id="239af-220">Complete las siguientes acciones para agregar una declaración a una regla de estilo existente.</span><span class="sxs-lookup"><span data-stu-id="239af-220">Complete the following actions to add a declaration to an existing style rule.</span></span>  

1.  <span data-ttu-id="239af-221">[Seleccione un elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="239af-221">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="239af-222">En el panel **estilos** , elija entre los corchetes de la regla de estilo a los que desea agregar la declaración.</span><span class="sxs-lookup"><span data-stu-id="239af-222">In the **Styles** pane, choose between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="239af-223">El cursor se centra, lo que le permite escribir texto.</span><span class="sxs-lookup"><span data-stu-id="239af-223">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="239af-224">Escriba un nombre de propiedad y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="239af-224">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="239af-225">Escriba un valor válido para esa propiedad y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="239af-225">Enter a valid value for that property and select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Agregar una declaración a una regla de estilo" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   <span data-ttu-id="239af-227">Agregar la `border-bottom-style:groove` declaración a una regla de estilo</span><span class="sxs-lookup"><span data-stu-id="239af-227">Add the `border-bottom-style:groove` declaration to a style rule</span></span>  
:::image-end:::  

### <span data-ttu-id="239af-228">Cambiar un nombre o valor de declaración</span><span class="sxs-lookup"><span data-stu-id="239af-228">Change a declaration name or value</span></span>  

<span data-ttu-id="239af-229">Elija y edite el nombre o el valor de una declaración para cambiarlo.</span><span class="sxs-lookup"><span data-stu-id="239af-229">Choose and edit the name or value of a declaration to change it.</span></span>  <span data-ttu-id="239af-230">Vea [cambiar valores de declaración con métodos abreviados de teclado](#change-declaration-values-with-keyboard-shortcuts) para métodos abreviados para aumentar o disminuir rápidamente un valor por `0.1` `1` unidades,, `10` o `100` .</span><span class="sxs-lookup"><span data-stu-id="239af-230">See [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts) for shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Cambiar el valor de una declaración" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   <span data-ttu-id="239af-232">Cambiar el valor de la `border-bottom-style` declaración</span><span class="sxs-lookup"><span data-stu-id="239af-232">Change the value of the `border-bottom-style` declaration</span></span>  
:::image-end:::  

### <span data-ttu-id="239af-233">Cambiar los valores de declaración con métodos abreviados de teclado</span><span class="sxs-lookup"><span data-stu-id="239af-233">Change declaration values with keyboard shortcuts</span></span>  

<span data-ttu-id="239af-234">Al editar el valor de una declaración, puede usar los siguientes métodos abreviados de teclado para incrementar el valor en una cantidad específica.</span><span class="sxs-lookup"><span data-stu-id="239af-234">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a specific amount.</span></span>  

*   <span data-ttu-id="239af-235">Seleccione `Alt` + `Up` \ (Windows \) o `Option` + `Up` \ (MacOS \) para incrementar `0.1` .</span><span class="sxs-lookup"><span data-stu-id="239af-235">Select `Alt`+`Up` \(Windows\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="239af-236">Seleccione `Up` para cambiar el valor por `1` , o por `0.1` si el valor actual se encuentra entre `-1` y `1` .</span><span class="sxs-lookup"><span data-stu-id="239af-236">Select `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="239af-237">Seleccione `Shift` + `Up` para incrementar `10` .</span><span class="sxs-lookup"><span data-stu-id="239af-237">Select `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="239af-238">Seleccione `Shift` + `Page Up` \ (Windows \) o `Shift` + `Command` + `Up` \ (MacOS \) para incrementar el valor `100` .</span><span class="sxs-lookup"><span data-stu-id="239af-238">Select `Shift`+`Page Up` \(Windows\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="239af-239">También funciona la reducción.</span><span class="sxs-lookup"><span data-stu-id="239af-239">Decrementing also works.</span></span>  <span data-ttu-id="239af-240">Solo tiene que reemplazar cada instancia de la `Up` mencionada anteriormente con `Down` .</span><span class="sxs-lookup"><span data-stu-id="239af-240">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <span data-ttu-id="239af-241">Agregar una clase a un elemento</span><span class="sxs-lookup"><span data-stu-id="239af-241">Add a class to an element</span></span>  

<span data-ttu-id="239af-242">Complete las siguientes acciones para agregar una clase a un elemento.</span><span class="sxs-lookup"><span data-stu-id="239af-242">Complete the following actions to add a class to an element.</span></span>  

1.  <span data-ttu-id="239af-243">[Seleccione el elemento](#select-an-element) en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="239af-243">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="239af-244">Elija **. CLS**.</span><span class="sxs-lookup"><span data-stu-id="239af-244">Choose **.cls**.</span></span>  
1.  <span data-ttu-id="239af-245">Escriba el nombre de la clase en el cuadro de texto **Agregar nueva clase** .</span><span class="sxs-lookup"><span data-stu-id="239af-245">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="239af-246">Seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="239af-246">Select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Panel clases de elementos" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   <span data-ttu-id="239af-248">Panel **clases de elementos**</span><span class="sxs-lookup"><span data-stu-id="239af-248">The **Element Classes** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="239af-249">Activar o desactivar una clase</span><span class="sxs-lookup"><span data-stu-id="239af-249">Toggle a class</span></span>  

<span data-ttu-id="239af-250">Complete las siguientes acciones para habilitar o deshabilitar una clase en un elemento.</span><span class="sxs-lookup"><span data-stu-id="239af-250">Complete the following actions to enable or disable a class on an element.</span></span>  

1.  <span data-ttu-id="239af-251">[Seleccione el elemento](#select-an-element) en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="239af-251">[Select the element](#select-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="239af-252">Abra el panel **clases de elementos** .</span><span class="sxs-lookup"><span data-stu-id="239af-252">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="239af-253">Vea [Agregar una clase a un elemento](#add-a-class-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="239af-253">See [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="239af-254">Debajo del cuadro de texto **Agregar nueva clase** se encuentran todas las clases que se están aplicando al elemento específico.</span><span class="sxs-lookup"><span data-stu-id="239af-254">Below the **Add New Class** text box are all of the classes that are being applied to the specific element.</span></span>  
1.  <span data-ttu-id="239af-255">Active la casilla situada junto a la clase que desea habilitar o deshabilitar.</span><span class="sxs-lookup"><span data-stu-id="239af-255">Toggle the checkbox next to the class that you want to enable or disable.</span></span>  

### <span data-ttu-id="239af-256">Agregar una regla de estilo</span><span class="sxs-lookup"><span data-stu-id="239af-256">Add a style rule</span></span>  

<span data-ttu-id="239af-257">Complete las siguientes acciones para agregar una nueva regla de estilo.</span><span class="sxs-lookup"><span data-stu-id="239af-257">Complete the following actions to add a new style rule.</span></span>  

1.  <span data-ttu-id="239af-258">[Seleccione un elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="239af-258">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="239af-259">Elija **nueva regla de estilo** \ ( ![ nueva regla de estilo ][ImageNewStyleRuleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="239af-259">Choose **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\).</span></span>  <span data-ttu-id="239af-260">DevTools inserta una nueva regla debajo del **elemento.** regla de estilo.</span><span class="sxs-lookup"><span data-stu-id="239af-260">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="239af-261">En la siguiente ilustración, DevTools agrega la `h1.devsite-page-title` regla de estilo después de elegir **nueva regla de estilo**.</span><span class="sxs-lookup"><span data-stu-id="239af-261">In the following figure, DevTools adds the `h1.devsite-page-title` style rule after you choose **New Style Rule**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Agregar una nueva regla de estilo" lightbox="../media/css-elements-styles-style-new.msft.png":::
   <span data-ttu-id="239af-263">Agregar una nueva regla de estilo</span><span class="sxs-lookup"><span data-stu-id="239af-263">Add a new style rule</span></span>  
:::image-end:::  

#### <span data-ttu-id="239af-264">Elegir la hoja de estilos a la que se va a agregar una regla</span><span class="sxs-lookup"><span data-stu-id="239af-264">Choose which stylesheet to add a rule to</span></span>  

<span data-ttu-id="239af-265">Al [Agregar una nueva regla de estilo](#add-a-style-rule), seleccione y mantenga presionada la **nueva** regla de estilo \ ( ![ nueva regla de estilo ][ImageNewStyleRuleIcon] \) para elegir a qué hoja de estilos desea agregar la regla de estilo.</span><span class="sxs-lookup"><span data-stu-id="239af-265">When [adding a new style rule](#add-a-style-rule), choose and hold **New Style Rule** \(![New Style Rule][ImageNewStyleRuleIcon]\) to choose which stylesheet to add the style rule to.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Elegir una hoja de estilos" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   <span data-ttu-id="239af-267">Elegir una hoja de estilos</span><span class="sxs-lookup"><span data-stu-id="239af-267">Choose a stylesheet</span></span>  
:::image-end:::  

#### <span data-ttu-id="239af-268">Agregar una regla de estilo a una ubicación específica</span><span class="sxs-lookup"><span data-stu-id="239af-268">Add a style rule to a specific location</span></span>  

<span data-ttu-id="239af-269">Complete las siguientes acciones para agregar una regla de estilo a una ubicación específica en la pestaña **estilos** .</span><span class="sxs-lookup"><span data-stu-id="239af-269">Complete the following actions to add a style rule to a specific location in the **Styles** tab.</span></span>  

1.  <span data-ttu-id="239af-270">Desplace el puntero sobre la regla de estilo que está justo encima del lugar donde desea agregar la nueva regla de estilo.</span><span class="sxs-lookup"><span data-stu-id="239af-270">Hover over the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="239af-271">[Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="239af-271">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="239af-272">Elija **Insertar regla de estilo a continuación** \ ( ![ Insertar regla de estilo debajo de ][ImageNewStyleRuleIcon] \).</span><span class="sxs-lookup"><span data-stu-id="239af-272">Choose **Insert Style Rule Below** \(![Insert Style Rule Below][ImageNewStyleRuleIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Insertar regla de estilo a continuación" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **<span data-ttu-id="239af-274">Insertar regla de estilo a continuación</span><span class="sxs-lookup"><span data-stu-id="239af-274">Insert Style Rule Below</span></span>**  
:::image-end:::  

### <span data-ttu-id="239af-275">Mostrar la barra de herramientas más acciones</span><span class="sxs-lookup"><span data-stu-id="239af-275">Reveal the More Actions toolbar</span></span>  

<span data-ttu-id="239af-276">La barra de herramientas **más acciones** le permite realizar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="239af-276">The **More Actions** toolbar lets you perform the following actions.</span></span>  

*   <span data-ttu-id="239af-277">Inserte una regla de estilo directamente debajo de la que se le está concentrando.</span><span class="sxs-lookup"><span data-stu-id="239af-277">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="239af-278">Agregue una `background-color` `color` declaración, `box-shadow` o `text-shadow` a la regla de estilo en la que se concentra.</span><span class="sxs-lookup"><span data-stu-id="239af-278">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="239af-279">Complete las siguientes acciones para mostrar la barra de herramientas **más acciones** .</span><span class="sxs-lookup"><span data-stu-id="239af-279">Complete the following actions to reveal the **More Actions** toolbar.</span></span>  

1.  <span data-ttu-id="239af-280">En la pestaña **estilos** , desplace el puntero sobre una regla de estilo.</span><span class="sxs-lookup"><span data-stu-id="239af-280">In the **Styles** tab, hover over a style rule.</span></span>  <span data-ttu-id="239af-281">**Más acciones** \ ( `...` \) se muestra en la parte inferior derecha de la sección regla de estilo.</span><span class="sxs-lookup"><span data-stu-id="239af-281">**More Actions** \(`...`\) is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="239af-282">En la siguiente ilustración, desplace el puntero sobre la `.header-holder.has-default-focus` regla de estilo y se revelarán **más acciones** en la parte inferior derecha de la sección regla de estilo.</span><span class="sxs-lookup"><span data-stu-id="239af-282">In the following figure, hover over the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Mostrar más acciones" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       <span data-ttu-id="239af-284">Mostrar **más acciones** \ ( `...` \)</span><span class="sxs-lookup"><span data-stu-id="239af-284">Reveal **More Actions** \(`...`\)</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="239af-285">Mantenga el mouse sobre **más acciones** \ ( `...` \) para mostrar las acciones mencionadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="239af-285">Hover over **More Actions** \(`...`\) to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="239af-286">La acción **Insertar regla de estilo se muestra** después de mantener el mouse sobre **más acciones**.</span><span class="sxs-lookup"><span data-stu-id="239af-286">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="La barra de herramientas más acciones" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       <span data-ttu-id="239af-288">La barra de herramientas **más acciones**</span><span class="sxs-lookup"><span data-stu-id="239af-288">The **More Actions** toolbar</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="239af-289">Activar o desactivar una declaración</span><span class="sxs-lookup"><span data-stu-id="239af-289">Toggle a declaration</span></span>  

<span data-ttu-id="239af-290">Completa las acciones de folllwoing para cambiar una única declaración de \ (o desactivada).</span><span class="sxs-lookup"><span data-stu-id="239af-290">Complete the folllwoing actions to toggle a single declaration on \(or off\).</span></span>  

1.  <span data-ttu-id="239af-291">[Seleccione un elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="239af-291">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="239af-292">En el panel **estilos** , desplace el puntero sobre la regla que define la declaración.</span><span class="sxs-lookup"><span data-stu-id="239af-292">In the **Styles** pane, hover over the rule that defines the declaration.</span></span>  <span data-ttu-id="239af-293">Aparece una casilla de verificación junto a cada declaración.</span><span class="sxs-lookup"><span data-stu-id="239af-293">A checkbox appears next to each declaration.</span></span>  
1.  <span data-ttu-id="239af-294">Active \ (o desactive \) la casilla junto a la declaración.</span><span class="sxs-lookup"><span data-stu-id="239af-294">Check \(or uncheck\) the checkbox next to the declaration.</span></span>  <span data-ttu-id="239af-295">Al desactivar una declaración, DevTools la cruza para indicar que ya no está activa.</span><span class="sxs-lookup"><span data-stu-id="239af-295">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="239af-296">En la siguiente ilustración, se `margin-top` ha desactivado la propiedad del elemento seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="239af-296">In the following figure, the `margin-top` property for the currently selected element has been toggled off.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Activar o desactivar una declaración" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   <span data-ttu-id="239af-298">Activar o desactivar una declaración</span><span class="sxs-lookup"><span data-stu-id="239af-298">Toggle a declaration</span></span>  
:::image-end:::  

### <span data-ttu-id="239af-299">Agregar una declaración de color de fondo</span><span class="sxs-lookup"><span data-stu-id="239af-299">Add a background-color declaration</span></span>  

<span data-ttu-id="239af-300">Complete las siguientes acciones para agregar una `background-color` declaración a un elemento.</span><span class="sxs-lookup"><span data-stu-id="239af-300">Complete the following actions to add a `background-color` declaration to an element.</span></span>  

1.  <span data-ttu-id="239af-301">Pase el puntero sobre la regla de estilo a la que desea agregar la `background-color` declaración.</span><span class="sxs-lookup"><span data-stu-id="239af-301">Hover over the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="239af-302">[Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="239af-302">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="239af-303">Elija **agregar color de fondo** \ ( ![ agregar color de fondo ][ImageAddBackgroundColorIcon] \).</span><span class="sxs-lookup"><span data-stu-id="239af-303">Choose **Add Background Color** \(![Add Background Color][ImageAddBackgroundColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Agregar color de fondo" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **<span data-ttu-id="239af-305">Agregar color de fondo</span><span class="sxs-lookup"><span data-stu-id="239af-305">Add Background Color</span></span>**  
:::image-end:::  

### <span data-ttu-id="239af-306">Agregar una declaración de color</span><span class="sxs-lookup"><span data-stu-id="239af-306">Add a color declaration</span></span>  

<span data-ttu-id="239af-307">Complete las siguientes acciones para agregar una `color` declaración a un elemento.</span><span class="sxs-lookup"><span data-stu-id="239af-307">Complete the following actions to add a `color` declaration to an element.</span></span>  

1.  <span data-ttu-id="239af-308">Pase el puntero sobre la regla de estilo a la que desea agregar la `color` declaración.</span><span class="sxs-lookup"><span data-stu-id="239af-308">Hover over the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="239af-309">[Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="239af-309">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="239af-310">Elija **agregar color** \ ( ![ agregar color ][ImageAddColorIcon] \).</span><span class="sxs-lookup"><span data-stu-id="239af-310">Choose **Add Color** \(![Add Color][ImageAddColorIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Agregar color" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **<span data-ttu-id="239af-312">Agregar color</span><span class="sxs-lookup"><span data-stu-id="239af-312">Add Color</span></span>**  
:::image-end:::  

### <span data-ttu-id="239af-313">Agregar una declaración de sombra de cuadro</span><span class="sxs-lookup"><span data-stu-id="239af-313">Add a box-shadow declaration</span></span>  

<span data-ttu-id="239af-314">Complete las siguientes acciones para agregar una `box-shadow` declaración a un elemento.</span><span class="sxs-lookup"><span data-stu-id="239af-314">Complete the follwoing actions to add a `box-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="239af-315">Pase el puntero sobre la regla de estilo a la que desea agregar la `box-shadow` declaración.</span><span class="sxs-lookup"><span data-stu-id="239af-315">Hover over the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="239af-316">[Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="239af-316">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="239af-317">Elija **Agregar, cuadro sombra** \ ( ![ cuadro de ][ImageAddBoxShadowIcon] adición).</span><span class="sxs-lookup"><span data-stu-id="239af-317">Choose **Add Box Shadow** \(![Add Box Shadow][ImageAddBoxShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Cuadro Agregar sombra" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **<span data-ttu-id="239af-319">Cuadro Agregar sombra</span><span class="sxs-lookup"><span data-stu-id="239af-319">Add Box Shadow</span></span>**  
:::image-end:::  

### <span data-ttu-id="239af-320">Agregar una declaración de sombra de texto</span><span class="sxs-lookup"><span data-stu-id="239af-320">Add a text-shadow declaration</span></span>  

<span data-ttu-id="239af-321">Complete las siguientes acciones para agregar una `text-shadow` declaración a un elemento.</span><span class="sxs-lookup"><span data-stu-id="239af-321">Complete the following actions to add a `text-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="239af-322">Pase el puntero sobre la regla de estilo a la que desea agregar la `text-shadow` declaración.</span><span class="sxs-lookup"><span data-stu-id="239af-322">Hover over the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="239af-323">[Mostrar la barra de herramientas **más acciones** ](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="239af-323">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="239af-324">Elija **Agregar sombra de texto** \ ( ![ Agregar sombra de texto ][ImageAddTextShadowIcon] ).</span><span class="sxs-lookup"><span data-stu-id="239af-324">Choose **Add Text Shadow** \(![Add Text Shadow][ImageAddTextShadowIcon]\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Agregar sombra de texto" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **<span data-ttu-id="239af-326">Agregar sombra de texto</span><span class="sxs-lookup"><span data-stu-id="239af-326">Add Text Shadow</span></span>**  
:::image-end:::  

### <span data-ttu-id="239af-327">Cambiar los colores con el selector de colores</span><span class="sxs-lookup"><span data-stu-id="239af-327">Change colors with the Color Picker</span></span>  

<span data-ttu-id="239af-328">El **selector de colores** proporciona una interfaz gráfica de usuario para el cambio `color` y las `background-color` declaraciones.</span><span class="sxs-lookup"><span data-stu-id="239af-328">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="239af-329">Complete las siguientes acciones para abrir el **selector de colores**.</span><span class="sxs-lookup"><span data-stu-id="239af-329">Complete the following actions to open the **Color Picker**.</span></span>  

1.  <span data-ttu-id="239af-330">[Seleccione un elemento](#select-an-element).</span><span class="sxs-lookup"><span data-stu-id="239af-330">[Select an element](#select-an-element).</span></span>  
1.  <span data-ttu-id="239af-331">En la pestaña **estilos** , busque la `color` `background-color` declaración similar que desea cambiar.</span><span class="sxs-lookup"><span data-stu-id="239af-331">In the **Styles** tab, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="239af-332">A la izquierda del `color` valor, `background-color` o similar, hay un pequeño cuadrado, que es una vista previa del color.</span><span class="sxs-lookup"><span data-stu-id="239af-332">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="239af-333">En la siguiente ilustración, el pequeño cuadrado situado a la izquierda de `rgba(0, 0, 0, 0.7)` es una versión preliminar de ese color.</span><span class="sxs-lookup"><span data-stu-id="239af-333">In the following figure, the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Vista previa del color" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       <span data-ttu-id="239af-335">Vista previa del color</span><span class="sxs-lookup"><span data-stu-id="239af-335">Color preview</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="239af-336">Elija la vista previa para abrir el **selector de colores**.</span><span class="sxs-lookup"><span data-stu-id="239af-336">Choose the preview to open the **Color Picker**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="El selector de colores" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       <span data-ttu-id="239af-338">El **selector de colores**</span><span class="sxs-lookup"><span data-stu-id="239af-338">The **Color Picker**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="239af-339">En la siguiente ilustración se muestra una lista de descries de cada uno de los elementos de la interfaz de usuario del **selector de colores**.</span><span class="sxs-lookup"><span data-stu-id="239af-339">The following figure and list descries of each of the UI elements of the **Color Picker**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="El selector de color, anotado" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   <span data-ttu-id="239af-341">El **selector de color**, anotado</span><span class="sxs-lookup"><span data-stu-id="239af-341">The **Color Picker**, annotated</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      <span data-ttu-id="239af-342">uno</span><span class="sxs-lookup"><span data-stu-id="239af-342">1</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="239af-343">Grada</span><span class="sxs-lookup"><span data-stu-id="239af-343">Shades</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="239af-344">1</span><span class="sxs-lookup"><span data-stu-id="239af-344">2</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="239af-345">Cuentagotas</span><span class="sxs-lookup"><span data-stu-id="239af-345">Eyedropper</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="239af-346">Para obtener más información, consulte [muestra de un color fuera de la página con el cuentagotas](#sample-a-color-off-the-page-with-the-eyedropper).</span><span class="sxs-lookup"><span data-stu-id="239af-346">For more information, see [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="239af-347">2</span><span class="sxs-lookup"><span data-stu-id="239af-347">3</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="239af-348">Copiar en el portapapeles</span><span class="sxs-lookup"><span data-stu-id="239af-348">Copy To Clipboard</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="239af-349">Copie el **valor para mostrar** en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="239af-349">Copy the **Display Value** to your clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="239af-350">cuatro</span><span class="sxs-lookup"><span data-stu-id="239af-350">4</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="239af-351">Valor para mostrar</span><span class="sxs-lookup"><span data-stu-id="239af-351">Display Value</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="239af-352">La representación RGBA, HSLA o hexadecimal del color.</span><span class="sxs-lookup"><span data-stu-id="239af-352">The RGBA, HSLA, or Hex representation of the color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="239af-353">4</span><span class="sxs-lookup"><span data-stu-id="239af-353">5</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="239af-354">Paleta de colores</span><span class="sxs-lookup"><span data-stu-id="239af-354">Color Palette</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="239af-355">Elija uno de los cuadrados para cambiar el color a ese cuadrado.</span><span class="sxs-lookup"><span data-stu-id="239af-355">Choose one of the squares to change the color to that square.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="239af-356">6</span><span class="sxs-lookup"><span data-stu-id="239af-356">6</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="239af-357">Altera</span><span class="sxs-lookup"><span data-stu-id="239af-357">Hue</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="239af-358">siete</span><span class="sxs-lookup"><span data-stu-id="239af-358">7</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="239af-359">Opacity</span><span class="sxs-lookup"><span data-stu-id="239af-359">Opacity</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="239af-360">4,8</span><span class="sxs-lookup"><span data-stu-id="239af-360">8</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="239af-361">Display Value Switcher</span><span class="sxs-lookup"><span data-stu-id="239af-361">Display Value Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="239af-362">Alternar entre las representaciones RGBA, HSLA y hexadecimal del color actual.</span><span class="sxs-lookup"><span data-stu-id="239af-362">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="239af-363">99,999</span><span class="sxs-lookup"><span data-stu-id="239af-363">9</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="239af-364">Conmutador de paleta de colores</span><span class="sxs-lookup"><span data-stu-id="239af-364">Color Palette Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="239af-365">Cambiar entre la [paleta de diseño de material][MaterialDesignColorSystem], una paleta personalizada o una paleta de colores de página.</span><span class="sxs-lookup"><span data-stu-id="239af-365">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="239af-366">DevTools genera la paleta de colores de la página en función de los colores que encuentre en las hojas de estilo.</span><span class="sxs-lookup"><span data-stu-id="239af-366">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="239af-367">Muestra un color de la página con el cuentagotas</span><span class="sxs-lookup"><span data-stu-id="239af-367">Sample a color off the page with the Eyedropper</span></span>  

<span data-ttu-id="239af-368">Al abrir el **selector de color**, el **cuentagotas** \ ( ![ cuentagotas ][ImageEyedropperIcon] \) está activado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="239af-368">When you open the **Color Picker**, the **Eyedropper** \(![Eyedropper][ImageEyedropperIcon]\) is on by default.</span></span>  <span data-ttu-id="239af-369">Complete las acciones siguientes para cambiar el color seleccionado a otro color de la página.</span><span class="sxs-lookup"><span data-stu-id="239af-369">Complete the following actions to change the selected color to some other color on the page.</span></span>  

1.  <span data-ttu-id="239af-370">Desplace el puntero sobre el color de destino en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="239af-370">Hover over the target color in the viewport.</span></span>  
1.  <span data-ttu-id="239af-371">Elija confirmar.</span><span class="sxs-lookup"><span data-stu-id="239af-371">Choose to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="239af-372">En la siguiente ilustración, el **selector de colores** muestra un valor de color actual de `rgba(0,0,0,0.7)` , que está cerca del negro.</span><span class="sxs-lookup"><span data-stu-id="239af-372">In the following figure, the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="239af-373">El color específico debe cambiar a la versión de negro que está resaltada en la ventanilla después de elegirla.</span><span class="sxs-lookup"><span data-stu-id="239af-373">The specific color should change to the version of black that is currently highlighted in the viewport after you chose it.</span></span>  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Usar el cuentagotas" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       <span data-ttu-id="239af-375">Usar el cuentagotas</span><span class="sxs-lookup"><span data-stu-id="239af-375">Using the Eyedropper</span></span>  
    :::image-end:::  
    
<!-- image links -->  

[ImageAddBackgroundColorIcon]: ../media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: ../media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: ../media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: ../media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: ../media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: ../media/select-an-element-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  
[DevToolsCSSGetStarted]: ../css/index.md "Introducción a la visualización y el cambio de CSS | Microsoft docs"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Agregar un PseudoState a una clase: Introducción a la visualización y el cambio de CSS | Microsoft docs"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Ver las CSS de un elemento: Introducción a la visualización y el cambio de CSS | Microsoft docs"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Forzar que Microsoft Edge DevTools al modo de vista previa de impresión (tipo de archivo CSS de impresión) | Microsoft docs"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#make-a-minified-file-readable "Hacer un archivo minified legible: referencia de depuración de JavaScript | Microsoft docs"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "El diseño de material del sistema de colores"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "El modelo de cuadro | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Especificidad de los tipos de selector | MDN"  

> [!NOTE]
> <span data-ttu-id="239af-385">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="239af-385">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="239af-386">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/reference) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="239af-386">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="239af-388">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="239af-388">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

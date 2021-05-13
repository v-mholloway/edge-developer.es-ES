---
description: Descubra nuevos flujos de trabajo para ver y cambiar CSS en Microsoft Edge DevTools.
title: Referencia de CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 0680b08c9809698c1db6c186a7be76a93c31df4b
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564479"
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
# <a name="css-reference"></a><span data-ttu-id="45c4b-104">Referencia de CSS</span><span class="sxs-lookup"><span data-stu-id="45c4b-104">CSS reference</span></span>  

<span data-ttu-id="45c4b-105">Descubra nuevos flujos de trabajo en la siguiente referencia completa de Microsoft Edge características de DevTools relacionadas con la visualización y el cambio de CSS.</span><span class="sxs-lookup"><span data-stu-id="45c4b-105">Discover new workflows in the following comprehensive reference of Microsoft Edge DevTools features related to viewing and changing CSS.</span></span>  

<span data-ttu-id="45c4b-106">Para obtener información básica, vaya a [Introducción con Ver y cambiar CSS][DevToolsCSSGetStarted].</span><span class="sxs-lookup"><span data-stu-id="45c4b-106">To learn the basics, navigate to [Get Started with Viewing and Changing CSS][DevToolsCSSGetStarted].</span></span>  

## <a name="choose-an-element"></a><span data-ttu-id="45c4b-107">Elegir un elemento</span><span class="sxs-lookup"><span data-stu-id="45c4b-107">Choose an element</span></span>  

<span data-ttu-id="45c4b-108">La **herramienta Elementos** de DevTools permite ver o cambiar el CSS de un elemento a la vez.</span><span class="sxs-lookup"><span data-stu-id="45c4b-108">The **Elements** tool of DevTools lets you view or change the CSS of one element at a time.</span></span>  <span data-ttu-id="45c4b-109">El elemento seleccionado se resalta en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="45c4b-109">The selected element is highlighted in the **DOM Tree**.</span></span>  <span data-ttu-id="45c4b-110">Los estilos del elemento se muestran en el **panel Estilos.**</span><span class="sxs-lookup"><span data-stu-id="45c4b-110">The styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="45c4b-111">Para obtener un tutorial, vaya [a Ver el CSS de un elemento][DevToolsCSSGetStartedTutorial].</span><span class="sxs-lookup"><span data-stu-id="45c4b-111">For a tutorial, navigate to [View the CSS for an element][DevToolsCSSGetStartedTutorial].</span></span>  

> [!NOTE]
> <span data-ttu-id="45c4b-112">En la siguiente figura, el elemento que se resalta `h1` en el árbol **DOM** es el elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="45c4b-112">In the following figure, the `h1` element that is highlighted in the **DOM Tree** is the selected element.</span></span>  <span data-ttu-id="45c4b-113">A la derecha, los estilos del elemento se muestran en el **panel Estilos.**</span><span class="sxs-lookup"><span data-stu-id="45c4b-113">On the right, the styles of the element are shown in the **Styles** pane.</span></span>  <span data-ttu-id="45c4b-114">A la izquierda, el elemento se resalta en la ventanilla, pero solo porque el mouse está activando el mouse sobre él en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="45c4b-114">On the left, the element is highlighted in the viewport, but only because the mouse is currently hovering over it in the **DOM Tree**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Un ejemplo de un elemento seleccionado" lightbox="../media/css-elements-styles-h1.msft.png":::
   <span data-ttu-id="45c4b-116">Un ejemplo de un elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="45c4b-116">An example of a selected element</span></span>  
:::image-end:::  

<span data-ttu-id="45c4b-117">Use una de las siguientes acciones para seleccionar un elemento.</span><span class="sxs-lookup"><span data-stu-id="45c4b-117">Use one the following actions to select an element.</span></span>  

*   <span data-ttu-id="45c4b-118">En la ventanilla, mantenga el mouse sobre el elemento, abra el menú contextual \(hacer clic con el botón secundario\) y elija **Inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="45c4b-118">In your viewport, hover on the element, open the contextual menu \(right-click\), and choose **Inspect**.</span></span>  
*   <span data-ttu-id="45c4b-119">En DevTools, elija **Seleccionar** un elemento \( Seleccionar un elemento \) o seleccione ![ ](../media/select-an-element-icon.msft.png) `Control` + `Shift` + `C` \(Windows, Linux\) o `Command` + `Shift` + `C` \(macOS\) y, a continuación, elija el elemento en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="45c4b-119">In DevTools, choose **Select an element** \(![Select an element](../media/select-an-element-icon.msft.png)\) or select `Control`+`Shift`+`C` \(Windows, Linux\) or `Command`+`Shift`+`C` \(macOS\), and then choose the element in the viewport.</span></span>  
*   <span data-ttu-id="45c4b-120">En DevTools, elija el elemento en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="45c4b-120">In DevTools, choose the element in the **DOM Tree**.</span></span>  
*   <span data-ttu-id="45c4b-121">En DevTools, ejecute una consulta como en la consola , mantenga el mouse sobre el resultado, abra el menú contextual \(haga clic con el botón secundario en\) y elija Mostrar en el `document.querySelector('p')` **panel Elementos**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="45c4b-121">In DevTools, run a query like `document.querySelector('p')` in the **Console**, hover on the result, open the contextual menu \(right-click\), and choose **Reveal in Elements panel**.</span></span>  

## <a name="view-css"></a><span data-ttu-id="45c4b-122">Ver CSS</span><span class="sxs-lookup"><span data-stu-id="45c4b-122">View CSS</span></span>  

### <a name="view-the-external-stylesheet-where-a-rule-is-defined"></a><span data-ttu-id="45c4b-123">Ver la hoja de estilos externa donde se define una regla</span><span class="sxs-lookup"><span data-stu-id="45c4b-123">View the external stylesheet where a rule is defined</span></span>  

<span data-ttu-id="45c4b-124">En el **panel Estilos,** elija el vínculo junto a una regla CSS para abrir la hoja de estilos externa que define la regla.</span><span class="sxs-lookup"><span data-stu-id="45c4b-124">In the **Styles** pane, choose the link next to a CSS rule to open the external stylesheet that defines the rule.</span></span>  <span data-ttu-id="45c4b-125">La hoja de estilos se abre en el **panel Editor** de la **herramienta** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="45c4b-125">The stylesheet opens in the **Editor** pane of the **Sources** tool.</span></span>  

<span data-ttu-id="45c4b-126">Si la hoja de estilos está minificada, elija el botón **Formato** \( Formato \) en la parte ![ inferior del ](../media/format-icon.msft.png) **panel** Editor.</span><span class="sxs-lookup"><span data-stu-id="45c4b-126">If the stylesheet is minified, choose the **Format** \(![Format](../media/format-icon.msft.png)\) button, at the bottom of the **Editor** pane.</span></span>  <span data-ttu-id="45c4b-127">Para obtener más información, vaya [a Volver a formatear un archivo JavaScript minificado con pretty-print][DevToolsJavascriptReferenceFormat].</span><span class="sxs-lookup"><span data-stu-id="45c4b-127">For more information, navigate to [Reformat a minified JavaScript file with pretty-print][DevToolsJavascriptReferenceFormat].</span></span>  

> [!NOTE]
> <span data-ttu-id="45c4b-128">En la siguiente figura, después de elegir, se le toma a la línea 2 de , donde se define la `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` regla `.content h1:first-of-type` CSS.</span><span class="sxs-lookup"><span data-stu-id="45c4b-128">In the following figure, after you choose `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` you are taken to line 2 of `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css`, where the `.content h1:first-of-type` CSS rule is defined.</span></span>  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Visualización de la hoja de estilos donde se define una regla" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  <span data-ttu-id="45c4b-130">Visualización de la hoja de estilos donde se define una regla</span><span class="sxs-lookup"><span data-stu-id="45c4b-130">Viewing the stylesheet where a rule is defined</span></span>  
:::image-end:::  

### <a name="view-only-the-css-that-is-actually-applied-to-an-element"></a><span data-ttu-id="45c4b-131">Ver solo el CSS que se aplica realmente a un elemento</span><span class="sxs-lookup"><span data-stu-id="45c4b-131">View only the CSS that is actually applied to an element</span></span>  

<span data-ttu-id="45c4b-132">El panel **Estilos** muestra todas las reglas que se aplican a un elemento, incluidas las declaraciones que se han invalidado.</span><span class="sxs-lookup"><span data-stu-id="45c4b-132">The **Styles** panel shows you all of the rules that apply to an element, including declarations that have been overridden.</span></span>  <span data-ttu-id="45c4b-133">Cuando no esté interesado en las declaraciones invalidadas, use el **panel** Calculado para ver solo el CSS que realmente se está aplicando a un elemento.</span><span class="sxs-lookup"><span data-stu-id="45c4b-133">When you are not interested in overridden declarations, use the **Computed** panel to view only the CSS that is actually being applied to an element.</span></span>  

1.  <span data-ttu-id="45c4b-134">[Seleccione un elemento](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="45c4b-134">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="45c4b-135">Vaya al panel **Calculado** de la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="45c4b-135">Navigate to the **Computed** panel in the **Elements** tool.</span></span>  

> [!NOTE]
> <span data-ttu-id="45c4b-136">En una ventana de DevTools amplia, el panel **Calculado** no existe.</span><span class="sxs-lookup"><span data-stu-id="45c4b-136">On a wide DevTools window, the **Computed** panel does not exist.</span></span>  <span data-ttu-id="45c4b-137">El contenido del panel **Calculado** se muestra en el panel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="45c4b-137">The contents of the **Computed** panel are shown on the **Styles** panel.</span></span>  

<span data-ttu-id="45c4b-138">Las propiedades heredadas son opacas.</span><span class="sxs-lookup"><span data-stu-id="45c4b-138">Inherited properties are opaque.</span></span>  <span data-ttu-id="45c4b-139">Para mostrar todos los valores heredados, active la **casilla Mostrar todo.**</span><span class="sxs-lookup"><span data-stu-id="45c4b-139">To display all inherited values, select the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="45c4b-140">En la siguiente figura, el panel **Calculado** muestra las propiedades CSS que se aplican al elemento seleccionado `h1` actualmente.</span><span class="sxs-lookup"><span data-stu-id="45c4b-140">In the following figure, the **Computed** panel shows the CSS properties being applied to the currently-selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="Panel calculado" lightbox="../media/css-elements-computed-h1.msft.png":::
   <span data-ttu-id="45c4b-142">Panel **calculado**</span><span class="sxs-lookup"><span data-stu-id="45c4b-142">The **Computed** panel</span></span>  
:::image-end:::  

### <a name="view-css-properties-in-alphabetical-order"></a><span data-ttu-id="45c4b-143">Ver propiedades CSS en orden alfabético</span><span class="sxs-lookup"><span data-stu-id="45c4b-143">View CSS properties in alphabetical order</span></span>  

<span data-ttu-id="45c4b-144">Use el panel **Calculado.**</span><span class="sxs-lookup"><span data-stu-id="45c4b-144">Use the **Computed** panel.</span></span>  <span data-ttu-id="45c4b-145">Navegue a [Ver solo el CSS que se aplica realmente a un elemento](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="45c4b-145">Navigate to [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <a name="view-inherited-css-properties"></a><span data-ttu-id="45c4b-146">Ver propiedades CSS heredadas</span><span class="sxs-lookup"><span data-stu-id="45c4b-146">View inherited CSS properties</span></span>  

<span data-ttu-id="45c4b-147">Active la **casilla Mostrar todo** en el panel **Calculado.**</span><span class="sxs-lookup"><span data-stu-id="45c4b-147">Check the **Show All** checkbox in the **Computed** panel.</span></span>  <span data-ttu-id="45c4b-148">Navegue a [Ver solo el CSS que se aplica realmente a un elemento](#view-only-the-css-that-is-actually-applied-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="45c4b-148">Navigate to [View only the CSS that is actually applied to an element](#view-only-the-css-that-is-actually-applied-to-an-element).</span></span>  

### <a name="view-the-box-model-for-an-element"></a><span data-ttu-id="45c4b-149">Ver el modelo de cuadro de un elemento</span><span class="sxs-lookup"><span data-stu-id="45c4b-149">View the box model for an element</span></span>  

<span data-ttu-id="45c4b-150">Para ver [el modelo de cuadro][MDNBoxModel] de un elemento, vaya al panel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="45c4b-150">To view [the box model][MDNBoxModel] of an element, navigate to the **Styles** panel.</span></span>  <span data-ttu-id="45c4b-151">Si la ventana DevTools es estrecha, el diagrama **modelo** de cuadro se encuentra en la parte inferior del panel.</span><span class="sxs-lookup"><span data-stu-id="45c4b-151">If your DevTools window is narrow, the **Box Model** diagram is at the bottom of the panel.</span></span>  

<span data-ttu-id="45c4b-152">Elija y edite en un valor para cambiar un valor.</span><span class="sxs-lookup"><span data-stu-id="45c4b-152">Choose and edit on a value to change a value.</span></span>  

> [!NOTE]
> <span data-ttu-id="45c4b-153">En la siguiente figura, el diagrama **Modelo de** cuadro del panel **Estilos** muestra el modelo de cuadro para el elemento `h1` seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="45c4b-153">In the following figure, the **Box Model** diagram in the **Styles** panel shows the box model for the currently selected `h1` element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="Diagrama del modelo de cuadro" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   <span data-ttu-id="45c4b-155">Diagrama **del modelo de** cuadro</span><span class="sxs-lookup"><span data-stu-id="45c4b-155">The **Box Model** diagram</span></span>  
:::image-end:::  

### <a name="search-and-filter-the-css-of-an-element"></a><span data-ttu-id="45c4b-156">Buscar y filtrar el CSS de un elemento</span><span class="sxs-lookup"><span data-stu-id="45c4b-156">Search and filter the CSS of an element</span></span>  

<span data-ttu-id="45c4b-157">Use el **cuadro de** texto Filtrar de los paneles **Estilos** y **Calculados** para buscar valores o propiedades CSS específicos.</span><span class="sxs-lookup"><span data-stu-id="45c4b-157">Use the **Filter** text box on the **Styles** and **Computed** panels to search for specific CSS properties or values.</span></span>  

<span data-ttu-id="45c4b-158">Para buscar también propiedades heredadas en el panel **Calculado,** active la casilla **Mostrar todo.**</span><span class="sxs-lookup"><span data-stu-id="45c4b-158">To also search inherited properties in the **Computed** panel, check the **Show All** checkbox.</span></span>  

> [!NOTE]
> <span data-ttu-id="45c4b-159">En la siguiente figura, el panel **Estilos** se filtra para mostrar solo las reglas que incluyen la consulta de búsqueda `color` .</span><span class="sxs-lookup"><span data-stu-id="45c4b-159">In the following figure, the **Styles** panel is filtered to only show rules that include the search query `color`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Filtrar el panel Estilos" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   <span data-ttu-id="45c4b-161">Filtrar el panel **Estilos**</span><span class="sxs-lookup"><span data-stu-id="45c4b-161">Filter the **Styles** panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="45c4b-162">En la siguiente figura, **el** panel Calculado se filtra para mostrar solo las declaraciones que incluyen la consulta de búsqueda `100%` .</span><span class="sxs-lookup"><span data-stu-id="45c4b-162">In the following figure, the **Computed** panel is filtered to only show declarations that include the search query `100%`.</span></span>  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Filtrar el panel calculado" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   <span data-ttu-id="45c4b-164">Filtrar el panel **calculado**</span><span class="sxs-lookup"><span data-stu-id="45c4b-164">Filter the **Computed** panel</span></span>  
:::image-end:::  

### <a name="toggle-a-pseudo-class"></a><span data-ttu-id="45c4b-165">Alternar una pseudo-clase</span><span class="sxs-lookup"><span data-stu-id="45c4b-165">Toggle a pseudo-class</span></span>  

<span data-ttu-id="45c4b-166">Complete las siguientes acciones para alternar una pseudo-clase como `:active` , `:focus` , o `:hover` `:visited` .</span><span class="sxs-lookup"><span data-stu-id="45c4b-166">Complete the following actions to toggle a pseudo-class like `:active`, `:focus`, `:hover`, or `:visited`.</span></span>  

1.  <span data-ttu-id="45c4b-167">[Seleccione un elemento](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="45c4b-167">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="45c4b-168">En la **herramienta Elementos,** vaya al panel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="45c4b-168">On the **Elements** tool, navigate to the **Styles** panel.</span></span>  
1.  <span data-ttu-id="45c4b-169">Elija **:hov**.</span><span class="sxs-lookup"><span data-stu-id="45c4b-169">Choose **:hov**.</span></span>  
1.  <span data-ttu-id="45c4b-170">Compruebe la pseudo-clase que desea habilitar.</span><span class="sxs-lookup"><span data-stu-id="45c4b-170">Check the pseudo-class that you want to enable.</span></span>  

> [!NOTE]
> <span data-ttu-id="45c4b-171">En la siguiente figura, alterna la `:hover` pseudo-clase.</span><span class="sxs-lookup"><span data-stu-id="45c4b-171">In the following figure, toggle the `:hover` pseudo-class.</span></span>  <span data-ttu-id="45c4b-172">En la ventanilla, compruebe que la declaración se aplica al elemento, aunque el elemento no `background-color: cornflowerblue` esté activando.</span><span class="sxs-lookup"><span data-stu-id="45c4b-172">In the viewport verify that the `background-color: cornflowerblue` declaration is being applied to the element, even though the element is not actually being hovered over.</span></span>  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Alternar la pseudo-clase :hover" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   <span data-ttu-id="45c4b-174">Alternar la `:hover` pseudo-clase</span><span class="sxs-lookup"><span data-stu-id="45c4b-174">Toggle the `:hover` pseudo-class</span></span>  
:::image-end:::  

<span data-ttu-id="45c4b-175">Para obtener un tutorial interactivo, vaya [a Agregar un pseudoestado a una clase][DevToolsCSSGetStartedAddPseudoState].</span><span class="sxs-lookup"><span data-stu-id="45c4b-175">For an interactive tutorial, navigate to [Add a pseudostate to a class][DevToolsCSSGetStartedAddPseudoState].</span></span>  

### <a name="view-a-page-in-print-mode"></a><span data-ttu-id="45c4b-176">Ver una página en modo de impresión</span><span class="sxs-lookup"><span data-stu-id="45c4b-176">View a page in print mode</span></span>  

<span data-ttu-id="45c4b-177">Complete las siguientes acciones para ver una página en modo de impresión.</span><span class="sxs-lookup"><span data-stu-id="45c4b-177">Complete the following actions to view a page in print mode.</span></span>  

1.  <span data-ttu-id="45c4b-178">[Abra el menú de comandos][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="45c4b-178">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="45c4b-179">Comience a escribir `Rendering` y seleccione `Show Rendering` .</span><span class="sxs-lookup"><span data-stu-id="45c4b-179">Start typing `Rendering` and select `Show Rendering`.</span></span>  
1.  <span data-ttu-id="45c4b-180">Para el desplegable **Emular medios CSS,** elija **imprimir**.</span><span class="sxs-lookup"><span data-stu-id="45c4b-180">For the **Emulate CSS Media** dropdown, choose **print**.</span></span>  

### <a name="view-used-and-unused-css-with-the-coverage-tool"></a><span data-ttu-id="45c4b-181">Ver CSS usado y sin usar con la herramienta Cobertura</span><span class="sxs-lookup"><span data-stu-id="45c4b-181">View used and unused CSS with the Coverage tool</span></span>  

<span data-ttu-id="45c4b-182">La **herramienta Cobertura** muestra qué CSS usa realmente una página.</span><span class="sxs-lookup"><span data-stu-id="45c4b-182">The **Coverage** tool shows you what CSS a page actually uses.</span></span>  

1.  <span data-ttu-id="45c4b-183">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) mientras DevTools [][DevToolsCommandMenu]está centrado para abrir el menú de comandos .</span><span class="sxs-lookup"><span data-stu-id="45c4b-183">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) while DevTools is in focus to [open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="45c4b-184">Empiece a escribir `coverage` y elija Mostrar **cobertura**.</span><span class="sxs-lookup"><span data-stu-id="45c4b-184">Start typing `coverage` and choose **Show Coverage**.</span></span>  <span data-ttu-id="45c4b-185">Aparece **la herramienta** Cobertura.</span><span class="sxs-lookup"><span data-stu-id="45c4b-185">The **Coverage** tool appears.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Abrir la herramienta Cobertura desde el menú comando" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             <span data-ttu-id="45c4b-187">Abra la **herramienta Cobertura** desde el **menú Comando**</span><span class="sxs-lookup"><span data-stu-id="45c4b-187">Open the **Coverage** tool from the **Command Menu**</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="La herramienta Cobertura" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             <span data-ttu-id="45c4b-189">La **herramienta Cobertura**</span><span class="sxs-lookup"><span data-stu-id="45c4b-189">The **Coverage** tool</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="45c4b-190">Elija **Iniciar la cobertura de instrumentación y actualizar la página** \( Iniciar la ![ instrumentación de la cobertura y actualizar la página ](../media/refresh-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="45c4b-190">Choose **Start instrumenting coverage and refresh the page** \(![Start instrumenting coverage and refresh the page](../media/refresh-icon.msft.png)\).</span></span>  <span data-ttu-id="45c4b-191">La página se actualiza y la herramienta **Cobertura** proporciona una introducción a la cantidad de CSS \(y JavaScript\) que se usa en cada archivo que carga el explorador.</span><span class="sxs-lookup"><span data-stu-id="45c4b-191">The page refreshes and the **Coverage** tool provides an overview of how much CSS \(and JavaScript\) is used from each file that the browser loads.</span></span>  <span data-ttu-id="45c4b-192">El color verde representa CSS usado.</span><span class="sxs-lookup"><span data-stu-id="45c4b-192">Green represents used CSS.</span></span>  <span data-ttu-id="45c4b-193">El rojo representa CSS sin usar.</span><span class="sxs-lookup"><span data-stu-id="45c4b-193">Red represents unused CSS.</span></span>  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Información general sobre la cantidad de CSS (y JavaScript) que se usa y no se usa" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       <span data-ttu-id="45c4b-195">Información general sobre la cantidad de CSS \(y JavaScript\) que se usa y no se usa.</span><span class="sxs-lookup"><span data-stu-id="45c4b-195">An overview of how much CSS \(and JavaScript\) is used and unused</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="45c4b-196">Para mostrar un desglose línea por línea de lo que se usa CSS, elija un archivo CSS.</span><span class="sxs-lookup"><span data-stu-id="45c4b-196">To display a line-by-line breakdown of what CSS is used, choose a CSS file.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="45c4b-197">En la siguiente figura, no se usan las líneas 145 a 147 y de 149 a 151, mientras que se usan las líneas `b66bc881.site-ltr.css` 163 a 166.</span><span class="sxs-lookup"><span data-stu-id="45c4b-197">In the following figure, lines 145 to 147 and 149 to 151 of `b66bc881.site-ltr.css` are unused, whereas lines 163 to 166 are used.</span></span>  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Desglose línea por línea de CSS usado y no usado" lightbox="../media/css-sources-css-coverage.msft.png":::
       <span data-ttu-id="45c4b-199">Desglose línea por línea de CSS usado y no usado</span><span class="sxs-lookup"><span data-stu-id="45c4b-199">A line-by-line breakdown of used and unused CSS</span></span>  
    :::image-end:::  
    
### <a name="force-print-preview-mode"></a><span data-ttu-id="45c4b-200">Forzar el modo de vista previa de impresión</span><span class="sxs-lookup"><span data-stu-id="45c4b-200">Force print preview mode</span></span>  

<span data-ttu-id="45c4b-201">Vaya a [Forzar DevTools al modo de vista previa de impresión.][DevToolsCssPrintPreview]</span><span class="sxs-lookup"><span data-stu-id="45c4b-201">Navigate to [Force DevTools into Print Preview mode][DevToolsCssPrintPreview].</span></span>  

## <a name="change-css"></a><span data-ttu-id="45c4b-202">Cambiar CSS</span><span class="sxs-lookup"><span data-stu-id="45c4b-202">Change CSS</span></span>  

<!-- todo s/CSS declaration/declaration/ -->  

### <a name="add-a-css-declaration-to-an-element"></a><span data-ttu-id="45c4b-203">Agregar una declaración CSS a un elemento</span><span class="sxs-lookup"><span data-stu-id="45c4b-203">Add a CSS declaration to an element</span></span>  

<span data-ttu-id="45c4b-204">El orden de las declaraciones afecta al estilo de un elemento, use la siguiente lista para ayudarle a agregar declaraciones de diferentes maneras.</span><span class="sxs-lookup"><span data-stu-id="45c4b-204">The order of declarations affects how an element is styled, use the following list to help you add declarations in different ways.</span></span>  

*   <span data-ttu-id="45c4b-205">[Agregue una declaración en línea](#add-an-inline-declaration).</span><span class="sxs-lookup"><span data-stu-id="45c4b-205">[Add a inline declaration](#add-an-inline-declaration).</span></span>  <span data-ttu-id="45c4b-206">Equivale a agregar `style` un atributo al HTML de un elemento.</span><span class="sxs-lookup"><span data-stu-id="45c4b-206">Equivalent to adding a `style` attribute to the HTML of an element.</span></span>  
*   <span data-ttu-id="45c4b-207">[Agregar una declaración a una regla de estilo](#add-a-declaration-to-a-style-rule).</span><span class="sxs-lookup"><span data-stu-id="45c4b-207">[Add a declaration to a style rule](#add-a-declaration-to-a-style-rule).</span></span>  

**<span data-ttu-id="45c4b-208">¿Qué flujo de trabajo debe usar?</span><span class="sxs-lookup"><span data-stu-id="45c4b-208">What workflow should you use?</span></span>** <span data-ttu-id="45c4b-209">Para la mayoría de los escenarios, probablemente quiera usar el flujo de trabajo de declaración en línea.</span><span class="sxs-lookup"><span data-stu-id="45c4b-209">For most scenarios, you probably want to use the inline declaration workflow.</span></span>  <span data-ttu-id="45c4b-210">Las declaraciones en línea tienen mayor especificidad que las externas, por lo que el flujo de trabajo en línea garantiza que los cambios tengan efecto en el elemento esperado.</span><span class="sxs-lookup"><span data-stu-id="45c4b-210">Inline declarations have higher specificity than external ones, so the inline workflow ensures that the changes take effect in your expected element.</span></span>  <span data-ttu-id="45c4b-211">Para obtener más información acerca de la especificidad, vaya a [Tipos de selector][MDNSelectorTypes].</span><span class="sxs-lookup"><span data-stu-id="45c4b-211">For more information about specificity, navigate to [Selector Types][MDNSelectorTypes].</span></span>  

<span data-ttu-id="45c4b-212">Si va a depurar cualquier estilo del elemento y necesita probar específicamente lo que sucede cuando una declaración se define en lugares diferentes, use el otro flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="45c4b-212">If you are debugging any styles of the element and you need to specifically test what happens when a declaration is defined in different places, use the other workflow.</span></span>  

#### <a name="add-an-inline-declaration"></a><span data-ttu-id="45c4b-213">Agregar una declaración en línea</span><span class="sxs-lookup"><span data-stu-id="45c4b-213">Add an inline declaration</span></span>  

<span data-ttu-id="45c4b-214">Complete las siguientes acciones para agregar una declaración en línea.</span><span class="sxs-lookup"><span data-stu-id="45c4b-214">Complete the following actions to add an inline declaration.</span></span>  

1.  <span data-ttu-id="45c4b-215">[Seleccione un elemento](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="45c4b-215">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="45c4b-216">En el **panel Estilos,** elija entre los corchetes de la **sección element.style.**</span><span class="sxs-lookup"><span data-stu-id="45c4b-216">In the **Styles** pane, choose between the brackets of the **element.style** section.</span></span>  <span data-ttu-id="45c4b-217">El cursor se centra, lo que permite escribir texto.</span><span class="sxs-lookup"><span data-stu-id="45c4b-217">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="45c4b-218">Escriba un nombre de propiedad y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="45c4b-218">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="45c4b-219">Escriba un valor válido para esa propiedad y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="45c4b-219">Enter a valid value for that property and select `Enter`.</span></span>  <span data-ttu-id="45c4b-220">En el **árbol DOM**, compruebe que se ha agregado un atributo `style` al elemento.</span><span class="sxs-lookup"><span data-stu-id="45c4b-220">In the **DOM Tree**, verify that a `style` attribute has been added to the element.</span></span>  

> [!NOTE]
> <span data-ttu-id="45c4b-221">En la siguiente figura, las `margin-top` propiedades y se han aplicado al elemento `background-color` seleccionado.</span><span class="sxs-lookup"><span data-stu-id="45c4b-221">In the following figure, the `margin-top` and `background-color` properties have been applied to the selected element.</span></span>  <span data-ttu-id="45c4b-222">En el **árbol DOM,** compruebe que las declaraciones se reflejan en el `style` atributo de un elemento.</span><span class="sxs-lookup"><span data-stu-id="45c4b-222">In the **DOM Tree** verify that the declarations are reflected in the `style` attribute for an element.</span></span>  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Agregar declaraciones en línea" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   <span data-ttu-id="45c4b-224">Agregar declaraciones en línea</span><span class="sxs-lookup"><span data-stu-id="45c4b-224">Add inline declarations</span></span>  
:::image-end:::  

#### <a name="add-a-declaration-to-a-style-rule"></a><span data-ttu-id="45c4b-225">Agregar una declaración a una regla de estilo</span><span class="sxs-lookup"><span data-stu-id="45c4b-225">Add a declaration to a style rule</span></span>  

<span data-ttu-id="45c4b-226">Complete las siguientes acciones para agregar una declaración a una regla de estilo existente.</span><span class="sxs-lookup"><span data-stu-id="45c4b-226">Complete the following actions to add a declaration to an existing style rule.</span></span>  

1.  <span data-ttu-id="45c4b-227">[Seleccione un elemento](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="45c4b-227">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="45c4b-228">En el **panel Estilos,** elija entre los corchetes de la regla de estilo a la que desea agregar la declaración.</span><span class="sxs-lookup"><span data-stu-id="45c4b-228">In the **Styles** pane, choose between the brackets of the style rule to which you want to add the declaration.</span></span>  <span data-ttu-id="45c4b-229">El cursor se centra, lo que permite escribir texto.</span><span class="sxs-lookup"><span data-stu-id="45c4b-229">The cursor focuses, allowing you to enter text.</span></span>  
1.  <span data-ttu-id="45c4b-230">Escriba un nombre de propiedad y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="45c4b-230">Enter a property name and select `Enter`.</span></span>  
1.  <span data-ttu-id="45c4b-231">Escriba un valor válido para esa propiedad y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="45c4b-231">Enter a valid value for that property and select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Agregar una declaración a una regla de estilo" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   <span data-ttu-id="45c4b-233">Agregar la `border-bottom-style:groove` declaración a una regla de estilo</span><span class="sxs-lookup"><span data-stu-id="45c4b-233">Add the `border-bottom-style:groove` declaration to a style rule</span></span>  
:::image-end:::  

### <a name="change-a-declaration-name-or-value"></a><span data-ttu-id="45c4b-234">Cambiar un nombre o valor de declaración</span><span class="sxs-lookup"><span data-stu-id="45c4b-234">Change a declaration name or value</span></span>  

<span data-ttu-id="45c4b-235">Elija y edite el nombre o el valor de una declaración para cambiarla.</span><span class="sxs-lookup"><span data-stu-id="45c4b-235">Choose and edit the name or value of a declaration to change it.</span></span>  <span data-ttu-id="45c4b-236">Para obtener accesos directos para incrementar o disminuir rápidamente un valor por , , , o unidades, vaya a Cambiar valores de declaración con `0.1` `1` `10` `100` [métodos abreviados de teclado.](#change-declaration-values-with-keyboard-shortcuts)</span><span class="sxs-lookup"><span data-stu-id="45c4b-236">For shortcuts for quickly incrementing or decrementing a value by `0.1`, `1`, `10`, or `100` units, navigate to [Change declaration values with keyboard shortcuts](#change-declaration-values-with-keyboard-shortcuts).</span></span>  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Cambiar el valor de una declaración" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   <span data-ttu-id="45c4b-238">Cambiar el valor de la `border-bottom-style` declaración</span><span class="sxs-lookup"><span data-stu-id="45c4b-238">Change the value of the `border-bottom-style` declaration</span></span>  
:::image-end:::  

### <a name="change-declaration-values-with-keyboard-shortcuts"></a><span data-ttu-id="45c4b-239">Cambiar valores de declaración con métodos abreviados de teclado</span><span class="sxs-lookup"><span data-stu-id="45c4b-239">Change declaration values with keyboard shortcuts</span></span>  

<span data-ttu-id="45c4b-240">Al editar el valor de una declaración, puede usar los siguientes métodos abreviados de teclado para incrementar el valor en una cantidad específica.</span><span class="sxs-lookup"><span data-stu-id="45c4b-240">While editing the value of a declaration, you may use the following keyboard shortcuts to increment the value by a specific amount.</span></span>  

*   <span data-ttu-id="45c4b-241">Seleccione `Alt` + `Up` \(Windows, Linux\) o `Option` + `Up` \(macOS\) para incrementar por `0.1` .</span><span class="sxs-lookup"><span data-stu-id="45c4b-241">Select `Alt`+`Up` \(Windows, Linux\) or `Option`+`Up` \(macOS\) to increment by `0.1`.</span></span>  
*   <span data-ttu-id="45c4b-242">Seleccione `Up` para cambiar el valor por , o por si el valor actual está entre y `1` `0.1` `-1` `1` .</span><span class="sxs-lookup"><span data-stu-id="45c4b-242">Select `Up` to change the value by `1`, or by `0.1` if the current value is between `-1` and `1`.</span></span>  
*   <span data-ttu-id="45c4b-243">Seleccione `Shift` + `Up` para incrementar por `10` .</span><span class="sxs-lookup"><span data-stu-id="45c4b-243">Select `Shift`+`Up` to increment by `10`.</span></span>  
*   <span data-ttu-id="45c4b-244">Seleccione `Shift` + `Page Up` \(Windows, Linux\) o `Shift` + `Command` + `Up` \(macOS\) para incrementar el valor por `100` .</span><span class="sxs-lookup"><span data-stu-id="45c4b-244">Select `Shift`+`Page Up` \(Windows, Linux\) or `Shift`+`Command`+`Up` \(macOS\) to increment the value by `100`.</span></span>  

<span data-ttu-id="45c4b-245">La decrementación también funciona.</span><span class="sxs-lookup"><span data-stu-id="45c4b-245">Decrementing also works.</span></span>  <span data-ttu-id="45c4b-246">Solo tiene que reemplazar cada instancia de `Up` la mencionada anteriormente por `Down` .</span><span class="sxs-lookup"><span data-stu-id="45c4b-246">Just replace each instance of `Up` mentioned above with `Down`.</span></span>  

### <a name="add-a-class-to-an-element"></a><span data-ttu-id="45c4b-247">Agregar una clase a un elemento</span><span class="sxs-lookup"><span data-stu-id="45c4b-247">Add a class to an element</span></span>  

<span data-ttu-id="45c4b-248">Complete las siguientes acciones para agregar una clase a un elemento.</span><span class="sxs-lookup"><span data-stu-id="45c4b-248">Complete the following actions to add a class to an element.</span></span>  

1.  <span data-ttu-id="45c4b-249">[Seleccione el elemento](#choose-an-element) en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="45c4b-249">[Select the element](#choose-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="45c4b-250">Elija **.cls**.</span><span class="sxs-lookup"><span data-stu-id="45c4b-250">Choose **.cls**.</span></span>  
1.  <span data-ttu-id="45c4b-251">Escriba el nombre de la clase en el **cuadro de** texto Agregar nueva clase.</span><span class="sxs-lookup"><span data-stu-id="45c4b-251">Enter the name of the class in the **Add New Class** text box.</span></span>  
1.  <span data-ttu-id="45c4b-252">Seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="45c4b-252">Select `Enter`.</span></span>  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Panel Clases de elementos" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   <span data-ttu-id="45c4b-254">Panel **Clases de** elementos</span><span class="sxs-lookup"><span data-stu-id="45c4b-254">The **Element Classes** pane</span></span>  
:::image-end:::  

### <a name="toggle-a-class"></a><span data-ttu-id="45c4b-255">Alternar una clase</span><span class="sxs-lookup"><span data-stu-id="45c4b-255">Toggle a class</span></span>  

<span data-ttu-id="45c4b-256">Complete las siguientes acciones para habilitar o deshabilitar una clase en un elemento.</span><span class="sxs-lookup"><span data-stu-id="45c4b-256">Complete the following actions to enable or disable a class on an element.</span></span>  

1.  <span data-ttu-id="45c4b-257">[Seleccione el elemento](#choose-an-element) en el **árbol DOM**.</span><span class="sxs-lookup"><span data-stu-id="45c4b-257">[Select the element](#choose-an-element) in the **DOM Tree**.</span></span>  
1.  <span data-ttu-id="45c4b-258">Abra el **panel Clases de** elementos.</span><span class="sxs-lookup"><span data-stu-id="45c4b-258">Open the **Element Classes** pane.</span></span>  <span data-ttu-id="45c4b-259">Vaya [a Agregar una clase a un elemento](#add-a-class-to-an-element).</span><span class="sxs-lookup"><span data-stu-id="45c4b-259">Navigate to [Add a class to an element](#add-a-class-to-an-element).</span></span>  <span data-ttu-id="45c4b-260">Debajo **del cuadro de texto Agregar** nueva clase se encuentran todas las clases aplicadas al elemento específico.</span><span class="sxs-lookup"><span data-stu-id="45c4b-260">Below the **Add New Class** text box are all of the classes applied to the specific element.</span></span>  
1.  <span data-ttu-id="45c4b-261">Activa o desactiva la casilla situada junto a la clase que quieras activar o desactivar.</span><span class="sxs-lookup"><span data-stu-id="45c4b-261">Toggle the checkbox next to the class that you want to turn on or off.</span></span>  

### <a name="add-a-style-rule"></a><span data-ttu-id="45c4b-262">Agregar una regla de estilo</span><span class="sxs-lookup"><span data-stu-id="45c4b-262">Add a style rule</span></span>  

<span data-ttu-id="45c4b-263">Complete las siguientes acciones para agregar una nueva regla de estilo.</span><span class="sxs-lookup"><span data-stu-id="45c4b-263">Complete the following actions to add a new style rule.</span></span>  

1.  <span data-ttu-id="45c4b-264">[Seleccione un elemento](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="45c4b-264">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="45c4b-265">Elija **Nueva regla de estilo** \( Nueva regla de estilo ![ ](../media/new-style-rule-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="45c4b-265">Choose **New Style Rule** \(![New Style Rule](../media/new-style-rule-icon.msft.png)\).</span></span>  <span data-ttu-id="45c4b-266">DevTools inserta una nueva regla debajo de la **regla element.style.**</span><span class="sxs-lookup"><span data-stu-id="45c4b-266">DevTools inserts a new rule beneath the **element.style** rule.</span></span>  

> [!NOTE]
> <span data-ttu-id="45c4b-267">En la siguiente figura, DevTools agrega la regla `h1.devsite-page-title` de estilo después de elegir Nueva regla de **estilo**.</span><span class="sxs-lookup"><span data-stu-id="45c4b-267">In the following figure, DevTools adds the `h1.devsite-page-title` style rule after you choose **New Style Rule**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Agregar una nueva regla de estilo" lightbox="../media/css-elements-styles-style-new.msft.png":::
   <span data-ttu-id="45c4b-269">Agregar una nueva regla de estilo</span><span class="sxs-lookup"><span data-stu-id="45c4b-269">Add a new style rule</span></span>  
:::image-end:::  

#### <a name="choose-which-stylesheet-to-add-a-rule-to"></a><span data-ttu-id="45c4b-270">Elegir la hoja de estilos a la que se va a agregar una regla</span><span class="sxs-lookup"><span data-stu-id="45c4b-270">Choose which stylesheet to add a rule to</span></span>  

<span data-ttu-id="45c4b-271">Al [agregar una nueva regla de estilo,](#add-a-style-rule)elija y mantenga presionada nueva regla de estilo **\(** Nueva regla de estilo \) para elegir a qué hoja de estilos agregar la ![ regla de ](../media/new-style-rule-icon.msft.png) estilo.</span><span class="sxs-lookup"><span data-stu-id="45c4b-271">When [adding a new style rule](#add-a-style-rule), choose and hold **New Style Rule** \(![New Style Rule](../media/new-style-rule-icon.msft.png)\) to choose which stylesheet to add the style rule to.</span></span>  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Elegir una hoja de estilos" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   <span data-ttu-id="45c4b-273">Elegir una hoja de estilos</span><span class="sxs-lookup"><span data-stu-id="45c4b-273">Choose a stylesheet</span></span>  
:::image-end:::  

#### <a name="add-a-style-rule-to-a-specific-location"></a><span data-ttu-id="45c4b-274">Agregar una regla de estilo a una ubicación específica</span><span class="sxs-lookup"><span data-stu-id="45c4b-274">Add a style rule to a specific location</span></span>  

<span data-ttu-id="45c4b-275">Complete las siguientes acciones para agregar una regla de estilo a una ubicación específica en el panel **Estilos.**</span><span class="sxs-lookup"><span data-stu-id="45c4b-275">Complete the following actions to add a style rule to a specific location in the **Styles** panel.</span></span>  

1.  <span data-ttu-id="45c4b-276">Mantenga el mouse sobre la regla de estilo que está directamente encima de donde desea agregar la nueva regla de estilo.</span><span class="sxs-lookup"><span data-stu-id="45c4b-276">Hover on the style rule that is directly above where you want to add your new style rule.</span></span>  
1.  <span data-ttu-id="45c4b-277">[Mostrar la **barra de herramientas Más** acciones](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="45c4b-277">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="45c4b-278">Elija **Insertar regla de estilo debajo** \( Insertar regla de estilo ![ debajo del icono ](../media/new-style-rule-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="45c4b-278">Choose **Insert Style Rule Below** \(![Insert Style Rule Below icon](../media/new-style-rule-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Insertar regla de estilo a continuación" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **<span data-ttu-id="45c4b-280">Insertar regla de estilo a continuación</span><span class="sxs-lookup"><span data-stu-id="45c4b-280">Insert Style Rule Below</span></span>**  
:::image-end:::  

### <a name="reveal-the-more-actions-toolbar"></a><span data-ttu-id="45c4b-281">Mostrar la barra de herramientas Más acciones</span><span class="sxs-lookup"><span data-stu-id="45c4b-281">Reveal the More Actions toolbar</span></span>  

<span data-ttu-id="45c4b-282">La **barra de herramientas** Más acciones le permite realizar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="45c4b-282">The **More Actions** toolbar lets you perform the following actions.</span></span>  

*   <span data-ttu-id="45c4b-283">Inserte una regla de estilo directamente debajo de la que está centrado.</span><span class="sxs-lookup"><span data-stu-id="45c4b-283">Insert a style rule directly below the one you are focused on.</span></span>  
*   <span data-ttu-id="45c4b-284">Agregue una , , o declaración a la regla de estilo en la `background-color` `color` que está `box-shadow` `text-shadow` centrado.</span><span class="sxs-lookup"><span data-stu-id="45c4b-284">Add a `background-color`, `color`, `box-shadow`, or `text-shadow` declaration to the style rule you are focused on.</span></span>  

<span data-ttu-id="45c4b-285">Complete las siguientes acciones para mostrar la **barra de herramientas Más** acciones.</span><span class="sxs-lookup"><span data-stu-id="45c4b-285">Complete the following actions to reveal the **More Actions** toolbar.</span></span>  

1.  <span data-ttu-id="45c4b-286">En el panel **Estilos,** mantenga el mouse sobre una regla de estilo.</span><span class="sxs-lookup"><span data-stu-id="45c4b-286">In the **Styles** panel, hover on a style rule.</span></span>  <span data-ttu-id="45c4b-287">**Más acciones** \( `...` \) se muestra en la parte inferior derecha de la sección de regla de estilo.</span><span class="sxs-lookup"><span data-stu-id="45c4b-287">**More Actions** \(`...`\) is revealed in the bottom-right of the style rule section.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="45c4b-288">En la siguiente figura, mantenga el puntero sobre la regla de estilo y Más acciones se muestra en la parte inferior derecha de la sección `.header-holder.has-default-focus` regla de estilo. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="45c4b-288">In the following figure, hover on the `.header-holder.has-default-focus` style rule and **More Actions** is revealed in the bottom-right of the style rule section.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Revelar más acciones" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       <span data-ttu-id="45c4b-290">Mostrar **más acciones** \( `...` \)</span><span class="sxs-lookup"><span data-stu-id="45c4b-290">Reveal **More Actions** \(`...`\)</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45c4b-291">Mantenga el **mouse en Más acciones** \( `...` \) para mostrar las acciones mencionadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="45c4b-291">Hover on **More Actions** \(`...`\) to reveal the actions mentioned above.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="45c4b-292">La **acción Insertar regla de** estilo debajo se muestra después de pasar el puntero sobre Más **acciones**.</span><span class="sxs-lookup"><span data-stu-id="45c4b-292">The **Insert Style Rule Below** action is revealed after hovering over **More Actions**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="La barra de herramientas Más acciones" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       <span data-ttu-id="45c4b-294">La **barra de herramientas Más** acciones</span><span class="sxs-lookup"><span data-stu-id="45c4b-294">The **More Actions** toolbar</span></span>  
    :::image-end:::  
    
### <a name="toggle-a-declaration"></a><span data-ttu-id="45c4b-295">Alternar una declaración</span><span class="sxs-lookup"><span data-stu-id="45c4b-295">Toggle a declaration</span></span>  

<span data-ttu-id="45c4b-296">Complete las acciones de folllwoing para alternar una sola declaración en \(or off\).</span><span class="sxs-lookup"><span data-stu-id="45c4b-296">Complete the folllwoing actions to toggle a single declaration on \(or off\).</span></span>  

1.  <span data-ttu-id="45c4b-297">[Seleccione un elemento](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="45c4b-297">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="45c4b-298">En el **panel Estilos,** mantenga el mouse sobre la regla que define la declaración.</span><span class="sxs-lookup"><span data-stu-id="45c4b-298">In the **Styles** pane, hover on the rule that defines the declaration.</span></span>  <span data-ttu-id="45c4b-299">Aparece una casilla junto a cada declaración.</span><span class="sxs-lookup"><span data-stu-id="45c4b-299">A checkbox appears next to each declaration.</span></span>  
1.  <span data-ttu-id="45c4b-300">Active \(o desactive\) la casilla situada junto a la declaración.</span><span class="sxs-lookup"><span data-stu-id="45c4b-300">Check \(or uncheck\) the checkbox next to the declaration.</span></span>  <span data-ttu-id="45c4b-301">Al desactivar una declaración, DevTools la cruza para indicar que ya no está activa.</span><span class="sxs-lookup"><span data-stu-id="45c4b-301">When you uncheck a declaration, DevTools crosses it out to indicate that it is no longer active.</span></span>  

> [!NOTE]
> <span data-ttu-id="45c4b-302">En la siguiente figura, se ha desactivado la propiedad del elemento `margin-top` seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="45c4b-302">In the following figure, the `margin-top` property for the currently selected element has been toggled off.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Alternar una declaración" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   <span data-ttu-id="45c4b-304">Alternar una declaración</span><span class="sxs-lookup"><span data-stu-id="45c4b-304">Toggle a declaration</span></span>  
:::image-end:::  

### <a name="add-a-background-color-declaration"></a><span data-ttu-id="45c4b-305">Agregar una declaración de color de fondo</span><span class="sxs-lookup"><span data-stu-id="45c4b-305">Add a background-color declaration</span></span>  

<span data-ttu-id="45c4b-306">Complete las siguientes acciones para agregar una declaración a `background-color` un elemento.</span><span class="sxs-lookup"><span data-stu-id="45c4b-306">Complete the following actions to add a `background-color` declaration to an element.</span></span>  

1.  <span data-ttu-id="45c4b-307">Mantenga el mouse sobre la regla de estilo a la que desea agregar `background-color` la declaración.</span><span class="sxs-lookup"><span data-stu-id="45c4b-307">Hover on the style rule that you want to add the `background-color` declaration to.</span></span>  
1.  <span data-ttu-id="45c4b-308">[Mostrar la **barra de herramientas Más** acciones](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="45c4b-308">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="45c4b-309">Elija **Agregar color de fondo** \( Icono Agregar color de fondo ![ ](../media/add-background-color-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="45c4b-309">Choose **Add Background Color** \(![Add Background Color icon](../media/add-background-color-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Agregar color de fondo" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **<span data-ttu-id="45c4b-311">Agregar color de fondo</span><span class="sxs-lookup"><span data-stu-id="45c4b-311">Add Background Color</span></span>**  
:::image-end:::  

### <a name="add-a-color-declaration"></a><span data-ttu-id="45c4b-312">Agregar una declaración de color</span><span class="sxs-lookup"><span data-stu-id="45c4b-312">Add a color declaration</span></span>  

<span data-ttu-id="45c4b-313">Complete las siguientes acciones para agregar una declaración a `color` un elemento.</span><span class="sxs-lookup"><span data-stu-id="45c4b-313">Complete the following actions to add a `color` declaration to an element.</span></span>  

1.  <span data-ttu-id="45c4b-314">Mantenga el mouse sobre la regla de estilo a la que desea agregar `color` la declaración.</span><span class="sxs-lookup"><span data-stu-id="45c4b-314">Hover on the style rule that you want to add the `color` declaration to.</span></span>  
1.  <span data-ttu-id="45c4b-315">[Mostrar la **barra de herramientas Más** acciones](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="45c4b-315">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="45c4b-316">Elija **Agregar color** \( Icono Agregar color ![ ](../media/add-color-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="45c4b-316">Choose **Add Color** \(![Add Color icon](../media/add-color-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Agregar color" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **<span data-ttu-id="45c4b-318">Agregar color</span><span class="sxs-lookup"><span data-stu-id="45c4b-318">Add Color</span></span>**  
:::image-end:::  

### <a name="add-a-box-shadow-declaration"></a><span data-ttu-id="45c4b-319">Agregar una declaración de sombra de cuadro</span><span class="sxs-lookup"><span data-stu-id="45c4b-319">Add a box-shadow declaration</span></span>  

<span data-ttu-id="45c4b-320">Complete las siguientes acciones para agregar una declaración a `box-shadow` un elemento.</span><span class="sxs-lookup"><span data-stu-id="45c4b-320">Complete the follwoing actions to add a `box-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="45c4b-321">Mantenga el mouse sobre la regla de estilo a la que desea agregar `box-shadow` la declaración.</span><span class="sxs-lookup"><span data-stu-id="45c4b-321">Hover on the style rule that you want to add the `box-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="45c4b-322">[Mostrar la **barra de herramientas Más** acciones](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="45c4b-322">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="45c4b-323">Elija **Agregar sombra de cuadro** \( Agregar icono de sombra de cuadro ![ ](../media/add-box-shadow-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="45c4b-323">Choose **Add Box Shadow** \(![Add Box Shadow icon](../media/add-box-shadow-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Agregar sombra de cuadro" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **<span data-ttu-id="45c4b-325">Agregar sombra de cuadro</span><span class="sxs-lookup"><span data-stu-id="45c4b-325">Add Box Shadow</span></span>**  
:::image-end:::  

### <a name="add-a-text-shadow-declaration"></a><span data-ttu-id="45c4b-326">Agregar una declaración de sombra de texto</span><span class="sxs-lookup"><span data-stu-id="45c4b-326">Add a text-shadow declaration</span></span>  

<span data-ttu-id="45c4b-327">Complete las siguientes acciones para agregar una declaración a `text-shadow` un elemento.</span><span class="sxs-lookup"><span data-stu-id="45c4b-327">Complete the following actions to add a `text-shadow` declaration to an element.</span></span>  

1.  <span data-ttu-id="45c4b-328">Mantenga el mouse sobre la regla de estilo a la que desea agregar `text-shadow` la declaración.</span><span class="sxs-lookup"><span data-stu-id="45c4b-328">Hover on the style rule that you want to add the `text-shadow` declaration to.</span></span>  
1.  <span data-ttu-id="45c4b-329">[Mostrar la **barra de herramientas Más** acciones](#reveal-the-more-actions-toolbar).</span><span class="sxs-lookup"><span data-stu-id="45c4b-329">[Reveal the **More Actions** toolbar](#reveal-the-more-actions-toolbar).</span></span>  
1.  <span data-ttu-id="45c4b-330">Elija **Agregar sombra de texto** \( Agregar icono sombra de texto ![ ](../media/add-text-shadow-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="45c4b-330">Choose **Add Text Shadow** \(![Add Text Shadow icon](../media/add-text-shadow-icon.msft.png)\).</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Agregar sombra de texto" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **<span data-ttu-id="45c4b-332">Agregar sombra de texto</span><span class="sxs-lookup"><span data-stu-id="45c4b-332">Add Text Shadow</span></span>**  
:::image-end:::  

### <a name="change-colors-with-the-color-picker"></a><span data-ttu-id="45c4b-333">Cambiar colores con el Selector de colores</span><span class="sxs-lookup"><span data-stu-id="45c4b-333">Change colors with the Color Picker</span></span>  

<span data-ttu-id="45c4b-334">El **selector de colores** proporciona una GUI para cambiar y las `color` `background-color` declaraciones.</span><span class="sxs-lookup"><span data-stu-id="45c4b-334">The **Color Picker** provides a GUI for changing `color` and `background-color` declarations.</span></span>  

<span data-ttu-id="45c4b-335">Complete las siguientes acciones para abrir el **Selector de colores**.</span><span class="sxs-lookup"><span data-stu-id="45c4b-335">Complete the following actions to open the **Color Picker**.</span></span>  

1.  <span data-ttu-id="45c4b-336">[Seleccione un elemento](#choose-an-element).</span><span class="sxs-lookup"><span data-stu-id="45c4b-336">[Select an element](#choose-an-element).</span></span>  
1.  <span data-ttu-id="45c4b-337">En el panel **Estilos,** busque la `color` declaración , o similar que desea `background-color` cambiar.</span><span class="sxs-lookup"><span data-stu-id="45c4b-337">In the **Styles** panel, find the `color`, `background-color`, or similar declaration that you want to change.</span></span>  <span data-ttu-id="45c4b-338">A la izquierda del `color` valor `background-color` , o similar, hay un cuadrado pequeño que es una vista previa del color.</span><span class="sxs-lookup"><span data-stu-id="45c4b-338">To the left of the `color`, `background-color`, or similar value, there is a small square which is a preview of the color.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="45c4b-339">En la siguiente figura, el pequeño cuadrado situado a la izquierda de `rgba(0, 0, 0, 0.7)` es una vista previa de ese color.</span><span class="sxs-lookup"><span data-stu-id="45c4b-339">In the following figure, the small square to the left of `rgba(0, 0, 0, 0.7)` is a preview of that color.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Vista previa del color" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       <span data-ttu-id="45c4b-341">Vista previa del color</span><span class="sxs-lookup"><span data-stu-id="45c4b-341">Color preview</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="45c4b-342">Elija la vista previa para abrir el **Selector de colores**.</span><span class="sxs-lookup"><span data-stu-id="45c4b-342">Choose the preview to open the **Color Picker**.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="Selector de colores" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       <span data-ttu-id="45c4b-344">Selector **de colores**</span><span class="sxs-lookup"><span data-stu-id="45c4b-344">The **Color Picker**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="45c4b-345">La siguiente figura y enumerar descries de cada uno de los elementos de la interfaz de usuario del **Selector de colores**.</span><span class="sxs-lookup"><span data-stu-id="45c4b-345">The following figure and list descries of each of the UI elements of the **Color Picker**.</span></span>  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="Selector de colores, anotado" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   <span data-ttu-id="45c4b-347">Selector **de colores**, anotado</span><span class="sxs-lookup"><span data-stu-id="45c4b-347">The **Color Picker**, annotated</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      <span data-ttu-id="45c4b-348">1</span><span class="sxs-lookup"><span data-stu-id="45c4b-348">1</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="45c4b-349">Sombras</span><span class="sxs-lookup"><span data-stu-id="45c4b-349">Shades</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="45c4b-350">2</span><span class="sxs-lookup"><span data-stu-id="45c4b-350">2</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="45c4b-351">Cuentagotas</span><span class="sxs-lookup"><span data-stu-id="45c4b-351">Eyedropper</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="45c4b-352">Para obtener más información, vaya [a Muestra de un color fuera de la página con cuentagotas](#sample-a-color-off-the-page-with-the-eyedropper).</span><span class="sxs-lookup"><span data-stu-id="45c4b-352">For more information, navigate to [Sample a color off the page with the Eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="45c4b-353">3</span><span class="sxs-lookup"><span data-stu-id="45c4b-353">3</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="45c4b-354">Copiar en el portapapeles</span><span class="sxs-lookup"><span data-stu-id="45c4b-354">Copy To Clipboard</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="45c4b-355">Copie el **valor para mostrar** en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="45c4b-355">Copy the **Display Value** to your clipboard.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="45c4b-356">4</span><span class="sxs-lookup"><span data-stu-id="45c4b-356">4</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="45c4b-357">Valor para mostrar</span><span class="sxs-lookup"><span data-stu-id="45c4b-357">Display Value</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="45c4b-358">La representación RGBA, HSLA o Hexadecimal del color.</span><span class="sxs-lookup"><span data-stu-id="45c4b-358">The RGBA, HSLA, or Hex representation of the color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="45c4b-359">5</span><span class="sxs-lookup"><span data-stu-id="45c4b-359">5</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="45c4b-360">Paleta de colores</span><span class="sxs-lookup"><span data-stu-id="45c4b-360">Color Palette</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="45c4b-361">Elija uno de los cuadrados para cambiar el color a ese cuadrado.</span><span class="sxs-lookup"><span data-stu-id="45c4b-361">Choose one of the squares to change the color to that square.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="45c4b-362">6</span><span class="sxs-lookup"><span data-stu-id="45c4b-362">6</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="45c4b-363">Tono</span><span class="sxs-lookup"><span data-stu-id="45c4b-363">Hue</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="45c4b-364">7</span><span class="sxs-lookup"><span data-stu-id="45c4b-364">7</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="45c4b-365">Opacity</span><span class="sxs-lookup"><span data-stu-id="45c4b-365">Opacity</span></span>**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="45c4b-366">8</span><span class="sxs-lookup"><span data-stu-id="45c4b-366">8</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="45c4b-367">Modificador de valor para mostrar</span><span class="sxs-lookup"><span data-stu-id="45c4b-367">Display Value Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="45c4b-368">Alterna entre las representaciones RGBA, HSLA y Hex del color actual.</span><span class="sxs-lookup"><span data-stu-id="45c4b-368">Toggle between the RGBA, HSLA, and Hex representations of the current color.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="45c4b-369">9</span><span class="sxs-lookup"><span data-stu-id="45c4b-369">9</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="45c4b-370">Conmutador de paleta de colores</span><span class="sxs-lookup"><span data-stu-id="45c4b-370">Color Palette Switcher</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="45c4b-371">Alterna entre la paleta [Diseño de materiales,][MaterialDesignColorSystem]una paleta personalizada o una paleta de colores de página.</span><span class="sxs-lookup"><span data-stu-id="45c4b-371">Toggle between the [Material Design palette][MaterialDesignColorSystem], a custom palette, or a page colors palette.</span></span>  <span data-ttu-id="45c4b-372">DevTools genera la paleta de colores de página en función de los colores que encuentre en las hojas de estilos.</span><span class="sxs-lookup"><span data-stu-id="45c4b-372">DevTools generates the page color palette based on the colors that it finds in your stylesheets.</span></span>  
   :::column-end:::
:::row-end:::  

#### <a name="sample-a-color-off-the-page-with-the-eyedropper"></a><span data-ttu-id="45c4b-373">Muestrear un color fuera de la página con el cuentagotas</span><span class="sxs-lookup"><span data-stu-id="45c4b-373">Sample a color off the page with the Eyedropper</span></span>  

<span data-ttu-id="45c4b-374">Al abrir el **Selector de colores**, el **cuentagotas** \( Cuentagotas ![ ](../media/eyedropper-icon.msft.png) \) está en la opción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="45c4b-374">When you open the **Color Picker**, the **Eyedropper** \(![Eyedropper](../media/eyedropper-icon.msft.png)\) is on by default.</span></span>  <span data-ttu-id="45c4b-375">Complete las siguientes acciones para cambiar el color seleccionado a otro color de la página.</span><span class="sxs-lookup"><span data-stu-id="45c4b-375">Complete the following actions to change the selected color to some other color on the page.</span></span>  

1.  <span data-ttu-id="45c4b-376">Mantenga el mouse sobre el color de destino en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="45c4b-376">Hover on the target color in the viewport.</span></span>  
1.  <span data-ttu-id="45c4b-377">Elija confirmar.</span><span class="sxs-lookup"><span data-stu-id="45c4b-377">Choose to confirm.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="45c4b-378">En la siguiente figura, el **Selector** de colores muestra un valor de color actual de `rgba(0,0,0,0.7)` , que está cerca del negro.</span><span class="sxs-lookup"><span data-stu-id="45c4b-378">In the following figure, the **Color Picker** shows a current color value of `rgba(0,0,0,0.7)`, which is close to black.</span></span>  <span data-ttu-id="45c4b-379">El color específico debe cambiar a la versión de negro que está resaltada actualmente en la ventanilla después de elegirlo.</span><span class="sxs-lookup"><span data-stu-id="45c4b-379">The specific color should change to the version of black that is currently highlighted in the viewport after you chose it.</span></span>  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Uso del cuentagotas" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       <span data-ttu-id="45c4b-381">Uso del cuentagotas</span><span class="sxs-lookup"><span data-stu-id="45c4b-381">Using the Eyedropper</span></span>  
    :::image-end:::  
    
<!--todo:  add the section on the Angle clock section for What's New 88.  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="45c4b-382">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="45c4b-382">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ejecutar comandos con el Microsoft Edge de comandos DevTools | Microsoft Docs"  
[DevToolsCSSGetStarted]: ../css/index.md "Introducción Con vista y cambio de CSS | Microsoft Docs"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Agregar un pseudoestado a una clase: Introducción Con ver y cambiar css | Microsoft Docs"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Ver el CSS de un elemento: Introducción ver y cambiar css | Microsoft Docs"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Forzar Microsoft Edge DevTools al modo de vista previa de impresión (tipo de medios de impresión CSS) | Microsoft Docs"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#reformat-a-minified-javascript-file-with-pretty-print "Volver a formatear un archivo JavaScript minificado con pretty-print: use el depurador | Microsoft Docs"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "El sistema de colores: diseño de material"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "El modelo de cuadro | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Tipos de selector: especificación | MDN"  

> [!NOTE]
> <span data-ttu-id="45c4b-392">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="45c4b-392">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="45c4b-393">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/css/reference) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="45c4b-393">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/css/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="45c4b-395">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="45c4b-395">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
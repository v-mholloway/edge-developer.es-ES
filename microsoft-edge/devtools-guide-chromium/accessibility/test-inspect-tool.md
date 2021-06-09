---
description: Use la herramienta Inspeccionar para detectar problemas de accesibilidad al pasar el mouse sobre la página web.
title: Usar la herramienta Inspeccionar para detectar problemas de accesibilidad al pasar el puntero sobre la página web
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: c95116d38e5b0bda88af43ef8bfde4204b8cb372
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597660"
---
# <a name="use-the-inspect-tool-to-detect-accessibility-issues-by-hovering-over-the-webpage"></a><span data-ttu-id="3ce76-104">Usar la herramienta Inspeccionar para detectar problemas de accesibilidad al pasar el puntero sobre la página web</span><span class="sxs-lookup"><span data-stu-id="3ce76-104">Use the Inspect tool to detect accessibility issues by hovering over the webpage</span></span>

<span data-ttu-id="3ce76-105">La **herramienta Inspeccionar** muestra información sobre los elementos individuales al pasar el puntero sobre la página web que se representa, incluida la información de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="3ce76-105">The **Inspect** tool displays information about individual elements as you hover over the rendered webpage, including accessibility information.</span></span>
<span data-ttu-id="3ce76-106">En cambio, la **herramienta Problemas** notifica automáticamente los problemas de toda la página web.</span><span class="sxs-lookup"><span data-stu-id="3ce76-106">In contrast, the **Issues** tool automatically reports issues for the entire webpage.</span></span>

<span data-ttu-id="3ce76-107">El **botón de** la herramienta Inspeccionar \( Inspect \) se encuentra en la esquina superior izquierda de ![ ](../media/inspect-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="3ce76-107">The **Inspect** tool button \(![Inspect](../media/inspect-icon.msft.png)\) is in the upper-left corner of DevTools.</span></span>  <span data-ttu-id="3ce76-108">Al seleccionar el botón **Inspeccionar** herramienta, el botón se vuelve azul, lo que indica que **la herramienta Inspeccionar** está activa.</span><span class="sxs-lookup"><span data-stu-id="3ce76-108">When you select the **Inspect** tool button, the button turns blue, indicating that the **Inspect** tool is active.</span></span>

<span data-ttu-id="3ce76-109">Cuando la **herramienta Inspeccionar** está activa, al mantener el mouse sobre cualquier elemento de la página web representada, se muestra **la superposición Inspeccionar.**</span><span class="sxs-lookup"><span data-stu-id="3ce76-109">When the **Inspect** tool is active, hovering over any element on the rendered webpage displays the **Inspect** overlay.</span></span> <span data-ttu-id="3ce76-110">Esta superposición muestra información general e información de accesibilidad sobre ese elemento.</span><span class="sxs-lookup"><span data-stu-id="3ce76-110">This overlay displays general information and accessibility information about that element.</span></span>  <span data-ttu-id="3ce76-111">La **sección Accesibilidad** de la superposición **Inspeccionar** muestra información sobre el contraste de color de texto, el texto del lector de pantalla y la compatibilidad con el teclado.</span><span class="sxs-lookup"><span data-stu-id="3ce76-111">The **Accessibility** section of the **Inspect** overlay displays information about text-color contrast, screen reader text, and keyboard support.</span></span>

:::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="La herramienta Inspeccionar, que muestra el área del elemento como una superposición multicolor y muestra los detalles del elemento como una superposición de información grande" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
    <span data-ttu-id="3ce76-113">La **herramienta Inspeccionar,** que muestra el área del elemento como una superposición multicolor y muestra los detalles del elemento como una superposición de información grande</span><span class="sxs-lookup"><span data-stu-id="3ce76-113">The **Inspect** tool, showing the element's area as a multicolor overlay, and showing the element's details as a large information overlay</span></span>
:::image-end:::


## <a name="check-individual-elements-for-text-contrast-screen-reader-text-and-keyboard-support"></a><span data-ttu-id="3ce76-114">Comprobar los elementos individuales para el contraste de texto, el texto del lector de pantalla y la compatibilidad con el teclado</span><span class="sxs-lookup"><span data-stu-id="3ce76-114">Check individual elements for text contrast, screen reader text, and keyboard support</span></span>

<!-- Inspect tool: Accessibility section of overlay -->

1.  <span data-ttu-id="3ce76-115">Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="3ce76-115">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="3ce76-116">Seleccione el **botón Inspeccionar** \( Inspeccionar \) en la esquina superior izquierda de DevTools para que el icono esté ![ resaltado ](../media/inspect-icon.msft.png) (azul).</span><span class="sxs-lookup"><span data-stu-id="3ce76-116">Select the **Inspect** \(![Inspect](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the icon is highlighted (blue).</span></span>

    :::image type="complex" source="../media/a11y-testing-basics-inspector.msft.png" alt-text="Para activar la herramienta Inspeccionar, seleccione el botón Inspeccionar" lightbox="../media/a11y-testing-basics-inspector.msft.png":::
        <span data-ttu-id="3ce76-118">Para activar la herramienta **Inspeccionar,** seleccione el **botón Inspeccionar**</span><span class="sxs-lookup"><span data-stu-id="3ce76-118">To turn on the **Inspect** tool, select the **Inspect** button</span></span>
    :::image-end:::

1.  <span data-ttu-id="3ce76-119">Mantenga el mouse sobre cualquier elemento de la página web de demostración que se represente.</span><span class="sxs-lookup"><span data-stu-id="3ce76-119">Hover over any element in the rendered demo webpage.</span></span>  <span data-ttu-id="3ce76-120">La **herramienta Inspeccionar** muestra una superposición de información debajo del elemento dentro de la página web representada.</span><span class="sxs-lookup"><span data-stu-id="3ce76-120">The **Inspect** tool shows an information overlay below the element within the rendered webpage.</span></span>

    :::image type="complex" source="../media/a11y-testing-basics-inspector-overlay.msft.png" alt-text="La herramienta Inspeccionar, que muestra el diseño del elemento como una superposición multicolor y muestra los detalles del elemento como una superposición de información grande" lightbox="../media/a11y-testing-basics-inspector-overlay.msft.png":::
        <span data-ttu-id="3ce76-122">La **herramienta Inspeccionar,** que muestra el diseño del elemento como una superposición multicolor y muestra los detalles del elemento como una superposición de información grande</span><span class="sxs-lookup"><span data-stu-id="3ce76-122">The **Inspect** tool, showing the element's layout as a multicolor overlay, and showing the element's details as a large information overlay</span></span>
    :::image-end:::

<span data-ttu-id="3ce76-123">La parte inferior de la **superposición Inspeccionar** tiene **una sección Accesibilidad** que contiene la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="3ce76-123">The bottom part of the **Inspect** overlay has an **Accessibility** section that contains the following information:</span></span>

*   <span data-ttu-id="3ce76-124">**El** contraste define si un elemento puede ser comprendido por personas con visión baja.</span><span class="sxs-lookup"><span data-stu-id="3ce76-124">**Contrast** defines whether an element can be understood by people with low vision.</span></span>  <span data-ttu-id="3ce76-125">La [relación de contraste][W3CContrastRatio] definida por las Directrices de [WCAG][WCAG] indica si hay suficiente contraste (un icono de marca de verificación verde) o no suficiente (icono de signo de exclamación naranja).</span><span class="sxs-lookup"><span data-stu-id="3ce76-125">The [contrast ratio][W3CContrastRatio] as defined by the [WCAG Guidelines][WCAG] indicates whether there is enough contrast (a green check mark icon) or not enough (an orange exclamation-point icon).</span></span>

*   <span data-ttu-id="3ce76-126">**Name** y **Role** son los elementos que la tecnología de asistencia, como los lectores de pantalla, informarán sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="3ce76-126">**Name** and **Role** are what assistive technology such as screen readers will report about the element.</span></span>
    *   <span data-ttu-id="3ce76-127">Name **es** el contenido de texto de un `a` elemento.</span><span class="sxs-lookup"><span data-stu-id="3ce76-127">The **Name** is the text content of an `a` element.</span></span>  <span data-ttu-id="3ce76-128">Para el elemento `<a href="/">About Us</a>` , el nombre **que** se muestra en la herramienta Inspeccionar es "Acerca de nosotros".</span><span class="sxs-lookup"><span data-stu-id="3ce76-128">For the element `<a href="/">About Us</a>`, the **Name** shown in the Inspect tool is "About Us".</span></span>
    *   <span data-ttu-id="3ce76-129">Role \*\*\*\* del elemento.</span><span class="sxs-lookup"><span data-stu-id="3ce76-129">The **Role** of the element.</span></span>  <span data-ttu-id="3ce76-130">Este suele ser el nombre del elemento, como `article` , `img` , o `link` `heading` .</span><span class="sxs-lookup"><span data-stu-id="3ce76-130">This is usually the element name, such as `article`, `img` , `link`, or `heading`.</span></span>  <span data-ttu-id="3ce76-131">Los `div` elementos y se `span` `generic` denominan .</span><span class="sxs-lookup"><span data-stu-id="3ce76-131">The `div` and `span` elements are referred to as `generic`.</span></span>

*   <span data-ttu-id="3ce76-132">**El enfoque de teclado** indica si los usuarios pueden llegar al elemento independientemente del dispositivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="3ce76-132">**Keyboard-focusable** indicates whether users can reach the element regardless of input device.</span></span>
    *   <span data-ttu-id="3ce76-133">Un icono de marca de verificación verde indica que el elemento se puede centrar en el teclado.</span><span class="sxs-lookup"><span data-stu-id="3ce76-133">A green check mark icon indicates that the element is keyboard-focusable.</span></span>
    *   <span data-ttu-id="3ce76-134">Un círculo gris con línea diagonal indica que el elemento no se puede centrar en el teclado.</span><span class="sxs-lookup"><span data-stu-id="3ce76-134">A gray circle with diagonal line indicates that the element isn't keyboard-focusable.</span></span>


## <a name="additional-information-in-the-inspect-overlay"></a><span data-ttu-id="3ce76-135">Información adicional en la superposición Inspeccionar</span><span class="sxs-lookup"><span data-stu-id="3ce76-135">Additional information in the Inspect overlay</span></span>

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

<span data-ttu-id="3ce76-136">La parte superior de la **superposición Inspeccionar,** que está encima de la sección **Accesibilidad,** enumera los siguientes detalles del elemento.</span><span class="sxs-lookup"><span data-stu-id="3ce76-136">The top part of the **Inspect** overlay, which is above the **Accessibility** section, lists the following details of the element.</span></span>

*   <span data-ttu-id="3ce76-137">Tipo de diseño.</span><span class="sxs-lookup"><span data-stu-id="3ce76-137">Layout type.</span></span> <span data-ttu-id="3ce76-138">Si el elemento se coloca mediante un flexbox o una cuadrícula, un icono \(</span><span class="sxs-lookup"><span data-stu-id="3ce76-138">If the element is positioned using a flexbox or grid, an icon \(</span></span>![Icono de diseño de cuadrícula](../media/grid-icon.msft.png)<span data-ttu-id="3ce76-140">\) se muestra.</span><span class="sxs-lookup"><span data-stu-id="3ce76-140">\) is displayed.</span></span>
*   <span data-ttu-id="3ce76-141">Nombre del elemento, como `h1` , `h2` o `div` .</span><span class="sxs-lookup"><span data-stu-id="3ce76-141">Name of the element, such as `h1`, `h2`, or `div`.</span></span>
*   <span data-ttu-id="3ce76-142">Dimensiones del elemento en píxeles.</span><span class="sxs-lookup"><span data-stu-id="3ce76-142">The dimensions of the element in pixels.</span></span>
*   <span data-ttu-id="3ce76-143">El color como una muestra de color (o un cuadrado pequeño y coloreado) y como una cadena (como `#336699` ).</span><span class="sxs-lookup"><span data-stu-id="3ce76-143">The color as a color swatch (or a small, colored square) and as a string (such as `#336699`).</span></span>
*   <span data-ttu-id="3ce76-144">Información de fuentes, como el tamaño y las familias de fuentes.</span><span class="sxs-lookup"><span data-stu-id="3ce76-144">Font information, such as size and font families.</span></span>
*   <span data-ttu-id="3ce76-145">Margen y relleno en píxeles.</span><span class="sxs-lookup"><span data-stu-id="3ce76-145">Margin and padding in pixels.</span></span>


## <a name="identify-nested-regions-using-color-highlighting"></a><span data-ttu-id="3ce76-146">Identificar regiones anidadas mediante resaltado de color</span><span class="sxs-lookup"><span data-stu-id="3ce76-146">Identify nested regions using color highlighting</span></span> 

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

<span data-ttu-id="3ce76-147">Además de la superposición de información, la herramienta **Inspeccionar** también proporciona un color de región similar al mantener el mouse en el árbol DOM de la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="3ce76-147">In addition to the information overlay, the **Inspect** tool also provides region-coloring that's similar to hovering in the DOM tree in the **Elements** tool.</span></span>

1.  <span data-ttu-id="3ce76-148">Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="3ce76-148">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="3ce76-149">Seleccione el **botón Inspeccionar** \( Icono de la herramienta Inspeccionar \) en la esquina superior izquierda ![ de DevTools, de modo que el botón esté resaltado ](../media/inspect-icon.msft.png) (azul).</span><span class="sxs-lookup"><span data-stu-id="3ce76-149">Select the **Inspect** button \(![Inspect tool icon](../media/inspect-icon.msft.png)\) in the top-left corner of DevTools, so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="3ce76-150">Mantenga el mouse sobre diferentes partes de la página web de demostración representado.</span><span class="sxs-lookup"><span data-stu-id="3ce76-150">Hover over different parts of the rendered demo webpage.</span></span>  <span data-ttu-id="3ce76-151">Cada elemento de la página web ahora se muestra con una superposición multicolor.</span><span class="sxs-lookup"><span data-stu-id="3ce76-151">Each element in the webpage now displays with a multicolor overlay.</span></span> <span data-ttu-id="3ce76-152">Esta superposición multicolor puede mostrar regiones anidadas dentro de un elemento.</span><span class="sxs-lookup"><span data-stu-id="3ce76-152">This multicolor overlay can display nested regions inside of an element.</span></span> <span data-ttu-id="3ce76-153">Por ejemplo, mantenga el mouse sobre el margen izquierdo de **Gatos**.</span><span class="sxs-lookup"><span data-stu-id="3ce76-153">For example, hover over the left margin of **Cats**.</span></span>  <span data-ttu-id="3ce76-154">La **herramienta Inspeccionar** resalta varias partes \*\*\*\* rectangulares de la sección Gatos con diferentes colores, que muestran el diseño que resulta de las definiciones de flexbox CSS en la página web.</span><span class="sxs-lookup"><span data-stu-id="3ce76-154">The **Inspect** tool highlights several rectangular portions of the **Cats** section with different colors, showing the layout that results from the CSS flexbox definitions on your webpage.</span></span>

:::image type="complex" source="../media/inspect-tool-flexbox-overlay.msft.png" alt-text="Superposición de flexbox multicolor y superposición de información al usar la herramienta Inspeccionar" lightbox="../media/inspect-tool-flexbox-overlay.msft.png":::
    <span data-ttu-id="3ce76-156">Superposición de flexbox multicolor y superposición de información al usar **la herramienta Inspeccionar**</span><span class="sxs-lookup"><span data-stu-id="3ce76-156">Multicolor flexbox overlay and information overlay when using the **Inspect** tool</span></span>
:::image-end:::

<span data-ttu-id="3ce76-157">Para configurar la superposición de cuadrícula o la superposición de flexbox, en la **herramienta Elementos,** seleccione la **pestaña** Diseño.  Para obtener más información, vaya a [Inspeccionar cuadrícula CSS](..\css\grid.md).</span><span class="sxs-lookup"><span data-stu-id="3ce76-157">To configure the grid overlay or flexbox overlay, in the **Elements** tool, select the **Layout** tab.  For more information, navigate to [Inspect CSS Grid](..\css\grid.md).</span></span>


## <a name="use-the-inspect-tool-to-hover-over-the-webpage-to-highlight-the-dom-and-css"></a><span data-ttu-id="3ce76-158">Usar la herramienta Inspeccionar para pasar el puntero sobre la página web para resaltar el DOM y CSS</span><span class="sxs-lookup"><span data-stu-id="3ce76-158">Use the Inspect tool to hover over the webpage to highlight the DOM and CSS</span></span>

<!-- general info about the Inspect tool, not particularly focused on accessibility -->

1.  <span data-ttu-id="3ce76-159">Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="3ce76-159">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="3ce76-160">Seleccione el **botón Inspeccionar** \( la herramienta Inspeccionar \) en la esquina superior izquierda ![ de DevTools, de modo que el botón esté ](../media/inspect-icon.msft.png) resaltado (azul).</span><span class="sxs-lookup"><span data-stu-id="3ce76-160">Select the **Inspect** button \(![the Inspect tool](../media/inspect-icon.msft.png)\) in the top-left corner of DevTools, so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="3ce76-161">Seleccione la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="3ce76-161">Select the **Elements** tool.</span></span>

1.  <span data-ttu-id="3ce76-162">Con la **herramienta Inspeccionar** activa, mantenga el puntero sobre distintas partes de la página web que se representa.</span><span class="sxs-lookup"><span data-stu-id="3ce76-162">With the **Inspect** tool active, hover over different parts of the rendered webpage.</span></span>  <span data-ttu-id="3ce76-163">En la **herramienta Elementos,** el árbol DOM HTML se expande automáticamente para mostrar información sobre el elemento sobre el que se mueve el mouse.</span><span class="sxs-lookup"><span data-stu-id="3ce76-163">In the **Elements** tool, the HTML DOM tree automatically expands to show information about the element you hover over.</span></span>  <span data-ttu-id="3ce76-164">Si se mantiene el mouse, el panel **Estilos no** se actualiza.</span><span class="sxs-lookup"><span data-stu-id="3ce76-164">Hovering doesn't cause the **Styles** pane to update.</span></span>

1.  <span data-ttu-id="3ce76-165">Ahora seleccione cualquier elemento dentro de la página web que se represente.</span><span class="sxs-lookup"><span data-stu-id="3ce76-165">Now select any element within the rendered webpage.</span></span>  <span data-ttu-id="3ce76-166">La **herramienta Elementos** se abre automáticamente y muestra el CÓDIGO HTML del elemento en el árbol DOM.</span><span class="sxs-lookup"><span data-stu-id="3ce76-166">The **Elements** tool automatically opens and displays the HTML of the element in the DOM tree.</span></span> <span data-ttu-id="3ce76-167">La herramienta también muestra el CSS aplicado en el elemento del **panel Estilos.**</span><span class="sxs-lookup"><span data-stu-id="3ce76-167">The tool also displays the applied CSS on the element in the **Styles** pane.</span></span>  <span data-ttu-id="3ce76-168">Al seleccionar un elemento en la página web que se representa, se desactiva la **herramienta Inspeccionar.**</span><span class="sxs-lookup"><span data-stu-id="3ce76-168">Selecting an element on the rendered webpage turns off the **Inspect** tool.</span></span>

:::image type="complex" source="../media/a11y-testing-basics-inspector-selected-element.msft.png" alt-text="Los detalles sobre el elemento seleccionado se muestran en la herramienta Elementos" lightbox="../media/a11y-testing-basics-inspector-selected-element.msft.png":::
    <span data-ttu-id="3ce76-170">Los detalles sobre el elemento seleccionado se muestran en la **herramienta** Elementos</span><span class="sxs-lookup"><span data-stu-id="3ce76-170">Details about the selected element are displayed in the **Elements** tool</span></span>
:::image-end:::

<span data-ttu-id="3ce76-171">Después de seleccionar un elemento en la página representada, puede \*\*\*\* usar la pestaña \*\*\*\* Accesibilidad (cerca de la pestaña Estilos) para ver el árbol de accesibilidad y usar el Visor de pedidos **de origen**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3ce76-171">After selecting an element in the rendered page, you could then use the **Accessibility** tab (near the **Styles** tab) to view the **Accessibility Tree** and use the **Source Order Viewer**.</span></span>


## <a name="see-also"></a><span data-ttu-id="3ce76-172">Consulta también</span><span class="sxs-lookup"><span data-stu-id="3ce76-172">See also</span></span>

*  [<span data-ttu-id="3ce76-173">Inspeccionar un nodo</span><span class="sxs-lookup"><span data-stu-id="3ce76-173">Inspect a node</span></span>](../dom/index.md#inspect-a-node)
*  [<span data-ttu-id="3ce76-174">Comprobar el contraste de color de texto en el estado predeterminado con la herramienta Inspeccionar</span><span class="sxs-lookup"><span data-stu-id="3ce76-174">Check text-color contrast in the default state using the Inspect tool</span></span>](test-inspect-text-contrast.md)
*  [<span data-ttu-id="3ce76-175">Información general sobre las pruebas de accesibilidad con DevTools</span><span class="sxs-lookup"><span data-stu-id="3ce76-175">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="3ce76-176">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3ce76-176">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"
[W3CContrastRatio]: https://www.w3.org/TR/WCAG21/#dfn-contrast-ratio "relación de contraste | W3C"
[WCAG]: https://www.w3.org/TR/WCAG21/ "Directrices de accesibilidad de contenido web | W3C"
